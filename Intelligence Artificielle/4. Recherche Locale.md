## Hill Climbing

```ad-definition

**Hill Climbing** est une méthode simple et générale utilisée pour trouver un optimum local d'une fonction. Le processus peut être décrit de la manière suivante :

1. **Commencer n'importe où :** L'algorithme commence à partir d'un point initial quelconque dans l'espace de recherche.
    
2. **Répéter :** L'algorithme répète itérativement les étapes suivantes.
    
    - **Se déplacer vers le meilleur état voisin :** L'algorithme se déplace vers l'état voisin qui est évalué comme étant le meilleur parmi les voisins actuels.
        
    - **Si aucun voisin n'est meilleur :** Si aucun voisin n'est évalué comme étant meilleur que l'état actuel, l'algorithme quitte la recherche, considérant qu'il a atteint un optimum local.
```

![[Pasted image 20231223092640.png]]

## Maximum local et global

![[Pasted image 20231223092836.png]]


## Simulated Annealing

```ad-definition

Le **simulated annealing** est un algorithme qui ressemble au processus de recuit utilisé pour refroidir les métaux lentement afin d'atteindre un état ordonné à basse énergie. L'idée de base de l'algorithme est la suivante :

1. **Permettre des mouvements "mauvais" occasionnellement :** L'algorithme permet occasionnellement des mouvements qui ne conduisent pas à une amélioration immédiate de la solution. La probabilité d'accepter ces "mauvais" mouvements dépend d'une variable appelée "température".
    
2. **Température élevée => plus de mouvements "mauvais" autorisés :** À des températures élevées, l'algorithme autorise davantage de mouvements "mauvais". Cela permet de secouer le système de son optimum local et d'explorer d'autres régions de l'espace de recherche.
    
3. **Réduction progressive de la température selon un calendrier :** La température est progressivement réduite selon un calendrier prédéfini. À mesure que la température diminue, la probabilité d'accepter des mouvements "mauvais" diminue également.
    
4. **Objectif :** L'objectif final est d'atteindre une température suffisamment basse pour converger vers une solution de haute qualité, tout en permettant au processus d'explorer différentes régions de l'espace de recherche à des stades plus chauds.

```

![[Pasted image 20231223093259.png]]

## Local Beam Search

```ad-definition

La **local beam search** consiste à créer $K$ copies d'un algorithme de recherche locale, initialement initialisées de manière aléatoire. À chaque itération de l'algorithme, les étapes suivantes sont répétées :

1. **Générer TOUS les successeurs à partir des $K$ états actuels :** Pour chaque copie de l'algorithme, générer tous les successeurs possibles à partir de son état actuel.
    
2. **Choisir les meilleurs $K$ parmi ces successeurs :** Sélectionner les $K$ meilleurs successeurs parmi l'ensemble des successeurs générés. Ces $K$ successeurs deviennent les nouveaux états actuels.

```

```ad-exemple

- $K=4$
	![[Pasted image 20231223093709.png]]

```

## Genetic algorithms

```ad-definition

Les **genetic algorithms** utilisent une métaphore de la sélection naturelle pour résoudre des problèmes d'optimisation. Le processus global peut être décrit comme suit :

1. **Échantillonnage de K individus à chaque étape (sélection) :** À chaque itération de l'algorithme, une population de $K$ individus est sélectionnée pour participer au processus évolutif. La sélection se fait de manière pondérée par une fonction de `fitness`, qui mesure la performance de chaque individu dans la résolution du problème.
    
2. **Combinaison par des opérateurs de croisement en paire, plus une mutation pour introduire de la variété :** Les individus sélectionnés sont combinés en utilisant des opérateurs de croisement en paire, simulant le processus de recombinaison génétique. Le croisement permet de combiner les caractéristiques des parents pour créer une nouvelle génération d'individus. De plus, une opération de mutation est appliquée de manière aléatoire sur certains individus pour introduire de la variété génétique.

```

```ad-exemple

![[Pasted image 20231223094137.png]]

```

![[Pasted image 20231223094155.png]]

