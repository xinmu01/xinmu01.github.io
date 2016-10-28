---
published: true
title: Bag-of-Word and N-gram Language Model
layout: post
---
## Bag-of-Word
Bag-of-word is the simplies language model, which is commonly used in methods of document classification where the (frequency of) occurrence of each word is used as a feature for training a classifier. In this model, a text (such as a sentence or a document) is represented as the bag (multiset) of its words, disregarding grammar and even word order but keeping multiplicity. 

For example, suppose we have two simple sentences:
(1) John likes to watch movies. Mary likes movies too.
(2) John also likes to watch football games.
Then a list of the words in these two sentences is ["John", "likes", "to", "watch", "movies", "also", "football", "games", "Mary", "too"].
We can select the frequency or counts of each words as features, and covert thest two sententences to numeric vectors:
(1) [1, 2, 1, 1, 2, 0, 0, 0, 1, 1]
(2) [1, 1, 1, 1, 0, 1, 1, 1, 0, 0]
