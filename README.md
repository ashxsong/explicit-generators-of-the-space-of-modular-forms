# Explicit Generators of the Space of Modular Forms
This code computes the coefficient matrix $\mathbf{A}$, its elimination matrix $\mathbf{P}$, and the entries of the anti-diagonal of $\mathbf{PA}$ in our paper "Explicit Generators of the Space of Modular Forms" (Tianyu Ni, Ashley Song, Yanhui Su, Hui Xue, Amanda Yin).

The actual coefficient matrix $\mathbf{A}$ is computed directly from the Eichler-Shimura relations [[1]](#1), which are given as follows: for $0\leq t\leq \kappa-2$, we have that

$$r_t+(-1)^{t}r_{\kappa-2-t}=0,$$
$$(-1)^{t}r_t+\sum_{\substack{0\leq \ell\leq t\\\\ \ell\equiv0\pmod2}}\binom{t}{\ell}r_{\kappa-2-t+\ell}+\sum_{\substack{0\leq \ell\leq \kappa-2-t\\\\\ell\equiv t\pmod2}}\binom{\kappa-2-t}{\ell}r_{\ell}=0,$$
$$\sum_{\substack{1\leq \ell\leq t\\\\\ell\equiv1\pmod2}}\binom{t}{\ell}r_{\kappa-2-t+\ell}+\sum_{\substack{0\leq \ell\leq \kappa-2-t\\\\\ell\not\equiv t\pmod2}}\binom{\kappa-2-t}{\ell}r_{\ell}=0.$$

## Proposition 2.2 (1)

Using the first Eichler-Shimura relation, for $t \leq \frac{\kappa - 2}{2}$, the second Eichler-Shimura relation can be rewritten as

$$\sum_{\substack{0\leq \ell\leq t\\\\ 2\mid \ell}} \left[\binom{\kappa - 2 - t}{\ell} - \binom{t}{t - \ell} \right] r_{\ell}+\sum_{\substack{t<\ell\leq \frac{\kappa - 2}{2}\\\\2 \mid (\ell - t)}}\left[\binom{\kappa - 2 - t}{\ell} -\binom{\kappa - 2 - t}{\kappa - 2 - \ell} \right]r_{\ell}= 0.$$

Applying the equation above, the entries of $\mathbf{A}$ are explicitly given by the following:

(1) If $m$ is even, then $\ell \leq t$ for all $i, j$, implying that

$$a_{ij} = \binom{6m + 2 \left\lceil\frac{3m}{2}\right\rceil-2i +2a - 2\left\lfloor\frac{a}{2}\right\rfloor}{ 2j} - \binom{ 6m - 2 \left\lceil\frac{3m}{2}\right\rceil + 2i + 2\left\lfloor\frac{a}{2}\right\rfloor-2}{ 2j}.$$

(2) If $m$ is odd, then $\ell \leq t$ for all $i, j$, except for $(i, j) = \left(1, \frac{3m + 1}{2}\right)$ and $a \in \\{0, 1\\}$. So the entries $a_{ij}$ are given by the formula above, except for $(i, j) = \left(1, \frac{3m + 1}{2}\right)$ and $a \in \\{0, 1\\}$, in which case

$$a_{ij} = \binom{9m +2a-1 }{3m+1} - \binom{9m+2a-1}{2}.$$

The elimination matrix $\mathbf{P}=(p_{ij})_{i, j}$ is given by the following:

(1) If $a$ is even, then 

$$p_{ij} = \begin{cases}(-1)^{j - i} \binom{2\left\lceil \frac{3m}{2} \right\rceil - 2i + 1}{j - i}, &\quad i \leq j, \\\\ 0, &\quad i > j. \end{cases}$$
        
(2) If $a$ is odd, then 

$$p_{ij} = \begin{cases} 
      (-1)^{j-i}\left[\binom{ 2\left\lceil\frac{3m}{2}\right\rceil-2i + 1}{ j-i} - \binom{2\left\lceil\frac{3m}{2}\right\rceil -2i+ 1}{j - i - 1}\right],&\quad i \leq j,\\
      0, &\quad i>j.
   \end{cases}$$


Now, we determine the entries of the anti-diagonal of $\mathbf{PA}$. Let $y = \left\lceil \frac{3m}{2} \right\rceil + 1 - j$. If $m$ is even, then

$$(\mathbf{PA})\_{yj} = \sum_{x = 1}^{\left\lceil \frac{3m}{2} \right\rceil} p_{yx} a_{xj} = \sum_{x = y}^{\left\lceil \frac{3m}{2} \right\rceil} p_{yx} a_{xj}= \begin{cases} 2^{2(j - 1)}(12m - 2j + 2a - 1), &\quad a \equiv 0 \pmod 2, \\\\ 2^{2j - 1}(12m - 2j + 2a - 1), &\quad a \equiv 1 \pmod 2.\end{cases}$$

If $m$ is odd, then $(\mathbf{PA})\_{yj}$ is given by the formula above, except for $j = \frac{3m + 1}{2}$ and $a \in \\{0, 1\\}$, in which case

$$(\mathbf{PA})\_{yj}=\sum_{x = 1}^{\left\lceil \frac{3m}{2} \right\rceil} p_{yx} a_{xj} = \sum_{x = y}^{\left\lceil \frac{3m}{2} \right\rceil} p_{yx} a_{xj} = \begin{cases}2^{3m - 1}(9m - 2) - \binom{9m - 1}{2}, &\quad a = 0,\\\\ 2^{3m}(9m) - \binom{9m + 1}{2}, &\quad a = 1.\end{cases}$$

## Proposition 2.2 (2)

Using the first Eichler-Shimura relation, for $t \leq \frac{\kappa -2}{2}$, the third Eichler-Shimura relation can be rewritten as

$$\sum_{\substack{1\leq \ell\leq t\\\\ 2 \nmid \ell}} \left[\binom{\kappa - 2 - t}{\ell} + \binom{t}{t - \ell} \right]r_{\ell}+\sum_{\substack{t < \ell \leq \frac{\kappa - 2}{2}\\\\ 2\nmid(\ell-t)}}\left[\binom{\kappa - 2 - t}{\ell} +\binom{\kappa - 2 - t}{\kappa - 2 - \ell} \right]r_{\ell}= 0.$$

Applying the equation above, the entries of $\mathbf{A}$ are explicitly given by the following:

(1) If $m$ is even, then $\ell \leq t$ for all $i, j$, implying that

$$a_{ij} =\binom{6m + 2 \left\lceil\frac{3m}{2}\right\rceil-2i +2a - 2\left\lfloor\frac{a}{2}\right\rfloor}{ 2j-1} + \binom{ 6m - 2 \left\lceil\frac{3m}{2}\right\rceil + 2i + 2\left\lfloor\frac{a}{2}\right\rfloor-2}{ 2j-1}.$$

(2) If $m$ is odd, then $\ell \leq t$ for all $i, j$, except for $(i, j) = \left(1, \frac{3m + 1}{2}\right)$ and $a \in \\{0, 1\\}$. So the entries $a_{ij}$ are given by the formula above, except for $(i, j) = \left(1, \frac{3m + 1}{2}\right)$ and $a \in \\{0, 1\\}$, in which case

$$a_{ij} = \binom{9m+2a - 1}{ 3m} +\binom{9m+2a- 1}{1}.$$

The elimination matrix $\mathbf{P}=(p_{ij})_{i,j}$ is given by the following: 

(1) If $a$ is even, then 

$$p_{ij} = \begin{cases} (-1)^{j-i}\left[\binom{ 2\left\lceil \frac{3m}{2}\right\rceil-2i - 1}{ j-i} - \binom{2\left\lceil\frac{3m}{2}\right\rceil-2i -1}{ j-i  - 2}\right],&\quad i \leq j,\\\\0, &\quad i>j.\end{cases} $$
      
(2) If $a$ is odd, then 

$$ p_{ij} = \begin{cases}(-1)^{j - i} \frac{2\left(\left\lceil \frac{3m}{2} \right\rceil - j + 1\right)^2}{\left(2\left\lceil \frac{3m}{2} \right\rceil - i - j + 2\right)\left(\left\lceil \frac{3m}{2} \right\rceil - i + 1\right)} \binom{2\left\lceil \frac{3m}{2} \right\rceil - 2i + 1}{j - i}, &\quad i \leq j, \\\\0, &\quad i > j. \end{cases}$$

Now, we determine the entries of the anti-diagonal of $\mathbf{PA}$. Let $y = \left\lceil \frac{3m}{2} \right\rceil + 1 - j$. If $m$ is even, then

$$(\mathbf{PA})\_{yj} = \sum_{x = 1}^{\left\lceil \frac{3m}{2} \right\rceil} p_{yx} a_{xj} = \sum_{x = y}^{\left\lceil \frac{3m}{2} \right\rceil} p_{yx} a_{xj} = \begin{cases}2^{2(j - 1)}(12m - 2j + 2a), &\quad a \equiv 0 \pmod 2, \\\\ 
\frac{2^{2(j - 1)}(12m - 2j + 2a)(2j - 1)}{j}, &\quad a \equiv 1 \pmod 2.
\end{cases}$$
    
If $m$ is odd, then $(\mathbf{PA})\_{yj}$ is given by the formula above, except for $j = \frac{3m+1}{2}$ and $a\in \\{0,1\\}$, in which case

$$(\mathbf{PA})\_{yj} =\sum_{x = 1}^{\left\lceil \frac{3m}{2} \right\rceil} p_{yx} a_{xj} = \sum_{x = y}^{\left\lceil \frac{3m}{2} \right\rceil} p_{yx} a_{xj} = \begin{cases}
            2^{3m - 1}(9m - 1) + (9m - 1), &\quad a = 0, \\\\
            \frac{2^{3m}(9m + 1)(3m)}{3m + 1} + (9m + 1), &\quad a = 1.
    \end{cases}$$
    
## References
<a id="1">[1]</a>
Ju. I. Manin. Periods of cusp forms, and p-adic Hecke series. Mat. Sb. (N.S.), 92(134):378–401, 503, 1973.
