---
layout: post
title: "Pandas DataFrame -- Creation and Slicing"
date: 2016-10-21
---

I this article, I summarize the methods of Pandas dataframe creation and slicing.

## Part 1. Create Pandas Dataframe

## Part 2. Slicing Pandas Dataframe

### Difference of .loc and .iloc

(1) loc gets rows (or columns) with particular labels from the index.<br />
(2) iloc gets rows (or columns) at particular positions in the index (so it only takes integers).<br />
(3) ix usually tries to behave like loc but falls back to behaving like iloc if a label is not present in the index.<br />

Note: in Pandas version 0.20.0 and above, ix is deprecated and the use of loc and iloc is encouraged instead.

To illustrate the differences between .loc and .iloc, consider the following Series:

>>> s = pd.Series(np.nan,index=[49,48,47,46,45, 1, 2, 3, 4, 5])

For this example, s.iloc[:3] returns us the first 3 rows (since it treats 3 as a position) and s.loc[:3] returns us the first 8 rows (since it treats 3 as a label):

>>> s.iloc[:3] # slice the first three rows
49   NaN
48   NaN
47   NaN

>>> s.loc[:3] # slice up to and including label 3
49   NaN
48   NaN
47   NaN
46   NaN
45   NaN
1    NaN
2    NaN
3    NaN

Notes:<br />
(1) Dataframe slicing follow the same rule as Series. <br />
(2) If the Series or Dataframe does not have labels for index or column, when using loc, the default 0,1,2,3... can be read as index or column by loc.  
