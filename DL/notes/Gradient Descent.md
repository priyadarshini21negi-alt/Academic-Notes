
## Goal
Find parameters $\theta$ that minimize the loss function:

$$
L(\theta)
$$

---
## Core Idea
Move parameters in the direction of steepest decrease of the loss.
Gradient ($\nabla L$) points in the direction of steepest increase.
Therefore, move in the opposite direction.

---

## Update Rule

$$
\theta_{new}
=
\theta_{old}
-
\eta \nabla L(\theta_{old})
$$

where:
- $\theta$ = model parameters
- $\eta$ = learning rate
- $\nabla L$ = gradient of loss

---
## Learning Rate
- Small $\eta$ → slow convergence
- Large $\eta$ → overshooting / instability
- Good $\eta$ → fast and stable convergence

---

## Linear Regression Example

Model:

$$
\hat y = mx + c
$$

Parameters:

$$
\theta = \{m,c\}
$$

Loss:

$$
L(m,c)
=
\frac1N
\sum_{i=1}^{N}
(\hat y_i-y_i)^2
$$

Updates:

$$
m
\leftarrow
m
-
\eta
\frac{\partial L}{\partial m}
$$

$$
c
\leftarrow
c
-
\eta
\frac{\partial L}{\partial c}
$$

---

## Local vs Global Minima

### Global Minimum
Lowest value of the loss function.

### Local Minimum
A low point that is not the absolute lowest point.
Gradient Descent may converge to a local minimum.

---

## Types of Gradient Descent

| Method | Data Used | Update Frequency |
|----------|----------|----------|
| Batch GD | Entire dataset | Once per epoch |
| SGD | One sample | Every sample |
| Mini-Batch GD | Small batch | Every batch |

### Batch GD
- Stable
- Slow
- High memory usage

### SGD
- Fast updates
- Noisy convergence
- Low memory usage

### Mini-Batch GD
- Most commonly used
- GPU-friendly
- Good balance of speed and stability

#### Convergence
![[Pasted image 20260623095511.png]]

---

## Key Takeaways
- Gradient Descent minimizes loss.
- Move opposite to the gradient.
- Learning rate controls step size.
- Mini-Batch GD is the standard in deep learning.
- Goal is to reduce loss over iterations.
 