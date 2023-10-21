
```ad-tldr
title: Définition
color: 255, 100, 100

Un **litéral** est une variable $x$ ou sa négation $\lnot x$

```

```ad-tldr
title: Définition
color: 255, 100, 100

Une **clause** est une disjonction de littéraux $l_{1}\lor\dots\lor l_{n}$. Elle est satisfaite par une valuation $V$ s’il existe $i$ tel que $V(l_{i})=1$. Par extension, on appelle $\bot$ la *clause vide*, qui est insatisfaisable.

```

```ad-tldr
title: Définition
color: 255, 100, 100

Un **ensemble de clauses** $A=\{C_{1},\dots,C_{n}\}$ est satisfait par une valuation $V$, noté $V \vDash A$, si pour tout $i$, $V\vDash C_{i}$. En particulier, toute valuation satisfait l’ensemble vide $A=\emptyset$

```

## Formes normales

```ad-tldr
title: Forme Normale Conjonctive (FNC)
color: 255,255,100

Une **formule** est en forme normale **conjonctive** si et seulement si c’est une **conjonction de disjonctions** de littéraux, de la forme: $\bigwedge_{i}(\bigvee_{j}(\lnot)x_{i,j})$

```

```ad-example
title: Exemple
color: 180, 180, 180
- $(\phi \lor \psi) \land (\lnot \phi \lor \lnot \psi)$ 
```

```ad-tldr
title: Forme Normale Disjonctive (FND)
color: 255,255,100

Une **formule** est en forme normale **disjonctive** si et seulement si c’est une **disjonction de conjonctions** de littéraux, de la forme: $\bigvee_{i}(\bigwedge_{j}(\lnot)x_{i,j})$

```

```ad-example
title: Exemple
color: 180, 180, 180
- $(\phi \land \psi) \lor (\lnot \phi \land \lnot \psi)$ 
```

```ad-tldr
title: Lemme
color: 255,255,100

Tout ensemble non-vide de clauses $A=\{C_{1},\dots,C_{n}\}$ est équivalent à la formule en **FNC** $\phi_{A} = \bigwedge^{n}_{i=1} C_{i}$, au sens où pour toute valuation, $V\vDash A$ si et seulement si $V \vDash \phi_{A}$

```





#TODO 