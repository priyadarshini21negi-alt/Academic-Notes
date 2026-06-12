#review 
## Random Tensor Generation 
### [[Uniform Random Distribution]] 
`torch.rand()` : generates tensors with values sampled from a Uniform Distribution over the interval $[0,1)$ :
Mathematical Representation : $X$ ~ $U(0,1)$  
#### Properties:-
- Probability density function: $f(x)=1$ for $x \in [0,1)$
- Mean $\mu = \frac{a+b}{2}=0.5$  
- Standard Deviation $\sigma = \frac{b-a}{\sqrt{12}}$
- For \(U(0,1)\):  
  
$$  
\sigma = \frac{1}{\sqrt{12}}  
\approx 0.2887  
$$

  
For $U(0,1)$:
```python
# 3X4 matrix with random values
random_tensor = torch.rand(size=(3,4)) 
#shape

#minimum value
print(f"{torch.min(random_tensor).item():.6f}")
#max
print(f"{torch.max(random_tensor).item():.6f}")
#mean
print(f"{torch.mean(random_tensor).item():.6f}")
#Std deviation
print(f"{torch.std(random_tensor).item():.6f}")
```
