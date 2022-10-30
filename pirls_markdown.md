PIRLS Hypotheses–Reproducible Code
================
4/15/2022

# Concatenate the data

Start by importing the data which has been downloaded from the PIRLS
website. Then re-code the dependent variables.

``` r
setwd("C:\\path\\ goes \\here")
pirls <-  intsvy::pirls.select.merge(folder = getwd(), 
                                     countries = c("USA"),
                                      student = c("IDSTUD"),
                                     school = c("ACBG03B"),
                                       teacher = c("ATBG05BB", "ATBG05BF", "ATBG05BC", "ATBR11F","ATBR13A", 
                                                   "ATBR20B", "ATBR11D", "ATBG05BF", "ATBG02", "ATBR12B", "ATBR11G", 
                                                   "ATBG05AA", "ATBR06","ATBR07","ATBR18","ATBR19A","ATBR19B","ATBR19C",
                                                   "ATBR11E","ATBR12E", "ATBR12C", "ATBG05BD", "ATBG10B", "ATBG06", "ATBR11E",
                                                   "ATBR12F", "ATBG05AD","ATBG05AB","ATBG05AA", "ATBR11C", "ATBR06", "ATBR07",
                                                   "ATBR14CA", "ATBR14CB", "ATBR14CC", "ATBR14CD","ATBR14CE", "ATBR14CF", "ATBG01","ATBR10D", "ATBG07A", "ATBR10B", "ATBG05AA"))


pirls$ATBR11F <- car::recode(pirls$ATBR11F, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR11G <- car::recode(pirls$ATBR11G, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR12B <- car::recode(pirls$ATBR12B, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR11E <- car::recode(pirls$ATBR11E, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR12C <- car::recode(pirls$ATBR12C, '1 = 4; 2 = 3; 3 = 2; 4 = 1')

pirls$ATBR13A <- car::recode(pirls$ATBR13A, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR11D <- car::recode(pirls$ATBR11D, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR12B <- car::recode(pirls$ATBR12B, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR11G <- car::recode(pirls$ATBR11G, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR18 <- car::recode(pirls$ATBR18, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR19A <- car::recode(pirls$ATBR19A, '1 = 3; 2 = 3; 3 = 2') # only goes up to 3

pirls$ATBR19B <- car::recode(pirls$ATBR19B, '1 = 3; 2 = 3; 3 = 2') # only goes up to 3

pirls$ATBR19C <- car::recode(pirls$ATBR19C, '1 = 3; 2 = 3; 3 = 2') # only goes up to 3

pirls$ATBR11E <- car::recode(pirls$ATBR11E, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR12E <- car::recode(pirls$ATBR12E, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR12C <- car::recode(pirls$ATBR12C, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR11E <- car::recode(pirls$ATBR11E, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR12F <- car::recode(pirls$ATBR12F, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR11D <- car::recode(pirls$ATBR11D, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR11G <- car::recode(pirls$ATBR11G, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR11C <- car::recode(pirls$ATBR11C, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR14CA <- car::recode(pirls$ATBR14CA, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR14CB <- car::recode(pirls$ATBR14CB, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR14CC <- car::recode(pirls$ATBR14CC, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR14CD <- car::recode(pirls$ATBR14CD, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR14CE <- car::recode(pirls$ATBR14CE, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR14CF <- car::recode(pirls$ATBR14CF, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR10D <- car::recode(pirls$ATBR10D, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBG07A <- car::recode(pirls$ATBG07A, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR10B <- car::recode(pirls$ATBR10B, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 
```

# Select variables

and sample the data using dplyr. Save the sampled data as an object.

``` r
library(dplyr)

pirls1 <- pirls %>%
  dplyr::select(ATBG05AD, ATBG07A, ATBG01,ATBR11D, ATBR12E,ATBR11G, ATBR11F,ATBR11C, ATBR11E, ATBR14CA, ATBR14CC, ATBR14CC, ATBR14CD, ATBR14CE, ATBR14CF, ATBR06, ATBR07, ATBR10D, ATBR10B,ATBG05AA)

pirls2 <- na.omit(pirls1) # omit rows with missing information

Samp <- pirls2 %>%
  group_by(ATBG05AA) %>%
  dplyr::filter(., ATBG01 < 6) #%>%
 # sample_frac(.9) # sample the dataframe...actually not needed
```

