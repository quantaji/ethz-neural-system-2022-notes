# A Short term synaptic plasticity
## Learning Goals
- How rapidly can synaptic strength vary?
- What is the effect of extracellular Ca concentration on synaptic dynamics?

## Facilitation, Augmentation, Depression, Potentiation
### Facilitation
- Facilitation is the increase in evoked postsynaptic potential (EPSP) during paired action potential stimulation.
    - a few miliseconds interval
- Experiment find same pre action potential pair, second post action potential is higher
    - One mechanism of facilitation depends on Calcium (that is still present due to the first action potential). More Calcium means more vesicles are released.
- Longger interval, less EPSP increase.

### Augmentation, Depression in one Experiment
- Experiment: given a train of spikes on pre side (also known as *tetanus*)
    - under normal Ca2+, EPSP shows a strong and fast *depression*
        - because of the depletion of vesicles
    - intermediate Ca2+, slows down the process of vescicle release: shows depression and *augmentation*
    - 0.1 normal Ca2+, further slow down, shows only augmentation, (and at very beginning, facilitation)
- augmentation is at timescale of a few seconds

### Post-tetanic Potentiation (PTP)
- as its name suggest, given a train of spikes (tetanus), after that, the response to a single spike is also increased
- time scale 30s - mintues
- PS: for plasticity, long term stands for  (> ~1h), short term < 0.5h

## Case Study of Applysia, behavioral plasticity: habituation and sensitization
- two part of Applysia, gill and siphon
- A gill is a respiratory organ found in many aquatic organisms that extracts dissolved oxygen from water and excretes carbon dioxide.
- A siphon (Ancient greek: "pipe, tube") is a tube-shaped organ through which water flows.
    - If we touch the siphon, gill will contract, controlled by *abdominal ganglion*
    - If we keep touching, contractless, this behavior is called *habituation*
- If we shock the applysia's tail, while touching, the contraction will recovery
    - this is *sensitization*, (short term)
- Sensitization last for about 1h, if we train the applysia 4times a day for 4 days, we get longer sensitization like a week (long term)
- The neural circuit in the slide shows how it works, 
    - The synapse of the sensory siphon neuron onto the motor neuron is where the action happens, habituation and (modulatory neuron onto senser synaptes leads to) sensitization.
- Modulatory interneuron release *serotonin*, which lead to sensitisation and to recruiting more neuron
    - serotonin, bind to G-Protein -> overall makes potassuim channel less effective --> membrane voltage is longer depolarized --> more Ca+ influx comes in.
- Long-term sensitization underlies changes in gene expression.
    - This may explain the behavior that someone get overly shocked by small stimulus. wrong stress response to small trigger.

## Questions
- What is the evidence of short-term synaptic plasticity underlying changes in behavior?
    - Applysia experiments show the link between plasticity level and behavior level.
- What could be the computational function of short-term forms of synaptic plasticity?
    - Like a high-pass filter, that enables transient responts, or fast adaptation. creating dynamics or motor patterns

# Long Term Synaptic Plasticity
## Learning Goals
- What structural changes happen at the postsynaptic site when excitatory synapses weaken or strengthen long term?
- What are silent synapses?
- What form of synaptic plasticity imprints the temporal ordering of neural activity?

## Gene Experiment on Fly
- give an animal poisonous red seed, then they will never eat red seeds. Just single one seed is enough for maintain memory for longtime. 
    - This is a perfect trial for long term memory
- mutation leads to failure in learning this, meaning Long Term Plasticity is gene involved.

## LTP Study in Hippocampus
- Hippocampus is where new memory are formed, ideal for plasticity study.
- Study of two CA3 cell connect to same CA1 cell, we can stimulate on either of CA3 and record the postsynaptic responce on CA1
- tetanus to pathway 1 leads to EPSP in pathway 1 (long term potentiation *LTP*), but not in pathway 2 (*specific*).
    - LTP can be as long as a year
- Long Term Potentiation (LTP) can also be triggered by pairing of pre- and postsynaptic activity. (*assiciative*) 
    - This means instead of tetanus, 2-3times per minute single pulse, and at the same time, we deploarized the CA1 post membrane potential.
    - This corresponds to the *Hebbian learning rule*, Fire together wire together
