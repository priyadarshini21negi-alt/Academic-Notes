---
sr-due: 2026-08-22
sr-interval: 1
sr-ease: 230
---

# 1. Single unit electrophysiology

## lecture material :-
   Single-unit recording involves sampling the activity of single neurons, or small clusters of neurons, using an array of microelectrodes implanted in the brain.
- Metal electrodes are used to record the spiking activity (action potential ) from single units.
- An electrode introduced into the brain of  living animals, can record the electrical activity happening near the tip of the electrode.
- If the tip  is placed near to a single neuron extracellularly , then we get single unit recording
- The difference in potential in the extracellular space of a neuron with reference to the ground is measured.
- The recorded action potentials are similar to the action potentials of a cell , but they are much smaller .
- Microelectrodes are very fine wires made of tungsten or platinum-iridium alloys that are insulated except at the tip of the electrode.
-   When there are more neurons near the electrode tip, there would be another set of spiking information(different shape or different time ) would also be present in the data
- With spike sorting techniques, we can differentiate the spiking activity of different neurons .
- The recordings could be from dendrites, multiple neurons or axons , since we are not sure about the placement of electrodes. The electrode may or may not capture the spiking activity or a single neuron or more number of neurons, but very limited.


## Questions
#### Q. What physical quantity does an extracellular microelectrode measure, and what does it reflect?
It measures the **potential difference in the extracellular space relative to ground**, which reflects the transmembrane currents generated during nearby neuronal spiking.
#### Q. Why are the recorded action potentials smaller than the action potentials measured inside a neuron?
Because the electrode is outside the neuron and is measuring the electrical signal indirectly through the extracellular space.

#### Q. Why can a single electrode record activity from multiple neurons?
Because the electrode detects electrical activity occurring near its tip, so nearby neurons can contribute their own spike signals to the recording.

#### Q. What is spike sorting, and why is it necessary in extracellular recordings??
Through **spike sorting**, which separates recorded spikes based on their characteristics so they can be attributed to different neurons.

#### Q. Why can't we assume an extracellular signal comes from a single soma, and what are the resulting limitations
Because the electrode tip blindly samples any nearby source—including axons, dendrites, or multiple adjacent cell bodies. As a result, it cannot provide exact anatomical localization, cell morphology, or definite single-cell isolation without post-processing.

#### Q. How does the physical construction of a microelectrode restrict its recording to a local region?
The microelectrode wire is fully insulated along its shaft and exposed only at the conductive tip (tungsten or platinum-iridium), preventing electrical pickup everywhere except the immediate extracellular volume around the tip.



# ---
# 2. Multiple channel electrodes

## lecture material
![[Pasted image 20260816125527.png]]

- Neuronal Population = a group of neurons considered together
## Conceptual Questions
### Multiple channel recording
#### Q. Why is recording from multiple neurons useful in electrophysiology experiments?
It allows researchers to study the **activity of a population of neurons simultaneously** rather than focusing on only one neuron.

#### Q. What are the limitations/drawbacks of multiple-channel recordings?
damage to brain tissue and require more recovery time.
### LFP
#### Q. How is a raw extracellular recording separated into spikes versus LFPs, and what frequency profile does each represent?
via **frequency filtering** (cutoff at ~200–300 Hz). The **high-frequency** band ($> 300\text{ Hz}$) isolates action potentials (spikes), while the **low-frequency** band ($< 200\text{–}300\text{ Hz}$) isolates Local Field Potentials (LFPs).

#### Q. Which signal characteristics are used to separate overlapping action potential during spike sorting?
Differences in waveform shape (amplitude, duration/width) and timing/firing patterns.
#### Q. How are LFP different from [[action potentials]] ?
LFP is the **low-frequency part of the extracellular signal**, reflecting activity in the local neural population. 
while action potentials are the **high-frequency signals associated with neuronal spiking**
#### Q. What biophysical process generates the Local Field Potential?
**Transient ionic imbalances** in extracellular space caused by collective cellular electrical activity

#### Q. How do 
# ---
# 3. Patch Clamp Technique
## Lecture notes
![[Pasted image 20260816132642.png]]
**Extracellular ($V_{\text{out}}$)** is the electrical potential in the fluid **outside** the cell membrane (in the surrounding tissue or bath solution).
**Intracellular ($V_{\text{in}}$)** is the electrical potential in the **cytoplasm/interior fluid** of the cell. It does not specifically target the nucleus; the whole intracellular fluid acts as a conductive medium.

Think of the cell membrane like an insulating wall separating two conductive pools of salt water:

- **Outside Pool:** Extracellular fluid ($V_{\text{out}}$).
    
- **Inside Pool:** Intracellular cytoplasm ($V_{\text{in}}$).
    
- **The Membrane:** The lipid barrier between them.


The **transmembrane potential** ($V_{\text{m}}$) is simply the difference in electrical charge across that thin membrane wall.

In a patch-clamp experiment, the glass pipette makes contact with the membrane and gains electrical access to the inside pool ($V_{\text{in}}$), while a reference electrode sits in the outside pool ($V_{\text{out}}$), directly measuring the voltage drop across the membrane barrier.
## Questions

#### Q. What physical quantity does whole-cell patch-clamp record, and how does it differ from extracellular recording? 
It directly measures the **transmembrane voltage difference** ($V_{\text{out}} - V_{\text{in}}$) across the membrane of a single neuron, rather than the indirect extracellular field potentials.
#### Q. What is the operational difference between Voltage Clamp and Current Clamp? 
- **Voltage Clamp:** Membrane **voltage is held constant** to measure the **current** flowing through ion channels.
    
- **Current Clamp:** Injected **current is held constant** to measure changes in membrane **voltage** (such as action potentials).

#### Q. What is the major experimental limitation of patch-clamp electrophysiology?
It is mechanically fragile; physical movement easily breaks the pipette-membrane seal, making it extremely difficult in awake, moving animals or humans.


# ---

# 4. Calcium imaging
## Lecture notes
![[Pasted image 20260816132725.png]]

## Questions
#### Q. What biophysical event does calcium imaging track to infer neural activity, and how does it work?
It tracks the **intracellular influx of $\text{Ca}^{2+}$ ions (calcium transients)** that occurs during action potentials, using fluorescent indicators (such as GCaMP or dye fluorophores) that emit light when bound to calcium.

#### Q. What major advantages does calcium imaging offer over traditional electrophysiology? 
- **Cell-type specificity:** Genetic targeting allows labeling of distinct subpopulations (e.g., VIP, SOM, PV neurons).
    
- **Structural context:** Resolves neuronal morphology, spatial organization, and microcircuit connectivity.
    
- **Population scale:** Simultaneously records optical signals from hundreds to thousands of individual neurons ($100\text{–}1000$).

#### Q. What is the primary physical limitation of two-photon calcium imaging?
**Limited recording depth**,
caused by light scattering and tissue absorption, which restricts imaging to superficial layers of the cortex




#
<hr>

#review
