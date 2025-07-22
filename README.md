# Explicit Generators of the Space of Modular Forms
This code computes the coefficient matrix $\mathbf{A}$, its elimination matrix $\mathbf{P}$, and the entries of the anti-diagonal of $\mathbf{PA}$ in our paper "Explicit Generators of the Space of Modular Forms" (Tianyu Ni, Ashley Song, Yanhui Su, Hui Xue, Amanda Yin).

The actual coefficient matrix $\mathbf{A}$ is computed directly from the Eichler-Shimura relations [[1]](#1), which are given as follows: for $0\leq t\leq \kappa-2$, we have that

$$r_t+(-1)^{t}r_{\kappa-2-t}=0,$$
$$(-1)^{t}r_t+\sum_{\substack{0\leq \ell\leq t\\\\ \ell\equiv0\pmod2}}\binom{t}{\ell}r_{\kappa-2-t+\ell}+\sum_{\substack{0\leq \ell\leq \kappa-2-t\\\\\ell\equiv t\pmod2}}\binom{\kappa-2-t}{\ell}r_{\ell}=0,$$
$$\sum_{\substack{1\leq \ell\leq t\\\\\ell\equiv1\pmod2}}\binom{t}{\ell}r_{\kappa-2-t+\ell}+\sum_{\substack{0\leq \ell\leq \kappa-2-t\\\\\ell\not\equiv t\pmod2}}\binom{\kappa-2-t}{\ell}r_{\ell}=0.$$

## Proposition 2.2(1)

Using the first Eichler-Shimura relation, for $t \leq \frac{\kappa - 2}{2}$, the second Eichler-Shimura relation can be rewritten as

$$\sum_{\substack{0\leq \ell\leq t\\\\ 2\mid \ell}} \left[\binom{\kappa - 2 - t}{\ell} - \binom{t}{t - \ell} \right] r_{\ell}+\sum_{\substack{t<\ell\leq \frac{\kappa - 2}{2}\\\\2 \mid (\ell - t)}}\left[\binom{\kappa - 2 - t}{\ell} -\binom{\kappa - 2 - t}{\kappa - 2 - \ell} \right]r_{\ell}= 0.$$

## Proposition 2.2(2)

Using the first Eichler-Shimura relation, for $t \leq \frac{\kappa -2}{2}$, the third Eichler-Shimura relation can be rewritten as

$$\sum_{\substack{1\leq \ell\leq t\\\\ 2 \nmid \ell}} \left[\binom{\kappa - 2 - t}{\ell} + \binom{t}{t - \ell} \right]r_{\ell}+\sum_{\substack{t < \ell \leq \frac{\kappa - 2}{2}\\\\ 2\nmid(\ell-t)}}\left[\binom{\kappa - 2 - t}{\ell} +\binom{\kappa - 2 - t}{\kappa - 2 - \ell} \right]r_{\ell}= 0.$$

## References
<a id="1">[1]</a>
Ju. I. Manin. Periods of cusp forms, and p-adic Hecke series. Mat. Sb. (N.S.), 92(134):378–401, 503, 1973.
