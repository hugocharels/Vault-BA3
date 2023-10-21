## Formalisation logique

```ad-definition
$q$ est une **conséquence logique** de $p$ est noté $p \models q$
```

## Construction de formules

Le vocabulaire du langage de la logique propositionnelle est composé :
- d’un ensemble, fini ou dénombrable, de propositions notées $x,y,z,\dots$
- de deux constantes : vrai $\top$ et faux $\bot$, parfois notée $1$ ou $0$
- d’un ensemble de connecteur logique : et $\land$, ou $\lor$, non $\lnot$, implique $\implies$, équivalent $\iff$ 
- les parenthèses : $(.)$

$$
\phi ::= \top | \bot | \phi_{1} \land \phi_{2} | \phi_{1} \lor \phi_{2} | \phi_{1} \implies \phi_{2} | \phi_{1} \iff \phi_{2} | \lnot \phi_{1} | (\phi_{1})
$$

## Règle de précédence

Ordre de précédence $\prec$ sur les opérateurs :
$$
\iff \prec \implies \prec \lor \prec \land \prec \lnot
$$
et associativité à gauche pour $\iff, \lor, \land$ et à droite pour $\implies$

```ad-example
title: Exemple
color: 180, 180, 180

$x \implies y \land z \implies t \equiv x \implies ((y \land z) \implies t)$

![[Pasted image 20231011222212.png]]

```

## La sémantique

```ad-definition
La valeur de vérité d’une formule propositionnelle $\phi$ formée à partir des propositions d’un ensemble $X$, évaluée avec la fonction d’interprétation $V$, est notée $[[\phi]]_{V}$. En particulier, on a $[[\phi]]_{V} \in \{0, 1\}$.
La fonction $[[\phi]]_{V}$ est définie par induction sur la syntaxe de $\phi$ de la façon suivante :
- $[[\top]]_{V} = 1; \quad [[\bot]]_{V} = 0; \quad [[x]]_{V} = V(x)$
- $[[\neg \phi]]_{V} = 1- [[\phi]]_{V}$ 
- $[[\phi_{1} \lor \phi_{2}]]_{V} = \max([[\phi_{1}]]_{V},[[\phi_{2}]]_{V})$
- $[[\phi_{1} \land \phi_{2}]]_{V} = \min([[\phi_{1}]]_{V},[[\phi_{2}]]_{V})$
- $[[\phi_{1} \implies \phi_{2}]]_{V} = \max([[1 - \phi_{1}]]_{V},[[\phi_{2}]]_{V})$
- $[[\phi_{1} \iff \phi_{2}]]_{V} = \min([[\phi_{1} \implies \phi_{2}]]_{V}, [[\phi_{2} \implies \phi_{1}]]_{V})$

Nous notons $V \models \phi$ si seulement si $[[\top]]_{V} = 1$, qui se lit « $V$ satisfait $\phi$ »

```

```ad-example
title: Exemple
color: 180, 180, 180

Pour $V_{1}(x)=0$
- $[[x]]_{V_{1}} = 0 \quad [[\neg x]]_{V_{1}} = 1 \quad [[x \land x]]_{V_{1}} = 0 \quad [[x \land \lnot x]]_{V_{1}} = 0$
- $[[x \implies x]]_{V_{1}} = 1 \quad [[x \iff x]]_{V_{1}} = 1 \quad [[\lnot x \implies x]]_{V_{1}} = 0$

```

## Validité et Satisfiabilité

```ad-definition

Une formule propositionnelle $\phi$ est **satisfaisable** si et seulement si il existe une fonctionne d’interprétation $V$ pour les propositions de $\phi$, telle que $V \models \phi$.

```

```ad-definition

Une formule propositionnelle $\phi$ est **valide** si et seulement si pour toute fonction d’interprétation $V$ pour les propositions de $\phi$, on a $V \models \phi$.

```

```ad-definition

Soit $\phi_{1}, \dots, \phi_{n}, \phi$ des formules. On dira que $\phi$ est une conséquence logique de $\phi_{1}, \dots, \phi_{n} \models \phi$, si $(\phi_{1} \land \dots \land \phi_{n}) \implies \phi$ est valide.

```

```ad-definition

Deux formules $\phi$ et $\psi$ sont dites équivalentes si la formule $\phi \iff \psi$ est valide. On notera $\phi \equiv \psi$ pour signifier que $\phi$ et $\psi$ sont équivalentes.

```

```ad-theorem
title: Théorème d’incomplétude de Gödel

Une formule propositionnelle $\phi$ est valide si et seulement si sa négation $\lnot \phi$ n’est pas satisfaisable.

```

```ad-demonstration

Nous devons démontrer une équivalence. On peut donc supposer ce qui est à gauche de l’équivalence et en déduire ce qui est à droite, et réciproquement.
- Supposons que $\phi$ est valide. Alors pour tout interprétation $V$, on a $V \models \phi$. Donc $V \not\models \lnot \phi$. Comme pour toute interprétation quelconque $V$, cela signifie que $\lnot \phi$ n’est pas satisfaisable.
- Réciproquement, supposons que $\lnot \phi$ ne soit pas satisfaisable. Alors pour toute interprétation $V$ quelconque, $V \not\models \lnot\phi$, donc $V \models \phi$. De nouveau, comme c’est pour toute interprétation quelconque $V$, on en déduit que $\phi$ est valide.

```

![[Pasted image 20231011224127.png]]

## Tableaux sémantiques

```ad-definition

Un **littéral** est une proposition $x$ ou la négation d’une proposition $\lnot x$.

- Un ensemble $S$ de littéraux est satisfaisable si et seulement si il ne contient pas une paire de littéraux complémentaires. Par exemple, $\{x, \lnot y\}$ est satisfaisable alors que $\{x, \lnot x\}$ ne l’est pas.
- Nous avons réduit le problème de satisfaction de $\phi$ à un problème de satisfaction d’ensemble de littéraux : $\phi$ est satisfaisable si et seulement si $\{x, \lnot y\}$ est satisfaisable ou $\{x, \lnot x\}$ est satisfaisable.

```

### Représentation en arbre

#TODO
