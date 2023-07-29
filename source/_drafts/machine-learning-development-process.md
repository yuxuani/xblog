---
title: machine learning development process
tags: notes
---
# Machine Learning Development Process
## Iterative loop of ML development
(fig here)

choose architecture-- train model -- diagnostics -- loop...
model, data, hyperparameter
bias/variance and error analysis

bigger neural networks?
more data?
features?
regularizations parameters?

## Error analysis
manually examine misclassified examples
collect new data, develope sophiscated features, etc

## Adding data
getting more data of everything
getting more data of specific 

## Transfer learning: using data from a different task
download (or train on your own) the pre-trained neural network
fine tuning the neural network
## Full cycle of a machine learning 
scope the project (define)
collect data
train model
deploy
## Fairness, bias and ethics
### Bias
For example:
- Hiring tool that discriminates agains women
- Facial recognition system matching dark skinned individuals to criminal mugshots
- Biased bank loan approval
- Toxic effect of reinforcing negative stereotypes
### Advere use Case
- Deepfakes
- Spreading toxic/incendiary speech through optimizing for engagement
- Generate fake content for commercial or political purpose
- Using ML to build harmful products, commit froud etc
### Guidelines
- Get a diverse team to brainstrom things that might go wrong, with emphathsis on possible harm to vulnerable groups
- Carry out literature search on standards/guidelines in your industry
- Audit the systems against possible harm pior to deployment
- Develop mitigation plan, and after deployment, monitor for possible harm
## Skewed Data
e.g. rare disease classification example
precise and recall
tradeoff between precise and recall

manually decide based on the purpose

Average (P+R)/2 not recommended
F1 score 1/2(1/P + 1/R) harmonic mean, emphasizes more on the smaller value