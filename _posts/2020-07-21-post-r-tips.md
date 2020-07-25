---
title: "R Tips"
last_modified_at: 2020-07-24 T16:20:02-05:00
categories:
  - R
tags:
  - Post Formats
  - readability
  - standard
---

Hide the legend in a bar chart:

```{r}
geom_col(show.legend = FALSE)    

```

Insert new section  

```r 
Ctrl-Shift-R

``` 

Identify na's and incompletes:
```r
    df %>% filter(!complete.cases(.)) %>% View()   This will show all cases with na/empty values   
	filter(age < 10 | age > 80)

```

Write to excel:
```r
    library(writexl)
    write_excel_csv(estate, "~/Desktop/2020-07-20-12-33 estate.csv", na = 'NA', append = FALSE, delim = ',', quote_escape = 'double')  
```

setting the axis and formats:
```r
  scale_y_continuous(labels = dollar_format())+
  scale_x_continuous()+
  expand_limits(y=0)+
```

rename 'cells' within a column by criteria:
```r
    mutate(street_address = fct_recode(street_address, "1040 Delaware Avenue","1040 Delaware Ave"))
```

see the built-in datasets:
```r
    data()
```

for long text in the x-axis labels, just rotate it vertically:
    theme(axis.text.x = element.text(angle=90, hjust=1)


clean the column names:
```r
tips %>%
    map(janitor::clean_names)

get rid of commas in numbers:
x <- c(23,460 , 12,340 , 3,451 , 57,999)
x <- mutate(x=readr::parse_number(x)
# this will give (23460 , 12340 , 3451 , 57999)
```
?
What does 'bind_rows' do?

?
```r
count(address, wt=n, sort = TRUE)
```

To reorder by the sum of a numerical variable:
```r
    mutate(region = fct_reorder(region, n, sum))
```

No more coord_flip()
Horizontal bar plots can be really useful, especially for categorical data whose levels have long names that overlap if placed on the x-axis. Previously, making horizontal bar plots required mapping the variable to be plotted to the x aesthetic and then applying a coord_flip() layer to flip the axes, e.g.
```r
ggplot(penguins, aes(x = species)) +
  geom_bar() +
  coord_flip()
![][penguins-species-bar-coord-flip-1]
geom_bar() now works in both directions, so the categorical variable can be directly mapped to the y aesthetic to achieve the horizontal box plot.

ggplot(penguins, aes(y = species)) +
  geom_bar()
![][penguins-species-bar-coord-flip-1-1]
```

Put the fct_reorder in ggplot:
```r
penguins %>%
  count(species) %>%
  mutate(prop = n / sum(n)) %>%
  ggplot(aes(x = prop, y = fct_reorder(species, prop))) +
  geom_col()
![][penguins-species-props-bar-reorder-1]
```


No more gather / spread
Previously you might have approached this with the gather()/spread() functions. But there is a new pair of much more intuitive functions in town (i.e. in the tidyr package): pivot_wider() for going from longer to wider data and pivot_longer() for going from wider to longer data. The following animated visualisation by Mara Averick does a fantastic job of visually explaining what we mean by pivoting the longer (or wider).
```r
![][tidyr-longer-wider]
```
which columns to pivot: any column that starts with the character string "body_mass",
what the name of the new variable where we put the names of the variables that are being pivoted should go to: names_to = "measurement", and
what the name of the new variable where the values of the the variables that are being pivoted should go to: values_to = "body_mass".
```r
penguins_madeup_long <- penguins_madeup_wide %>%
  pivot_longer(
    cols = starts_with("body_mass"),
    names_to = "measurement",
    names_prefix = "body_mass_",
    values_to = "body_mass"
  )

penguins_madeup_long
```


Using 'summarise across'
```r
penguins_madeup_wide %>%
  summarise(across(
    starts_with("body_mass"),
    list(sample_mean = mean, sample_sd = sd)
  ))
```

Turn blank into na:
```r
  mtcars%>%
    na_if("")
```

Nice shortcut (reassignment pipe):
```r
mtcars <- mtcars%>%
    na_if("")

# Is the same as
   mtcars%<>%
     na_if("")
```
Use skimr: ref youtube watch?v=uG3igAGX7UE
```r
    multiple_choice_responses %>%
    select_if(is.numeric) %>%
    skimr::skim()
```
Find number of distinct values by col:
```r
![][Image]
```

separate a column and rows based on what you choose to separate it by
```r
![][Image-1]
```

order a graph correctly

Add percent scales:
```r
    scale_y_continuous(labels = scales::percent)
```
For knitr output that show up as scientific notation (eg The total number of question attempts was `r sum(expert$attempts)`. 
yields 5.12312414 ^{5}

to correct this, just include the following line of code inside the setoptions-chunk in the beginning of a knitr document:
```r
knitr::opts_chunk$set(echo = TRUE, options(scipen=999))
```
```r
scale_x_continuous(breaks = 1:9) # if there were nine seasons
```

```r
rotate text 90 degrees on the x-axis:
    theme(axis.text.x = element_text(angle = 90, hjust = 1))
```

No Legend:
```r
    theme(legend.position = "none")
```
Ignore words in a blacklist in the df$word column:
```r
    blacklist_words = c("dog", "cat", "sheep:)
    df %>%
       filter(!word %in% blacklist_words)
```

In ggplot, order the bars correctly:
```r
mutate(word = reorder_within (word, tf_idf, character) %>%
scale_x_reordered()+
```

**Use a gradient of colors in ggplot:** 
```r
scale_color_gradient2(low="blue", high="red", midpoint = 0.5, labels = scales::percent_format())
```

**Change years into decades:**
```r
mutate(decade = 10* (year%/% 10))
```


#R


[penguins-species-bar-coord-flip-1]: penguins-species-bar-coord-flip-1.png

[penguins-species-bar-coord-flip-1-1]: penguins-species-bar-coord-flip-1.png

[penguins-species-props-bar-reorder-1]: penguins-species-props-bar-reorder-1.png

[tidyr-longer-wider]: tidyr-longer-wider.gif

[Image]: Image.jpeg

[Image-1]: Image.jpeg