## Work with the data

to run tests. Shapiro test in R to run for normality,

``` r
setwd("C:\\Users\\mario\\OneDrive\\Desktop\\PIRLS\\P16_SPSSData_pt2")
pirls <-  intsvy::pirls.select.merge(folder = getwd(), 
                                     countries = c("USA"),
                                      student = c("IDSTUD"),
                                     school = c("ACBG03B"),
                                       teacher = c("ATBG05BB", "ATBG05BF", "ATBG05BC", "ATBR11F","ATBR13A", 
                                                   "ATBR20B", "ATBR11D", "ATBG05BF", "ATBG02", "ATBR12B", "ATBR11G", 
                                                   "ATBG05AA", "ATBR06","ATBR07","ATBR18","ATBR19A","ATBR19B","ATBR19C",
                                                   "ATBR11E","ATBR12E", "ATBR12C", "ATBG05BD", "ATBG10B", "ATBG06", "ATBR11E",
                                                   "ATBR12F", "ATBG05AD","ATBG05AB","ATBG05AA", "ATBR11C", "ATBR06", "ATBR07",
                                                   "ATBR14CA", "ATBR14CB", "ATBR14CC", "ATBR14CD","ATBR14CE", "ATBR14CF", "ATBG01","ATBR10D", "ATBG07A", "ATBR10B", "ATBG05AA"))


pirls$ATBR11F <- car::recode(pirls$ATBR11F, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR11G <- car::recode(pirls$ATBR11G, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR12B <- car::recode(pirls$ATBR12B, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR11E <- car::recode(pirls$ATBR11E, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR12C <- car::recode(pirls$ATBR12C, '1 = 4; 2 = 3; 3 = 2; 4 = 1')

pirls$ATBR13A <- car::recode(pirls$ATBR13A, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR11D <- car::recode(pirls$ATBR11D, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR12B <- car::recode(pirls$ATBR12B, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR11G <- car::recode(pirls$ATBR11G, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR18 <- car::recode(pirls$ATBR18, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR19A <- car::recode(pirls$ATBR19A, '1 = 3; 2 = 3; 3 = 2') # only goes up to 3

pirls$ATBR19B <- car::recode(pirls$ATBR19B, '1 = 3; 2 = 3; 3 = 2') # only goes up to 3

pirls$ATBR19C <- car::recode(pirls$ATBR19C, '1 = 3; 2 = 3; 3 = 2') # only goes up to 3

pirls$ATBR11E <- car::recode(pirls$ATBR11E, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR12E <- car::recode(pirls$ATBR12E, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR12C <- car::recode(pirls$ATBR12C, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR11E <- car::recode(pirls$ATBR11E, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR12F <- car::recode(pirls$ATBR12F, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR11D <- car::recode(pirls$ATBR11D, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR11G <- car::recode(pirls$ATBR11G, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR11C <- car::recode(pirls$ATBR11C, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR14CA <- car::recode(pirls$ATBR14CA, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR14CB <- car::recode(pirls$ATBR14CB, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR14CC <- car::recode(pirls$ATBR14CC, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR14CD <- car::recode(pirls$ATBR14CD, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR14CE <- car::recode(pirls$ATBR14CE, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR14CF <- car::recode(pirls$ATBR14CF, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR10D <- car::recode(pirls$ATBR10D, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBG07A <- car::recode(pirls$ATBG07A, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 

pirls$ATBR10B <- car::recode(pirls$ATBR10B, '1 = 4; 2 = 3; 3 = 2; 4 = 1') 
```

# Select variables, and sample the data using dplyr. Save the sampled data as an object.

``` r
library(tidyverse)

# Strategy 1: sample the whole group

library(dplyr)

pirls1 <- pirls %>%
  dplyr::select(ATBG05AD, ATBG07A, ATBG01,ATBR11D, ATBR12E,ATBR11G, ATBR11F,ATBR11C, ATBR11E, ATBR14CA, ATBR14CC, ATBR14CC, ATBR14CD, ATBR14CE, ATBR14CF, ATBR06, ATBR07, ATBR10D, ATBR10B,ATBG05AA)

pirls2 <- pirls1 %>%
  tidyr::drop_na(ATBG01) # omit rows with missing information



Samp <- pirls2 %>%
  group_by(ATBG05AA) %>%
  dplyr::filter(., ATBG01 < 6) 

# n = 922 

saveRDS(Samp, "c:/users/mario/OneDrive/Desktop/PIRLS/SAMPLED DATA/beginningteachers_correct_variable_5yrs-922.rds")
```

