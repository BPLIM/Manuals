---
title: Guide to Using Parquet Files with Stata
author: BPLIM
date: 23 January 2025
format:
  pdf:
    documentclass: scrartcl
    papersize: A4
    toc: true
    toc-title: Contents
    toc-depth: 3
  html:
    embed-resources: true
    toc: true
    toc-location: left
    html-math-method: katex
    code-copy: true
jupyter:
  kernelspec:
    display_name: Stata (nbstata)
    language: stata
    name: nbstata
---

## 1. What is Parquet?

Parquet is an open-source file format designed for efficient data storage and retrieval.   
Parquet is particularly useful when working with large datasets because it offers faster read times and significantly reduced file sizes compared to *.dta* files.[^1] The **stata-parquet-io** package, developed by John Rothbaum, allows you to efficiently handle Parquet files directly in Stata. 

For installation instructions, visit the **stata-parquet-io** package [GitHub](https://github.com/jrothbaum/stata_parquet_io) page and consult the help files with `help pq` for more information. Make sure you are using the latest version of the package (version 1.9.1 as of this date). This package is already available in BPLIM containers. 

This guide includes example usage of `pq` and does not replace the pq documentation. Please refer to the stata-parquet-io [GitHub](https://github.com/jrothbaum/stata_parquet_io) page for full details.

[^1]: All examples in this guide used Stata version 19.5. 

## 2. Key Features of Parquet

### 2.1. Store Layout and Predicate Pushdown   
In Stata, the system first retrieves all data from the data source and then applies the filtering conditions during processing, even when using the `if()` option in the `use` command. This means that all the data, including irrelevant rows and columns, must be transferred and processed, which can be inefficient for large datasets.    
However, Parquet uses columnar storage with row groups, meaning that data is stored in column chunks. This structure allows filtering to occur at the data source, transferring and processing only the rows that satisfy the condition and the selected columns. This results in **faster reads and more efficient queries**. 

### 2.2. Efficient Data Storage     
Parquet uses two main encoding types that help compress data, reducing the memory footprint of the file. The first is **dictionary encoding**, in which Parquet creates a dictionary of unique column values and replaces them with compact integer references from the dictionary. The second is **run-length encoding (RLE)**. When a column contains many repeated values, Parquet stores each run as a pair of value-count, further reducing storage needs.      
Additionally, Parquet also supports multiple **compression algorithms** that significantly reduce data size.   

### 2.3. Partitioning    
Parquet allows large files to be divided into smaller chunks, which involves **dividing data into subdirectories** based on the values of one or more columns.   
The main advantage is that if queries involve the partitioning columns, Parquet can skip reading entire directories that don't match the filter conditions, leading to faster query performance. This minimizes the amount of data read from disk, reduces I/O operations, and keeps data well organized.

## 3. Advantages of Parquet   
Considering the key features of Parquet explained above, the **main advantages** of Parquet are:   

- Parquet is an open-source format;
- Thanks to its hybrid storage layout and partitioning, Parquet supports fast read operations;
- Parquet provides efficient data compression, reducing storage requirements both in memory and on disk;   
- Parquet is compatible with multiple languages and tools, including Python, R, Julia, Stata and many processing frameworks.

## 4. How to handle Parquet files in Stata?

The Stata user-written command `pq` (**stata-parquet-io** package) allows to describe, use, save, merge and append Parquet files. There is also an official Stata command `import parquet`, but it is less flexible.

### 4.1 Describe Parquet Files in Stata - `pq describe`

To describe Parquet files in Stata use the subcommand **pq describe**:    

`pq describe using filename`   

This subcommand describes the content of a Parquet file and lists the available variables, even before using the dataset.      

Before reading a Parquet file, it is a good practice to use this subcommand to know the structure of the file and define the variables to be used next. However, be aware that a major limitation of Parquet files is that they do not preserve the metadata (value labels, variable labels, variable formats, etc.) meaning that the `pq describe` subcommand only shows the variable name and type. BPLIM always makes complete metadata files available (*metaxl* files) along with the Parquet data files. 

##### **Example 1**

```{stata}
*| output: false
*| echo: false
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T17:35:47.649273Z', iopub.status.busy: '2026-01-22T17:35:47.649040Z', iopub.status.idle: '2026-01-22T17:35:48.372868Z', shell.execute_reply: '2026-01-22T17:35:48.372307Z', shell.execute_reply.started: '2026-01-22T17:35:47.649242Z'}

global examples = "/mnt/cephfs/colaborativo/DEE-BPLIM/data/projects/parquet/examples"
global output = "/mnt/cephfs/colaborativo/DEE-BPLIM/data/projects/parquet/outputs"

adopath ++ /usr/local/stata/ado/plus
adopath ++ /mnt/cephfs/colaborativo/DEE-BPLIM/data/projects/parquet/ados/
```

The dataset **panel_GR_2010_2018.dta** is used as an illustrative example to compare the use and performance of *.dta* and *.parquet* files. In this example, the associated metadata file is named "META_PANEL_GR.xlsx". This comparison depends on the complexity, size, and structure of the data, meaning that performance may vary. Each observation is uniquely identified by the combination of worker (variable *niss_ps_encrip*), firm (variable *tina_ee*), and month (variable *cod_mes*). This dataset contains more than 775 million observations between January 2010 and December 2018, and the corresponding *.dta* file size is 30.3 GB.   

```{stata}
*| output: false
*| echo: false
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T17:35:48.373911Z', iopub.status.busy: '2026-01-22T17:35:48.373542Z', iopub.status.idle: '2026-01-22T17:35:48.408201Z', shell.execute_reply: '2026-01-22T17:35:48.407565Z', shell.execute_reply.started: '2026-01-22T17:35:48.373882Z'}

cd ${examples}
```

For the *.dta* dataset:

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T17:35:48.409115Z', iopub.status.busy: '2026-01-22T17:35:48.408886Z', iopub.status.idle: '2026-01-22T17:35:48.488616Z', shell.execute_reply: '2026-01-22T17:35:48.488052Z', shell.execute_reply.started: '2026-01-22T17:35:48.409091Z'}
describe using "panel_GR_2010_2018.dta"
```

For the same dataset in *.parquet*:

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T17:35:48.489534Z', iopub.status.busy: '2026-01-22T17:35:48.489300Z', iopub.status.idle: '2026-01-22T17:35:49.882611Z', shell.execute_reply: '2026-01-22T17:35:49.881961Z', shell.execute_reply.started: '2026-01-22T17:35:48.489509Z'}
pq describe using "panel_GR_2010_2018.parquet"
```

### 4.2 Read Parquet Files in Stata - `pq use`

To import Parquet files into Stata use the subcommand **pq use**: 

`pq use using filename`
 
The subcommand also allows to:   

- Select the variables that you want to import into Stata;   
- Specify a subset of rows to read (*in* option);
- Import only the rows that satisfy a specified condition (*if* option);
- Sort the data by specified variables during the read operation (*sort* option);
- Read data concurrently and improve efficiency (*parallelize* option). For tall datasets (many rows) use *parallelize(rows)* and for wide datasets (many columns) use *parallelize(columns)*.

As mentioned before, Parquet files do not preserve the metadata. To overcome this limitation, BPLIM `metaxl` tool can be used after importing the data into Stata. The `metaxl` package provides multiple solutions to help users handle metadata and is available on [BPLIM's GitHub](https://github.com/BPLIM/Tools/tree/master/ados/General/metaxl) and all BPLIM containers. The subcommand `metaxl apply` applies metadata saved in an Excel file to the data in memory. For more information, please consult the help files. 

#### Examples

##### **Example 2: Reading a complete dataset**

For the *.dta* dataset:

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T17:35:49.883588Z', iopub.status.busy: '2026-01-22T17:35:49.883350Z', iopub.status.idle: '2026-01-22T17:38:41.229667Z', shell.execute_reply: '2026-01-22T17:38:41.228848Z', shell.execute_reply.started: '2026-01-22T17:35:49.883564Z'}
use "panel_GR_2010_2018.dta", clear
count
```

For the same dataset in *.parquet*:

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T17:38:41.232009Z', iopub.status.busy: '2026-01-22T17:38:41.231777Z', iopub.status.idle: '2026-01-22T17:41:48.439255Z', shell.execute_reply: '2026-01-22T17:41:48.438450Z', shell.execute_reply.started: '2026-01-22T17:38:41.231984Z'}
pq use using "panel_GR_2010_2018.parquet", clear
count
```

<img src="./images/lampada.png" width="20"/> In this example, reading either the *.dta* or *.parquet* dataset takes roughly the same amount of time (approximately 2 minutes).

##### **Example 3: Reading a set of variables**

In most cases, we do not need to use the entire dataset; reading only a small subset of variables is sufficient.    
For the *.dta* dataset:

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T17:41:48.440186Z', iopub.status.busy: '2026-01-22T17:41:48.439962Z', iopub.status.idle: '2026-01-22T17:44:37.524564Z', shell.execute_reply: '2026-01-22T17:44:37.523859Z', shell.execute_reply.started: '2026-01-22T17:41:48.440163Z'}
use cod_mes niss_ps_encrip tina_ee val_remun using "panel_GR_2010_2018.dta", clear
count
```

For the same dataset in *.parquet*:

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T17:44:37.525550Z', iopub.status.busy: '2026-01-22T17:44:37.525298Z', iopub.status.idle: '2026-01-22T17:45:50.068755Z', shell.execute_reply: '2026-01-22T17:45:50.067922Z', shell.execute_reply.started: '2026-01-22T17:44:37.525523Z'}
pq use cod_mes niss_ps_encrip tina_ee val_remun using "panel_GR_2010_2018.parquet", clear
count
```

<img src="./images/lampada.png" width="20"/> In this example, reading a *.parquet* file takes less than 1 minute, while a *.dta* file takes 2 minutes. 

##### **Example 4: Reading a partitioned dataset**

As mentioned above, Parquet files can be partitioned according to one or more variables. To read a complete partitioned *.parquet* dataset, use `pq use` as usual and specify the main Parquet file name without the need to identify any partition:

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T17:45:50.069728Z', iopub.status.busy: '2026-01-22T17:45:50.069503Z', iopub.status.idle: '2026-01-22T17:50:15.268731Z', shell.execute_reply: '2026-01-22T17:50:15.268013Z', shell.execute_reply.started: '2026-01-22T17:45:50.069706Z'}
pq use using "panel_GR_2010_2018_byear.parquet", clear
tab year, miss
```

<img src="./images/lampada.png" width="20"/> In this example, reading a partitioned or a non-partitioned parquet dataset takes approximately the same time.

##### **Example 5: Reading data for a specific year**

For the *.dta* dataset, Stata must load the entire data into memory before applying any filtering conditions, even when using the *if* option:

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T17:50:15.269430Z', iopub.status.busy: '2026-01-22T17:50:15.269300Z', iopub.status.idle: '2026-01-22T17:52:41.122622Z', shell.execute_reply: '2026-01-22T17:52:41.121877Z', shell.execute_reply.started: '2026-01-22T17:50:15.269417Z'}
use if year == 2015 using "panel_GR_2010_2018.dta", clear
tab year, miss
```

When using a *.parquet* file partitioned by year, it is possible to read only the required partition:

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T17:52:41.123174Z', iopub.status.busy: '2026-01-22T17:52:41.123043Z', iopub.status.idle: '2026-01-22T17:54:04.573720Z', shell.execute_reply: '2026-01-22T17:54:04.572958Z', shell.execute_reply.started: '2026-01-22T17:52:41.123160Z'}
pq use using "panel_GR_2010_2018_byear.parquet", clear if(year == 2015)
tab year
```

<img src="./images/lampada.png" width="20"/> In this example, loading one year of data takes over 3 minutes when using *.dta* files, whereas using partitioned *.parquet* files only takes a few seconds.
    
<br>

##### **Example 6: Combining filters**

You can combine filters using partition variables along with other conditions.
For instance, it is possible to load only the 2015 partition while also selecting workers with *tipo_qualificacao* equal to 1071:

```{stata}
*| output: false
*| echo: false
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T17:54:04.574566Z', iopub.status.busy: '2026-01-22T17:54:04.574418Z', iopub.status.idle: '2026-01-22T17:54:04.607954Z', shell.execute_reply: '2026-01-22T17:54:04.607401Z', shell.execute_reply.started: '2026-01-22T17:54:04.574549Z'}

set linesize 160
```

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T17:54:04.608619Z', iopub.status.busy: '2026-01-22T17:54:04.608497Z', iopub.status.idle: '2026-01-22T17:55:18.961399Z', shell.execute_reply: '2026-01-22T17:55:18.960651Z', shell.execute_reply.started: '2026-01-22T17:54:04.608607Z'}
pq use using "panel_GR_2010_2018_byear.parquet", clear if(year == 2015 & tipo_qualificacao == 1071)
tab year, miss
tab tipo_qualificacao, miss
```

> **Tip: Filtering dates**   
> The *if* option filters observations during data import by translating Stata syntax into SQL for Parquet filtering.   
> While most Stata expressions behave as expected, datetime functions are not supported in this context (as of version 1.9.1). For **example**, the following command will result in an error:
>    
> `pq use using "panel_GR_2010_2018_byear.parquet", clear if(year == 2015 & cod_mes >= td(01nov2015))`
>
> In addition, Stata dates are measure as the number of days since 1 January 1960, whereas Polars uses the Unix epoch (1 January 1970) as its reference. Consequently, numeric Stata dates cannot be used directly in Parquet filters. For **example**, 1 November 2015 corresponds to 20393 days in Stata, but the following command will import no observations:
>
> `pq use using "panel_GR_2010_2018_byear.parquet", clear if(year == 2015 & cod_mes >= 20393)`
>
> Therefore, when filtering on dates, users must use Polars syntax. In the previous **example**, the correct filter condition to import observations with dates on or after 1 November 2015 is as follows:
>
> `pq use using "panel_GR_2010_2018_byear.parquet", clear if(year == 2015 & cod_mes >= date('01nov2015','%d%b%Y'))` 

##### **Example 7: Using `metaxl` to apply metadata**

As mentioned before, *.parquet* files do not preserve the metadata such as variable and value labels or storage types:

```{stata}
*| output: false
*| echo: false
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T17:55:18.962147Z', iopub.status.busy: '2026-01-22T17:55:18.962006Z', iopub.status.idle: '2026-01-22T17:55:19.033760Z', shell.execute_reply: '2026-01-22T17:55:19.033290Z', shell.execute_reply.started: '2026-01-22T17:55:18.962133Z'}

set linesize 140
cd "${examples}"
```

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T17:55:19.034349Z', iopub.status.busy: '2026-01-22T17:55:19.034226Z', iopub.status.idle: '2026-01-22T17:56:44.886276Z', shell.execute_reply: '2026-01-22T17:56:44.885684Z', shell.execute_reply.started: '2026-01-22T17:55:19.034337Z'}
pq use using "panel_GR_2010_2018_byear.parquet", clear if(year == 2015)
describe
```

To apply the metadata to a *.parquet* file use the `metaxl apply` subcommand, specifying the name of the metafile in the option *meta*:

```{stata}
*| output: false
*| echo: true
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T17:56:44.887200Z', iopub.status.busy: '2026-01-22T17:56:44.886966Z', iopub.status.idle: '2026-01-22T17:57:26.174324Z', shell.execute_reply: '2026-01-22T17:57:26.173574Z', shell.execute_reply.started: '2026-01-22T17:56:44.887175Z'}

metaxl apply, meta("META_PANEL_GR") nobackup 
```

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T17:57:26.175274Z', iopub.status.busy: '2026-01-22T17:57:26.175055Z', iopub.status.idle: '2026-01-22T17:57:26.208656Z', shell.execute_reply: '2026-01-22T17:57:26.208148Z', shell.execute_reply.started: '2026-01-22T17:57:26.175252Z'}
describe
```

> **Tip: Extract Metadata**   
> If you don't have a metadata file, or you modified the existing metadata, you can use the `metaxl extract` subcommand to save a new Excel metadata file for later use. For example, to replace the existing metadata file ("META_PANEL_GR.xlsx") use the following command:
> ```
> metaxl extract, metafile("META_PANEL_GR") replace nobackup
>```

### 4.3. Save Parquet Files in Stata - `pq save`

To save data as a Parquet file use the **pq save** subcommand:   

`pq save using filename`

The subcommand allows to:    

- Select the variables to save;
- Overwrite an existing Parquet file (*replace* option);
- Save only rows that satisfy a specified condition (*if* option);
- Create a partitioned Parquet dataset (*partition_by* option);
- Add information without overwriting existing partitions (*nopartitionoverwrite* option). All partitions must have the same variable names and types; otherwise, the data will not be saved correctly and reading the dataset will fail;     
- Specify the compression algorithm to use in the saved Parquet file, with *zstd* used by default (*compression* option);
- Compress the data during the read operation to reduce memory usage (*compress* option). When working with Stata variables that require high numeric precision, this option should be used with caution, as it can change storage types and result in a loss of precision.

#### Examples

##### **Example 8: Saving a complete dataset**

```{stata}
*| output: false
*| echo: false
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T17:57:26.209418Z', iopub.status.busy: '2026-01-22T17:57:26.209222Z', iopub.status.idle: '2026-01-22T17:57:42.371966Z', shell.execute_reply: '2026-01-22T17:57:42.371150Z', shell.execute_reply.started: '2026-01-22T17:57:26.209398Z'}

cd "${examples}"
use "panel_GR_2010_2018.dta", clear
cd "${output}"
```

To save as *.dta*:

```{stata}
*| output: false
*| echo: true
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T17:57:42.372955Z', iopub.status.busy: '2026-01-22T17:57:42.372733Z', iopub.status.idle: '2026-01-22T18:03:02.945737Z', shell.execute_reply: '2026-01-22T18:03:02.944999Z', shell.execute_reply.started: '2026-01-22T17:57:42.372932Z'}

sort niss_ps_encrip tina_ee cod_mes 
save "panel_GR_2010_2018_v1.dta", replace
```

To save the same data as *.parquet*:

```{stata}
*| output: false
*| echo: true
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T18:03:02.946706Z', iopub.status.busy: '2026-01-22T18:03:02.946482Z', iopub.status.idle: '2026-01-22T18:05:53.545647Z', shell.execute_reply: '2026-01-22T18:05:53.544978Z', shell.execute_reply.started: '2026-01-22T18:03:02.946683Z'}

sort niss_ps_encrip tina_ee cod_mes
pq save using "panel_GR_2010_2018_v1.parquet", replace
```

<img src="./images/lampada.png" width="20"/> In this example, saving the *.dta* takes 5 minutes, while saving the *.parquet* takes approximately 3 minutes. Additionally, the *.dta* file is 30.3 GB, whereas the corresponding *.parquet* file is only 2.4 GB — a reduction in file size of over **90%**.

> **Tip: Sort**   
The way you sort the data before saving it as a *.parquet* affects the size of the Parquet file.   
As a general rule, the data should be sorted by the combined key, with the variable that has the most unique values first. However, depending on the structure of the data, this may not be the most efficient option. 
>   
> In the previous **example** the data are sorted by *niss_ps_encrip* (5 577 919 unique values), *tina_ee* (765 590 unique values) and *cod_mes* (108 unique values). This sorting order reduces file size significantly: the dataset is **2.4 GB**, compared with **5.4 GB** when unsorted.

##### **Example 9: Saving a set of variables**

To save as *.dta*:

```{stata}
*| output: false
*| echo: false
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T18:05:53.548049Z', iopub.status.busy: '2026-01-22T18:05:53.547911Z', iopub.status.idle: '2026-01-22T18:06:02.039719Z', shell.execute_reply: '2026-01-22T18:06:02.039067Z', shell.execute_reply.started: '2026-01-22T18:05:53.548035Z'}

cd "${examples}"
use "panel_GR_2010_2018.dta", clear
cd "${output}"
```

```{stata}
*| output: false
*| echo: true
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T18:06:02.040349Z', iopub.status.busy: '2026-01-22T18:06:02.040225Z', iopub.status.idle: '2026-01-22T18:11:30.204348Z', shell.execute_reply: '2026-01-22T18:11:30.203644Z', shell.execute_reply.started: '2026-01-22T18:06:02.040336Z'}

keep cod_mes niss_ps_encrip tina_ee val_remun
sort niss_ps_encrip tina_ee cod_mes
save "panel_GR_2010_2018_v2.dta", replace
```

To save the same data as *.parquet* there is no need to modify the data in memory:

```{stata}
*| output: false
*| echo: false
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T18:11:30.205364Z', iopub.status.busy: '2026-01-22T18:11:30.205102Z', iopub.status.idle: '2026-01-22T18:11:45.566398Z', shell.execute_reply: '2026-01-22T18:11:45.565829Z', shell.execute_reply.started: '2026-01-22T18:11:30.205337Z'}

cd "${examples}"
use "panel_GR_2010_2018.dta", clear
cd "${output}"
```

```{stata}
*| output: false
*| echo: true
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T18:11:45.567026Z', iopub.status.busy: '2026-01-22T18:11:45.566895Z', iopub.status.idle: '2026-01-22T18:17:23.926028Z', shell.execute_reply: '2026-01-22T18:17:23.925246Z', shell.execute_reply.started: '2026-01-22T18:11:45.567012Z'}

sort niss_ps_encrip tina_ee cod_mes
pq save cod_mes niss_ps_encrip tina_ee val_remun using "panel_GR_2010_2018_v2.parquet", replace
```

<img src="./images/lampada.png" width="20"/> In this example, saving a *.dta* file or a *.parquet* file takes 5 minutes. However, the *.dta* file is 15.9 GB, whereas the *.parquet* is 557 MB.

##### **Example 10: Saving data for a specific year**

To save as *.dta*:

```{stata}
*| output: false
*| echo: false
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T18:17:23.926972Z', iopub.status.busy: '2026-01-22T18:17:23.926752Z', iopub.status.idle: '2026-01-22T18:17:33.581552Z', shell.execute_reply: '2026-01-22T18:17:33.580433Z', shell.execute_reply.started: '2026-01-22T18:17:23.926949Z'}

cd "${examples}"
use "panel_GR_2010_2018.dta", clear
cd "${output}"
```

```{stata}
*| output: false
*| echo: true
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T18:17:33.582660Z', iopub.status.busy: '2026-01-22T18:17:33.582430Z', iopub.status.idle: '2026-01-22T18:18:58.022990Z', shell.execute_reply: '2026-01-22T18:18:58.022116Z', shell.execute_reply.started: '2026-01-22T18:17:33.582636Z'}

keep if year == 2015
sort niss_ps_encrip tina_ee cod_mes
save "panel_GR_2015.dta", replace
```

Again, to save the same data as *.parquet* there is no need to modify the data in memory:

```{stata}
*| output: false
*| echo: false
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T18:18:58.023981Z', iopub.status.busy: '2026-01-22T18:18:58.023751Z', iopub.status.idle: '2026-01-22T18:19:11.200369Z', shell.execute_reply: '2026-01-22T18:19:11.199577Z', shell.execute_reply.started: '2026-01-22T18:18:58.023956Z'}

cd "${examples}"
use "panel_GR_2010_2018.dta", clear
cd "${output}"
```

```{stata}
*| output: false
*| echo: true
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T18:19:11.201164Z', iopub.status.busy: '2026-01-22T18:19:11.201011Z', iopub.status.idle: '2026-01-22T18:24:43.038716Z', shell.execute_reply: '2026-01-22T18:24:43.037886Z', shell.execute_reply.started: '2026-01-22T18:19:11.201144Z'}

sort niss_ps_encrip tina_ee cod_mes
pq save using "panel_GR_2015.parquet", replace if(year == 2015)
```

<img src="./images/lampada.png" width="20"/> In this example, the *.dta* file is 3.6 GB, whereas the *.parquet* is 310 MB, and saving both takes approximately the same time (less than 2 minutes).

##### **Example 11: Saving a partitioned dataset by year**

```{stata}
*| output: false
*| echo: false
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T18:24:43.039731Z', iopub.status.busy: '2026-01-22T18:24:43.039504Z', iopub.status.idle: '2026-01-22T18:24:51.787357Z', shell.execute_reply: '2026-01-22T18:24:51.786581Z', shell.execute_reply.started: '2026-01-22T18:24:43.039707Z'}

cd "${examples}"
use "panel_GR_2010_2018.dta", clear
cd "${output}"
```

To save a *.parquet* file with partitions by year:

```{stata}
*| output: false
*| echo: true
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-23T16:38:08.600132Z', iopub.status.busy: '2026-01-23T16:38:08.599800Z', iopub.status.idle: '2026-01-23T16:40:44.521044Z', shell.execute_reply: '2026-01-23T16:40:44.520248Z', shell.execute_reply.started: '2026-01-23T16:38:08.600107Z'}

sort niss_ps_encrip tina_ee cod_mes
pq save using "panel_GR_2010_2018_byear.parquet", replace partition_by(year)
```

The result is a folder **panel_GR_2010_2018_byear.parquet** divided into subfolders, one for each year. 

![](./images/partitions1.png)

<img src="./images/lampada.png" width="20"/> In this example, saving a *.parquet* file with partitions takes roughly 5 minutes and each folder is 360 MB maximum.

> **Tip: Date type variables (e.g. monthly, quartely, ...)**     
> The `pq save` subcommand correctly saves date variables in daily format, allowing them to be read properly by other software such as R, Python, and Julia. This is not the case for monthly, quarterly, or other non-daily formats. Therefore, we recommend conversion of all date variables to a daily format before saving the data in Parquet format.
> 
> To convert monthly dates to daily dates (using the first day of the month as default):
> ```
> gen cod_mes2 = dofm(cod_mes)
> format cod_mes2 %td   
> ```   
>     
> To convert quarterly dates to daily dates (using the first day and month of the quarter as default):
> ```
> gen cod_mes3 = dofq(cod_mes)
> format cod_mes3 %td   
> ```   

### 4.4. Merging Parquet Files - `pq merge`

To merge a Parquet file with data in memory, use the **pq merge** subcommand:

`pq merge merge_type using filename`

The subcommand allows to:   

- Specify which observations to keep after merging (*keep* option);
- Specify which variables to keep from the using dataset (*keepusing* option);
- Replace the missing values in the master dataset with values from the using dataset (*update* option).

#### Examples

Consider that the dataset **panel_GR_2010_2018.dta** is merged with the dataset **QLF_2023_2025.dta**, which contains information on worker-firm relationship (variables *niss_ps_encrip* and *tina_ee*, respectively):

```{stata}
*| output: false
*| echo: false
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T18:30:43.205267Z', iopub.status.busy: '2026-01-22T18:30:43.205036Z', iopub.status.idle: '2026-01-22T18:30:49.980164Z', shell.execute_reply: '2026-01-22T18:30:49.979313Z', shell.execute_reply.started: '2026-01-22T18:30:43.205243Z'}

cd ${examples}
use "QLF_2023_2025.dta", clear
set linesize 120
```

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T18:30:49.981226Z', iopub.status.busy: '2026-01-22T18:30:49.980969Z', iopub.status.idle: '2026-01-22T18:30:50.015422Z', shell.execute_reply: '2026-01-22T18:30:50.014742Z', shell.execute_reply.started: '2026-01-22T18:30:49.981185Z'}
describe
```

##### **Example 12: Merging two datasets**

For the *.dta* datasets:

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T18:30:50.016409Z', iopub.status.busy: '2026-01-22T18:30:50.016171Z', iopub.status.idle: '2026-01-22T18:36:03.933453Z', shell.execute_reply: '2026-01-22T18:36:03.932778Z', shell.execute_reply.started: '2026-01-22T18:30:50.016386Z'}
use "panel_GR_2010_2018.dta", clear 
merge m:1 niss_ps_encrip tina_ee using "QLF_2023_2025.dta", keepusing(data_inicio_qualificacao data_fim_qualificacao)
```

For the same datasets in *.parquet*:

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T18:36:03.934276Z', iopub.status.busy: '2026-01-22T18:36:03.934082Z', iopub.status.idle: '2026-01-22T18:49:22.296538Z', shell.execute_reply: '2026-01-22T18:49:22.295738Z', shell.execute_reply.started: '2026-01-22T18:36:03.934257Z'}
pq use using "panel_GR_2010_2018.parquet", clear 
pq merge m:1 niss_ps_encrip tina_ee using "QLF_2023_2025.parquet", keepusing(data_inicio_qualificacao data_fim_qualificacao)
```

<img src="./images/lampada.png" width="20"/> In this example, merging *.dta* files takes 7 minutes, whereas merging *.parquet* files takes 8 minutes.

> **Tip: Sort**    
> The merge varlist should follow the same order as the sorting of the master dataset to optimize performance.   
>
> In this example, the data are first sorted by *niss_ps_encrip* and then by *tina_ee*. The merge varlist should be defined in this same order. Reversing the order increases the merge time from 8 minutes to 12.

##### **Example 13: Applying metadata to merged datasets**

When merging two datasets, it is necessary to apply the metadata from both the master and the using dataset. There are two ways to do this using the BPLIM `metaxl` package:   

- The first option is to apply two separate metadata files — one for each dataset. Apply the first metadata file and then, when applying the second with `metaxl apply`, use the *skip* option to preserve the metadata already applied.   
- The second option is to merge the two metadata files into a single one using the `metaxl combine` subcommand, and then apply the combined metadata file using the `metaxl apply` as usual.
 
The best solution depends on the datasets. If both datasets share common variables but differ in storage types, variable labels or value label categories, using `metaxl combine` is recommended to avoid inconsistencies. Regardless of the method, ensure you are using version 0.7 or later of the `metaxl` package, when applying metadata to a merged dataset.

###### **Example 13.1: `metaxl apply` with *skip* option**

```{stata}
*| output: false
*| echo: false
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T18:49:22.297521Z', iopub.status.busy: '2026-01-22T18:49:22.297312Z', iopub.status.idle: '2026-01-22T18:49:22.331690Z', shell.execute_reply: '2026-01-22T18:49:22.330974Z', shell.execute_reply.started: '2026-01-22T18:49:22.297499Z'}

cd ${examples}
```

First, import the **panel_GR_2010_2018.parquet** dataset and apply the corresponding metadata file - "META_PANEL_GR.xlsx" - with `metaxl apply`:

```{stata}
*| output: false
*| echo: true
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T18:49:22.332654Z', iopub.status.busy: '2026-01-22T18:49:22.332422Z', iopub.status.idle: '2026-01-22T18:55:19.194447Z', shell.execute_reply: '2026-01-22T18:55:19.193760Z', shell.execute_reply.started: '2026-01-22T18:49:22.332628Z'}

pq use using "panel_GR_2010_2018.parquet", clear 
metaxl apply, meta("META_PANEL_GR") nobackup
```

Next, add the variables *data_inicio_qualificacao* and *data_fim_qualificacao* from the **QLF_2023_2025.parquet** dataset, using `pq merge` as shown earlier:

```{stata}
*| output: false
*| echo: false
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T18:55:19.195081Z', iopub.status.busy: '2026-01-22T18:55:19.194956Z', iopub.status.idle: '2026-01-22T18:55:19.228154Z', shell.execute_reply: '2026-01-22T18:55:19.227649Z', shell.execute_reply.started: '2026-01-22T18:55:19.195067Z'}

set linesize 140
```

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T18:55:19.228640Z', iopub.status.busy: '2026-01-22T18:55:19.228529Z', iopub.status.idle: '2026-01-22T19:04:56.569102Z', shell.execute_reply: '2026-01-22T19:04:56.568322Z', shell.execute_reply.started: '2026-01-22T18:55:19.228628Z'}
pq merge m:1 niss_ps_encrip tina_ee using "QLF_2023_2025.parquet", keepusing(data_inicio_qualificacao data_fim_qualificacao)
drop _merge
describe
```

All variables from the master dataset have metadata, unlike the variables merged from the using dataset: *data_inicio_qualificacao* and *data_fim_qualificacao*. We now want to add metadata only for these two variables, skipping those that already include metadata.  

To do this, we apply the "META_QLF.xlsx" metadata file with the `metaxl apply` command, specifying the variables already with metadata in the *skip* option:

```{stata}
*| output: false
*| echo: false
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T19:04:56.569985Z', iopub.status.busy: '2026-01-22T19:04:56.569821Z', iopub.status.idle: '2026-01-22T19:04:56.602878Z', shell.execute_reply: '2026-01-22T19:04:56.602352Z', shell.execute_reply.started: '2026-01-22T19:04:56.569968Z'}

set linesize 140
```

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T19:04:56.603494Z', iopub.status.busy: '2026-01-22T19:04:56.603358Z', iopub.status.idle: '2026-01-22T19:06:07.353493Z', shell.execute_reply: '2026-01-22T19:06:07.352797Z', shell.execute_reply.started: '2026-01-22T19:04:56.603479Z'}
label language default, delete
metaxl apply, meta("META_QLF") skip(year cod_mes tina_ee cod_estabelecimento niss_ps_encrip qtd_numero_dias val_remun cod_regime tipo_qualificacao nat_remuneracao) nobackup
```

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T19:06:07.354288Z', iopub.status.busy: '2026-01-22T19:06:07.354146Z', iopub.status.idle: '2026-01-22T19:06:07.387966Z', shell.execute_reply: '2026-01-22T19:06:07.387373Z', shell.execute_reply.started: '2026-01-22T19:06:07.354274Z'}
describe
```

> **Tip: Language**   
> In Stata, variable and value labels may exist in multiple languages — for example, Portuguese (pt) and English (en). You can use the `label language` command to check which languages are defined in the data. By default, Stata creates a label language called "default".   
> To successfully use the *skip* option in `metaxl apply`, one condition must be met: the label language in the data must match at least one of the languages of the metadata being applied.
>
> In the previous **example**, the data include two languages: "pt" and "default":   
> <img src="./images/language.png" width="70%">  
>    
> The metadata to be applied use the "pt" language:   
> ![](./images/language_excel.png)    
>   
> Therefore, the "default" language must be removed with the command `label language default, delete`.

###### **Example 13.2: `metaxl combine`**

```{stata}
*| output: false
*| echo: false
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T19:06:07.388624Z', iopub.status.busy: '2026-01-22T19:06:07.388498Z', iopub.status.idle: '2026-01-22T19:06:07.454692Z', shell.execute_reply: '2026-01-22T19:06:07.454094Z', shell.execute_reply.started: '2026-01-22T19:06:07.388612Z'}

cd ${examples}
set linesize 120
```

First, use the `metaxl combine` subcommand to combine the metadata files "META_PANEL_GR.xlsx" and "META_QLF.xlsx", specifying which file should be prioritized in case of inconsistent metadata with the option *keep*.   
In this example, the option `keep(f1)` indicates that, in the case of insconsistencies between both metadata files (e.g., duplicate variable or value labels), the ones specified in the first metadata file (f1) will be kept:

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T19:06:07.455298Z', iopub.status.busy: '2026-01-22T19:06:07.455170Z', iopub.status.idle: '2026-01-22T19:06:11.156404Z', shell.execute_reply: '2026-01-22T19:06:11.155606Z', shell.execute_reply.started: '2026-01-22T19:06:07.455286Z'}
metaxl combine, f1("META_PANEL_GR") f2("META_QLF") keep(f1) meta("META_ALL") replace
```

Then merge the *.parquet* files as shown before:

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T19:06:11.157233Z', iopub.status.busy: '2026-01-22T19:06:11.157083Z', iopub.status.idle: '2026-01-22T19:19:34.137852Z', shell.execute_reply: '2026-01-22T19:19:34.137133Z', shell.execute_reply.started: '2026-01-22T19:06:11.157219Z'}
pq use using "panel_GR_2010_2018.parquet", clear 
pq merge m:1 niss_ps_encrip tina_ee using "QLF_2023_2025.parquet", keepusing(data_inicio_qualificacao data_fim_qualificacao)
drop _merge
describe
```

Finally, apply the combined metadata file ("META_ALL") to the merged dataset using `metaxl apply`. This option will replace all the metadata in memory with the one contained in the combined metadata file:

```{stata}
*| output: false
*| echo: true
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T19:19:34.138579Z', iopub.status.busy: '2026-01-22T19:19:34.138439Z', iopub.status.idle: '2026-01-22T19:25:00.087522Z', shell.execute_reply: '2026-01-22T19:25:00.086754Z', shell.execute_reply.started: '2026-01-22T19:19:34.138565Z'}

metaxl apply, meta("META_ALL") nobackup
```

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T19:25:00.088173Z', iopub.status.busy: '2026-01-22T19:25:00.088045Z', iopub.status.idle: '2026-01-22T19:25:00.121419Z', shell.execute_reply: '2026-01-22T19:25:00.120891Z', shell.execute_reply.started: '2026-01-22T19:25:00.088159Z'}
describe
```

<img src="./images/lampada.png" width="20"/> In this example, using `metaxl apply` with the *skip* option or using `metaxl combine` takes roughly the same amount of time. Therefore, the better choice depends on the specifics of each case, such as whether the datasets share common variables or whether value labels categories differ.

### 4.5. Appending Parquet Files - `pq append`

To append a Parquet file to data in memory, use the **pq append** subcommand:

`pq append using filename`

All `pq use` options are also available for `pq append`.

#### Examples

Consider that the dataset **panel_GR_2010_2018.dta**, containing data between January 2010 and December 2018, is appended to a similar dataset **panel_GR_2019_2025.dta**, with data from January 2019 to August 2025.

```{stata}
*| output: false
*| echo: false
*| scrolled: true
*| execution: {iopub.execute_input: '2026-01-22T19:25:00.121935Z', iopub.status.busy: '2026-01-22T19:25:00.121823Z', iopub.status.idle: '2026-01-22T19:25:00.155069Z', shell.execute_reply: '2026-01-22T19:25:00.154560Z', shell.execute_reply.started: '2026-01-22T19:25:00.121924Z'}

cd ${examples}
```

##### **Example 14: Appending two datasets**

For the *.dta* datasets:

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T19:25:00.155567Z', iopub.status.busy: '2026-01-22T19:25:00.155456Z', iopub.status.idle: '2026-01-22T19:28:03.171786Z', shell.execute_reply: '2026-01-22T19:28:03.171058Z', shell.execute_reply.started: '2026-01-22T19:25:00.155556Z'}
use "panel_GR_2010_2018.dta", clear
tab year, miss
```

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T19:28:03.172468Z', iopub.status.busy: '2026-01-22T19:28:03.172338Z', iopub.status.idle: '2026-01-22T19:33:30.794277Z', shell.execute_reply: '2026-01-22T19:33:30.793596Z', shell.execute_reply.started: '2026-01-22T19:28:03.172454Z'}
append using "panel_GR_2019_2025.dta"
tab year, miss
```

For the same datasets in *.parquet*:

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T19:33:30.794929Z', iopub.status.busy: '2026-01-22T19:33:30.794800Z', iopub.status.idle: '2026-01-22T19:36:34.133296Z', shell.execute_reply: '2026-01-22T19:36:34.132566Z', shell.execute_reply.started: '2026-01-22T19:33:30.794916Z'}
pq use using "panel_GR_2010_2018.parquet", clear
tab year, miss
```

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T19:36:34.134039Z', iopub.status.busy: '2026-01-22T19:36:34.133906Z', iopub.status.idle: '2026-01-22T19:40:43.183759Z', shell.execute_reply: '2026-01-22T19:40:43.183352Z', shell.execute_reply.started: '2026-01-22T19:36:34.134025Z'}
pq append using "panel_GR_2019_2025.parquet"
tab year, miss
```

<img src="./images/lampada.png" width="20"/> In this example, the append takes 4 minutes with *.dta* files and 2 minutes with *.parquet* files.

> **Tip: Metadata**   
> As the dataset gets larger, the `metaxl apply` subcommand will take more time to run. When the metadata is valid for both datasets, apply it to the first dataset in memory and then execute `pq append` to achieve better performance. For example:
>
> ```   
> pq use using "panel_GR_2010_2018.parquet", clear   
> metaxl apply, meta("META_PANEL_GR") nobackup   
> pq append using "panel_GR_2019_2025.parquet"   
> ```   
> 
> However, if different metadata files are required, use one of the options described above: `metaxl apply` with the *skip* option, or `metaxl combine` followed by `metaxl apply`.

##### **Example 15: Appending a set of variables**

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T19:40:43.184311Z', iopub.status.busy: '2026-01-22T19:40:43.184179Z', iopub.status.idle: '2026-01-22T19:43:07.172854Z', shell.execute_reply: '2026-01-22T19:43:07.172190Z', shell.execute_reply.started: '2026-01-22T19:40:43.184298Z'}
pq use using "panel_GR_2010_2018.parquet", clear
tab year, miss
```

```{stata}
*| execution: {iopub.execute_input: '2026-01-22T19:43:07.173764Z', iopub.status.busy: '2026-01-22T19:43:07.173541Z', iopub.status.idle: '2026-01-22T19:45:12.825345Z', shell.execute_reply: '2026-01-22T19:45:12.824591Z', shell.execute_reply.started: '2026-01-22T19:43:07.173741Z'}
pq append year cod_mes niss_ps_encrip val_remun using "panel_GR_2019_2025.parquet"
tab year, miss
```

<img src="./images/lampada.png" width="20"/> In this example, appending all the variables takes 2 minutes, while appending only a set takes only a few seconds.    

> **Tip: Package version**    
Only use the `pq append` subcommand with version 1.9.0 or later. Previous versions will not work properly.

## 5. Conclusion

In conclusion, Parquet files offer significant advantages in terms of storage efficiency. Moreover, when used properly, they can outperform *.dta* files in processing speed.    
Below is a summary of the key recommendations discussed above for an efficient use of Parquet files: 

1. In reading Parquet files, always use the *parallelize* option;
2. Read only the necessary variables;
3. Use `metaxl` to apply the metadata to Parquet files;
4. Save Parquet files with partitions that will be use to filter the data;
5. Before saving a Parquet file, ensure that monthly and quarterly dates are save in a daily format;
6. Sort the dataset by the key variables before saving it in a Parquet file to more efficient storage;
7. In merging Parquet files, ensure that the order of the keys in the subcommand corresponds to the sorting order of the data.

