# Requirements
Pleae install the following softare:
 * current R installation i.e. `3.4.0`. Install from https://cran.r-project.org/mirrors.html if on a mac installation via homebrew is possible by executing:
 ```
 brew tap homebrew/scienc
 brew install r
 ```
and these packages:
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
install.packages(c("data.table","dplyr","devtools","roxygen2","tidyverse","shiny","xml2","rvest","robustbase","mvoutlier","Rcpp", "sparklyr"))
```
