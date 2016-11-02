---
published: true
title: Parsing XML File in Python
layout: post
---

In this article, I will summarize some notes about using Python to parse the XML file.

1. What is the difference between cElementtree and Elementtree?

   Both cElementtree and Elementtree are the libries in Python to parse the XML file. cElementtree is implemented by C, and Elementtree is    implemented by Python. Basically, they have the same functionality.  

2. What is the difference between parse() and interparse()?

   parse() read the whole XML file into memory as Tree structure, while interparse() does not read in the whole XML file. For large XML      file, the interparse() works well.
