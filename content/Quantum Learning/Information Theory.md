Say we want to transmit $n$ bits from point A to point B. Let $p$ be the probability of an error per bits, which are IID. How do we make sure the correct message is sent?

# Repetition

> [!math|{"type":"definition","number":"auto","setAsNoteMathLink":false,"title":"KL Divergence","label":"kl-divergence","_index":0}] Definition 1 (KL Divergence).
> Let $E$ be a set of events $\{ 1\dots n \}$ and $p,q$ be probability distributions on $E$. Then, the divergence between the two distributions is the KL-Divergence:
> $$
> D_{KL}(p \mid \mid q) = \sum_{i \in E}^{}p_{i}\log\left( \frac{p_{i}}{q_{i}} \right).
>$$

> [!math|{"type":"theorem","number":"auto","setAsNoteMathLink":false,"title":"Chernoff Bound","label":"chernoff-bound","_index":1}] Theorem 2 (Chernoff Bound).
> For random Bernoulli variables $X_{i}, i \in \{ 1\dots n \}$,
> $$
> P\left( \sum_{i}^{}x_{i}>nq \right) < \exp(-nD_{KL}(p \mid\mid q))
>$$
> for $q \geq p$.

By repeating 