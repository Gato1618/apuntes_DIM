```theme-toggle

```
# Parte 1: Axiomas de conjuntos

---
## Sec: 8 

>[!blue]- Definición: Igualdad de clases
Si $A, B$ son clases, y $(\forall x, x \in A \Leftrightarrow x \in B)$ entonces $A = B$.

>[!red]-  Axioma 1: De individualidad
Si $x \in \mathcal{A}$ y $x = y$, entonces $y \in \mathcal{A}$

>[!blue]- Definición: Conjunto
Una clase $A$ es un conjunto si existe una clase $\mathcal{A}$ tal que $A \in \mathcal{A}$.

>[!red]- Axioma 2: De formación de clase
Si $p(x)$ es una proposición lógica que involucra variables conjuntos, existe una clase $\mathcal{A}$ tal que $x\in\mathcal{A}\Leftrightarrow x$ es conjunto $\land\; p(x)$.

>[!blue]- Definición: Clase vacía
$\emptyset$ es la clase tal que $\forall\;x\;\neg(x\in\emptyset)$.

>[!red]- Axioma 3: De el conjunto vacío
$\emptyset$ es un conjunto.

>[!red]- Axioma 4: De emparejamiento
Si $A$ y $B$ son conjuntos distintos, la clase $\mathcal{A} = \{x \mid (x = A) \lor (x = B)\}$  es conjunto (Que consta de exactamente dos elementos) Se denota: $\{A, B\}$.

>[!blue]- Definición: Familia de conjuntos
$\mathcal{A}$ es conjunto y para cada $\alpha \in \mathcal{A}, A_{\alpha}$ es conjunto. A los conjuntos de la forma $A_{\alpha}$ se le llama una familia de conjuntos.
> - Union de los conjuntos de la familia: 
$\bigcup_{\alpha}A_{\alpha} = \bigcup_{\alpha \in \mathcal{A}}A_{\alpha} = \{x \mid \exists \alpha \in \mathcal{A}: x \in A_{\alpha}\}$
>
> - Intersección de conjuntos de la familia:
$\bigcap_{\alpha}A_{\alpha} = \bigcap_{\alpha \in \mathcal{A}}A_{\alpha} = \{x \mid \forall \alpha \in \mathcal{A}, x \in A_{\alpha}\}$

>[!red]- Axioma 5: Union
Si $\mathcal{A}$  es un conjunto y $\forall\alpha\in \mathcal{A}, A_{\alpha}$ es un conjunto, entonces $\bigcup_{\alpha \in \mathcal{A}}A_{\alpha}$ es un conjunto.

>[!blue]- Definición: $\mathcal{A} \times \mathcal{B}$
Dadas las clases $\mathcal{A}, \mathcal{B}$, definimos la clase $\mathcal{A} \times \mathcal{B}$ como $\{\{a, \{a, b\}\}\mid a \in \mathcal{A} \land b \in \mathcal{B}\}$.
Al conjunto $\{a,\{a,b\}\}$ lo escribimos como $(a,b)$.

>[!blue]- Definición: Función
Una función $\mathcal{f}$ de $\mathcal{A}$ en $\mathcal{B}$ es una sub-clase de $\mathcal{A} \times \mathcal{B}$ tal que $\forall a \in \mathcal{A}, \exists ! b\in\mathcal{B}$ tal que $(a,b) \in \mathcal{f}$.

>[!red]- Axioma 6: De sustitución
Si $A$ es conjunto y $\mathcal{f}:A \rightarrow \mathcal{B}$ función, $\mathcal{f}(A):= \{b \in \mathcal{B} \mid \exists a \in A \; tq \; (a,b) \in \mathcal{f}\}$ es conjunto.

>[!red]- Axioma 7: De refinamiento
Si $A$ es conjunto y $\mathcal{A}$ es clase, $A\cap\mathcal{A}$ es conjunto.

>[!blue]- Definición: Clase potencia
Si $\mathcal{A}$ es clase, $P(\mathcal{A})=\{A\subset\mathcal{A}\mid A\;es\;conjunto\}$ es clase.
> - Ejemplo:
$A=\{0,1\}, \; P(A) = \{\{0\},\{1\},A,\emptyset\}$

>[!red]- Axioma 8: Del conjunto de potencia
Si $A$ es conjunto, $P(A)$ es conjunto.

>[!cian]- Teorema 8.5
Si $A$ es conjunto y $p(x)$ proposición lógica sobre el conjunto, entonces $\{x \in A \mid p(x)\}$ es conjunto.

>[!cian]- Teorema 8.9 
Si $A, B$ son conjuntos, la clase de funciones de $A$ en $B$ es conjunto.

>[!red]- Axioma 9: De fundación
En cada conjunto no vacío $A$, hay $u \in A$ tal que $u\cap A = \emptyset$.

>[!cian]- Teorema 8.11
>1) Si $A$ es conjunto no vacío, $A\notin A$.
>2) Si $A,B$ son conjuntos no vacíos, entonces $\neg(A\in B \; \land \; B\in A)$.

>[!red]- Axioma 10: Del infinito
Existe un conjunto $A$ tal que $\emptyset \in A$ y si $a\in A$, entonces $a\cup\{a\}\in A$.

