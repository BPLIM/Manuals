<meta charset="utf-8"/>
# Central Balance Sheet Harmonized Panel Data
## Descriptive statistics
`extraction`: June 2019

## **Corporate Actions - Harmonized Panel**

```
    di _new _new "AMARC - 2006-2017"
    quietly use "S:/data/Products/CB/2019_06/CB_Panel/Output/Data/Firms/CBHP_A_YFRM_20062017_JUN19_AMARC_V01.dta", clear
    sum, separator(1000)

    di "Descriptive Statistics by Year"
    bysort ano: sum, separator(1000)
```






