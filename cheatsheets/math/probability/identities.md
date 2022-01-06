# Definitions

$$
\begin{align}
P_X(x) &= \sum_y P_{(X, Y)}(x, y) &\quad \text{Marginal Dist.} \\
P_Y(x) &= \sum_y P_{(X, Y)}(x, y) &\quad \text{Marginal Dist.} \\
P_{X|y}(x) &= \frac{P_{(X, Y)}(x, y)}{P_Y(y)} &\quad \text{Conditional Dist.}\\
P_{X|Y}(x, y) &= \frac{P_{(X, Y)}(x, y)}{P_Y(y)}\\
H[P_X(X)] &= E_{x \sim P_X}[-\log P_X(x)] &\quad \text{Entropy}\\
H[X] &= E_{x \sim P_X}[-\log P_X(x)] &\quad \text{Entropy when distribution is obvious} \\
H[p] & =E_p[-\log p] &\quad \text{Entropy when variable is obvious} \\
H[X|y] &= E_{x \sim P_{(X|y)}}[-\log P_{X|y}(x)] &\quad \text{Entropy of Conditional Dist.} \\
H[X|Y] &= E_{y \sim P_Y}[H[X|y]] = E_{x, y \sim P_{(X,Y)}}[-\log P_{X|Y}(x, y)] &\quad \text{Conditional Entropy} \\
H[p, q] &= \mathrm{E}_{p}[-\log q] &\quad \text{Cross Entropy} \\
D_{KL}(p || q) &= H_{x \sim p}\left[\log \frac{p(x)}{q(x)}\right] = H[p, q] - H[p] &\quad \text{KL Divergence} \\
\operatorname{pmi}(x; y) &= \log\frac{P_{(X, Y)}(x, y)}{P_{X}(x) P_{Y}(y)} &\quad \text{Pointwise Mutual Information}\\
I(X ; Y) &= D_{\mathrm{KL}}\left(P_{(X, Y)} \| P_{X} \otimes P_{Y}\right) = E_{x, y \sim P_{(X, Y)}} \left[\log \frac{P_{(X, Y)}(x, y)}{P_{X}(x) P_{Y}(y)} \right] = E_{x, y \sim P_{(X, Y)}}[\operatorname{pmi}(x; y)] &\quad \text{Mutual Information} \\
\end{align}
$$

# Identities

$$
\begin{align}
H[p, q] &\geq H[p] &\quad \text{Gibb's Inequality} \\
D_{KL}(p || q) &= H[p, q] - H[p] \geq 0\\
\mathrm{H}(X, Y) &= \mathrm{H}(X | Y) + \mathrm{H}(Y) = \mathrm{H}(Y | X) + \mathrm{H}(X) &\quad \text{Chain Rule} \\
\mathrm{I}(X ; Y) 
& \equiv \mathrm{H}(X)-\mathrm{H}(X \mid Y) = E_{x,y \sim P_{(X, Y)}}[-\log P_X(x)] - E_{x, y \sim P_{(X,Y)}}[-\log \frac{P_{(X, Y)}(x, y)}{P_Y(y)}] \\ 
& \equiv \mathrm{H}(Y)-\mathrm{H}(Y \mid X) \\ 
& \equiv \mathrm{H}(X)+\mathrm{H}(Y)-\mathrm{H}(X, Y) \\ 
& \equiv \mathrm{H}(X, Y)-\mathrm{H}(X \mid Y)-\mathrm{H}(Y \mid X) \\

\end{align}
$$

# Useful Inequalities

1. Log-sum inequality: $\sum_{i=1}^{n} a_{i} \log \frac{a_{i}}{b_{i}} \geq a \log \frac{a}{b}$ 
   1. $a=\sum_i a_i$, $b=\sum_i b_i$
   2. $a_i \geq 0$ , $b_i \geq 0$

