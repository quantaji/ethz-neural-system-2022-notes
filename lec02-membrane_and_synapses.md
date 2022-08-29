# A Active Condunctance
## Learning Goals
- What electrophysiology technique help us understand the biophysics of neurons?
    - voltage clamp
- Why is the condunctance a useful concept for understanding active membranes?
    - because condunctance is voltage dependent (and originate from the number of open and closed channel on membrane)
- How do we measure membrane condunctance and their properties?
    - we block the other channel and usd ``g=I/U``
    

## Voltage clamp (VC)
- This is a negative feedback loop to adjust the *membrane potential* to the value you want. It needs *two* electrode, so only possible on the nerve of giant squid.
    - For central neural system, people now use single electrode, a few ms for injection, a few ms for measurement.
    - Notes: in previous experiment, people control by injecting current, or ion concentration. But directly control of voltage decouple variable in H-H model.

## Hodgkin-Huxley model (not taught in class, present here for better intepretation)
- conductance law: ``I=C_{m} \frac{\mathrm{d} V_{m}}{\mathrm{~d} t}+\bar{g}_{\mathrm{K}} n^{4}\left(V_{m}-V_{K}\right)+\bar{g}_{\mathrm{Na}} m^{3} h\left(V_{m}-V_{N a}\right)+\bar{g}_{l}\left(V_{m}-V_{l}\right)``, current = capacity + K channel + Na channel + Leakage channel.
- master equation for ion gate: ``\begin{aligned}&\frac{d n}{d t}=\alpha_{n}\left(V_{m}\right)(1-n)-\beta_{n}\left(V_{m}\right) n \\&\frac{d m}{d t}=\alpha_{m}\left(V_{m}\right)(1-m)-\beta_{m}\left(V_{m}\right) m \\&\frac{d h}{d t}=\alpha_{h}\left(V_{m}\right)(1-h)-\beta_{h}\left(V_{m}\right) h\end{aligned}``
    - Sodium is controled by two different gate, while potassium is only one.
    
- If we control voltage by VC, then ``m,h,n`` have analytical dependence, ``\begin{array}{ll}
m(t)=m_{0}-\left[\left(m_{0}-m_{\infty}\right)\left(1-e^{-t / \tau_{m}}\right)\right] \\
h(t)=h_{0}-\left[\left(h_{0}-h_{\infty}\right)\left(1-e^{-t / \tau_{h}}\right)\right]  \\
n(t)=n_{0}-\left[\left(n_{0}-n_{\infty}\right)\left(1-e^{-t / \tau_{n}}\right)\right] 
\end{array}``, where ``n_{\infty}=\frac{\alpha_{n}}{\left(\alpha_{n}+\beta_{n}\right)}`` and ``\tau_{n}=\frac{1}{\left(\alpha_{n}+\beta_{n}\right)}``
    - For K+ :experiment data shows ``\alpha_{n}=\frac{0.01(V+55)}{1-\exp (-0.1(V+55))}, \beta_{n}=0.125 \exp (-0.0125(V+65))``, turns out to ``n_{\infty}`` increase w.r.t ``V``, while ``\tau_{n}`` decrease. 
        - Since the reversal potential is about ``-88\mathrm{mV}``, the higher ``V``, the more potassium comes out, --> drive ``V`` down to resting potential, this is a negative feed back.
    - For Na+: ``\alpha_{m}=\frac{0.1(V+40)}{1-\exp (-0.1(V+40))}, \beta_{m}=4 \exp (-0.0556(V+65)), \alpha_{h}=0.07 \exp (-0.05(V+65)), \beta_{h}=\frac{1}{1+\exp (-0.1(V+35))}``
        - When ``V`` increases, ``m_{\infty}\to1`` while ``h_{\infty}\to0``, Depolarization causes h to decrease and hyperpolarization causes h to increase. this results in a *transient conductance increase*, which corresponds to the peak
        - Since the reversal potential for Na+ is ``+66\mathrm{mV}``. 

