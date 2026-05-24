Naive Bayes is a [[probabilistic classification algorithm]] based on [[Bayes' Theorem]] with a strong (and "naive") assumption: 
	**All features are independent given the class label**

----
## Core Idea 

We want to compute: 
$$
P\big(y \mid x_1, x_2, \dots, x_n\big)
$$ Using Bayes' theorem : 
$$
P(y \mid x) = \frac{P(x \mid y)\, P(y)}{P(x)}
$$
 Key Assumption(The "Naive" Part)

Instead of modelling joint probability :-

$$

P\big(x_1, x_2, \dots, x_n \mid y\big), 
\text{ we assume}
$$
We assume:
$$
P\big(x_1, x_2, \dots, x_n \mid y\big)
=
\prod_{i=1}^{n} P(x_i \mid y)
$$
