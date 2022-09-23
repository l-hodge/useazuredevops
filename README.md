
# useazuredevops

<!-- badges: start -->
<!-- badges: end -->

This package provides capability to run 'R CMD Check' on R packages in Azure DevOps repositories.

## Installation

You can install the development version of useazuredevops from [GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("l-hodge/useazuredevops")
```

## Example

```r
library(useazuredevops)
use_azure_check()
```
This creates a .yml file in the base directory of your R package. Every time you push changes to the repository the .yml will trigger a 'R CMD Check' and run code coverage. 
