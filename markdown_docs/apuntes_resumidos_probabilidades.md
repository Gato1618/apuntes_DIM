```theme-toggle

```

# Parte 1: Espacios de probabilidades

>[!blue]- Definición: Estrucutra de $\sigma-álgebra$ 
>Sea $\Omega$ un conjunto y $\mathscr{B} \subset P(\Omega) = 2^{\Omega}$, decimos que $\mathscr{B}$ es una $\sigma-álgebra$ si y solo sí:
>1) $\emptyset \; ,\; \Omega\in\mathscr{B}$.
>2) $A\in\mathscr{B}\Rightarrow A^c\in\mathscr{B}$.
>3) $(A_i)_{i\in I}\subset \mathscr{B}$ con $I$ numerable, entonces, $\bigcup_{i\in I}A_i\in\mathscr{B}$.

>[!blue]- Definición: Probabilidad 
>Se dice que $\mu:\mathscr{B}\rightarrow[0,1]$ con $\mathscr{B}$ una $\sigma-álgebra$ de $P(\Omega)$ es una *probabilidad* si verifica:
>1) $\mu(\Omega) = 1$ (Se puede definir con: $\mu(\emptyset)=0$).
>2) Si $(A_i)_{i\in I}$ colección númerable disjunta en $\mathscr{B}$ entonces $\mu(\bigcup_{i\in I}A_i)=\sum_{i\in I}\mu(A_i)$.

>[!blue]- Definición: Espacio de probabilidad
>Es una tripleta $(\Omega,\mathscr{B},\mu)$ donde $\Omega$ conjunto, $\mathscr{B}\subset P(\Omega)$ $\sigma-álgebra$ y $\mu:\mathscr{B}\rightarrow[0, 1]$ probabilidad.

>[!cian]- Propiedad: Intersección de una familia de $\sigma-álgebra$
>Sean $(B_{\lambda})_{\lambda \in \Lambda}$ una familia de $\sigma-álgebra$ de $\Omega$ se tiene que, $\mathscr{B} = \bigcap_{\lambda\in\Lambda}B_\lambda$ es $\sigma-álgebra$.
>>[!green]- Comentario:
>>La union de $\sigma-álgebra$ no necesariamente es $\sigma-álgebra$.

>[!blue]- Definición: $\sigma-álgebra$ engendrada
>Sea $\Omega$ conjunto (no vacío) y $\mathscr{C}\subset P(\Omega)$ una clase de subconjuntos de $\Omega$ se define: $\sigma(\mathscr{C})$ como la $\sigma-álgebra$ más pequeña que contiene a $\mathscr{C}$,  $\sigma(\mathcal{C}) = \bigcap_{(B\:\sigma-álgebra\: que contiene\: a\: \mathscr{C})} B$.

>[!yellow]- Observación: Algunas propiedades del $\sigma-álgebra$ engendrada
>1) $\mathscr{C}\subset\mathscr{C'} \Rightarrow \sigma(\mathscr{C})\subset\sigma(\mathscr{C'})$.
>2) Si $\mathscr{C}$ es $\sigma-álgebra$, $\sigma(\mathscr{C})=\mathscr{C}$.
>3) Como la union no es $\sigma-álgebra$ en general se define: ${\large{\mathsf{V}}_{\lambda\in\Lambda}}B_{\lambda} = \sigma(\bigcup_{\lambda\in\Lambda}B_\lambda)$.

>[!purple]- Ejemplo: Algunas  importantes
>1)$\Omega=\mathbb{R}$: En general usamos $\mathscr{B}(\mathbb{R})$ que es la $\sigma-álgebra$ más pequeña de $\mathscr{C}=\{\:[a,b):a,b\in\mathbb{R}.a<b\}$.
>2)$\Omega=\mathbb{R}^n$: En general usamos $\mathscr{B}(\mathbb{R}^n)$ = $\sigma(\{intervalos\:cartesianos\:de\:\mathbb{R}^2\})$.