>[!red]- Axioma 11: De elección
Dada una familia no vacía $\{A_{\alpha}\mid\alpha\in\mathcal{A}\}$ de conjuntos no vacíos y mutuamente disjuntos, entonces existe un conjunto $S$ que consiste en exactamente de un elemento de cada $A_{\alpha}$.
> >[!yellow]- Observación
>Este axioma es solamente necesario si $\mathcal{A}$ es un conjunto infinito.

---
## Sec: 9

>[!blue]- Definición: ${\large{X}_{\alpha \in \mathcal{A}}}\; A_\alpha$
Dado $\mathcal{A}$ conjunto no vacío y $A_\alpha$ conjunto para $\alpha\in\mathcal{A}$. 
${\large{X}_{\alpha \in \mathcal{A}}}\; A_\alpha := \{\mathcal{f}: \mathcal{A} \rightarrow \bigcup_{\alpha}A_{\alpha} \mid \forall \alpha \in \mathcal{A}, \mathcal{f}(\alpha)\in A_\alpha\}$.
>>[!green]- Comentario
>>1) ${\large{X}_{\alpha \in \mathcal{A}}}\; A_\alpha$ es conjunto, ya que $\{\mathcal{f}:\mathcal{A}\rightarrow\bigcup_{\alpha}A_\alpha\}$ es conjunto.
>>2) Si $\exists\alpha$ tal que $A_{\alpha}=\emptyset,\; {\large{X}_{\alpha \in \mathcal{A}}}\; A_\alpha$ es vacío.

>[!cian]- Teorema 9.2
>Las siguientes tres propiedades son equivalentes:
>1) Si $A_{\alpha}\neq \emptyset, \; \forall\alpha\in\mathcal{A}$ entonces ${\large{X}_{\alpha \in \mathcal{A}}}\; A_{\alpha}\neq\emptyset$.
>2) Axioma de elección.
>3) Sea $\{A_{\alpha}\mid\alpha\in\mathcal{A}\}$ familia no vacía de conjuntos no vacíos, existe $c:\mathcal{A}\rightarrow\bigcup_{\alpha}A_{\alpha}$ talque $\forall \alpha, \;c(\alpha)\in A_{\alpha}$.

>[!cian]- Teorema 9.3
>Sea $\{A_{\alpha}\mid\alpha\in\mathcal{A}\}$ una familia de conjuntos nos vacíos, y sea $\mathcal{A}\subset\mathcal{B}$, y definamos $P:{\large{X}_{\alpha \in \mathcal{A}}}\; A_{\alpha}\rightarrow{\large{X}_{\alpha \in \mathcal{B}}}\; A_\alpha$ por $P(c) = c\mid\mathcal{B}$. Entonces $P$ es sobreyectiva.
 
___
___ 
# Parte 2: Ordinales y Cardinales 

---
## Sec: 1

>[!blue]- Definición: Relación 
>Sea $A$ una clase, una relación es una subclase de $A\times A$.
>>[!green]- Comentario
>>Escribimos $x\prec y$ sí y solo si $(x, y)$ pertenece a la relación, en este caso se dice que $x$ precede a $y$.

>[!blue]- Definición: Preorden
>Una *relación* es un *preorden* si es:
>1) *Reflexiva:* $x\prec x, \forall x\in A$.
>2) *Tansitiva:* $x\prec y \;\land\;y\prec z \Rightarrow x\prec z$.

>[!blue]- Definiciones: Elemento maximal, cota superior y cadena
>Sea $(A,\prec)$ una clase con *preorden*.
>1) $m\in A$ es **elemento maximal** si $(\forall a \in A:m\prec a),\;a\prec m$.
>2) $a_{0}\in A$ es una **cota superior** de $B\subset A$ si $\forall b \in B$, $b\prec a_0$.
>3) $B\subset A$ es una **cadena** (*Chain*) en $A$ si cada para de elementos de $B$ estan relacionados, es decir, si $x,y\in B$, $x\prec y \;\lor\; y\prec x$.

>[!blue]- Definición: Orden parcial
>Una relación es un orden parcial si es:
>1) *Reflexiva:* $x\prec x, \forall x\in A$.
>2) *Transitiva:* $x\prec y \;\land\; y\prec z \Rightarrow x\prec z$.
>3) *Antisimétrica:* $x\prec y\;\land\;y\prec x\Rightarrow x=y$.

>[!blue]- Definición: Orden total
>$(A,\prec)$ con *orden parcial* es *orden total* si $A$ es *cadena*.

>[!blue]- Definición: Buen orden
>Un *orden parcial* $\prec$ es un *buen orden* en $A$ si cada subconjunto no vacío $B\subset A$ tiene un elemento minimal, es decir, existe $b_{0}\in B$ tal que $b_{0}\prec b, \forall b\in B$.

--- 
## Sec: 2

>[!cian]- Teorema 2.1
>Los siguientes son equivalentes.
>1) *Axioma de elección.*
>2) **Lema de Zorn**: Sea $(x, \prec)$, con $x$ conjunto y $\prec$ *orden parcial*, si cada *cadena* en $x$ tiene *cota superior*, entonces, existe un *elemento maximal*, en el conjunto $x$.
>3) Cada conjunto admite un *buen orden*.

>[!green]- Comentario
>*Bien ordenado* $\Rightarrow$ *totalmente ordenando*.