- These experiments shows LTP is both specific and associative.
    - (A) Strong activity initiates LTP at active synapse is without initiating LTP at nearby inactive synapses.
    - (B) Weak stimulation of pathway 2 alone does not trigger LTP, but in conjunction with strong stimulation of pathway 1 it does. 
        - Pathway 1 makes CA1 also depolarized.

## NMDA and AMDA for Long Term Potentiation (LTP)
- both are iontroppic receptor (simple receptor). 
- The NMDA channel is permeable to Ca 2+ but is blocked by physiological Mg2+  
    - NMDA have Mg2+ sitting on it, blocking it. Mg2+ is released when postsynaptics is depolarised. When Ca2+ comes in --> some protein process --> insertion of AMPA --> LTP
- Usually, Ca2+ does not come into post-synaptic side, but NMDA does.
    -  calcium is a key ion player both on the pre-and postsynaptic sides.
-  The NMDA receptor behaves like a molecular coincidence detector (coincidence between glutamate and postsynaptic depolarization).
-  LTP is expressed by postsynaptic protein kinases which lead to AMPA receptor insertion.
    - Mg2+ unblocked --> Ca2+ inside --> induce more AMPA to be present at membrane --> more conductivity --> silent synapse become non-silent

### Visualization of AMPA insertion
- experiment: put glutamate everywhere in the solution and use laser to uncage it (glutamate gets free from binding from one molecule) you can visualise where the glutamate receptors are.
    - LTP --> more AMPA receptor --> more glutamate nearby 
- *Silent synapse/neuron*: The silence is not because ``V_{res} \approx V_{rev}``, it is caused by the block of Ma2+
- LTP can induce AMP for silent synapse, turn it into active
- from a figure in slides, you can see along the dendrite, there are silent receptors everywhere waiting to get involved in learning.
- in juveniles rats (10 days old), AMPA receptors are largely absent. Receptors have been immunolabelled.
    - while In adult (5 weeks old) rats, many synapses contain both AMPA and NMDA receptors
- similar for human, in 2 years old, kids have the most number of synaptic connectivities. born-> no connect -> 2y maximum --> after, pruning (which is another mechanism)
- LTP maintainess requires protein synthesis, otherwise, LTP can be forgoted.
    - This synthesize pathway shows that LTP also requires gene expression (CREB gene).
- LTP can also induces new spines. (changes the shape of neuron)

## Long-term depression (LTD) 
- LTD can be induced by prolonged 1 Hz (low-frequency) stimulation.
- LTD is due to AMPA internalization.
- The dividing line between LTP and LTD is set by the Ca 2+ concentration: 
    - Small and slow rises of Ca 2+ lead to depression, 
    - whereas large and fast Ca 2+ lead to potentiation. 
- => Bienenstock-Cooper-Munro (BCM) learning rule. ``y =\sum_{i} w_{i} x_{i}, \frac{d w_{i}}{d t} =y(y-\theta) x_{i}-\epsilon w_{i}``, ``y`` post activity, ``x`` pre activity, ``w`` synaptic weight
    - y have positive effect only above a threshold, zero y gives no effect. This explains the term.
    - deviation from gaussian
- LTD is found in cerebellum (function for fine motor control of voluntary movements.), 
    - in hippocampus stimulus leads to potentiation, 
    - while in  cerebellum leads to depression. Depends on neurontype this is not universal
- Experiment found Pairing the stimulation of climbing fibers (CF) and parallel fibers (PF) causes LTD that reduces the parallel fiber EPSC.
- Glutamate release by parallel fibers activates both AMPA receptors and metabotropic glutamate receptors. 
    - Increased Ca 2+ from climbing-fiber induced depolarization here has the opposite effect of leading to internalization of postsynaptic AMPA receptors and to weakening of the parallel fiber synapse.

## Spike-Time dependent synaptic plasticity (STDP)
- when pre is after post -> you get long term depression!!!
- when pre is before post firing -> LTP
    - This Anti-Hebbian part might be good for distangle causal signal.
- STDP is modulated by dopamine

## Questions
- Could (i) post-tetanic potentiation and (ii) *LTP caused by pairing pre-and postsynaptic activity* is subserved by the same mechanism?
    - Yes. Post synapse depolarisation is probably caused by pre fires so much
- Is the spike time-dependent form of synaptic plasticity in agreement with Hebb's postulate?
    - Comparable but not identical. Pre after Post gives depression is not predicted by Hebb's law