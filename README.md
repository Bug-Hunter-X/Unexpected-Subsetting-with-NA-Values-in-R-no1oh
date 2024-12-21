# Unexpected Subsetting with NA Values in R

This repository demonstrates a common, yet subtle, error in R related to subsetting data frames when dealing with missing values (NA).

The `bug.r` file contains code that attempts to subset a data frame based on a condition involving NA.  Due to how R handles comparisons with NA, the result is unexpected. The `bugSolution.r` file provides the corrected code, illustrating how to properly handle NA values in such situations.

## Problem:

When comparing values to NA using logical operators (>, <, ==, etc.), the result is always NA.  This means that rows containing NA values are neither included nor excluded from the subset, leading to an empty subset even if some rows might logically satisfy the condition.

## Solution:

The solution involves explicitly handling NA values using functions like `is.na()` to check for missing data and adjust the subsetting logic accordingly.  You can exclude NA values or treat them differently based on your needs.