## Voltage clamp experiment

### hyperpolarizing voltage command
- onlu capacitive current, no membrane currents, since all channels are closed.

### depolarizing voltage command
- transient inward current
    - larger voltage commands lead to decreased inward current, this is a *peak* shape w.r.t ``V``.
    - sodium dependent,
        - increase w.r.t. outside sodium concentration
        - if sodium channel blocked by Tetrodotoxin (TTX), no current
    - When fixed ``V``, ``g_{Na}`` (conductance) increase then decrease. (This coincide with the open and close process of Na channel), conductance is calculated by ``I/U``, and the other channel is blocked.
- delayed outward current
    - larger voltage commands lead to increased delayed outward current, this is a steady increase shape w.r.t. ``V``
    - potassium dependent, if potassium channel blocked by Tetraethylammonium (TEA), no current.
    - When fixed ``V``, ``g_{K}`` increase.
- Both Na (peak condunctance) and K conductance dependency is like a sigmoid function, w.r.t ``V``
- Na conductance goes down, two reasons: 
    - 1. potassium also comes in and re-polarize the membrane, 
    - 2. sodium channel inactivate.
- Action potential generation as a dynamic process with both a positive feedback loop (Na), and a negative feedback loop (K). 
    - Because positive feedback loops tend to be unstable, they must have a built-in limiting mechanism (inactivation).

### Refractoriness
- If two spikes of input is very close, the second action potential will be lower.
- Refractoriness is due to the inactivation of sodium channel. It turns on and off, and then it gets tired.  
- 1ms /1kHz is the limitation of sodium channel. Time for recovery.

## Question
- What electrophysiology method is used to study membrane biophysics?
    - voltage clamp
- In what way does the action potential shape change when you increase the extracellular sodium concentration?
    - The action potential goes up.
- What happens when you punch a small hole into a neuron?
    - The threshold is about -50mV, so  a small hole is like a 0mV voltage camp that will keep triggering the neuron to fire until it dies

# B Passive membrane properties
## Leaerning Goals
- What equations describe an axon with passive ion channels (passive cable)?
- How to design a passive cable with far-reaching influence?

## Passive current flow in an axon
- the injected current propagate through axon, with a decay length about 2mm.
- Time dependence is of same shape, but different and decaying magnitude.
    - It is like an RC curve, membrane resistance and membrane capacitance.
- Cole and Curtis's point model ``C_{m} \frac{d V}{d t}=-g\left(V-E_{m}\right)+I_{a p p}``, ``\tau=C_{m} / g``
- The decay is characterized by Kirchhoff's law ``\frac{\partial V}{\partial x}=-j_{i} r_{i}``, then ``\frac{\partial^{2} V}{\partial x^{2}}=\frac{r_{i}}{r_{m}} V``, and ``\lambda=\sqrt{\frac{r_{m}}{r_{i}}}``
    - ``r_m`` membrane resistivity, and ``r_i`` intracellular resistance per unit length.

## Questions
- How would you design an axon with large electrotonic length? (how to make the spactial decay of membrane potential as wide as possible?)
    - Large membrane resistivity, fewer leak channel, or Myelin sheath 
    - small intracellular resistance, a lot ion inside cell.

# C Active membrane properties
## Learning Goals
- How do spikes propagate along an axon?
- Why do spikes in Myelinated axons propagate faster?
    - more channel in Ranvier
    - 

## Action potential propagation
- it is like point case, but model out the axon dimension.
- The signal is directional, meaning it only propagate to one direction, this is due to the refractory of Na+ channel of the other direction.

## Myelination
- Condunctance is higher in Ranvier, and lower in Myelin sheath, Na channels not even distributed.
    - A lot of Na+ channels in the Node of Ranvier, to give lower threshold, less current needed to triger action potential --> faster signal speed 
- compared with unmyelinated axon, signal in myelinated axon "jumps" here and there, this is called *saltatory propagation.*
- unmyelinated axon, squid giant axon, speed: 20 m/s
- myelinated axon, rabbit, 100m/s.

