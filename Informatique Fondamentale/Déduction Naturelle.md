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
	$\begin{align}\\
		& 1. x \land y \sep prem.\\
		& 2. z \space\space\space\tab\sep prem.\\
		& 3. y \space\space\tab\sep \land_{e_2},1\\
		& 4. y \land z \sep \land_{i},2-3\\
	\end{align}$ 
$\space$

- $(x \land y) \land z, t \land h \vdash y \land t$
	#TODO 

```

## La disjonction $(\lor)$

```ad-tldr
title: Règle d’introduction
color: 130,130,255

$$
\frac{\phi}{\phi\lor\psi}\lor_{i_{1}} \quad \frac{\psi}{\phi\lor\psi}\lor_{i_{2}}
$$

```

```ad-tldr
title: Règle d’élimination
color: 130,130,255

#TODO better
$$
\psi_{1} \text{hyp.} \quad \psi_{2} \text{hyp.}
$$
$$
\vdots\quad\vdots
$$
$$
\frac{\psi_{1}\lor\psi_{2}\quad\phi\text{fin hyp.}\quad\phi\text{fin hyp.}}{\phi} \lor_{e}
$$

```

```ad-example
title: Exemple
color: 180, 180, 180
#TODO 
```

## L’implication $(\implies)$

```ad-tldr
title: Règle de L’introduction
color: 130,130,255
#TODO better
$$
\phi \quad \text{hyp.}
$$
$$
\vdots
$$
$$
\frac{\psi \quad \text{fin hyp.}}{\phi\implies\psi}\implies_{i}
$$
```

```ad-tldr
title: Règle d’élimination (Modus Ponens)
color: 130,130,255
$$
\frac{\phi\quad\phi\implies\psi}{\psi}\implies_{MP}
$$

_Si j’ai une preuve de $\phi$ et une preuve de $\phi\implies\psi$ alors j’ai une preuve de $\psi$_

$\implies_{MP}$ _ est parfois noté _ $\implies_{e}$

```

```ad-example
title: Exemple
color: 180, 180, 180

- $x, x\implies y, x\implies (y\implies z) \vdash z$
#TODO 

- $x\implies(y\implies z), x, \lnot z, \vdash \lnot y$
#TODO

```

## La négation $(\lnot)$

```ad-tldr
title: Règle d’introduction
color: 130,130,255

$$
\phi\quad\text{hyp.}
$$
$$
\vdots
$$
$$
\frac{\bot\quad\text{fin hyp.}}{\lnot\phi}\lnot_{i}
$$

```

```ad-tldr
title: Règle d’élimination
color: 130,130,255

$$
\frac{\phi\quad\lnot\phi}{\bot}\lnot_{e}
$$

```

```ad-example
title: Exemple
color: 180, 180, 180
#TODO 
```

## Le faux $(\bot)$

```ad-tldr
title: Règle d’élimination
color: 130,130,255

$$
\frac{\bot}{\phi}\bot_{e}
$$

```

```ad-example
title: Exemple
color: 180, 180, 180
#TODO 
```

## La double négation $(\lnot\lnot)$

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

_Si j’ai une preuve de $\lnot\lnot\phi$ alors j’ai aussi une preuve de $\phi$_

```

```ad-example
title: Exemple
color: 180, 180, 180

#TODO 

```

## Le si et seulement si $(\iff)$

```ad-tldr
title: Règle d’introduction
color: 130,130,255
$$
\frac{\phi_{1}\implies\phi_{2}\quad\phi_{2}\implies\phi_{1}}{\phi_{1}\iff\phi_{2}}\iff_{i}
$$

```

```ad-tldr
title: Règle d’élimination
color: 130,130,255
$$
\frac{\phi_{1}\iff\phi_{2}}{\phi_{1}\implies\phi_{2}}\iff_{e_{1}}\quad
\frac{\phi_{1}\iff\phi_{2}}{\phi_{2}\implies\phi_{1}}\iff_{e_{2}}
$$

```

```ad-example
title: Exemple
color: 180, 180, 180
#TODO 
```

## Règles dérivées

```ad-tldr
title: Règle d’introduction du LEM
color: 130,130,255
$$
\frac{}{\phi\lor\lnot\phi} LEM
$$

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
#TODO 
```
