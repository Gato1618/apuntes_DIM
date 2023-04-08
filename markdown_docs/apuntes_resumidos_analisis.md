```theme-toggle

```
# Parte 1: Teoría de conjuntos

---
##  Axiomática de NBG

>[!yellow]- Comentario: Signos del lenguaje matemático
>Hay que explícitar todos los signos del lenguaje matemático. Existen varias alternativas, pero la más habitual es considerar que el lenguaje de la teoría de conjuntos consta de los doce signos siguientes:
>$$\land, \lor, \neg, \Rightarrow, \Leftrightarrow, \exists, \forall, (,), |, \in$$
>más una lista infinita de variables, como:
>$$x,y,z,...,\alpha,\beta,\gamma,...$$
>Este lenguaje corresponde a la siguiente agrupación de objetos:
>1) Lógica proposicional:
>	- Sean $p, q$ *proposiciones*.
>	- Se tiene los *operadores lógicos* $\{\land,\lor,\neg,\Rightarrow,\Leftrightarrow\}$.
>	- *Cuatificadores*: $\{\exists,\forall\}$ y variables $p(x)$.
>	- Valores *verdadero (V)* y  *falso (F)*.
>2) Conceptos no definidos:
>	- *Pertenecia*: $\in$
>	- El concepto de *clase* corresponde a cualquier objeto de la forma $\{x|p(x)\}$ donde $p$ es una proposición.

>[!blue]- Definición: Elementos básicos de la teoría de conjuntos
>1) Igualdad de clases: Si $A, B$ son clases, y $(\forall x, x \in A \Leftrightarrow x \in B)$ entonces $A = B$.
>2) No pertenencia: $x\notin A\Leftrightarrow\neg(x\in A)$
>3) La contención de clases como: $A\subset B\Leftrightarrow(\forall x), (x\in A\Rightarrow x\in B)$.

>[!red]-  Axioma 1: De individualidad
Si $x \in \mathscr{A}$ y $x = y$, entonces $y \in \mathscr{A}$

>[!blue]- Definición: Conjunto
Una clase $A$ es un conjunto si existe una clase $\mathscr{A}$ tal que $A \in \mathscr{A}$.

>[!red]- Axioma 2: De formación de clase
Si $p(x)$ es una proposición lógica que involucra variables conjuntos, existe una clase $\mathscr{A}$ tal que $x\in\mathscr{A}\Leftrightarrow x$ es conjunto $\land\; p(x)$.

>[!blue]- Definción: Clase propia
>Decimos que una clase $A$ es propia si no existe una clase $B$ tal que $A\in B$.

>[!blue]- Definción: Clase universal y Clase de Russel
>1) Se llama *clase de Russell* a la clase de los elmentos que no pertenences en si mismos, esto se escribe: $R:=\{x|x\;es\;conjunto\;\land x\notin x\}$.
>2) Se llama *clase universal* a la clase de todos los conjuntos que son iguales a si mismos, esto se escribe: $U:=\{x|x\;es\;conjunto\;\land x=x\}$
>>[!cian]- Proposición:
>>$R$ es *clase propia*.

>[!blue]- Definición: Clase vacía
$\emptyset$ es la clase tal que $\forall\;x\;\neg(x\in\emptyset)$.

>[!red]- Axioma 3: De el conjunto vacío
$\emptyset$ es un conjunto.

>[!red]- Axioma 4: De emparejamiento
Si $A$ y $B$ son conjuntos distintos, la clase $\mathscr{A} = \{x \mid (x = A) \lor (x = B)\}$  es conjunto (que consta de exactamente dos elementos) Se denota: $\{A, B\}$.

