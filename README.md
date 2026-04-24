# EDSD: Bayesian Demography Computer Labs


# About

In the computer labs, we will generate probabilistic population projections for all 19 NUTS-3 regions of Finland, including probabilistic projections of the individual components of population change, such as the total fertility rate, life expectancy at birth and net migration.

# Pre-requisites

## Software
The projections are generated using the programming language [R](https://cran.r-project.org). The most convenient way to work with R is from  the [RStudio Desktop](https://www.rstudio.com/products/rstudio/download). Basic familiarity with R is recommended.

To install packages needed in these labs, open your R application and type

```
install.packages(c("bayesTFR", "bayesLife", "bayesPop", 
        "MortCast", "bayesMig", "devtools"), dependencies = TRUE)
```

The latest UN projections (WPP 2024) are available in the [wpp2024](https://github.com/PPgp/wpp2024) R package. Install it via:

```
options(timeout = 600)
devtools::install_github("PPgp/wpp2024")
```

Check that you have the latest versions installed, for example by typing

```
library(bayesPop)
library(wpp2024)
sessionInfo()
```
You should see versions of the above packages. Check that they are as follows:

```
wpp2024_1.1-3  bayesPop_12.0-1   MortCast_2.8-0   bayesLife_5.3-1   
bayesTFR_7.4-4 
```

## Data
To organize our work, let's set up a working directory, called "EDSDbayespop", which can be done by cloning this repository:

```
git clone https://github.com/PPgp/EDSDbayespop EDSDbayespop
```

Alternatively, one can clone it directly from an R Studio via File -> New Project -> Version Control -> Git. As repository URL enter https://github.com/PPgp/EDSDbayespop and as Project directory name enter EDSDbayespop. Then click on "Create Project".

Both of these alternatives create a directory "EDSDbayespop" which will be your working directory for the labs. It is only a template of the directory structure we will be using. It contains the subdirectory "inputs" that will hold our input datasets.

The subnational data needed in this demo are in a different GitHub repository, namely ["PPgp/bayesPopFINdata"](https://github.com/PPgp/bayesPopFINdata). Clone this repository into the "inputs" subdirectory, called "FINdata". For example, from the command line navigate into the directory "EDSDbayespop/inputs" and clone the repo via

```
git clone https://github.com/PPgp/bayesPopFINdata FINdata
```

Now the directory "EDSDbayespop/inputs/FINdata" should contain the subnational datasets for Finland.

For projecting the total fertility rate and life expectancy at birth (e0), national probabilistic projections are needed and they should be placed into the subdirectory "inputs/wpp2024\_projections". They could be generated from scratch, but to save time, please download them from our [website](https://bayespop.csss.washington.edu/data) as follows:

1. Download the [TFR](https://bayespop.csss.washington.edu/data/bayesTFR/TFR1simWPP2024.tgz) compressed file and unpack it (e.g. using 7-Zip or WinZip on Windows or "tar xvfz" on Unix-based systems) into the "EDSDbayespop/inputs/wpp2024\_projections" directory. It creates a subdirectory called "TFR1unc".
2. Repeat the same with the [e0](https://bayespop.csss.washington.edu/data/bayesLife/e01simWPP2024.tgz) file. It creates a subdirectory called "e01".

After these steps, your "EDSDbayespop" directory should look like this:


# Workshop Material

Coming soon.
