Homework \#1 – Pet Names Dataset
================
Wejdan Awad
2021-02-14

\*\*Student ID:2201002744

**Deadline:** 23:59 on Saturday, 13 February 2021

**Total Points:** 30

## Loading Packages

``` r
library(tidyverse)
library(openintro)
library(ggrepel)
```

\#\#Exercises

\`1

(4 points)

Write your narrative here

52519 .

\`2.

(4 points)

Write your narrative below

7 .

\`3. Copy the code provided in the homework documentation and paste it
here.

(4 points)

``` r
seattlepets %>%
count(animal_name, sort = TRUE)
```

    ## # A tibble: 13,930 x 2
    ##    animal_name     n
    ##    <chr>       <int>
    ##  1 <NA>          483
    ##  2 Lucy          439
    ##  3 Charlie       387
    ##  4 Luna          355
    ##  5 Bella         331
    ##  6 Max           270
    ##  7 Daisy         261
    ##  8 Molly         240
    ##  9 Jack          232
    ## 10 Lily          232
    ## # … with 13,920 more rows

Write your narrative here NA 483 Lucy 439 Charlie 387 Luna 355

\`4.

(10 points)

``` r
 seattlepets %>%
     group_by(species) %>%
     count(animal_name, sort = TRUE) %>%
     slice_max(n, n = 5)%>%arrange(species, n) 
```

    ## # A tibble: 53 x 3
    ## # Groups:   species [4]
    ##    species animal_name     n
    ##    <chr>   <chr>       <int>
    ##  1 Cat     Max            83
    ##  2 Cat     Lily           86
    ##  3 Cat     Lucy          102
    ##  4 Cat     Luna          111
    ##  5 Cat     <NA>          406
    ##  6 Dog     Daisy         221
    ##  7 Dog     Luna          244
    ##  8 Dog     Bella         249
    ##  9 Dog     Charlie       306
    ## 10 Dog     Lucy          337
    ## # … with 43 more rows

\`5. What names are more common for cats than dogs? The ones above the
line or the ones below the line?

Answer here

Oliver and lily .

(4 points)

\`6. Is the relationship between the two variables (proportion of cats
with a given name and proportion of dogs with a given name) positive or
negative? What does this mean in context of the data?

Answer here

Positive , if dogs names increase the cats names increase also and also
if dogs names decrease the cats name decrease also in the same name of
them

(4 points)