>[!blue]- Definición: $\sigma-álgebra$ del producto
>1) Para conjuntos finitos: En general si $\Omega = \tilde{\Omega}\times\tilde{\Omega}\times\cdot\cdot\cdot\times\tilde{\Omega}$, y $\tilde{\mathscr{B}}$ es una $\sigma-álgebra$ de $\tilde{\Omega}$, se define la $\sigma-álgebra$ producto en $\Omega$, $\mathscr{B}=\tilde{\mathscr{B}}\times\cdot\cdot\cdot\times\tilde{\mathscr{B}}=\sigma(\mathscr{C})$ con $\mathscr{C}=\{A_1\times\cdot\cdot\cdot\times A_{l}\mid A_1,...,A_{l}\in\tilde{\mathscr{B}}\}$. 
>2) Para conjuntos numerables: $\Omega={\large \mathsf{X}}_{i\geq1}\tilde{\Omega}$, y $\mathscr{B}={\large \mathsf{X}}_{i\geq1}\tilde{\mathscr{B}}_{i}=\sigma(\{{\large \mathsf{X}}_{i\geq1}A_i\mid\forall i\geq1,A_i\in\tilde{\mathscr{B}}\})$.
>>[!cian]- Propiedad
>>$\mathscr{B}=\sigma(\{{\large \mathsf{X}}_{i\geq1}A_i\mid\forall i\geq1,A_i\in\tilde{\mathscr{B}},\exists I\subset \mathbb{N}\:finito,\:tal\,que\:\forall i\in\mathbb{N}-I,A_i=\tilde{\Omega}\})$ Al conjunto contenido en la $\sigma$ se denomina Cilindro.

>[!cian]- Propiedades: De las probabilidades
>Dado un espacio de probabilidad $(\Omega,\mathscr{B},\mu)$:
>1) Si $A\in\mathscr{B},\;\mu(A^{c})=1-\mu(A)$.
>2) Si $A,\,B\in\mathscr{B},\;\mu(A\cup B)=\mu(A)+\mu(B)-\mu(A\cap B)$.
>3) Desigualdad  de Boole (finita): Si $(A_i)^{n}_{i=1}$ en $\mathscr{B}$ entonces $\mu(\bigcup^{n}_{i=1}A_{i})\leq\sum^{n}_{i=1}\mu(A_i)$.
>4) Monotonía: $A,\,B\in\mathscr{B}$, tal que, $A\subset B\Rightarrow\mu(A)\leq\mu(B)$.
>
>>[!cian]- Corolario
>>$\mu(B-A)=\mu(B)-\mu(A)$, si $A\subset B$.
>
>5) Familias crecientes y decreciente: $(A_i)_{i\geq1}$ en $\mathscr{B}$ se dice:
>	- *Creciente* si $\forall i\geq1,\,A_{i}\subset A_{i+1}$ ($\uparrow$).
>	- *Decreciente* si $\forall i\geq2,\,A_{i}\subset A_{i-1}$ ($\downarrow$).
>	Entonces, 
>	- Si $(A_i)_{i\geq1}$ es creciente se define: $\lim_{n\rightarrow\infty}\uparrow A_{n}=\bigcup_{n\geq1}A_n$.
>	- Si $(A_i)_{i\geq1}$ es decreciente se define: $\lim_{n\rightarrow\infty}\downarrow A_{n}=\bigcap_{n\geq1}A_n$.
>	- Si $(A_i)_{i\geq1}$ es creciente, $\mu(\bigcup_{n\geq1}A_n)=\lim_{n\rightarrow\infty}\mu(A_n)$.
>	- Si $(A_i)_{i\geq1}$ es decreciente, $\mu(\bigcap_{n\geq1}A_n)=\lim_{n\rightarrow\infty}\mu(A_n)$.
>6) Desigualdad de Boole (numerable): $\mu(\bigcup_{i\geq1}A_{i})\leq\sum_{i\geq1}\mu(A_i)$.
>7) $\limsup$ y $\liminf$: Sea $(A_i)_{i\geq1}$ una familia de conjuntos en $\mathscr{B}$. Se define:
>	- $\limsup_{n\rightarrow\infty}A_n=\bigcap_{n\geq1}\bigcup_{m\geq n}A_m$ ($\omega\in\limsup_{n\rightarrow\infty}A_n\Leftrightarrow\forall n\geq1,\exists m\geq n,\omega\in A_m$) En palabras más simples: $\omega$ ocurre en una infinidad de $A_m$'s.
>	- $\liminf_{n\rightarrow\infty}A_n=\bigcup_{n\geq1}\bigcap_{m\geq n}A_m$ ($\omega\in\liminf_{n\rightarrow\infty}A_n\Leftrightarrow\exists n\geq1,\forall m\geq n,\omega\in A_m$) En palabras más simples: $\omega$ pertenece a todos los $A_m$'s, salvo una contidad finita.
>	- Claramente, $\bigcap_{n\geq1}A_n\subset\liminf_{n\rightarrow\infty}A_n\subset\limsup_{n\rightarrow\infty}A_n\subset\bigcup_{n\geq1}A_n$.

