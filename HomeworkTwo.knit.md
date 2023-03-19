---
title: "Homework 2"
author: "amirarsalan faghani 21080056!"
output: pdf_document
---



**Before attempting to solve these homework questions make sure that you've install `tinytex` package onto your system with `install.packages(tinytex)` and `tinytex::install_tinytex()` commands.**

\vspace{1cm}

**Question 1** Calculate how many minutes in January.


```r
start_date <- as.POSIXct("2023-01-01 00:00:00")
end_date <- as.POSIXct("2023-01-31 23:59:59")
total_seconds <- difftime(end_date, start_date, units = "secs")
total_minutes <- as.numeric(total_seconds) / 60
cat("There are", total_minutes, "minutes in January 2023.")
```

```
## There are 44639.98 minutes in January 2023.
```

**Question 2** Add the numbers 3 1 4 1 5 9 2 6 without *using the addition sign*.


```r
sum(c(3, 1, 4, 1, 5, 9, 2, 6))
```

```
## [1] 31
```

**Question 3** Create a vector named `x` containing the series -1, -0.9, ..., 0, 0.1, ..., 0.9, 1 and print the result.


```r
x <- seq(from = -1, to = 1, by = 0.1)
print(x)
```

```
##  [1] -1.0 -0.9 -0.8 -0.7 -0.6 -0.5 -0.4 -0.3 -0.2 -0.1  0.0  0.1  0.2  0.3  0.4
## [16]  0.5  0.6  0.7  0.8  0.9  1.0
```

**Question 4** How do we get R to print the text "SBF!" 30 times without repeatingly typing it?


```r
cat(rep("SBF! ", 30))
```

```
## SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!  SBF!
```

```r
#rep() function 
```

**Question 5** Create two vectors named "wizards" and "ranking".
Let the "wizards" include the names Harry, Ron, Fred, George and Sirius, while the "ranking" includes the numbers 4, 2, 5, 1, and 3.


```r
wizards <- c("Harry", "Ron", "Fred", "George", "Sirius")
ranking <- c(4, 2, 5, 1, 3)
```

**Question 6** Print/extract the second element of the wizards vector.


```r
wizards <- c("Harry", "Ron", "Fred", "George", "Sirius")
print(wizards[2])
```

```
## [1] "Ron"
```

**Question 7** Replace the names Fred, George and Sirius in the vector 'wizards' with the names Hermione, Ginny, and Malfoy.


```r
wizards <- c("Harry", "Ron", "Fred", "George", "Sirius")
wizards[c(3, 4, 5)] <- c("Hermione", "Ginny", "Malfoy")
print(wizards)
```

```
## [1] "Harry"    "Ron"      "Hermione" "Ginny"    "Malfoy"
```

**Question 8** Anyone who hasn't read Harry Potter (like the professor of this class) needs tags to know who these characters are.
Name the elements of the `wizards` vector as **Lead**, **Friend**, **Friend**, **Wife** and **Rival**.
Print the results.


```r
wizards <- c("Harry", "Ron", "Fred", "George", "Sirius")
names(wizards) <- c("Lead", "Friend", "Friend", "Wife", "Rival")
print(wizards)
```

```
##     Lead   Friend   Friend     Wife    Rival 
##  "Harry"    "Ron"   "Fred" "George" "Sirius"
```

**Question 9** 26 students entered the PEC206 midterm exam.
The grades of these students are: 18, 95, 76, 90, 84, 83, 80, 79, 63, 76, 55, 78, 90, 81, 88, 89, 92, 73, 83, 72, 85, 66, 77, 82, 99 and 87.
Save test scores in a vector named 'scores'.
Calculate the mean, median, and range of exam grades.


```r
scores <- c(18, 95, 76, 90, 84, 83, 80, 79, 63, 76, 55, 78, 90, 81, 88, 89, 92, 73, 83, 72, 85, 66, 77, 82, 99, 87)

mean_score <- mean(scores)
print(paste("Mean score:", mean_score))
```

```
## [1] "Mean score: 78.5"
```

```r
median_score <- median(scores)
print(paste("Median score:", median_score))
```

```
## [1] "Median score: 81.5"
```

```r
range_score <- range(scores)
print(paste("Range of scores:", range_score[2] - range_score[1]))
```

```
## [1] "Range of scores: 81"
```

**Question 10** In 2015, Nilay had an annual income of 22,000 TL, and total expenses of 3,000 TL.
In 2016, his annual income was 67,000 TL, and his total expenses were 23,000 TL.
In 2017, his annual income was 70,000TL, and his total expenses were 32,000TL.
Finally, in 2018, his annual income was 72,000 TL and his total expenses were 35,000 TL.
To save this information, create 3 different vectors named 'years', 'income' and 'expenses'.
Calculate Nilay's annual savings and save these values in a vector named 'savings'.


```r
years <- c(2015, 2016, 2017, 2018)
income <- c(22000, 67000, 70000, 72000)
expenses <- c(3000, 23000, 32000, 35000)
savings <- income - expenses
print(paste("Years:", years))
```

```
## [1] "Years: 2015" "Years: 2016" "Years: 2017" "Years: 2018"
```

```r
print(paste("Income:", income))
```

```
## [1] "Income: 22000" "Income: 67000" "Income: 70000" "Income: 72000"
```

```r
print(paste("Expenses:", expenses))
```

```
## [1] "Expenses: 3000"  "Expenses: 23000" "Expenses: 32000" "Expenses: 35000"
```

```r
print(paste("Savings:", savings))
```

```
## [1] "Savings: 19000" "Savings: 44000" "Savings: 38000" "Savings: 37000"
```