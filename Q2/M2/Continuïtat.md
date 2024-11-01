# Funcions de variable real

Una funció de variable real és una aplicació $f:D \rightarrow \mathbb{R}$ on $D$ és un subconjunt de $\mathbb{R}$ denominat *domini* de la funció $f$. La funció associa a cada element $x \in D$, un sol element $y \in \mathbb{R}$, que de forma que $y = f(x)$. En aquest cas, es diria que $y$ és la imatge de $x$, i que $x$ és la antiimatge d' $y$.

## Funció inversa
Si $f: D \rightarrow \mathbb{R}$ és injectiva, aleshores té inversa.


## Simetria
Sigui $f: D \rightarrow \mathbb{R}$, on suposem que $x \in D \Longleftrightarrow -x \in D$
- $f$ és parella $\Longleftrightarrow f(-x) = f(x)$
- $f$ és senar $\Longleftrightarrow f(-x) = -f(x)$

## Periodicitat
Una funció $f: D \rightarrow \mathbb{R}$ és periòdica amb periode $p \in \mathbb{R}$ \
$\Longleftrightarrow$ per cada $x \in D$ es compleix que $x+p \in D$ i que $f(x+p) = f(x)$. 

## Suma i producte de funcions
Siguin $f: D_1 \rightarrow \mathbb{R}$, i $g: D_2 \rightarrow \mathbb{R}$,
- La suma es defineix com: $(f+g)(x) = f(x) + g(x)$
- El producte es defineix com: $(f·g)(x) = f(x)·g(x)$
 
<a/>

En tots dos casos, el domini de la nova funció és: $D_1 \cap D_2$.

## Composició de funcions
Siguin $f: D_1 \rightarrow \mathbb{R}$, i $g: D_2 \rightarrow \mathbb{R}$, on el domini de $g$ conté el recorregut d' $f$, és a dir $f(D_1) \subseteq D_2$,

La composició $(g \circ f)(x) = g(f(x))$

## Cotes 
Sigui $f:D \rightarrow \mathbb{R}$ una funció, on $A \subseteq D$. 

- Si existeix $k \in \mathbb{R}$ tal que $f(x) \leq k$ per a tot $x \in A$, aleshores $k$ és una *cota superior* d' $f$. En aquest cas es diu que la funció $f$ està *acotada superiorment* en $A$, i la menor de les cotes superiors s'anomena *suprem* d' $f$.

- Si existeix $k \in \mathbb{R}$ tal que $f(x) \geq k$ per a tot $x \in A$, aleshores $k$ és una *cota inferior* d' $f$. En aquest cas es diu que la funció $f$ està *acotada inferiorment* en $a$, i la major de les cotes inferiors s'anomena *ínfim* d' $f$.

- Si una funció està acotada *superiorment* i *inferiorment* en $a$, es diu que està *acotada* en $A$.

# Límits de funcions
 
Quan es treballa amb funcions de variable real, es fa servir la notació: $\lim\limits_{x \to \triangle} f(x) = \square$, on:
- $\triangle \in \set{a,a⁺,a⁻,+ \infty, -\infty} $
- $\square \in \set{\ell,+ \infty, -\infty} $
- $a$ i $\ell$ són nombres reals.

## Propietats
- Si existeix el límit de $f$ en \triangle, aleshores és únic.
- $\lim\limits_{x \to a} f(x) = \ell \Longleftrightarrow \lim\limits_{x \to a⁺} f(x) = \lim\limits_{x \to a⁻} f(x) = \ell$

# Continuïtat

Sigui $f: D \rightarrow \mathbb{R}$, $f$ és *continua* en $a \Leftrightarrow \lim\limits_{x \to a} f(x) = f(a)$.\
\
Això és equivalent a què es compleixin alhora: 
1. Existeix $\ell = \lim\limits_{x \to a} f(x)$, i és un nombre real
2. $a \in D$
3. $\ell = f(a)$

Si es compleix la propietat 1 però fallen la 2 o la 3, es diu que $f$ té una discontinuïtat evitable. (Es pot crear una nova funció $F(x)$ de forma que igual a $f$ en tots els punts menys a $x=a$, on es definex que $F(x) = \ell$

## Propietats
Siguin $f:D_1 \rightarrow \mathbb{R}$, i $g:D_2 \rightarrow \mathbb{R}$
- Si $f$ i $g$ són continues en $a$, aleshores $f+g$ i $f·g$ també ho són
- Si $f$ és continua en $a$ i $g$ és continua en $f(a)$, aleshores $g \circ f$ és continua en a 
- Si $f$ és continua i injectiva en  [a,b] aleshores $f^{-1}$ és continua en $f([a,b])$
- Totes les funcions elementals són continues en el seu domini. $(x^a,e^x,log,sin,cos,tan,arcsin,arccos,arctan,sinh,cosh,tanh...)$

***

### Teorema de la conservació del signe

Sigui $f:D_1 \rightarrow \mathbb{R}$, si
- $f$ és continua
- Siguin $a,b \in \mathbb{R}$, tal que a < b
- Existeix $c \in \mathbb{R}$, tal que $f(c) \neq 0$


Aleshores, $\exists \delta > 0 \forall x \in (c-\delta, c+\delta) f(x)·f(c)>0$ \
\
És a dir que en un entorn de $c$, la funció té el mateix signe que en $c$.
***
### Teorema dels valors intermitjos
Sigui $f:D_1 \rightarrow \mathbb{R}$, si f és continua en un interval $\[a,b\]$, aleshores 
$\forall k \in [f(a),f(b)],\exists c \in \[a,b\] f(c) = k$

***
### Teorema de Bolzano

Sigui $f:D_1 \rightarrow \mathbb{R}$, si 
- $f$ és continua en $\[a,b\]$ 
- $f(a)·f(b)$ < 0, 

<a/>

Aleshores existeix $c \in (a,b)$ tal que $f(c) = 0$.
***
### Teorema de Weierstrass

Sigui $f:D_1 \rightarrow \mathbb{R}$, si $f$ és continua en $\[a,b\]$, alsehores:
- $f(\[a,b\])$ té un màxim $M$ i un mínim $m$.
- El recorregut de $f$ és $f(\[a,b\]) = \[m,M\]$