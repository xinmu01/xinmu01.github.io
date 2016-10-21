---
published: true
title: Numpy Array -- Summary
layout: post
---
In this post, I summarize some key points of Numpy array.

1. Numpy array is much faster than the normal python list;
2. Define 1D array: numpy.array([1,2,3],float); Note that this is a row vector;
3. Define 2D array: numpy.array([[1,2,3],[4,5,6]],float);
4. numpy.dot() gives an array contains the 1 number;
5. 2D array index:
    a = numpy.array([[1,2,3],[4,5,6]],float)
    a[1,1] = 5.
    a[1][1] = 5.
    a[1,:] = [4.,5.,6.]
    a[;,2] = [3., 6.] 
    Note: the last two are both row vector.