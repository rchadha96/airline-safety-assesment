# Airline Safety Assesment
Project Goal: To Assess Airline Safety and generate Risk Score based on track record using R  

## Introduction

The case study was done to assess the safety of airlines based on its track record, using the airline safety data hosted by FiveThirtyEight, which provides the safety records of major commercial airlines, over a span of 30 years. The context of this analysis is the outcome of certain academic studies that high-profile crashes can shift passenger demand away from the airlines involved in the disasters. 

The dataset divides the 30-year period into two halves and gives information about the number of crashes, fatal accidents and fatalities occurred over these years along with available seat kilometers (ASKs) of 56 different airlines. 

The prime objective of the case study was to check whether there was a relation between the crash rates of first time period and that of the second which would imply that the risk is persistent and is predictable based on its crash history.

## Analysis
### Data Standardization:
Based on the dataset obtained we have categorized the airline into private and government airlines.

```r
  ir <- read_csv("AirlineSafety-SAS.csv")
  # Adding Type of airline.
  air <- air %>%
  mutate(type=ifelse(grepl("*", airline, fixed = TRUE),"Government","Private"))
```
  

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/rchadha96/airline-safety-assesment/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