>[!blue]- Definición: Familia de conjuntos
$\mathscr{A}$ es conjunto y para cada $\alpha \in \mathscr{A}, A_{\alpha}$ es conjunto. A los conjuntos de la forma $A_{\alpha}$ se le llama una familia de conjuntos.
> - Union de los conjuntos de la familia: 
$\bigcup_{\alpha}A_{\alpha} = \bigcup_{\alpha \in \mathscr{A}}A_{\alpha} = \{x \mid \exists \alpha \in \mathscr{A}: x \in A_{\alpha}\}$
>
> - Intersección de conjuntos de la familia:
$\bigcap_{\alpha}A_{\alpha} = \bigcap_{\alpha \in \mathscr{A}}A_{\alpha} = \{x \mid \forall \alpha \in \mathscr{A}, x \in A_{\alpha}\}$

>[!red]- Axioma 5: De union
Si $\mathscr{A}$  es un conjunto y $\forall\alpha\in \mathscr{A}, A_{\alpha}$ es un conjunto, entonces $\bigcup_{\alpha \in \mathscr{A}}A_{\alpha}$ es un conjunto.

>[!blue]- Definición: Producto cartesiano, par odenado y relación de clases
>1) Dadas las clases $\mathscr{A}, \mathscr{B}$, definimos la clase $\mathscr{A} \times \mathscr{B}$ como $\{\{a, \{a, b\}\}\mid a \in \mathscr{A} \land b \in \mathscr{B}\}$.
>2) Al conjunto, decimos que es un *par ordenado* $\{a,\{a,b\}\}$ lo escribimos como $(a,b)$ .
>3) Decimos que una *relación* $\mathcal{R}$ en $\mathscr{A}\times\mathscr{B}$ es una subclase de $\mathscr{A}\times\mathscr{B}$. Denotamos: $(a,b)\in\mathcal{R}\Leftrightarrow x\mathcal{R}y$.

>[!blue]- Definición: Función
Una función ${f}$ de $\mathscr{A}$ en $\mathscr{B}$ es una *relacion* de $\mathscr{A} \times \mathscr{B}$ tal que $(\forall a \in \mathscr{A})\;( \exists ! b\in\mathscr{B})$ tal que $a\mathcal{R}b$, en cuyo caso diremos que $(a,b)\in f$.

>[!red]- Axioma 6: De sustitución
Si $A$ es conjunto y $\mathcal{f}:A \rightarrow \mathscr{B}$ función, $\mathcal{f}(A):= \{b \in \mathscr{B} \mid \exists a \in A : (a,b) \in \mathcal{f}\}$ es conjunto.

>[!red]- Axioma 7: De refinamiento
Si $A$ es conjunto y $\mathscr{A}$ es clase, $A\cap\mathcal{A}$ es conjunto.

>[!blue]- Definición: Clase potencia
Si $\mathscr{A}$ es clase, $P(\mathscr{A})=\{A\;|\;A\subset\mathscr{A}\land A\;es\;conjunto\}$ es clase.

>[!red]- Axioma 8: Del conjunto de potencia
Si $A$ es conjunto, $P(A)$ es conjunto.

>[!cian]- Proposiciones importantes 
>1) Sea $(A_{\alpha})_{\alpha \in \mathscr{A}}$ una familia de conjuntontos. Entonces $P(\bigcap_{\alpha \in \mathscr{A}}A_{\alpha})=\bigcap_{\alpha \in \mathscr{A}}P(A_{\alpha})$ y $\bigcup_{\alpha \in \mathscr{A}}P(A_{\alpha})\subset P(\bigcup_{\alpha \in \mathscr{A}}A_{\alpha})$
>2) Si $A$ es conjunto y $p(x)$ proposición lógica sobre el conjunto, entonces $\{x \in A \mid p(x)\}$ es conjunto.
>3) Si $B$ es una subclase de un conjunto $A$ entonces $B$ es conjunto.
>4) Si $A$ es un cojunto entonces $\{A\}$ es un cojunto.
>5) SI $A$ y $B$ son cojuntos, $A\times B$ también.
>6) Si $A, B$ son conjuntos, la clase de funciones de $A$ en $B$ es conjunto.

