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
Interpretation (HWC Format) : 
- Height = 224
- Width = 224
- Channels = 3
CHW Format(PyTorch model format): Channels x Height x Width.
Why CWH?
	Faster GPU computation, Efficient Memory Layout, Standard PyTorch Convention
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
#### Number of Elements 
Formula : $Height$ x $Width$ x $Channels$ 
#### Total Memory 
$Memory$ = $Elements$×$Bytes Per Element$ 
Example: $150,528×4=602,112$ $bytes$ $\approx 0.57 \text{ MB}$

## Common Datasets 
### MNIST : 
Handwritten digits. Size = `28 x 28` 

### CIFAR-10:
color images. Size = `32 x 32 x 3` 

### ImageNet 
Large-scale image dataset. Common size = `224 × 224 × 3`



## Generating Sequences 
`torch.arrange()` - Creates a sequence of values 

```python
#Example :-
torch.arrange(0,10)

# Custom Step-Size 
torch.arrange(0,10,2) 

# Decimal Step-Size - used for Index generation, sampling, position values
torch.arange(
    start=0.5,
    end=5,
    step=0.5
)
```
## Creating Tensors from Existing Tensors 
#### zeros_like() 
Creates tensor with:-
- Same shape
- all values = 0
Eg, `y=torch.zeros_like(x)` 
eg, 
```python
x = torch.rand(3,4)
y = torch.zeros_like(x)
``` 
```output 
3x4 tensor of zeros 
```


## Data Types 
### Float32 
```python
torch.float32
``` 
Used for : Neural Networks, Continuous values, Gradient Calculations 
```python
torch.tensor(
	[3.0, 6.0, 9.0]
)

#Default 
torch.float32
``` 
### Int64 
```python 
torch.int64
```
Used for : Labels, Integer Indexing 
```python
#Example 
torch.tensor(
	[3, 6, 9]
	dtype = torch.int64
)
```

### Gradient Tracking 
