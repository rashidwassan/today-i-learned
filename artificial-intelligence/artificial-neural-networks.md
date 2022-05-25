# Artificial Neural Networks

## Definition
Artificial Neural Networks, also called Neurocomputing or Parallel Distributed Process (PDP) or connectionist networks are interconnected assemblies of simple processing elements called neurons, or nodes, which act like a biological neuron.
- Processing ability is stored in in the inner-unit connection strength.
- Weights are obtained in the process of adaptation to, or learning from set of training patterns.
## Main Features of Neural Networks
- They learn by experience rather than programming or modelling.
- ANN architectures are distributed, inherently parallel and potentially realtime.
- Have the ability to generalize.
- Do not require prior understanding of the process.
- Can form arbitrary continuos non-linear mappings.
- Robust to noisy data.
- VLSI (Very large scale integration) Implementation is easy.

## Applications of ANNs
- Pattern recognition
  - Character recognition
- Speech recognition
- Face recognition
- Online signature recognition
- Color recognition
- Weather forecasting
- Load forecasting
- Intelligent routes and traffic management
- Intelligent controller design
- Intelligent modelling

## Limitations
- Conventional networks are black box models
- Tools for analysis and validation are not well established
- Only problems for which machine is trained will be solved
- Human brain cannot be fully simulated

## Biological Neuron

### Soma or Cell Body: 
Central part of a neuron. It contains nucleus and protein synthesis machine. Size can be 10 to 80 micrometers.
### The dendrites:
- Dendrites represent a highly branching tree of fibers and are attached to soma.
- Taken from Greek word `dendro` which means tree.
- Connect neuron to other set of neurons.

### The axon
- Long tubular fiber.
- Divides itself to the number of branches towards its end.
- Length can be from 100um to 1M.
- Transmits the generated neural activity to other neurons or muscle fibers.
- It is `output channel` of a neuron.
- The point at which the axon is connected to its cell body is called `Hillock Zone`.

### Synapsis
- The junction at which a signal is passed from one neuron to the next is called a synapse (from the Greek verb to join).
- Button like shape.
- 1 um diameter.
- Usually not a physical connection. There can be some gap called `synaptic cleft`.
- The strength of connection can be altered to adapt organism to work efficiently in the environment.

## Is is possible ot simulate a human brain?
- No, with current processing power, it is impossible.
- Reasons:
  - Human brain contains about 100 billion neurons. Each neuron has up to 1000 dendrites.
  - It makes total of 100,000 synapses in brain.
  - Behavior of the real nervous system is very complex and not fully known yet.

## Model of Artificial Neuron:
![](https://upload.wikimedia.org/wikipedia/commons/6/60/ArtificialNeuronModel_english.png)
- Input parameters:
  - Input signals: x1, x2, x3, ....., xn.
  - Synaptic weights: wx1, wx2, wx3, ..... wxn.
  - Summing function: uk = ∑xi*wxi
  - Bias = bk.

## Perceptrons
- Multiple input nodes
- Single output node
  - Takes weighted sum of inputs.
  - Unit function calculates the output of the network.
- Useful to study because:
  - We can use perceptrons for building larger networks.
- Perceptrons have limited representational abilities.
### Activation functions:
- Also known as transfer function.
- Maybe linear or non-linear.
- A particular activation function is used or different purposes.

### Types of Activation Functions:
- Linear functions:
- Threshold functions:
- Step function:
- Sigma function: 