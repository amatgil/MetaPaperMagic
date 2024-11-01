# Taylor
Vols aproximar una funció difícil amb un polínomi? El polinomi de Taylor és el que busques!

## Formula

$$P_n(f, a, x) = \frac{f(a)}{0!}(x-a)^0 + \frac{f'(a)}{1!}(x-a)^1 + \ldots = \sum_0^n \frac{f^{(n)}(a)}{n!}(x-a)^n$$

## Càlcul de l'error (residu de Lagrange)
$$\exists c \in (x, a) \text{ tal que } R_n(f, a, x) = \frac{f^{(n + 1)}(c)}{(n+1)!}(x-a)^{(n+1)}$$

Per tant, si $M$ és el màxim de l'interval

$$\varepsilon < \frac{f^{(n + 1)}(M)}{(n+1)!}(x-a)^{(n+1)}$$
