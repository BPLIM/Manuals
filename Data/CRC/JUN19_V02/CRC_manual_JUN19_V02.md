---
title:  Central Credit Responsibility Database - Firm, Firm-Bank and Exposure Level - Data Manual
subtitle: Extraction Date - June 2019 V02
author: BPLIM
date: 18 February 2026
abstract: 'The Central Credit Responsibility (CCR) database reports monthly credit data from all credit-granting institutions in Portugal, supporting participating entities in the risk assessment of credit granting. This research product is derived from the official CCR reporting and is available from 1999 onward. Microdata available to external researchers are aggregated at the firm and firm-bank levels, while internal researchers also have access to data at the individual credit exposure level. The dataset was last updated in 2019, with the most recent month available being August 2018. No further updates will be made to this product. For more recent credit data, please refer to the HCRC product.'
keywords: credit exposure, firm level, firm-bank level, credit-granting institutions, firm-bank relationship, revisions.
pdf-engine: pdflatex
engine: knitr
execute:
  echo: false
  warning: false
format:
  pdf:
    toc: true
    toc-depth: 3         # include up to H3 headings
    number-sections: true
  html:
    toc: true
    footnotes-hover: true
    code-fold: true
    code-copy: true
    theme: default
    toc-depth: 3         # include up to H3 headings
    number-sections: true
jupyter: nbstata
---
```{r setup}
#| include: false
library(Statamarkdown)
```

# General Information

> **Data Type**: Longitudinal Data

> **Unit of Analysis**: firm, firm-bank, credit exposure

> **Frequency**: Monthly

> **Start Date**: January, 1999

> **Most Recent Date**: August, 2018

> **Reference Date**: the last day of a month

> **Data Organization**: the data are provided as three Stata datasets, one for each unit of analysis, along with a complementary Stata file that can be used with any of the units.

> **Version of the Data**: the data made available by BPLIM corresponds to a data freeze at a specific point in time. Accordingly, all files reflect the information as reported on the extraction date. 
The most recent data update was performed in June 2019, and the current release corresponds to version V02. The changes relative to version V01 are described below.

> **Languages Available**: Variables labels are available in Portuguese and English.[^1] 

[^1]: To view labels in English, type `label language en` in Stata. To view labels in Portuguese, type `label language pt`.

