---
# weight: 1
# aliases: ["/first"]
author: "Me"
# author: ["Me", "You"] # multiple authors
# showToc: false
# TocOpen: true
# draft: true
comments: true
# canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
# searchHidden: true
# ShowReadingTime: false
# ShowBreadCrumbs: true
# ShowPostNavLinks: false
ShowRssButtonInSectionTermList: true
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
# editPost:
#     URL: "https://github.com/vitamickey/digital-garden/tree/main/content"
#     Text: "Suggest Changes" # edit text
#     appendFilePath: true # to append file path to Edit link
date: 2022-07-25T09:49:47+10:00
title: "Discrete Mathematics II"
# description: ""
tags: ["mathematics"]
# series: [""]
# bookofbible: [""]
lastmod: 2022-07-28T21:49:47+10:00
math: true
---

## I Basic Counting (pg. 5)

### 1 Selections (pg. 5)

#### 1.1-1.4 Basic counting formulas

Given a set of \\(n\\) objects, the number of ways of selecting \\(r\\) objects can be found according to the table below.

| | No repetition | With repetition |
| :---: | :---: | :---: |
| **Order matters (Ordered)** | \\(\frac{n!}{(n-r)!}\\) | \\(n^r\\) |
| **Order does not matter (Unordered)** | \\(\binom{n}{r} = \frac{n!}{(n-r)!r!}\\) | \\(\binom{n+r-1}{r} = \binom{n+r-1}{n-1}\\) |

#### 1.4 Intuition for unordered selections with repetition

This is the balls and buckets representation. If we wish to select \\(r\\) objects from an \\(n\\)-set, we essentially want to count the number of ways we can split up the \\(n\\) objects (i.e. the balls) into \\(r\\) parts (i.e. the buckets). Say we have \\(n=8\\) balls and set \\(r=3\\). Under the original question, we ask" "how many unordered selections of 3 objects from 8 objects are there with repetition allowed?". Under this buckets and balls framework, we ask, "how many ways can we fill 3 buckets with 8 balls, if some of those buckets can be empty?".

(to edit)

#### Equivalent combinatorial counts

(to edit)

### 2 Combinatorial Identities (pg. 9)

Pascal's Triangle

- \\(\binom{n+1}{r} = \binom{n}{r} + \binom{n}{r-1}\\)
- \\(\left(x+y\right)^n = \sum_{r=0}^{n} \binom{n}{r} x^{n}y^{n-r}\\)
- \\(\sum_{r=0}^{n} \binom{n}{r} = 2^n\\)
- \\(\binom{n}{r} = \sum_{i=0}^{n-1} \binom{i}{r-1}\\)
  - Equivalently, can index from \\(r-1\\) to \\(n\\)
- \\(\sum_{r=0}^{n} (-1)^{r}\binom{n}{r}=0\\)

## II Inclusion-Exclusion and Related Techniques (pg. 13)

### 3 The Principle of Inclusion and Exclusion (pg. 13)

### 4 Permutations and Derangements (pg. 15)

### 5 Classical M¨obius Inversion (pg. 17)

## Upcoming

- 6 Partially Ordered Sets (pg. 20)
- 7 M¨obius Function for Posets (pg. 22)
- III Counting with Groups (pg. 24)
- 8 Symmetry Groups and Group Actions (pg. 24)
- 9 Orbits and Stabilizers (pg. 26)
- 10 The Counting Theorem (pg. 28)
- IV Generating Functions and Partitions (pg. 31)
- 11 Ordinary Generating Functions (pg. 31)
- 12 Exponential Generating Functions (pg. 36)
- 13 Linear Recurrence Relations (pg. 40)
- 14 Partitions (pg. 44)
- V Classification of surfaces (pg. 49)
- 15 Basic concepts (pg. 49)
- 16 The big questions (pg. 51)
- 17 More surfaces (pg. 52)
- 18 Invariants and Euler characteristic (pg. 54)
- 19 Small polygonal constructions (pg. 56)
- 20 Orientability (pg. 58)
- 21 Operations on polygons (pg. 59)
- 22 Word representations (pg. 61)
- 23 Rules for words (pg. 63)
- 24 The classification theorem (pg. 66)
- VI Graph Theory (pg. 70)
- 25 Introduction to Graphs (pg. 70)
- 26 Walks in graphs (pg. 75)
- 27 Trees (pg. 78)
- 28 Matchings (pg. 80)
- 29 Graph colouring (pg. 82)
- VII Graph Algorithms (pg. 87)
- 30 Shortest Paths (pg. 87)
- 31 Spanning Trees (pg. 88)
- 32 Finding patterns in strings (pg. 89)
- 33 Algorithms for maximum matchings in bipartite graphs (pg. 90)
- VIII Design Theory (pg. 95)
- 34 Introduction to Combinatorial Design Theory (pg. 95)
- 35 Latin Squares (pg. 96)
- 36 Steiner Triple Systems (pg. 97)

Everything sourced from my discrete maths course unless stated otherwise.

Related notes:

- [Mathematics](mathematics)

[^1]: https://math.stackexchange.com/questions/208377/combination-with-repetitions
