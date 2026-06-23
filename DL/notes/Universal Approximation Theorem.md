 
 > Why can neural networks solve problems that linear regression cannot? 
 > 
	**Because neural networks use nonlinear activation functions (ReLU, sigmoid, tanh, etc.), which allow them to create curved and complex shapes instead of only straight lines.**

A neural network with **just one hidden layer** and **enough neurons** can approximate almost any continuous function as closely as you want. 

### Formal Definition : 
![[Pasted image 20260623093902.png]]

> If you give me enough neurons, I can make my neural network's curve look almost identical to your target curve. 


### Theorem
"There exists a path to the treasure."
### Training
"Can you actually find the path?"

*Two different questions.*
*UAT only answers the first one.*


# Summary : Important Points 
- [[Linear Regression]] can only learn linear relationships.
- [[Neural networks]] use activation functions to introduce nonlinearity.
- Without activations, a deep network is just a linear model.
- Universal Approximation Theorem says a single hidden-layer neural network with enough neurons can approximate any continuous function on a bounded domain.
- The theorem guarantees representational capacity, not successful training.
- Deep networks are used because they are more efficient than extremely wide shallow networks. 

#review
