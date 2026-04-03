It is a type of ML model that learns **how the data is generated** by modelling the **[[joint probability distribution]]** $P(x, y)$ or equivalently $P(x \mid y)  P(y)$
- Generates new data samples
- For example:
	- Generate new images
	- Fill missing data
	- Simulate sequences
Informal meaning : it learns **how features *x* are produced for each class *y***
### Intuition 
Imagine you want to recognize cats vs dogs:
	A generative model asks : 
		"What does a cat look like? What does a dog look like?"
     It learns : 
     - Shapes, patters, structure of each class 
     - then uses to classify 
## Types
1. [[Naive Bayes]]
2. [[Gaussian Mixture Models]]
3. [[Hidden Markov Models]]

## Step by Step working 
TLDR : Learn how data is generated -> $P(x \mid y)$, $P(y)$ 
	   Then classify using Bayes' Theorem
### Step 1 : Learn [[prior probability]]
- Probability of each class:  $P(y)$ 

### Step 2 : Learn [[Likelihood]]
- How data looks given a class:  $P(x \mid y)$

### Step 3 : Use [[Bayes' Theorem]] to classify 

$$  
P(y \mid x) = \frac{P(x \mid y)\,P(y)}{P(x)}  
$$
- Choose class with highest probability 
		- Meaning :-
			- $P(y∣x)$: Posterior
			- $P(y \mid x)$ : Likelihood 
			- $P(y)$: Prior 
			- $P(x)$ : Evidence


## Mathematical Construction 
### Step-by-step generative process 

Given dataset,
$$  
D = \{(x_i, y_i)\}_{i=1}^{n}, \quad x_i \in \{0,1\}^{d}, \quad y_i \in \{0,1\}  
$$

##### Step 1: Generate Label
$$
P(y = 1) = p,\quad P(y = 0) = 1 - p
$$
##### Step 2: Generate Features
