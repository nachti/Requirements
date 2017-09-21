# Requirements
Pleae install the following softare:
 * current R installation i.e. `3.4.0`. Install from https://cran.r-project.org/mirrors.html if on a mac installation via homebrew is possible by executing:
 ```
 brew tap homebrew/science
 brew install r
 ```
 * RStudio https://www.rstudio.com on ma mac installlation via brew is possible by executing
 ```
 brew cask install rstudio
 ```
and these packages:
 * data.table
 * dplyr
 * dbplyr
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
 * replyr
 * sparklyr
 * rmarkdown
 * xtable
 * stargazer
 
 Additionally, some packages with data sets are required:
 
 
This line installs all the packages:
```r
install.packages(c("data.table","dplyr","dbplyr","devtools","roxygen2","tidyverse","shiny","xml2","rvest","robustbase","mvoutlier","Rcpp", "replyr", "rmarkdown", "xtable", "stargazer"))
devtools::install_github("rstudio/sparklyr",lib="")

# some data to analyze later on
install.packages(c("nycflights13", "Lahman"))
```

## Tools for R-Package development

Please follow the instructions here:
https://support.rstudio.com/hc/en-us/articles/200486498-Package-Development-Prerequisites

Windows users should install Rtools and a LaTeX distribution.

Links:
https://cran.r-project.org/bin/windows/Rtools/

https://cran.r-project.org/bin/windows/Rtools/Rtools.txt

http://thecoatlessprofessor.com/programming/rcpp/install-rtools-for-rcpp/

There are some issues with Windows 10:

https://stackoverflow.com/questions/45309492/unable-to-install-rtools-and-configure-the-path-correctly

https://github.com/hadley/devtools/issues/885

```r
Sys.which("gcc.exe")
```
should return a path an not an empty string if the (gcc) installation is ok.

## Preparations for the talks / labs
### R for HPC and big data
Java8 i.e. JRE8 or JDK8 should be installed.

On the first run you also must download spark. First check for available versions 
```spark_available_versions()```
Then, download the latest version of spark. Currently, this is `2.2.0`:
```
library(sparklyr)
spark_install(version = "2.2.0", hadoop_version = "2.7")
```