## Work with the data to run tests. Shaprio-wilks to run for normality, Wilcoxon tests to run for non-parametric version of t-tests, and the t-test

``` r
library(tidyverse)
```

    ## -- Attaching packages --------------------------------------- tidyverse 1.3.2 --
    ## v ggplot2 3.3.6     v purrr   0.3.4
    ## v tibble  3.1.7     v dplyr   1.0.9
    ## v tidyr   1.2.0     v stringr 1.4.0
    ## v readr   2.1.2     v forcats 0.5.1

    ## Warning: package 'ggplot2' was built under R version 4.1.3

    ## Warning: package 'tibble' was built under R version 4.1.3

    ## Warning: package 'tidyr' was built under R version 4.1.3

    ## Warning: package 'readr' was built under R version 4.1.3

    ## Warning: package 'dplyr' was built under R version 4.1.3

    ## -- Conflicts ------------------------------------------ tidyverse_conflicts() --
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

``` r
# ATBR12E ATBR11D, ATBR12E,ATBR11G, ATBR11F,ATBR11C,ATBR11C, ATBR11E, ATBR14CA, ATBR14CC,  ATBR14CD, ATBR14CE, ATBR14CF, ATBR06, ATBR07, ATBR10D



mydata <- readRDS("c:/users/mario/OneDrive/Desktop/PIRLS/SAMPLED DATA/beginningteachers_correct_variable_5yrs-922.rds")

mydata$ATBG05AA <- as.character(mydata$ATBG05AA)
```

``` r
mydata[1:18] %>%
map(., function(x) shapiro.test(x)) 
```

    ## $ATBG05AD
    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  x
    ## W = 0.55046, p-value < 2.2e-16
    ## 
    ## 
    ## $ATBG07A
    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  x
    ## W = 0.77507, p-value < 2.2e-16
    ## 
    ## 
    ## $ATBG01
    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  x
    ## W = 0.86618, p-value < 2.2e-16
    ## 
    ## 
    ## $ATBR11D
    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  x
    ## W = 0.42019, p-value < 2.2e-16
    ## 
    ## 
    ## $ATBR12E
    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  x
    ## W = 0.73447, p-value < 2.2e-16
    ## 
    ## 
    ## $ATBR11G
    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  x
    ## W = 0.78672, p-value < 2.2e-16
    ## 
    ## 
    ## $ATBR11F
    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  x
    ## W = 0.81495, p-value < 2.2e-16
    ## 
    ## 
    ## $ATBR11C
    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  x
    ## W = 0.57004, p-value < 2.2e-16
    ## 
    ## 
    ## $ATBR11E
    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  x
    ## W = 0.50382, p-value < 2.2e-16
    ## 
    ## 
    ## $ATBR14CA
    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  x
    ## W = 0.83168, p-value < 2.2e-16
    ## 
    ## 
    ## $ATBR14CC
    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  x
    ## W = 0.86643, p-value < 2.2e-16
    ## 
    ## 
    ## $ATBR14CD
    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  x
    ## W = 0.87198, p-value < 2.2e-16
    ## 
    ## 
    ## $ATBR14CE
    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  x
    ## W = 0.83007, p-value < 2.2e-16
    ## 
    ## 
    ## $ATBR14CF
    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  x
    ## W = 0.87147, p-value < 2.2e-16
    ## 
    ## 
    ## $ATBR06
    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  x
    ## W = 0.93334, p-value < 2.2e-16
    ## 
    ## 
    ## $ATBR07
    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  x
    ## W = 0.91907, p-value < 2.2e-16
    ## 
    ## 
    ## $ATBR10D
    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  x
    ## W = 0.82778, p-value < 2.2e-16
    ## 
    ## 
    ## $ATBR10B
    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  x
    ## W = 0.68291, p-value < 2.2e-16

