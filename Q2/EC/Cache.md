# Cache

## Concepte bàsic:

Un adreça de memòria principal (MP) s'ha de mapejar a la cache (MC). La cache ha de emmagatzemar les dades, recordar quina és la seva adreça i mantindre coherència. Les dues primeres parts es fan:

### Com s'emmagatzemen

Una linia de cache es visualitza així:

| V | Tag                        | Dades                     |
|---|----------------------------|---------------------------|
| 1 | [Primers bits de l'adreça] | Dada 1 - D2 - D3 - ... DN |

Per agafar una dada (e.g. un byte), podem agafar el principi de l'adreça, buscar això al tag i extreure-hi-la de l'offset corresponent.

## Com i on s'hi escriu

Hem de decidir com/on s'escriure per raons de sentit comú.


### Escriptura

| Escriptura - Hit | Quan escrivim a MP?                               |
|------------------|---------------------------------------------------|
| Immediata        | Immediatament                                     |
| Retardada        | Quan haguem de reemplaçar un block i `Dirty == 1` |

| Escriptura - Miss | Posem la dada a MC?  |
|-------------------|----------------------|
| Amb assignació    | Sí, i l'editem allà  |
| Sense assignació  | No, ignorem la cache |


Per tant, queden tres tipus coherents:

| Escriptura (H + M)                  | Caracteristiques                                                  |
|-------------------------------------|-------------------------------------------------------------------|
| Immediata amb assignació (<-- Mars) | Sempre ho fem tot per la MC, duplicant a la MP                    |
| Immediata sense assignació          | Només toquem la MC en cas de HIT                                  |
| Retardada amb assignació            | Sempre ho fem tot per la MC, però la MP no està sempre up-to-date |

Visualitzats amb aquesta taula:

| MP \\ MC  | Amb assignació                       | Sense assignació  |
|-----------|--------------------------------------|-------------------|
| Immediata | Sempre toquem MC, MP **up**-to-date  | Només MC per Hits |
| Retardada | Sempre toquem MC, MP **out**-of-date | ∅                 |


## Mesurant la eficàcia
Volem mirar $t_{accès}$ per raons obvies.

Dos casos:
- Hit: $t_{accès} = t_h$
- Miss: $t_{accès} = t_h + t_p$

Ara veurem com trobar el temps de penalització $t_p$.

## Com trobar el temps de penalització $t_p$
Dos camins a recorrer: `CPU <-> MC` i `MC -> MP || MC <- MP`(anoments $t_h$ i $t_{block}$. Ambdos depenen de la política d'escriptura.

Tots els casos son: `todo!()` (el PDF els explica molt bé, em fa pal copiar-ho ara a les tantes de la matinada)

## On guardem els blocks?
Hi ha més casos apart de la directa: la associativa (Free for All), la associativa per conjunts (Teams vs Teams)
