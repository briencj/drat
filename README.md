---
title: Repository for the most recent versions of packages maintained by Chris Brien
output:
  html_document: default
  pdf_document: default
  word_document: default
---

Email: <Chris.Brien@unisa.edu.au>
URL: <http:\\chris.brien.name>

## Installing a package

### I. From this repo using `drat`

1. Make sure that you have the package [drat](https://cran.r-project.org/web/packages/drat/index.html) installed.

2. When you want to install a package, execute `library(drat)` followed by `addRepo("briencj")` in R, if you have not already done so in your current session.

3. Use `install.packages` or `update.packages` in the usual way: e.g. `install.packages("asremlPlus")`.

### Directly from this repo

Use the R command `install.packages(pkgs, repos = "http://briencj.github.io/drat")`. 

Replace `install.packages` with `update.packages` to check for updates.

### Download and install

Download either the Windows binary or the source file for a package, using the links on this page, to a directory on your computer and then use your favourite method for installing packages on your computer. For example, use the R command `install.packages(repos=NULL, pkgs="path\\file")` where path is the path to the `directory` where you saved the file and `file` is the name of the downloaded file.

(Note: To install the source file under Windows, you need to have [Rtools](https://cran.r-project.org/bin/windows/Rtools/) installed.)

## The packages available

* [`asremlPlus`](#aplus) - augments the use of `ASReml-R` in fitting mixed models.

* [`dae`](#dae) - facilitates the use of R for the design and analysis of variance of experiments.

* [`imageData`](#idata) - aids in processing and plotting data from a Lemna-Tec Scananalyzer.

### `asremlPlus` {#aplus}
*(last updated 23rd September 2018)*

The `asremlPlus` package is a collection of R functions to augment the use of `ASReml-R` in fitting mixed models. This version  is compatible with both `ASReml-R` versions 3 and 4.1, but not 4.0. `ASReml-R` version 4.1 is currently undergoing $\beta$-testing and has some changes in syntax that necessitate changes in `asremlPlus`. This version of `asremlPlus` is a major revamp of the package and also includes substantial syntax changes. For more information install the package and run the R command `news(package = “asremlPlus”)` or consult the manual. An overview can be obtained using `?asremlPlus`.

Windows binary: [asremlPlus_4.1-07.zip](http://briencj.github.io/drat/bin/windows/contrib/3.5/asremlPlus_4.1-07.zip);  Package source: [asremlPlus_4.1-07.tar.gz](http://briencj.github.io/drat/src/contrib/asremlPlus_4.1-07.tar.gz).

The package is also be available from CRAN [asremlPlus_2.0-13](https://cran.r-project.org/web/packages/asremlPlus/index.html). However, the version on CRAN may not be the latest version. 
The final version of asremlPlus that was produced specifically for ASReml-R version 3 is version 2.0-13.  It is no longer being developed. It is described in asremlPlus.pdf, which also found in the `asremlPlus\doc` directory where the package is installed. An overview can be obtained using `?asremlPlus`. A version built for R 3.5.0 is available as `asreml3Plus`  version 2.0-14; that is, to use this version, a `3` must be included in the package name. 

Windows binary: [asreml3Plus_2.0-14.zip](http://briencj.github.io/drat/bin/windows/contrib/3.5/asreml3Plus_2.0-14.zip);  Package source: [asreml3Plus_2.0-14.tar.gz](http://briencj.github.io/drat/src/contrib/asreml3Plus_2.0-14.tar.gz) (built under R 3.5.0).

Windows binary: [asremlPlus_2.0-13.zip](http://briencj.github.io/drat/bin/windows/contrib/3.4/asremlPlus_2.0-13.zip);  Package source: [asremlPlus_2.0-13.tar.gz](http://briencj.github.io/drat/src/contrib/asremlPlus_2.0-13.tar.gz).

### `dae` {#dae}
*(last updated 17th October 2018)*

The `dae` package of R functions has been developed to facilitate the use of R for the design and analysis of variance of experiments; these days the emphasis is on design. It is described in dae-manual.pdf, which is also found in the `dae\doc` directory where the package is installed. Also found in this directory is a vignette describing the how to use designRandomize to produce randomized layout for experiments and designAnatomy to assessing the properties of designs. It covers both standard and multiphase experimental designs. The data sets that go with the vignette are available in dae.

Windows binary: [dae_3.0-23.zip](http://briencj.github.io/drat/bin/windows/contrib/3.5/dae_3.0-23.zip);  Package source: [dae_3.0-23.tar.gz](http://briencj.github.io/drat/src/contrib/dae_3.0-23.tar.gz).

The package is also available from CRAN: <https://cran.r-project.org/web/packages/dae/index.html>. However, the version here is likely to be more recent than that on CRAN.

## `imageData` {#idata}
*(last updated 15th July 2018)*

The `imageData` package is a collection of R functions that aids in processing and plotting data from a Lemna-Tec Scananalyzer. It is described in imageData-manual.pdf, which also found in the `imageData\doc` directory where the package is installed. An overview can be obtained using `?imageData`. The functions can be applied selectively to longitudinal data in general.

Windows binary: [imageData_0.1-53.zip](http://briencj.github.io/drat/bin/windows/contrib/3.5/imageData_0.1-53.zip);  Package source: [imageData_0.1-53.tar.gz](http://briencj.github.io/drat/src/contrib/imageData_0.1-53.tar.gz).

The package is also available from CRAN: <https://cran.r-project.org/web/packages/imageData/index.html>. However, the version here is likely to be more recent than that on CRAN.

