## Definició de successió:
Una successió es una aplicació $a:D\rightarrow \mathbb{R}$, el domini de la qual $D$ és
un subconjunt infinit de $\mathbb{N}$. La imatge de $n \in D$ a la successió $a$ es denomina $a_n$.

## Cotes:
Sigui ($s_n$) una successió. 

- Si existeix $k \in \mathbb{R}$ tal que $a_n \leq k$ per a tot $n$, aleshores $k$ és una *cota superior* d'($a_n$). En aquest cas es diu que la successió ($a_n$) està *acotada superiorment*, i la menor de les cotes superiors s'anomena *suprem* d'($a_n$).

- Si existeix $k \in \mathbb{R}$ tal que $a_n \geq k$ per a tot $n$, aleshores $k$ és una *cota inferior* d'($a_n$). En aquest cas es diu que la successió ($a_n$) està *acotada inferiorment*, i la major de les cotes inferiors s'anomena *ínfim* d'($a_n$).

- Si una successió està acotada *superiorment* i *inferiorment*, es diu que està *acotada*.
## Límits:
El límit d'una successió ($a_n$) és:

- El nombre real $\ell$ si per cada real $\epsilon$ > 0, existeix un natural $N$ tal que $|a_n-l| < \epsilon$ per a tot $n \geq N$ ($a_n$ és *convergent*)
- $+ \infty$ si per a cada nombre real $M > 0$ existeix un natural $N$ tal que $a_n > M$ per a tot $n \geq N$ ($a_n$ és *divergent*)
- $- \infty$ si per a cada nombre real $M < 0$ existeix un natural $N$ tal que $a_n < M$ per a tot $n \geq N$ ($a_n$ és *divergent*)


## Càlcul de límits: (Indeterminacions)
Quan treballes amb límits, sovint et trobes amb operacions que involucren $\pm \infty$. En molts casos aquestes es poden solucionar de forma intuïtiva fent com si $\infty$ fos simplement un nombre *molt gran*. Però hi ha 7 casos en què aquesta lògica pot fallar:

- $\infty - \infty$
- $0· \infty$
- $\infty / \infty$
- $0/0$
- $1^ \infty $
- $0^0$
- $\infty ^ 0$

### Propietats: 
- **Regla de l'entrepà:** Si existeix un natural $N$ tal que $b_n \leq a_n \leq c_n$ per a tot $n \geq N$, i $\lim b_n = \ell = \lim c_n$, aleshores $\lim a_n = \ell$
- $\lim a_n = \ell \implies \lim |a_n| = |\ell|$
- $\lim |a_n| = 0 \Longleftrightarrow \lim a_n = 0$

## Criteris per calcular límits:
(Utilitzarem $\mathbb{R}^\omega$ per dir $(\mathbb{R} \cup \set{\infty})$, perquè s'utilitza molt aquí)
### Criteri de l'arrel: 
$$\lim \sqrt[n]{|a_n|} = L \in \mathbb{R}^\omega \implies \begin{cases}
\lim a_n = 0 & \quad \text{quan } L < 1 \\
\lim |a_n| = +\infty &\quad \text{quan } L > 1
\end{cases}$$


### Criteri del quocient:

$$((a_n) \neq 0) \land \lim \frac{|a_n|}{|a_{n-1}|} = L \in \mathbb{R}^\omega \implies \begin{cases}
\lim a_n = 0 & \quad \text{quan } L < 1 \\
\lim |a_n| = +\infty & \quad \text{quan } L > 1
\end{cases}$$


### Criteri del quocient i l'arrel:
$$ \lim \frac{|a_n|}{|a_{n-1}|} = L \in \mathbb{R}^\omega \implies \lim \sqrt[n]{|a_n|} = L$$
## Successions monòtones:
Definicions:
- *Creixent*: $m < n \implies a_m \leq a_n$
- *Estrictament creixent:* $m < n \implies a_m < a_n$
- *Decreixent*: $m < n \implies a_m \geq a_n$
- *Estrictament decreixent:* $m < n \implies a_m > a_n$

### Teorema de la convergència monòtona.

Tota successió monòtona i acotada és convergent. De fet, per una successió creixent i acotada superiorment, el límit és el suprem i per una decreixent i acotada inferiorment, el límit és l'ínfim.