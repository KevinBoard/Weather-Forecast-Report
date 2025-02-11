setwd("C:/Users/kboar/OneDrive/511/Week 3")

install.packages("swirl")
library(swirl)
install_from_swirl("R Programming")
swirl()

dataset <- hw3_data

colnames(dataset)
#1: "Ozone"   "Solar.R" "Wind"    "Temp"    "Month"   "Day"

head(dataset, 2)
#2: Ozone Solar.R Wind Temp Month Day
#1     41     190  7.4   67     5   1
#2     36     118  8.0   72     5   2

nrow(dataset)
#3: 153

tail(dataset, 2)
#4:   Ozone Solar.R Wind Temp Month Day
#152     18     131  8.0   76     9  29
#153     20     223 11.5   68     9  30

dataset[47, "Ozone"]
#5: 21

sum(is.na(dataset$Ozone))
#6: 37

mean(dataset$Ozone, na.rm = TRUE)
#7: 42.12931

subset_data <- subset(dataset, Ozone > 31 & Temp > 90)
mean(subset_data$Solar.R, na.rm = TRUE)
#8: 212.8

mean(dataset$Temp[dataset$Month == 6], na.rm = TRUE)
#9: 79.1

max(dataset$Ozone[dataset$Month == 5], na.rm = TRUE)
#10: 115
