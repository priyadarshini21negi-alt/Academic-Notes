#review 
****# TL;DR 
- ultimate goal of neuroscience is to relate all human experience to neural activity. 
- Psychophysics is the essential starting point — it gives you precise, rigorous measurements of perception that can then be linked to neural mechanisms 
- Techniques like 2AFC, psychometric function fitting, and staircase methods allow measurement of sensitivity and bias while controlling for confounds like decision criterion and response bias.

# Def:
- coined by Gustav Fechner in 1860
- Refers to the scientific study of the relationship between physical stimuli and the sensations or perceptions they produce.
- More practically, it means systematically varying stimulus properties and measuring how that affects a person's experience or behavior. 

# Why do Psychophysics? 
## 1. Practical Applications
- Understand human perception helps design better technology.
- Human eye has a "sweet spot" for spatial frequency - most sensitive to medium frequencies.
- psychophysics can tell you whether the extra resolution is even perceivable from a normal viewing distance, since the eye simply can't resolve beyond a certain spatial frequency.
## 2. Understanding Neural Representations 
- precise perceptual measurements let you form theories about how the brain encodes information 
	- ### 2 classic examples :-
		- #### Trichromacy
			- All colours can be mixed from 3 primaries 
			- We have 3 types of cone photoreceptors (S, M, L) with different wavelength sensitivities R G B 
		- #### Webner-Fechner Law 
			- Webner found JND (Just Noticeable Difference - the smallest change you can detect) is always a *constant fraction* of the baseline stimulus, not a constant absolute amount.
			- eg, if the JND for weight is 5%, you can just notice 20g vs 21g, but not 100g vs 101g — you'd need 105g to notice a difference there. 
			- Fechner interpreted this as meaning the brain encodes stimuli *Logarithmically* 
$$
			\text{perceived sensation} = \log(\text{stimulus intensity})
			
$$
			- This is why decibels and musical scales are Logarithmic 
			
# How do to Psychophysics? 
## 1. Task Designs 
- YES/NO DESIGN -
		experimenter presents a stimulus (e.g. a flash of light) and asks "did you see it?" The problem here is the subject's **decision criterion** — how cautious or bold they are about saying "yes."
		A conservative person says yes only when very sure; a gung-ho person says yes at the slightest hint. This shifts the psychometric function left or right, meaning a single measurement can't tell you about true sensitivity — it confounds sensitivity with criterion.
- TWO-INTERVAL FORCED CHOICE (2IFC) :-
		experimenter presents two intervals (one with the stimulus, one without) and asks "which interval had the light?" The subject must choose, eliminating the decision criterion problem entirely. Performance is always 50% at zero signal (pure chance), and rises toward 100% as the signal gets stronger. This gives a clean measure of sensitivity.
- TWO-ALTERNATIVE FORCED CHOICE (2AFC) DISCRIMINATION:-
		Instead of detection from nothing, the subject compares two stimuli and judges which is heavier, brighter, faster, etc. This lets you measure both sensitivity and perceptual bias.

## 2. The Psychometric Function 
This is the S-shaped curve relating stimulus intensity to probability of a correct response. From it you extract two key quantities: 
### 1. Threshold 
The stimulus level at which performance reaches some defined level (commonly 75% or 84% correct). Sensitivity = 1/threshold. A lower threshold means higher sensitivity.
### 2. Point of Subject Equivalence (PSE)
In a discrimination task with a reference stimulus, the PSE is the test stimulus value at which the subject judges both equally likely to be stronger (50% responses each way). 
- If the PSE differs from the actual reference value, there's a perceptual **bias** 
### Just Noticeable Difference (JND) 
horizontal distance from the PSE to the threshold performance level. It represents how much you need to change the stimulus before reliably noticing a difference.

## 3. Methods of Measuring Threshold 
### 1. Method of Constant Stimuli 
Present many trials at several fixed, pre-chosen stimulus levels, collect enough data at each, then fit a curve.
Very reliable but slow and inefficient because many trials are wasted at easy levels where the answer is obvious 

### 2. Staircase Procedure 
Adaptively home in on the threshold: if the subject answers correctly, make the next trial harder; if wrong, make it easier.
The stimulus "walks" towards the threshold and stays near it, making data collection much more efficient.
Con : early errors can throw it off, so averaging several interleaved staircases is recommended. 