## Question
- If myelination makes signals propagate fasterm why are not all axons myelinated?
    - 1. volume limitation
    - 2. differential calculation like ears, needs slow signal speed to have more significant signal (time difference), delay length

# D Synaptic Transmission
## Learning Goals
- How do electrical synapses work and how are signals at synapses transmitted from the pre-to the postsynaptic cell?
    - ions flow through gap junction channels, causing post synapse action potential
- What is proof of existence of chemical synaptic transmission?
    - Loewi's experiment
- What is the organization and function of chemical synapses?
- What are the defining characteristics of neurotransmitters?
- What are the two main families of neurotransmitters as distinguished by their forms of synthesis?

## Chemical and electrical synapses
- Electrical are usually fixed, 
    - ion flow through *gap junction channels*
        - very small and needs super high resolution to observe with EM.
    - Very synchronised spikes for pre and post synaptic neurons.  (from spike experiment)
        - Hoppfield Network can be originated from this *symmetric connection*.
    - neurons that controls the heart, and release hormons, reliable reaction.
    - earlier existence in evolution.
- chemical is much more complex, Process: 
    1. There is nearly no Ca2+ inside cell at rest
    2. Signal triggers Ca2+ comes into pre synaptic cell -> 
    3. vesicle start fusion --> 
    4. release transmitter (milisecond) --> 
    5. transmitter binding to post synaptic cell's receptor --> 
    6. open or close of postsynaptic channels -->
    7. current cause depolarizing / hyper polarizing membrane --> 
    8. spike --> 
    9. channel close again --> 
    10. vesicle reformation.


## Loewi's experiment
- 1920s, proof of chemical transimission.
- two frog heart share same liquid environment, vagus nerve stimulate to one of the hearts
    --> heart rate goes down. 
    --> another heart start slowing down too after a few second
    --> only chemical transition is possible
- The transmitter is acetylcholine (乙酰胆碱), which controls all muscles. and have sth to do with attention
- 100 type of neurotransmitter


## What characterize/define a neurotransmitter
1. Presence, the chemical should be there, synthesized by body and stored in cell.
2. can be triggered
3. have receptor
- Nitrous oxide is also neuro transmitter


## Small molecule and peptide transmitters
### SMT
- small molecude transmitters
- most abondant type
- The enzymes are synthesized near cell body, in golgi apparatus and dilivered to synapses through axon
    - precursors from previous release are gathered and sythecized by enzymes near synaps
- vesicles are small and therefore light in microscopy

### PT
- peptide transmitters
- transmitters are directly synthesized near cell body, and delivered to dendrite from cell body.
- vesicles are dense/black and big in microscopy

### difference 
- speed is different.
- SMT is fast, 0.5m per day
    - in fast signalling ,move around, listen
- PT is slow, a few mm per day
    - used in changing behavioural state. e,g, female mouse whether to care for their offsprings or eat them 

## Questions
- why are cocaine and alcohol not neurotransmitters?
    - They (1) not present (2)  alcohol, there is no receptor.
- Why do chemical synapses use Ca instead of Na of K for triggering synaptic transmission?
    - Does not mess up with action potential, another degree of freedom for independent control.  The amount of transmittion can be modulated.
- Neuropeptide transmitter are slow to be made available, so what could be their advantage, computationally?
    - More federal, controllable by nuclear. SMT is more self-organizing.

# E Neuromuscular junction -- Example of Chemical transmitter, study of pre synpase in transmission
This is a particular type of synapse that help understanding of general synapses.

## Learning Goals
- Which probabilistic model governs synaptic release?
- How can we visualize synaptic transmission in mid-action?
- What happens with a vesicle after its content has been released?

## End Plate Potentials (EPPs)
- Experiments in 1950s: when you stimulate pre-synaptic cell, and record on post-synaptic potential
    - an action potential in pre side causes sub/super threshold voltage change on post side
    - in central nerv system, this EPP is called evoked postsynaptic potential
    - 40-50mV
