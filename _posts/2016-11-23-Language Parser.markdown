---
published: true
title: Language Parser
layout: post
---

I this article, I will summarize the basic knowlege of building a language parser(English).

## Context Free Grammar
Context free grammar(CFG) consists of different rules. Generally speaking, there could be numerious different rules.

A string s is said to be in the language defined by a CFG if there is a least one deviation whose yeild is s. 

### Parse Tree
Every sentence can be represented as a parse tree according to the CFG. The task of parsing is to build the parse tree of a sentence.
### Unary rule

NN -> man;
S -> NP;

### Cocke–Younger–Kasami(CYK) algorithm
CYK algorithm is a dynamic programming method to find most probable parse tree for a given sentence. This algorithm can be used only when the CFG is in the Chomsky normal form (CNF). It is possible to convert any PCFG into an equivalent grammar in CNF. 
