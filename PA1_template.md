# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data


```r
if (!file.exists("activity.csv")) {
  download.file("https://d396qusza40orc.cloudfront.net/repdata%2Fdata%2Factivity.zip", 
                method="curl", destfile="repdata_data_activity.zip");
  unzip("repdata_data_activity.zip");
}

activity = read.csv("activity.csv");
activity$date = as.POSIXlt(activity$date, "%YYYY-%MM-%DD");
```

```
## Warning: unknown timezone '%YYYY-%MM-%DD'
## Warning: unknown timezone '%YYYY-%MM-%DD'
## Warning: unknown timezone '%YYYY-%MM-%DD'
## Warning: unknown timezone '%YYYY-%MM-%DD'
## Warning: unknown timezone '%YYYY-%MM-%DD'
## Warning: unknown timezone '%YYYY-%MM-%DD'
## Warning: unknown timezone '%YYYY-%MM-%DD'
## Warning: unknown timezone '%YYYY-%MM-%DD'
## Warning: unknown timezone '%YYYY-%MM-%DD'
## Warning: unknown timezone '%YYYY-%MM-%DD'
## Warning: unknown timezone '%YYYY-%MM-%DD'
```

## What is mean total number of steps taken per day?