>[!blue]- Definición: Producto cartesiano idexado
Dado $\mathscr{A}$ conjunto no vacío y $A_\alpha$ conjunto para $\alpha\in\mathscr{A}$. 
${\large{\mathsf{X}}_{\alpha \in \mathscr{A}}}\; A_\alpha := \{\mathcal{f}: \mathscr{A} \rightarrow \bigcup_{\alpha}A_{\alpha} \mid \forall \alpha \in \mathscr{A}, \mathcal{f}(\alpha)\in A_\alpha\}$.
>>[!green]- Comentario
>>1) ${\large{\mathsf{X}}_{\alpha \in \mathscr{A}}}\; A_\alpha$ es conjunto, ya que $\{\mathcal{f}:\mathscr{A}\rightarrow\bigcup_{\alpha}A_\alpha\}$ es conjunto.
>>2) Si $\exists\alpha$ tal que $A_{\alpha}=\emptyset,\; {\large{\mathsf{X}}_{\alpha \in \mathscr{A}}}\; A_\alpha$ es vacío.

>[!red]- Axioma 9: De fundación
En cada conjunto no vacío $A$, hay $u \in A$ tal que $u\cap A = \emptyset$.

>[!cian]- Teorema 
>1) Si $A$ es conjunto no vacío, $A\notin A$.
>2) Si $A,B$ son conjuntos no vacíos, entonces $\neg(A\in B \; \land \; B\in A)$.

---
## Axioma del infinito

>[!red]- Axioma 10: Del infinito
Existe un conjunto $A$ tal que $\emptyset \in A$ y si $a\in A$, entonces $a\cup\{a\}\in A$.

---
## Axioma de elección

>[!red]- Axioma 11: De elección
Dada una familia no vacía $\{A_{\alpha}\mid\alpha\in\mathscr{A}\}$ de conjuntos no vacíos y mutuamente disjuntos, entonces existe un conjunto $S$ que consiste en exactamente de un elemento de cada $A_{\alpha}$.
> >[!yellow]- Observación
>Este axioma es solamente necesario si $\mathscr{A}$ es un conjunto infinito.

>[!blue]- Definición: Función de elección
>Dada una familia de conjuntos no vaciós $(A_\alpha)_{\alpha \in \mathscr{A}}$ (no necesariamente disjuntos), llamamos *función de elección* a la función $f:\mathscr{A}\rightarrow\bigcup_{\alpha\in\mathscr{A}}A_\alpha$ donde para todo $\alpha\in\mathscr{A}$ se cumple que $f(\alpha)\in A_{\alpha}$.

>[!cian]- Teorema: Equivalencias al ax. de elección
>Las siguientes tres propiedades son equivalentes:
>1) Si $A_{\alpha}\neq \emptyset, \; \forall\alpha\in\mathscr{A}$ entonces ${\large{\mathsf{X}}_{\alpha \in \mathscr{A}}}\; A_{\alpha}\neq\emptyset$.
>2) Es cierto el *Axioma de elección* para $(A_\alpha)_{\alpha \in \mathscr{A}}$.
>3) Existe una *función de elección* para $(A_\alpha)_{\alpha \in \mathscr{A}}$.

>[!cian]- Teorema
>Sea $\{A_{\alpha}\mid\alpha\in\mathscr{A}\}$ una familia de conjuntos nos vacíos, y sea $\mathcal{A}\subset\mathscr{B}$, y definamos $P:{\large{\mathsf{X}}_{\alpha \in \mathscr{A}}}\; A_{\alpha}\rightarrow{\large{\mathsf{X}}_{\alpha \in \mathscr{B}}}\; A_\alpha$ por $P(c) = c\mid\mathscr{B}$. Entonces $P$ es sobreyectiva.

---
## Principio del buen orden

>[!blue]- Definición: Relación 
>Sea $A$ y $B$ una clased, una relación es una subclase de $A\times B$.
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

>[!blue]- Definición: Elemento minimal
>Dado un orden parcial $(B,\prec),\;b_{0}\in B$ se dice *elemento minimal*, si $b_{0} \prec b,\;\forall b\in B$.