>[!cian]- Algunos cálculos: Lema de Borel-Cantelli
>1) $\mu(\liminf_{n\rightarrow\infty}A_{n)}=\lim_{n\rightarrow\infty}\uparrow \mu(\bigcap_{n\geq m}A_{n})$. 
>2) $\mu(\limsup_{n\rightarrow\infty}A_{n)}=\lim_{n\rightarrow\infty}\downarrow \mu(\bigcup_{n\geq m}A_{n})$. 
>3) *Lema de Borel-Canrelli* (convergente): $\sum_{i\geq1}\mu(A_i)<\infty\Rightarrow\mu(\limsup_{n\rightarrow\infty}A_{n})=0$.

>[!blue]- Definición: Probabilidades condicionales 
>Sea $A\in\mathscr{B}$ la probabilidad de $A$ dado $B$ es, $\mu(A\mid B) = \frac{\mu(A\cap B)}{\mu(B)}\in[0,1]$.

>[!blue]- Definición: Conjuntos independientes
>Decimos que $A,\,B\in\mathscr{B}$ son independientes para $\mu$, si se cumple: $\mu(A\cap B)=\mu(A)\cdot\mu(B)$ si $\mu(B)\neq0$, esto es lo mismo que $\mu(A\mid B)=\mu(A)$.

>[!cian]- Algunos cálculos
>1) $\mu(A_{1}\cap A_2\cap\cdot\cdot\cdot\cap A_{n})=\mu(A_{1})\cdot\mu(A_{2}\mid A_{1})\cdot\mu(A_{3}\mid A_{1}\cap A_{2})\cdot\;...$.
>2) Fórmula de probabilidades totales: Sea $(B_i)^{n}_{i=1}$ una partición en $\mathscr{B}$ de $\Omega$. Es decir, $B_{i}\cap B_{j}=\emptyset$ para $i\neq j$, $\bigcup^{n}_{i=1}B_i=\Omega$, $B_{i}\in\mathscr{B}$ Se tiene que: Si $A\in\mathscr{B},\,\mu(A)=\sum^{n}_{i=1}\mu(A\cap B_{i})$ si $\mu(B_{i})\neq0, \mu(A)=\sum^{n}_{i=1}\mu(B_{i})\cdot\mu(A\mid B_{i})$.
>3) Fórmula de Bayes: Sean $A\in\mathscr{B}$ y $(B_{i})^{n}_{i=1}$ partición de $\mathscr{B}$ de $\Omega$, $\mu(B_{i}\mid A)=\large\frac{\mu(B_i)\cdot\mu(A\mid B_i)}{\sum^{n}_{j=1}\mu(B_{j})\cdot\mu(A\mid B_{j})}$.

>[!blue]- Definición: Conjuntos independientes 
>Si $(\Omega,\mathscr{B},\mu)$ es *e.p* y $A_{1},...,A_{n}\in\mathscr{B}$ se dice que $A_{1}, ..., A_{n}$ son idenpendientes si y solo sí $\forall I\subset\{1,...,n\}\;\mu(\bigcap_{i\in I}A_{i}) = \prod_{i\in I}\mu{A_i}$.
>>[!cian]- Propiedad
>>Si $A_{1},...,A_{n}$ son independientes entonces $A_{1}^{c},...,A_{n}^{c}$ son independientes, o cualquier combinación de conjuntos y complementos.





