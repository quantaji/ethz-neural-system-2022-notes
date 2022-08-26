# A Introduction

## Learning Goals
- In what way do brains relate to intelligence?
    - control muscle -> do behavior, or say, implement algoirthm.
- What 2 basic cells types is the brain composed of?
    - Neurons and Glial
- What are the compartments of a neuron and how do we visualize them?
    - dendrite, axon, soma, etc.
    - electrical microscopy, fluorescent microscopy
- what are the synapses and how can we recognized them?
    - The synapse is a junction between two nerve cells, consisting of a minute gap across which impulses pass by diffusion of a neurotransmitter.
    - Synapses are characterized by the co-localization of a postsynaptic density and synaptic vesicles.
## Brain
- Neural systems are composed of a body with sensors and actuators, and a brain. The goal of neural systems is to produce behavior. To understand neural systems we must research the behavioral algorithms and their implementations in terms of the brain’s neurobiology.

- the number of genes does not seem to be the critical factor for determining the complexity of an organism, with the potato having about 60% more genes a human.
- The number of neurons gets us closer to reflecting the level of intelligence of an organism. (Yet, some whales have twice as many neurons as humans do)
- The heaviest brain is that of the sperm whale, weighing about 8 kg. Humans stand out in terms of the size of their brain relative to their body weight. The human brain weighs only about 2% of body weight, but it consumes about 20% of energy.
## Neuron compartements
- *Mitochondria* (线粒体): energy
- *Ribosome* (核糖体): binds mRNA tRNA to synthesize polypeptides and proteins.
- The *golgi apparatus* (高尔基体): secretion and intracellular transport.
- *nucleus* (细胞核): chromosomes, DNA
- *endoplasmic reticulum* (内质网): has ribosomes attached, protein and lipid synthesis.
- *dendrite* (树突): Neuron signal input
- The *axon* (轴突): neuron signal output
- *Myelin* (髓磷脂): To increase the speed of electrical signal.

A human has 100 billion (10^11) neurons and 10^15 synapses.
- The synapse is a junction between two nerve cells, consisting of a minute gap across which impulses pass by diffusion of a neurotransmitter. 
    - Synapses are characterized by the co-localization of a postsynaptic density and synaptic vesicles.
    - The postsynaptic density (PSD) is a protein dense specialization attached to the postsynaptic membrane.

## Neuro Transmitter
- amino acid
    - excitatory: glutamate (谷氨酸)
    - inhibitory transmitter: GABA (γ-氨基丁酸)
- monoamines transmitter (单胺类神经递质):
    - dopamine (多巴胺), norepinephrine (去甲肾上腺素), serotonine (血清素), histamine (组胺)
- endocannabinoids (內源性大麻素)
- opioids (阿片类)

## Method of visualization
bind reporter gene (flourescent protein) after  promoter of DNA

## Glia (神经胶质细胞)
- Astrocytes or astroglia: nutrition, ion balance and repair.
- Oligodendrocytes: production of myelin sheath
- Microglial: for immune of brain

## Question
- What are the advantages/disadvantages of light and election microscopy for visualizing neurons?
    - Pros:
        1. high resolution
        2. labels everything 
    - Cons:
        3. not super specific, cannot label certain protein, do targeting 
        4. cannot target certain protein
        5. massive data to be processed. 

# B Systems and Computational Neuroscience
## Learning Goals
- What is a 'neural mechanism'?
    - Given behaviour, describe the behaviour and explain it with neural circuit. 
- How does a simple reflex work
- What signals are convey by a neuron?
    - spikes
- what is a receptive field?
    - The receptive field, or sensory space, is a delimited medium where some physiological stimuli can evoke a sensory neuronal response.

    
## Knee-jerk reflex
- Two types of neurons underlie the generation of the knee jerk reflex. 
    - Afferent neurons carry signals from the periphery toward the brain, and 
    - efferent neurons away from the brain. 
- The simple neural circuit they form with the stretch receptors and the muscles, together with their timed activation, is the ‘neural mechanism’ of the myotatic reflex.
- Systems neuroscience studies the structure and function of neural circuits and systems.
- The responses elicited in extensor and flexor motor neurons are different, in support of an extending leg movement. 
    - brain is wired up not just the contract the muscle of interest, but also to relax the antagonistic muscle on the other side of the joint.

## Action Potential 
- An action potential is a short-lasting event in which the electrical membrane potential of a cell rapidly rises and falls, following a consistent trajectory.

