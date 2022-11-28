
# useazuredevops

<!-- badges: start -->
[![R-CMD-check](https://github.com/l-hodge/useazuredevops/workflows/R-CMD-check/badge.svg)](https://github.com/l-hodge/useazuredevops/actions)
<!-- badges: end -->

This package provides [usethis](https://usethis.r-lib.org/)-like functionality to setup the automated running of `R CMD check` for R packages in Azure DevOps repositories.

## Installation

You can install the development version of useazuredevops from [GitHub](https://github.com/l-hodge/useazuredevops) with:

``` r
# install.packages("devtools")
devtools::install_github("l-hodge/useazuredevops")
```

## Example

```r
library(useazuredevops)
use_azure_check()
```
This creates a .yml file in the base directory of your R package. Subsequently, every time changes are committed to the repository this workflow installs the latest release of R (on a current distribution of Linux) and runs `R CMD check` via the [rcmdcheck](https://github.com/r-lib/rcmdcheck) package and code coverage via the [covr](https://github.com/r-lib/covr/) package.
