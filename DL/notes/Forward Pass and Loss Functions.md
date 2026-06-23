
# Forward Pass and Loss Functions

## Big Idea
A neural network performs two tasks:
1. Makes a prediction (Forward Pass)
2. Measures prediction error (Loss Function)
---
# Forward Pass

## Definition
The forward pass is the process of passing an input through all layers of a neural network to produce a prediction.

Input → Hidden Layers → Output

---
## Computation at Each Layer

### Step 1: Linear Transformation

$$
z^{[l]} = W^{[l]}a^{[l-1]} + b^{[l]}
$$

where:

- $W^{[l]}$ = weight matrix
- $a^{[l-1]}$ = previous layer activations
- $b^{[l]}$ = bias vector
- $z^{[l]}$ = weighted sum

### Step 2: Activation Function

$$
a^{[l]} = g(z^{[l]})
$$

where:

- $g$ = activation function
- $a^{[l]}$ = output of current layer

Examples:

- ReLU
- Sigmoid
- Tanh

---

## Forward Pass Flow

Input

$$
a^{[0]} = x
$$

For each layer:

$$
z^{[l]} = W^{[l]}a^{[l-1]} + b^{[l]}
$$

$$
a^{[l]} = g(z^{[l]})
$$

Final prediction:

$$
\hat y = a^{[L]}
$$

---

# Loss Function

## Definition

A loss function measures the difference between:

- True value: $y$
- Predicted value: $\hat y$

Output is a single scalar value.

Goal:

Minimize loss during training.

---

# Mean Squared Error (Regression)

Used for:

- House prices
- Temperature prediction
- Stock prediction

Formula:

$$
MSE = \frac{1}{N}\sum_{i=1}^{N}(y_i-\hat y_i)^2
$$

### Properties

- Penalizes large errors heavily
- Sensitive to outliers

---

# Cross Entropy Loss (Classification)

Used for:

- Cat vs Dog
- Spam Detection
- Disease Classification

Formula:

$$
L = -\sum_{c=1}^{C} y_c \log(\hat y_c)
$$

where:

- $y_c$ = true class indicator
- $\hat y_c$ = predicted probability

---

## Example

True Label:

$$
[1,0,0]
$$
Good Prediction:

$$
[0.8,0.1,0.1]
$$

Low Loss

Bad Prediction:

$$
[0.1,0.2,0.7]
$$

High Loss

---

# Key Takeaways

- Forward pass generates predictions.
- Every layer performs:
  - Linear transformation
  - Activation function
- Loss function measures prediction error.
- MSE is used for regression.
- Cross Entropy is used for classification.
- Training aims to minimize loss.

---

# Intuition

Forward Pass:
"Make a prediction."

Loss Function:
"Measure how wrong the prediction is."

Training:
"Adjust weights to reduce loss." 

#review 
