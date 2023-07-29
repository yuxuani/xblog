---
title: bias_and_variance
date: 2023-05-12 19:10:50
tags: machine learning, notes
---

# Machine Learning: bias/variance
## Diagonising bias/variance
- underfit -- high bias
  - J_train large
  - J_cv large
- overfit -- high variance
  - J_train small
  - J_cv large

recall: cross validation, J_train, J_cv (link here)

## Regularization and bias/variance

lambda: regularization parameter

def.: formula here

- lambda large
  - w_j tends to be small (lower degree of polynomial)
  - tends to be underfit
  - high bias
  - J_train large, J_cv >> J_train

- lambda small
  - more w_j will be preserved (higher degree of polynomial)
  - tends to be overfit
  - high variance
  - J_train small, J_cv >> J_train

(curve here)

## Establishing a baseline of performance
judge based on
- human level of performance (e.g. unstructured data like audios, images, texts, etc)
- competitive algorithms
- guess based on experience

compare the gap between baseline-J_train and J_train-J_cv
- large, small? -- high bias
- small, large? -- high variance
- large, large? -- high bias and high vairance (not that common)

## Learning curve
error to m_train (number of training examples)
as m_train increases, J_train goes up and flaten out, J_cv goes down and also flaten out ...

- high bias
  - J_train is much higher than baseline level of performance
  - adding more training examples won't help much
- high variance
  - J_cv goes down and gets closer to baseline lever of performance
  - adding more traning examples is likely to help

(curve here)

## Deciding what to try next revisited
for solving a problem of 
- high variance
  - get more training examples
  - make the model simpler
    - smaller sets of features
    - increasing lambda
- high bias
  - make the model more complex
    - getting additional features/adding polynomial features
    - decreasing lambda

recall: regularization

## Bias/variance and neural networks
simple model: high bias
complex model: high variance
tradeoff

bigger neural networks are low bias machines (but: expensive)

workflow:
1. Do well on the training set? 
   - Yes (J_train baseline) -- go to 2.
   - No (J_train >> baseline) -- bigger neural network
2. Do well on the cross validation set?
   - Yes (J_cv J_train) -- done!
   - No (J_cv >> J_train) -- get more data -- go to 1.

(loop fig here)

## Optional Lab
to be continue...

## Reference
Machine Learning Specialization Course 2 Week 3 Bias/Variance