# Definicions bàsiques
- `Graf`: $G = (V, A)$  on
	- $V$ és un conjunt no-buit finit
	- $A$ és un conjunt d'arestes: 
	- `aresta`: Un conjunt $\{u, v\}$ on $u \neq v$ són vèrtexs
- `ordre` ($n$): nº de vèrtexs, $|V|$
- `mida` ($m$): nº d'arestes presents, $|A|$
- `grau` ($g(u)$): nº d'arestes incidents a un vertex $u$, $|\{v\in V | u \sim v\}|$
	- $\delta(G) = \min g(u)$  (grau màxim)
	- $\Delta(G) = \max g(u)$  (grau mínim)
- $xy$ (shorthand for ${x, y}$) és una aresta $\iff$  $x$ és _adjacent_ a $y$  $\iff$ $x\sim y$
- $a = xy$, $b = yz$ son arestes $\iff$ a és _incident_ a b $\iff$ $a \sim b$  (mateixa notació per vertexs i arestes)
- `r-regular`: tot $u$ té el mateix $g(u)$

# Propietats
1. $$0 \leq m \leq \frac{n(n-1)}{2}$$
El màxim és ${n\choose 2}$ , o més intuïtiu: un complet té $n$ nodes amb grau $n-1$. Cada aresta té dues connexions, les desrepetim: $n(n-1)/2$.
3. $$0 \leq g(u) \leq n - 1$$ (Si $g(u) = n-1$, diem que $u$ és "universal$)
4. $$\forall u (g(u) = 0\ \text{xor}\ n - 1 )$$
És a dir, dins d'un mateix graf no poden haver-hi tant un vertex sol com un d'universal
4. A cada graf, $$\exists u, v (g(u) = g(v) \land u \neq v)$$
Si tenim $n$ nodes, els graus poden ser $0, 1, 2, ... n - 1$. Però $0$ i $n - 1$ no poden coexistir, llavors hem de distribuir $n - 1$ opcions sobre $n$ nodes. Hi ha d'haver un repetit!

# Taula bàsica
| Nom       | Ordre   | Mida       | Graus        | Regular          | Bipartit |
| --------- | ------- | ---------- | ------------ | ---------------- | -------- |
| $N_n$     | $n$     | $0$        | $0$          | Sí               |       Sí   |
| $K_n$     | $n$     | $n(n-1)/2$ | $n - 1$      | Sí               |    No      |
| $T_n$     | $n$     | $n - 1$    | $1$, $2$     | No               |   Sí       |
| $C_n$     | $n$     | $n$        | $2$          | Sí               |  Iff $n$ parell     |
| $W_n$     | $n$     | $2n$       | $2$, $n - 1$ | No               |   No       |
| $K_{r,s}$ | $r + s$ | $rs$       | $r$, $s$     | Iff $r = s$ | Sí         |

# El Lema de les Encaixades
Amb un graf $G = (V, A)$ ordre $n$, mida $m$, sempre es compleix que

$$\sum_{u\in V} g(u) = 2m$$

És a dir, el nombre d'arestes és la meitat de la suma de tots els graus (obviament clar, dit així és trivial).


## Conseqüencies
1. Si $G$ és regular, 
$$\sum_{u\in V} g(x) = \sum_{u\in V} r  = nr \stackrel{Lema}{=} 2m$$
Per tant, $nr = 2m$ ($nr$ ha de ser parell!)
2. Sempre hi ha un nombre parell de graus imparells (perquè la suma ha de ser parella)
$$2m = \sum g(u) = \stackrel{Parells}{\sum g(u)} + \stackrel{Imparells}{\sum g(u)}$$
Sabem que $\stackrel{Parells}{\sum g(u)}$ és parell, per tant $\stackrel{Imparells}{\sum g(u)}$ també ho ha de ser (perquè sumen $2m$).

# Subgrafs
- $H(W, B)$ és un subgraf de $G$ $\iff$ $W \subseteq V \land B \subseteq A$
	- Propietat massa general, poc utilitzada
- $H(W, B)$ és un subgraf **induït** de $G$ si $B = \{\ uv\ |\ u,v \in W, uv \in A\ \}$
	- Es a dir, _tria_ els _verts_ i _agafa_ totes les _arestes_ que ja existien
	- Notació: $H = G[W]$, on $W$ son els verts triats
- $H(W, B)$ és un subgraf **generador** de $G$ $\iff$ $W = V$
	- _Agafa_ tots els _verts_  i _tria_ les _arestes_

En resum: **induït** == "tria els vertex", **generador** == "tria arestes" (havent agafat tots els vertex)
Si $H$ és induït i generador, $H = G$

# Operacions
## Generals
$G_1 = (V_1, A_1)$
$G_2 = (V_2, A_2)$
### Unió

$$G_1 \cup G_2 := (V_1 \cup V_2, A_1 \cup A_2)$$  
Si $V_1 \cap V_2 = \emptyset$, et queda un graf no-connex. Si en comparteixen, vigila!

Solem dir coses com " $K_3 \cup T_4$ ", i si no s'especifiquen els noms, assumim que no en comparteixen (i queden dos disconnexos).

### Producte cartesià
$$G_1 \times G_2 := (V_1 \times V_2, B)$$
$B$ és:
	$$(u, v) \sim (u',v') \iff (u = u' \land v \sim v')\lor(u\sim u' \land v = v')$$

- $ordre(G_1 \times G_2) = ordre(G_1)ordre(G_2)$
- $mida(G_1 \times G_2) = ordre(G_1)mida(G_2) + ordre(G_2)mida(G_1$
- $g_{G_1\times{}G_2}(u) = g_{G_1}(u) + g_{G_2}(u)$
### Complementari
$$G^C = (V, A^C)$$ (donat un cert $\Omega$)

$$u \sim v \text{ in } G \iff u \not\sim v \text{ in } G^C$$

- $ordre(G^C) = ordre(G)$
- $mida(G^C) = mida(K_n) - mida(G) = \frac{n(n-1)}{2} - mida(G)$
- $g_{G^C}(u) = g_{K_n}(u) - g_G(u) = (n - 1) - g_G(u)$

NOTE: $$G \cup G^C = K_n$$

### Restar vertex
$$G - u = (V - \{u\}, A - \{uz\ |\ z \in V, uz \in A\})$$
(traure el vertex i totes les arestes que li toquen)

### Restar aresta
$$ G - a = (V, A - \{a\})$$
(treure-la i ja)

### Afegir aresta
$$G + xy = (V, A\cup \{xy\})$$
(afegir-la i ja)

NOTA: no hi ha operació d'afegir un node perquè no està ben definit. t'ho defineixes tu a cada problema


| -     | $G$ | $G - u$    | $G - a$ | $G + a$  |
| ----- | --- | -------- | ----- | ------ |
| ordre | $n$ | $n - 1$    | $n$     | $n$      |
| mida  | $m$ | $m - g(u)$ | $n - 1$ | $n + 1$ | 

# Isomorfisme
$G_1 = (V_1, A_1)$
$G_2 = (V_2, A_2)$

Dos grafs $G_1$ i $G_2$ son isomorfs si existeix una aplicació bijectiva $f: V_1 -> V_2$ tal que $$u \sim v \iff f(u) \sim f(v)$$
**NOTE**: és un bicondicional! Les arestes es mantenen arestes **i les NO arestes es mantenen NO arestes**.

Notació
$$G_1 \cong G_2$$

## IMPORTANT:
($P$ és una propietat de grafs)

- Si $G_1 \cong G_2 \implies P(G_1) = P(G_2)$ 
i el contrarrecíproc, que és més important encara:
- Si $P(G_1) \neq P(G_2) \implies G_1 \not\cong G_2$

# Recorreguts
Un recorregut de longitud $k \geq 1$ és una successió de vertex tal que
$$u_i \sim u_{i+1},\ i = 0,\cdots,k-1$$
La longitud és el nombre d'arestes, no de vertex.
## Tipus
- Recorreguts tancats: $u_0 = u_k$
- **Camí**: No podem repetir vertex
- Cicle: camí tancat
- Sendero: no arestes repetides
- Circuits: senderos tancat
- Aciclic: tal com sona

## Propietats
1. $$\exists u-v\text{ recorregut}\ (u \neq v) \implies \exists u-v\text{ cami de longitut }\leq k$$


# Grafs connexos

$$G\text{ connex} \iff\forall v,u \in V, \exists u-v\ \text{camí}$$

## Perspectives
### Perspectiva de Relació
Definim una relació: $$uRv \iff \exists u-v\text{ cami}$$ 
És una relació, complex les tres propietats de les relacions.


Llavors $V$ queda dividit en _classes d'equivalència_!. Aquestes són els subgrafs induïts: $G[V_1], G[V_2], ..$

### Perspectiva de subgrafs

Un subgraf és una **component connexa** (c.c.) de $G$ sí:
- és un subgraf induït (no et deixes/inventes arestes)
- és connex
- no hi ha cap altre subgraf induït connex més gran
	- No et pots deixar cap vertex, llavors! Sempre has d'agafar-los tots

## Desconnexió
Si li treiem un vertex/aresta a $G$ connex, quante c.c. tenim?
- $G - a$ té màxim **2** c.c.
- $G - u$ té màxim $g(u)$ c.c.

### Demostracions
$$G - u\text{ té màxim }g(u)\text{ c.c.}$$
La veritat és que aquesta no la vaig entendre: **TODO**
$$G - a\text{ té màxim }2\text{ c.c.}$$
Analitzem la part del graf: `z---?---x-----y---?---z`, $xy = a$

A $G$, hi ha un $z-x$ camí ($z\in V$) perquè és connex. Dos casos:
- $z,..,x$ no utilitza $a$ $\implies \exists z-x$ a $G - a$ $\implies$ $z$ i $x$ comparteixen c.
- $z,..,x$ utilitza $a$ $\implies \exists z-y$ a $G - a$ $\implies$ $z$ i $y$ comparteixen c.

Els dos casos son exclusius $\implies$ 2 c.c. màxim

## Demostracions
G connex, 2-regular, $n\geq 3 \implies G \cong C_n$

És a dir: si una c.c. és 2.regular ha de ser un cicle. Si no és connex, és una unió de cicles

Per Inducció:
- Pas base: $n = 3 \land 2-reg \implies C_3 \implies \blacksquare$ 
- Pas inductiu:
	- H.I.: Tots els connexos 2-reg amb ordre $n \geq 3$ són isomorfs a  $C_n$
	- T.I: Els connexos 2-reg amb ordre $n + 1$ és isomorf a $C_n$?
	- $G$ ordre $n+1$ i 2-reg, $G' = (G - z) + xy$
		- Per H.I., $G'$ és connex $\land$ 2-reg $\implies$ $G' \cong C_n$. Si hi afegim un vertex i les ajustem les seves dos arestes, no podem no continuar el cicle.

