Analysis on Physical Characteristics of Penguins in the Palmer
Archipelago
================
2025-11-17

# Analysis on Physical Characteristics of Penguins in the Palmer Archipelago

#### Jyotika Sharma, Selena Cooper, Grace Kolker

## Introduction

The goal of this project is to explore the Palmer Penguins dataset to
better understand the differences in physical traits between penguin
species. This dataset includes measurements collected on three penguins
species (Adelie, Gentoo, and Chinstrap) living on multiple islands in
the Palmer Archipelago in Antarctica. By analyzing these physical
measurements, we hope to identify patterns, species differneces, and
relationships between body size variables. Understanding these traits
can help explain how environmental conditions and biological factors may
influence species variation and survival.

In pursuit of the stated goal, we will explore the following questions:

1.  How do body size measurements vary between penguin species? Are
    certain species consistently larger in one or more measurements such
    as body mass or flipper length? - Selena

2.  How do bill length and bill depth interact to help differentiate
    penguin species? Can these measurements be used to identify species
    differences effectively? - Selena

3.  Is there a relationship between flipper length and body mass across
    species? Do larger flippers indicate heavier penguins, and does this
    relationship differ by species? - Jyotika

4.  How does sex influence body size? Are male penguins consistently
    larger than female penguins across all species, and does this vary
    in strength across difference species? - Jyotika

5.  Does the island a penguins inhabits affect its body measurements?
    Are physical differences across islands still present even after
    accounting for species? - Grace

6.  Which variable (bill length, bill depth, flipper length, or body
    mass) provides the strongest prediction of species classification?
    How do combines variables compare to single-variable predication? -
    Grace

These are the main questions we intend to answer through analysis of the
Palmer Penguins dataset. With the findings, we will be able to draw
meaningful conclusions about physical trait differences and the
ecological factors that influence species variation in Antarctic
penguins.

## Data

### Structure

The link to the dataset is

``` r
library(palmerpenguins)
```

    ## 
    ## Attaching package: 'palmerpenguins'

    ## The following objects are masked from 'package:datasets':
    ## 
    ##     penguins, penguins_raw

``` r
data(package = "palmerpenguins")
```

### Cleaning

### Variables

``` r
dim(penguins)
```

    ## [1] 344   8

``` r
str(penguins)
```

    ## tibble [344 × 8] (S3: tbl_df/tbl/data.frame)
    ##  $ species          : Factor w/ 3 levels "Adelie","Chinstrap",..: 1 1 1 1 1 1 1 1 1 1 ...
    ##  $ island           : Factor w/ 3 levels "Biscoe","Dream",..: 3 3 3 3 3 3 3 3 3 3 ...
    ##  $ bill_length_mm   : num [1:344] 39.1 39.5 40.3 NA 36.7 39.3 38.9 39.2 34.1 42 ...
    ##  $ bill_depth_mm    : num [1:344] 18.7 17.4 18 NA 19.3 20.6 17.8 19.6 18.1 20.2 ...
    ##  $ flipper_length_mm: int [1:344] 181 186 195 NA 193 190 181 195 193 190 ...
    ##  $ body_mass_g      : int [1:344] 3750 3800 3250 NA 3450 3650 3625 4675 3475 4250 ...
    ##  $ sex              : Factor w/ 2 levels "female","male": 2 1 1 NA 1 2 1 2 NA NA ...
    ##  $ year             : int [1:344] 2007 2007 2007 2007 2007 2007 2007 2007 2007 2007 ...

There are 344 penguins in the dataset. There are 3 different species of
penguins collected from 3 different islands in the Parmer Archipelago.

- species: the biological species of each penguin (Adelie, Gentoo, and
  Chinstrap)
- island: The island within the Palmer Archipelago where the penguin was
  observed (Biscoe, Dream, and Torgersen)
- bill_length_mm: The length of the penguin’s bill (from tip to base)
  measured in milimeters
- bill_depth_mm: Thickness (depth) fo the penguin’s bill measured at the
  base in milimeters
- flipper_length_mm: Length of the penguin’s flipper from shoulder to
  tip measured in milimeters
- body_mass_g: Body weight of the penguin measured in grams
- sex: Sex of the penguin (male or female)
- year: The year the penguin was sampled during the Palmer Station field
  seasons (2007, 2008, 2009)

## Results