>[!blue]- Definición: Buen orden
>Un *orden parcial* $\prec$ es un *buen orden* en $A$ si cada subconjunto no vacío $B\subset A$ tiene un *elemento minimal*.

>[!cian]- Teorema fundamental: Equivalencias del axioma de elección, lema de Zorn y principio del buen ordenamiento
>Los siguientes son equivalentes.
>1) *Axioma de elección.*
>2) *Lema de Zorn*: Sea $(x, \prec)$, con $x$ conjunto y $\prec$ *orden parcial*, si cada *cadena* en $x$ tiene *cota superior*, entonces, existe un *elemento maximal*, en el conjunto $x$.
>3) *Principio del buen ordenamiento*: Cada conjunto admite un *buen orden*.

>[!green]- Comentario
>*Bien ordenado* $\Rightarrow$ *totalmente ordenando*.

---
---
# Parte 2: Ordinales y Cardinales 

---
## Ordinales 

>[!blue]- Definición: Función inyectiva, sobreyectiva y biyectiva
>$\mathcal{f}:A\rightarrow B$ función es:
>1) *Inyectiva* (*one-to-one*) si $x\neq y\Rightarrow f(x)\neq f(y)$.
>2) *Sobreyectiva* (*onto*) $f(A)=B$.
>3) *Biyectiva* si se tienen ambos anteriores.

>[!blue]- Definición: Monomorfismo y isomorfismo
>Sean $(X,\prec_{x})$ y $(Y, \prec_{y})$ bien ordenados, $\mathcal{f}:X\rightarrow Y$ es:
>1) *Monomorfismo* si es inyectiva y $x_{1}\prec_{x}x_{2}\Rightarrow f(x_{1})\prec_{y}f(x_{2})$.
>2) *Isomorfismo* si es monomorfismo y biyección, si existe un *isomorfismo* entre dos conjuntos, se dice que tienen el mismo *Ordinal*.

>[!blue]- Definición: Ideal e intervalo inicial
>Sea $(W,\prec)$ bien oredenado:
>1) $S\subset W$ es *ideal* en $W$ si $\forall x:(x\in S)\land(y\prec x)\Rightarrow y\in S$.
>2) $\forall a\in W, S(a)=\{x\in W\mid(x\prec a)\land(x\neq a)\}$ se llama *intervalo inicial* de $a$.

>[!cian]- Teorema: Principio de inducción transfinita
>Sea $(X,\prec)$ *buen orden* y $A\subset X$ tal que $(\forall x\in X, S(x)\subset A\Rightarrow x\in A),$ entonces $A=X$.
>>[!green]- Comentario
>>Es importante definir bien los conjuntos $A$ y $X$ y demostrar la hipotesis para mostrar que $A=X$.

>[!cian]- Teorema: Sobre la existencia de *isomorfismos*
>Sean $W,\,X$  bien ordenados, uno y solo y de los siguientes se cumple:
>1) $\exists!$ *isomorfismo* de $W$ a $X$.
>2) $\exists!$ *isomorfismo* de $W$ sobre *inicial* de $X$.
>3) $\exists!$ *isomorfismo* de $X$ sobre *inicial* de $W$.

---
## Cardinales 

>[!blue]- Definición: Cardinalidad
>Sean $A,\,B$ conjuntos,
>1) Sea $[A]$ la clase de equivalencia de un conjunto $A$ definida por $[A]:= \{B\;es\;conjunto\;|\;\exists f:A\rightarrow B\;biyectiva\}$ a la clase anterio se le denomina cadinal de $A$.
>2) $Card(A)=Card(B)$, $|A|=|B|$ o se dice que $A$ y $B$ son equipotentes, si existe una biyección entre $A$ y $B$.
>3) $Card(A)\leq Card(B)$, si existe una inyección de $A$ en $B$.

>[!cian]- Teorema: De Schröder-Bernstein:
>Si $Card(A)\leq Card(B)$ y $Card(B)\leq Card(A)$ entonces $Card(A)=Card(B)$.

