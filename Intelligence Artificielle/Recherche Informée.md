![[Pasted image 20230926101649.png]]

```ad-definition

Une **heuristique** est une fonction spécifiquement conçue pour évaluer à quel point un état donné se rapproche d'un objectif. Cette fonction est adaptée à un problème de recherche particulier.

```

## Greedy Search

![[Pasted image 20231223085433.png]]

### Stratégie

| Meilleur cas    | Pire cas    |
| --- | --- |
| ![[Pasted image 20231223085547.png]]    |  ![[Pasted image 20231223085558.png]]   |


## A* Search

![[Pasted image 20231223085741.png]]

### Stratégie

La stratégie A* consiste à développer un nœud $n$ qui a le plus de chances d'être situé sur un chemin optimal. Pour cela, l'algorithme évalue les nœuds en fonction de la somme de deux coûts :

- $g(n)$ représente le coût du chemin du nœud racine jusqu'au nœud $n$.
- $h^*(n)$ représente le coût optimal du nœud $n$ jusqu'au but le plus proche.

L'idée est d'élargir le nœud $n$ qui a la plus faible valeur de $g(n)+h^*(n)$. Cependant, dans la pratique, $h^*(n)$ n'est souvent pas connu, mais on peut utiliser une approximation heuristique $h(n)$ à la place.

Ainsi, l'algorithme A* effectue une recherche dans l'arbre en utilisant une file de priorité où les nœuds sont ordonnés en fonction de la valeur de $f(n)=g(n) + h(n)$, où $h(n)$ est l'heuristique utilisée.

## Admissibilité d'une heuristique 

```ad-definition

Une heuristique $h$ est dite admissible si, pour tout nœud $n$ dans l'espace de recherche, la valeur de $h(n)$ est comprise entre zéro et $h^∗(n)$. Ici, $h^∗(n)$ représente le coût réel du chemin optimal du nœud $n$ au but le plus proche.

Formellement, l'admissibilité est définie comme suit : $0\leq h(n) \leq h^*(n)$

En d'autres termes, une heuristique admissible ne surestime jamais le coût pour atteindre un but à partir d'un nœud donné. Elle fournit toujours une estimation du coût inférieure ou égale au véritable coût optimal.

```


## Comparaison des recherches

| Greedy ($f(n) = h(n)$)               | Uniform Cost ($f(n) = g(n)$)         | A* ($f(n) = g(n)+h(n)$)              |
| ------------------------------------ | ------------------------------------ | ------------------------------------ |
| ![[Pasted image 20231223091035.png]] | ![[Pasted image 20231223091050.png]] | ![[Pasted image 20231223091107.png]] |

## Consistence d'une heuristique

```ad-definition

La **consistance** d'une heuristique repose sur l'idée principale que les coûts heuristiques estimés doivent être inférieurs ou égaux aux coûts réels. Pour être considérée comme consistante, une heuristique doit satisfaire l'admissibilité et l'heuristique doit également satisfaire la consistance, ce qui se traduit par la `triangle inequality` (inégalité triangulaire). Pour chaque arc entre deux nœuds $A$ et $C$, l'heuristique pour $A$ moins l'heuristique pour $C$ doit être inférieure ou égale au coût réel de cet arc.
Formellement : $h(A)-h(C) \leq c(A, C)$ ou $h(A) \leq c(A, C) + h(C)$

La recherche de graphe avec A* est optimale si l'heuristique est consistante.

```

## Tree Search VS Graph Search

![[Pasted image 20231223092005.png]]

![[Pasted image 20231223092055.png]]

