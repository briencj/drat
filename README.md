---
title: Repository for the most recent versions of packages maintained by Chris Brien
output:
  html_document: default
  pdf_document: default
---

Email: <chris.brien@adelaide.edu.au>
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

Use the links on this page to download either the Windows binary, for one or both of the two versions for R for which binaries are available, or the source file for a package, saving them in a directory on your computer. Then use your favourite method for installing packages on your computer. For example, use the R command `install.packages(repos=NULL, pkgs="path\\file")` where path is the path to the `directory` where you saved the file and `file` is the name of the downloaded file.

(Note: To install the source file under Windows, you need to have [Rtools](https://cran.r-project.org/bin/windows/Rtools/) installed.)

## The packages available

* [`asremlPlus 4.4.16`](#aplus) - augments `ASReml-R` in fitting mixed models and packages generally in exploring prediction differences.

* [`dae 3.2.19`](#dae) - facilitates the use of R for the design and analysis of variance of experiments.

* [`growthPheno 2.1.21`](#gpheno) - functional analysis of phenotypic growth data to smooth and extract traits.

* [`imageData 0.1-62`](#idata) - aids in processing and plotting data from a Lemna-Tec Scananalyzer (superseded by [`growthPheno`](#gpheno)).

### `asremlPlus` {#aplus}
*(last updated 18th October 2023)*

The `asremlPlus` package is a collection of `R` functions to augment `ASReml-R` in fitting mixed models and packages generally in exploring prediction differences. The current version  is compatible with both `ASReml-R` versions 3, 4.1 and 4.2, but not 4.0.  *The current version has known issues when the Intel MKL libraries are installed in the R installation directories.* 

Versions 4.4 of `asremlPlus` are compatible with `ASReml-R` 4.2 and include a number of functions for fitting models for local spatial variation that includes (i) residual correlation models, (ii) two-dimensional tensor-product natural cubic smoothing spline models and (iii) two-dimensional tensor-product P-spline models with the ability to change the degree of the spline and the order of the differencing for the penalty. 

Note that most functions are S3 methods and so the object supplied for the first argument must be of the class (the the function name's suffix) for which the function is a method and the class of the object can be omitted from the function name when calling the function. For example, `plotPredictions.data.frame` is a `plotPredictions` method for a `data.frame` and can be called using just `plotPredictions`; the object supplied to `data` must be a `data.frame`. The `alldiffs` and `data.frame` methods in `asremlPlus` can be applied to objects produced with other mixed modelling software.

For more information, install the package and run the R command `news(package = “asremlPlus”)`. For an overview enter `?asremlPlus`. Otherwise, you could consult the manual using `vignette("Manual", package = "asremlPlus")`. Also available is the Wheat.analysis vignette [`vignette("Wheat.analysis", package = "asremlPlus")`] that shows how to select the terms, using REML ratio tests, to be included in a mixed model for an experiment that involves spatial variation; it also illustrates diagnostic checking and prediction production and presentation for this example. A second vignette is the Wheat.SpatialModels vignette [`vignette("Wheat.SpatialModels", package = "asremlPlus")`] that differs from the Wheat.analysis vignette in using the functions for choosing local spatial variation models and in using the AIC to make the choice of model.  The third Wheat vignette is the Wheat.infoCriteria vignette [`vignette("Wheat.infoCriteria", package = "asremlPlus")`] that illustrates the facilities in `asremlPlus` for producing and using information criteria. Two further vignettes show how to use `asremlPlus` for exploring and presenting predictions from a linear mixed model analysis in the context of a three-factor factorial experiment on ladybirds: one vignette, Ladybird.asreml vignette [`vignette("Ladybird.asreml", package = "asremlPlus")`], uses `asreml` and `asremlPlus` to produce and present  predictions; the other vignette, Ladybird.lm vignette [`vignette("Ladybird.lm", package = "asremlPlus")`], uses `lm` to produce the predictions and `asremlPlus` to present the predictions..

Windows binary R 4.3: [asremlPlus_4.4.16.zip](http://briencj.github.io/drat/bin/windows/contrib/4.3/asremlPlus_4.4.16.zip); Windows binary R 4.2: [asremlPlus_4.4.16.zip](http://briencj.github.io/drat/bin/windows/contrib/4.2/asremlPlus_4.4.16.zip);   Package source: [asremlPlus_4.4.16.tar.gz](http://briencj.github.io/drat/src/contrib/asremlPlus_4.4.16.tar.gz).

The package is also available from CRAN at <https://cran.r-project.org/package=asremlPlus> and from the Github repo at <https://github.com/briencj/asremlPlus>. However, the CRAN version, currently 4.4.15, is not updated as frequently as the version that is here and on [GitHub](https://github.com/briencj/asremlPlus). Older versions of the package and versions for older R versions are available from <https://github.com/briencj/drat/tree/gh-pages>.

The final version of `asremlPlus` that was produced specifically for ASReml-R version 3 is version 2.0-13.  It is no longer being developed. A version of `asremlPlus` 2.0-13 built for `R` 3.5.0 is available as `asreml3Plus`  version 2.0-14; that is, to load this version, a `3` must be included in the package name. 

Windows binary R 3.5: [asreml3Plus_2.0-14.zip](http://briencj.github.io/drat/bin/windows/contrib/3.5/asreml3Plus_2.0-14.zip);  Package source: [asreml3Plus_2.0-14.tar.gz](http://briencj.github.io/drat/src/contrib/asreml3Plus_2.0-14.tar.gz) (built under R 3.5.0).

Windows binary R 3.4: [asremlPlus_2.0-13.zip](http://briencj.github.io/drat/bin/windows/contrib/3.4/asremlPlus_2.0-13.zip);  Package source: [asremlPlus_2.0-13.tar.gz](http://briencj.github.io/drat/src/contrib/asremlPlus_2.0-13.tar.gz).

### `dae` {#dae}
*(last updated 8th August 2023)*

The `dae` package of `R` functions has been developed to facilitate the use of R for the design and analysis of variance of experiments; these days the emphasis is on design. It is described in the manual, which can be found using `vignette("Manual", package = "dae")`. Also found using `vignette("DesignNotes", package = "dae")` is a vignette describing how to use `designRandomize` to produce randomized layouts for experiments and `designAnatomy` to assessing the properties of designs. It covers both standard and multiphase experimental designs. The data sets that go with the vignette are available in `dae`.

Windows binary R 4.3: [dae_3.2.19.zip](http://briencj.github.io/drat/bin/windows/contrib/4.3/dae_3.2.19.zip);  Windows binary R 4.2: [dae_3.2.19.zip](http://briencj.github.io/drat/bin/windows/contrib/4.2/dae_3.2.19.zip);  Package source: [dae_3.2.19.tar.gz](http://briencj.github.io/drat/src/contrib/dae_3.2.19.tar.gz).

The package is also available from CRAN at <https://cran.r-project.org/package=dae> and from the Github repo at <https://github.com/briencj/dae>. However, the CRAN version, currently 3.2.19, is not updated as frequently as the version that is here and on [GitHub](https://github.com/briencj/dae). Older versions of the package and versions for older R versions are available from <https://github.com/briencj/drat/tree/gh-pages>.  

## `growthPheno` {#gpheno}
*(last updated 23rd August 2023)*

The `growthPheno` package is a collection of R functions for the functional analysis of phenotypic growth data to smooth and extract traits (SET), as described by Brien et al. (2020). Version 2.0.15 and subsequent versions represent a major overhaul of the functions and usage of the package. It now has two functions, `traitSmooth` and `traitExtractFeatures`, that are sufficient to perform the SET on a set of growth data. In addition, new functions have been added to the package that will eventually replace the corresponding old functions, the new functions having revised arguments as compared to the old functions in an attempt to simplify function calls.  

The `growthPheno` functions are described in growthPheno-manual.pdf, which can be found using `vignette("Manual", package = "growthPheno")`. An overview can be obtained using `??growthPheno`. Two vignettes, `Tomato` and `Rice`, illustrate the process for smoothing and extraction of traits (SET), the former being the example presented in Brien et al. (2020). Use `vignette("Tomato", package = "growthPheno")` or `vignette("Rice", package = "growthPheno")` to access either of the vignettes. Many of the functions can be applied to longitudinal data in general.

Windows binary R 4.3: [growthPheno_2.1.21.zip](http://briencj.github.io/drat/bin/windows/contrib/4.3/growthPheno_2.1.21.zip); Windows binary R 4.2: [growthPheno_2.1.21.zip](http://briencj.github.io/drat/bin/windows/contrib/4.2/growthPheno_2.1.21.zip);  Package source: [growthPheno_2.1.21.tar.gz](http://briencj.github.io/drat/src/contrib/growthPheno_2.1.21.tar.gz).

The package is also available from CRAN: <https://cran.r-project.org/package=growthPheno> and from the Github repo at <https://github.com/briencj/growthPheno>. However, the CRAN version, currently 2.1.21, is not updated as frequently as the version here. Older versions of the package and versions for older R versions are available from <https://github.com/briencj/drat/tree/gh-pages>.

#### Reference

Brien, C., Jewell, N., Garnett, T., Watts-Williams, S. J., & Berger, B. (2020). Smoothing and extraction of traits in the growth analysis of noninvasive phenotypic data. *Plant Methods*, **16**, 36. <http://dx.doi.org/10.1186/s13007-020-00577-6>.

## `imageData` {#idata}
*(last updated 23rd August 2023)*

This package has been superseded by `growthPheno` and is no longer being developed, being retained for legacy purposes only.

The `imageData` package is a collection of R functions that aids in processing and plotting data from a Lemna-Tec Scananalyzer. It is described in imageData-manual.pdf, which can be found using `vignette("Manual", package = "imageData")`. An overview can be obtained using `?imageData`. The functions can be applied selectively to longitudinal data in general.

Windows binary R 4.3: [imageData_0.1-62.zip](http://briencj.github.io/drat/bin/windows/contrib/4.3/imageData_0.1-62.zip); Windows binary R 4.2: [imageData_0.1-62.zip](http://briencj.github.io/drat/bin/windows/contrib/4.2/imageData_0.1-62.zip);   Package source: [imageData_0.1-62.tar.gz](http://briencj.github.io/drat/src/contrib/imageData_0.1-62.tar.gz).

The package is also available from CRAN: <https://cran.r-project.org/package=imageData>.

