# Individual MFI Balance Sheet Items Portugal (iBSIPT) - Data Manual
BPLIM
2026-09-10

<script src="iBSIPT_manual_JUN26_files/libs/kePrint-0.0.1/kePrint.js"></script>
<link href="iBSIPT_manual_JUN26_files/libs/lightable-0.0.1/lightable.css" rel="stylesheet" />

- [General Information](#general-information)
- [Acronyms and Abbreviations](#acronyms-and-abbreviations)
- [Full Description](#full-description)
- [Geographical Coverage](#geographical-coverage)
- [Population](#population)
- [Methodology](#methodology)
- [Description of Files](#description-of-files)
- [Description of Variables](#description-of-variables)
  - [A. Identifiers](#a-identifiers)
  - [B. MFI Characteristics](#b-mfi-characteristics)
  - [C. Balance Sheet Items](#c-balance-sheet-items)
  - [D. Breakdown of Balance Sheet Items](#d-breakdown-of-balance-sheet-items)
  - [E. Amounts](#e-amounts)
- [Basic Descriptive Statistics](#basic-descriptive-statistics)
  - [A. Internal Researchers Dataset (INT)](#a-internal-researchers-dataset-int)
  - [B. External Researchers Dataset (EXT)](#b-external-researchers-dataset-ext)
- [FAQ](#faq)
  - [How can I obtain aggregate values of balance sheet items for each MFI and period?](#how-can-i-obtain-aggregate-values-of-balance-sheet-items-for-each-mfi-and-period)
  - [How can I compute total assets for each MFI and period?](#how-can-i-compute-total-assets-for-each-mfi-and-period)
  - [Can I obtain the balance sheet data at group level from the iBSIPT?](#can-i-obtain-the-balance-sheet-data-at-group-level-from-the-ibsipt)
  - [Can I obtain balance sheet information before December 2014?](#can-i-obtain-balance-sheet-information-before-december-2014)
  - [How is the iBSIPT dataset related to the discontinued BBS dataset?](#how-is-the-ibsipt-dataset-related-to-the-discontinued-bbs-dataset)
  - [How does the iBSIPT relate to the iBSI provided by the ECB for research purposes?](#how-does-the-ibsipt-relate-to-the-ibsi-provided-by-the-ecb-for-research-purposes)
- [References](#references)
- [Auxiliary Files](#auxiliary-files)
- [Useful Ado Files](#useful-ado-files)
  - [linkbank](#linkbank)
- [Citation of this Dataset](#citation-of-this-dataset)

------------------------------------------------------------------------

# General Information

> **Dataset Designation in English**: Individual Monetary Financial Institutions Balance Sheet Items - Portugal (iBSIPT)

> **Dataset Designation in Portuguese**: Balanço individual das Instituições Financeiras Monetárias - Portugal (iBSIPT)

> **Data Type**: longitudinal data

> **Unit of Analysis**: MFI / balance sheet item / original maturity / counterparty sector / counterparty residency (or counterparty region)

> **Frequency**: monthly

> **Start Date**: December, 2014

> **Most recent year**: December, 2024

> **Reference date**: end-of-month

> **Data Organization**: asset and liability information provided in a single file available in Stata format.

> **Version of the Data**: the data made available by BPLIM corresponds to a data freeze at a certain time of the year. Therefore, all files contain information as reported at the extraction date. The most recent update of the data occurred in June 2026.

> **Languages Available**: variables and value labels are available in Portuguese and in English.[^1]

> **Data Access**: This dataset includes two different subproducts with varying levels of detail and access mode. Internal researchers can access data covering all monetary financial institutions (MFIs), including detailed balance sheet information broken down by counterparty country. For external researchers, the balance sheet information is aggregated by counterparty region and excludes the reporting of MFIs of the type *Money Market Funds*. Furthermore, the data available to external researchers is modified to ensure confidentiality. For more details on the conditions for data access, please check the *[Guide for Researchers Using Banco de Portugal Microdata Research Laboratory (BPLIM) Data](https:///msites-dee-bplim-prd.azurewebsites.net/sites/default/files/guide_for_researchers_v2021_v2.pdf)*.

> **Digital Object Identifier**: 10.17900/iBSIPT.Jun2026.V1

# Acronyms and Abbreviations

- BPLIM: Laboratório de Investigação em Microdados do Banco de Portugal \| Banco de Portugal Microdata Research Laboratory

- BSI: Balance Sheet Items

- ECB: European Central Bank

- ESA: European System of Accounts

- ESCB: European System of Central Banks

- EU: European Union

- iBSI: individual Balance Sheet Items

- MFI: Monetary Financial Institution

- MMF: Money Market Funds

- NCB: National Central Banks

- non-MFI: Non-Monetary Financial Institution

# Full Description

The data are collected within the legal framework of the monthly balance sheet statistics of monetary financial institutions (MFIs) operating in Portugal, namely the [Instruction No. 14/2021](https:///www.bportugal.pt/instrucao/142021) and [Instruction No. 25/2014](https:///www.bportugal.pt/instrucao/252014) (no longer in force) of Banco de Portugal. The dataset includes granular individual MFI‑level information on the end-of-month outstanding amounts of balance‑sheet items, broken down by counterparty sector and residency, and by its original maturity, for selected items.

The Statistics Department of Banco de Portugal collects and prepares the data to fulfill its reporting obligations to the European Central Bank (ECB), contributing to the consolidated balance sheet and monetary aggregates of the euro area. Accordingly, on top of the Portuguese legal framework, the data collection is also ruled by the [Regulation (EU) No. 2021/379](https:///eur-lex.europa.eu/eli/reg/2021/379/oj) and [Regulation (EU) No. 1071/2013](https:///eur-lex.europa.eu/eli/reg/2013/1071/oj) (no longer in force) of the ECB, and the methodological details can be found in the [*Manual on MFI Balance Sheet Statistics*](https:///www.ecb.europa.eu/pub/pdf/other/ecb.manualmfibalancesheetstatistics202402%7E8e4fc2ccca.en.pdf) (ECB, 2024). By definition, the data are of statistical nature, which means that differences from accounting and supervisory-based reporting are to be expected.

BPLIM’s iBSIPT product builds on data collected by the Statistics Department, structured and formatted to facilitate research analysis while preserving the confidentiality and integrity of the data. Whenever possible, the data structure follows that of the ECB’s Balance Sheet Items (BSI – aggregate series) and individual BSI (microdata panel) datasets. However, some differences remain, and a direct comparison cannot always be established.[^2]

Balance sheet data are organized in accordance with the structure presented in <a href="#tbl-ibsipt-structure" class="quarto-xref">Table 1</a>, including breakdowns by original maturity, counterparty sector, and counterparty residency.

<div id="tbl-ibsipt-structure">

Table 1: iBSIPT balance sheet structure (on‑balance items)

| **Asset-side**[^3] | **Liability-side** |
|:---|:---|
| Cash | Overnight deposits |
| Loans | Deposits with agreed maturity |
| Debt securities held | Deposits redeemable at notice |
| MMF shares/units | Repurchase agreements |
| Equity and non-MMF investment fund shares/units | Debt securities issued |
| Non-financial assets (including fixed assets) | Capital and reserves |
| Remaining assets | Remaining liabilities |

</div>

Due to the confidential nature of the information, the dataset is structured into two subproducts: one for **internal researchers** (*INT*) and another for **external researchers** (*EXT*). These subproducts differ in terms of population coverage and the level of aggregation, with the *EXT* dataset containing a reduced set of variables, some of which with less granularity.

# Geographical Coverage

The dataset includes institutions resident in Portugal, including branches of foreign MFIs.

# Population

**For internal researchers:** The dataset covers MFIs (excluding central banks), as defined in Section 2.1 of Banco de Portugal’s Instruction No. 14/2021. If an institution ceases to be classified as an MFI during this period, its data reporting is discontinued. In the case of mergers or acquisitions, data may be reassigned between institutions to ensure continuity of the reporting series.

Figure <a href="#fig-mfi" class="quarto-xref">1</a> provides a simple visual overview of the distinction between [*MFI*](https:///data.ecb.europa.eu/methodology/what-monetary-financial-institution) and [*non-MFI*](https:///data.ecb.europa.eu/methodology/what-non-monetary-financial-institution) institutions, with those included in this dataset highlighted in grey.

<div id="fig-mfi">

<img src="./aux_files/figures/MFI%20and%20non_MFI%20BBS.png" style="width:85.0%" />

Figure 1: Monetary Financial Institutions included in iBSIPT

</div>

Deposit-taking corporations (excluding central banks) comprise all monetary financial institutions (MFIs) whose core activity is to accept deposits or close substitutes from the public and use these funds to grant credit or invest on their own account. It includes: credit institutions (banks) that take deposits and provide loans; other financial intermediaries that collect deposit-like funds from non-MFIs and use them for lending or investment; and certain electronic money institutions when they primarily engage in financial intermediation through issuing electronic money.

Money market funds (MMFs) are collective investment undertakings authorized under EU regulation that issue shares or units which act as close substitutes for bank deposits, due to their high liquidity and capital stability. Only those MMFs whose shares/units function as deposit-like instruments are included in the MFI sector.

**For external researchers:** The dataset is restricted to MFIs classified as deposit-taking corporations, excluding central banks, and thus does not include MMF.

# Methodology

The iBSIPT dataset contains microdata on monthly balance‑sheet statistics compiled by the Statistics Department of Banco de Portugal. The information refers exclusively to end‑of‑period outstanding amounts (stocks) of individual entities and is aggregated by items to facilitate balance sheet analysis. In exceptional cases where information at the individual entity level is not available, the iBSIPT dataset reports data at the group level.

To ensure consistency and comparability, the dataset is aligned, whenever possible, with the structure and nomenclature of the ECB’s *[BSI - Balance Sheet Items](https:///data.ecb.europa.eu/data/datasets/BSI/data-information)* dataset and the *[iBSI - Individual Balance Sheet Items](https:///www.ecb.europa.eu/stats/accessing-our-data/pdf/pilot_criteria_for_researchers.pdf)* microdata panel. In particular, series identifiers, dimensional breakdowns, and metadata closely follow the conventions defined in the *[BSI underlying Data Structure Definition (ECB_BSI1)](https:///data.ecb.europa.eu/data/datasets/BSI/structure)*. Any deviations from the ECB framework are highlighted in the [“Description of Variables” section](#description-of-variables) and documented in the [“Auxiliary Files”](#auxiliary-files) section.[^4]

Data are reported at a detailed level. Each balance‑sheet item, in <a href="#tbl-ibsipt-structure" class="quarto-xref">Table 1</a>, is disaggregated by maturity, counterparty sector, and counterparty residency (*counterparty country* for internal researchers and *counterparty region* for external researchers). Consequently, total amounts by item for a given month must be obtained by aggregating observations across these dimensions. All items are reported in millions of euros.

While most monetary financial institutions (MFIs) report data on a monthly basis, some entities are exempt from monthly reporting and provide information quarterly. For these institutions, the reported quarterly values are replicated across the three months of the reference quarter in order to maintain continuous time series. Quarterly reporters can be identified using the *flag_q* indicator.

To preserve confidentiality, all MFIs are anonymized through unique identifiers. In addition, for external researchers, balance‑sheet values are subject to statistical perturbation before being made available.[^5]

# Description of Files

The iBSIPT dataset is made available in a Stata-format file, using the following naming conventions.

***IBSIPT_meth_MBNK_2014yyyy_sub_Vxx.dta***

where *meth* indicates the method used to prepare the data (*“A”* for Anonymized, and *“P”* for Anonymized and Perturbed), *yyyy* refers to the last year available in the dataset, *sub* indicates the subproduct (*“INT”* for internal researchers, and *“EXT”* for external ones), and *Vxx* indicates the version.

Each observation corresponds to a combination of date, entity, balance sheet item, original maturity, counterparty residency (country or region) and counterparty sector.

# Description of Variables

Below we provide a general description of the variables included in the data. The metadata files are available in the [“Auxiliary Files” section](#auxiliary-files).

## A. Identifiers

`MFI anonymized identification number` (*bina*) : Unique identifier that enables tracking the MFI over time. *bina* is the anonymized identification number created by BPLIM.

`Time period` (*date*) : The reference month and year of the data, indicating the end of the reporting period.

`Quarterly reporter flag` (*flag_q*) : Flag equal to 1 when an institution reports quarterly, and 0 otherwise. For institutions that report quarterly, the values are repeated in the following two months, which means that even if flag_q=1, an institution will have observations as if it reported monthly.

For the period between 2021m12 and 2022m02, some institutions flagged as quarterly reporters show small changes in their monthly values due to a series break. Despite these differences, they should still be considered quarterly reporters, and *flag_q* equal to one is maintained.

## B. MFI Characteristics

`MFI type` (*mfi_type*) (**only available for internal researchers**)[^6]: MFI’s reference sector, mostly following the data structure defined by the ECB in *BS_REP_SECTOR*.

<div id="tbl-mfi">

Table 2: `MFI type` categories

| Code | Description | Correspondence in ECB data structure |
|:---|:---|:---|
| 1 | 1 - Money Market Funds | CL_BS_REP_SECTOR = F |
| 2 | 2 - Credit institutions legally incorporated in Portugal | CL_BS_REP_SECTOR = W |
| 3 | 3 - Branches of non-domestic and euro area-based credit institutions | CL_BS_REP_SECTOR = X |
| 4 | 4 - Branches of non-domestic and non-euro area based credit institutions | CL_BS_REP_SECTOR = Y + Z |

</div>

## C. Balance Sheet Items

`Balance sheet item code` (*item*): Code for the balance sheet item, following a data structure similar to the one defined by the ECB in *BS_ITEM*. Asset-side items begin with an *1* (*A* in ECB’s format), while liability-side items begin with a *2* (*L* in ECB’s format).[^7]

<div id="tbl-assets">

Table 3: `Balance sheet item code` categories: assets-side

| Code | Description | Correspondence in ECB data structure |
|:---|:---|:---|
| 110 | 110 - Cash | BS_ITEM = A10 |
| 122 | 122 - Loans, house purchase | BS_ITEM = A22 |
| 123 | 123 - Loans, other lending | All non-A22 and non-A25 loans are reported by ECB as A20 |
| 125 | 125 - Loans, consumption and other personal lending | BS_ITEM = A25 |
| 130 | 130 - Debt securities held | BS_ITEM = A30 |
| 142 | 142 - MMF shares/units | BS_ITEM = A42 |
| 150 | 150 - Equity and non-MMF investment fund shares/units | BS_ITEM = A50 |
| 160 | 160 - Non-financial assets (including fixed assets) | BS_ITEM = A60 |
| 170 | 170 - Remaining assets | BS_ITEM = A70 |
| 199 | 199 - Residual value that ensures accounting identity (computed) [^8] | n.a. |

</div>

<div id="tbl-liabilities">

Table 4: `Balance sheet item code` categories: liabilities-side

| Code | Description | Correspondence in ECB data structure |
|:---|:---|:---|
| 221 | 221 - Overnight deposits | BS_ITEM = L21 + partially BS_ITEM = L2C and L2D |
| 222 | 222 - Deposits with agreed maturity | BS_ITEM = L22 + partially BS_ITEM = L2C and L2D |
| 223 | 223 - Deposits redeemable at notice | BS_ITEM = L23 + partially BS_ITEM = L2C and L2D |
| 224 | 224 - Repurchase agreements | BS_ITEM = L24 + partially BS_ITEM = L2C and L2D |
| 240 | 240 - Debt securities issued | BS_ITEM = L40 |
| 260 | 260 - Capital and reserves | BS_ITEM = L60 |
| 270 | 270 - Remaining liabilities | BS_ITEM = L70 |

</div>

## D. Breakdown of Balance Sheet Items

`Original maturity` (*maturity_orig*): Code for the original maturity of the items reported, following the data structure defined by the ECB in *MATURITY_ORIG*. Availability and applicability vary depending on the balance sheet item (please see <a href="#tbl-mat_item" class="quarto-xref">Table 6</a>).

<div id="tbl-mat">

Table 5: `Original maturity` categories

| Code | Description                  | Correspondence in ECB data structure |
|:-----|:-----------------------------|:-------------------------------------|
| 1    | 1 - Up to 3 months           | MATURITY_ORIG = D                    |
| 2    | 2 - Over 3 months            | MATURITY_ORIG = E                    |
| 3    | 3 - Up to 1 year             | MATURITY_ORIG = F                    |
| 4    | 4 - Over 1 and up to 2 years | MATURITY_ORIG = G                    |
| 5    | 5 - Over 2 years             | MATURITY_ORIG = H                    |
| 6    | 6 - Over 5 years             | MATURITY_ORIG = J                    |
| 7    | 7 - Over 1 year              | MATURITY_ORIG = K                    |
| 8    | 8 - Over 2 and up to 5 years | MATURITY_ORIG = T                    |
| 99   | 99 - Not applicable          | MATURITY_ORIG = X                    |

</div>

<div id="tbl-mat_item">

Table 6: Availability of original maturity by balance sheet item code

<div class="cell-output-display">

| item |  1  |  2  |  3  |  4  |  5  |  6  |  7  |  8  | 99  |
|:----:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 110  |     |     |     |     |     |     |     |     |  x  |
| 122  |     |     |  x  |  x  |     |  x  |     |  x  |     |
| 123  |     |     |  x  |  x  |     |  x  |     |  x  |     |
| 125  |     |     |  x  |  x  |     |  x  |     |  x  |     |
| 130  |     |     |  x  |  x  |  x  |     |     |     |     |
| 142  |     |     |     |     |     |     |     |     |  x  |
| 150  |     |     |     |     |     |     |     |     |  x  |
| 160  |     |     |     |     |     |     |     |     |  x  |
| 170  |     |     |     |     |     |     |     |     |  x  |
| 199  |     |     |     |     |     |     |     |     |  x  |
| 221  |     |     |     |     |     |     |     |     |  x  |
| 222  |     |     |  x  |  x  |  x  |     |     |     |     |
| 223  |  x  |  x  |     |     |     |     |     |     |     |
| 224  |     |     |  x  |     |     |     |  x  |     |     |
| 240  |     |     |  x  |  x  |  x  |     |     |     |     |
| 260  |     |     |     |     |     |     |     |     |  x  |
| 270  |     |     |     |     |     |     |     |     |  x  |

</div>

</div>

`Counterparty country` (*count_country*) **(only available for internal researchers)**: Code for the country of the counterparty of the items reported, following the ISO Numeric-3. Classified as *999*, if *“not applicable”*.

`Counterparty region` (*count_region*): Code for the region of the counterparty of the items reported, following the data structure defined by the ECB in *AREA_EE*.

<div id="tbl-region">

Table 7: `Counterparty region` categories

| Code | Description                      | Correspondence in ECB data structure |
|:-----|:---------------------------------|:-------------------------------------|
| 1    | 1 - Domestic                     | AREA_EE = U6                         |
| 2    | 2 - Euro area, excluding PT [^9] | AREA_EE = U5                         |
| 3    | 3 - Rest of the world            | AREA_EE = U4                         |

</div>

`Counterparty sector` (*count_sector*) **(only available for internal researchers)**: Code for the sector of the counterparty of the items reported, following the data structure defined by the ECB in *BS_COUNT_SECTOR*. The classification is derived from the sector codes used in the European System of Accounts (ESA 2010) and corresponds to the sum of resident and non-resident counterparties. For example, the *“1210 Deposit-taking corporations except the central bank”* includes sector S.122 and S.2022. Availability and applicability vary depending on the balance sheet item (please see <a href="#tbl-sector_item" class="quarto-xref">Table 9</a>), and, in some cases, on the balance sheet item and the original_maturity (please see <a href="#tbl-sector_item_mat" class="quarto-xref">Table 10</a>).

<div id="tbl-sector">

Table 8: `Counterparty sector` categories

| Code | Description |
|:---|:---|
| 0 | 0 - Unspecified counterparty sector |
| 1100 | 1100 - Central Bank |
| 1210 | 1210 - Deposit-taking corporations, except the central bank |
| 1220 | 1220 - Money market funds |
| 2110 | 2110 - Central Government |
| 2121 | 2121 - State Government |
| 2122 | 2122- Local Authorities |
| 2123 | 2123 - Social security funds |
| 2210 | 2210 - Financial corporations except MFI’s and insurance corporations and pension funds |
| 2221 | 2221 - Insurance corporations |
| 2222 | 2222 - Pension funds |
| 2240 | 2240 - Non-financial corporations |
| 2251 | 2251 - Households |
| 2252 | 2252 - Non-Profit institutions serving Households |

</div>

<div id="tbl-sector_item">

Table 9: Availability of counterparty sector by balance sheet item code

<div class="cell-output-display">

| item |  0  | 1100 | 1210 | 1220 | 2110 | 2121 | 2122 | 2123 | 2210 | 2221 | 2222 | 2240 | 2251 | 2252 |
|:----:|:---:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
| 110  |     |  x   |      |      |      |      |      |      |      |      |      |      |      |      |
| 122  |     |      |      |      |      |      |      |      |      |      |      |      |  x   |      |
| 123  |     |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |      |      |
| 125  |     |      |      |      |      |      |      |      |      |      |      |      |  x   |  x   |
| 130  |     |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |      |      |
| 142  |     |      |      |  x   |      |      |      |      |      |      |      |      |      |      |
| 150  |     |  x   |  x   |      |  x   |      |  x   |  x   |  x   |  x   |  x   |  x   |      |  x   |
| 160  |  x  |      |      |      |      |      |      |      |      |      |      |      |      |      |
| 170  |  x  |      |  x   |  x   |  x   |  x   |  x   |      |  x   |  x   |  x   |  x   |  x   |  x   |
| 199  |  x  |      |      |      |      |      |      |      |      |      |      |      |      |      |
| 221  |     |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |
| 222  |     |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |
| 223  |     |      |  x   |      |  x   |      |  x   |      |  x   |  x   |      |  x   |  x   |  x   |
| 224  |     |      |  x   |      |  x   |      |      |      |  x   |      |      |      |      |      |
| 240  |  x  |      |      |      |      |      |      |      |      |      |      |      |      |      |
| 260  |  x  |      |  x   |      |  x   |  x   |  x   |      |  x   |  x   |  x   |  x   |  x   |  x   |
| 270  |  x  |  x   |  x   |  x   |  x   |  x   |  x   |      |  x   |  x   |  x   |  x   |  x   |  x   |

</div>

</div>

<div id="tbl-sector_item_mat">

Table 10: Differences in availability of original maturity by counterparty sector and balance sheet item code

<div class="cell-output-display">

| item | countsector | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 99 |
|:--:|:---|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| 123 | 1220 |  |  | x |  |  |  |  | x |  |
| 123 | 1100 |  |  | x |  |  | x |  |  |  |
| 123 | 2222 |  |  | x | x |  | x |  |  |  |
| 123 | 1210,2110,2121,2122<br>2123,2210,2221,2240 |  |  | x | x |  | x |  | x |  |
| 130 | 1220,2221,2222 |  |  |  |  | x |  |  |  |  |
| 130 | 2122,2123 |  |  | x |  | x |  |  |  |  |
| 130 | 1100,1210,2110,2121<br>2210,2240 |  |  | x | x | x |  |  |  |  |
| 222 | 1220 |  |  | x | x |  |  |  |  |  |
| 222 | 1100,1210,2110,2121<br>2122,2123,2210,2221<br>2222,2240,2251,2252 |  |  | x | x | x |  |  |  |  |
| 223 | 2110,2122,2210,2221<br>2240,2252 | x |  |  |  |  |  |  |  |  |
| 223 | 1210,2251 | x | x |  |  |  |  |  |  |  |
| 224 | 2110 |  |  | x |  |  |  |  |  |  |
| 224 | 1210,2210 |  |  | x |  |  |  | x |  |  |

</div>

</div>

`Counterparty sector (aggregated)` (*count_sector2*) **(only available for external researchers)**: Similar to `Counterparty sector`, but with less granular classification. Availability and applicability vary depending on the balance sheet item (please see <a href="#tbl-sector2_item" class="quarto-xref">Table 12</a>), and, in some cases, on the balance sheet item and the original_maturity (please see <a href="#tbl-sector2_item_mat" class="quarto-xref">Table 13</a>).

<div id="tbl-sector2">

Table 11: `Counterparty sector (aggregated)` categories

| Code | Description |
|:---|:---|
| 0 | 0 - Unspecified counterparty sector |
| 1100 | 1100 - Central Bank |
| 1210 | 1210 - Deposit-taking corporations except the central bank |
| 1220 | 1220 - Money market funds |
| 2100 | 2100 - General Government |
| 2210 | 2210 - Financial corporations except MFI’s and insurance corporations and pension funds |
| 2220 | 2220 - Insurance corporations and pension funds |
| 2240 | 2240 - Non-Financial corporations |
| 2250 | 2250 - Households and non-profit institutions serving households |

</div>

<div id="tbl-sector2_item">

Table 12: Availability of counterparty sector (aggregated) by balance sheet item code

<div class="cell-output-display">

| item |  0  | 1100 | 1210 | 1220 | 2100 | 2210 | 2220 | 2240 | 2250 |
|:----:|:---:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
| 110  |     |  x   |      |      |      |      |      |      |      |
| 122  |     |      |      |      |      |      |      |      |  x   |
| 123  |     |  x   |  x   |  x   |  x   |  x   |  x   |  x   |      |
| 125  |     |      |      |      |      |      |      |      |  x   |
| 130  |     |  x   |  x   |  x   |  x   |  x   |  x   |  x   |      |
| 142  |     |      |      |  x   |      |      |      |      |      |
| 150  |     |  x   |  x   |      |  x   |  x   |  x   |  x   |  x   |
| 160  |  x  |      |      |      |      |      |      |      |      |
| 170  |  x  |      |  x   |  x   |  x   |  x   |  x   |  x   |  x   |
| 199  |  x  |      |      |      |      |      |      |      |      |
| 221  |     |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |
| 222  |     |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |
| 223  |     |      |  x   |      |  x   |  x   |  x   |  x   |  x   |
| 224  |     |      |  x   |      |  x   |  x   |      |      |      |
| 240  |  x  |      |      |      |      |      |      |      |      |
| 260  |  x  |      |  x   |      |  x   |  x   |  x   |  x   |  x   |
| 270  |  x  |  x   |  x   |  x   |  x   |  x   |  x   |  x   |  x   |

</div>

</div>

<div id="tbl-sector2_item_mat">

Table 13: Differences in availability of original maturity by counterparty sector (aggregated) and balance sheet item code

<div class="cell-output-display">

| item | countsector2                          |  1  |  2  |  3  |  4  |  5  |  6  |  7  |  8  | 99  |
|:----:|:--------------------------------------|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 123  | 1220                                  |     |     |  x  |     |     |     |     |  x  |     |
| 123  | 1100                                  |     |     |  x  |     |     |  x  |     |     |     |
| 123  | 1210,2100,2210,2220<br>2240           |     |     |  x  |  x  |     |  x  |     |  x  |     |
| 130  | 1220,2220                             |     |     |     |     |  x  |     |     |     |     |
| 130  | 1100,1210,2100,2210<br>2240           |     |     |  x  |  x  |  x  |     |     |     |     |
| 222  | 1220                                  |     |     |  x  |  x  |     |     |     |     |     |
| 222  | 1100,1210,2100,2210<br>2220,2240,2250 |     |     |  x  |  x  |  x  |     |     |     |     |
| 223  | 2100,2210,2220,2240                   |  x  |     |     |     |     |     |     |     |     |
| 223  | 1210,2250                             |  x  |  x  |     |     |     |     |     |     |     |
| 224  | 2100                                  |     |     |  x  |     |     |     |     |     |     |
| 224  | 1210,2210                             |     |     |  x  |     |     |     |  x  |     |     |

</div>

</div>

## E. Amounts

`Reported amounts` (*value*): outstanding amounts at the end-of-period (stocks) for each balance sheet item breakdown. Amounts reported in millions of euros with two-digit precision.

# Basic Descriptive Statistics

To support data analysis, we provide metadata files in Excel format that can be used to understand the structure of the dataset. These files, available in the [“Auxiliary Files”](#auxiliary-files) section, are generated using BPLIM’s Stata package *metaxl*, which provides a set of tools for managing and documenting metadata and is available through the SSC repository.

In addition, we provide an Excel file containing descriptive statistics for the entire dataset, also generated using the *metaxl* package and available on the BPLIM’s servers.

## A. Internal Researchers Dataset (INT)

For the **INT** subproduct (available exclusively to internal researchers), the number of reporting entities varies over time, as reported in <a href="#tbl-obsy_int" class="quarto-xref">Table 14</a>. The corresponding total assets closely mirrors the aggregate series *“Total assets of MFIs excluding NCB, Stocks, Portugal, Monthly” (BSI.M.PT.N.A.T00.A.1.Z5.0000.Z01.E)* published by the ECB, as shown in <a href="#fig-assets" class="quarto-xref">Figure 2</a>.

<div id="tbl-obsy_int">

Table 14: Number of entities in the end of each year

<div class="cell-output-display">

|   date   | bina |
|:--------:|:----:|
| Dec 2014 |  74  |
| Dec 2015 |  69  |
| Dec 2016 |  67  |
| Dec 2017 |  66  |
| Dec 2018 |  63  |
| Dec 2019 |  69  |
| Dec 2020 |  71  |
| Dec 2021 |  72  |
| Dec 2022 |  70  |
| Dec 2023 |  71  |
| Dec 2024 |  72  |

</div>

</div>

<div id="fig-assets">

<img src="./aux_files/stata/total_assets2.png" style="width:90.0%" />

Figure 2: Total assets of MFIs excluding NCB, Stocks, Portugal, Monthly

</div>

## B. External Researchers Dataset (EXT)

For the **EXT** subproduct (available to external researchers), the number of reporting entities varies over time, as reported in <a href="#tbl-obsy_ext" class="quarto-xref">Table 15</a>. The dataset excludes money market funds from its reporting population. This exclusion has a negligible impact, accounting for less than 1% of total assets.

<div id="tbl-obsy_ext">

Table 15: Number of entities in the end of each year

<div class="cell-output-display">

|   date   | bina |
|:--------:|:----:|
| Dec 2014 |  67  |
| Dec 2015 |  62  |
| Dec 2016 |  61  |
| Dec 2017 |  61  |
| Dec 2018 |  60  |
| Dec 2019 |  67  |
| Dec 2020 |  68  |
| Dec 2021 |  69  |
| Dec 2022 |  67  |
| Dec 2023 |  68  |
| Dec 2024 |  69  |

</div>

</div>

# FAQ

## How can I obtain aggregate values of balance sheet items for each MFI and period?

The iBSIPT dataset is highly disaggregated: multiple records together form the total value of a balance‑sheet item. To compute aggregate values by MFI and reporting period, you need to sum the observations across all disaggregation dimensions. You can do this using the following command:

    collapse (sum) value, by(date bina item)

## How can I compute total assets for each MFI and period?

Balance‑sheet items corresponding to assets are identified by item codes between 100 and 200. To calculate total assets for each MFI and period, flag asset items and aggregate the data:

    collapse (sum) value if item<200, by(date bina)

## Can I obtain the balance sheet data at group level from the iBSIPT?

No. BPLIM does not currently provide information on banking group structures. Moreover, even if group composition were known, consolidated balance sheet figures could not be derived from iBSIPT, as the dataset does not allow the identification and elimination of intra-group positions and transactions. Therefore, a simple aggregation of reporting entities would not yield valid group-level consolidated values.

## Can I obtain balance sheet information before December 2014?

BPLIM currently does not provide microdata prior to December 2014 due to changes in the data collection methodology that introduced significant breaks in the time series.

## How is the iBSIPT dataset related to the discontinued BBS dataset?

Both datasets are derived from the same underlying data source; however, they differ in their structure, level of aggregation, and methodological treatment of certain items. The iBSIPT dataset is designed to ensure that observations can be aggregated directly across reporting entities without introducing double counting. This makes it particularly easy to compute aggregate values by accounting item, for example. In the *INT* file each observation is a unique combination of date , bina, item, original maturity, counterparty country, and counterparty sector. In the *EXT* file each observation is a unique combination of date, bina, item, original maturity, counterparty region, and counterparty sector (aggregated).

In contrast, the BBS dataset follows a different reporting framework and therefore is not fully comparable on a one-to-one basis, for example, in BBS exposures to counterparties in Spain may be reported both under the country=“ES” and under the aggregate geographical country=“UM-PT”. Beyond differences in aggregation, the datasets also diverge in several methodological aspects. One of the most important distinctions is the treatment of own securities and equity holdings. While the iBSIPT framework excludes these positions from the reported amounts, the BBS dataset includes them. As a result, reported values in the BBS may be systematically higher for institutions with significant holdings of their own debt securities or equity instruments, which should be taken into account when comparing figures across the two datasets.

## How does the iBSIPT relate to the iBSI provided by the ECB for research purposes?

Access to the iBSI microdata panel for the euro area was granted exclusively to researchers selected through a pilot project for research access to confidential statistical data managed by the ECB, and is not available outside that framework. More information about the pilot project can be found [here](https:///www.ecb.europa.eu/stats/accessing-our-data/microdata-pilot/html/index.en.html). While the data structures are generally similar, differences in aggregation methodologies, data treatment, and population coverage may apply. Detailed information can be found in the documentation provided in the [“Auxiliary Files”](#auxiliary-files) section.

# References

- ECB (2024), **Manual on MFI Balance Sheet Statistics**, European Central Bank, February 2024. [ENG version](https:///www.ecb.europa.eu/pub/pdf/other/ecb.manualmfibalancesheetstatistics202402%7E8e4fc2ccca.en.pdf)

Legislation applicable during the covered period:

- *[Instruction No. 14/2021 of the Banco de Portugal](https:///www.bportugal.pt/instrucao/142021)*

- *[Instruction No. 25/2014 of the Banco de Portugal](https:///www.bportugal.pt/instrucao/252014)* \[revoked\]

- *[Regulation (EU) No. 2021/379 of the European Central Bank](https:///eur-lex.europa.eu/eli/reg/2021/379/oj)*

- *[Regulation (EU) No. 2013/1071 of the European Central Bank](https:///eur-lex.europa.eu/eli/reg/2013/1071/oj)* \[revoked\]

# Auxiliary Files

- For the detailed correspondence between iBSIPT and iBSI, please check the document: [How iBSIPT compares to iBSIECB](./aux_files/How-iBSIPT-compares-to-iBSIECB.pdf)

- For the metadata, and summary statistics please check the following auxiliary files:

| File | Metadata | Summary Statistics |
|:---|:--:|:--:|
| INT | [meta_INT](./aux_files/metadata/META_IBSIPT_A_MBNK_20142024_JUN26_INT_V01.xlsx) | [stat_INT](./aux_files/descriptive_statistics/METATSS_IBSIPT_A_MBNK_20142024_JUN26_INT_V01.xlsx) |
| EXT | [meta_EXT](./aux_files/metadata/META_IBSIPT_P_MBNK_20142024_JUN26_EXT_V01.xlsx) | [stat_EXT](./aux_files/descriptive_statistics/METATSS_IBSIPT_A_MBNK_20142024_JUN26_EXT_V01.xlsx) |

# Useful Ado Files

We provide an ado file, developed by BPLIM staff, designed to assist researchers in integrating datasets containing financial corporation data defined at different levels of analysis.

## linkbank

This tool is essential for accurately linking individual entity registers from datasets derived from Central Credit Register data (such as CRC and HCRC) to other datasets, like SLB or iBSIPT (which represents banking groups or stand-alone institutions).

For the latest information and updates on the tool, please visit our GitHub page: [**linkbank**](https:///github.com/BPLIM/Tools/tree/master/ados/CRC_FRMBNK/linkbank)

# Citation of this Dataset

Banco de Portugal Microdata Research Laboratory (BPLIM) (2026): Individual Monetary Financial Institutions Balance Sheet Items - Portugal (iBSIPT). Extraction: June 2026. Version: V1. Banco de Portugal - BPLIM. Dataset. https:///doi.org/10.17900/iBSIPT.Jun2026.V1

To cite this dataset, you can use the *biblatex* package with the following BibTeX entry:

``` stata
@dataset{iBSIPT.Jun2026.V1,
  author    = {{Banco de Portugal Microdata Research Laboratory (BPLIM)}},
  title     = {{I}ndividual {M}onetary {F}inancial {I}nstitutions {B}alance {S}heet   
    {I}tems {P}ortugal (iBSIPT)}},
  publisher = {Banco de Portugal - BPLIM. Dataset},
  year      = {2026},
  version   = {V1},
  note      = {Extraction June 2026},
  doi       = {10.17900/iBSIPT.Jun2026.V1},
  url       = {https:///doi.org/10.17900/iBSIPT.Jun2026.V1}
}
```

[^1]: To see the labels in English type the following command line in Stata: ‘label language en’.

[^2]: Researchers wishing to compare the structure of the data with that of the ECB’s iBSI dataset are encouraged to carefully review the notes in the [“Description of variables” section](#description-of-variables) and consult *How iBSIPT compares to iBSIECB*, a document prepared by the BPLIM detailing the correspondence between iBSIPT and iBSI, available in the [“Auxiliary Files”](#auxiliary-files) section.

[^3]: On the asset side, there is an additional item calculated by BPLIM to ensure the accounting identity holds. For more details, please refer to the [“Description of variables” section](#description-of-variables).

[^4]: The BSI dataset is publicly available, whereas access to the iBSI dataset was granted for research purposes through a [pilot project for research access to confidential statistical data managed by the ECB](https:///www.ecb.europa.eu/stats/accessing-our-data/microdata-pilot/html/index.en.html).

[^5]: For more details on the conditions for data access, please check the *[Guide for Researchers Using Banco de Portugal Microdata Research Laboratory (BPLIM) Data](https:///msites-dee-bplim-prd.azurewebsites.net/sites/default/files/guide_for_researchers_v2021_v2.pdf)*.

[^6]: This variable is not available in the dataset for external researchers. Furthermore, the external dataset does not include institutions classified as mfi_type = 1 and covers only deposit-taking institutions classified as mfi_type = 2, 3, or 4.

[^7]: Some balance-sheet items do not have a direct correspondence to the ECB data structure. For example, the ECB classifies deposits that might qualify as M3 into a separate category - L2C and L2D. For more details, please consult *How iBSIPT compares to iBSIECB*, a document prepared by the BPLIM detailing the correspondence between iBSIPT and iBSI, available in the [“Auxiliary Files”](#auxiliary-files) section.

[^8]: The code *199* refers to a residual value computed by BPLIM to ensure that the accounting identity — assets equal liabilities plus equity — holds. This residual should be negligible, as it arises solely from rounding differences. If you are using Stata to verify the accounting identity, make sure to round the *value* variable to two decimal places. This is important because values are stored in binary format, which can cause small discrepancies—even when numbers appear correctly rounded on screen.

[^9]: Euro area changing composition (except PT), according to the end-of-month classification.
