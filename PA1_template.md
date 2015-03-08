# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data

```r
data <- read.csv("activity.csv", header = TRUE)
str(data)
```

```
## 'data.frame':	17568 obs. of  3 variables:
##  $ steps   : int  NA NA NA NA NA NA NA NA NA NA ...
##  $ date    : Factor w/ 61 levels "2012-10-01","2012-10-02",..: 1 1 1 1 1 1 1 1 1 1 ...
##  $ interval: int  0 5 10 15 20 25 30 35 40 45 ...
```


## What is mean total number of steps taken per day?

Calcualte the sum of steps for each day:

```r
stepsPerDay <- tapply(data$steps, data$date, sum, na.rm =TRUE)
```

Plot a histogram of this data:


```r
hist(stepsPerDay)
```

![](PA1_template_files/figure-html/unnamed-chunk-3-1.png) 

The mean of steps taken each day is

```r
mean(stepsPerDay)
```

```
## [1] 9354.23
```

And the median is

```r
median(stepsPerDay)
```

```
## [1] 10395
```

## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
