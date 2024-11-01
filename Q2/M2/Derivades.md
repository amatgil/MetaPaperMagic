# Derivades
## Definició
$$f'(x) = \lim_{x\rightarrow a}\frac{f(x) - f(a)}{x-a} = \lim_{h\rightarrow 0}\frac{f(a + h) - f(a)}{h}$$

La recta tangent al punt $(a, f(a))$ és $y = f'(a)(x-a)+ f(a)$ (la pendent és $f'(a)$, la variable és $x-a$)

## Regles per calcular-ne
$$(f\times g)' = f' g + g' f$$

$$(\frac{f}{g})' = \frac{f'g - fg'}{g^2}$$

$$(f(g(x)))' = f'(g(x))\times g'(x) $$


## Notables a memoritzar
$$\log_b f(x) \implies \frac{f'(x)}{f(x)\times \ln b}$$

$$\tan(f(x)) \implies f'(x)\frac{1}{\cos^2(f(x))}$$

$$a^{f(x)} \implies a^{f(x)}\cdot\ln a \cdot f'(x)$$


## Teoremes
Assumeixen continuitat a l'interval $[a, b]$ i derivabilitat al $(a, b)$

### Rolle
$$f(a) = f(b) \implies \exists c, f'(c) = 0$$

### Cauchy
$$\exists c, g'(c)(f(b)-f(a)) = f'(c)(g(b)-g(a))$$

### Valor mig
$$\exists c, f(b) - f(a) = f'(c)\cdot (b-a)$$