## Mètode de la bisecció
Donada una equació $f(x) = 0$, si coneixem $a$ i $b$ tals que $f(a)·f(b) < 0$, i $f$ és continua en l'interval $\[a,b\]$, aleshores podem afirmar (per Bolzno) que hi ha una solució dins de l'interval. Per trobar-la, fem servir el següent algoritme: 
### Algoritme
- Agafem una $c \in \(a,b\)$, de forma que $c = \dfrac{a+b}{2}$
- Si $f(c) = 0$, hem trobat la solució. \
   Si $f(a)·f(c) < 0$, repetim el procés a l'interval $(a,c)$ \
   Si $f(b)·f(c) < 0$, repetim el procés a l'interval $(c,b)$

### Fita de l'error
La fita superior de l'error que es fa a cada iteració, es pot trobar amb la fórmula:
- $\varepsilon = \dfrac{b-a}{2^n}$ 

Això vol dir que podem trobar el nombre d'iteracions que cal realitzar amb:
- $n = \log_2{\dfrac{b-a}{\varepsilon}}$

## Mètode de la secant
Sigui $f: D \rightarrow \mathbb{R}$, una funció contínua en l'interval $\[a,b\]$. Si es compleix que $f(a)·f(b) < 0$, aleshores podem trobar la solució de l'equació $f(x) = 0$ agafant $x_0 = a, x_1 = b$, i aplicant la fórmula:
## Formula
$$x_{n+1} = x_n - f(x_n)· \dfrac{x_n - x_{n-1}}{f(x_n) - f(x_{n-1})}$$

(Que, en realitat, és Newton d'amagatotis: fixeu-vos que com $f'(x) = \frac{f(x_n) - f(x_{n-1})}{x_n - x_{n-1}}$, les formules son idèntiques!)

La successió $(a_n)$ convergeix en la solució de l'equació.
### Criteri d'aturada
Podem aturar el procés, un cop es compleixin:
- $|x_{n+1} - x_n| < \varepsilon$
- $|f(x_{n+1})| < \varepsilon$

Gràficament:

<img src="https://github.com/amatgil/MetaPaperMagic/blob/master/Q2_M2/secant_precisio.png" width="400">

### Fita de l'error


## Mètode de la tangent (Newton)
### Formula
$$x_{n+1} = x_n - \frac{f(x_n)}{f'(x_n)}$$
### Criteri d'aturada
Idèntic a la secant (perquè son el mateix mètode in disguise!)
- $|x_{n+1} - x_n| < \varepsilon$
- $|f(x_{n+1})| < \varepsilon$