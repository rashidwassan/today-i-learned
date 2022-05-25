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
  - simply output the weighted sum.
- Threshold functions:
  - Output low values
    - Until weighted sum gets over a threshold.
    - Then outputs high values.
    - Equivalent of 'firing' of neurons.
- Step function:
  - Output +1 if S> threshold T.
  - Output -1 otherwise.
- Sigma function: 
  - Similar to step function but differentiable.

1) The hard limit activation function:
   1) Sets the output to 0 if the function argument is less than 0.
   2) Sets output to 1 is argument value is greater than or equal to zero.
   3) Used in neurons which classify inputs into two distinct classes.
   4) `Net input = u = 1.8x3 = 5.4. Neuron O/P: f(u) = 1`.

2) Symmetric hard limit:
   1) Similar to hard limit activation function, but outputs -1 if input is less than zero.

3) Linear activation function:
   1) y = u
   2) Output = input

4) The log-sigmoid function
   1) Takes the value of input, squashes it into the range of 0-1.
   2) `y=1/(1+e^-u)`

5) Hyperbolic Tangent Sigmoid:
   1) Shown in figure:
   
   ![](https://assets-global.website-files.com/5d7b77b063a9066d83e1209c/60be1a9bac9b73842964585e_math-20210607%20(8).png)

---
## Example perceptron
- Categorization of 2x2 pixel black & white images into `bright` and `dark`.
- Representation: if number of white pixels >= 2, image is bright.
- Dark otherwise.

## Perceptron architecture
- Four input units, one for each pixel.
- One output unit: +1 for white, -1 for dark.
- Example: Categorizing vehicles.

## Learning in perceptrons:
- Need to learn: weights between input & output units. Value for threshold.
- Make calculations easier by: Thinking of threshold as a weight from special input where output is always 1.
- Exactly the same result: But we have to worry about learning weights.

## Artificial Neural Network Architectures:
- Connecting several neurons in specific manner.
- Defines the network structure.
- The weights or the strength of connections is adapted to yield good performance.
- Each ANN has its own learning rule.
- Types:
1) Feedforward:
  - Most popular
  - Easily implemented
  - Based on layers, all neurons on same level contain same activation function.
  - Different level neurons may have different activation functions.
  - Signal propagates forward only.
### Single Level Feedforward Networks:
- Consists of single layer of output nodes.
- Inputs are fed directly to the outputs via series of weights.
- Sum of the products of weights and inputs is calculated at each node.
- If value is above some threshold (typically 0), neuron fires and takes either activated value (+1) or deactivated value (-1).
- Neurons like these are called *linear threshold units*.
- Term `perceptron` often refers to the networks consisting of just one of these units.

### Multilayer Feedforward Networks
- Contain input layer, hidden layer(s), and output layer.
- Hidden layers cannot be accessed from outside the network.
- There maybe some partially connected feedforward networks with one hidden layer.

## Recurrent or Feedback networks:
- Models with bidirectional dataflow, data can flow back to earlier stage as well.

## Some other ANNs
- Hopfield network
- Echo state network
- Stochastic neural networks
- Boltzmann machine
- Committee of machines
- Associative neural network

## ANN Training Algorithm
- Weights are set random initially.
- For each training example E:
  - Calculate observed O/P from ANN o(E).
  - If target t(E) is different to o(E), tweak all the weights to make them closer.
  - Tweaking is done by perceptron training rule.