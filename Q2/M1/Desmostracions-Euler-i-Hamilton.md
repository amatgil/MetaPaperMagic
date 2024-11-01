# Euler
Sigui $G = (V,A)$, un graf connex
- $G$ és eulerià $\Longleftrightarrow G$ és connex $\land$ $g(v)$ és parell $\forall v \in V$
- $G$ té un sender eulerià $\Longleftrightarrow G$ és connex $\land$ $G$ té exactament $2$ vèrtexs de grau senar. 

# Hamilton
## Per demostrar que no és hamiltonià: condicions necessàries
- $G$ ham $\implies$ $G$ connex
- $G$ ham $\implies$ $G-(k$ vèrtexs $)$ té màxim $k$ c.c $\implies$ G no té vèrtex d'articulació
- $G$ ham $\land$ $G$ té vèrtex de grau dos $\implies$ el cicle ha de passar per aquestes dues arestes


## Per demostrar que és hamiltonià: theoremes

Sigui $G = (V,A)$, un graf d'ordre $n \geq 3$

- **Dirac:** $u \nsim v \wedge u \neq v \rightarrow g(u)+g(v) \geq n\ \ \forall u,v \in V \implies G$ és Hamiltonià

- **Ore:** $g(u) \geq \dfrac{n}{2}\ \ \forall u \in V \implies G$ és Hamiltonià