## Miniature EPPs
- If there is no presynaptic stimulus --> there is still EPP, called *miniature EPP* (MEPP)
    - possion distributed
    - This is caused by random release of pre-synaptic vesicles? therefore is *Spontaneous*
    - about 1mV
- Both EPPs and MEPPs are sensitive to pharmacological agents that block postsynaptic acetylcholine receptors.
    - PS: therefore proves the cause is by vesicles release
- Practical Meaning for mEPPs
    - when you see something fore a long time, it stays there.
    - But it you block the muscle of your eyes, you become blind. 
    - --> If you really don't move your eyes, you get blind because there is retina application, e.g. get blind when get used to dark env. So every retina cell get used to its brightness
    - This stochastic nature help you not getting blind
## Quantized distribution of EPPs
- Experimentally observed a discrete distribution for <u>amplitude of EPPs</u>, 
    - shows a binomial distribution ``P_{k}=\left(\begin{array}{l}n \\k\end{array}\right) ^{k}(1-p)^{n-k}``
    - k=0 correspond to (1-p)^n, and the decay fits very well.
- Gaussian distribution for MEPP, this is like a single vesicle release.

### Experimentally obsearved fusion of vesicles
- frog muscle, stimulate muscle and then freeze the muscle and free fracture it (take it into slices) -> observe with electromicroscope
    - we can see the crater and calcium vesicle fusing with membrane
    - you can count the number of vesicles released.
- This is proof of synaptic vesicles exocytosis

### 4-AP experiment
- 4-AP this drug widens the action potential, more Ca+ comming in -> more quantile released -> wider range of measurement
- experiment shows more number of quanta released --> more number of vesicle fusing, linear dependency.
## Synaptic vesicles recycling - Experiment of HRP dye
- To prove the idea of endocytosis to release and extocytosis to take it up, HRP is a dye that gives dark color. 
- If you do not stimulate, no dark found inside.
- HRP is found in coated vesicles first, then in endosomes, then in synaptic vesicles. An endosome is a membrane-bound compartment of the membrane transport pathway originating from the trans Golgi membrane.
- Timescale 1 min

## Question
- Which synapses are very deterministic? (assume Triggered transmission >> spontaneous transmission) Hint: for binomial process, mean = ``np``, variance = ``\sigma^2=np(1-p)``
    - p can not be 1. otherwise all vesicles are released. it is not a good idea to release all vesicles, longer time for vescicle replenish.
    - we can make n small, n is the number of <u>available, releasable vesicles</u>.
- What control experiment would you perform to *proof* synaptic vesicle recycling is triggered by presynaptic action potentials?
    - make HRP outside first, and then do not trigger any action potential, after some time, watch the microscopy to see the dye is outside or in vesicles.

# F Synaptic Potential - Study of post synaptic side in transmission
## Learning Goals
- What are gain-of-function and loss-of-function experiments?
    - Example Ca-dependence of synaptic vesicle release.
- What are the transmission characteristics of single ACh synaptic receptors?
- What ions are ACh receptor permissible to?

## Ca dependency for synapses
- If Ca blocked by cadmium (镉), no pre-synaptic calcium current --> no postsynaptic membrane potential. (*loss of function experiments*)
- If directly inject Ca into pre-side, --> depolarization of post-synaptic membrane (*gain of functoin*)
- If add BAPTA (calcium buffer that makes Ca2+ not triggering vesicle to release) --> no post potential (*loss of function*)

## Different release of neuro peptide and SMT 
- low freq -> SMT
- high freq -> corelease of STM and PT

## Patch clamp
- an experiment that can catch single channel current
- shows a randomized quantized current of 2pA.
- A probablistic funciton is smoothed when channel are many. probablitstic -> deterministic.

## Voltage clamp on Post side
- stimulate on pre side, voltage clamp on post side, 
    - to study the influence of postsynaptic potential on end plate currents
