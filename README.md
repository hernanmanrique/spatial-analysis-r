
<!-- README.md is generated from README.Rmd. Please edit that file -->
<!-- IMPORTANT: DO NOT KNIT WITH KNIT BUTTON. INSTEAD USE THIS:
     rmarkdown::render('README.Rmd', output_format = 'github_document', output_file = 'README.md') 
-->

# An Introduction to Spatial Data Analysis and Statistics: A Course in R

<!-- badges: start -->
<!-- NOTE: the binder badge was created by holepunch and it makes reference to 
     ../gh/paezha/spatial-analysis-R/master?urlpath=rstudio 
     This causes a mistake, as master branch is now named main. Revise to ../gh/paezha/spatial-analysis-R/main?urlpath=rstudio
-->

[![Launch Rstudio
Binder](http://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/paezha/spatial-analysis-R/main?urlpath=rstudio)
[![Netlify
Status](https://api.netlify.com/api/v1/badges/2867ef30-f33c-4043-9940-fac934c27341/deploy-status)](https://app.netlify.com/sites/spatial-analysis-r/deploys)
[![DOI](https://zenodo.org/badge/391072865.svg)](https://zenodo.org/badge/latestdoi/391072865)
<!-- badges: end -->

## Introduction

This repository hosts the code underlying the book *An Introduction to
Spatial Data Analysis and Statistics: A Course in R*, by [Antonio
Paez](https://www.science.mcmaster.ca/ees/component/comprofiler/userprofile/paezha.html):

> Paez, Antonio (2021). *An Introduction to Spatial Data Analysis and
> Statistics: A Course in R*. McMaster Invisible Press. The online
> version of this book is free to read at
> <https://www.spatial-analysis-R.org/>.

This part was copied from Geocompr:

## Contributing

We encourage contributions on any part of the book, including:

-   improvements to the text, e.g. clarifying unclear sentences, fixing
    typos (see guidance from [Yihui
    Xie](https://yihui.name/en/2013/06/fix-typo-in-documentation/));
-   changes to the code, e.g. to do things in a more efficient way; and
-   suggestions on content (see the project’s [issue
    tracker](https://github.com/paezha/spatial-analysis-R/issues)).

<!-- Need to check what the style is
See [our-style.md](https://github.com/Robinlovelace/geocompr/blob/master/our-style.md) for the book's style.

-->

Many thanks to all contributors to the book so far via GitHub (this list
will update automatically):
[Robinlovelace](https://github.com/Robinlovelace).

<!-- Need to figure out what this is
During the project we aim to contribute 'upstream' to the packages that make geocomputation with R possible.
This impact is recorded in [`our-impact.csv`](https://github.com/Robinlovelace/geocompr/blob/master/our-impact.csv).
-->

## Reproducing the book

TODO <!--
To ease reproducibility, we created the `geocompkg` package.
Installing it from GitHub will install all the R packages needed build the book (you will a computer with necessary [system dependencies](https://github.com/r-spatial/sf#installing) and the [**remotes**](https://github.com/r-lib/remotes/) package installed):



```r
install.packages("remotes")
remotes::install_github("geocompr/geocompkg")
```

You need a recent version of the GDAL, GEOS, PROJ and UDUNITS libraries installed for this to work on Mac and Linux. See the **sf** package's [README](https://github.com/r-spatial/sf) for information on that.

Once the dependencies have been installed you should be able to build and view a local version the book with:


```r
bookdown::render_book("index.Rmd") # to build the book
browseURL("_book/index.html") # to view it
```

<!-- The code associated with each chapter is saved in the `code/chapters/` folder. -->
<!-- `source("code/chapters/07-transport.R")` runs run the code chunks in chapter 7, for example. -->
<!-- These R scripts are generated with the follow command which wraps `knitr::purl()`: -->

## Geocompr in binder

TODO <!--
For many people the quickest way to get started with Geocomputation with R is in your web browser via Binder.
To see an interactive RStudio Server instance click on the following button, which will open [mybinder.org](https://mybinder.org/v2/gh/robinlovelace/geocompr/master?urlpath=rstudio) with an R installation that has all the dependencies needed to reproduce the book:

#[![Launch Rstudio Binder](http://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/robinlovelace/geocompr/master?urlpath=rstudio)

You can also have a play with the repo in RStudio Cloud by clicking on this link (requires log-in):

-->

## Spatial Data Analysis and Statistics in a Docker container

TODO <!--
To ease reproducibility we have made Docker images available, at [geocompr/geocompr](https://hub.docker.com/r/geocompr/geocompr/) on DockerHub.
These images allow you to explore Geocomputation with R in a virtual machine that has up-to-date dependencies.

After you have [installed docker](https://www.docker.com/community-edition#/download) and set-it up on [your computer](https://docs.docker.com/install/linux/linux-postinstall/) you can start RStudio Server without a password (see the [Rocker project](https://www.rocker-project.org/use/managing_users/) for info on how to add a password and other security steps for public-facing servers):

```sh
docker run -p 8787:8787 -e DISABLE_AUTH=TRUE geocompr/geocompr
```

If it worked you should be able to open-up RStudio server by opening a browser and navigating to
http://localhost:8787/ resulting in an up-to-date version of R and RStudio running in a container.

Start a plain R session running:

```sh
docker run -it geocompr/geocompr R
```

See the [geocompr/docker](https://github.com/geocompr/docker#geocomputation-with-r-in-docker) repo for details, including how to share volumes between your computer and the Docker image, for using geographic R packages on your own data and for information on available tags.
-->

## Reproducing this README

To reduce the book’s dependencies, scripts to be run infrequently to
generate input for the book are run on creation of this README.

The additional packages required for this can be installed as follows:

``` r
source("code/extra-pkgs.R")
```

With these additional dependencies installed, you should be able to run
the following scripts, which create content for the book, that we’ve
removed from the main book build to reduce package dependencies and the
book’s build time:

``` r
source("code/cranlogs.R")
source("code/sf-revdep.R")
source("code/08-urban-animation.R")
source("code/08-map-pkgs.R")
```

Note: the `.Rproj` file is configured to build a website not a single
page. To reproduce this
[README](https://github.com/Robinlovelace/geocompr/blob/master/README.Rmd)
use the following command:

``` r
rmarkdown::render("README.Rmd", output_format = "github_document", output_file = "README.md")
```

<!-- ## Book statistics -->
<!-- An indication of the book's progress over time is illustrated below (to be updated roughly every week as the book progresses). -->
<!--






<!-- Book statistics: estimated number of pages per chapter over time. -->

## Citations

TODO

<!--
To cite packages used in this book we use code from [Efficient R Programming](https://csgillespie.github.io/efficientR/):


```r
# geocompkg:::generate_citations()
```

This generates .bib and .csv files containing the packages.
The current of packages used can be read-in as follows:


```r
#pkg_df = readr::read_csv("extdata/package_list.csv")
```

Other citations are stored online using Zotero.

If you would like to add to the references, please use Zotero, join the [open group](https://www.zotero.org/groups/418217/energy-and-transport) add your citation to the open [geocompr library](https://www.zotero.org/groups/418217/energy-and-transport/items/collectionKey/9K6FRP6N).

We use the following citation key format:

```
[auth:lower]_[veryshorttitle:lower]_[year]
```

This can be set from inside Zotero desktop with the Better Bibtex plugin installed (see [github.com/retorquere/zotero-better-bibtex](https://github.com/retorquere/zotero-better-bibtex)) by selecting the following menu options (with the shortcut `Alt+E` followed by `N`), and as illustrated in the figure below:

```
Edit > Preferences > Better Bibtex
```

![](figures/zotero-settings.png)

Zotero settings: these are useful if you want to add references.

We use Zotero because it is a powerful open source reference manager that integrates well with the **citr** package.
As described in the GitHub repo [Robinlovelace/rmarkdown-citr-demo](https://github.com/Robinlovelace/rmarkdown-citr-demo).

## References


```r
# remotes::install_github("gadenbuie/regexplain")
# regexplain::regexplain_file("extdata/package_list.csv")
#pattern = " \\[[^\\}]*\\]" # perl=TRUE
#pkg_df$Title = gsub(pattern = pattern, replacement = "", x = pkg_df$Title, perl = TRUE)
#knitr::kable(pkg_df)
```
-->