## Receptive field
- The receptive field, or sensory space, is a delimited medium where some physiological stimuli can evoke a sensory neuronal response.
    - a stimulus in the center elicits an increase in neural firing and a stimulus in the surround a decrease,

## Computational Neuroscience
- Computational Neuroscience mathematical model, theoretical analysis, to understand the principles that govern development, structure, physiology and cognitive abilites of nerve system.
    - single neuron (bio-phy) -- sensory processing, motor control -- memory and synaptic plasticity -- neural population behavior (encoding decoding) -- cognition -- network models

## Questions
- What does neural circuit of a relex tell us, that goes beyond evidence of muscle contraction?
    - muscle relaxation. The reflex really wants to generate the movement. If two muscle on each side are both contracted, no movement.
- Why is computational neuroscience important
    - modern machine learning come from neuroscience....?. cs has wrong idea, two-layer can do anything, but the brain is multi-layer
    - to assist experiment, understand healthy brain, and what goes wrong in disease. experiment is impossible and prohibited in some country.



# C Electrical Signals of nerve cells
## Learning Goals
- Why do neurons have a negative resting potential?
    - concentration gradient of ions
- What do neurons and batteries have in common?
    - concentration difference for several type of ion
- What is an action potential?
    - injection current --> threshold --> burst
    - An action potential is a short-lasting event in which the electrical membrane potential of a cell rapidly rises and falls, following a consistent trajectory.
- What is the input-output characteristic of a neuron?
    - Non-Linear, ReLU like.

## Type of neural signal
- Action potential
- receptor potential (analog?)
- synaptic potential (stimulus on pre, signal on post)

## Experiment done by Hodgkin-Huxley, injection of current.
- negative current, and part of current below threshold leads to passive response (RC curve)
- Threshold is about -50 mV, resting potential is about -65 mV.
- more current, more frequent action potential
    - ReLU like function

## Experiment of changing outside ion potential
- The resting potential is caused by concentration gradient, which is the result of semi-permeable membrane, like *batteries*, ``E_{m}=\frac{k_{B} T}{e} \ln \left(\frac{\sum_{i=1}^{N} P_{M_{i}^{+}}\left[M_{i}^{+}\right]_{\text {out }}+\sum_{i=1}^{N} P_{A_{j}^{-}}\left[A_{j}^{-}\right]_{\text {in }}}{\sum_{i=1}^{N} P_{M_{i}^{+}}\left[M_{i}^{+}\right]_{\text {in }}+\sum_{i=1}^{N} P_{A_{j}^{-}}\left[A_{j}^{-}\right]_{\text {out }}}\right)``, where ``P`` is the permiability of certain ion, and ``[\cdot]_{-/+}`` is ion concentration.
    - for single ion, this turns to Nernst equilibrium potential ``\frac{k_{B} T}{e} \log \frac{\left[\mathrm{K}^{+}\right]_{2}}{\left[\mathrm{~K}^{+}\right]_{1}}``
    - ``\left[\mathrm{K}^{+}\right]_{\text{in}} \gg \left[\mathrm{~K}^{+}\right]_{\text{out}}``
    - ``\left[\mathrm{Na}^{+}\right]_{\text{in}} \ll \left[\mathrm{~Na}^{+}\right]_{\text{out}}``
- The *resting potential* depends mainly on the extracellular potassium concentration, nearly no dependence on sodium.
    - The slop for ``E`` w.r.t ``\log [\mathrm{K}^{+}]_{\mathrm{out}}`` is nearly ``\frac{k_{B} T}{e}=58\mathrm{mV}``
    - The deviation for this linear dependence is due to the voltage dependence of conductance.
- The amplitude for *action potential* (*positive reversal potential*) depends mainly on sodium ``\mathrm{Na}^{+}``
    - the slop for positive reversal potential w.r.t ``\log [\mathrm{Na}^{+}]_{\mathrm{out}}`` is also nearly ``58\mathrm{mV}``, the deviation also due to conductance's voltage dependency.
- Shape of action potential pattern depends on the function of neurons. The shape modulates the Calcium. 

## Questions
- What simple nonlinearity describes the input-output relationship of a neuron?
    - ReLU, (but the freq will saturate at some time, when current is large, but the brain tries to avoid these regions), Linear-Non-linear regime.
- Why do neurons exhibit actoin potentials?
    - Not all animals have action potential. Worms have no action potential. Action potential is an active process to transmit signal through *large distance*.