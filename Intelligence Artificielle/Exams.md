# 2. Algorithme de recherche simple

```ad-rule
title: Description d'un problème


1. $S$ : l'espace d'état
2. $s_0$ : l'état initial
3. $A(s)$ : un ensemble d'action pour chaque état
4. $T(s,a)$ : un modèle de transition
5. $G(s)$ : une fonction de test d'objectif
6. $c(s, a, s')$ : une fonction de coût d'action


```

```ad-exemple

![[Pasted image 20231225112149.png]]

1. $S$ : n'importe quelle configuration des six blocs
2. $s_0$ : l'état initial est celui de gauche sur l'image
3. $A(s)$ : prendre un bloc et le déplacé
4. $T(a, s)$ : 
5. $G(s)$ : vérifie que l'état est équivalent a celui de droite sur l'image
6. $c(s, a, s')$ : $1$, chaque mouvement a un coût de $1$

```


# 3. Algorithme de recherche informés

```ad-definition

**Une heuristique est admissible** si, pour tout nœud $n$ dans l'espace de recherche, la valeur de $h(n)$ est comprise entre $0$ et $h^∗(n)$. Ici, $h^∗(n)$ représente le coût réel du chemin optimal du nœud $n$ au but le plus proche.

Formellement, l'admissibilité est définie comme suit : $0\leq h(n) \leq h^*(n)$

```

```ad-definition

**Une heuristique est consistante** si, elle est admissible et si l'heuristique de l'état $s$ moins celui de l'état $s'$ est inférieure ou égale au coût réel. C'est à dire $h(s) - h(s') \leq c(s, a, s')$ ou $h(s) \leq c(s, a, s') + h(s')$

```

# 4. Recherche locale


# 5. Jeux et recherche adversariale

