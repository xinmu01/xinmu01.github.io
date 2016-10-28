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

Then a list of the words in these two sentences is:

["John", "likes", "to", "watch", "movies", "also", "football", "games", "Mary", "too"].

We can select the frequency or counts of each words as features, and covert these two sentences to numeric vectors:

(1) [1, 2, 1, 1, 2, 0, 0, 0, 1, 1]

(2) [1, 1, 1, 1, 0, 1, 1, 1, 0, 0]

This numeric representation does not preserve the order of the words in the original sentences. This kind of representation has several successful applications, such as email filtering.

## N-gram Model
Bag-of-word model is an orderless document representation, which means only the counts of words matter. For instance, in the above example "John likes to watch movies. Mary likes movies too", the bag-of-words representation will not reveal the fact that a person's name is always followed by the verb "likes" in this text. As an alternative, the n-gram model can be used to store this spatial information within the text. Applying to the same example above, a bigram model will parse the text into following units:

["John likes", "likes to", "to watch", "watch movies", "Mary likes", "likes movies", "movies too"]

Then the term frequency of each unit is stored as before. Conceptually, we can view bag-of-word model as a special case of the n-gram model, with n=1.



