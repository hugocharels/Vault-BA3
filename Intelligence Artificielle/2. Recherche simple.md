![[Pasted image 20230926101617.png]]

```ad-definition

Un **agent de planification** est un agent chargé de prendre des décisions en se basant sur l'évaluation de séquences d'actions futures. Ces agents utilisent généralement des algorithmes de recherche qui supposent certains aspects de l'environnement, tels que :

- **Modèle de transition connu et déterministe :** L'agent suppose que les effets des actions sont déterministes et que le modèle de transition entre les états est entièrement connu.
    
- **États et actions discrets :** L'agent opère dans un environnement où les états et les actions sont discrets, permettant une modélisation formelle et une recherche systématique.
    
- **Entièrement observable :** Les états de l'environnement sont entièrement observables par l'agent, ce qui signifie qu'il a une connaissance complète de l'état actuel du système.
    
- **Représentation atomique :** Les états de l'environnement sont représentés de manière atomique, c'est-à-dire qu'ils ne sont pas décomposables en sous-parties indépendantes.
    
- **Objectif défini :** Ces agents ont généralement un objectif défini qu'ils cherchent à atteindre. Cet objectif peut être spécifié explicitement et constitue la base de la planification.
    
- **Optimalité :** Les agents de planification visent généralement à atteindre leur objectif de manière optimale, c'est-à-dire en minimisant le coût associé à la réalisation de l'objectif.

```

```ad-definition

Un **problème de recherche** est composé de :
- Un état d’espace `state space` : $S$
- Un état initial : $s_0$
- D’actions à chaque état : $A(s)$
- D’un modèle de transition : $Result(s,a)$
- D’un test d’objectif : $G(s)$
- Le cout des actions : $c(s,a,s’)$

Une **solution** est une séquence d'action qui mènent à l'objectif.

La **solution optimale** a le coût le plus faible de toutes les solutions.

```

```ad-definition

Un état d’espace est composé de :
- L’état du monde `world state` : tout les éléments de l’environnement
- L’état de recherche `search state` : une abstraction qui ne contient que les éléments nécéssaire
- La taille de l’état d’espace `state space size` : le nombre d’état possible
- Le graph de l’état d’espace `state space graph` : le graphe ou chaque sommet est un état et les arrête désigne les état atteignables depuis celui ci
- L’arbre de recherche `search tree` : crée un arbre depuis le state space graphe (infini si cycle)

```

```ad-example 
title: Exemple
color: 180, 180, 180

- `world state` : ![[Pasted image 20230926092141.png]]
- `search state` : ![[Pasted image 20230926092214.png]]
- `state space size` : ![[Pasted image 20230926092254.png]]
- `state space graph` : ![[Pasted image 20230926092340.png]]
- `search tree` : ![[Pasted image 20230926092448.png]]

```

### Tree Search
 ![[Pasted image 20230926092752.png]]

### Systematic Search

```ad-definition

1. La frontière sépare la région étendue de la région inexplorée du graphe espace-état
2. Expansion d'un noeud de frontière : 
	1. Déplace un noeud de la frontière vers la région étendue 
	2. Ajoute des noeuds de la région inexplorée vers la frontière, en conservant la propriété 1

![[Pasted image 20231223084131.png]]

```

### Complexité des parcours

| Search              | Frontier | Completeness                                            | Optimality | Time               | Space              |
| ------------------- | -------- | ------------------------------------------------------- | ---------- | ------------------ | ------------------ |
| DFS                 | Stack    | tree search - no (cycle) / graph search - yes if (finite) | no         | $O(b^{m})$         | $O(bm)$            |
| BFS                 | Queue    | yes                                                     | no         | $O(b^{s})$         | $O(b^{s})$         |
| Iterative Deepening | Stack    | yes                                                     | no         | $O(b^{s})$         | $O(bs)$            |
| UCS (Dijkstra)                | Heap     | yes                                                     | yes        | $O(b^\frac{c}{e})$ | $O(b^\frac{c}{e})$ |

- $b$ : le nombre d'actions possible pour chaque état (branching factor)
- $m$ : la profondeur maximale
- $s$ : la profondeur de la solution optimale
- $c$ : coût de la solution optimale
- $e$ : coût minimum entre $2$ nodes

