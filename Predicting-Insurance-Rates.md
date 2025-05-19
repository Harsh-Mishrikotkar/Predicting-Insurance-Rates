Predicting-Insurance-Rates
================
Harsh Mishrikotkar
2025-05-19

### Importing Libraries and the Data Set

    ## ── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
    ## ✔ dplyr     1.1.4     ✔ readr     2.1.5
    ## ✔ forcats   1.0.0     ✔ stringr   1.5.1
    ## ✔ ggplot2   3.5.1     ✔ tibble    3.2.1
    ## ✔ lubridate 1.9.4     ✔ tidyr     1.3.1
    ## ✔ purrr     1.0.4     
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()
    ## ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors
    ## 
    ## Attaching package: 'gridExtra'
    ## 
    ## 
    ## The following object is masked from 'package:dplyr':
    ## 
    ##     combine
    ## 
    ## 
    ## Rows: 1338 Columns: 7
    ## ── Column specification ────────────────────────────────────────────────────────
    ## Delimiter: ","
    ## chr (3): sex, smoker, region
    ## dbl (4): age, bmi, children, charges
    ## 
    ## ℹ Use `spec()` to retrieve the full column specification for this data.
    ## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

### Explanation of Variables and Summary of data set

- **Age:** Age of primary beneficiary
- **Sex:** Insurance contractor gender, female, male
- **BMI:** Body mass index, providing an understanding of body, weights
  that are relatively high or low relative to height, objective index of
  body weight (kg / m ^ 2) using the ratio of height to weight
- **Children:** Number of children covered by health insurance / Number
  of dependents
- **Smoker:** Smoking
- **Region** The beneficiary’s residential area in the US, northeast,
  southeast, southwest, northwest
- **Charges:** Individual medical costs billed by health insurance

<!-- -->

    ##       age            sex                 bmi           children    
    ##  Min.   :18.00   Length:1338        Min.   :15.96   Min.   :0.000  
    ##  1st Qu.:27.00   Class :character   1st Qu.:26.30   1st Qu.:0.000  
    ##  Median :39.00   Mode  :character   Median :30.40   Median :1.000  
    ##  Mean   :39.21                      Mean   :30.66   Mean   :1.095  
    ##  3rd Qu.:51.00                      3rd Qu.:34.69   3rd Qu.:2.000  
    ##  Max.   :64.00                      Max.   :53.13   Max.   :5.000  
    ##     smoker             region             charges     
    ##  Length:1338        Length:1338        Min.   : 1122  
    ##  Class :character   Class :character   1st Qu.: 4740  
    ##  Mode  :character   Mode  :character   Median : 9382  
    ##                                        Mean   :13270  
    ##                                        3rd Qu.:16640  
    ##                                        Max.   :63770

![](Predicting-Insurance-Rates_files/figure-gfm/create%20histograms%20and%20bar%20charts-1.png)<!-- -->

#### Based of the Histogram and Bar plots:

- **Age**
  - has no distribution, with a slightly larger grouping at
    approximately 20, 30, 40 and 54
- **Sex**
  - has an almost equal split between Male and Female, with Male
    occurring slightly more often
- **BMI**
  - has an approximately normal distribution with a peak at about 30
- **Children**
  - has a skewed right distribution with a peak at 0
- **Smoker**
  - has a large split between smokers and non smokers, with a large
    majority of the beneficiaries being non-smokers
- **Region**
  - has an almost equal split between the 4 regions, with slightly more
    beneficiaries being from the southeast
- **Charges**
  - has a skewed right distribution with a peak just bellow \$10,000
