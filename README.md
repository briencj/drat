# Repository for the most recent versions of packages maintained by Chris Brien

Email: <Chris.Brien@unisa.edu.au>
URL: <http://chris.brien.name>

## Installing a package from here

While the packages are available on CRAN, they are more frequently updated here so that often a more recent version will be available from here.

### I. From this repo(sitory) using `drat`

1. Make sure that you have the package [drat](https://cran.r-project.org/web/packages/drat/index.html) installed.

2. When you want to install a package, execute `library(drat)` followed by `addRepo("briencj")` in R, if you have not already done so in your current session.

3. Use `install.packages` or `update.packages` in the usual way: e.g. `install.packages("asremlPlus")`.

### II. Directly from this repo(sitory) without using `drat`

Use the R command `install.packages(pkgs, repos = "http://briencj.github.io/drat")`. 

Replace `install.packages` with `update.packages` to check for updates.

### III. Download and install

Download either the Windows binary or the source file for a package, using the links on this page, to a directory on your computer and then use your favourite method for installing packages on your computer. For example, use the R command `install.packages(repos=NULL, pkgs="path\\file")` where path is the path to the `directory` where you saved the file and `file` is the name of the downloaded file.

(Note: To install the source file under Windows, you need to have [Rtools](https://cran.r-project.org/bin/windows/Rtools/) installed.)

## The packages available

* [`asremlPlus 4.1-37`](#aplus) - augments `ASReml-R` in fitting mixed models and packages generally in exploring prediction differences.

* [`dae 3.1-22`](#dae) - facilitates the use of R for the design and analysis of variance of experiments.

* [`growthPheno 1.0-21`](#gpheno) - plotting, smoothing and growth trait extraction for longitudinal data.

* [`imageData 0.1-59`](#idata) - aids in processing and plotting data from a Lemna-Tec Scananalyzer.

### `asremlPlus` {#aplus}
*(last updated 27th January 2020)*

The `asremlPlus` package is a collection of R functions to augment `ASReml-R` in fitting mixed models and packages generally in exploring prediction differences. The current version  is compatible with both `ASReml-R` versions 3 and 4.1, but not 4.0. Its `alldiffs` and `data.frame` methods can be applied to objects produced with other mixed modelling software.

Versions 4.x-xx of `asremlPlus` are a major revamp of the package and include substantial syntax changes. In particular, most functions are S3 methods and so the object supplied for the first argument must be of the class (the name after the last full stop in the function name) for which the function is a method and the class of the object can be omitted from the function name when calling the function. For example, `plotPredictions.data.frame` is a `plotPredictions` method for a `data.frame` and can be called using just `plotPredictions`; the object supplied to `data` must be a `data.frame`.

For more information, install the package and run the R command `news(package = “asremlPlus”)`. For an overview enter `?asremlPlus`. Otherwise, you could consult the manual using `vignette("Manual", package = "asremlPlus")`. Also available is a vignette describing how to use `asremlPlus` to analyse a wheat experiment that involves spatial variation (`vignette("Wheat", package = "asremlPlus")`) and another that focusses on predictions for a three-factor Ladybird experiment (`vignette("Ladybird", package = "asremlPlus")`).  

Windows binary R 3.6: [asremlPlus_4.1-37.zip](http://briencj.github.io/drat/bin/windows/contrib/3.6/asremlPlus_4.1-37.zip);  Windows binary R 3.5: [asremlPlus_4.1-37.zip](http://briencj.github.io/drat/bin/windows/contrib/3.5/asremlPlus_4.1-37.zip);  Package source: [asremlPlus_4.1-37.tar.gz](http://briencj.github.io/drat/src/contrib/asremlPlus_4.1-37.tar.gz).

The package is also available from CRAN at <https://cran.r-project.org/package=asremlPlus> and from the Github repo at <https://github.com/briencj/asremlPlus>. However, the CRAN version, currently 4.1-36, is not updated as frequently as the version here or on GitHub. 

The final version of `asremlPlus` that was produced specifically for ASReml-R version 3 is version 2.0-13.  It is no longer being developed. A version of `asremlPlus` 2.0-13 built for R 3.5.0 is available as `asreml3Plus`  version 2.0-14; that is, to load this version, a `3` must be included in the package name. 

Windows binary R 3.5: [asreml3Plus_2.0-14.zip](http://briencj.github.io/drat/bin/windows/contrib/3.5/asreml3Plus_2.0-14.zip);  Package source: [asreml3Plus_2.0-14.tar.gz](http://briencj.github.io/drat/src/contrib/asreml3Plus_2.0-14.tar.gz) (built under R 3.5.0).

Windows binary: [asremlPlus_2.0-13.zip](http://briencj.github.io/drat/bin/windows/contrib/3.4/asremlPlus_2.0-13.zip);  Package source: [asremlPlus_2.0-13.tar.gz](http://briencj.github.io/drat/src/contrib/asremlPlus_2.0-13.tar.gz).

### `dae` {#dae}
*(last updated 16th January 2020)*

The `dae` package of R functions has been developed to facilitate the use of R for the design and analysis of variance of experiments; these days the emphasis is on design. It is described in the manual, which can be found using `vignette("Manual", package = "dae")`. Also found using `vignette("DesignNotes", package = "dae")` is a vignette describing how to use `designRandomize` to produce randomized layouts for experiments and `designAnatomy` to assessing the properties of designs. It covers both standard and multiphase experimental designs. The data sets that go with the vignette are available in `dae`.

Windows binary R 3.6: [dae_3.1-22.zip](http://briencj.github.io/drat/bin/windows/contrib/3.6/dae_3.1-22.zip);  Windows binary R 3.5: [dae_3.1-22.zip](http://briencj.github.io/drat/bin/windows/contrib/3.5/dae_3.1-22.zip);  Package source: [dae_3.1-22.tar.gz](http://briencj.github.io/drat/src/contrib/dae_3.1-22.tar.gz).

The package is also available from CRAN at <https://cran.r-project.org/package=dae> and from the Github repo at <https://github.com/briencj/dae>. However, the CRAN version, currently 3.1-21, is not updated as frequently as the version here or on GitHub.  

## `growthPheno` {#gpheno}
*(last updated 12th January 2020)*

The `growthPheno` package is a collection of R functions that can be used to plot, smooth and extract growth traits for longitudinal data. It is described in growthPheno-manual.pdf, which can be found using `vignette("Manual", package = "growthPheno")`. An overview can be obtained using `?growthPheno`. Many of the functions can be applied to longitudinal data in general.

Windows binary R 3.6: [growthPheno_1.0-21.zip](http://briencj.github.io/drat/bin/windows/contrib/3.6/growthPheno_1.0-21.zip);  Windows binary R 3.5: [growthPheno_1.0-21.zip](http://briencj.github.io/drat/bin/windows/contrib/3.5/growthPheno_1.0-21.zip);  Package source: [growthPheno_1.0-21.tar.gz](http://briencj.github.io/drat/src/contrib/growthPheno_1.0-21.tar.gz).

The package is also available from CRAN: <https://cran.r-project.org/package=growthPheno>. However, the CRAN version, currently 1.0-15, is not updated as frequently as the version here.


## `imageData` {#idata}
*(last updated 23rd June 2019)*

This package has been superseded by `growthPheno` and is no longer maintained, being retained for legacy purposes only..

The `imageData` package is a collection of R functions that aids in processing and plotting data from a Lemna-Tec Scananalyzer. It is described in imageData-manual.pdf, which can be found using `vignette("Manual", package = "imageData")`. An overview can be obtained using `?imageData`. The functions can be applied selectively to longitudinal data in general.

Windows binary R 3.6: [imageData_0.1-59.zip](http://briencj.github.io/drat/bin/windows/contrib/3.6/imageData_0.1-59.zip);  Windows binary R 3.5: [imageData_0.1-59.zip](http://briencj.github.io/drat/bin/windows/contrib/3.5/imageData_0.1-59.zip);  Package source: [imageData_0.1-59.tar.gz](http://briencj.github.io/drat/src/contrib/imageData_0.1-59.tar.gz).

The package is also available from CRAN: <https://cran.r-project.org/package=imageData>.

