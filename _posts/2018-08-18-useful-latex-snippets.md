---
author: Mythreyi
date: 2018-08-18 00:05:11+00:00
excerpt: A quick "here you go" post with useful LaTeX snippets.
layout: post
slug: latex-snippets
title: Useful LaTeX Snippets
tags: tools
---

There have been many a time where I have gone to previous .tex files that I have created to retrieve a specific snippet of $$\LaTeX$$ code. Since reusability is one strong point for $$\LaTeX$$, I think a collection of these snippets in one place will be pretty useful, especially for last-minute maths assignments. :P

## Basics

### Images

## Mathematics

### Linear Algebra

#### Matrices with different kinds of braces
_Bonus:_ Dots!

$$A = \begin{bmatrix}  a_{11} & \dots & a_{1n} \\ \vdots & \ddots & \\ a_{m1} &        & a_{mn}  \end{bmatrix} \text{ and } B = \begin{bmatrix}  b_{11} & \dots & b_{1p} \\ \vdots & \ddots & \\ b_{n1} &        & b_{np}  \end{bmatrix}$$

```latex
\[
A = \begin{bmatrix} 
    a_{11} & \dots & a_{1n} \\
    \vdots & \ddots & \\
    a_{m1} &        & a_{mn} 
    \end{bmatrix}
\text{ and }
B = \begin{bmatrix} 
    b_{11} & \dots & b_{1p} \\
    \vdots & \ddots & \\
    b_{n1} &        & b_{np} 
    \end{bmatrix}
\]
```

 