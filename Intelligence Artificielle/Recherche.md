![[Pasted image 20230926101617.png]]

```ad-definition

Un problème de recherche est composé de :
- Un état d’espace « state space » : $S$
- Un état initial : $s_0$
- D’actions à chaque état : $A(s)$
- D’un modèle de transition : $Result(s,a)$
- D’un test d’objectif : $G(s)$
- Le cout des actions : $c(s,a,s’)$

```

```ad-definition

Un état d’espace est composé de :
- L’état du monde « world state » : tout les éléments de l’environnement
- L’état de recherche « search state » : une abstraction qui ne contient que les éléments nécéssaire
- La taille de l’état d’espace « state space size » : le nombre d’état possible
- Le graph de l’état d’espace « state space graph » : le graph ou chaque sommet est un état et les arrête désigne les état atteignables depuis celui ci
- L’arbre de recherche « search tree » : crée un arbre depuis le state space graph (infini si cycle)

```

```ad-example 
title: Exemple
color: 180, 180, 180

- world state : ![[Pasted image 20230926092141.png]]
- search state : ![[Pasted image 20230926092214.png]]
- state space size : ![[Pasted image 20230926092254.png]]
- state space graph : ![[Pasted image 20230926092340.png]]
- search tree : ![[Pasted image 20230926092448.png]]

```

### Tree Search
 ![[Pasted image 20230926092752.png]]

### Complexité des parcours
|Search|Frontier|Completeness|Optimality|Time|Space|
|---|---|---|---|---|---|
|DFS|Stack|tree search - no (cycle) graph search - yes if (finite)|no|$O(b^{m})$|$O(bm)$|
|BFS|Queue|yes|no|$O(b^{s})$|$O(b^{s})$|
|Iterative Deepening|Stack|yes|no|$O(b^{s})$|$O(bs)$|
|UCS|Heap|yes|yes|$O(b^\frac{c}{e})$|$O(b^\frac{c}{e})$|

- $b$ : degré de la racine de l’arbre (branching factor)
- $m$ : la profondeur maximum
- $s$ : la profondeur la plus petite de la solution
- $c$ : coût de la solution optimale
- $e$ : coût minimum entre $2$ nodes