- use voltage clamp to very hyper-polarize post side (-110mV), when stimulate pre side, there is still post side stimulus (measured in current (nA)) 
- When other voltage is used, the conductance is nearly the same, 
    - Channels opened by ACh are largely insensitive to membrane voltage, different from Na/K channel that is used for signal transmittion.
    - -> ``𝑔_{𝐴𝐶ℎ} (𝑡)`` is time dependent only, on presynaptic transmitter.
- The reversal potential is about 0mV, for excitatory synapse.
- Changing ion concentration, shows that, Both K Na are involved, also Cl, these channels are not so selective

## Question
- What is the main shortcoming of synaptic weights in artificial neural network models given the biophysics of synaptic currents?
    - ANN response is fixed, BPNN: depend on voltage

# G Excitatory and Inhibitory synapses
## Learning Goal
- What are the two main synapse types of the central nervous system?
- What are signaling pathways (on the postsynaptic site)?

## EPC EPP
- Excitatory postsynaptic currents (EPCs) and excitatory postsynaptic potentials (EPPs).

## Inhibitory postsynaptic potential (IPSP) and EPSP (evoked)
- excitatory: glutamate, ~80%
- inhibitory: GABA. ~20%
- other types are rare, like dopamane
- The reversal potential (when the channel is open) is determined by the cell, and this determines whether the neural is inhibitory or excitatory 
- Therefore, some GABA's reversal potential can be above resting potential 
    - -> although the receptor type is inhibitory, it is still depolarising the cell. But it will never trigger an action potential

## Experiment of Multi synapse connection
- Purpose is to study, how a post cell fire, when it is connected to several differen type of cell.
- A cell is connected to E1, I, E2
- Results is roughly linear
    - E1 or E2, EPSP below threshold
    - E1 + E2: action potential
    - I: IPSP
    - E1 + I: summed
    - E1 + I + E2: summed
- The fourth one, EPSP + IPSP is most prevalent in brain. 
    - Co-tuning of excitation and inhabitation.  principle of brain. 

### Experiment for measuring E/I connectivity
- Use voltage clamp to tune the post synas to excitatory/inhibitory resting potential, so that this type no current. This is a way to measure the average connectivity.
- Results shows that: Nearly all cells are co-tune
    -  -> inhibition is strong when excitation is also strong, roughly balancing each other in the state. 
    -  Reason -> bring the neurons to the edge of chaos. 
    -  A little change will bring large deviation -> nerons can respond rapidly.

## Receptor Type
- *Ligand-gated* ion channels of ionotropic receptor has extracellular site that binds neurotransmitter and membrane-spanning domain that forms ion channel.
- *Metabotropic receptors* affect channel activation via intermediate *G-proteins*, they are also known as G-protein-coupled receptors. 
    - These receptors mediate slow postsynaptic actions ranging up to hours and days. 
- A given transmitter may activate both ionotropic and metabotropic receptors.
- Comparison: M-receptor More flexibility. slightly remote, binds G-protein -> intracellular protin.  
    - This model can be modulated, unlike the previous one Ligand channel, the neuron is just a slave of presynapse

## Question
- Do IPSPs at inhibitory synapses always lead to hyperpolarization?
    - no, if reversal potential (when channel is open?) is above resting potential. then depolarization.
- Do EPSPs at excitatory synapses always lead to depolarization?
    - In practice Yes. but in theory, when synapse is active during the action potential, the membrane voltage is positive, -> bring polarisation to membrane. But this is a small effect. 
- What computational role would you ascribe to a synapse with reversal potential near the resting potential?
    - some synapse is too strong, the conductance is too much, this small voltage can weaken the synapse.
- What computational abilities do metabotropic receptors have that ionotropic receptors do not?
    - IR: only binary state on/off
    - MR: state machine, alpha beta gamma's state. Many hidden state, easily/hardly modifiable. Continual learning, that they can not change memory.