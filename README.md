# nccs-core-harmonization

Crosswalk and scripts to harmonize NCCS Core files over time. 


```r
library( dplyr )

pc.2019 <- "https://nccs-data.urban.org/dl.php?f=core/2019/coreco.core2019pc.csv"
d.2019 <- read.csv( pc.2019 )

pc.2018 <- "https://nccs-data.urban.org/dl.php?f=core/2018/coreco.core2018pc.csv"
d.2018 <- read.csv( pc.2018 )

names( d.2019 )

names( d.2019 ) %>% sort()

# to paste names into excel
writeClipboard( sort( names(d.2018) ) )

# all names in BOTH versions 
intersect( names(d.2019), names(d.2018) ) 

# all names in 2019 version NOT in 2018
setdiff( names(d.2019), names(d.2018) )

# all names in 2018 version NOT in 2019
setdiff( names(d.2018), names(d.2019) )
```
