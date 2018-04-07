---
output:
  html_document: default
  pdf_document: default
---
# Drat repository for most recent versions of packages maintained by C. J. Brien

## Installing packages from this repo using `drat`

1. Make sure that you have the package `drat` installed (it is available on CRAN).

2. When you want to install a package, execute `addRep("briencj")`, if you have not already done so in your current session.

3. Use `install.packages` or `update.packages` in the usual way: e.g. `install.packages("asremlPlus")`.

## Installing packages directly

Use `install.packages(pkgs, repos = "http://briencj.github.io/drat")`.

## The packages available

### `asremlPlus` 
*(last updated 29th December 2017)*

The `asremlPlus` package is a collection of R functions to augment the use of `ASReml-R` in fitting mixed models . This version  is compatible with both `ASReml-R` versions 3 and 4. `ASReml-R` version 4 is currently undergoing $\beta$-testing and has some changes in syntax that necessitate changes in `asremlPlus`. This version of `asremlPlus` is a major revamp of the package and also includes substantial syntax changes. For more information install the package and run the R command `news(package = “asremlPlus”)` or consult the manual. An overview can be obtained using `?asremlPlus`.

Windows binary: [asremlPlus_4.0-27.zip](http://briencj.github.io/drat/bin/windows/contrib/3.5/asremlPlus_4.0-27.zip);  Package source: [asremlPlus_4.0-27.tar.gz](http://briencj.github.io/drat/src/contrib/asremlPlus_4.0-27.tar.gz).

### `dae`
*(last updated 6th April 2018)*

The `dae` package of R functions has been developed to facilitate the use of R for the design and analysis of variance of experiments. It is described in dae-manual.pdf, which is also found in the dae\\doc directory where the package is installed. Also found in this directory is a vignette describing the how to use designRandomize to produce randomized layout for experiments and designAnatomy to assessing the properties of designs. It covers both standard and multiphase experimental designs. The data sets that go with the vignette are available in dae.

Windows binary: [dae_3.0-15.zip](http://briencj.github.io/drat/bin/windows/contrib/3.5/dae_3.0-15.zip);  Package source: [dae_3.0-15.tar.gz](http://briencj.github.io/drat/src/contrib/dae_3.0-15.tar.gz).
