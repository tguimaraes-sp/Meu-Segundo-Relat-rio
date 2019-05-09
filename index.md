Meu Segundo Relatório
================

``` r
library(dplyr)
```

``` r
library(ggplot2)
```

``` r
library(gapminder)
```

``` r
head(gapminder)
```

    ## # A tibble: 6 x 6
    ##   country     continent  year lifeExp      pop gdpPercap
    ##   <fct>       <fct>     <int>   <dbl>    <int>     <dbl>
    ## 1 Afghanistan Asia       1952    28.8  8425333      779.
    ## 2 Afghanistan Asia       1957    30.3  9240934      821.
    ## 3 Afghanistan Asia       1962    32.0 10267083      853.
    ## 4 Afghanistan Asia       1967    34.0 11537966      836.
    ## 5 Afghanistan Asia       1972    36.1 13079460      740.
    ## 6 Afghanistan Asia       1977    38.4 14880372      786.

``` r
nrow (gapminder)
```

    ## [1] 1704

``` r
gapminder %>%
  select(year) %>%
  unique() %>%
  nrow()
```

    ## [1] 12

``` r
df<-gapminder
```

``` r
gapminder %>%  
  group_by(year)%>% 
  summarise( n=n() )
```

    ## # A tibble: 12 x 2
    ##     year     n
    ##    <int> <int>
    ##  1  1952   142
    ##  2  1957   142
    ##  3  1962   142
    ##  4  1967   142
    ##  5  1972   142
    ##  6  1977   142
    ##  7  1982   142
    ##  8  1987   142
    ##  9  1992   142
    ## 10  1997   142
    ## 11  2002   142
    ## 12  2007   142
