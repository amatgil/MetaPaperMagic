# Definicions base
$$ (f\star g)(x) = f(x) \star g(x)$$
$$ (f \dot g )(x) = f(g(x)) $$

## Definició Delta-Epsilon del límit
$$(\forall \delta, 0 < |x - a| < \delta \implies \exists \varepsilon, |f(x) - l| < \varepsilon) \implies \lim_{x\rightarrow a} f(x) = l$$

## Indeterminacions:
- $\infty - \infty$
- $\infty \times 0$
- $\frac{\infty}{\infty}$
- $\frac{0}{0}$
- $1^\infty$
- $0^0$
- $\infty^0$

# Mètodes per resoldre-les
## Per $\infty - \infty$
- Si són fraccions, trobem la seva resta i adeu indeterminació.
- Si són arrels, mulipliquem i dividim pel conjugat

## Per $\infty \times 0$
Es pot reduïr a $0 / 0$ o $\infty / \infty$

## Per $1^{(+\infty)}$
$$\lim u(x)^{v(x)} = 1 \land u(x) \neq 1 \implies \lim u(x)^{v(x)} = e^{\lim (u(x) - 1)v(x)}$$

## Per $\frac{0}{0}$
- Multiplica pel conjugat
- Ves al metge (lmao)

## Per $\frac{\infty}{\infty}$
- Divideix pel terme que creixi més ràpidament
- o aplica l'Hôpital.

## Per $0^0$
- Apliques $ln(L)$, i abaixes l'exponent multiplicant devant.
- D'aquesta manera obtens una indeterminació $0·(-\infty)$
- Aplica l'Hôpital i prega perquè les derivades no siguin quilomètriques.

## Per $\infty^0$
- Apliques $ln(L)$, i abaixes l'exponent multiplicant devant.
- Així consegueixes la indeterminació $0·\infty$
- Aplica l'Hôpital.