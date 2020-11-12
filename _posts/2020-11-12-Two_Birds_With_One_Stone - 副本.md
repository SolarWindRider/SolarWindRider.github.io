# Two Birds With One Stone: An Efficient Hierarchical Framework for Top-k and Threshold-based String Similarity Search  
ICDE Conference 2015

## I. Introduction

1. String similarity search has a widespread applications such as web search, spell checking and DNA sequence discovery.

2. There are many methods to quantify the similarity such as Jaccar, Cosine and edit distance. This work focus on **edit distance** only.

3. Two kinds of string similarity search:  
  **(1) threshold_based**  
  It identifies all the strings from dataset whose edit distance is within the threshold.  
  **(2) top-k**  
  It find k strings from dataset that have smallest edit distance to the query.  

4. Problem to address:  
  Existing methods are not efficient enough.

5. **Four main contributions:**  
  (1) Propose HS-tree to improve top-k algorithm and threshold-based algorithm.  
  (2) Develop HS-Search and HS-topk based on HS-tree to improve threshold-base algorithm and top-k algorithm.  
  (3) Develop batch-based and greedy-match-based pruning strategies to prune dissimilar strings.  

  (4) Experiments' result shows that their method is better than the state-of-the-art.

## II. Preliminaries

### A. Problem Definition

***Definition 1 (Threshold-based)***:

Given a string set S, a query q, and a threshold τ, threshold-based similarity search finds all strings s ∈ S such that ED(s, q) ≤ τ.

***Definition 2 (top-k)***:

Given a string set S, a query q, and an integer k, top-k similarity search finds a subset R ⊆ S, such that \|R\| = k and for any r ∈ R and s ∈ S − R, ED(r, q) ≤ ED(s, q).

### B. Related Works

(1) Threshold-based:  

Generally rather expensive than top-k.

(2) Top-k:

Their method has two advantages.

First, utilize the HS-tree to eliminate dissimilar strings. 

Second, select appropriate nodes in the HS-tree to efficiently identify the answer.

(3) Similarity Join:

Similarity Join methods, such PassJoin, are designed to find all similar string pairs in the two given string sets.

Their HS-tree is helpful to improve similarity join

(4) Other related works:

Not important enough to check out all of them for me.

## III. The Hierarchical Segment Index

![HS-tree Index](HS-tree.png)
