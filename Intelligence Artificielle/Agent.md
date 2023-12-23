
```ad-definition

Un **agent** est une entité qui **perçoit** et **agis**. Il est **rationnel** si il choisit l'action qui maximize l'utilitée attendue.
Un **agent** perçoit sont **environnement** à travers les **capteurs** _(sensors)_ et agis grâce aux **actionneurs** _(actuators)_.

![[Screenshot 2023-09-15 192346.png]]

```

## Fonction d'agent

```ad-definition

La **fonction d'agent** attribue une action en fonction de ce que l'agent perçoit. $f : P^{*} \rightarrow A$

```

## Programme d'agent

```ad-definition

Le **programme d'agent** $l$ s'exécute sur une machine $M$ et implémente $f$ :$f = Agent(l,M)$. 
_$f$ dépend de $M$ et $l$_

```

## Rationalité

```ad-definition

La **rationalité** peut être définie comme la capacité d'un agent à prendre des décisions logiques et efficaces dans le but d'atteindre ses objectifs. Contrairement à l'omniscience, les agents rationnels ne possèdent pas une connaissance totale, mais sont plutôt limités par les perceptions disponibles. Ils ne sont pas clairvoyants, ce qui signifie qu'ils peuvent manquer de connaissances sur la dynamique de l'environnement.

Les agents rationnels explorent et apprennent, particulièrement dans des environnements inconnus, afin d'améliorer leur performance. Bien que les agents rationnels ne commettent pas d'erreurs intrinsèques, leurs actions peuvent néanmoins être infructueuses. En outre, la rationalité implique une autonomie croissante à mesure que les agents apprennent, ce qui signifie qu'ils transcendent progressivement leur programme initial pour baser davantage leur comportement sur leur propre expérience.

```

## Environnement de Tâche - PEAS

- **Performance measure:** les points que l'agents qui gagne ou perd en fonction de ce qu'il se produit dans l'environnement
- **Environment:** ce dans quoi l'agent se trouve et peut interagir avec
- **Actuators:** les actions que l'agent peut faire
- **Sensors:** l'environnement visible pour l'agent

## Types d'environnements

- **L'observabilitée:** complètement ou partiellement observable, si l'environnement et les capteurs sont les même ou pas.
- **Les agents:** simple ou multiple, si l'environnement contient plusieurs agents.
- **Déterminisme:** déterministe ou stochastique, la manière dont l'agent choisi ses actions.
- **Système:** statique ou dynamique, si l'agent ne fait rien, comment évolue le système.
- **Milieu:** discret ou continu, les actions sont discrètes ou continues
- **Physique**: si elle est connue ou pas
- **Performance measure:** si elle est connue ou pas

## Design de l'agent

- **Partiellement observable:** l'agent a besoin de mémoire.
- **Stochastique:** l'agent peut être amené à se préparer à des éventualités.
- **Multi-agent**: l'agent peut être amené à se comporter de manière aléatoire.
- **Système statique:** l'agent a le temps de prendre une décision rationnelle.
- **Temps continu:** contrôleur à fonctionnement continu
- **Physique inconnue**: besoin d'exploration.
- **Performance measure inconnue:** observer/interagir avec le principal humain

## Types d'agents

### Simple reflex agent
![[Pasted image 20230918182833.png]]

### Reflex agent with state
![[Pasted image 20230918183012.png]]

### Goal based agent
![[Pasted image 20230918183128.png]]

### Utility based agent
![[Pasted image 20230918183212.png]]