> **Data Access**: This dataset is available to external researchers under the conditions detailed in the *[Guide for Researchers Using Banco de Portugal Microdata Research Laboratory (BPLIM) Data](https://github.com/BPLIM/Manuals/blob/master/Guides/01_Guide_for_Researchers/Guide_for_researchers_v072024.pdf)*. External researchers have access to anonymized data at the firm and firm–bank levels. Internal researchers also have access to anonymized data at the credit exposure level.

> **Digital Object Identifier**: 10.17900/CRC.FRM.Jun2019.V2;   
10.17900/CRC.FRMBNK.Jun2019.V2; 10.17900/CRC.EXP.Jun2019.V1.

> **New on V02**: The reporting of credit information by participating entities has changed over time. These changes are observable in the exposure-level data and are documented in this manual. Version V02 harmonizes the rules used to compute aggregates at the firm and firm–bank data, while leaving the exposure-level data unchanged relative to V01. The main changes are: (i) the exclusion of foreign credit reported 
by banks during 2006–2008 (tipocredito 13 and 14); (ii) the exclusion of guarantee exposures from credit amounts, as these are not consistently reported over the full period (tipocredito 11 and 12 for 2006–2008, and produto 14 and 15 from 2009 onward); (iii) the inclusion of credit amounts associated with joint credit for remaining debtors (nivelresponsabilidade 3 and 31–35) in the computation of aggregates, and (iv) the exclusion of data reported by mutual guarantee societies to avoid double counting. For more details on the rules to construct the firm and firm-bank level data, please consult the subsection [“Aggregate credit amounts”](#sec-aggregateamounts).

    
# Geographical Coverage

In its origin, the Central Credit Responsibility (CCR) primarily covers firms operating in mainland Portugal and the autonomous regions of Azores and Madeira, as reported by participating entities to Banco de Portugal. Although the CCR includes some information on foreign firms, the reporting requirements for credit granted to them have changed over time. In 2006, loans granted to foreign firms operating in Portugal became subject to reporting under Instrução nº 7/2006. In the same period, following the EU national central banks’ Memorandum[^3], credit exposures above €25,000 of Portuguese entities obtained from financial institutions in participating countries were required to be reported. From 2009, credit extended to Portuguese firms by foreign branches of Portuguese banks can be identified using the variable *paisbalcaoid*.[^4]

**To maintain consistency over time, research products prepared at firm and firm–bank level include only Portuguese firms and credit granted in Portugal.**

[^3]: In addition to Portugal, the countries currently subscribed include Germany, Austria, Belgium, Spain, France, Italy, Czech Republic and Romania.

[^4]: CCR only includes foreign credits originated in the MOU countries (that is, Germany, Austria, Belgium, Spain, France, Italy, Czech Republic and Romania) since 2006. The reporting threshold (25000 euros) in this case is higher than that for firms resident in Portugal (50 euros).
       

# Population

The Central Credit Responsibility (CCR) collects data on the indebtedness of borrowers (including collective persons, individual entrepreneurs and private persons) as reported by credit-granting institutions/participating entities (institutions operating in Portugal or foreign branches of Portuguese banks). For some periods, it also includes credit granted by some foreign entities to Portuguese firms.

The reporting entities participating in CCR include: banks, saving banks, mutual agricultural credit banks, financial credit institutions, leasing companies, factoring companies, securitization companies, mutual guarantee societies, and financial companies for credit acquisitions. Firms subject to credit report include non-financial institutions, as well as non-monetary financial institutions, but it can change across years.

**The firm and firm-bank data exclude:** (1) firms with a non-valid tax identification number; (2) individual entrepreneurs and private persons whose tax identification number starts with a 1, 2 or 8; (3) participating entities classified as mutual guarantee societies (to avoid double counting).

**The credit exposure data exclude:** (1) firms with a non-valid tax identification number; (2) individual entrepreneurs and private persons whose tax identification number starts with a 1 or 2.

Also note that:

- the coverage of borrowers in the CCR has changed over time. Some individual entrepreneurs may still appear in the data because, in 2009, entrepreneurs with tax identification codes starting with 8 were reassigned to codes beginning with 5 or 9 (consistent with firms) or 1 or 2 (consistent with individuals). As a result, discontinuities in the coverage of different types of firms, as well as a noticeable gap in firm entries and exits, can be observed in January 2009.

- some financial institutions in Portugal have experienced acquisitions and/or mergers, which induced credit flows from one institution to another. The list of participating entities has therefore changed over time. 


    
# Methodology {#sec-methodology}

The Central Credit Responsibility (CCR) plays a crucial role in monitoring and assessing credit risk at institution and national level. The participating entities are obliged to report to the Banco de Portugal their credit balances by the end of each month, thus reflecting the situation of the liabilities of their customers by that date. Banco de Portugal is responsible for centralizing and disseminating the credit information after quality control. The identification of the debtors is cross-checked with other sources, ensuring that the identification exists and is valid.[^5]

**To ensure the accuracy of credit reports, banks and financial companies are required to verify and correct any errors promptly. Although the quality of data in the CCR and the coverage of credit exposures have improved over time, some limitations remain due to specific features and changes in the reporting structure.** For instance, credit transfers between participating entities that belong to the same group may cause unusual fluctuations at the level of individual institutions.

The original dataset comprises the credit exposure data, characterized using a predefined set of contractual conditions. All credit obligations above the reporting threshold are included, regardless if the credit is performing, overdue, under litigation or written-off. The mandatory loan registration threshold in Portuguese Credit Responsibility is 50 euros but, in some periods, participating entities have the discretion to report credit below the thresholds.

Between 1999 and 2018, the CCR underwent several major revisions, which introduced structural breaks that may affect empirical analysis. Two revisions are particularly relevant.

The first occurred in 2006, under Banco de Portugal Instruction No. 7/2006, which expanded the reporting framework to include guarantees and effective and potential credit reported by certain foreign central banks on behalf of institutions resident in their jurisdictions.

The second occurred in 2009, under Banco de Portugal Instruction No. 21/2008, and involved: (i) a change in the reporting structure from aggregates by credit type to a more granular exposure level; (ii) the harmonization of coding for several categorical variables and the introduction of new variables, including credit-operation characteristics such as maturity date; (iii) a reformulation of the reporting of guarantees introduced in 2006; among other changes.

**To ensure comparability over time of aggregated variables at the firm and firm–bank levels, we applied a set of harmonization procedures, including restrictions to coverage and the recoding of variables. To understand the applied treatment, users should first refer to the changes in the CCR exposure data, as reflected in the Section [“Description of variables”](#sec-description), and then consult the rules adopted in the construction of the credit amounts for firm and firm–bank datasets, as described in Subsection [“Aggregated credit amounts”](#sec-aggregateamounts).**

[^5]: For instance, the tax identification number (NIF) managed by the Tax and Customs Authority and the National File of Collective Persons (FNPC) managed by the Ministry of Justice are cross checked.

Additional cleaning conducted at BPLIM includes (1) the correction of scale and currency report to ensure that values are always expressed in euros, and (2) the anonymization of participating entities and firms through unique identifiers.


# Description of Files

Three levels of data files are provided: credit exposure (FRMEXP), firm-bank relationships (FRMBNK), and firm-level data (FRM). Each file is organised by year and contains monthly information.[^6] In addition, a supplementary file (COVER) is available for use across all three levels, providing firm characteristics such as legal form, institutional sector, location, and other attributes.


[^6]: Note that some variables are only available after 2009.


## Credit exposure level data (FRMEXP)

Credit exposure data are provided through three files: the general exposure characteristics file (BAL), available for 1999–2018; the collateral information file (COLL), available from 2009–2018; and the special characteristics file (SCHAR), also available from 2009–2018.

The reporting of credit exposures underwent a major structural change in 2009, which explains why only the BAL file is available prior to that year. From 2009 onward, exposures are reported at a more granular level and are identified by an anonymized credit identifier *cina*.


The **general exposure characteristics** files follow the file-naming convention below:

*CRC\_A\_MFRMEXP\_YYYY\_MMMYY\_BAL\_VXX.dta*,

where *YYYY* is the reporting year; *MMMYY* is the extraction date; *VXX* is the version.

   
The **collateral information** files (only available from 2009) report the
collateral type and the collateral value for secured credit. One can merge
the collateral information file with the exposure characteristics file
using the variable *cina*. **One credit exposure *cina* may be associated with more than one collateral.**

The collateral information files follow the file-naming convention below:

*CRC\_A\_MFRMEXP\_YYYY\_MMMYY\_COLL\_VXX.dta,*

where *YYYY* is the reporting year; *MMMYY* is the extraction date; *VXX* is the version.  


The **special characteristics** files (only available from 2009) specify credit
exposures with special characteristics and/or credit exposures extended
according to special regimes, for instance, credit used in a
securitization operation and credit for protecting permanent housing
property (as framed by Decree-Law103/2009). One can merge
the special characteristics file with the exposure characteristics file
using the variable *cina*. One credit exposure may be
associated with more than one special characteristics.

The special characteristics files follow the file-naming convention below:

*CRC\_A\_MFRMEXP\_YYYY\_MMMYY\_SCHAR\_VXX.dta*

where *YYYY* is the reporting year; *MMMYY* is the extraction date; *VXX* is the version.


## Firm-bank level data (FRMBNK)

**Each row corresponds to a firm-bank pair in a given month.**   

The firm-bank level data is organized in the credit outstanding (CO) file that follows the file-naming convention below:

*CRC_A_MFRMBNK_YYYY_MMMYY_CO_VXX.dta*

where *YYYY* is the reporting year; *MMMYY* is the date; *VXX* is the version.

The variables included are:   

- **from 1999 to 2008:** date, tina, bina, valor_global, valor_efectivo, valor_potencial, valor_vencido, valor_curto_o, valor_longo_o;

- **from 2009 onward:** date, tina, bina, valor_global, valor_efectivo, valor_potencial, valor_vencido, valor_curto_o, valor_curto_r, valor_longo_o, valor_longo_r, prazomedia_o, prazomedia_r, valor_prazo1_o, valor_prazo2_o, valor_prazo3_o, valor_prazo4_o, valor_prazo5_o, valor_prazo1_r, valor_prazo2_r, valor_prazo3_r, valor_prazo4_r, valor_prazo5_r, valor_g1, valor_g2, valor_g3, valor_g4, valor_g5, valor_g6.

Note: Firm–bank relationship variables are not included in this data file, but can be generated using the *relationspell* ado.


## Firm level data (FRM)

**Each row corresponds to a firm in a given month.**   

The firm level data is organized in the credit outstanding & bank relationship (COBR) file that follows the file-naming convention below:

*CRC_A_MFRM_YYYY_MMMYY_COBR_VXX.dta*

where *YYYY* is the reporting year; *MMMYY* is the extraction date; *VXX* is the version.

The variables included are the same as in FRMBNK, plus max_relacao, nb_relacao, hhi_relacao.

  
  
## Characteristics of the firm (COVER)

**Each row corresponds to a firm in a given period to which the classification applies.**  

Firm characteristics are provided in the cover file (COVER), which follows the file-naming convention below:

*CRC_A_FRM_MMMYY_COVER_VXX.dta*

where *YYYY* is the reporting year; *MMMYY* is the date; *VXX* is the version.



# Description of Variables {#sec-description}

## Identifiers


-  `Reference date`

The reference month of the data 

+-------------------------------------------------------+--------------------------------+
| Abbreviation                                          | Definition                     |
+:======================================================+:===============================+
| *date*                                                | Reference month of the data    |
+-------------------------------------------------------+--------------------------------+


**Availability**: January, 1999-August, 2018   

<br>   
<br>   

-  `Debtor identifier`

Unique identifier that enables tracking debtors over time.
*tina* is the anonymized tax identification number, available in all files.
 It should be noted that reporting to CCR does not depend on the nationality of the
debtors but their country of residence. In situations where a debtor
is not resident in Portugal and does not have a tax number assigned in
Portugal, the debtor is reported through a unique code generated by the
participating institution itself, namely "Source Code".[^7] Banco de
Portugal controls the credibility of debtor identification in CCR by
cross-checking other sources to ensure that the identification
exists and is valid.

+-------------------------------------------------------+--------------------------------------+
| Abbreviation                                          | Definition                           |
+:======================================================+:=====================================+
| *tina*                                                | Anonymized tax identification number |
+-------------------------------------------------------+--------------------------------------+

**Availability**: January, 1999-August, 2018

<br>   
<br>   

-  `Creditor identifier`

Unique identifier that enables tracking creditors over time. *bina* is the anonymized bank identification number, available in the credit exposure file (EXP) and the bank-firm level credit outstanding file (CO).

+-------------------------------------------------------+-------------------------------------------+
| Abbreviation                                          | Definition                                |
+:======================================================+:==========================================+
| *bina*                                                | Anonymized bank identification number     |
+-------------------------------------------------------+-------------------------------------------+

**Availability**: January, 1999-August, 2018

<br>   
<br>   

-  `Credit exposure identifier`

Identifier for each credit exposure. *cina* is the anonymized credit identification number, only available in the credit exposure file (EXP). For the same credit exposure, **the code changes on a monthly basis and therefore cannot be used to follow a credit through time**. This variable is, however, useful to merge with auxiliary data files of collateral and special characteristics.

+-------------------------------------------------------+--------------------------------+
| Abbreviation                                          | Definition                     |
+:======================================================+:===============================+
| *cina*                                                | Anonymized credit identifier   |
+-------------------------------------------------------+--------------------------------+

**Availability**: January, 2009-August, 2018


[^7]: The use of the Source Code allows compliance with the reporting of a firm/individual’s liabilities resulting from all credit operations. However, the centralization and dissemination of centralized information for debtors reported with Source Code might be limited, since the same debtor will surely have a distinct code communicated by different institutions.

<br>   
<br>   

## Exposure characteristics (credit exposure files only)

-  `Type of credit`

The type of credit, reported in CCR before 2009, characterizes general
credit status. The classification has changed over time. The first
classification regime includes only the codes 1-7, defining different
types of financial instruments. To facilitate further assessment of
credit risk in Portugal, new categories of "credit in litigation" (code
8) and "written-off credit" (code 9) were introduced in January, 1993,
and "renegotiated credit" (code 10) in November, 2001. Later, following
the Instrução nº 7/2006, additional types (codes 11-14) were
incorporated in October, 2006, including guarantees, sureties, and
credit communicated by foreign central banks.

+-------------------------------------------------------+--------------------------------+
| Abbreviation                                          | Definition                     |
+:======================================================+:===============================+
| *tipocredito*                                         | Type of credit                 |
+-------------------------------------------------------+--------------------------------+


**Availability**: January, 1999-December, 2008

+---------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
| Classification                                    | Definition                                                                                                                  |
+:==================================================+:============================================================================================================================+
|  1                                                | Commercial                                                                                                                  |
+---------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  2                                                | Discount funding                                                                                                            |
+---------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  3                                                | Other short term funding                                                                                                    |
+---------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  4                                                | Medium and Long term funding                                                                                                |
+---------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  5                                                | Other responsibilities                                                                                                      |
+---------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  6                                                | Off balance sheet liabilities (potential credit)                                                                            |
+---------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  7                                                | Overdue Credit (non-performing loans)                                                                                       |
+---------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  8                                                | Credit in litigation                                                                                                        |
+---------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  9                                                | Written-off credit                                                                                                          |
+---------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  10                                               | Renegotiated credit                                                                                                         |
+---------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  11                                               | Guarantees provided by participating entities to ensure the compliance of credit operations by other participating entities |
+---------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  12                                               | Guarantees or sureties                                                                                                      |
+---------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  13                                               | Effective credit communicated by foreign banks                                                                              |
+---------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  14                                               | Potential credit communicated by foreign banks                                                                              |
+---------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+

<br>   
<br>   

-  `Responsibility level`

The responsibility level characterizes the type of participation that
the client has in a credit operation, allowing to distinguish between
borrowers and sureties/guarantors and between individual and joint responsibilities.

The credit exposures for a debtor and its sureties/guarantor
 are communicated with identical characteristics,
except for the variables associated with the level of responsibility and
identification of the debtor.

The exposure of the guarantor is reported with characteristics similar
to the secured exposure in all variables except for the followings:
The identification of the party (debtor/guarantor);
The responsibility level;
The credit situation.

This variable is available from 1999 and has undergone a series of
changes in classification, as framed by the Instrução nº 16/2001, the
Instrução nº 7/2006, and the Instrução nº21/2008. To construct a
harmonized series, one can use the ado file provided by BPLIM.

+-------------------------------------------------------+--------------------------------+
| Abbreviation                                          | Definition                     |
+:======================================================+:===============================+
| *nivelresponsabilidade*                               | Responsibility level           |
+-------------------------------------------------------+--------------------------------+

**Availability**: January, 1999-August, 2018

+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
| Classification                                          | Definition                                                                                                                  |
+:========================================================+:============================================================================================================================+
| *from January, 1999 to October, 2001*                   |                                                                                                                   |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  1                                                      | Individual credit                                                                                                           |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  11                                                     | Individual credit - savings-emigrant - acquisition of buildings                                                             |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  12                                                     | Individual credit - savings-emigrant - other activities                                                                     |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  13                                                     | Individual credit - savings-emigrant - buildings + other activities                                                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  2                                                      | Joint credit (credit more than one beneficiary) - 1ºdebtor                                                                  |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  21                                                     | Joint credit 1ºdebtor. - saving-emigrant - acquisition buildings                                                            |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  22                                                     | Joint credit 1ºdebtor. - saving-emigrant - other activities                                                                 |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  23                                                     | Joint credit 1ºdebtor. - saving-emigrant - buildings + other activities                                                     |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  3                                                      | Joint credit (credit more than one beneficiary) - remaining debtors                                                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  31                                                     | Joint credit- remaining debtors - saving-emigrant - acquisition buildings                                                   |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  32                                                     | Joint credit - remaining debtors - saving-emigrant - other activities                                                       |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  33                                                     | Joint credit - remaining debtors - savings-emigrant - buildings+ other activities                                           |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
| *from November, 2001 to September, 2006*                |                                                                                                                   |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  1                                                      | Individual credit                                                                                                           |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  11                                                     | Individual credit - savings-emigrant - acquisition of buildings                                                             |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  12                                                     | Individual credit - savings-emigrant - other activities                                                                     |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  13                                                     | Individual credit - savings-emigrant - buildings + other activities                                                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  14                                                     | Individual credit - credit due to operations of securitization                                                              |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  2                                                      | Joint credit (credit more than one beneficiary) - 1ºdebtor                                                                  |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  21                                                     | Joint credit 1ºdebtor. - saving-emigrant - acquisition buildings                                                            |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  22                                                     | Joint credit 1ºdebtor. - saving-emigrant - other activities                                                                 |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  23                                                     | Joint credit 1ºdebtor. - saving-emigrant - buildings + other activities                                                     |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  24                                                     | Joint credit 1ºdebtor. - credit due to operations of securitization                                                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  25                                                     | Joint credit 1ºdebtor. -  mortgage-backed obligations or obligations in the public sector                                   |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  3                                                      | Joint credit (credit more than one beneficiary) - remaining debtors                                                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  31                                                     | Joint credit- remaining debtors - saving-emigrant - acquisition buildings                                                   |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  32                                                     | Joint credit - remaining debtors - saving-emigrant - other activities                                                       |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  33                                                     | Joint credit - remaining debtors - savings-emigrant - buildings+ other activities                                           |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  34                                                     | Joint credit - remaining debtors - credit due to operations of securitization                                               |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
| *from October, 2006 to December, 2008*                  |                                                                                                                   |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  1                                                      | Individual credit                                                                                                           |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  11                                                     | Individual credit - savings-emigrant - acquisition of buildings                                                             |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  12                                                     | Individual credit - savings-emigrant - other activities                                                                     |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  13                                                     | Individual credit - savings-emigrant - buildings + other activities                                                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  14                                                     | Individual credit - credit due to operations of securitization                                                              |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  15                                                     | Individual credit -  mortgage-backed obligations or obligations in the public sector                                        |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  2                                                      | Joint credit (credit more than one beneficiary) - 1ºdebtor                                                                  |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  21                                                     | Joint credit 1ºdebtor. - saving-emigrant - acquisition buildings                                                            |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  22                                                     | Joint credit 1ºdebtor. - saving-emigrant - other activities                                                                 |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  23                                                     | Joint credit 1ºdebtor. - saving-emigrant - buildings + other activities                                                     |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  24                                                     | Joint credit 1ºdebtor. - credit due to operations of securitization                                                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  25                                                     | Joint credit 1ºdebtor. -  mortgage-backed obligations or obligations in the public sector                                   |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  3                                                      | Joint credit (credit more than one beneficiary) - remaining debtors                                                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  31                                                     | Joint credit- remaining debtors - saving-emigrant - acquisition buildings                                                   |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  32                                                     | Joint credit - remaining debtors - saving-emigrant - other activities                                                       |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  33                                                     | Joint credit - remaining debtors - savings-emigrant - buildings+ other activities                                           |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  34                                                     | Joint credit - remaining debtors - credit due to operations of securitization                                               |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  35                                                     | Joint credit - remaining debtors –  mortgage-backed obligations or obligations in the public sector                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  4                                                      | Joint credit – communicated via foreign channels                                                                            |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
| *from 2009 onward*                                     |                                                                                                                   |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  1                                                      | Individual credit                                                                                                           |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  2                                                      | Joint credit – 1.º debtor                                                                                                   |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  3                                                      | Joint credit – remaining debtors                                                                                            |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  4                                                      | Individual guarantor                                                                                                        |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  5                                                      | Joint guarantor                                                                                                             |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+

<br>   
<br>   

-  `Credit situation`

The credit situation characterizes the exposure as to its current status of usage
and the degree of compliance with the payment of the
credit. For overdue or written-off credit, this variable indicates whether legal proceedings exist and, if so, their validity, enforceability, and stage of enforcement.

This variable is available from 2009 onward and underwent a major change
in classification in June, 2014, framed by the Instrução nº 17/2013.
Specifically, "Overdue credit" (code 3) is thereafter
separated into two distinct exposures, i.e., "Overdue credit" (code 3)
and "Overdue credit in litigation" (code 6). "Written-off credit"
 (code 4) is separated into two distinct exposures,
i.e., "Written-off credit" (code 4) and "Written-off credit in
litigation" (code 7). The harmonization of this variable can be
conducted using the ado file provided by BPLIM.


+-------------------------------------------------------+--------------------------------+
| Abbreviation                                          | Definition                     |
+:======================================================+:===============================+
| *situacaocredito*                                     | Credit situation               |
+-------------------------------------------------------+--------------------------------+

+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
| Classification                                          | Definition                                                                                                                  |
+:========================================================+:============================================================================================================================+
|  1                                                      | Regular credit                                                                                                              |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  2                                                      | Potential Credit                                                                                                            |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  3                                                      | Overdue credit                                                                                                              |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  4                                                      | Written-off credit                                                                                                          |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  5                                                      | Renegotiated credit                                                                                                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  6                                                      | Overdue credit in litigation                                                                                                |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  7                                                      | Written-off credit in litigation                                                                                            |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+

**Availability**: January, 2009-August, 2018


**Notes:**   

- Regular Credit: Credit exposure not yet due, on-balance performing credit.

- Potential Credit: Credit that might become effective in the future. Only irrevocable commitments of participating entities.

- Overdue Credit: Credit exposure that remains unpaid past the due maturity date.

- Written-off Credit: Credit exposure that has become seriously delinquent and the creditor has given up on being paid. 

- Renegotiated Credit: Credit exposure that is overdue and has been renegotiated without additional collateral.             

- Overdue Credit in Litigation: Overdue credit that is filed in court. The classification starts from the initialization of the legal proceedings and ends after the final decision.

- Written-Off Credit in Litigation: Written-off credit that is filed in court. Similarly, the classification should occur since the initialization of the legal proceedings until the final decision.

<br>   
<br>   

-  `Overdue credit class`

This variable is intended to indicate the time elapsed from the time
that a credit enters into default, that is, when the credit situation is denoted as
"overdue credit" or "overdue credit in litigation".

The credit overdue class list is the same as defined for the purposes of
the banking chart of accounts (NCA and PCSB), with only the exception of
the shortest duration classes "up to 3 months", which is further divided
into three classes in the table adopted in CCR ("up to 1 month", "from 1
to 2 months" and "from 2 to 3 months"). In the case when loans are
repaid in varying installments, the total overdue amount of unpaid
installments is communicated in a single overdue credit exposure,
classified in overdue credit class corresponding to the installments
with longer overdue time.

+-------------------------------------------------------+--------------------------------+
| Abbreviation                                          | Definition                     |
+:======================================================+:===============================+
| *classecreditovencido*                                | Overdue credit class           |
+-------------------------------------------------------+--------------------------------+

+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
| Classification                                          | Definition                                                                                                                  |
+:========================================================+:============================================================================================================================+
|  1                                                      | Up to 1 month                                                                                                               |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  2                                                      | From 1 to 2 months                                                                                                          |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  3                                                      | From 2 to 3 months                                                                                                          |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  4                                                      | From 3 to 6 months                                                                                                          |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  5                                                      | From 6 to 9 months                                                                                                          |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  6                                                      | From 9 to 12 months                                                                                                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  7                                                      | From 12 to 15 months                                                                                                        |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  8                                                      | From 15 to 18 months                                                                                                        |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  9                                                      | From 18 to 24 months                                                                                                        |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  10                                                     | From 24 to 30 months                                                                                                        |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  11                                                     | From 30 to 36 months                                                                                                        |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  12                                                     | From 36 to 48 months                                                                                                        |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  13                                                     | From 48 to 60 months                                                                                                        |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  14                                                     | More than 60 months                                                                                                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+


**Availability**: January, 2009-August, 2018

<br>   
<br>   

-  `Maturity`

All credit exposures reported in the CCR after 2009 are classified based
on their original maturity, established in contractual terms, as well as on their
residual maturity, defined as the time interval between the reference
date and the maturity date of the credit agreement. The original term of
the credit characterizes the exposure in relation to
the maturity that was contracted for the full repayment of the credit,
while the residual term of the credit characterizes the exposure in
relation to the maturity between the date to which the communication
refers and the date contracted for the full amortization of the credit.

These two variables are defined in ranges, including a category
"Undetermined" (code 1) which is used to characterize credit exposures
which, by their nature, do not have a contractually defined maturity or
for which it is not possible to determine a due date.

This variable is available from 2009 onward but has undergone a major change
in classification in December, 2013, framed by the Instrução nº 17/2013.
For example, the maturity class "1 to 5 years" (code 5) is only valid
between January, 2009 and November, 2013. From December 2013, this
category is replaced by the maturity class codes 51-54. The same applies
to the maturity class "5 to 10 years" (code 6 replaced by codes 61-65),
and the maturity class "10 to 20 years" (code 7 replaced by codes 71 and
72). The harmonization of this variable can be conducted using the ado
file provided by BPLIM.

+-------------------------------------------------------+--------------------------------+
| Abbreviation                                          | Definition                     |
+:======================================================+:===============================+
| *prazooriginal*                                       | Original maturity              |
+-------------------------------------------------------+--------------------------------+
| *prazoresidual*                                       | Residual maturity              |
+-------------------------------------------------------+--------------------------------+

**Availability**: January, 2009-August, 2018



+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
| Classification                                          | Definition                                                                                                                  |
+:========================================================+:============================================================================================================================+
| *before December, 2013*                                 |                                                                                                                             |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  1                                                      | Undefined                                                                                                                   |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  2                                                      | Up to 90 days                                                                                                               |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  3                                                      | From 90 days to 180 days                                                                                                    |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  4                                                      | From 180 days to 1 year                                                                                                     |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  5                                                      | From  1  to 5 years                                                                                                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  6                                                      | From  5  to 10 years                                                                                                        |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  7                                                      | From  10  to 20 years                                                                                                       |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  8                                                      | From 20 to 25 years                                                                                                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  9                                                      | From 25 to 30 years                                                                                                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  10                                                     | Over 30 years                                                                                                               |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
| *from December, 2013 onward*                           |                                                                                                                             |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  1                                                      | Undefined                                                                                                                   |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  2                                                      | Up to 90 days                                                                                                               |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  3                                                      | From 90 days to 180 days                                                                                                    |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  4                                                      | From 180 days to 1 year                                                                                                     |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  51                                                     | From 1  to 2 years                                                                                                          |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  52                                                     | From 2  to 3 years                                                                                                          |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  53                                                     | From 3  to 4 years                                                                                                          |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  54                                                     | From 4  to 5 years                                                                                                          |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  61                                                     | From 5  to 6 years                                                                                                          |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  62                                                     | From 6  to 7 years                                                                                                          |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  63                                                     | From 7  to 8 years                                                                                                          |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  64                                                     | From 8  to 9 years                                                                                                          |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  65                                                     | From 9  to 10 years                                                                                                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  71                                                     | From 10  to 15 years                                                                                                        |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  72                                                     | From 15  to 20 years                                                                                                        |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  8                                                      | From 20 to 25 years                                                                                                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  9                                                      | From 25 to 30 years                                                                                                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  10                                                     | Over 30 years                                                                                                               |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+

<br>   
<br>   

-  `Financial product`

The financial product characterizes the types
of credit and/or purpose of the credit. In order to facilitate the
classification of credit exposures, the nomenclature used is close to
that adopted in the chart of accounts in accordance with the NCA. The
classification covers 15 different categories covering the most
representative types of credit, based on businesses funding as well as on
individual financing. Some of the financial products are geared to
individual financing while others are mainly for businesses and other
legal persons. For instance, products such as "current account (credit
lines)", "factoring", "real estate leasing" and "financing to the
corporate activity or equivalent" are more geared to finance activities
of firms or other legal persons. Debtors characterized as individual
entrepreneurs may also have credits of typical financial product as
companies do.


+-------------------------------------------------------+--------------------------------+
| Abbreviation                                          | Definition                     |
+:======================================================+:===============================+
| *produto*                                             | Financial product              |
+-------------------------------------------------------+--------------------------------+

**Availability**: January, 2009-August, 2018


+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
| Classification                                          | Definition                                                                                                                  |
+:========================================================+:============================================================================================================================+
|  1                                                      | Discount and other credits secured by effects                                                                               |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  2                                                      | Current account (credit lines)                                                                                              |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  3                                                      | Overdrafts on deposit accounts                                                                                              |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  4                                                      | Recourse factoring                                                                                                          |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  5                                                      | Non-recourse factoring                                                                                                     |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  6                                                      | Real estate leasing                                                                                                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  7                                                      | Non-real estate leasing                                                                                                     |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  8                                                      | Financing to the corporate activity or equivalent                                                                           |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  9                                                      | Credit card                                                                                                                 |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  10                                                     | Mortgage credit                                                                                                             |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  11                                                     | Consumer credit                                                                                                             |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  12                                                     | Automobile credit                                                                                                           |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  13                                                     | Other credit                                                                                                                |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  14                                                     | Bank Guarantees from other participating institutions                                                                       |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  15                                                     | Other bank guarantees                                                                                                       |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+

<br>   
<br>   

-  `Collateral`

As long as the collateral/guarantee exists, it is
mandatory to communicate to CCR its existence together with the credit exposure
that it ensures. The collateral/guarantee is reported to CCR on a
monthly basis, regardless of whether its value changes or not. The
collateral amounts relating to a credit are aggregated by type of collateral using the same
criteria as to the credit exposure.

This variable is available from 2009 onward and it has undergone a
major change in classification in June, 2014, as framed by the Instrução
nº 17/2013. For example, the collateral "Real Collateral Mortgage" (code
1) is only valid in the reporting period between January 2009 and May 2014.
From June 2014, it is replaced by the categories "Real Collateral
Mortgage - Real Estate" (code 11) and "Real Collateral Mortgage --
Other" (code 12). The same applies to the categories "Financial
Collateral" (code 3) which was replaced by the codes 31-39, and
"Personal Guarantee - granted by the State or financial institution"
(code 5) which was replaced by the Codes 51 to 53. The harmonization of
this variable before and after the affecting month can be realized by
using the ado file provided by BPLIM.


+-------------------------------------------------------+--------------------------------+
| Abbreviation                                          | Definition                     |
+:======================================================+:===============================+
| *tipogarantia*                                        | Type of collateral             |
+-------------------------------------------------------+--------------------------------+
| *valorg*                                              | Amount of collateral           |
+-------------------------------------------------------+--------------------------------+

**Availability**: January, 2009-August, 2018


+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
| Classification                                          | Definition                                                                                                                  |
+:========================================================+:============================================================================================================================+
| *before June, 2014*                                     |                                                                                                                             |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  1                                                      | Real collateral mortgage                                                                                                    |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  2                                                      | Real collateral - Not mortgaged                                                                                             |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  3                                                      | Financial collateral                                                                                                        |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  4                                                      | Personal guarantee - Provided by firm or individual                                                                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  5                                                      | Personal guarantee - Granted by the state or financial institution                                                          |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  6                                                      | Other guarantees                                                                                                            |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
| *from June, 2014 onward*                                |                                                                                                                             |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  11                                                     | Real collateral mortgage - Housing                                                                                          |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  12                                                     | Real collateral mortgage - Others                                                                                           |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  2                                                      | Real collateral - Not mortgaged                                                                                             |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  31                                                     | Financial collateral - Deposits                                                                                             |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  32                                                     | Financial collateral – Portuguese public debt                                                                               |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  33                                                     | Financial collateral – Public debt of non-residents and multinational organizations                                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  34                                                     | Financial collateral – Debt of other entities                                                                               |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  35                                                     | Financial collateral – Stocks and other participation in listed companies                                                  |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  36                                                     | Financial collateral – Stocks and other participation in unlisted companies                                                |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  39                                                     | Financial collateral – Other instruments                                                                                    |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  4                                                      | Personal guarantee - Provided by firm or individual                                                                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  51                                                     | Personal guarantee – Granted by the Portuguese State                                                                        |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  52                                                     | Personal guarantee – Granted by other governments or by multinational organizations                                         |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  53                                                     | Personal guarantee – Granted by financial institutions                                                                      |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+
|  6                                                      | Other guarantees                                                                                                            |
+---------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------+

<br>   
<br>   

-  `Special characteristics`

This variable characterizes special regimes to which a credit exposure belongs for
the purpose of performing supervision, financial system stability or
monetary policy analyses. New classifications are introduced over time.
For instance, the Decree-Law No. 103/2009, of 12 May, led to the
creation of a special and temporary credit line, provided by the State,
for the protection of permanent residence in cases that at least one of
the debtors is unemployed (code 10). Credit delivered as collateral for
Eurosystem credit operations (code 11) and credit with an IEB Code (code
12) are introduced according to the Instrução N.º 7/2012. In addition,
the codes 13 to 15 are included as framed by the Instrução 18/2012, the
Instrução 16/2004, the Decree law 227/2012 and the Law 58/2012.

+-------------------------------------------------------+--------------------------------+
| Abbreviation                                          | Definition                     |
+:======================================================+:===============================+
| *caracteristicas*                                     | Special characteristics        |
+-------------------------------------------------------+--------------------------------+

**Availability**: January, 2009-August, 2018


| Classification  | Definition |
|:-----| :------------|
|  1 | Credit conceded in a recognized securitization operation with the intervention of a resident financial vehicle |
|  2 | Credit conceded in a recognized securitization operation with the intervention of a nonresident financial vehicle |
|  3 | Credit conceded in an unrecognized securitization operation with the intervention of a resident financial vehicle |
|  4 | Credit conceded in an unrecognized securitization operation with the intervention of a nonresident financial vehicle |
|  5 | Syndicated loan |
|  6 | Mortgage-backed loan |
|  7 | Public loan |
|  8 | Credit associated with emigrant´s savings accounts for purchasing buildings |
|  9 | Credit associated with emigrant´s savings accounts for other purposes |
|  10 | Credit for protecting permanent housing property ([**Decree-Law103/2009**](./aux_files/legislation/Lei_103-2009.pdf)) |
|  11 | Loan extended as collateral for credit operations in Eurosystem ([**Instruction N.º 7/2012**](./aux_files/legislation/Instrucao_07-2012.pdf)) |
|  12 | Loan featured with identification code (IEB) ([**Instruction N.º 7/2012**](./aux_files/legislation/Instrucao_07-2012.pdf)) |
|  13 | Credit restructured for customers in financial difficulties ([**Instruction 18/2012**](./aux_files/legislation/Instrucao_18-2012.pdf)) |
|  14 | Credit at risk ([**Instruction 16/2004**](./aux_files/legislation/Instrucao_16-2004.pdf)) |
|  15 | Credit in an out-of-course renegotiation procedure (PERSI) ([**Decree-Law No. 227/2012**](./aux_files/legislation/Lei_227-2012.pdf)) or in a Special Regime ([**Law 58/2012**](./aux_files/legislation/Lei_58-2012.pdf)) |

<br>   
<br>   

-  `Credit amount`

This variable identifies the total amount of a credit. For data before 2009, loans of the same debtor and creditor with
identical characteristics are aggregated into a single exposure. Note that regardless of the credit denominated currency, the value of the exposure must always be expressed in euro units.

+-------------------------------------------------------+--------------------------------+
| Abbreviation                                          | Definition                     |
+:======================================================+:===============================+
| *valor*                                               | Credit amount                  |
+-------------------------------------------------------+--------------------------------+

**Availability**: January, 1999-August, 2018

<br>   
<br>   

-  `Bank's branch country`

This variable indicates the country of the branch in which a credit was
granted. **Note that credit granted by foreign branches of Portuguese
banks is only reported after 2009 and in the exposure file. Firm and firm-bank level files do not include data on foreign branches.** Please refer to the Appendix for the [“Country Code List”](#sec-country)

+-----------------------------------------------+--------------------------------------------------------+
| Abbreviation                                  | Definition                                             |
+:==============================================+:=======================================================+
| *paisbalcaoid*                                |Bank\'s branch country                                  |
+-----------------------------------------------+--------------------------------------------------------+

**Availability**: January, 2009-August, 2018

<br>   
<br>   

-  `Base currency`

After 2009, information on whether the credit was granted in a different
currency is provided. This variable is denoted using 3-digit ISO currency code (ISO 4217).The value of the credit (*valor*) is always reported in
euros. Please refer to the Appendix for the [“Currency Code List”](#sec-currency)

+-----------------------------------------------+--------------------------------------------------------+
| Abbreviation                                  | Definition                                             |
+:==============================================+:=======================================================+
| *moeda*                                       |Base currency                                           |
+-----------------------------------------------+--------------------------------------------------------+

**Availability**: January, 2009-August, 2018

<br>   
<br>   

## Aggregated credit amounts (firm and firm-bank files) {#sec-aggregateamounts}

The aggregated variables, constructed at both the firm and firm–bank levels, are derived from exposure-level data on outstanding and written-off credit and follow a common set of computation rules:

- **before 2009**: (1) includes credit exposures classified with *nivelresponsabilidade* 1 to 3; (2) excludes guarantees reported as *tipocredito* 11-12; (3) excludes credit communicated by foreign central banks and reported as *tipocredito* 13-14; (4) excludes mutual guarantee societies reporting (to avoid double counting).   


- **from 2009 onward**: (1) includes credit exposures classified with *nivelresponsabilidade* 1 to 3; (2) excludes guarantees reported as *produto* 14-15; (3) excludes credit granted outside Portugal and reported as *paisbalcaoid* "PRT"; (4) excludes mutual guarantee societies reporting (to avoid double counting).   

<br>   
<br>   

-  `Global Credit`

Global credit is defined as the sum of effective credit (regardless of whether it is on- or off-balance, performing, or overdue) and potential credit. The aggregation rule is:

- *Global Credit = Effective Credit + Potential Credit*

+-----------------------------------------------+--------------------------------------------------------+
| Abbreviation                                  | Definition                                             |
+:==============================================+:=======================================================+
| *valor_global*                                |Total available credit that a firm can access           |
+-----------------------------------------------+--------------------------------------------------------+

**Availability**: January, 1999-August, 2018

<br>   
<br>   

-  `Effective Credit`

Effective credit refers to the total credit regardless of whether it is performing, overdue, in litigation, or written off, and excludes potential credit. The aggregation rule is:

- **before 2009**: includes tipocredito 1-10, except for tipocredito 6 (potential credit)

- **from 2009 onward**: includes situacaocredito 1-7, except for situacaocredito 2 (potential credit)


+---------------------------------------------------------------+--------------------------------------------------------+
| Abbreviation                                                  | Definition                                             |
+:==============================================================+:=======================================================+
| *valor_efectivo*                                              | Credit that a firm used effectively                    |
+---------------------------------------------------------------+--------------------------------------------------------+

**Availability**: January, 1999-August, 2018

<br>   
<br>   

-  `Potential Credit`

Potential credit represents the irrevocable commitments of participating entities that may become effective credit in the future. Revocable credit obligations are excluded, although certain breaks in the data series may occur. Please see the notes below. The aggregation rule is:

- **before 2009**: includes tipocredito 6 (potential credit)

- **from 2009 onward**: includes situacaocredito 2 (potential credit)


+---------------------------------------------+--------------------------------------------------------------------------------------------------------------+
| Abbreviation                                | Definition                                                                                                   |
+:============================================+:=============================================================================================================+
| *valor_potencial*                           | Credit that a firm can access because of irrevocable commitments of the participating entities               |
+---------------------------------------------+--------------------------------------------------------------------------------------------------------------+

**Availability**: January, 1999-August, 2018

**Examples of potential credit**: Irrevocable unused amounts of credit cards or lines of credit.                                                       

**Notes**: Banco de Portugal requires the reporting of irrevocable credit obligations only, which in principle implies the exclusion of revocable obligations. **However, several discontinuities in the data series affect the reporting of potential credit and should be taken into account:**

1. Aviso no 5/2007 introduced differentiated risk-weighted assets for revocable and irrevocable credit obligations. This regulatory change created incentives for financial institutions to shift towards revocable credit, which may partly explain the observed decline in reported potential credit.

2. Instruction 21/2008 changed the structure of the Central Credit Register (CCR) reporting, moving from aggregate credit data by type of credit to a more detailed credit reporting. This change is likely to have affected the recorded split between revocable and irrevocable obligations.

3. Despite reporting guidelines, some institutions continued to report revocable credit. In particular, one institution ceased reporting revocable credit card obligations in May 2013, leading to a break in the series.

<br>   
<br>   

-  `Overdue Credit`

All credit exposures recorded as non-performing (including overdue, written-off, renegotiated credit, overdue credit in litigation, and written off credit in litigation) are aggregated to calculate overdue credit. It includes principal, interest and related fees. The aggregation rule is:

- **before 2009**: includes tipocredito 7-10 (overdue, in litigation, written-off, and renegotiated)

- **from 2009 onward**: includes situacaocredito 3-7 (overdue, written-off, renegotiated, overdue in litigation, written-off in litigation)


+---------------------------------------------------------+------------------------------------------------+
| Abbreviation                                            | Definition                                     |
+:========================================================+:===============================================+
| *valor_vencido*                                         | Non-performing credit of a firm                |
+---------------------------------------------------------+------------------------------------------------+

**Availability**: January, 1999-August, 2018

<br>   
<br>   

-  `Short-term Effective Credit`

**Short-term credit is derived from effective credit**, includes credit with a maturity of one year or less, and can be defined using two alternative concepts: original maturity (*valor_curto_o*) and residual maturity (*valor_curto_r*). **A structural break occurs in 2009 due to a change in the underlying data construction.**

- **before 2009**: the CCR dataset did not report maturity information. Short-term credit is therefore defined as the sum of commercial credit, discount funding, and other inherently short-term funding, and can only be computed based on original maturity (*valor_curto_o*).

- **from 2009 onward**: the CCR reports contractual maturity by ranges, allowing short-term credit to be computed using contract information.

| Abbreviation  | Definition |
|:-------| :------------|
| *valor_curto_o* | Credit with an original maturity of less than or equal to 1 year |
| *valor_curto_r* | Credit with a residual maturity of less than or equal to 1 year  |


**Availability**: January, 1999-August, 2018 for *valor_curto_o*; January, 2009-August, 2018 for *valor_curto_r*

<br>   
<br>   

-  `Long-term Effective Credit`

**Long-term credit is derived from effective credit**, includes credit with maturity of over one year, and can be defined using two alternative concepts: original maturity (*valor_longo_o*) and residual maturity (*valor_longo_r*). **A structural break occurs in 2009 due to a change in the underlying data construction.**

- **before 2009**: the CCR dataset did not report maturity information. Long-term credit is therefore defined as the sum of total credit excluding commercial credit, discount funding, and other inherently short-term funding, and can only be computed based on original maturity (*valor_longo_o*).

- **from 2009 onward**: the CCR reports contractual maturity by ranges, allowing long-term credit to be computed using contract information.


| Abbreviation  | Definition |
|:-------| :------------|
| *valor_longo_o* | Credit with an original maturity of more than 1 year |
| *valor_longo_r* | Credit with a residual maturity of more than 1 year |


**Availability**: January, 1999-August, 2018 for *valor_longo_o*; January, 2009-August, 2018 for *valor_longo_r*

<br>   
<br>   

-  `Weighted average debt maturity`

**Weighted average debt maturity is derived from effective credit** and is available from 2009 onward for original and residual maturity. Please refer to the notes below for details on how it is computed.


| Abbreviation  | Definition |
|:---------| :------------|
| *prazomedia_o* | The weighted average original debt maturity |
| *prazomedia_r* | The weighted average residual debt maturity |


**Availability**: January, 2009-August, 2018

**Notes:** All credit exposures reported in the CCR after 2009 are classified based on their original maturity, established in contractual terms, and residual maturity, defined as the time interval between the reference date and the maturity date of the credit agreement. In other words, the original term of the credit characterizes the exposure in relation to the maturity that was contracted for the full repayment of the credit, while the residual term of the credit characterizes the exposure in relation to the maturity between the date to which the communication refers and the date contracted for the full amortization of the credit.

These two variables are defined in ranges, including a category “Undetermined” (code 1) which is used to characterize credit exposures that, by their nature, do not have a contractually defined maturity or for which it is not possible to determine a due date. In addition, the reporting of debt maturity has undergone a major change in classification in December, 2013. For example, the maturity class “1 to 5 years” (code 5) is only valid between January, 2009 and November, 2013. From December 2013, this category is replaced by the maturity class codes 51-54. The same applies to the maturity class “5 to 10 years” (code 6 replaced by codes 61-65), and the maturity class “10 to 20 years” (code 7 replaced by codes 71 and 72).

Due to these specificities, we adopt the following procedure:

- Firstly, we harmonize the debt maturity information after December, 2013 using the classification of September, 2009 as the latter is less disaggregated than the former.

- Secondly, we assign the midpoint maturity for each maturity classification (0.5 years for maturity less than or equal to 1 year; 3 years for maturity more than 1 year and less than or equal to 5 years; 7.5 years for maturity more than 5 years and less than or equal to 10 years; 15 years for maturity more than 10 year and less than or equal to 20 years; 22.5 years for maturity more than 20 year and less than or equal to 25 years; 27.5 years for maturity more than 25 year and less than or equal to 30 years). We assign an average value of 40 years for credit maturing in more than 30 years.

- Thirdly, we calculate the average debt maturity, weighted by the credit outstanding with the corresponding maturity.

- Lastly, we reassign a maturity class to the calculated weighted average maturity value:

| Maturity Class | Definition |
|:-------| :------------|
|  1 | Credit with a calculated weighted average maturity of less than or equal to 1 year |
|  2 | Credit with a calculated weighted average maturity of more than 1 year and  less than or equal to 5 years |
|  3 | Credit with a calculated weighted average maturity of more than 5 years and less than or equal to 10 years |
|  4 | Credit with a calculated weighted average maturity of more than 10 years and  less than or equal to 20 years |
|  5 | Credit with a calculated weighted average maturity of more than 20 years |


<br>   
<br>   

-  `Credit by maturity structure`

From 2009 onward, we breakdown the amount of credit using various maturity classifications, as illustrated below.

| Abbreviation  | Definition |
|:-------| :------------|
| *valor_prazo1_o* | Credit with an original maturity of less than or equal to 1 year |
| *valor_prazo2_o* | Credit with an Original maturity of more than 1 year and  less than or equal to 5 years |
| *valor_prazo3_o* | Credit with an Original maturity of more than 5 years and less than or equal to 10 years |
| *valor_prazo4_o* | Credit with an Original maturity of more than 10 years and  less than or equal to 20 years |
| *valor_prazo5_o* | Credit with an Original maturity of more than 20 years |


**Availability**: January, 2009-August, 2018

| Abbreviation  | Definition |
|:-------| :------------|
| *valor_prazo1_r* | Credit with a residual maturity of less than or equal to 1 year |
| *valor_prazo2_r* | Credit with a residual maturity of more than 1 year and  less than or equal to 5 years |
| *valor_prazo3_r* | Credit with a residual maturity of more than 5 years and less than or equal to 10 years |
| *valor_prazo4_r* | Credit with a residual maturity of more than 10 years and  less than or equal to 20 years |
| *valor_prazo5_r* | Credit with a residual maturity of more than 20 years |            


**Availability**: January, 2009-August, 2018

<br>   
<br>   

-  `Secured credit by collateral type`

From 2009 onward, we calculate the amount of secured credit broken down by collateral type.

+-------------------------------------------+-----------------------------------------------------------------------------------------+
| Abbreviation                              | Collateral Type                                                                         |
+:==========================================+:========================================================================================+
| *valor_g1*                                | Credit secured by real collateral mortgaged                                             |
+-------------------------------------------+-----------------------------------------------------------------------------------------+
| *valor_g2*                                | Credit secured by real collateral not mortgaged                                         |
+-------------------------------------------+-----------------------------------------------------------------------------------------+
| *valor_g3*                                | Credit secured by financial collateral                                                  |
+-------------------------------------------+-----------------------------------------------------------------------------------------+
| *valor_g4*                                | Credit secured by personal guarantee provided by firm or individual                     |
+-------------------------------------------+-----------------------------------------------------------------------------------------+
| *valor_g5*                                | Credit secured by personal guarantee granted by the state or financial institution      |
+-------------------------------------------+-----------------------------------------------------------------------------------------+
| *valor_g6*                                | Credit secured by other guarantees                                                      |
+-------------------------------------------+-----------------------------------------------------------------------------------------+

**Availability**: January, 2009-August, 2018

<br>   
<br>   


## Bank relationship (firm file only)

The bank relationship variables are only available in the firm level file, but can be obtained from the firm-bank level file using the *relationspell* ado provided by BPLIM. The definition of relationship considers all types of credit, including potential.

<br>   
<br>   

-  `Number of bank relationships`

This variable measures the size of a firm’s bank relationships. Precisely, we calculate the number of active bank relationships, i.e., the number of banks from whom a firm is able to borrow in a specific month. It means that unused credit (potential) is also taken into account in the calculation of bank relationships.

<br>   
<br>   

-  `Largest bank relationship`

This variable features the borrowing from a firm´s major bank. It is measured as the percentage of a firm´s available credit from the major bank to the firm´s total available credit (valor_global).

<br>   
<br>   

-  `Concentration of bank relationships`

The concentration of bank relationship is calculated using the Herfindahl–Hirschman Index as the sum of the squares of the bank lending share for a firm.

+------------------------------------------------+---------------------------------------------------------------------------+
| Abbreviation                                   | Definition                                                                |
+:===============================================+:==========================================================================+
| *nb_relacao*                                   | The number of active bank relationships of a firm                         |
+------------------------------------------------+---------------------------------------------------------------------------+
| *max_relacao*                                  | The largest bank relationship (in percentage terms) of a firm              |
+------------------------------------------------+---------------------------------------------------------------------------+
| *hhi_relacao*                                  | The concentration of a firm's bank relationships                          |
+------------------------------------------------+---------------------------------------------------------------------------+


## Firm characteristics (cover file only)

Firm characteristics are available exclusively in the cover file and can be merged with any of the three proposed levels of credit data files. Note that these characteristics are time-varying; therefore, the corresponding mindate and maxdate must be taken into account.

Available variables: tina,  natjur, cae21, cae3, district, municipality, si, si_final, mindate, and maxdate.



# Building Compatible Series Using Credit Exposure Data

For internal researchers interested in building consistent time series using
the exposure level data, there are a few caveats that are important to
keep in mind.


## Relevant filters

-   Aggregate series of credit should consider *nivelresponsabilidade* 1, 2 and 3. However, in earlier periods, misreporting may have caused duplication of credit in cases of joint responsibilities.

-   The variable *si* and *si\_final* classifies firms according to
    institutional sector at the moment of the data. As some firms may
    have changed from one sector to the other, in order to implement a
    consistent sample selection (such as non-financial firms), it is
    usually recommended to keep the most recent classification only or
    only firms that never switched sectors.

-   It is only possible to create a consistent series for credit granted
    domestically, regardless of the firm's country of origin (which is
    only identifiable after 2009). Therefore, when creating aggregate
    series, only loans with *paisbalcaoid* equal to "PRT" should be
    included.
  
- Mutual guarantee societies report potential credit related to the loans they guarantee. This credit is converted into effective credit only if the original obligation is settled, which may result in double counting when considered as potential credit. It is therefore recommended to exclude mutual guarantee societies from the series.

- Guarantees are not reported consistently over the entire period. Their inclusion should be reconsidered depending on the research objective.

- Between 2006 and 2008, credit exposures reported by foreign central banks are included. Consider excluding them by filtering for tipocredito 13–14.
   
   
## Compatibility issues

Definitions of the variables in CCR changed over time. To build
compatible time series, it is important to harmonize the data.[^10]


### Credit situation

The variable of credit situation is not available before 2009. To
construct the time series for "credit situation" before 2009, one will
need to use the following correspondence table between the variable
"type of credit" (*tipo*) and the variable "credit situation"
(*situacaocredito*).

[^10]: One can fulfill this step using an ado file available at BPLIM.


**Correspondence table between "type of credit" (before 2009) and "credit situation" (2009 onward)**

| |  **January, 1999-December, 2008**  | |**January, 2009-present**|
|:--------|:----------------|:--------|:---------------|
|Code | Type of Credit| Code | Credit Situation|
|1    |Commercial|    1|    Regular|
|2|    Discount funding|    1    |Regular|
|3    |Other short term funding|    1|    Regular|
|4    |Medium and Long term Funding|    1    |Regular|
|5    |Other responsibilities|    1|    Regular|
|6    |Off balance sheet liabilities (potential credit)|    2|    Potential|
|7    |Overdue Credit (non-performing loans)|    3    |Overdue|
|8    |Credit in litigation|    6    |Overdue in litigation|
|9    |Written-off credit    |4    |Written-off credit|
|10    |Renegotiated credit|    5    |Renegotiated credit|
|11    |Guarantees    | not coded |
|12    |Guarantees or sureties    | not coded |
|13    |Effective credit communicated by foreign banks|   not coded |
|14    |Potential credit communicated by foreign banks|   not coded |


Some reporting specificities also need to be noted in order to construct
compatible series of credit.

- Credit exposures may have different states regarding their credit situation. A special caveat needs to be noted for "potential credit" (code 2), which is credit granted but not yet used, corresponding to lines of credit, or other irrevocable commitments by the credit institution. The credit exposures of guarantors and guarantors are also characterized using this code, except in cases where they are in default.

- The classification of overdue credits has implications for other characteristics of the exposure, because (1) credit in this situation is required to identify the overdue credit class and (2) the residual maturity should always be classified as "undetermined". In the case that guarantors are required to replace the debtors in the payment of credit, the participating entity informs the credit situation and set a deadline for the payment of the claim. If payment is not made within the deadline, the institution will report a situation of in-default, i.e. the credit exposure associated with that guarantee is no longer reported in situation "potential credit" (code 2) but is now reported as "overdue credit" (code 3).

- Renegotiated credit was classified as overdue at some point in the past and, at the discretion of the reporting bank, classified as renegotiated. This renegotiation may correspond to changes in loan characteristics (in particular maturity extension and interest payment reduction), but does not imply involvement of the firm. If these loans are paid regularly, they are then reclassified as regular credit after 6-12 months (depending on the bank). To identify restructured loans, it is preferable to use the special characteristic (*caracteristicas*).

- In case of having renegotiated the terms of credit payment in
regular situation, the respective exposures continue to be reported
as \"regular credit\" (code 1) instead of "renegotiated credit"
(code 5). The same rule applies to the renegotiation of credit
payment leading to a new contract or major changes, for example,
addition of new collateral. Another aspect to be noted regarding
the communication of credits in this situation refers to other
actors other than the debtor, for example, guarantors. When the
debtor\'s credit exposure is classified as renegotiated loans (in
credit institution), the exposure relative to the responsibilities
of the guarantor, which was classified as overdue loans, will be
re-classified as a potential credit (code 2). In the case of joint
credits, the rules for the debtors of individual loans applies to
all debtors involved.

- The criteria for classifying credit as written-off is left to the discretion of the reporting institutions, so that while some banks may report written-off credit for a few months and then remove it from the CCR, others have a policy of never removing it. The values in written-off and renegotiated credit often correspond to overdue interest payments and not overdue installments or principal reductions. There are a few institutions, such as restructuring funds, which purchase non-performing loans and then revise the report to the CCR. When they do so, a number of characteristics may change, in particular the overdue amount may seem to go up due to the addition of the accumulated overdue interest payments which are not routinely reported to the CCR.

- For the classification of "overdue credit in litigation", the following aspects must be noted:

  -  The initiation of the action corresponds to the date on which the
    institution filed the action in court, or the date of notification
    of the institution in the case of the action being filed by third
    parties;

  -   The closure of the proceeding is considered as the date when major
    legal sequence is offered, and can be considered as a reference to
    the date of the transition to the final juridical decision;

  -   All overdue loans whose existence, validity or enforceability is
    subject to the jurisdiction of the courts should be considered as in
    litigation;

  -   In the cases when a third party triggers a juridical process and the
    credit exposure is found overdue, this should be reported as overdue
    loans in litigation;

  -   In an insolvency proceedings - a universal implementation process
    that may call the credit feasibility into question, an overdue
    exposure of a debtor in insolvency proceedings should be classified
    as overdue credit in litigation;

  -   For an overdue credit in litigation for which there is still a part
    in good standing, this part should be reported as "1 - regular
    credit", while the overdue part should be reported as "6 - overdue
    loans in litigation".


- For written-off credits, the following aspects must be noted:


  -   The initiation of the action corresponds to the date on which the
    institution placed the action in court, or the date of notification
    of the institution in the case of the action being filed by third
    parties;

  -   The closure of the proceeding is considered as the date when major
    legal sequence is offered, and can be considered as a reference to
    the date of the transition to the final juridical decision;

  -   All overdue loans whose existence, validity or enforceability is
    subject to the jurisdiction of the courts should be considered as in
    litigation

  -   In the cases where a third party triggers a juridical process and
    the credit exposure is found written off, this should be reported as
    written-off loans in litigation;

  -   In an insolvency proceedings - a universal implementation process
    that may call the credit feasibility into question, a written-off
    exposure of a debtor in insolvency proceedings should be classified
    as written-off credit in litigation;
  
  -   The classification in question does not provide any detail as to the
    characteristics of litigation in progress.
   

### Debt maturity

Concerning the characterization of the contractual and residual
maturity, some rules must be noted, in particular:

- The original maturity is usually equal to or greater than the
residual maturity, with only the exception of renegotiated credits (for
example, the maturity is extended);

- The category "Undetermined" (code 001) is only used when the original
maturity is unknown or is not contractually agreed (for example, credit
lines). An "Undetermined" original maturity also implies an
"Undetermined" residual maturity;

- The credits in overdue or written off situations, including those in
litigation are always assigned an "Undetermined\' residual maturity,
regardless of the original maturity.

Some financial products, by their nature, may not have a defined
maturity date contract, such as "current account (credit lines)" (code
2), "overdrafts on deposit accounts" (code 3) and credit card (code 9).
In this situation, the variables "original maturity" and "residual
maturity" shall be communicated with the code 1 (Undetermined).


### Exposure restructuring

It is possible that in some cases, the same credit is divided into more
than one exposure. Please see the following examples:

-   Considering a line of credit or credit card for which part of the
    exposure is effectively used at the end of the month. The
    information communicated to the CCR is in two exposures: one in the
    amount corresponding to the portion used, classified as "regular
    credit", and the other in the amount corresponding to the unused
    portion, classified as "potential credit", given that it corresponds
    to the institution\'s credit commitment;

-   Considering a fully utilized credit with a periodic amortization
    schedule, with some installments overdue and the remaining part
    regular. It is necessary to communicate to the CCR two exposures:
    one in the amount corresponding to the overdue part for accounting
    purposes, and the other corresponding to the remaining part,
    classified as "regular credit";

-   Considering an overdue credit in which there was some room for a
    renegotiation between the lending institution and the borrower for
    the payment terms of the overdue part. It is necessary to
    communicate to CCR two exposures: one in the amount corresponding to
    the regular part, classified as "regular credit", and the other
    corresponding to the renegotiated part, classified as "renegotiated
    credit". While the agreed payment terms are respected and the
    overdue part have not been written down, the communication of the
    outstanding exposure to the CCR follows this rule.
   

### Special characteristics

Each credit exposure may be associated with more than one special
characteristics. However, by its nature, the coexistence of certain
special features are not allowed on the same exposure credit. For
instance, a credit used in a securitization operation (codes 1 to 4)
cannot be used as collateral in the issuance of mortgage covered bonds
or public sector bonds (code 6 or 7); a credit used as collateral in the
issuance of mortgage covered bonds (code 6) cannot be used
simultaneously as collateral of public sector bond (code 7); a credit
used in a securitization operation (codes 1 to 4) or as collateral of
mortgage covered bonds or as collateral of public sector bonds (code 6
or 7) cannot be delivered as collateral for Eurosystem credit operations
(code 11); an integrated credit in PERSI or Special Regime (code 15)
cannot be delivered as collateral for Eurosystem credit operations (code
11).
  

### Guarantor

Credit liabilities guaranteed by surety or guarantor are identified by
collateral classification - *tipoidentificacao* as "personal guarantees"
(codes 4 to 53). However, this classification is not sufficient for
identifying the respective guarantors and sureties. The responsibilities
assumed by guarantors and sureties are also reported in separate
registers, with the identical characteristics except for the following
variables:

-   Level of responsibility, which has the code "4" or "5", depending on
    whether the guarantor/surety is individual or conjoint;

-   Credit situation, which will have the code "2" (potential credit),
    except as described in 2.3;

-   Value, which should correspond to the amount that the
    guarantor/surety is contractually obligated to secure and can be
    different from the original exposure.

It is important to note that a guarantee or surety is never communicated
without the associated credit exposure being also reported. When there
is more than one entity to provide guarantees or sureties to the same
credit, the exposures of credit liabilities associated with all
guarantors and sureties are communicated to the CCR. In cases when a
borrower fails to meet its payment obligations and there is a guarantor
(surety or guarantor) associated with that contract, the credit
institution will notify the guarantor of the situation and set a
deadline for it to proceed to payments due by the debtor. This may
result in the following situations:

-   The guarantor fully liquidates the loan, thereby
    stopping any report to the CCR regarding the loan in question (on
    behalf of the borrower, and on behalf of guarantor/surety);

-   The guarantor fully liquidates the overdue part of the
    loan. In this situation, CCR only ceases to report the
    exposure in default. The outstanding exposure continues to be
    reported on behalf of the borrower as "regular credit" and the
    exposure associated with the guarantor/surety will be reported as
    "potential credit";

-   The guarantor pays the loan installments regularly, instead of the
    debtor </u>. In this situation, reporting on the
    guarantor/surety remains regarding the characterization of credit
    liabilities, that is, the *level of responsibility* equal to "4"/"5"
    but the *credit* *situation* will be equal to "1". However, if the
    underlying "financial product" requires the communication of
    "monthly installment", this credit exposure should continue to be
    reported on behalf of the debtor and on behalf of the guarantor.
    This situation must ensure that the guarantor/surety respects the
    established amortization plan. So the report for the debtor will be:
    "*Responsibility Level*" = 1 (if it is an individual credit) and
    "Credit Situation" = 1 (if it is an effective credit). [^11]

If the guarantor/surety fails to fulfill its obligations after
notification by the credit institution and after a reasonable period for
the regularization of non-compliance, the report concerning the
guarantor would be: "Responsibility level" = 4 or 5 and "Credit
Situation" = 3 (overdue loans). Regarding the borrower, the report will
continue to be: "Responsibility level" = 1 (if it is an individual
credit) and "Credit Situation" = 3 (overdue loans). Note that the
existence of such periods for the guarantor before passing to report the
situation of overdue credit is ensured by the participating
institutions.

The situation exemplified above has two variants: the case when the
credit was written off and the case when there is renegotiation of
credit after default. Regarding the variable "credit situation", the
credit claims with personal guarantees or guarantees can be schematized
as follows, considering the two types of actors (debtor and guarantor
/surety):

[^11]: This classification of credit situation is based on the principle that overdue credit should not be reported to the CCR if not, for accounting purposes, classified as such. Although in this situation the borrower is not fulfilling its obligations, someone is fulfilling for him due to contractual conditions of the loan. As a result, the credit is not classified as overdue.


**Credit situation report on claims with personal guarantees or guarantees**


|**Exposure in debtor’s name**|**Exposure in guarantor’s name**| **Observations**|
|:-----------|:-----------|:--------------------|
|1 - Regular Credit| 2 - Potential Credit| There is no default. |
|1 - Regular Credit| 2 - Potential Credit | There has been default of the debtor, and the guarantor paid the benefits due. The debtor assumed the payment of future installments, with no renegotiation of credit. |
|1 - Regular Credit|1 - Regular Credit|There has been default of the debtor, and the guarantor paid the overdue installments and also assumed the payment of future installments, with no renegotiation of credit. |
|3 - Overdue Credit|2 - Potential Credit |Default of the debtor but the guarantor has not been notified of the breach or the guarantor has been notified of the breach and its obligation to settle but the deadline for the settlement is not exhausted. |
|3 - Overdue Credit|3 - Overdue Credit|The guarantor has been notified of the default and did not pay any debt portion within the set deadline. |
|4 – Written-off credit |4 – Written-off credit |Identical to the previous case but the debt has already been written off. |
|5 – Renegotiated credit |2 - Potential Credit |Renegotiated debt, after the default of the debtor, and the agreed terms are being met. |


It is important to note that regarding the reporting of responsibilities
of guarantors and sureties, the variable "responsibility level" will
always be coded as "4" (surety or guarantor - individual) or "5"
(guarantor or guarantor - joint), regardless whether the guarantor has
to ensure the total or partial repayment of the secured loan.


### Collateral

Each credit exposure may be associated with more than one type of
collateral and the value of the collateral corresponds to the value of
each type of collateral associated with the credit exposure. The
valuation of collateral depends on the type of collateral.

Regarding the real collateral, financial collateral, or other collateral
(codes 1- 39 and 6), the value of the collateral corresponds to the fair
value of the underlying asset (registered accounting value) and can
therefore be distinguished from credit amount. In the case of a mortgage
real collateral, its value will be limited by the mortgage amount and
may be less than the outstanding credit amount.

In the case of personal guarantees (codes 4 - 53), since these
correspond to a commitment to pay debt by third parties in the event of
default by the debtors, the collateral value should be updated as a
function of the outstanding value of the credit. The collateral can be
higher than the value of the outstanding credit if the guarantee is also
associated with the overdue interest and related expenses or with
potential credit.

In the case of financial leasing, the value of the associated collateral
(non-mortgage real collateral) is assessed by the financial institution.


**Special cases:**


-   When the same asset is used as a collateral to more than one loan

    In the case where the same asset or good is used as collateral for more than one loan which has different characteristics, i.e., they are reported to the CCR in more than one exposure of responsibilities, the guarantee amount shall be distributed proportionally by the different exposures, according to the outstanding amounts of each one.

-   When a loan is guaranteed by more than one asset

    In the case where a loan is secured by more than one asset (e.g., debt securities, stocks, deposits, \...), communication of this exposure to the CCR shall include the characterization of different types of collaterals and the corresponding values, using the valuation rules mentioned above. In this situation, the sum of the collateral values attached to the loan may be different (lower or higher) from the credit value.

-   When a guaranteed loan has an overdue part and a due part

    For collateralized loans for which one part is overdue and the other part due, two separate exposures are communicated to the CCR. If possible, the collateral value is also distributed by the two components in order to fully cover the value of the overdue part, and the remaining affecting the due part.


### Additional concerns

Also, as CCR only obliges the reporting of the full position of each debtor, it is sometimes difficult to unambiguously identify each
individual credit exposure for the same debtor. This restriction has
repercussions in the process of modifying or correcting the reported
credit exposures. For example, one may observe a split in credit
exposure from a month to another, which can happen when a bank
restructure the loan, e.g., one part of the loan becomes overdue.

<u> **Comment** </u>: The inclusion of some variable categories
does not always corresponds to the effective dates as defined in
legislation. For instance, for the variable "type", the classification
"10" comprises overdue credit that has been renegotiated, which was
requested to report from July, 2001. Yet, the series appeared already in
January, 2001, although it was only with one exposure. Loans that were
extended as collateral for credit operations in Euro system and loans
featured with IEB identification code were started to be reported in
September, 2010 and in April, 2011, respectively. But it was only until
November, 2012 that these two credit exposures were systematically
reported.


# Legislation

Variable definitions changed over time. Some variables, for instance, credit situation (*situacaocredito*), maturity (*prazooriginal* and *prazoresidual*), and collateral type (*tipogarantia*) have undergone major changes in classification, as framed by *Banco de Portugal*’s instructions. It is important to note that even small changes may require a infrastructural update on the part of the participating financial entities, possibly leading to a gradual implementation of the instruction even though legally all the entities should implement the instructions at the same time.
Below is a list of relevant legislation:


-    [**Decree-Law no. 47909/1967**](./aux_files/legislation/Decreto-Lei_47909.pdf), September 7 and [**Decree-Law no. 48731/1968**](./aux_files/legislation/Decreto-Lei_48731.pdf), December 4 - established the service of centralizing and disseminating credit risk information and defines its purpose and operation, given the need of credit and other financial institutions to properly assess the risks of their operations.

-    [**Carta Circular no 29/96/DOC**](./aux_files/legislation/Carta-Circular_29-96-DOC.pdf), September 18 – eliminated credit classes associated with *empréstimos de poupança-crédito*, which are now classified as *empréstimos de poupança-emigrante* (the conversion of savings-credit loans into savings-immigrant loans).

-    [**Decree-Law no. 5/1998**](./aux_files/legislation/Lei_5-1998.pdf), January 31 – amended the Organic Law of *Banco de Portugal*, with a view to its integration into the European System of Central Banks.

-    [**Decree-Law no. 67/1998**](./aux_files/legislation/Lei_67-1998.pdf), October 27 – transposed the Directive 95/46/CE of the European Parliament and the Directive of the Council in 24-10-1995 on the protection of individuals in processing and circulating data.

-    [**Instrução no. 16/2001**](./aux_files/legislation/Instrucao_16-2001_full.pdf) – reviewed the separation of potential from actual amounts of credit.

-    [**Instrução no. 11/2002**](./aux_files/legislation/Instrucao_11-2002.pdf) – establishment of a 90 day period to register a credit exposure (*sem direito de regresso*) or overdue credit (*com direito de regresso*) after invoices are due; revocable commitments (code 921) are  no longer reported as a credit of type 6 (off balance sheet commitments); factoring credit more than 90 days overdue reported as type 7 (non-performing credit) or 8 (credit in litigation). Participating entities are encouraged to provide relevant information for credit risk assessment. In addition, renegotiated credits are requested to be reported since July, 2001.

-    [**Instrução no. 15/2002**](./aux_files/legislation/Instrucao_15-2002.pdf) – made procedural changes to access and occasional communication requested by the Banco de Portugal (no analysis impact).

-    [**Decree-Law no. 53/2004**](./aux_files/legislation/Lei_53-2004.pdf), March 18 – integrated the information on court decisions regarding insolvency proceedings of collective or individual people, provided by the Ministry of Justice, following the approval of the CIRE - Insolvency Code.

-    [**Instrução no. 7/2006**](./aux_files/legislation/Instrucao_7-2006_full.pdf) – created new types of credit for the variable type (codes 11-14) which include guarantees, sureties, and credit communicated by foreign central banks.

-    [**Instrução no. 21/2008**](./aux_files/legislation/Instrucao_21-2008_full.pdf) – changed the CCR to its current format (as in *Caderno* da CCR) and defined the scope, reporting deadline, and stress the important of reporting the types of information. Some codes were significantly changed.

-    [**Instrução no. 7/2009**](./aux_files/legislation/Instrucao_7-2009.pdf) – included credit reports from the State to protect unemployed individuals’ real estate ownership and created a special classification for these credits. This revised version contains more loan-level variables. Another important consequence of the revision was the incorporation of loans to Portuguese firms granted by foreign branches of Portuguese banks.

-    [**Instrução no. 18/2010**](./aux_files/legislation/Instrucao_18-2010.pdf) – imposed mandatory reporting of credit less than 90 days overdue (*crédito sem recurso*) if used in guarantee pools in Eurosystem operations; excluded shareholder’s advances (*suprimentos*) from financial institutions; imposed mandatory reporting of securitized debt issued for a certain debtor (even if the financial institution does not have ownership) and exclusion of securitized debt in the exposure sheet of the institution.

-    [**Instrução no. 17/2013**](./aux_files/legislation/Instrucao_17-2013.pdf) – separated overdue and written-off credit in litigation – codes 6 and 7; added new maturity categories and new collateral classifications

- [**Memorandum of Understanding on the exchange of information among national central credit registers**](./aux_files/legislation/Memorandum.pdf) - included credit exposures obtained from financial institutions located in the other EU
    countries (greater than or equal to 25000 euros). In 2003, the Banco de Portugal signed the "Memorandum of Understanding on the exchange of information among national central credit registers for the purpose of passing it on to the reporting Institutions"- MoU for the purpose of exchanging information between Central Credit Registers managed by National central banks of other member states of the European Union. Following the availability of this agreement, since 2005, credit exposures of collective residents in Portugal obtained from financial institutions located in the subscribed countries are included. Currently, in addition to Portugal, the countries subscribed include Germany, Austria, Belgium, Spain, France, Italy, Czech Republic and Romania. As the disclosure *timing* of other countries' CCRs in general does not coincide with the dissemination of information by the Portuguese CCR, it is normal to have a non-lower than one-month reporting lag between the reference date of the internal credit information and the reference date of the external credit included in the same regular dissemination file.


# Citation of this dataset
Banco de Portugal Microdata Research Laboratory (BPLIM) (2019): Central Credit Responsibility Database - Firm Level Data. Extraction: June 2019. Version: V2. BANCO DE PORTUGAL. Dataset. https://doi.org/10.17900/CRC.FRM.Jun2019.V2

Banco de Portugal Microdata Research Laboratory (BPLIM) (2019): Central Credit Responsibility Database - Bank-Firm Level Data. Extraction: June 2019. Version: V2. BANCO DE PORTUGAL. Dataset. https://doi.org/10.17900/CRC.FRMBNK.Jun2019.V2

Banco de Portugal Microdata Research Laboratory (BPLIM) (2019): Central Credit Responsibility Database - Exposure Level Data. Extraction: June 2019. Version: V1. BANCO DE PORTUGAL. Dataset. https://doi.org/10.17900/CRC.EXP.Jun2019.V1



# Auxiliary files

- For the metadata and summary statistics of firm and firm-bank data, please check the following auxiliary files: ^[The summary statistics are available in BPLIM's servers.]

| File | Description of Variables | Summary Statistics |
|:-------|:----:|:----:|
| FRM_COBR | [meta_FRM](./aux_files/metadata/META_CRC_A_MFRM_JUN19_COBR_V02.xlsx) | [stat_FRM](./aux_files/metadata/METATSS_CRC_A_MFRM_JUN19_COBR_V02.xlsx) |
| FRMBNK_CO | [meta_FRMBNK](./aux_files/metadata/META_CRC_A_MFRMBNK_JUN19_CO_V02.xlsx) | [stat_FRMBNK](./aux_files/metadata/METATSS_CRC_A_MFRMBNK_JUN19_CO_V02.xlsx) |


- For the metadata of exposure level data, please contact bplim@bportugal.pt.


# Useful Links

[CCR home page](https://www.bportugal.pt/area-cidadao/formulario/227)

[Statistical Bulletin](https://www.bportugal.pt/en/publicacao/statistical-bulletin)


# Useful Ado Files

We provide a handful of ado files written by BPLIM staff for researchers to implement certain calculations and variable arrangements.

<br>   
<br>   

## Harmonization of variables over time

**To use an ado compatible with the V02 criteria, please use the version 02 of the ado file**


`Description`

The CCR has undergone some major revisions. `harmonize ` is a Stata user-written command to help harmonize variables and make them compatible over time.

`Syntax`

```
harmonize `variable`

```

where `variable` denotes the variable to be harmonized. The ado processes one variable at a time; valid options are `tipogarantia`, `prazooriginal`, `prazoresidual`, `nivelresponsabilidade`, and `situacaocredito`. The harmonized output is stored in a new variable named "_variable_h"

<br>   
<br>   

## Aggregation

`Description`

`aggregate ` is a Stata user-written command to help compute aggregates of credit and bank relationship at different frequencies (yearly and quarterly) using various methods (period-end or period average). By default, the ado should only be applied to the original CCR datasets prepared by BPLIM.


`Syntax`

```
aggregate panelvar timevar, [options]

```

where `panelvar` is a unit identifier for the panel and `timevar` identifies the time variable.


`General Options`

*YEAR*: aggregation by year.

*QUARTER*: aggregation by quarter.

*AVG*: period average.

*END*: period end.

*NOCHECK*: ignore the difference between the current dataset and the original dataset prepared by BPLIM.

<br>   
<br>   

## Construction of firm default profile

`Description`

`default ` is a Stata user-written command to help calculate default events using information from the CCR datasets.


`Syntax`

```
default panelvar timevar overduevar benchmarkvar, [options]

```
where `panelvar` is a unit identifier for the panel, `timevar` identifies the time variable, `overduevar` identifies the variable of total overdue credit and `benchmarkvar` identifies the benchmark variable with which one can calculate the overdue intensity.


`General Options`

*THRESHOLD*: a pre-determined threshold of overdue credit ratio, 0.025 by default.

*RUNS*: a sequence/run of consecutive threshold hits for the same individual, 3 by default.

*IGNOREGAP*: allow gaps in the data when counting runs.


`Generated Variables`

Firm default variables are constructed based on the default definition of Antunes, Gonçalves and Prego (2016). By default, we flag out firm-month observations when more than 2.5% percent of total credit is reported overdue and define default event if a firm is flagged up for at least three consecutive months. For example, if a firm has overdue credit that amounts to more than 2.5% of its total credit in January and February, 2015 but later paid off the overdue credit in March, 2015, the firm will not be considered as in default in January and February, 2015. Researchers can also choose to apply an alternative threshold for the overdue credit ratio or/and an alternative duration of overdue status.

The variables generated include:

-    Overdue credit flag (*\_flag*). This is an indicator for the existence of overdue credit. It takes the follow values:

|:-------- |
|  0 - no credit is past due at the time |
|  1 - overdue credit is present but below the threshold |
|  2 - overdue credit is above the threshold |


- Default event (*\_default*). The default event occurs when a firm has credit overdue above the threshold for a run of defined consecutive months (three months by default).

- First default event (*\_fdefault*).The first default event occurs (flagged out with the value of 1) when a firm has credit overdue above the threshold for a run of defined consecutive months for the first time.

<br>   
<br>   

## Construction of firm-bank relationship spells

`Description`

`relationspell ` is a Stata user-written command to help construct bank-firm relationship variables which reflect the start,
discontinuity, and continuity of relationship between a firm and a bank.


`Syntax`

```
relationspell panelvar1 panelvar2 timevar, [options]

```

where `panelvar1` and `panelvar2` are identifiers for a firm and its bank, `timevar` identifies the time variable,



`General Options`

*STARTYR*:  start year.

*FINYEAR*:  end year.

*FREQUENCY*:  data frequency with the options of daily, monthly and annual (1, 2, and 3, respectively). The default option is monthly.

*GAPS*:  max gaps allowed in a relationship, 0 by default.


`Generated Variables`

The variables generated include:

-   Relationship ID (\_*relation*)

Relationship identification number.

-   Validity of a relationship (\_*relation\_valid*)

The status of a relationship spell. 0 denotes that the relationship is
discontinued for the given period and 1 denotes that the relationship is
active.

-   Relation spell (\_*spell*)

Relationship spell is an ordered variable for the relationship sequence
between a firm and a bank.

-   Start of a relationship spell (\_*mindate\_spell*)

The start of a relationship spell

-   End of a relationship spell (\_*maxdate\_spell*)

The end of a relationship spell

-   Length of a relationship spell (\*len\_spell*)

The length of a relationship spell

-   Start of relationship (\_*mindate*)

The start of a bank-firm relationship

-   End of relationship (\_*maxdate*)

The end of a bank-firm relationship

-   Length of relationship (\_*len\_all*)

The length of a bank-firm relationship

-   Length of active relationship (\_*len\_act*)

The length of active relationship

-   Length of inactive relationship (\_*len\_inact*)

The length of inactive relationship


# Frequently Asked Questions
The most frequently asked questions on the CCR report by participating entities can be found [here](https://www.bportugal.pt/perguntas-frequentes/276). If you have a question that is not covered in this manual, please send an email to bplim@bportugal.pt.
   

# References

Banco de Portugal (1987). Central de Responsabilidades de Crédito. Cadernos do Banco de Portugal. Lisboa.

Banco de Portugal (1993). Central de Responsabilidades de Crédito. Cadernos do Banco de Portugal. Lisboa.

Banco de Portugal (2003). Central de Responsabilidades de Crédito. Cadernos do Banco de Portugal. Lisboa.

Banco de Portugal (2010). Central de Responsabilidades de Crédito. Cadernos do Banco de Portugal. Lisboa.

Banco de Portugal (2011). Central de Responsabilidades de Crédito. Cadernos do Banco de Portugal. Lisboa.

Banco de Portugal (2014). Central de Responsabilidades de Crédito. [**Manual de Procedimentos Instrução no. 21/2008**](./iles/legislation/ManualdeprocedimentosdaCRC.pdf). Lisboa.

Banco de Portugal (2015). Central de Responsabilidades de Crédito. Cadernos do Banco de Portugal. Lisboa.

João Cadete de Matos (2015). The Portuguese Central Credit Register: a powerful multipurpose tool, relevant for many central bank functions. IFC workshop on “Combining micro and macro statistical data for financial stability analysis”. Bank for International Settlements.

Antunes, António, Homero Gonçalves, and Pedro Prego (2016). Firm Default Probabilities Revisited. Banco de Portugal Economic Studies, 2, 21-45.


# Appendix

## Country code list {#sec-country}

|**Country Code** |  **Country Name**  |
|:--------|:---------------|
ABW    |    Aruba    |
AFG    |    Afghanistan    |
AGO    |    Angola    |
AIA    |    Anguilla    |
ALA    |    Aland Islands    |
ALB    |    Albania    |
AND    |    Andorra    |
ANT    |    Netherlands Antilles    |
ARE    |    United Arab Emirates    |
ARG    |    Argentina    |
ARM    |    Armenia    |
ASM    |    American Samoa    |
ATA    |    Antarctica    |
ATF    |    South territories of France    |
ATG    |    Antigua and Barbuda    |
AUS    |    Australia    |
AUT    |    Austria    |
AZE    |    Azerbaijan    |
BDI    |    Burundi    |
BEL    |    Belgium    |
BEN    |    Benin    |
BFA    |    Burkina Faso    |
BGD    |    Bangladesh    |
BGR    |    Bulgaria    |
BHR    |    Bahrain    |
BHS    |    Bahamas    |
BIH    |    Bosnia Herzegovina    |
BLM    |    St. Bartholomew    |
BLR    |    Belarus    |
BLZ    |    Belize    |
BMU    |    Bermuda    |
BOL    |    Bolivia    |
BRA    |    Brazil    |
BRB    |    Barbados    |
BRN    |    Brunei    |
BTN    |    Bhutan    |
BVT    |    Bouvet Island (Norway Territory)    |
BWA    |    Botswana    |
CAF    |    Central African Republic    |
CAN    |    Canada    |
CCK    |    Cocos    |
CHE    |    Switzerland    |
CHL    |    Chile    |
CHN    |    China    |
CIV    |    Costa do Marfim    |
CMR    |    Cameroon    |
COD    |    Democratic Republic of Congo (former Zaire)    |
COG    |    Congo    |
COK    |    Cook Islands    |
COL    |    Colombia    |
COM    |    Comoros    |
CPV    |    Cape Verde    |
CRI    |    Costa Rica    |
CUB    |    Cuba    |
CUW    |    Curacao    |
CXR    |    Christmas island    |
CYM    |    Cayman Islands    |
CYP    |    Cyprus    |
CZE    |    Czech republic    |
DEU    |    Germany    |
DJI    |    Djibouti    |
DMA    |    dominica    |
DNK    |    Denmark    |
DOM    |    Dominican Republic    |
DZA    |    Algeria    |
ECU    |    Ecuador    |
EGY    |    Egypt    |
ERI    |    Eritrea    |
ESH    |    Western Sahara (former Spanish Sahara)    |
ESP    |    Spain    |
EST    |    Estonia    |
ETH    |    Ethiopia    |
FIN    |    Finland    |
FJI    |    Fiji    |
FLK    |    Falkland Islands (Malvinas)    |
FRA    |    France    |
FRO    |    Faroes Islands    |
FSM    |    Micronesia    |
GAB    |    Gabon    |
GBR    |    Great Britain (United Kingdom, UK)    |
GEO    |    Georgia    |
GGY    |    Guernsey    |
GHA    |    Ghana    |
GIB    |    Gibraltar    |
GIN    |    Guinea    |
GLP    |    Guadeloupe    |
GMB    |    Gambia    |
GNB    |    Guinea Bissau    |
GNQ    |    Equatorial Guinea    |
GRC    |    Greece    |
GRD    |    Grenade    |
GRL    |    Greenland    |
GTM    |    Guatemala    |
GUF    |    French Guiana    |
GUM    |    Guam (US Territory)    |
GUY    |    Guiana    |
HKG    |    Hong Kong    |
HMD    |    Heard and McDonald Islands (territory of Australia)    |
HND    |    Honduras    |
HRV    |    Croatia (Hrvatska)    |
HTI    |    Haiti    |
HUN    |    Hungary    |
IDN    |    Indonesia    |
IMN    |    Isle of Man    |
IND    |    India    |
IOT    |    Territory British Indian Ocean    |
IRL    |    Ireland    |
IRN    |    Will    |
IRQ    |    Iraq    |
ISL    |    Iceland    |
ISR    |    Israel    |
ITA    |    Italy    |
JAM    |    Jamaica    |
JEY    |    jersey    |
JOR    |    Jordan    |
JPN    |    Japan    |
KAZ    |    Kazakhstan    |
KEN    |    Kenya    |
KGZ    |    Kyrgyzstan    |
KHM    |    Cambodia    |
KIR    |    Kiribati    |
KNA    |    Saint Kitts and Nevis    |
KOR    |    South Korea    |
KWT    |    Kuwait    |
LAO    |    Laos    |
LBN    |    Lebanon    |
LBR    |    Liberia    |
LBY    |    Libya    |
LCA    |    Saint Lucia    |
LIE    |    Liechtenstein    |
LKA    |    Sri Lanka    |
LSO    |    Lesotho    |
LTU    |    Lithuania    |
LUX    |    Luxembourg    |
LVA    |    Latvia    |
MAC    |    Macao    |
MAF    |    St. Martin    |
MAR    |    Morocco    |
MCO    |    Monaco    |
MDA    |    Moldova    |
MDG    |    Madagascar    |
MDV    |    Maldives    |
MEX    |    Mexico    |
MHL    |    Marshall Islands    |
MKD    |    Macedonia (Republic Yugoslav)    |
MLI    |    Mali    |
MLT    |    Malta    |
MMR    |    Myanmar (former Burma)    |
MNE    |    Montenegro    |
MNG    |    Mongolia    |
MNP    |    Northern Mariana Islands    |
MOZ    |    Mozambique    |
MRT    |    Mauritania    |
MSR    |    montserrat    |
MTQ    |    Martinique    |
MUS    |    Mauritius    |
MWI    |    Malawi    |
MYS    |    Malaysia    |
MYT    |    Mayotte    |
NAM    |    Namibia    |
NCL    |    New Caledonia    |
NER    |    Niger    |
NFK    |    Norfolk Islands    |
NGA    |    Nigeria    |
NIC    |    Nicaragua    |
NIU    |    Niue    |
NLD    |    Netherlands    |
NOR    |    Norway    |
NPL    |    Nepal    |
NRU    |    Nauru    |
NZL    |    New Zealand    |
OMN    |    Oman    |
PAK    |    Pakistan    |
PAN    |    Panama    |
PCN    |    Pitcairn island    |
PER    |    Peru    |
PHL    |    Philippines    |
PLW    |    Palau    |
PNG    |    Papua New Guinea    |
POL    |    Poland    |
PRI    |    Puerto Rico    |
PRK    |    North Korea    |
PRT    |    Portugal    |
PRY    |    Paraguay    |
PSE    |    Occupied Palestinian Territories    |
PYF    |    French Polynesian    |
QAT    |    Qatar    |
REU    |    Reunion island    |
ROU    |    Romania    |
RUS    |    Russian Federation    |
RWA    |    Rwanda    |
SAU    |    Saudi Arabia    |
SDN    |    Sudan    |
SEN    |    Senegal    |
SGP    |    Singapore    |
SGS    |    South Georgia and the South Sandwich Islands    |
SHN    |    Saint Helen    |
SJM    |    Svalbard and Jan Mayen Islands    |
SLB    |    Solomon Islands    |
SLE    |    Sierra Leone    |
SLV    |    El Salvador    |
SMR    |    San Marino    |
SOM    |    Somalia    |
SPM    |    St. Pierre and Miquelon    |
SRB    |    Serbia    |
STP    |    Sao Tome and Principe    |
SUR    |    Suriname    |
SVK    |    Slovakia    |
SVN    |    Slovenia    |
SWE    |    Sweden    |
SWZ    |    Swaziland    |
SYC    |    Seychelles    |
SYR    |    Syria    |
TCA    |    Turks and Caicos Islands    |
TCD    |    Chad    |
TGO    |    Togo    |
THA    |    Thailand    |
TJK    |    Tajikistan    |
TKL    |    Tokelau Islands    |
TKM    |    Turkmenistan    |
TLS    |    East Timor (former East Timor)    |
TON    |    Tonga    |
TTO    |    Trinidad and Tobago    |
TUN    |    Tunisia    |
TUR    |    Turkey    |
TUV    |    Tuvalu    |
TWN    |    Taiwan    |
TZA    |    Tanzania    |
UGA    |    Uganda    |
UKR    |    Ukraine    |
UMI    |    US Outlying Islands    |
URY    |    Uruguay    |
USA    |    U.S    |
UZB    |    Uzbekistan    |
VAT    |    Vatican    |
VCT    |    Saint Vincent and the Grenadines    |
VEN    |    Venezuela    |
VGB    |    Virgin Islands (England)    |
VIR    |    Virgin Islands (United States)    |
VNM    |    Vietnam    |
VUT    |    Vanuatu    |
WLF    |    Wallis and Futuna Islands    |
WSM    |    Western Samoa    |
YEM    |    Yemen    |
ZAF    |    South Africa    |
ZMB    |    Zambia    |
ZWE    |    Zimbabwe    |


## Currency code list {#sec-currency}

|**Currency Code** |  **Currency Name**  |
|:--------|:---------------|
AED    |    UAE Dirham    |
ALL    |    Lek    |
AMD    |    Armenian Dram    |
ANG    |    Netherlands Antillean Guilder    |
AOA    |    Kwanza    |
ARS    |    Argentine Peso    |
AUD    |    Australian Dollar    |
AWG    |    Aruban Florin    |
AZN    |    Azerbaijan Manat    |
BAM    |    Convertible Mark    |
BBD    |    Barbados Dollar    |
BDT    |    Taka    |
BGN    |    Bulgarian Lev    |
BHD    |    Bahraini Dinar    |
BIF    |    Burundi Franc    |
BMD    |    Bermudian Dollar    |
BND    |    Brunei Dollar    |
BOB    |    Boliviano    |
BOV    |    Mvdol    |
BRL    |    Brazilian Real    |
BSD    |    Bahamian Dollar    |
BTN    |    Ngultrum    |
BWP    |    Pula    |
BYN    |    Belarusian Ruble    |
BZD    |    Belize Dollar    |
CAD    |    Canadian Dollar    |
CDF    |    Congolese Franc    |
CHE    |    WIR Euro    |
CHF    |    Swiss Franc    |
CHW    |    WIR Franc    |
CLF    |    Unidad de Fomento    |
CLP    |    Chilean Peso    |
CNY    |    Yuan Renminbi    |
COP    |    Colombian Peso    |
COU    |    Unidad de Valor Real    |
CRC    |    Costa Rican Colon    |
CUC    |    Peso Convertible    |
CUP    |    Cuban Peso    |
CVE    |    Cabo Verde Escudo    |
CZK    |    Czech Koruna    |
DJF    |    Djibouti Franc    |
DKK    |    Danish Krone    |
DOP    |    Dominican Peso    |
DZD    |    Algerian Dinar    |
EGP    |    Egyptian Pound    |
ERN    |    Nakfa    |
ETB    |    Ethiopian Birr    |
EUR    |    Euro    |
FJD    |    Fiji Dollar    |
FKP    |    Falkland Islands Pound    |
GBP    |    Pound Sterling    |
GEL    |    Lari    |
GHS    |    Ghana Cedi    |
GIP    |    Gibraltar Pound    |
GMD    |    Dalasi    |
GNF    |    Guinean Franc    |
GTQ    |    Quetzal    |
GYD    |    Guyana Dollar    |
HKD    |    Hong Kong Dollar    |
HNL    |    Lempira    |
HRK    |    Kuna    |
HTG    |    Gourde    |
HUF    |    Forint    |
IDR    |    Rupiah    |
ILS    |    New Israeli Sheqel    |
INR    |    Indian Rupee    |
IQD    |    Iraqi Dinar    |
IRR    |    Iranian Rial    |
ISK    |    Iceland Krona    |
JMD    |    Jamaican Dollar    |
JOD    |    Jordanian Dinar    |
JPY    |    Yen    |
KES    |    Kenyan Shilling    |
KGS    |    Som    |
KHR    |    Riel    |
KMF    |    Comorian Franc     |
KPW    |    North Korean Won    |
KRW    |    Won    |
KWD    |    Kuwaiti Dinar    |
KYD    |    Cayman Islands Dollar    |
KZT    |    Tenge    |
LAK    |    Lao Kip    |
LBP    |    Lebanese Pound    |
LKR    |    Sri Lanka Rupee    |
LRD    |    Liberian Dollar    |
LSL    |    Loti    |
LYD    |    Libyan Dinar    |
MAD    |    Moroccan Dirham    |
MDL    |    Moldovan Leu    |
MGA    |    Malagasy Ariary    |
MKD    |    Denar    |
MMK    |    Kyat    |
MNT    |    Tugrik    |
MOP    |    Pataca    |
MRU    |    Ouguiya    |
MUR    |    Mauritius Rupee    |
MVR    |    Rufiyaa    |
MWK    |    Malawi Kwacha    |
MXN    |    Mexican Peso    |
MXV    |    Mexican Unidad de Inversion (UDI)    |
MYR    |    Malaysian Ringgit    |
MZN    |    Mozambique Metical    |
NAD    |    Namibia Dollar    |
NGN    |    Naira    |
NIO    |    Cordoba Oro    |
NOK    |    Norwegian Krone    |
NPR    |    Nepalese Rupee    |
NZD    |    New Zealand Dollar    |
OMR    |    Rial Omani    |
PAB    |    Balboa    |
PEN    |    Sol    |
PGK    |    Kina    |
PHP    |    Philippine Peso    |
PKR    |    Pakistan Rupee    |
PLN    |    Zloty    |
PYG    |    Guarani    |
QAR    |    Qatari Rial    |
RON    |    Romanian Leu    |
RSD    |    Serbian Dinar    |
RUB    |    Russian Ruble    |
RWF    |    Rwanda Franc    |
SAR    |    Saudi Riyal    |
SBD    |    Solomon Islands Dollar    |
SCR    |    Seychelles Rupee    |
SDG    |    Sudanese Pound    |
SEK    |    Swedish Krona    |
SGD    |    Singapore Dollar    |
SHP    |    Saint Helena Pound    |
SLL    |    Leone    |
SOS    |    Somali Shilling    |
SRD    |    Surinam Dollar    |
SSP    |    South Sudanese Pound    |
STN    |    Dobra    |
SVC    |    El Salvador Colon    |
SYP    |    Syrian Pound    |
SZL    |    Lilangeni    |
THB    |    Baht    |
TJS    |    Somoni    |
TMT    |    Turkmenistan New Manat    |
TND    |    Tunisian Dinar    |
TOP    |    Pa’anga    |
TRY    |    Turkish Lira    |
TTD    |    Trinidad and Tobago Dollar    |
TWD    |    New Taiwan Dollar    |
TZS    |    Tanzanian Shilling    |
UAH    |    Hryvnia    |
UGX    |    Uganda Shilling    |
USD    |    US Dollar    |
UYU    |    Peso Uruguayo    |
UYW    |    Unidad Previsional    |
UZS    |    Uzbekistan Sum    |
VES    |    Bolívar Soberano    |
VND    |    Dong    |
VUV    |    Vatu    |
WST    |    Tala    |
XAF    |    CFA Franc BEAC    |
XCD    |    East Caribbean Dollar    |
XOF    |    CFA Franc BCEAO    |
XPF    |    CFP Franc    |
XSU    |    Sucre    |
XUA    |    ADB Unit of Account    |
YER    |    Yemeni Rial    |
ZAR    |    Rand    |
ZMW    |    Zambian Kwacha    |
ZWL    |    Zimbabwe Dollar    |