``` r
lapply(mydata[-19], function(x) WRS2::yuenbt(x ~ mydata$ATBG05AA))
```

    ## $ATBG05AD
    ## Call:
    ## WRS2::yuenbt(formula = x ~ mydata$ATBG05AA)
    ## 
    ## Test statistic: Inf (df = NA), p-value = 0
    ## 
    ## Trimmed mean difference:  1 
    ## 95 percent confidence interval:
    ## NA     NA 
    ## 
    ## 
    ## $ATBG07A
    ## Call:
    ## WRS2::yuenbt(formula = x ~ mydata$ATBG05AA)
    ## 
    ## Test statistic: 0.9782 (df = NA), p-value = 0.29716
    ## 
    ## Trimmed mean difference:  0.08207 
    ## 95 percent confidence interval:
    ## -0.0791     0.2433 
    ## 
    ## 
    ## $ATBG01
    ## Call:
    ## WRS2::yuenbt(formula = x ~ mydata$ATBG05AA)
    ## 
    ## Test statistic: 0.8194 (df = NA), p-value = 0.38397
    ## 
    ## Trimmed mean difference:  0.21503 
    ## 95 percent confidence interval:
    ## -0.2751     0.7052 
    ## 
    ## 
    ## $ATBR11D
    ## Call:
    ## WRS2::yuenbt(formula = x ~ mydata$ATBG05AA)
    ## 
    ## Test statistic: -4.3627 (df = NA), p-value = 0
    ## 
    ## Trimmed mean difference:  -0.34328 
    ## 95 percent confidence interval:
    ## -0.5013     -0.1852 
    ## 
    ## 
    ## $ATBR12E
    ## Call:
    ## WRS2::yuenbt(formula = x ~ mydata$ATBG05AA)
    ## 
    ## Test statistic: 11.0638 (df = NA), p-value = 0
    ## 
    ## Trimmed mean difference:  0.92815 
    ## 95 percent confidence interval:
    ## 0.7657     1.0906 
    ## 
    ## 
    ## $ATBR11G
    ## Call:
    ## WRS2::yuenbt(formula = x ~ mydata$ATBG05AA)
    ## 
    ## Test statistic: 8.5782 (df = NA), p-value = 0
    ## 
    ## Trimmed mean difference:  0.7116 
    ## 95 percent confidence interval:
    ## 0.5626     0.8605 
    ## 
    ## 
    ## $ATBR11F
    ## Call:
    ## WRS2::yuenbt(formula = x ~ mydata$ATBG05AA)
    ## 
    ## Test statistic: 15.0219 (df = NA), p-value = 0
    ## 
    ## Trimmed mean difference:  1.27937 
    ## 95 percent confidence interval:
    ## 1.1095     1.4492 
    ## 
    ## 
    ## $ATBR11C
    ## Call:
    ## WRS2::yuenbt(formula = x ~ mydata$ATBG05AA)
    ## 
    ## Test statistic: 5.5155 (df = NA), p-value = 0
    ## 
    ## Trimmed mean difference:  0.46186 
    ## 95 percent confidence interval:
    ## 0.2963     0.6274 
    ## 
    ## 
    ## $ATBR11E
    ## Call:
    ## WRS2::yuenbt(formula = x ~ mydata$ATBG05AA)
    ## 
    ## Test statistic: 4.3679 (df = NA), p-value = 0
    ## 
    ## Trimmed mean difference:  0.55224 
    ## 95 percent confidence interval:
    ## 0.2843     0.8202 
    ## 
    ## 
    ## $ATBR14CA
    ## Call:
    ## WRS2::yuenbt(formula = x ~ mydata$ATBG05AA)
    ## 
    ## Test statistic: -10.3573 (df = NA), p-value = 0
    ## 
    ## Trimmed mean difference:  -1.0452 
    ## 95 percent confidence interval:
    ## -1.2386     -0.8518 
    ## 
    ## 
    ## $ATBR14CC
    ## Call:
    ## WRS2::yuenbt(formula = x ~ mydata$ATBG05AA)
    ## 
    ## Test statistic: 2.279 (df = NA), p-value = 0.09015
    ## 
    ## Trimmed mean difference:  0.45198 
    ## 95 percent confidence interval:
    ## -0.0872     0.9912 
    ## 
    ## 
    ## $ATBR14CD
    ## Call:
    ## WRS2::yuenbt(formula = x ~ mydata$ATBG05AA)
    ## 
    ## Test statistic: -0.8081 (df = NA), p-value = 0.40234
    ## 
    ## Trimmed mean difference:  -0.16949 
    ## 95 percent confidence interval:
    ## -0.627     0.288 
    ## 
    ## 
    ## $ATBR14CE
    ## Call:
    ## WRS2::yuenbt(formula = x ~ mydata$ATBG05AA)
    ## 
    ## Test statistic: 3.377 (df = NA), p-value = 0.03339
    ## 
    ## Trimmed mean difference:  0.71186 
    ## 95 percent confidence interval:
    ## 0.0305     1.3933 
    ## 
    ## 
    ## $ATBR14CF
    ## Call:
    ## WRS2::yuenbt(formula = x ~ mydata$ATBG05AA)
    ## 
    ## Test statistic: 13.0752 (df = NA), p-value = 0
    ## 
    ## Trimmed mean difference:  0.74576 
    ## 95 percent confidence interval:
    ## 0.6353     0.8563 
    ## 
    ## 
    ## $ATBR06
    ## Call:
    ## WRS2::yuenbt(formula = x ~ mydata$ATBG05AA)
    ## 
    ## Test statistic: -4.0581 (df = NA), p-value = 0
    ## 
    ## Trimmed mean difference:  -108.1619 
    ## 95 percent confidence interval:
    ## -157.0929     -59.231 
    ## 
    ## 
    ## $ATBR07
    ## Call:
    ## WRS2::yuenbt(formula = x ~ mydata$ATBG05AA)
    ## 
    ## Test statistic: -1.6648 (df = NA), p-value = 0.11352
    ## 
    ## Trimmed mean difference:  -93.7991 
    ## 95 percent confidence interval:
    ## -211.5192     23.921 
    ## 
    ## 
    ## $ATBR10D
    ## Call:
    ## WRS2::yuenbt(formula = x ~ mydata$ATBG05AA)
    ## 
    ## Test statistic: 7.0668 (df = NA), p-value = 0
    ## 
    ## Trimmed mean difference:  0.63392 
    ## 95 percent confidence interval:
    ## 0.4593     0.8085 
    ## 
    ## 
    ## $ATBR10B
    ## Call:
    ## WRS2::yuenbt(formula = x ~ mydata$ATBG05AA)
    ## 
    ## Test statistic: 2.8441 (df = NA), p-value = 0.00167
    ## 
    ## Trimmed mean difference:  0.24161 
    ## 95 percent confidence interval:
    ## 0.0821     0.4012

