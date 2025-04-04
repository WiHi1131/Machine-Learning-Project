<a href = "https://wihi1131.github.io/Machine-Learning-Project/">Home</a>

# Naïve Bayes' 

## Overview

Naïve Bayesian algorithms are a method of supervised learning. These algorithms are based on Bayes' Theorem, which deals with probabilities of events occurring based on prior knowledge of causes of those events also occurring. We say that these algorithms are "naïve" because we assume conditional independence of features, which may not actually be the case. Even with this simplifying assumption, these algorithms have still been shown to work very well in real-world applications such as spam filtering [1]. 

We use different types of Naïve Bayesian (NB) algorithms depending on the distribution of data we are dealing with, as explained below: 

- **Multinomial NB** is catered for use with discrete data, such as with trying to classify text documents with word counts [1]. 
- Bernoulli NB is designed to be used with binary or boolean data; multiple features can be used but each is "assumed to be a binary-valued (Bernoulli, boolean) variable" [1].
- Other types depending on distribution of data, such as Gaussian NB and Categorical NB, as necessary.

### Multinomial Naïve Bayes

Multinomial Naïve Bayes is designed to be used with features containing counts, such as the text document example above. Bayes' Theorem works within this algorithm to update class probabilities (such as if a text document is spam or not spam) as it sees increasing evidence within the word counts. To elaborate, the Multinomial NB algorithm calculates conditional probabilities of each feature (words in our example) when given the class label to begin. Under the assumption that all features are conditionally independent, the algorithm calculates the probability of seeing all features (word counts) by multiplying them together, and then can predict the class of an unseen data point by finding which class has a higher probability of containing all known feature probabilities in the new data point. 

The below image was taken from medium.com[2] and gives a simplified overview: 

## Sources

[1] 1.9. Naive Bayes. (n.d.). Scikit-learn. https://scikit-learn.org/stable/modules/naive_bayes.html
[2] Mocquin, Y. (2024, November 30). Multinomial Naive Bayes Classifier - TDS Archive - Medium. Medium. https://medium.com/data-science/multinomial-naive-bayes-classifier-c861311caff9



<a href = "https://wihi1131.github.io/Machine-Learning-Project/">Home</a>
