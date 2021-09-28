---
title: "Calculus Based Statistics"
date: 2021-08-26T00:00:00+08:00
---

Based on *Probability and Statistics for Engineering and the Sciences* 9e.

## Descriptive Statistics

|Description|Equations|
|-:|:-|
|Sample mean|$\bar{x} = \dfrac{1}{n}\sum\limits_{i=1}^n x_i$|
|Sample median|$\tilde{x} = \footnotesize \begin{cases}\text{middle ordered value} &\text{if odd} \cr \text{average of two middle ordered values} &\text{if even} \end{cases}$|
|Deviation|$x_i - \bar{x}$|
|Sum of squared deviation|$\begin{aligned} S_{xx} &= \textstyle \sum(x_i - \bar{x})^2 \cr &= \textstyle \sum x_i^2 - \dfrac{1}{n}(\sum x_i)^2 \cr &= \textstyle \sum x_i^2 - n(\bar{x})^2 \end{aligned}$|
|Sample variance|$s^2 = \dfrac{S_{xx}}{n-1}$|
|Sample standard deviation|$s = \sqrt{s^2}$|
|Properties of sample variance|$x_i' = x_i + c \implies s_{x'}^2 = s_{x}^2 \newline x_i' = cx_i \implies s_{x'}^2 = c^2s_{x}^2$|

## Probability

### Basic Probability

#### Notations

|Description|Equations|
|-:|:-|
|Sample space|$\mathcal{S}$|
|Event|$A$|
|Union (or)|$A \cup B$|
|Intersection (and)|$A \cap B$|
|Complement (not)|$A'$|
|Null event|$\varnothing$|
|Disjoint (mutually exclusive)|$A \cap B = \varnothing$|
|Probability of event $A$|$P(A)$|

#### Axioms

|Description|Equations|
|-:|:-|
|Non-negativity|$P(A) \ge 0$|
|Probability of event in sample space|$P(\mathcal{S}) = 1$|
|Addition of infinite disjoint events|$\bigcap\limits_{i=1}^\infty A_i = \varnothing \implies P\left(\bigcup\limits_{i=1}^\infty A_i\right) = \sum\limits_{i=1}^\infty P(A_i)$|

#### Properties

|Description|Equations|
|-:|:-|
|Null event and zero probability|$P(\varnothing) = 0$|
|Probability of event and its complement|$P(A) + P(A') = 1$|
|Maximum probability|$P(A) \le 1$|
|Addition of disjoint events|$P(A \cup B) = P(A) + P(B)$|
|Addition of any two events|$P(A \cup B \cup C) = P(A) + P(B) - P(A \cap B)$|
|Addition of any three events|$P(A \cup B) = P(A) + P(B) + P(C) - P(A \cap B) - P(B \cap C) - P(A \cap C) + P(A \cap B \cap C)$|

#### Conditional probability

|Description|Equations|
|-:|:-|
|Conditional probability of $A$ given $B$ occured|$P(A\vert B) = \dfrac{P(A \cap B)}{P(B)}$|
|Probability of event intersection|$P(A \cap B) = P(A \vert B)P(B)$|
|Law of total probability|$\bigcap\limits_{i=1}^{k} A_i = \varnothing \implies P(B) = \sum\limits_{i=1}^{k} P(B \vert A_i)P(A_i)$|
|Bayes' Theorem|$P(A \vert B)={\dfrac {P(B \vert A)P(A)}{P(B)}}$|
|**Bayes' Theorem**|$P(A_j \vert B) = \dfrac{P(A_j \cap B)}{P(B)} = \dfrac{P(B \vert A_j)P(A_j)}{\sum\limits_{i=1}^{k} P(B \vert A_i)P(A_i)}$|

#### Independence

|Description|Equations|
|-:|:-|
|Independent events|$P(A \vert B) = P(A)$|
|Dependent events|$P(A \vert B) \not= P(A)$|
|Probability of independent event intersection|$P(A \vert B) = P(A) \iff P(A \cap B) = P(A)P(B)$|
|Mutually independent events|$P(\bigcap\limits_{i=1}^k A_i) = \prod\limits_{i=1}^k P(A_i)$|

#### Counting

|Description|Equations|
|-:|:-|
|$k$-tuples|Ordered collection of $k$ elements|
|Product rule for $k$-tuples|A set of $k$-tuples with probability $p_i$ for $i$th element has $\prod p_i$ possible $k$-tuples.|
|Permutations (ordered subset) of size k formed from n individuals|$P_{k, n} = \dfrac{n!}{(n-k)!}$|
|Combinations (unordered subset) of size k formed from n individuals|$\displaystyle C_{k, n} = \binom{n}{k} = \dfrac{P_{k, n}}{k!} = \dfrac{n!}{k!(n-k)!}$|

### Discrete Random Variables and Probability Distributions

#### Random variables

|Description|Equations|
|-:|:-|
|||
|||
|||
|||
|||
|||
|||

## Inferential Statistics

<!--
|Description|Equations|
|-:|:-|
|||
|||
|||
|||
|||
|||
|||
-->