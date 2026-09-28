---
title: BPLIM Datasets Guide
author: "Banco de Portugal's Microdata Research Laboratory (BPLIM)"
date: "October 2026"
format:
  pdf: 
    documentclass: scrartcl
    papersize: A4
    toc: true
    toc-title: Contents
    toc-depth: 3
    number-sections: true   
    pdf-engine: xelatex
  html:
    theme: cosmo
    embed-resources: true
    toc: true
    toc-location: left
    html-math-method: katex
    code-copy: true
    number-sections: true
    
##bibliography: references.bib
##csl: apa-6th-edition
##output:
  ##html_document:
    ##citation_package: citeproc
---


{{< pagebreak >}}


# General Remarks

This Guide describes the datasets available at BPLIM, both those **produced and owned by Banco de Portugal** (BdP) and those external databases that BPLIM has access to through **Protocols** established with various entities. 

This Guide is intended to complement the information provided in the [**Guide for Researchers**](https://github.com/BPLIM/Manuals/tree/master/Guides/01_Guide_for_Researchers), published by BPLIM, which describes the functioning of BPLIM, including the process of accessing data, types of anonymization, output control rules, among other topics. We **strongly recommend that researchers carefully read the Guide for Researchers** before proceeding with this Guide.

In section 3.5 of the Guide for Researchers, the different levels of anonymization that BPLIM uses are described. Briefly, BPLIM uses **four levels of anonymization**:

**Level 1**: All information that could lead to the direct identification of statistical units is omitted;

**Level 2**: In addition to Level 1, the values of variables containing sensitive information are replaced by modified values, which are random values that exhibit some correlation with the original values;

**Level 3**: In addition to Level 2, variables may be sorted randomly and independently to break the link between the observations.

**Level 4**: A subset of the data is generated randomly (pseudo-data), respecting only the metadata and the time structure of the original data.


The first part of the Guide outlines the datasets accessible to **External Researchers**, including a brief description of the data, their characteristics, the available time range, the Digital Object Identifier (DOI) when available, the confidentiality classification, the types of access available to external researchers, and the levels of anonymization applied.

The second part of the Guide details the additional datasets provided by BPLIM, which are primarily available to **Internal Researchers**. 

Lastly, the Guide highlights the datasets that BPLIM plans to make available in the near **future** for both internal and external researchers.

{{< pagebreak >}}



# Datasets Available for External Researchers


![Summary of External Researcher Access Options](./images/Fluxog.png)



## Central Balance Sheet Database (CB)

The Central Balance Sheet Database is constructed and made available by BdP and provides **economic and financial information on non-financial corporations operating in Portugal**. It contains annual data from 2006 onwards and is mostly based on information reported through *Informação Empresarial Simplificada* (IES, Simplified Corporate Information). 

Until 2009, the data were reported according to the *Plano Oficial de Contabilidade* (POC, Official Chart of Accounts). In 2010, a new accounting system, the *Sistema de Normalização Contabilística* (SNC, Accounting Standards System) was put in place.
Thus, all data reported after 2009 follow the SNC. This is a structural change that is reflected in the way the dataset is organized and poses some challenges in the comparability of the variables over time.

BPLIM provides two different products: the annual firm-level set **(CB)** and the firm harmonized panel **(CBHP)**. CB contains the data as reported while CBHP contains variables that were made consistent over time. Besides these two products, any variable available at IES can be added on demand.

For more information on this dataset, please refer to the **Manuals and Auxiliary Documentation** (metadata files, variable descriptions) available in the [**BPLIM Github Repository - CB**](https://github.com/BPLIM/Manuals/tree/master/Data/CB).
<br>



![Central Balance Sheet Available Products](./images/CB.png)



(1) There are two variables that, if requested by an external researcher, will be anonymized at Level 2.



{{< pagebreak >}}


## Fast and Exceptional Enterprise Survey - COVID-19 (IREE-COVID)

The Fast and Exceptional Enterprise Survey - COVID-19 (IREE-COVID) was launched by Statistics Portugal (INE) and the BdP aiming to identify the main effects of the COVID-19 pandemic on key aspects of the enterprises activity, such as firm's turnover, workforce, prices, credit conditions and the use of Government support measures. This survey was addressed to a representative sample of non-financial firms located in Portugal. The data started being collected with a weekly frequency on April 6-10, 2020 and refers to a fortnight from May 2020 onwards. Although the survey was suspended after July 2020, two new editions were implemented, in November 2020 and in the first fortnight of February 2021 given the evolution of the pandemic situation. 

For more information on this dataset, please refer to the **Manuals and Auxiliary Documentation** (metadata files, variable descriptions) available in the [**BPLIM Github Repository - IREE**](https://github.com/BPLIM/Manuals/tree/master/Data/IREE).
<br>



![COVID-IREE Available Products](./images/IREE.png)

{{< pagebreak >}}


## The Incentives Systems (SI)

The Incentives Systems Database (SI) includes information for projects submitted to the incentives systems funded by the European Regional Development Fund (ERDF) within the QREN (2007-2013) framework and the European Regional Development Fund and European Social Fund (ESF) within the PT2020 (2014-2020) framework. The data include information on both approved and non-approved applications. The data made available by BPLIM corresponds to a data freeze at a certain moment. The QREN data will no longer be subject to updates and corresponds to a freeze that occurred on September 2017. The PT2020 data is updated annually.

For more information on this dataset, please refer to the **Manuals and Auxiliary Documentation** (metadata files, variable descriptions) available in the [**BPLIM Github Repository - SI**](https://github.com/BPLIM/Manuals/tree/master/Data/SI).
<br>



![Incentives Systems Available Products](./images/SI.png)



## Entreprise Groups (GE)

The Enterprise Groups Database (GE) is constructed and made available by BdP and provides information on the participations in equity capital and voting rights of non-financial corporations operating in Portugal. This dataset contains annual data from 2014 onwards and is based on the information reported through Informação Empresarial Simplificada (IES, Simplified Corporate Information).

For more information on this dataset, please refer to the **Manuals and Auxiliary Documentation** (metadata files, variable descriptions) available in the [**BPLIM Github Repository - GE**](https://github.com/BPLIM/Manuals/tree/master/Data/GEXXXXX).
<br>



![Entreprise Groups Available Products](./images/GE.png)


{{< pagebreak >}}


## Spanish and Portuguese Companies Microdata (iBACH)

The Spanish and Portuguese Companies Microdata (iBACH) contains economic and financial granular information on non-financial Spanish and Portuguese corporations from iBACH. This dataset derives from BACH dataset. BACH is a database of aggregated and harmonized accounting data of non-financial companies, based on national accounting standards (individual annual accounts). 

This dataset is also made available by the [**Data Laboratory of the Banco de España - BELab**](https://www.bde.es/wbe/en/para-ciudadano/servicios/belab/contenido/microdatos-disponibles/microdatos-de-empresas-espanolas-y-portuguesas--ibach-.html).

For more information on this dataset, please refer to the **Manuals and Auxiliary Documentation** (metadata files, variable descriptions) available in the [**BPLIM Github Repository - iBACH**](https://github.com/BPLIM/Manuals/tree/master/Data/iBACH).
<br>



![iBACH Available Products](./images/iBACH.png)

{{< pagebreak >}}



## Central Credit Register Database (CRC)

The Central Credit Register (CRC) database reports credit supplied by all credit-granting institutions in Portugal. Data are collected monthly with the objective of supporting participating institutions in assessing credit risk.

Until 2018, Banco de Portugal collected information at the **credit exposure level** and produced three datasets with different levels of granularity: **exposure-level**, **firm-bank-level** and **firm-level** data (this database is now known as the Old CRC). The database was updated annually until 2018. The Old CRC underwent a major revision in September 2018 and was replaced by a new reporting system.

In 2026, the database underwent a further revision, resulting in **Version 2** of the dataset, which incorporates several methodological changes.

For more information on this dataset, please refer to the **Manuals and Auxiliary Documentation** (metadata files, variable descriptions) available in the [**BPLIM Github Repository - CRC**](https://github.com/BPLIM/Manuals/tree/master/Data/CRC).
<br>


![CRC Available Products](./images/CRC.png)

{{< pagebreak >}}


## Harmonized Central Credit Register (HCRC)

The Portuguese Central Credit Register (with the database prior to September 2018 known as the Old CRC) underwent a major revision in September 2018 and was replaced by a new reporting system (known as the New CRC), which started to collect granular credit data at the **instrument level**.

The Harmonized Central Credit Register Database (HCRC) aims to construct compatible series between the Old CRC and the New CRC by selecting a set of the most relevant variables and applying the necessary procedures to harmonize the data. The database is updated annually, covers the period from 2009 onwards, and provides information aggregated at the  **firm-level** and **bank-firm level**. 

Data constructed at **exposure level** mimicking the data structure of the Old CRC is only available to internal researchers.

For more information on this dataset, please refer to the **Manuals and Auxiliary Documentation** (metadata files, variable descriptions) available in the [**BPLIM Github Repository - HCRC**](https://github.com/BPLIM/Manuals/tree/master/Data/HCRC).
<br>



![HCRC Available Products](./images/HCRC.png)

{{< pagebreak >}}



## Bank Balance Sheet (BBS)– Discontinued

The Monetary Financial Institutions (MFIs) Balance Sheet Database (BBS) reports, on an **individual basis**, detailed information on the assets and liabilities of **MFIs operating in Portugal**. The dataset contains monthly data from 1997 to December 2023.

The BBS has been **discontinued** for methodological reasons and is no longer updated. It has been replaced by the **Individual MFI Balance Sheet Items Portugal (iBSIPT**) database, first made available by BPLIM in 2026. 

For more information on the new database, please refer to the **iBSIPT section** of this Manual and to the **Manuals and Auxiliary Documentation** available in the [**BPLIM Github Repository - iBSIPT**](https://github.com/BPLIM/Manuals/tree/master/Data/iBSIPT).

<br>



![BBS Products](./images/BBS.png)


{{< pagebreak >}}



## Historical Series of Portuguese Banking Sector (SLB)

The Historical Series of the Portuguese Banking Sector Database (SLB) reports, on a **consolidated basis**, a wide range of information on banks' financial statements (i.e., balance sheet, income statement, and solvency), loans to customers, interest rates, human resources, branch networks, and payment systems. The data are collected and assembled by a working group at Banco de Portugal, established at the end of 2017 with the objective of constructing historical series for the Portuguese banking sector.

The SLB database covers the period from 1990 onwards and is available at an annual frequency. For some tables (i.e., balance sheet, income statement, solvency, loans to customers, and interest rates), data are also available at a quarterly frequency. The dataset is updated annually.

For more information on this dataset, please refer to the **Manuals and Auxiliary Documentation** (metadata files, variable descriptions) available in the [**BPLIM Github Repository - SLB**](https://github.com/BPLIM/Manuals/tree/master/Data/SLB).
<br>



![SLB Available Products](./images/SLB.png)

{{< pagebreak >}}



## Individual MFI Balance Sheet Items Portugal (iBSIPT)

The Individual MFI Balance Sheet Items Portugal Database (iBSIPT) reports, on an **individual basis**, detailed balance sheet information for monetary financial institutions (MFIs) operating in Portugal. The database provides monthly outstanding amounts of balance sheet items, broken down by counterparty sector and residency and, for selected items, by original maturity.

The iBSIPT database covers the period from December 2014 onwards and is available at a monthly frequency. The dataset was first made available by BPLIM in 2026 and replaces the discontinued Bank Balance Sheet Database (BBS).

For more information on this dataset, please refer to the **Manuals and Auxiliary Documentation** (metadata files, variable descriptions) available in the [**BPLIM Github Repository - iBSIPT**](https://github.com/BPLIM/Manuals/tree/master/Data/iBSIPT).
<br>



![iBSIPT Available Products](./images/iBSIPT.png)

{{< pagebreak >}}



## Summary


![Summary of Datasets Available to External Researchers](./images/summary_ext.png)

{{< pagebreak >}}




# Additional Datasets Available for Internal Researchers

Although these datasets are primarily available for internal use, all datasets produced by Banco de Portugal may also be made available to external researchers through **remote execution**, provided that the project's research topic is considered relevant to Banco de Portugal's **research agenda**.


![Additional Datasets Available for Internal Researchers](./images/internal.png)



## Central Credit Register (CRC) - Households

The Central Credit Register (CRC) database contains credit exposure data for both firms and **households**. Data on credit granted to households is only available for Internal Researchers. This information is considered **highly confidential** due to its sensitive nature. 



## Supermarket Daily Prices (SDP) and Matched Supermarket Daily Prices (MSDP)

The Supermarket Daily Prices (**SDP**) database provides **daily data on the prices** of food and beverage products sold in six supermarkets in Portugal: Auchan, Continente, Minipreço, Pingo Doce, Froiz, and Supercor. This information is **webscraped** from the supermarkets' online stores by BPLIM.

Based on these data, BPLIM created the Matched Supermarket Daily Prices (**MSDP**) database, which provides daily prices for food and beverage products matched across multiple supermarkets included in the SDP database, enabling price comparisons across supermarket chains.

Both the SDP and MSDP datasets cover the period from 2021 onwards and are updated **annually for research purposes**.

These datasets are only available for research projects involving internal researchers.


{{< pagebreak >}}



# Future Developments


![Upcoming Datasets](./images/future.png)


## Statistical Central Credit Register (CRCE)

The Portuguese Central Credit Register underwent a major revision in September, 2018 (with the database prior to September 2018 known as the Old CRC) and was replaced by a new reporting system (i.e. NEWCRC) which started to collect granular credit data on a loan-by-loan basis.

To **facilitate and harmonize** the use of credit information, the Statistical Central Credit Register (Statistical CRC) was created. This database contains credit information at the micro level, where information reported to the CRC is made available after statistical data processing processes. These processes include the correction of flaws identified in the reported information and the calculation of additional variables following harmonized methodologies. 

As a result, the Statistical CRC provides a common and consistent source of granular credit information, helping to ensure comparability across analyses based on these data.

The data will be available at the **firm level**, **firm-bank level**, and **instrument level**.



## Balance of Payments (BoP)

The Portuguese Balance of Payments records transactions between residents and non-residents over a given period, typically a month, quarter, or year. Transactions are classified according to the nature of the underlying economic resources and are grouped into **three main categories**: the current account, capital account, and financial account.

The current account records transactions between residents and non-residents involving goods and services, primary income (income associated with the use of factors of production, such as capital and labour), and secondary income (current transfers).

These data will only be available for research projects involving internal researchers.


## E-Fatura

E-Fatura data are received monthly under a **Protocol between Banco de Portugal and Statistics Portugal (INE)**. The database contains **information on invoices** issued by entities with their headquarters or a permanent establishment in Portugal. The information is aggregated by the tax identification number (NIF) of the issuer (for legal persons only) and the acquirer.

Before sharing the data with Banco de Portugal, INE performs data cleaning procedures, including the imputation of missing values and the treatment of outliers.

These data will only be available to Internal Researchers. 


## Social Security (SS)

Social Security Data (SS) are received monthly under a **Protocol between Banco de Portugal and the Social Security Institute**. The database provides monthly information, from January 2010 onwards, on individuals' classification for contribution purposes, wage records, and Social Security transfers. Information on pensions is available from January 2017 onwards.

These data will only be available to Internal Researchers. 



## Institute for Employment and Vocational Training Database (IEFP)

IEFP data cover job applications, job offers, applications to job offers, interventions, and calls managed through the information system of the Institute for Employment and Vocational Training (IEFP).

The database tracks individuals registered with IEFP for job-search purposes and provides information on their interactions with the Institute, including interventions, calls from job centres, and job applications. It also includes information on the outcomes of these interactions.

These data will only be available to Internal Researchers.


