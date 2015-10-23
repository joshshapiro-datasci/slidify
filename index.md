---
title       : Calorie calculator
subtitle    : for sedentary activity
author      : Joshua Shapiro
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Synopsis
Obesity is a medical condition in which excess body fat has accumulated to the extent that it may have a negative effect on health, leading to reduced life expectancy and/or increased health problems. In Western countries, people are considered obese when their body mass index (BMI), a measurement obtained by dividing a person's weight by the square of the person's height, exceeds 30 kg/m2, with the range 25-30 kg/m2 defined as overweight.


---

## Causes
At an individual level, a combination of excessive food energy intake and a lack of physical activity is thought to explain most cases of obesity.[68] A limited number of cases are due primarily to genetics, medical reasons, or psychiatric illness.[69] In contrast, increasing rates of obesity at a societal level are felt to be due to an easily accessible and palatable diet,[70] increased reliance on cars, and mechanized manufacturing.

---

## Sedentary lifestyle
A sedentary lifestyle plays a significant role in obesity. Worldwide there has been a large shift towards less physically demanding work, and currently at least 30% of the world's population gets insufficient exercise.

---

## Calorie calculator
There is one great calorie calculator which can help you to measure calorie needs for sedentary activity: https://joshshapiro.shinyapps.io/shiny. It has very simple and intuitive interface. Just choose your sex, weight, height and age. For example, my daily caloric needs for weight maintaining is

```r
sedentaryCoef <- 1.2
isWoman <- 0
womanShiftCoef <- -166
weight <- 86
height <- 184
age <- 31

round(sedentaryCoef * (10 * weight + 6.25 * height - 5 * age + womanShiftCoef * isWoman + 5))
```

```
## [1] 2232
```
