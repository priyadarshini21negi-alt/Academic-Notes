#review 
## Random Tensor Generation 
Random tensors contain randomly generated values.
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

## Image Tensors 
Images are stored as tensors. 
`image_tensor = torch.rand(224,224,3)` 
Interpretation : 
- Height = 224
- Width = 224
- Channels = 3

#### RGB channels 
color images contain : Red, Green, Blue 
therefore, channels = 3 
#### Why 224 x 224? 
Historical convention from ImageNet 
Many CNN architectures use : 224 x 224 

### Tensor Shape 
given,
```python 
image_tensor.shape
``` 
Output: 
`torch.Size([224,224,3])` 
`
### Extracting Dimensions - Used for image manipulation

```
height,width,channels = image_tensor.shape
```

Result:

```
height = 224
width = 224
channels = 3
``` 

### Total Pixels 
$Pixels$= $Height$ × $Width$

### Tensor Memory Usage 
Every tensor occupies memory 
#### Bytes Per Element
Float32:
`4 bytes` 

### Number of Eleme