``` r
psych::describeBy(mydata, mydata$ATBG05AA) # get descriptive statistics
```

    ## 
    ##  Descriptive statistics by group 
    ## group: 1
    ##           vars   n   mean     sd median trimmed    mad min  max range  skew
    ## ATBG05AD     1 813   1.83   0.37      2    1.92   0.00   1    2     1 -1.79
    ## ATBG07A      2 813   3.29   0.73      3    3.36   1.48   2    4     2 -0.51
    ## ATBG01       3 813   2.77   1.44      3    2.71   1.48   1    5     4  0.13
    ## ATBR11D      4 813   1.13   0.42      1    1.01   0.00   1    3     2  3.25
    ## ATBR12E      5 813   3.53   0.53      4    3.56   0.00   2    4     2 -0.48
    ## ATBR11G      6 813   3.32   0.69      3    3.40   1.48   2    4     2 -0.51
    ## ATBR11F      7 813   3.20   0.89      3    3.30   1.48   1    4     3 -0.75
    ## ATBR11C      8 813   3.77   0.46      4    3.85   0.00   2    4     2 -1.76
    ## ATBR11E      9 813   3.80   0.51      4    3.93   0.00   2    4     2 -2.49
    ## ATBR14CA    10 588   2.49   0.96      3    2.49   0.00   1    4     3 -0.38
    ## ATBR14CC    11 588   2.22   0.80      2    2.22   1.48   1    4     3  0.09
    ## ATBR14CD    12 588   2.49   0.80      2    2.48   1.48   1    4     3  0.06
    ## ATBR14CE    13 588   2.38   0.67      2    2.32   0.00   1    4     3  0.74
    ## ATBR14CF    14 588   2.68   1.06      3    2.72   1.48   1    4     3 -0.19
    ## ATBR06      15 813 559.91 288.28    600  537.78 222.39  60 1500  1440  0.96
    ## ATBR07      16 813 625.09 348.77    570  580.47 326.17 100 1800  1700  1.25
    ## ATBR10D     17 798   3.14   0.88      3    3.25   1.48   1    4     3 -0.79
    ## ATBR10B     18 813   3.51   0.76      4    3.67   0.00   1    4     3 -1.51
    ## ATBG05AA*   19 813   1.00   0.00      1    1.00   0.00   1    1     0   NaN
    ##           kurtosis    se
    ## ATBG05AD      1.21  0.01
    ## ATBG07A      -0.99  0.03
    ## ATBG01       -1.39  0.05
    ## ATBR11D      10.02  0.01
    ## ATBR12E      -1.06  0.02
    ## ATBR11G      -0.81  0.02
    ## ATBR11F      -0.53  0.03
    ## ATBR11C       2.18  0.02
    ## ATBR11E       5.16  0.02
    ## ATBR14CA     -0.98  0.04
    ## ATBR14CC     -0.61  0.03
    ## ATBR14CD     -0.46  0.03
    ## ATBR14CE      0.27  0.03
    ## ATBR14CF     -1.20  0.04
    ## ATBR06        1.79 10.11
    ## ATBR07        1.74 12.23
    ## ATBR10D      -0.15  0.03
    ## ATBR10B       1.68  0.03
    ## ATBG05AA*      NaN  0.00
    ## ------------------------------------------------------------ 
    ## group: 2
    ##           vars   n   mean     sd median trimmed    mad min  max range  skew
    ## ATBG05AD     1 109   1.00   0.00      1    1.00   0.00   1    1     0   NaN
    ## ATBG07A      2 109   3.40   0.49      3    3.38   0.00   3    4     1  0.39
    ## ATBG01       3 109   2.69   1.58      2    2.62   1.48   1    5     4  0.31
    ## ATBR11D      4 109   1.40   0.49      1    1.38   0.00   1    2     1  0.39
    ## ATBR12E      5 109   2.71   0.66      3    2.64   1.48   2    4     2  0.38
    ## ATBR11G      6 109   2.73   0.65      3    2.67   0.00   2    4     2  0.31
    ## ATBR11F      7 109   2.23   0.83      2    2.17   0.00   1    4     3  0.69
    ## ATBR11C      8 109   3.36   0.73      4    3.44   0.00   2    4     2 -0.65
    ## ATBR11E      9 109   3.28   0.79      3    3.34   1.48   2    4     2 -0.52
    ## ATBR14CA    10  97   3.61   0.49      4    3.63   0.00   3    4     1 -0.44
    ## ATBR14CC    11  97   2.09   1.16      2    2.00   1.48   1    4     3  0.74
    ## ATBR14CD    12  97   2.59   1.22      2    2.61   1.48   1    4     3  0.10
    ## ATBR14CE    13  97   1.92   1.23      1    1.78   0.00   1    4     3  0.92
    ## ATBR14CF    14  97   1.99   0.59      2    1.99   0.00   1    3     2  0.00
    ## ATBR06      15  97 660.72 255.72    750  655.19 444.78 300 1070   770  0.14
    ## ATBR07      16 109 616.97 359.15    900  635.39  74.13 120  950   830 -0.34
    ## ATBR10D     17 109   2.73   0.65      3    2.67   0.00   2    4     2  0.31
    ## ATBR10B     18 109   3.50   0.50      3    3.49   0.00   3    4     1  0.02
    ## ATBG05AA*   19 109   1.00   0.00      1    1.00   0.00   1    1     0   NaN
    ##           kurtosis    se
    ## ATBG05AD       NaN  0.00
    ## ATBG07A      -1.87  0.05
    ## ATBG01       -1.50  0.15
    ## ATBR11D      -1.87  0.05
    ## ATBR12E      -0.79  0.06
    ## ATBR11G      -0.76  0.06
    ## ATBR11F       0.03  0.08
    ## ATBR11C      -0.88  0.07
    ## ATBR11E      -1.24  0.08
    ## ATBR14CA     -1.83  0.05
    ## ATBR14CC     -0.93  0.12
    ## ATBR14CD     -1.65  0.12
    ## ATBR14CE     -0.88  0.12
    ## ATBR14CF     -0.12  0.06
    ## ATBR06       -1.08 25.96
    ## ATBR07       -1.74 34.40
    ## ATBR10D      -0.76  0.06
    ## ATBR10B      -2.02  0.05
    ## ATBG05AA*      NaN  0.00

