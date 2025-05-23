DS 202 Final Project
================

<!-- README.md is generated from README.Rmd. Please edit the README.Rmd file -->

This repository serves as a starter repo for your final project, and
this Rmd is supposed to serve as a starter file for your project report.

## Part I: Repo Structure

The structure sketched out below is an idea of what your repository
might look like. You can use it as a starting base and change according
to your needs. But think about the changes that you make!

    -- code
    |   |   -- any R scripts you need but don't want to include directly in the write-up
    -- data
    |   |   -- csv files (cleaned data)
    -- data-raw
    |   |   -- raw data files 
    |   |   -- data description files, origin
    |   |   -- Codebook
    -- final-project.Rmd
    -- images  # only images that are not created by the Rmd
    -- LICENSE
    -- README.md
    -- README.Rmd
    -- README_files # folder with files created during the knitting process

## Part II: Project report

# Title of your project

Authors: Cole Flickinger, Isaac Irving, Cameron Kraklio

## Abstract (TL;DR)

An abstract is a quick summary of your work. Ideally it should motivate
someone to read the rest of the paper. Include one sentence each on

- what is the project about?
- what is the motivation for doing it?
- what data is your work based on? and where does it come from? = what
  are your main findings? (one sentence each)

# Intro/Background/Motivation

What is the topic of your project, why is it relevant? Our project looks
at a number of health categories and how they relate to sleep and
lifestyle choices. It is relevant since sleep and health statistics are
categories that everyone is going to be concernerd about.

