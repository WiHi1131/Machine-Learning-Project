<a href = "https://wihi1131.github.io/Machine-Learning-Project/">Home</a>

# Support Vector Machines

## Overview

Support Vector Machines (SVMs for short) are a type of supervised algorithm that can be used for either classification or regression. They function through the use of a hyperplane, learned from analyzing input data. The goal of an SVM is to optimize this hyperplane such that it separtes different classes of data, and to maximize a space known as a margin in-between the classes. We call the nearest data points to the hyperplane support vectors, and both are used when defining what is known as a decision boundary. New data points are binned into one side or the other of this decision boundary based on their features by the algorithm. 

### Support Vector Machines are Linear Separators

The decision function for the hyperplane is given by: 

f(x)=sign(w^⊤x+b)

Where w is the weight vector, x is an input vector of data points, and b is the bias, or error term. This is clearly a linear equation (reminiscent of y = mx + b). The image below illustrates a hyperplane separating two classes of data. Note the equation of the hyperplane on the image: 

<div>
  <img src = "images/SVM_margin_pic.PNG" title = "SVM Margin" alt = "SVM margin">
  <div>
    <p>
      <b>This is an example of a the margin hyperplane for an SVM model [1]. </b>
    </p>
  </div>
</div>

Even if the data isn't linearly separable, SVMs transform the data into a space where a flat, straight hyperplane will work to separate the data linearly. This is done using the kernel trick, described below. 

## Sources

-[1]: Wikipedia contributors. (2025, April 28). Support vector machine. Wikipedia. https://en.wikipedia.org/wiki/Support_vector_machine#/media/File:SVM_margin.png


<a href = "https://wihi1131.github.io/Machine-Learning-Project/">Home</a>


