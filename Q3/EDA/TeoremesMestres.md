# Els Teoremes Mestres

N'hi ha dos:
- Subtractiva: $T(n) = a\cdot{}T(n-c) + g(n^k)$
- Divisora: $T(n) = a\cdot{}T(\frac{n}{b}) + g(n^k)$

## Subtractiva
$$T(n) = a\cdot{}T(n-c) + g(n^k)$$

llavors

$$
T(n) \in
\begin{cases}
\Theta(n^k) si a < 1\\
\Theta(n^{k+1}) si a = 1\\
\Theta(a^\frac{n}{c}) si a > 1
\end{cases}
$$

## Divisora
$$T(n) = a\cdot{}T(\frac{n}{b}) + g(n^k)$$

Important: $$\alpha = \log_b{a}$$

$$
T(n) \in
\begin{cases}
\Theta(n^k) si \alpha < k \\
\Theta(n^k \log n) si \alpha = k\\
\Theta(n^\alpha) si \alpha > k
\end{cases}
$$
