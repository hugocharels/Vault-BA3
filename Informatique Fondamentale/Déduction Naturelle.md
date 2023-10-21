## La conjonction $(\land)$

```ad-rule
title: Règle d’introduction
$$
\frac{\phi\quad\psi}{\phi\land\psi} \land_{i}
$$
_Si j’ai une preuve de $\phi$ et une preuve de $\psi$ alors j’ai une preuve de $\phi\land\psi$_.

```

```ad-rule
title: Règle d’élimination
$$
\frac{\phi\land\psi}{\phi}\land_{e_{1}} \quad \frac{\phi\land\psi}{\psi}\land_{e_{2}}
$$

_Si j’ai une preuve de $\phi\land\psi$ alors j’ai une preuve de $\phi$ et de $\psi$_.

```

```ad-exemple

- $x \land y, z \vdash y \land z$
	$\begin{align}\\
		& 1. x \land y \sep prem.\\
		& 2. z \space\space\space\tab\sep prem.\\
		& 3. y \space\space\tab\sep \land_{e_2},1\\
		& 4. y \land z \sep \land_{i},2-3\\
	\end{align}$ 
$\space$

- $(x \land y) \land z, t \land h \vdash y \land t$
	$\begin{align}\\
		& 1. (x \land y) \land z \sep prem.\\
		& 2. t \land h \space\space\sep\sep prem.\\
		& 3. x \land y \sep\sep \land_{e_1},1\\
		& 4. y \space\space\space\tab\sep\sep \land_{e_2},3\\
		& 5. t \space\space\space\tab\sep\sep \land_{e_1},2\\
		& 6. y \land t \space\sep\sep \land_{i},4-5\\
	\end{align}$

```

## La disjonction $(\lor)$

```ad-rule
title: Règle d’introduction

$$
\frac{\phi}{\phi\lor\psi}\lor_{i_{1}} \quad \frac{\psi}{\phi\lor\psi}\lor_{i_{2}}
$$

```

```ad-rule
title: Règle d’élimination

$$
\sep\psi_{1} \quad \text{hyp.} \sep \psi_{2} \quad \text{ hyp.}
$$
$$
\vdots \sep\sep\tab \vdots
$$
$$
\frac{\psi_{1}\lor\psi_{2}\quad\phi\text{ fin hyp.}\quad\phi\text{ fin hyp.}}{\phi} \lor_{e}
$$

```

```ad-exemple
#TODO 
```

## L’implication $(\rightarrow)$

```ad-rule
title: Règle de L’introduction
$$
\phi \quad \text{hyp.}
$$
$$
\vdots\sep
$$
$$
\frac{\psi \quad \text{fin hyp.}}{\phi\rightarrow\psi}\rightarrow_{i}
$$
```

```ad-rule
title: Règle d’élimination (Modus Ponens)
$$
\frac{\phi\quad\phi\rightarrow\psi}{\psi}\rightarrow_{MP}
$$

_Si j’ai une preuve de $\phi$ et une preuve de $\phi\rightarrow\psi$ alors j’ai une preuve de $\psi$_

$\rightarrow_{MP}$ _ est parfois noté _ $\rightarrow_{e}$

```

```ad-exemple

- $x, x\rightarrow y, x\rightarrow (y\rightarrow z) \vdash z$
#TODO 

- $x\rightarrow(y\rightarrow z), x, \lnot z, \vdash \lnot y$
#TODO

```

## La négation $(\lnot)$

```ad-rule
title: Règle d’introduction

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

```ad-rule
title: Règle d’élimination

$$
\frac{\phi\quad\lnot\phi}{\bot}\lnot_{e}
$$

```

```ad-exemple
#TODO 
```

## Le faux $(\bot)$

```ad-rule
title: Règle d’élimination

$$
\frac{\bot}{\phi}\bot_{e}
$$

```

```ad-exemple
#TODO 
```

## La double négation $(\lnot\lnot)$

```ad-rule
title: Règle d’introduction
$$
\frac{\phi}{\lnot\lnot\phi}\lnot\lnot i
$$

_Si j’ai une preuve de $\phi$ alors j’ai aussi une preuve de non non $\phi$_

```

```ad-rule
title: Règle d’élimination
$$
\frac{\lnot\lnot\phi}{\phi}\lnot\lnot e
$$

_Si j’ai une preuve de $\lnot\lnot\phi$ alors j’ai aussi une preuve de $\phi$_

```

```ad-exemple

#TODO 

```

## Le si et seulement si $(\leftrightarrow)$

```ad-rule
title: Règle d’introduction
$$
\frac{\phi_{1}\rightarrow\phi_{2}\quad\phi_{2}\rightarrow\phi_{1}}{\phi_{1}\leftrightarrow\phi_{2}}\leftrightarrow_{i}
$$

```

```ad-rule
title: Règle d’élimination
$$
\frac{\phi_{1}\leftrightarrow\phi_{2}}{\phi_{1}\rightarrow\phi_{2}}\leftrightarrow_{e_{1}}\quad
\frac{\phi_{1}\leftrightarrow\phi_{2}}{\phi_{2}\rightarrow\phi_{1}}\leftrightarrow_{e_{2}}
$$

```

```ad-exemple
#TODO 
```

## Règles dérivées

```ad-rule
title: Règle d’introduction du LEM
$$
\frac{}{\phi\lor\lnot\phi} LEM
$$

```

```ad-rule
title: Règle de contraposition (Modus Tollens)
$$
\frac{\phi\rightarrow\psi\quad\lnot\psi}{\lnot\phi}MT
$$

_Si j’ai une preuve de $\phi\rightarrow\psi$ et une preuve de $\lnot\psi$ alors je peut en déduire $\lnot\phi$_

```

```ad-exemple
#TODO 
```
