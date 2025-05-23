<meta charset="utf-8"/>

---
title: Monetary Financial Institutions Balance Sheet Database - Data Manual
---

`Extraction Date`: June 2023

`Manual Date`: 27 July 2023  \

####  **Abstract**: The Monetary Financial Institutions (MFIs) Balance Sheet Database reports detailed information on the assets and liabilities of the monetary financial institutions (MFIs) operating in Portugal. The database covers the period from 1997 to 2022 and is updated annually.

**Keywords**: balance sheet, asset, liabilities, instrument, counterparty, revisions. \


# Table of contents
1. [General Information](#general-information)

2. [Geographical Coverage](#geographical-coverage)

3. [Population](#population)

4. [Methodology](#methodology)

5. [Description of Files](#description-of-files)

6. [Description of Variables](#description-of-variables)

7. [Basic Descriptive Statistics](#basic-descriptive-statistics)

8. [Auxiliary Files](#auxiliary-files)

9. [Useful Links](#useful-links)

10. [Legislation](#legislation)

11. [Useful Tools](#useful-tools)

12. [Citation of this dataset](#citation-of-this-dataset)



# General Information
> `Data Type`: longitudinal data

> `Unit of Analysis`: instrument-counterparty

> `Frequency`: monthly

> `Start Date`: September, 1997

> `Most Recent Date`: December, 2022

> `Reference date`: month-end

> `Data Organization`: data is organized for assets and liabilities separately. All data files are available in Stata format.

> `Version of the Data`: the data made available by BPLIM corresponds to a data freeze at a certain time of the year. Therefore, all files contain information as reported at the extraction date. The most recent update of the data occurred in June 2023.

> `Languages Available`: variables labels are available in Portuguese and in English. [^1]

> `Data Access`: this data set is available to external researchers under certain conditions.[^2]

[^1]: To see the labels in Portuguese type the following command line in Stata: “label language pt”.

[^2]: Conditions for data access for external researchers are detailed in the *Guide for Researchers Using Banco de Portugal Microdata Research Laboratory (BPLIM) Data*.

>  `Digital Object Identifier`: 10.17900/BBS.Jun2023.V1.

# Geographical Coverage
The MFIs Balance Sheet Database includes the assets and liabilities of all monetary financial institutions (MFIs) operating in mainland Portugal and autonomous regions - Azores and Madeira.

# Population
The MFIs Balance Sheet Database collects the balance sheet data for all monetary financial institutions (MFIs) that were in operation in Portugal between September 1997 and December 2022.


<u>**Comment**</u> : Non-monetary financial agents are not covered in the database. In case an institution stops to be classified as MFI, data reporting will be discontinued. Some MFIs in Portugal have experienced acquisitions and/or mergers, which induced asset/liability flows from one institution to another.


# Methodology
The MFIs Balance Sheet Database has undergone the first major revision in December, 2014 which lead to the reclassification of financial institutions and counterparties.[^3]. Due to this revision, there are some breaks in the series. The revision also adds an extra variable that indicates institution type.

Furthermore, in March 2021 a new data Warehouse was implemented at the Bank of Portugal, which expands the reporting of the balance sheet information for the Monetary Financial Institutions (MFIs) after December 2014 within the scope of Instruction No. 14/2021. The reporting was extended to a wider range of financial instruments and reflects mark-to-market values, taking into account changes in prices and exchange rates. The previous Instruction No. 25/2014 was revoked with effect from January 31, 2022.

To make variables compatible over time, we have harmonized the data based on the correspondence table illustrated in the [*Description of Variables*](#description-of-variables) section.


To preserve confidentiality, MFIs are anonymized through unique identifiers and the instrument values are perturbed for external researchers.[^4]


[^3]: Please refer to the [variable spreadsheet](./aux_files/variables_description/var_bbs.html) for details.

[^4]: See the *Guide for Researchers Using Banco de Portugal Microdata Research Laboratory (BPLIM) Data*.


# Description of Files
The MFIs Balance Sheet Database is organized separately for assets and liabilities in the bank balance sheet (BBS) files. Each row corresponds to an instrument-counterparty pair in a given month.

The data files are organized with the following nomenclature:

***BBS_METH_BNK_xxxx_yyyy_V01.dta***

where *xxxx* denotes the data range (eg: SEP1997DEC2022), *yyyy* denotes the type of balance (ASSET for asset instruments; LIAB for liability instrument), and *METH* denotes the method used to prepare the data (*“A”* for Anonymized and *“P”* for Perturbed).

Identification of MFIs will be anonymized in the data. Additionally, for external researchers the data values are perturbed.

We also provide a harmonized data set to facilitate the comparison between the two reporting systems, i.e. before and after December, 2014.


# Description of Variables

`Bank identifier`

Anonymized identification number for MFI that enables tracking the MFI over time. BPLIM provides an anonymized version of the MFIs identifier which is denoted by *bina*.

| Abbreviation | Definition |
| :------ | :------ |
| *bina* | Anonymized bank identificaton number |


**Availability**: Sep. 1997 - Dec. 2022

`Reference date`

The reference month of the data

| Abbreviation | Definition |
| :------ | :------ |
| *date* | Reference month of the data |


**Availability**: Sep. 1997 - Dec. 2022

`Instrument code`

Classification of the financial instrument

The classification of financial instruments was revised in December, 2014. As a result, a new categorization was applied thereafter. Below is the correspondence table for the instrument codes between the two reporting systems (aligned based on the previous reporting system).

| Abbreviation | Definition |
| :------ | :------ |
| *instrument_asset* | Financial instruments: asset side  |
| *instrument_liab* | Financial instruments: liability side |


**Availability**: Sep. 1997 - Dec. 2022


**Table 2**  - Correspondence Table for Financial Instruments

Panel A: Asset side (*instrument_asset*)

|  **Before December 2014** |  | **December 2014 onwards**  |  |
| :---------- | :-------------------- |:-------------- |:------------ |
|**Code** | **Designation** | **Code** | **Designation** |
|10|	Banknotes and coins |	10	|Banknotes and coins |
|20|	Credit and equivalent - up to 1 year|	20|	Credit and equivalent - up to 1 year|
|30|	Credit and equivalent - from 1 year to 5 years| 30 |Credit and equivalent - from 1 year to 2 years|
|30|  Credit and equivalent - from 1 year to 5 years| 40|	Credit and equivalent - from 2 year to 5 years|
|40|	Credit and equivalent - more than 5 years | 50|	Credit and equivalent - more than 5 years|
|50|	Securities other than equity - up to 1 year | 60|	Debt securities - up to 1 year |
|60|	Securities other than equity - from 1 year to 2 years | 70|	Debt securities - from 1 year to 2 years|
|70|	Securities other than equity - more than 2 years | 80|	Debt securities - more than 2 years	|
|80|	Equity securities | 90|	Traded shares|
|80|  Equity securities | 100| Untraded shares|
|80|  Equity securities | 110| Other equities|
|80|  Equity securities | 120| Units|
|100|	Properties, furnitures, and equipments | 130|	Properties, furnitures, and equipments|
|110|	Miscellaneous assets | 140|	Miscellaneous assets|
|90|	Units (included in equity securities) | 120| Units|

<u>**Comment**</u> : Before December 2014, the financial instrument “Units” (coded 90) is also included in the financial instrument “Equity securities” (coded 80).

**When calculating the aggregates, to avoid double counting the value for “Unit” should be dropped.**


Panel B: Liability side (*instrument_liab*)

|  **Before December 2014** |  | **December 2014 onwards**  |  |
| :---------- | :-------------------- |:-------------- |:------------ |
|**Code** | **Designation** | **Code** | **Designation** |
|130|	Demand deposits (excluding sight deposits) |380|	Demand deposits (excluding sight deposits)|
|140|	Deposits redeemable at a notice of up to 90 days  (excluding sight deposits) |390|	Deposits redeemable at a notice of up to 90 days  (excluding sight deposits)	|
|150|	Deposits redeemable at a notice of more than 90 days  (including sight deposits) |400|	Deposits redeemable at a notice of more than 90 days  (including sight deposits)|
|170|	Deposits and equivalent  (excluding demand deposits, deposits redeemable at notice, and trading liabilities) - up to 1 year |420|	Deposits and equivalent  (excluding demand deposits, deposits redeemable at notice, and trading liabilities) - up to 1 year	|
|180|	Deposits and equivalent  (excluding demand deposits, deposits redeemable at notice, and trading liabilities) - from 1 to 2 years | 430|	Deposits and equivalent  (excluding demand deposits, deposits redeemable at notice, and trading liabilities) - from 1 to 2 years	|
|190|	Deposits and equivalent  (excluding demand deposits, deposits redeemable at notice, and trading liabilities) - more than 2 years|440|	Deposits and equivalent  (excluding demand deposits, deposits redeemable at notice, and trading liabilities) - more than 2 years	|
|200|	Trading liabilities |450|	Trading liabilities - up to 1 year	|
|200| Trading liabilities |460|	Trading liabilities - more than 1 year |
|210|	Securities other than capital - up to 1 year |470|	Debt securities issued - up to 1 year	|
|220|	Securities other than capital - from 1 to 2 years |480|	Debt securities issued - from 1 to 2 years	|
|230|	Securities other than capital - from 2 years |490|	Debt securities issued - more than 2 years	|
|240|	Capital and reserves |500|	Capital and reserves	|
|260|	Miscellaneous liabilities |520|	Miscellaneous Liabilities	|


`Counterparty code`

Classification of counterparty


| Abbreviation | Definition |
| :------ | :------ |
| *counterparty_asset* | Classification of counterparty: asset side  |
| *counterparty_liab* | Classification of counterparty: liability side |

**Availability**: Sep. 1997 - Dec. 2022


The classification of counterparties was also revised in December, 2014. The correspondence table for the counterparty codes between the two reporting systems (aligned based on the previous reporting system) is:

**Table 3** - Correspondence Table for Counterparties

Panel A: Asset side (*counterparty_asset*)

|  **Before December 2014** |  | **December 2014 onwards**  |  |
| :---------- | :-------------------- |:-------------- |:------------ |
|**Code** | **Designation** | **Code** | **Designation** |
|10|	Monetary financial institutions |11|	Central banks|
|10|  Monetary financial institutions |12	|Money market funds|
|10|  Monetary financial institutions |13|	Deposit institutions, excluding central banks|
|20|	Other financial intermediaries and financial auxiliaries |18|	Other financial intermediaries, financial auxiliaries, and captive financial institutions and money lenders	|
|20|  Other financial intermediaries and financial auxiliaries |22|	Investment fund, excluding money market funds|
|30|	Insurance corporations and pension funds |31|	Insurance corporations	|
|30|  Insurance corporations and pension funds |32|	Pension funds|
|40|	Central government |40|	Central government	|
|50|	Regional government |50|	Regional government	|
|60|	Local government |60|	Local government	|
|70|	Social security |70|	Social security	|
|80|	Non-financial institutions |80|	Non-financial institutions	|
|90|	Individuals |91|	Family|
|90|  Individuals |92|	Non-profit institutions serving households|
|120|	Irrelevant sector |120|	Irrelevant sector	|


Panel B: Liability side (*counterparty_liab* )

|  **Before December 2014** |  | **December 2014 onwards**  |  |
| :---------- | :-------------------- |:-------------- |:------------ |
|**Code** | **Designation** | **Code** | **Designation** |
|10|	Central banks |10|	Central banks	|
|20|	Institutions not subject to minimum reserves, namely the money market funds |21|	Money market funds 	|
|30|	Institutions subject to minimum reserves |22|	Deposit institutions, excluding central banks	|
|40|	Other financial intermediaries and financial auxiliaries |39|	Other financial intermediaries, financial auxiliaries, and captive financial institutions and money lenders 	|
|40|  Other financial intermediaries and financial auxiliaries |43|	Investment fund, excluding money market funds |
|50|	Insurance corporations and pension funds |51|	Insurance corporations	|
|50|  Insurance corporations and pension funds |52|	Pension funds|
|60|	Central government |60|	Central government	|
|70|	Regional government |70|	Regional government	|
|80|	Local government |80|	Local government	|
|90|	Social security |90|	Social security	|
|100|	Non-financial institutions |100|	Non-financial institutions	|
|110|	Individuals |111|	Family	|
|110| Individuals |112|	Non-profit institutions serving households|
|120|	Irrelevant sector |120|	Irrelevant sector	|



`Country`

Country of origin or region of the counterparty

| Abbreviation | Definition |
| :------ | :------ |
| *country* | Country of origin [^5]|

**Availability**: Sep. 1997 - Dec. 2022

[^5]: This variable has experienced a reclassification in the current extraction, causing a break in the data after December 2014. The affected instruments include Properties, furnitures, and equipments; Miscellaneous assets;	Debt securities issued - up to 1 year;	Debt securities issued - from 1 to 2 years;	Debt securities issued - more than 2 years;	Capital and reserves;	Miscellaneous Liabilities. Furthermore, the following components: *Portugal, Monetary Union countries excluding Portugal (UM-PT) and Countries outside Monetary Union (PT-UM).* are no longer available in the data after December, 2014, but can be reconstructed summing up the values of the related countries.


**Table 4** - Counterparty Countries (*country*)

| **Code**	| **Designation** |
| :------------|:----------------|
|UM-PT|	Monetary Union countries excluding Portugal|
|TP-UM|	Countries outside Monetary Union|
|EUB|	European Central Bank|
|AUT|	Austria|
|BEL|	Belgium|
|CYP|	Cyprus|
|DEU|	Germany|
|ESP|	Spain|
|EST|	Estonia|
|FIN|	Finland|
|FRA|	France|
|GRC|	Greece|
|IRL|	Ireland|
|ITA|	Italy|
|LTU|	Lithuania|
|LUX|	Luxembourg|
|LVA|	Latvia|
|MLT|	Malta|
|NLD|	Netherlands|
|PRT|	Portugal|
|SVK|	Slovakia|
|SVN|	Slovenia|

 <u>**Comment**</u> : One should take caution not to double count the Monetary Union (UM) countries when calculating the aggregates.

`Institution type`

 Type of institution. This variable is only available from December, 2014 onwards.

 | Abbreviation | Definition |
 | :------ | :------ |
 | *inst_type* | Type of institution |

 **Availability**: Dec. 2014 - Dec. 2022



 **Table 5** – Institution type (*inst_type*)

| **Code**	| **Designation** |
| :-------|:-----------|
|1 |Banks|
|2 |Saving banks|
|3 |Money market fund|
|4 |Central agricultural credit bank and mutual agricultural credit banks|
|5 |Branch of Credit Institution Headquartered in the EU|
|6 |Branch of Credit Institution Headquartered in Third Countries|
|7 |Branch of Affiliates of Financial Institutions headquartered in the EU|


`Value`

Value outstanding of a financial instrument, expressed in millions of euros.


| Abbreviation | Definition |
| :------ | :------ |
| *value* | Amount (in million euros) |

**Availability**: Sep. 1997 - Dec. 2022



# Basic Descriptive Statistics

**Table 6** - Number of observations over the data period (as of December)


```{stata}
*| output: TRUE
*| echo: FALSE

set linesize 200
local extraction="JUN23"
local ref="2023_06"
local period="SEP1997DEC2022"
local version="V01"
local file1="MBNK"


  quietly use "Z:/data/Products/BBS/`ref'/BBS_Panel/Output/Data/BBS_P_`file1'_`period'_`extraction'_ASSET_`version'.dta", clear

  quietly keep if month(dofm(date))==12
  quietly gen Year= year(dofm(date))

  table Year, contents(freq) center

```


# Auxiliary Files


For a description of each variable in each dataset (name, unit of measurement, data and storage type, format, year of first and last observation), an account of the changes occurred over time, summary statistics for each dataset and a codebook for each dataset, please check the following auxiliary files:

| Data File | Description of Variables | Summary Statistics | Codebook | Dataset description |
| :---- | :----: | :----: | :----: |  :----: |
| Bank Balance Sheet (BBS) |	[var_bbs.html](./aux_files/variables_description/var_bbs.html) | [stat_bbs.html](./aux_files/descriptive_statistics/stat_bbs.html)[^6] | 	[cdbk_bbs.html](./aux_files/codebook/cdbk_bbs.html) | [dscr_bbs.html](./aux_files/describe_dataset/dscr_bbs.html) |

\

The Summary Statistics, Codebook and Dataset Description files are available on BPLIM's servers.

[^6]: Please note that the summary statistics are run based on the perturbed data.


# Useful Links

<https://www.bportugal.pt/EstatisticasWEB/MetadataItens/MContexto_IFM_EN.htm>

# Legislation

Below is a list of relevant legislations:

1.    [**Instrução no. 43/97**](./Instruções EMF-combine/43-97i67.pdf)

2.    [**Instrução no. 19/2002**](./Instruções EMF-combine/19-2002i7.pdf)

3.    [**Instrução no. 12/2010**](./Instruções EMF-combine/12-2010i4.pdf)

4.    [**Instrução no. 20/2012**](./Instruções EMF-combine/20-2012i4.pdf)

5.    [**Instrução no. 25/2014**](./Instruções EMF-combine/25-2014m.pdf)

6.    [**Instrução no. 14/2021**](./Instruções EMF-combine/14-2021.pdf)

# Useful Tools

We provide an ado file written by BPLIM staff for researchers to implement the
matching of the Monetary Financial Institutions (MFIs) Balance Sheet Database with the other BPLIM databases that report bank-related information.


## linkbank

`Description`

`linkbank` is a Stata user-written command to help create linking ids for financial institutions operating in Portugal for the purpose of merging various BPLIM databases, such as the Central Credit Responsibility (CRC) database, the Bank Balance Sheet (BBS) and Historical Series of the Portuguese Banking Sector (SLB)

`Syntax`

```
linkbank bankid timeid, options

```

where `bankid` is BPLIM's anonymized bank identifier and `timeid` identifies the time variable.

`options`


*base* specifies the database to link with (BBS or SLB)

*method* specifies the linking method (i.e. assign ids of the parent banks; take into account credit transfers due to Mergers and Acquisitions)

*replace* replace the bank id with the new linking bank id that users can use to merge CRC with BBS/SLB

*generate* creates a variable with the new linking bank id that users can use to merge CRC with BBS/SLB

*keepindicator* indicates the situations in which the new linking bank id is assigned

*add* includes further information on the institutions (i.e. the banking group to which a financial institution belongs and the type of affiliation; banking events and the type of counterparties)


# Citation of this dataset

Banco de Portugal Microdata Research Laboratory (BPLIM)(2023): Bank Balance Sheet Monthly Data. Extraction: June 2023. Version:V1. BANCO DE PORTUGAL. Dataset. https://doi.org/10.17900/BBS.Jun2023.V1
