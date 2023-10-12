## La conjonction $(\land)$

```ad-tldr
title: Règle d’introduction
color: 130,130,255
$$
\frac{\phi\quad\psi}{\phi\land\psi} \land_{i}
$$
_Si j’ai une preuve de $\phi$ et une preuve de $\psi$ alors j’ai une preuve de $\phi\land\psi$_.

```

```ad-tldr
title: Règle d’élimination
color: 130,130,255
$$
\frac{\phi\land\psi}{\phi}\land_{e_{1}} \quad \frac{\phi\land\psi}{\psi}\land_{e_{2}}
$$

_Si j’ai une preuve de $\phi\land\psi$ alors j’ai une preuve de $\phi$ et de $\psi$_.

```

```ad-example
title: Exemple
color: 180, 180, 180

- $x \land y, z \vdash y \land z$
	#TODO 
 
- $(x \land y) \land z, t \land h \vdash y \land t$
	#TODO 

```

## La double négation

```ad-tldr
title: Règle d’introduction
color: 130,130,255
$$
\frac{\phi}{\lnot\lnot\phi}\lnot\lnot i
$$

_Si j’ai une preuve de $\phi$ alors j’ai aussi une preuve de non non $\phi$_

```

```ad-tldr
title: Règle d’élimination
color: 130,130,255
$$
\frac{\lnot\lnot\phi}{\phi}\lnot\lnot e
$$

_Si j’ai une preuve de $\not\lnot\phi$ alors j’ai aussi une preuve de $\phi$_

```

```ad-example
title: Exemple
color: 180, 180, 180

#TODO 

```

## L’implication

```ad-tldr
title: Règle d’élimination (Modus Ponens)
color: 130,130,255
$$
\frac{\phi\quad\phi\implies\psi}{\psi}\implies_{MP}
$$

_Si j’ai une preuve de $\phi$ et une preuve de $\phi\implies\psi$ alors j’ai une preuve de $\psi$_

$\implies_{MP}$ _ est parfois noté _ $\implies_{e}$

```

```ad-tldr
title: Règle de contraposition (Modus Tollens)
color: 130,130,255
$$
\frac{\phi\implies\psi\quad\lnot\psi}{\lnot\phi}MT
$$

_Si j’ai une preuve de $\phi\implies\psi$ et une preuve de $\lnot\psi$ alors je peut en déduire $\lnot\phi$_

```

```ad-example
title: Exemple
color: 180, 180, 180

- $x, x\implies y, x\implies (y\implies z) \vdash z$
#TODO 

- $x\implies(y\implies z), x, \lnot z, \vdash \lnot y$
#TODO

```
