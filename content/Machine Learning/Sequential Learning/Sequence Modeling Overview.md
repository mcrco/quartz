# History and Explanation

Recurrent neural networks (RNNs) are used for sequential values, like [[CNN]]s with images. 

They can scale to **long sequences** by **sharing parameters across different parts of model**. 

Benefits of shared parameters:
- generalize across sequences of different lengths
- find recurring patterns in sequences
	- "I went to Nepal in 2009" vs "In 2009, I went to Nepal"

Have been efforts to use convolution ([[CNN]]) but with 1-D temporal info, where shared parameter is convolution kernel.

# Computational Graphs for Recurrent Systems

Computational graphs visualize the structure of computations. Recursive/recurrent networks have their own, which can be unfolded due to its self-looping nature.

The classical form of a dynamical system is as follows:

$$
\mathbf{s}^{t} = f(\mathbf{s}^{t-1}; \theta),
$$

where $\mathbf{s}^{t}$ is the state of the system and $\theta$ is a shared parameter. Unfolding the graph of this system means that we can rewrite $\mathbf{s}^{3}$ as follows:

$$
\begin{align}
\mathbf{s}^{3} &= f(\mathbf{s}^{2}; \theta) \\
&= f(f(\mathbf{s}^{1};\theta);\theta)
\end{align}
$$

Below is an unfolded computation graph of a dynamical system

![[dynamical system.png]]

A dynamical system driven by an external system can be written as follows:

$$
\mathbf{s}^{t} = f(\mathbf{s}^{t-1}, \mathbf{x}(t);\theta)
$$

This is the formula for the hidden state in many RNNs:

$$
\mathbf{h}^{t} = f(\mathbf{h}^{t-1}, \mathbf{x}^{t}; \theta)
$$

RNNs learn to use $\mathbf{h}^{t}$ as a lossy summary of past inputs (it's a fixed length vector, but the sequences of input are arbitrary length). 

Below is a recurrent graph and an unfolded graph of a RNN's hidden state (left and right, respectively).

![[unfolded rnn h.png]]

The benefit of the unfolded RNN representation is that rather than having the hidden state as a function of all past inputs, you can define a singular function that uses the same parameters at each time step and requires input of the same length. It also makes visualizing the forwards and backwards computation of outputs and losses and gradients easier.-   Under Options > Files and Links, set the New link format to always use Absolute Path in Vault.