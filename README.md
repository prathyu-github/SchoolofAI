# SchoolofAI
**What is a neural network neuron?**
A nueral network is graphically connected through nuerons along with relations among themselves. Basically, a neuron is a computational unit which is a mathematical operation that takes it's input, multiplies it by it's weights and then passes the sum through the activation function  to the other neurons to give output.
y=x1w1+x2w2+x3w3+...+xnwn.

**What is the use of the learning rate?**
Learning rate is a hyper-parameter that controls the weights of our neural network with respect to the loss gradient. It defines how quickly the neural network updates the concepts it has learned. A desirable learning rate is low enough that the network converges to something useful, but high enough that it can be trained in a reasonable amount of time.

**How are weights initialized?**
Neural network models are fit using an optimization algorithm called stochastic gradient descent that incrementally changes the network weights to minimize a loss function, and to make useful predictions. This optimization algorithm requires a starting point in the space of possible weight values from which to begin the optimization process. Weight initialization is a procedure to set the weights of a neural network to small random values that define the starting point for the optimization (learning or training) of the neural network model.
Historically, weight initialization follows simple heuristics, such as:
Small random values in the range [-0.3, 0.3]
Small random values in the range [0, 1]
Small random values in the range [-1, 1]

**What is "loss" in a neural network?**
Loss is nothing but a prediction error of Neural Net and the method to calculate the loss is called Loss Function. In simple words, the Loss is used to calculate the gradients and the gradients are used to update the weights of the Neural Net.

**What is the "chain rule" in gradient flow?**
The chain rule is used when we need the derivative of an expression composed of nested subexpressions. In order to calculate the total gradient, we need to calculate the gradient of the insider gradient. Chain rules are defined in terms of nested functions, like y=f(g(x)) for a single variable chain rule.