``` r
lapply(mydata[-19], function(x) WRS2::akp.effect(x ~ mydata$ATBG05AA))
```

    ## $ATBG05AD
    ## $AKPeffect
    ## [1] Inf
    ## 
    ## $AKPci
    ## [1] Inf Inf
    ## 
    ## $alpha
    ## [1] 0.05
    ## 
    ## $call
    ## WRS2::akp.effect(formula = x ~ mydata$ATBG05AA)
    ## 
    ## attr(,"class")
    ## [1] "AKP"
    ## 
    ## $ATBG07A
    ## $AKPeffect
    ## [1] 0.1058695
    ## 
    ## $AKPci
    ## [1] -0.1296210  0.3418961
    ## 
    ## $alpha
    ## [1] 0.05
    ## 
    ## $call
    ## WRS2::akp.effect(formula = x ~ mydata$ATBG05AA)
    ## 
    ## attr(,"class")
    ## [1] "AKP"
    ## 
    ## $ATBG01
    ## $AKPeffect
    ## [1] 0.1071094
    ## 
    ## $AKPci
    ## [1] -0.1551754  0.3881055
    ## 
    ## $alpha
    ## [1] 0.05
    ## 
    ## $call
    ## WRS2::akp.effect(formula = x ~ mydata$ATBG05AA)
    ## 
    ## attr(,"class")
    ## [1] "AKP"
    ## 
    ## $ATBR11D
    ## $AKPeffect
    ## [1] -1.304883
    ## 
    ## $AKPci
    ## [1] -1.8372252 -0.8346508
    ## 
    ## $alpha
    ## [1] 0.05
    ## 
    ## $call
    ## WRS2::akp.effect(formula = x ~ mydata$ATBG05AA)
    ## 
    ## attr(,"class")
    ## [1] "AKP"
    ## 
    ## $ATBR12E
    ## $AKPeffect
    ## [1] 1.198505
    ## 
    ## $AKPci
    ## [1] 0.9600768 1.3897862
    ## 
    ## $alpha
    ## [1] 0.05
    ## 
    ## $call
    ## WRS2::akp.effect(formula = x ~ mydata$ATBG05AA)
    ## 
    ## attr(,"class")
    ## [1] "AKP"
    ## 
    ## $ATBR11G
    ## $AKPeffect
    ## [1] 0.9204186
    ## 
    ## $AKPci
    ## [1] 0.7399022 1.1144335
    ## 
    ## $alpha
    ## [1] 0.05
    ## 
    ## $call
    ## WRS2::akp.effect(formula = x ~ mydata$ATBG05AA)
    ## 
    ## attr(,"class")
    ## [1] "AKP"
    ## 
    ## $ATBR11F
    ## $AKPeffect
    ## [1] 1.060734
    ## 
    ## $AKPci
    ## [1] 0.9162017 1.2339260
    ## 
    ## $alpha
    ## [1] 0.05
    ## 
    ## $call
    ## WRS2::akp.effect(formula = x ~ mydata$ATBG05AA)
    ## 
    ## attr(,"class")
    ## [1] "AKP"
    ## 
    ## $ATBR11C
    ## $AKPeffect
    ## [1] 0.6985911
    ## 
    ## $AKPci
    ## [1] 0.5079689 2.0027380
    ## 
    ## $alpha
    ## [1] 0.05
    ## 
    ## $call
    ## WRS2::akp.effect(formula = x ~ mydata$ATBG05AA)
    ## 
    ## attr(,"class")
    ## [1] "AKP"
    ## 
    ## $ATBR11E
    ## $AKPeffect
    ## [1] 1.306419
    ## 
    ## $AKPci
    ## [1] 1.097301 2.242855
    ## 
    ## $alpha
    ## [1] 0.05
    ## 
    ## $call
    ## WRS2::akp.effect(formula = x ~ mydata$ATBG05AA)
    ## 
    ## attr(,"class")
    ## [1] "AKP"
    ## 
    ## $ATBR14CA
    ## $AKPeffect
    ## [1] -0.8438628
    ## 
    ## $AKPci
    ## [1] -1.1472595 -0.6985947
    ## 
    ## $alpha
    ## [1] 0.05
    ## 
    ## $call
    ## WRS2::akp.effect(formula = x ~ mydata$ATBG05AA)
    ## 
    ## attr(,"class")
    ## [1] "AKP"
    ## 
    ## $ATBR14CC
    ## $AKPeffect
    ## [1] 0.4657272
    ## 
    ## $AKPci
    ## [1] 0.01091848 0.95899548
    ## 
    ## $alpha
    ## [1] 0.05
    ## 
    ## $call
    ## WRS2::akp.effect(formula = x ~ mydata$ATBG05AA)
    ## 
    ## attr(,"class")
    ## [1] "AKP"
    ## 
    ## $ATBR14CD
    ## $AKPeffect
    ## [1] -0.1668702
    ## 
    ## $AKPci
    ## [1] -0.5279327  0.2571725
    ## 
    ## $alpha
    ## [1] 0.05
    ## 
    ## $call
    ## WRS2::akp.effect(formula = x ~ mydata$ATBG05AA)
    ## 
    ## attr(,"class")
    ## [1] "AKP"
    ## 
    ## $ATBR14CE
    ## $AKPeffect
    ## [1] 0.7143912
    ## 
    ## $AKPci
    ## [1] 0.2820885 1.3628199
    ## 
    ## $alpha
    ## [1] 0.05
    ## 
    ## $call
    ## WRS2::akp.effect(formula = x ~ mydata$ATBG05AA)
    ## 
    ## attr(,"class")
    ## [1] "AKP"
    ## 
    ## $ATBR14CF
    ## $AKPeffect
    ## [1] 0.6222917
    ## 
    ## $AKPci
    ## [1] 0.5013114 0.7207238
    ## 
    ## $alpha
    ## [1] 0.05
    ## 
    ## $call
    ## WRS2::akp.effect(formula = x ~ mydata$ATBG05AA)
    ## 
    ## attr(,"class")
    ## [1] "AKP"
    ## 
    ## $ATBR06
    ## $AKPeffect
    ## [1] -0.4446018
    ## 
    ## $AKPci
    ## [1] -0.7095537 -0.2230399
    ## 
    ## $alpha
    ## [1] 0.05
    ## 
    ## $call
    ## WRS2::akp.effect(formula = x ~ mydata$ATBG05AA)
    ## 
    ## attr(,"class")
    ## [1] "AKP"
    ## 
    ## $ATBR07
    ## $AKPeffect
    ## [1] -0.252337
    ## 
    ## $AKPci
    ## [1] -0.54075617  0.05543956
    ## 
    ## $alpha
    ## [1] 0.05
    ## 
    ## $call
    ## WRS2::akp.effect(formula = x ~ mydata$ATBG05AA)
    ## 
    ## attr(,"class")
    ## [1] "AKP"
    ## 
    ## $ATBR10D
    ## $AKPeffect
    ## [1] 0.5552583
    ## 
    ## $AKPci
    ## [1] 0.3719061 0.9921191
    ## 
    ## $alpha
    ## [1] 0.05
    ## 
    ## $call
    ## WRS2::akp.effect(formula = x ~ mydata$ATBG05AA)
    ## 
    ## attr(,"class")
    ## [1] "AKP"
    ## 
    ## $ATBR10B
    ## $AKPeffect
    ## [1] 0.3213116
    ## 
    ## $AKPci
    ## [1] 0.1399348 0.5038774
    ## 
    ## $alpha
    ## [1] 0.05
    ## 
    ## $call
    ## WRS2::akp.effect(formula = x ~ mydata$ATBG05AA)
    ## 
    ## attr(,"class")
    ## [1] "AKP"
