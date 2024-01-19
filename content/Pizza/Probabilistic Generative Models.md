- take samples of probabilistic distributions -> generate new, original probabilistic distributions
- challenges: non-Gaussian distributions
- transport maps
	- characterize distributions
	- $T$ couples a target distribution $\pi$ and a simple reference $\eta$ if $\mathbf{z} \sim n$ 
	- pushforwad, pullback operators

# Normalizing Flows (NF)

- construct $T_{\theta}: \mathbb{R}^{d} \to \mathbb{R}^{d}$ to be diffeomorphic (smooth and invertible)
- learn $T_{\theta}$ by maximizing likelihood of samples

## Change of Variables

- Assume $T_{\theta}$ is diffeomorphic
- change of variables formula describes density of transformed random variable $\mathbf{x} \sim T_{\theta}(\mathbf{z})$ for $\mathbf{z} \sim \eta$.

$$
p_{\theta}(\mathbf{x}) = p_{\eta}(T_{\theta}^{-1}(x))
$$

- maximim likelihood

# Generative Adversarial Networks (GAN)

- support non-invertible $T_{\theta}: \mathbb{R}^{r} \to \mathbb{R}^{d}$ using low-dimensional reference (latent) distribution $r\ll d$
- learn $T_{\theta}$ by minimizing transport distance

# Variational Autoencoders (VAE)

- support non-invertible $T_{\theta}$
- approximate inverse $S_{\theta}:\mathbb{R}^{d} \to \mathbb{R}^{r}$ with another map
- learn maps using likelihood lower bound

