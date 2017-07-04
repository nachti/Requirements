# Requirements
Please install the following packages:
 * data.table
 * dplyr
 * devtools
 * roxygen2
 * tidyverse
 * shiny
 * xml2 
 * rvest
 * robustbase
 * mvoutlier
 * Rcpp
   * including the compiler (Xcode from the MacAppStore on macOS or for Windows [Rtools](https://cran.r-project.org/bin/windows/Rtools)
   * if everything is set up, the follwing line should return 4:
```r
Rcpp::evalCpp("2+2")
```
This line installs all the packages:
```r
install.packages(c("data.table","dplyr","devtools","roxygen2","tidyverse","shiny","xml2","rvest","robustbase","mvoutlier","Rcpp"))
```
