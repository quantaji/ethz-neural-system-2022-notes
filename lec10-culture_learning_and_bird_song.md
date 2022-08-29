# A Cultural and Statistical Learning
## Learning Goals
- The central assumption of evolutionary theory
- The main distinction between humans and animals
- Benefits and pitfalls of learning from observation
- The double-U curve of generalization in artificial systems

## How does human different from monkey?
- The central assumption of evolutionary is that life only merge once 
- Humans and apes have common ancestors
- The most significant difference for human and apes is: *nonhuman primates (monkeys, orangutans, chimpanzees, etc) cannot imitate actions*
    - Only difference is cumulative culture, what others do before, we can build on that
    - most primalogist thinks monkeys cannot imitate. maybe the monkey just see the fish and stick and  invent the method again
- This can be tested: the most strict definition: teach some thing that normally the monkey will not do.
- What animals can imitate: Songbirds, hummingbirds, parrots, cetaceans, bats, elephants.

### Experimental proof of monkey cannot imitate
- Setting: box, a hole in it, there are nuts in it (rewards). 
- it was closed, if you do some strange action, you will be able to open it, (this is natually not related to opening the box), like a riddle
- most children did action, they over-imitate useless action, 
    - we imitate for the sake of imitate, what's behind is for later to understand
- but non of monkey did.
    - If there is no obvious relation with outcome, monkeys dont do
- Actually there are 2 actions that require the kids to do, some can do both, some can do one, and some do nothing, but for monkey, it is nothing.

## How do we transmit culture? learning from experience v.s. learning from observation
- how can you teach child no to put knife in your mouth? 1. say no (hard for kids to understand) 2. show the child --> let kids to imitate

### Bird song experiment
- Bird are played with syllables (recorded from other birds), S1-S10
    - S1-S5 are short, no airpuff after the pitch
    - S6 - S10 are longer, and we train/reinforce the bird to be blowed by airpuff, negative feedback, to ask the bird to leave.  
- How do we test generalization?
    - Just same stimuli, but taken from another day (sung by another bird, maybe a different version).
    - after training, the bird leave before the puff come, given the "leaving" stimuli

- two way to learn, learn from experienec: whether to experience airpuff. learn from observation: see other bird's reaction
- After we get a well-trained bird, we let the observer watch the trained bird
    - the observer instantaneouly learn what to do. 
    - PS: This faster learning might be cause you already have experience, no need for trial and error.
- but what is interesting, is that observer generalize poorly. --> benefit for experiencing

### Statistical Learning theory
- The experiment result can be linked to overfitting and underfitting
- *imitation* correspond to the *overfitting* regime, where we can exactly fit the learn pitch, but poor on generalized pitch
- learn by experiencing corresponds to the optimial regime, the airpuff (and the underlining brain circuit) act as a regularization)
- Teach gives examples for L1 regularization, which can be seen as pruning the network, to reduce model/network complexity.

### The double U in DL era
- when we further increase model complexity, the generalization further goes better, giving the double U curve
- I heard it is because implicit regularization
- The teacher believe, in overfitting regime, when you train further, you are actually finding some optimial representation for your model, how you can deal with it faster, etc.

## Categorical Perception
- young infants can distinguish any consonants, but this  ability disappears in one year

## Question
- Can you provide an intuitive understanding of the double-U curve of generalization?
    - implicit regularization?
- What is a good test of the capacity for action imitation?
    - using uncommon actions, 
- If songbirds have the capacity of action imitation, why do they not have cumulative culture?
    - songs does not have meanings, language is the solution
- Should we think of categorical perception as learning or unlearning?
    - Unlearning.

# B Birdsong Development
## Learning Goals
- Parallels between birdsong and speech learning
- Dependence of learning outcome on social context
- How to measure performance errors during song learning
- Linear assignment (optimal transport) of performance error
- Link between birdsong and natural language processing

## Zebra finch
- Experiment bird, because they sing all year
- Female does not sing, but they can.
- 71% of birds species, female can sing
- Song is part of the courtship display 
    - Female likes complex syllables, but the patch should be consistent, meaning it should be the same very time.

### different phase of learning
- hatch - 60 days: sensory phase: store a memory (template) of tutor song
- 30-90days: sensorimotor phase: practice their own songs to arrive at a good copy of the template
- 90days+: crystlized
- In sensory motor phase, 
    - begins with *subsong*, characterized by the production of highly variable individual song notes and note sequences.
    - then *plastic* song, where individual song notes and note sequences become less variable.
    - finches reach adulthood, individual notes and note sequences become *stereotyped*.
- The song is very steotyped, can be nearly the same between 1 year

### Song learning require tutor and feedback
- Experiment shows if the bird is isolated (no tutor) it produce long syllable, not steotyled: this means bird needs another bird to sing correctly
- If the bird is deaf, the sound is non-structured, prove that it needs to hear from itself.
- From the first day the bird starts singing, it does not need to hear from others any more, you can remove the tutor. In sensory motor phase, it uses the memories it create in sensory phase. It is like a template-matching process.

### De novo(new) establishment of wild-type song culture
- Experiment: a colony of birds, never heard a sound. We take the bird from the colony, raised them in separate boxed, and when they are adults, put them together.
- Then we look at their offspring, when the offspring turns adult. to study how does this culture of singing emerge in generattions.
- result shows random syllables turns into regularized songs after generations.
- a long iregular syllable turns into normal syllable, shorten the syllable -> steotyle the syllable.
- Bird songs have stable attractor

