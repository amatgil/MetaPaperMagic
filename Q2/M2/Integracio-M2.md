# Integració

## Regla de Barrow
Si $f$ i $F$ son continues a l'interval, $F$ derivable tal que $F' = f$, llavors $$\int_a^b f(x)dx = F(b) - F(a)$$

## Aproximacions
Recordem que $h = \frac{b-a}{n}$ i $x_i = i\cdot{}h$

### Trapezis

#### Formula
$$T_n = h\left(\frac{f(a)}{2} + \sum_{i = 1}^{n - 1}(f(x_i)) + \frac{f(b)}{2}\right),\ h = \frac{b - a}{n}$$
#### Error 
$$\epsilon \lt \frac{(b-a)^3}{12n^2} \cdot f^{(2)}(\zeta)$$


### Simpson
(Recordem que $n$ parell!)
#### Formula
$$S_n = \frac{h}{3}\left(f(a) + f(b) + 2 \sum_{i = 1}^{n/2 - 1} f(x_{2j}) + 4\sum_{i = 1}^{n/2}f(x_{2i-1})\right)$$

En català, seria:
$$S_n = \frac{h}{3}\left(f(a) + f(b) + 2\sum_{\text{i parell}}f(x_i) + 4\sum_{\text{j imparell}}f(x_j)\right)$$

#### Error
$$\epsilon \lt \frac{(b-a)^5}{180n^4} \cdot f^{(4)}(\eta)$$