At the end of the Intro, write a sentence describing what each of the
(result) sections is about, e.g. in section [Results 1](#results-1) we
show the relationship between XXX and YYY, section [Results
2](#results-2) also considers the effect of variable ZZZ. … Finally we
conclude with a quick summary of our findings and potential follow-up
work in section [Conclusions](#conclusions).

Somewhere at the beginning of your project, include a code chunk that
includes all of the R packages you are using throughout. In this
document, the setup code chunk is called `setup` (see line 8) Also make
sure to set defaults for the code chunks - like should they be visible?
(probably not: echo=FALSE). Do you want to automatically include
warnings? (probably yes, for creating the Rmd, to make sure that all
warnings are accounted for)

# Quick Data Summary

What are the variables that you will be using in the main part of the
report? What are their ranges? You could include a table with variable
names, a short explanation, and (very broad) summary statistics.

The variables we will be focusing on are: Occupation: what the person
does for work Stress level - ranged from 3 to 8 Sleep duration - ranges
from 5.8 to 8.5 hours Quality of sleep - ranges from 4 to 9 BMI
category - what category the person fits into on the BMI scale

# Results

Each line of exploration is supposed to be featured in one of the
Results sections. Make sure to change to more interesting section
headers!

## Results 1

<p>
<small><strong><a name='fig:scatterplot'>scatterplot</a></strong>: This
is the figure caption. Make sure to use the description we practised in
the homework: first sentence describes structure of the plot, second
sentence describes main finding, third sentence describes
outliers/follow-up.</small>
</p>

    ## spc_tbl_ [374 × 13] (S3: spec_tbl_df/tbl_df/tbl/data.frame)
    ##  $ Person ID              : num [1:374] 1 2 3 4 5 6 7 8 9 10 ...
    ##  $ Gender                 : chr [1:374] "Male" "Male" "Male" "Male" ...
    ##  $ Age                    : num [1:374] 27 28 28 28 28 28 29 29 29 29 ...
    ##  $ Occupation             : chr [1:374] "Software Engineer" "Doctor" "Doctor" "Sales Representative" ...
    ##  $ Sleep Duration         : num [1:374] 6.1 6.2 6.2 5.9 5.9 5.9 6.3 7.8 7.8 7.8 ...
    ##  $ Quality of Sleep       : num [1:374] 6 6 6 4 4 4 6 7 7 7 ...
    ##  $ Physical Activity Level: num [1:374] 42 60 60 30 30 30 40 75 75 75 ...
    ##  $ Stress Level           : num [1:374] 6 8 8 8 8 8 7 6 6 6 ...
    ##  $ BMI Category           : chr [1:374] "Overweight" "Normal" "Normal" "Obese" ...
    ##  $ Blood Pressure         : chr [1:374] "126/83" "125/80" "125/80" "140/90" ...
    ##  $ Heart Rate             : num [1:374] 77 75 75 85 85 85 82 70 70 70 ...
    ##  $ Daily Steps            : num [1:374] 4200 10000 10000 3000 3000 3000 3500 8000 8000 8000 ...
    ##  $ Sleep Disorder         : chr [1:374] "None" "None" "None" "Sleep Apnea" ...
    ##  - attr(*, "spec")=
    ##   .. cols(
    ##   ..   `Person ID` = col_double(),
    ##   ..   Gender = col_character(),
    ##   ..   Age = col_double(),
    ##   ..   Occupation = col_character(),
    ##   ..   `Sleep Duration` = col_double(),
    ##   ..   `Quality of Sleep` = col_double(),
    ##   ..   `Physical Activity Level` = col_double(),
    ##   ..   `Stress Level` = col_double(),
    ##   ..   `BMI Category` = col_character(),
    ##   ..   `Blood Pressure` = col_character(),
    ##   ..   `Heart Rate` = col_double(),
    ##   ..   `Daily Steps` = col_double(),
    ##   ..   `Sleep Disorder` = col_character()
    ##   .. )
    ##  - attr(*, "problems")=<externalptr>

![](README_files/figure-gfm/unnamed-chunk-1-1.png)<!-- -->

    ## `geom_smooth()` using formula = 'y ~ x'

![](README_files/figure-gfm/unnamed-chunk-1-2.png)<!-- -->![](README_files/figure-gfm/unnamed-chunk-1-3.png)<!-- -->![](README_files/figure-gfm/unnamed-chunk-1-4.png)<!-- -->![](README_files/figure-gfm/unnamed-chunk-1-5.png)<!-- -->

Additionally, you can also refer to different sections in your writeup
by using anchors (links) to section headers. Here, we are referring to
subsection [Results 3](#results-3). The code for that is `[Results 3]`.

## Results 2

Cole Flickinger: Attempt to look at health and sleep based on occupation
alone.

    ## Initial dataset dimensions: 374 13

    ## Column names: Person ID Gender Age Occupation Sleep Duration Quality of Sleep Physical Activity Level Stress Level BMI Category Blood Pressure Heart Rate Daily Steps Sleep Disorder

    ## spc_tbl_ [374 × 13] (S3: spec_tbl_df/tbl_df/tbl/data.frame)
    ##  $ Person ID              : num [1:374] 1 2 3 4 5 6 7 8 9 10 ...
    ##  $ Gender                 : chr [1:374] "Male" "Male" "Male" "Male" ...
    ##  $ Age                    : num [1:374] 27 28 28 28 28 28 29 29 29 29 ...
    ##  $ Occupation             : chr [1:374] "Software Engineer" "Doctor" "Doctor" "Sales Representative" ...
    ##  $ Sleep Duration         : num [1:374] 6.1 6.2 6.2 5.9 5.9 5.9 6.3 7.8 7.8 7.8 ...
    ##  $ Quality of Sleep       : num [1:374] 6 6 6 4 4 4 6 7 7 7 ...
    ##  $ Physical Activity Level: num [1:374] 42 60 60 30 30 30 40 75 75 75 ...
    ##  $ Stress Level           : num [1:374] 6 8 8 8 8 8 7 6 6 6 ...
    ##  $ BMI Category           : chr [1:374] "Overweight" "Normal" "Normal" "Obese" ...
    ##  $ Blood Pressure         : chr [1:374] "126/83" "125/80" "125/80" "140/90" ...
    ##  $ Heart Rate             : num [1:374] 77 75 75 85 85 85 82 70 70 70 ...
    ##  $ Daily Steps            : num [1:374] 4200 10000 10000 3000 3000 3000 3500 8000 8000 8000 ...
    ##  $ Sleep Disorder         : chr [1:374] "None" "None" "None" "Sleep Apnea" ...
    ##  - attr(*, "spec")=
    ##   .. cols(
    ##   ..   `Person ID` = col_double(),
    ##   ..   Gender = col_character(),
    ##   ..   Age = col_double(),
    ##   ..   Occupation = col_character(),
    ##   ..   `Sleep Duration` = col_double(),
    ##   ..   `Quality of Sleep` = col_double(),
    ##   ..   `Physical Activity Level` = col_double(),
    ##   ..   `Stress Level` = col_double(),
    ##   ..   `BMI Category` = col_character(),
    ##   ..   `Blood Pressure` = col_character(),
    ##   ..   `Heart Rate` = col_double(),
    ##   ..   `Daily Steps` = col_double(),
    ##   ..   `Sleep Disorder` = col_character()
    ##   .. )
    ##  - attr(*, "problems")=<externalptr>

    ##    Person ID         Gender               Age         Occupation       
    ##  Min.   :  1.00   Length:374         Min.   :27.00   Length:374        
    ##  1st Qu.: 94.25   Class :character   1st Qu.:35.25   Class :character  
    ##  Median :187.50   Mode  :character   Median :43.00   Mode  :character  
    ##  Mean   :187.50                      Mean   :42.18                     
    ##  3rd Qu.:280.75                      3rd Qu.:50.00                     
    ##  Max.   :374.00                      Max.   :59.00                     
    ##  Sleep Duration  Quality of Sleep Physical Activity Level  Stress Level  
    ##  Min.   :5.800   Min.   :4.000    Min.   :30.00           Min.   :3.000  
    ##  1st Qu.:6.400   1st Qu.:6.000    1st Qu.:45.00           1st Qu.:4.000  
    ##  Median :7.200   Median :7.000    Median :60.00           Median :5.000  
    ##  Mean   :7.132   Mean   :7.313    Mean   :59.17           Mean   :5.385  
    ##  3rd Qu.:7.800   3rd Qu.:8.000    3rd Qu.:75.00           3rd Qu.:7.000  
    ##  Max.   :8.500   Max.   :9.000    Max.   :90.00           Max.   :8.000  
    ##  BMI Category       Blood Pressure       Heart Rate     Daily Steps   
    ##  Length:374         Length:374         Min.   :65.00   Min.   : 3000  
    ##  Class :character   Class :character   1st Qu.:68.00   1st Qu.: 5600  
    ##  Mode  :character   Mode  :character   Median :70.00   Median : 7000  
    ##                                        Mean   :70.17   Mean   : 6817  
    ##                                        3rd Qu.:72.00   3rd Qu.: 8000  
    ##                                        Max.   :86.00   Max.   :10000  
    ##  Sleep Disorder    
    ##  Length:374        
    ##  Class :character  
    ##  Mode  :character  
    ##                    
    ##                    
    ## 

    ## Number of duplicate rows: 0

    ## After removing duplicates: 374 13

    ## Missing values per column:

    ##               Person ID                  Gender                     Age 
    ##                       0                       0                       0 
    ##              Occupation          Sleep Duration        Quality of Sleep 
    ##                       0                       0                       0 
    ## Physical Activity Level            Stress Level            BMI Category 
    ##                       0                       0                       0 
    ##          Blood Pressure              Heart Rate             Daily Steps 
    ##                       0                       0                       0 
    ##          Sleep Disorder 
    ##                       0

    ## Warning: Unknown or uninitialised column: `BMI.Category`.

    ## NULL

    ## 
    ## Final cleaned dataset dimensions: 374 14

    ## # A tibble: 6 × 14
    ##   `Person ID` Gender   Age Occupation        `Sleep Duration` `Quality of Sleep`
    ##         <dbl> <chr>  <dbl> <chr>                        <dbl>              <dbl>
    ## 1           1 Male      27 Software Engineer              6.1                  6
    ## 2           2 Male      28 Doctor                         6.2                  6
    ## 3           3 Male      28 Doctor                         6.2                  6
    ## 4           4 Male      28 Sales Representa…              5.9                  4
    ## 5           5 Male      28 Sales Representa…              5.9                  4
    ## 6           6 Male      28 Software Engineer              5.9                  4
    ## # ℹ 8 more variables: `Physical Activity Level` <dbl>, `Stress Level` <dbl>,
    ## #   `BMI Category` <chr>, Systolic <int>, Diastolic <int>, `Heart Rate` <dbl>,
    ## #   `Daily Steps` <dbl>, `Sleep Disorder` <chr>

    ## # A tibble: 6 × 13
    ##   `Person ID` Gender   Age Occupation        `Sleep Duration` `Quality of Sleep`
    ##         <dbl> <chr>  <dbl> <chr>                        <dbl>              <dbl>
    ## 1           1 Male      27 Software Engineer              6.1                  6
    ## 2           2 Male      28 Doctor                         6.2                  6
    ## 3           3 Male      28 Doctor                         6.2                  6
    ## 4           4 Male      28 Sales Representa…              5.9                  4
    ## 5           5 Male      28 Sales Representa…              5.9                  4
    ## 6           6 Male      28 Software Engineer              5.9                  4
    ## # ℹ 7 more variables: `Physical Activity Level` <dbl>, `Stress Level` <dbl>,
    ## #   `BMI Category` <chr>, `Blood Pressure` <chr>, `Heart Rate` <dbl>,
    ## #   `Daily Steps` <dbl>, `Sleep Disorder` <chr>

    ##    Person ID         Gender               Age         Occupation       
    ##  Min.   :  1.00   Length:374         Min.   :27.00   Length:374        
    ##  1st Qu.: 94.25   Class :character   1st Qu.:35.25   Class :character  
    ##  Median :187.50   Mode  :character   Median :43.00   Mode  :character  
    ##  Mean   :187.50                      Mean   :42.18                     
    ##  3rd Qu.:280.75                      3rd Qu.:50.00                     
    ##  Max.   :374.00                      Max.   :59.00                     
    ##  Sleep Duration  Quality of Sleep Physical Activity Level  Stress Level  
    ##  Min.   :5.800   Min.   :4.000    Min.   :30.00           Min.   :3.000  
    ##  1st Qu.:6.400   1st Qu.:6.000    1st Qu.:45.00           1st Qu.:4.000  
    ##  Median :7.200   Median :7.000    Median :60.00           Median :5.000  
    ##  Mean   :7.132   Mean   :7.313    Mean   :59.17           Mean   :5.385  
    ##  3rd Qu.:7.800   3rd Qu.:8.000    3rd Qu.:75.00           3rd Qu.:7.000  
    ##  Max.   :8.500   Max.   :9.000    Max.   :90.00           Max.   :8.000  
    ##  BMI Category       Blood Pressure       Heart Rate     Daily Steps   
    ##  Length:374         Length:374         Min.   :65.00   Min.   : 3000  
    ##  Class :character   Class :character   1st Qu.:68.00   1st Qu.: 5600  
    ##  Mode  :character   Mode  :character   Median :70.00   Median : 7000  
    ##                                        Mean   :70.17   Mean   : 6817  
    ##                                        3rd Qu.:72.00   3rd Qu.: 8000  
    ##                                        Max.   :86.00   Max.   :10000  
    ##  Sleep Disorder    
    ##  Length:374        
    ##  Class :character  
    ##  Mode  :character  
    ##                    
    ##                    
    ## 

    ##    Length     Class      Mode 
    ##       374 character character

    ##  [1] "Software Engineer"    "Doctor"               "Sales Representative"
    ##  [4] "Teacher"              "Nurse"                "Engineer"            
    ##  [7] "Accountant"           "Scientist"            "Lawyer"              
    ## [10] "Salesperson"          "Manager"

    ## `geom_line()`: Each group consists of only one observation.
    ## ℹ Do you need to adjust the group aesthetic?

![](README_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

![](README_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->![](README_files/figure-gfm/unnamed-chunk-5-2.png)<!-- -->

    ## `geom_smooth()` using formula = 'y ~ x'

![](README_files/figure-gfm/unnamed-chunk-5-3.png)<!-- --> Notable:
there is only 1 manager, 26 salespersons, and 4 sales representatives.

## Results 3

    ##    Length     Class      Mode 
    ##       374 character character

![](README_files/figure-gfm/unnamed-chunk-6-1.png)<!-- -->![](README_files/figure-gfm/unnamed-chunk-6-2.png)<!-- -->![](README_files/figure-gfm/unnamed-chunk-6-3.png)<!-- -->![](README_files/figure-gfm/unnamed-chunk-6-4.png)<!-- -->![](README_files/figure-gfm/unnamed-chunk-6-5.png)<!-- -->

    ## [1] 7.22973

    ## [1] 7.036508

    ## [1] 7.664865

    ## [1] 6.968254

    ## [1] 4.675676

    ## [1] 6.079365

…

# Conclusions

Give a quick summary of your work. Here is the place to be a bit
critical and discuss potential limitations. Add a sentence on what else
you would have liked to include in your data exploration if you had more
time or more members in your team.

## Data source

Where does the data come from, who owns the data? Where are all the
scripts that you need to clean the data?

## References

List all resources you used.
