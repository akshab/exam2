---
title: "Exam 2" 
author: "Aakansha Bagepally"
output: pdf_document
---

library(readxl)
college_scorecard <- read_excel("2021_exam2_data.xlsx", 
    sheet = "college_scorecard")
View(college_scorecard)
summary(college_scorecard)
library(tidyverse)
small_scorecard <- college_scorecard %>% filter(state_abbr == "TX"| state_abbr == "LA") %>% filter(year == 2014 | year == 2015) %>% filter(pred_degree_awarded_ipeds == 3)