### Vocal imitation in zebra finches is inversely related to model abundance
- Birds are given motif of songs, of differen amount. The more they listen, the less they learn.

## How do we compute vocal performance error?
- Problem fomulation: The change in syllables, how to explain. Is this part come from that part? (this kind of question)
- How does the young bird assign error to part of the syllable

### Serial tutoring paradigm
- Serial tutoring paradigm: when they understand, teach them new songs, and see what the vocals are adapted to.
    - e.g. first teach them a source AAA, then teach them ABABAB, and see how they adapt to new pitch
- The correction contains two part: *Syntax error* (the vocabulary is the same but ordering changed) and *pitch error* (new pitch)

### Correction of syntax error (sequence error)
- Example, Source: ABC, target: ACB
- Turns out for birds, they need to learn three new transition: AC, CB, BA, 
    - originally, you know AB, BC, CA
- Only when the three transition are learned (experimentally observed increase frequence for the three new transition), the bird will sing the new song

#### correspondence in infant
- Experiments finds: Incorporation of new syllables into infants’ babbling utterances.
    - initially, the infant only can produce "Da", so it produce combination of "Da-Da"
    - but when it learns "Ga", "Da-Ga" starts to appear in the combination
- When a new syllable appears, the infants make not too much novel transition, but as time goes on, this novel transition goes up.
- This shows that Chrildren do not invent all syllables at the same time,
    -  --> e.g. german 'r' very difficult
    -  This means when they learn a new syllable, they will try it will all other syllable (in terms of transition)
    -  Insight: The ablility for our language to combine sounds may not be the strategy of learning, but the outcome of learning.

### Correction of Pitch Error (Spectual error)
- Source : ABAB, Target: AB'AB', B' have higher/lower frequency
- The bird assign error to pitch

#### When one source syllable is replaced by two targets, birds do not ‘bifurcate syllables’
- Source: ABAB, Target: AB+AB-
- The bird does not change first to B+ and second to B- (bifurcation)
- what it does it If turns to B-, then the bird learns separately B+ (*call*), then try to learn transition of A-> B+
- Further experiment shows Bird will either let B go to B- or B+, but they will never go to two call or two target

### Combination of Pitch and Syntax error
- This is a Quadratic assignment problem, which is NP hard
- ``E(\mathrm{~S}, \Delta)=\underbrace{\sum_{i, j} e\left(S_{j}, T_{i}\right) \delta_{i, j}}_{\text {phonology }}+c \underbrace{\sum_{i j}^{n m} \sum_{k \neq \mid j+1]}^{m} \delta_{i, j} \delta_{[i+1], k}}_{\text {syntax }}``
    - how to assign a syllable to a target ``\delta_{i j} \in\{0,1\}``

#### Experiment result of birds
- Source: ABC, Target: AC'B
- Three possible way:
    1. Drop B and C put other things like A$% -> AC'B
    2. ABC -> ABC' -> AC'B
    3. ABC -> ACB -> AC'B
- This is what bird actually do: ABC -> ABC' -> AC'B
- *They first correct pitch error, then correct syntax error*.

#### Context does not bias pitch error assignment
- Source ABC, Target: AB-C+
- Most efficient is to change B -> B- and then invent B+
    - but half of birds choose b -> B+
    - Seems that the birds first deal with it as if they are completely blind/deaf to the order

#### Pitch error assignment is not random but greedy
- Souce: ABCB+1, target: AB+2CB-1
- We want to test whether bird prefer to go for 
    - the right context (B-> B+2, B+1 -> B-1)
    - the closes match in semitune (B-> B-1, B+1 -> B+2)
- result shows that prefer closest match in semitune (pitch error greedy)

#### Linear Assignment Problem
- What the bird does is a linear assignment problem, they ombit the syntax error term first (ignore the quadratic term in the error assignment problem), only deal with pitch error, then solve the syntax error lateron
- ``\Delta^{*}=\arg \min _{\Delta} \sum_{i, j}\left\|S_{j}-T_{i}\right\| \delta_{i, j} \quad \delta_{i j} \in\{0,1\}``, and for syllables ``\sum_{j} \delta_{i j} \leq 1``, for targets ``\sum_{i} \delta_{i j}=1``.
- This is similar to word mover distance problem
    - ``\min _{\mathbf{T} \geq 0} \sum_{i=1} \mathbf{T}_{i j} c(i, j)``, ``c(i,j)`` is word distance, or similarity
    - subject to word count ``\sum_{j=1}^{n} \mathbf{T}_{i j}=d_{i}``, ``\sum_{i=1}^{n} \mathbf{T}_{i j}=d_{j}^{\prime}``.
- word similarity can be computed using CWOB or Skipgram

## Questions
- How do we know that birds learn their song by reference to a memorized template they heard earlier in life?
    - When they are isolated, they wont sing normal song, and when they have tutor, they will copy.
- What songs do female zebra finches find attractive?
    - complex but stereotyped
- How does serial tutoring help with dissection of performance error assignment?
    - We teach the first song, so that we can see what they are actually singing, then we can follow every single vocalization on what is going,
- Why do birds learn syntax independently of phonology?
    - It is an NP hard problem
- In what way is learning a new song like comparing two documents?
    - See how well the words align in two documents
- On what basis are words mapped to a vector space in word2vec?
    - context