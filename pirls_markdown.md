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

to run tests. Shapiro test in R to run for normality, Wilcoxon test to
run for non-parametric version of t-tests, and the t-test

``` r
# ATBR12E ATBR11D, ATBR12E,ATBR11G, ATBR11F,ATBR11C,ATBR11C, ATBR11E, ATBR14CA, ATBR14CC,  ATBR14CD, ATBR14CE, ATBR14CF, ATBR06, ATBR07, ATBR10D


mydata <- readRDS("Path\to\data\here.rds") 

psych::describeBy(mydata, mydata$ATBG05AA) # get descriptive statistics

shapiro.test(mydata$ATBR11D) # test for normality 

wilcox.test(ATBR07 ~ ATBG05AA, data = mydata) # nonparametric version of t-tests
```

## Get medians

with a homemade function

``` r
# ATBR10D, ATBR12E ATBR11D, ATBR11G, ATBR11F,ATBR11C, ATBR11E, ATBR14CA, ATBR14CC,  ATBR14CD, ATBR14CE, ATBR14CF, ATBR06, ATBR07, 

sv <- function(a){
library(magrittr)
library(dplyr)
mo <- mydata%>%
  dplyr::group_by(ATBG05AA) %>%
  dplyr::filter(ATBG05AA == 1) %>%
  dplyr::summarise(median({{a}}))

me <- mydata%>%
  dplyr::group_by(ATBG05AA) %>%
  dplyr::filter(ATBG05AA == 2) %>%
  dplyr::summarise(median({{a}}))

return(list(mo,me))

}
```

## Calculate effect sizes

``` r
# Effect sizes

# ATBR10D, ATBR12E ATBR11D, ATBR11G, ATBR11F,ATBR11C, ATBR11E, ATBR14CA, ATBR14CC,  ATBR14CD, ATBR14CE, ATBR14CF, ATBR06, ATBR07


effectsize::rank_biserial(ATBR10D ~ ATBG05AA, data = mydata) #effect size for mann whitney U
```