>[!cian]- Lema: Cardinalidad de las particiones
>Si $\{x_{i}\mid i\in\mathbb{N}\}$ es partición de $X$ y $\{y_{i}\mid i\in\mathbb{N}\}$ partición de $Y$, tales que $|x_i|=|y_i|\;\forall i\in\mathbb{N}$, entonces $|X|=|Y|$.

>[!blue]- Notación: Funciones de $A$ en $B$
>Dados $A,\, B$ conjuntos, se denota, $B^{A} =\{Funciones\;de\;A\;en\;B\}$.

>[!cian]- Proposición
>Sean $X$ un cojunto no vacío, se tiene que $|P(x)|=|\{0,1\}^{X}|$.

>[!cian]- Proposición
>Dados $X, Y$ conjuntos, si existe una función $g:X\rightarrow Y$ sobreyectiva, entonces $|Y|\leq|X|$.

>[!Yellow]- Comentarios: Sobre Cardinalidad
>1) Se denota $\aleph_{0}= Card(\mathbb{N})$.
>2) Dado dos conjuntos $A,\;B$, si $|A|\leq|B|$ y $|A|\neq|B|$, escribimos $|A|<|B|$.
>3) Dado un conjunto $X$, $X$ se dice *contable* o *nomberable* si $|X|\leq|\mathbb{N}|$.
>4) Dado un cojunto $X$, $X$ se dice *infinito*, si existe un cojunto $X' \subsetneq X$ tal que, $|X'|=|X|$.

>[!cian]- Proposición
>Sea $X$ un conjunto, entonces $|P(X)|>|X|$.

--- 
## Extra: Construcción de los número reales 

En esta sección se van a asumir conocido $\mathbb{N}$, los números naturales.

>[!blue]- Definición: Números enteros
>Se define $\mathbb{Z}=(\mathbb{N}\times\mathbb{N})/\sim_{s}$, donde $(n,\,m)\sim_{s}(n',\,m')\Leftrightarrow n+m'=n'+m$.
>Luego, es valido definir una suma y un producto.

>[!blue]- Definición: Números racionales
>Se define $\mathbb{Q}=(\mathbb{Z}\times(\mathbb{Z}-\{0\})) /\sim_D$, donde $(p,\,q)\sim_{D}(p',\,q') \Leftrightarrow p\cdot q' = q\cdot p'$.
>Luego, es valido definir las operaciones entre racionales.

>[!blue]- Definición: Números reales
>Se define el conjunto $\mathbb{R}$ con el conjunto de todos los pares ordenados $(L,\;R)$ tales que $L,\;R$ son particiones de $\mathbb{Q}$ y cumplen que:
>1) Si $x\in L\;\land\;y\in R, x<y$.
>2) Si $x\in L$, existe $x'\in L$ tal que $x<x'$.
>A estos pares de conjuntos de les conoce como *cortes de Debekind*.

>[!blue]- Definición: Menor o igual
>Para $(L,R),\;(L',R')\in\mathbb{R}$, $(L,R)\leq(L',R')\Leftrightarrow L\subset L'$.

>[!cian]- Teorema: Existencia del supremo
>Si $X=\{Familias\;de\;cortes\;de\;Debekind\}$ acotado, entonces tiene supremo.

>[!cian]- Proposición
>$|[0,1]|=|P(\mathbb{N})|=|\{0,1\}^{\mathbb{N}}|$.

>[!Cian]- Corolario
>$|\mathbb{R}|=|[0,1]| = |P(\mathbb{N})|$.

>[!blue]- Definición: Conjunto de Cantor
>Si $C_{0}=[0,1],\;C_{n+1}=\left( \frac{1}{3}C_{n} \right)\cup\left( \frac{1}{3}C_{n}+\frac{2}{3} \right)$.
>Luego el *conjunto de Cantor* se define como: $\mathscr{C}=\bigcap_{n\in\mathbb{N}}C_n$.

