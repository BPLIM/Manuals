---
title: Output Control at BPLIM
author: "Banco de Portugal's Microdata Research Laboratory (BPLIM)"
date: 22 February 2024
format:
  pdf: 
    documentclass: scrartcl
    papersize: A4
    toc: false
    toc-title: Contents
    toc-depth: 3
    number-sections: true  
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


## Rules for Outputs Extraction at BPLIM

Only researchers identified in the project may request extraction of outputs. BPLIM will not check the “correctness” of the scripts used to produce the output files. The code is the sole responsibility of the researcher. However, researchers should abide by the following rules:

  > - Output files should never contain information that reveals individual records. This means that listings of individual records, tables with cells whose values were obtained by manipulation of three or less observations, statistical measures with standard errors of zero, minimum and maximum values, etc., are not allowed. BPLIM may refuse disclosure of output files if it perceives that the information in the logs may, directly or indirectly, reveal confidential information.
  
  > -	All outputs files must be generated by a script file which should be easy to identify. Requests for output extraction may be refused if BPLIM cannot associate the script file with the output.
   
  > -	All aggregate statistics must report the underlying value of N. This means, for example, that all regression outputs must report the number of observations and tables must report the number of observations per cell. Depending on the type of data BPLIM may impose stricter criteria at its discretion.
  
  > -	Output files of results must be plain text files (allowed formats are “txt”, “csv”, “log” and “tex”).
  
  > -	Comments in output files should not include references to data values.
  
  > -	The only graphical outputs allowed are “png” files. The information depicted in the graph must be of aggregated values. In some circumstances BPLIM may request that authors report a table with the N associated with each data point depicted in the graphic.  
  
  > -	Researchers should keep their output requests to a minimum and, as much as possible, these should be of final outputs.
  
  
  
Note that output verification depends on staff availability and may take longer in periods when the workload is higher. BPLIM staff will only answer requests for output extraction sent by email and will take as long as needed to ensure that all confidentiality requirements are safeguarded.


To request an extraction researchers should place the files in the “results” folder and send an email requesting extraction of the results to **bplim@bportugal.pt**. Please do not forget to include the project number in the subject.