---
---
# Parte 3: Topología

---
## Espacios topologícos

>[!blue]- Definición: Topología 
>Sea $X$ un conjunto $\mathscr{T}\subset P(X)$ se llama *topología* si:
>1) $X,\emptyset\in\mathscr{T}$.
>2) Si $\{A_{\alpha}\;|\;\alpha\in\mathscr{A}\}\subset\mathscr{T}$, entonces, $\bigcup_{\alpha\in\mathscr{A}}A_{\alpha}\in\mathscr{T}$.
>3) Si $\{A_{\alpha}\;|\;\alpha\in\mathscr{A}\}\subset\mathscr{T}$, con $\mathscr{A}$ finito, entonces, $\bigcap_{\alpha\in\mathscr{A}}A_{\alpha}\in\mathscr{T}$.
>Si $A\in\mathscr{T}$, se dice que $A$ es *abierto*.

>[!blue]- Definición: Topología más fina
>Si $\mathscr{T}$ y $\mathscr{T'}$ son topologías sobre $X$, se dice que:
>1) $\mathscr{T'}$ es *más fina* que $\mathscr{T}$ si $\mathscr{T}\subset\mathscr{T'}$, análogamente se puede decir que $\mathscr{T}$ es *más gruesa* que $\mathscr{T'}$.
>2) $\mathscr{T'}$ es *estricatamente más fina* que $\mathscr{T}$ si $\mathscr{T}\subsetneq\mathscr{T'}$.

>[!blue]- Definición: Base
>Sea $X$ un conjunto, $\mathscr{B}\in P(X)$  se dice *base* si:
>1) $\forall\, x\in X$, existe $B\in\mathscr{B}$ tal que $x\in B$.
>2) $\forall\,x\in X$, si existen $B_{1}, B_{2}$ tal que $x\in B_{1}$ y $x\in B_{2}$, existe $B_3\in\mathscr{B}$ tal que $x\in B_{3}\subset B_{1}\cap B_{2}$.

>[!blue]- Definición: Topología generada
>Si $\mathscr{B}$ es una base, la *topología generada* por $\mathscr{B}$, $\mathscr{T}$ es definida tal que, $A\in\mathscr{T}\Leftrightarrow \forall x \in A\;,\exists B\in\mathscr{B}$ tal que $x\in B\subset A$.
>>[!cian]- Proposición
>>La *topología generada* por una base es *topología*.

>[!cian]- Lema
>Sea $X$ espacio topologíco. $\mathscr{B},\mathscr{B'}$ bases que generan $\mathscr{T},\mathscr{T'}$. $\mathscr{T'}$ es más fina que $\mathscr{T}$ si y solo sí $\forall\, x\in X$ y $B \in \mathscr{B}$ que contiene a $x$, existen $B' \in \mathscr{B'}$ tal que $x\in B'$.

>[!cian]- Lema
>Si $\mathscr{B}$ es base para $\mathscr{T}$, $\mathscr{T}=\{\bigcup_{\alpha}B_{\alpha}\;|\;\forall\,\alpha\in\mathscr{A}, B_{\alpha}\in\mathscr{B}\}$.

 >[!blue]- Definición: Sub base
 >Una *sub base* en $X$ es una colección de subconjuntos que recubren $X$. Sea $\mathcal{S}$ *sub base*, la topología generada por $\mathcal{S}$ es la colección, $\mathscr{T}=\{Union\;de\;intersecciones\;finitas\;de\;elementos\;de\;\mathcal{S}\}$.
 >>[!cian]- Proposición
 >>$\mathscr{T}$ es una topología.

>[!blue]- Definición: Orden simple
> Se dice que la relación $<$ es un orden simple si:
> 1) $\forall x,\,y$ tal que $x\neq y$, $x<y\;\lor\; y<x$.
> 2) $x<x$ es siempre falso.
> 3) $x<y\;\land\;y<z\Rightarrow x<z$.








