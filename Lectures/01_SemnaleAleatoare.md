
# Capitolul I. Semnale aleatoare

## I.1 Variabile aleatoare

### Variabile aleatoare

- **Variabilă aleatoare** = o variabilă care denumește o valoare produsă printr-un fenomen aleator
    - Practic, reprezintă *un nume* atașat unei valori arbitrare
    - Prescurtat: v.a.
- Notație uzuală: $X$, $Y$ etc..

- Exemple:
    - $X$ = Numărul obținut prin aruncarea unui zar
    - $V_{in}$ = Voltajul măsurat într-un punct dintr-un circuit

### Realizări ale unei variabile aleatoare

- **Realizare** a unei v.a. = o valoare particulară posibilă 

- **Spațiul realizărilor** $\Omega$ = mulțimea valorilor posibile ale unei v.a
    - mulțimea tuturor realizărilor

- Exemplu: aruncarea unui zar
    - V.a. se notează $X$
    - Se poate obține o realizare $X = 3$
    - Dar s-ar fi putut obține orice valoare din spațiul realizărilor
    $$\Omega = \left\{1, 2, 3, 4, 5, 6\right\}$$

### Aruncarea unei monede

- Variabila aleatoare X = "fața obținută la atuncarea unei monede"
	
	\smallskip

    ![](img/RandomVariable_img.svg){.id width=50%}

(sursa imaginii: *https://www.mathsisfun.com/data/random-variables.html*)

### V.a. discrete și continue

- V.a. **discretă**: dacă $\Omega$ este o mulțime discretă
    - Exemplu: Numărul obținut prin aruncarea unui zar
- V.a. **continuă**: dacă $\Omega$ este o mulțime compactă
    - Exemplu: Valoarea tensiunii măsurate într-un punct

### Unde se întâlnesc variabile aleatoare?

- Variabilele aleatoare modelează semnale de **zgomot**

- Exemple:
    - Se măsoară tensiunea într-un punct dintr-un circuit
    - Dacă se măsoară de mai multe ori, se obțin valori *ușor diferite*.
    - Valoarea este afectată de zgomot
    - Valoarea tensiunii este o *variabilă aleatoare*

### Funcția masă de probabilitate

- Fie o v.a. discretă $A$

- **Funcția masă de probabilitate** (FMP) (*probability mass function*) = 
probabilitatea ca $A$ să aibă valoarea egală cu $x$
$$w_A(x)= P\left\{ A = x\right\}$$

- pe scurt, se mai numește **distribuția** variabilei A

- Exemplu: FMP pentru valoarea unui zar, grafic pe tablă

### Calculul probabilității cu FMP

- Probabilitatea ca $A$ să aibă valoarea $v$
$$P\left\{ A = v\right\} = w_A(v)$$

- Probabilitatea ca A să fie între valorile $a$ și $b$ (inclusiv):
$$P\left\{ a \leq A \leq b\right\} = \sum_{x=a}^b w_A(x)$$

### Funcția de repartiție

- **Funcția de repartiție (FR)** = probabilitatea ca $A$ 
să aibă valoarea mai mică sau egală cu $x$
$$F_A(x) = P\left\{ A \leq x \right\}$$

- Exemplu: FR pentru un zar, grafic la tablă

- Pentru v.a. discrete, FR este "în trepte"

### Calculul probabilității cu FR

- Probabilitatea ca $A$ să aibă valoarea $v$
$$P\left\{ A = v\right\} = F_A(v) - F_A(v-1)$$

- Probabilitatea ca A să fie între valorile $a$ și $b$ (inclusiv):
$$P\left\{ a \leq A \leq b\right\} = F_A(b) - F_A(a-1)$$

### Relația între FMP și FR

- FR este *suma cumulativă* (un fel de "integrală discretă") a FMP
$$F_A(x) = \sum_{t = -\infty}^{t = x} w_A(t)$$

- Exemplu pentru zar: grafic, la tablă

### Funcția densitate de probabilitate

- Fie o v.a. **continuă** $A$

- **Funcția densitate de probabilitate (FDP)** 
= probabilitatea ca valoarea lui $A$ să fie într-o vecinătate $\epsilon$ mică în jurul lui $x$, totul supra $\epsilon$

- Se notează $w_A(x)$, se mai numește **distribuția** variabilei A

- Informal: FDP reprezintă probabilitatea ca valoarea lui $A$ să fie **în jurul lui** $x$

### Variabile aleatoare discrete și continue

\smallskip

![](img/RandomVariable_Types.png){.id width=80%}

(sursa imaginii: "Probability Distributions: Discrete and Continuous", Seema Singh, *https://towardsdatascience.com/probability-distributions-discrete-and-continuous-7a94ede66dc0*)


### Probabilitatea unei valori exacte

- Probabilitatea ca o v.a. continuă $A$ să ia **exact** o valoare $x$ este **zero**
    - pentru că există o infinitate de valori posibile (v.a. continuă)
    - de aceea nu se poate defini o funcție masă de probabilitate ca la v.a. discrete

- De aceea FDP reprezintă probabilitatea de a fi **într-o vecinătate** a valorii $x$, și nu exact egal cu $x$

### Calculul probabilității cu FDP

- Probabilitatea ca $A$ să aibă exact valoarea $v$ este întotdeauna 0
$$P\left\{ A = v\right\} = 0$$

- Probabilitatea ca A să fie între valorile $a$ și $b$  = integrala FDP între $a$ și $b$:
$$P\left\{ a \leq A \leq b\right\} = \int_a^b w_A(x) dx$$

### Funcția de repartiție

- **Funcția de repartiție (FR)** = probabilitatea ca $A$ 
să aibă valoarea mai mică sau egală cu $x$
$$F_A(x) = P\left\{ A \leq x \right\}$$

- Aceeași definiție ca și la v.a. discrete

### Calculul probabilității cu FR

- Probabilitatea ca valoarea lui A să fie între $a$ și $b$:
$$P\left\{ a \leq A \leq b\right\} = F_A(b) - F_A(a)$$

- Nu contează dacă intervalul este deschis sau închis
    - $[a,b]$ sau $(a,b)$, nu contează
    - de ce? 

### Relația între FDP și FR

- FR este **integrala** FDP
- FDP este **derivata** FR

$$F_A(x) = \int_{-\infty}^x w_A(x) \mathrm{d}x$$

$$\begin{split}
w_A(x) &= \frac{\mathrm{d}F_A(x)}{\mathrm{d}x} \\
&= \lim_{\epsilon \to 0}{\frac{F_A(x+\epsilon) - F_A(x-\epsilon)}{2 \epsilon}} \\
&= \lim_{\epsilon \to 0}{\frac{P(A \in [x-\epsilon, x+\epsilon])}{2 \epsilon}}
\end{split}$$

### Interpretare grafică

* Probabilitatea ca $A$ să fie între $a$ și $b$ este **suprafața de sub FDP**
    * adică integrala de la $a$ la $b$

* Probabilitatea ca $A$ să fie exact egal cu o valoare este zero
    * aria de sub un punct este nulă

\smallskip

![](img/RandomVariable_AreaPDFProb.png){.id width=50%}

(sursa: "https://intellipaat.com/blog/tutorial/statistics-and-probability-tutorial/probability-distributions-of-continuous-variables/*)



### V.a. discrete vs continue

Comparație între v.a. discrete și continue

- FR $F_A(x)$ are aceeași definiție, înseamnă același lucru
- FDP/FMP $w_A(x)$ este derivata FR
    - la v.a. continue:
        - este o derivată obișnuită
        - reprezintă probabilitatea de a fi "in jurul" valorii $x$
    - la v.a. discrete:
        - un fel de "derivată discretă"
        - reprezintă probabilitatea de a avea exact valoarea $x$

### Proprietățile v.a

FR:

- FR este mereu pozitivă, $F_A(x) \geq 0$
- FR este monoton crescătoare (nu descrește)
- FR pornește din 0 și ajunge la valoarea 1
$$F_A(-\infty) = 0 \;\;\;\; F_A(\infty) = 1$$

FDP/FMP:

- PDF/PMF sunt mereu pozitive $w_A(x) \geq 0$
- Integrala/suma pe întreg domeniul = 1
$$\int_{-\infty}^\infty w_A(x) \mathrm{d}x = 1$$
$$\sum_{x = -\infty}^\infty w_A(x) = 1$$


### Diferite distribuții

* Semnal sinusoidal


![](figures/01_SemnaleAleatoare_figure1_1.png){width=8cm}\


### Diferite distribuții

* Sinus + zgomot (normal, $\mu = 0, \sigma^2 = 1$)


![](figures/01_SemnaleAleatoare_figure2_1.png){width=8cm}\


### Diferite distribuții

* Sinus + zgomot (uniform $\mathcal{U} [-1,1]$)

* Ce diferă? Tipul distribuției


![](figures/01_SemnaleAleatoare_figure3_1.png){width=8cm}\


### Diferite distribuții

* Imagine originală


![](figures/01_SemnaleAleatoare_figure4_1.png){width=8cm}\


### Diferite distribuții

* Imagine + zgomot (normal, $\mu = 0, \sigma^2 = 1$)


![](figures/01_SemnaleAleatoare_figure5_1.png){width=8cm}\


### Diferite distribuții

* Imagine + zgomot mai mare (normal, $\mu = 0, \sigma^2 = 10$)


![](figures/01_SemnaleAleatoare_figure6_1.png){width=8cm}\


### Diferite distribuții

* Imagine + zgomot (uniform, $\mathcal{U} [-5, 5]$)


![](figures/01_SemnaleAleatoare_figure7_1.png){width=8cm}\



### Distribuția normală

* Densitatea de probabilitate:

$$w_A(x) = \frac{1}{\sigma \sqrt{2 \pi}} e^{-\frac{(x-\mu)^2}{2 \sigma^2}}$$


![](figures/01_SemnaleAleatoare_figure8_1.png){width=8cm}\


### Distribuția normală

* Are doi parametri:
    * **Media** $\mu$ = "centrul" funcției
    * **Deviația standard** $\sigma$  = "lățimea" funcției
        - $\sigma$ mic = funcție îngustă și înaltă
        - $\sigma$ mare = funcție largă și joasă

* Constanta de la începutul expresiei asigură normalizarea (faptul că integrala = 1)
    
* Extrem de des întâlnită în practică

* Orice valoare reală este posibilă ($w_A(x) > 0, \forall x \in \mathbb{R}$)

* Se notează cu $\mathcal{N}(\mu, \sigma^2)$

### Distribuția normală

- Distribuția descrește pe măsură ce $x$ se îndepărtează de centrul $\mu$
    - Datorită termenului $-(x - \mu)^2$ de la exponent
    - Valorile cele mai probabile sunt în jurul lui $\mu$ ($x - \mu = 0$)
    - Valorile apropiate de $\mu$ sunt mai probabile, valorile mai depărtate de $\mu$ sunt mai puțin probabile

- Distribuția exprimă o preferință pentru valori apropiate de $\mu$, 
cu probabilitate din ce în ce mai scăzută la valori mai depărtate de $\mu$

### Exemple de valori generate cu distribuția normală (mu=0, sigma^2=1)


![](figures/01_SemnaleAleatoare_figure9_1.png){width=8cm}\


### Exemple de valori generate cu distribuția normală (mu=2, sigma^2=4)


![](figures/01_SemnaleAleatoare_figure10_1.png){width=8cm}\


### Distribuția uniformă

* Densitatea de probabilitate = constantă între două limite 

$$w_A(x) = 
\begin{cases}
\frac{1}{b-a}, & x \in [a, b] \\
 0, &elsewhere
\end{cases}$$


![](figures/01_SemnaleAleatoare_figure11_1.png){width=8cm}\


### Distribuția uniformă

* Are doi parametri: limitele $a$ și $b$ ale intervalului

* "Înălțimea" funcției este $\frac{1}{b-a}$ pentru normalizare
    - pentru ca integrala (aria) să fie 1
    
* Sunt posibile doar valori din intervalul $[a, b]$
    - valorile din afara intervalului au probabilitatea 0

* Se notează cu $\mathcal{U} \;[a, b]$

### Alte distribuții

* Nenumărate variante, apar în diverse aplicații

### Calculul probabilității pentru distribuția normală

- Cum calculăm $\int_a^b$ dintr-o distribuție normală?
    - Nu se poate prin formule algebrice, funcție ne-elementară

- Se folosește *the error function*:
$$erf(z) = \frac{2}{\sqrt{\pi}} \int_0^z e^{-t^2} dt$$

- Funcția de repartiție a unei distribuții normale $\mathcal{N}(\mu, \sigma^2)$
$$F_A(X) = \frac{1}{2}(1 + erf(\frac{x - \mu}{\sigma \sqrt{2}}))$$

- Valorile funcției *erf()* sunt tabelate / se calculează numeric
    - de ex. pe Google, căutați $erf(0.5)$
    - Alte valori folositoare:
        - $erf(-\infty) = -1$
        - $erf(\infty) = 1$

### Exercițiu 

Exercițiu:

  - Fie $A$ o v.a. cu distribuția $\mathcal{N}(3, 2)$. 
Calculați probabilitatea ca $A \in [2, 4]$

### Suma unei constante cu o v.a.

- Fie o v.a. $A$
- Ce reprezintă $B = 5 + A$?

Răspuns:

- B este tot o variabilă aleatoare
- B are același tip de distribuție, dar "translată" cu 5 la dreapta

Exemplu:

- A este o v.a. cu distribuție normală $w_A(x) = \mathcal{N}(\mu=3, \sigma^2=2)$
- Care este distribuția variabilei $B = 5 + A$?
- Răspuns: $w_B(x) = \mathcal{N}(\mu=8, \sigma^2=2)$

### V.a. ca funcții de alte v.a

- O funcție aplicată unei v.a. produce o altă v.a.

- Exemple: dacă $A$ este o v.a. distribuită $\mathcal{U}\;[0,10]$, atunci
    - $B = 5 + A$ este o altă v.a., distribuită $\mathcal{U}\;[5,15]$
    - $C = A^2$ este de asemenea o v.a.
    - $D = cos(A)$ este de asemenea o v.a.
    
- Motivație: dacă $A$ este aleatoare, și valorile $B$, $C$, $D$ sunt aleatoare

- A, B, C, D nu sunt independente
    - O anumită valoare a uneia implică automat și valoarea celorlalte

### Sisteme de mai multe variabile aleatoare

- Fie un sistem cu două v.a. continue $A$ și $B$

- Care este probabilitatea ca perechea $(A,B)$ să aibă valoarea
în jurul $(x,y)$?

- Distribuția valorilor perechii $(A,B)$ este descrisă de:
    - Densitatea de probabilitate comună $w_{AB}(x,y)$
    - Funcția de repartiție comună $F_{AB}(x,y)$
    
### Sisteme de mai multe variabile aleatoare
    
- Funcția de repartiție comună:
$$F_{AB}(x,y) = P_{AB}\left\{ A \leq x \cap B \leq y \right\}$$

- Densitatea de probabilitate comună:
$$w_{AB}(x,y) = \frac{\partial^2 F_{AB}(x,y)}{\partial x \partial y}$$

* FDP comună descrie probabilitatea ca perechea $(A,B)$
să aibă valoarea într-o vecinătate a $(x,y)$

* Similar pentru v.a discrete:
$$w_{AB}(x,y) = P\left\{ A = x \cap B = y \right\}$$

### Variabile independente

- Două v.a. $A$ și $B$ sunt **independente** dacă valoarea uneia nu 
influențează în nici un fel valoarea celeilalte

- Pentru v.a. independente, probabilitatea ca $A$ să fie în jurul lui
 $x$ și $B$ în jurul lui $y$ este produsul celor două probabilități

$$w_{AB}(x,y) = w_A(x) \cdot w_B(y)$$

- Valabilă pentru FR / FDP / FMP, v.a. continue sau aleatoare etc.

- Similar pentru mai mult de două v.a.

### Variabile independente

Exercițiu: 

  - Calculați probabilitatea ca trei v.a. $X$, $Y$ și $Z$ i.i.d. $\mathcal{N}(-1,1)$
  să fie toate pozitive
      - ***i.i.d*** = "independente și identic distribuite"

### Multiple v.a. normale

- Fie un set de $N$ v.a. normale $(A_1, ...A_N)$, 
cu medii diferite $\mu_i$ dar aceeași deviație standard $\sigma$

- Probabilitatea ca $(A_1,...A_N)$ să fie în jurul valorii 
$(x_1, ...x_N)$ este
$$w_{A_1,...A_N}(x_1,...x_N) = \frac{1}{(\sigma\sqrt{2\pi})^N} e^{\frac{(x_1-\mu_1)^2+...+(x_N - \mu_N)^2}{2\sigma^2}}$$

- Probabilitatea depinde de **distanța Euclideană** dintre
$\mathbf{x}=(x_1,...x_N)$ și $\mathbf{\mu} = (\mu_1,...\mu_N)$

### Distanța Euclideană

- **Distanța Euclideană (geometrică)** între 2 vectori N-dimensionali
 $$d(\mathbf{u},\mathbf{v}) = \| \mathbf{u}-\mathbf{v} \| = \sqrt{(u_1-v_1)^2+...+(u_N - v_N)^2}$$

- Unidimensional: $\|\mathbf{u}-\mathbf{v}\| = |u-v|$

- 2D: $\|\mathbf{u}-\mathbf{v}\| = \sqrt{(u_1 - v_1)^2 + (u_2 - v_2)^2}$
       
- 3D: $\|\mathbf{u}-\mathbf{v}\| = \sqrt{(u_1 - v_1)^2 + (u_2 - v_2)^2 + (u_3 - v_3)^2}$

- ...

- N-dimensional: $\|\mathbf{u}-\mathbf{v}\| = \sqrt{\sum_{i=1}^N(u_i - v_i)^2}$

- ...

- Semnale continue: $\|\mathbf{u}-\mathbf{v}\| = \sqrt{\int_{-\infty}^{\infty}(u(t) - v(t))^2 dt}$

### Multiple v.a. normale

- Probabilitatea a $N$ v.a. normale, independente,
cu același $\sigma$ dar diferite $\mu_i$
depinde de **pătratul distanței Euclidiene față de vectorul medie** $\mathbf{\mu} = (\mu_1,...\mu_N)$
    - Aproape de $\mu$: probabilitate mai mare
    - Departe de $\mu$: probabilitate redusă
    - Două puncte la aceeași distanță de $\mu$ au aceeași probabilitate

### Distribuția normală 2D

- Distribuția a 2 v.a. normale (distribuția normală 2D)
![](img/2DNormal.png)

### Distribuția normală 2D  - vedere de sus

- Vedere de sus
- Aici, $\mu = (0,0)$
- Probabilitatea scade pe măsură ce crește distanța față de centru,
în cercuri concentrice (simetric)

![](img/2DNormal-TopView.png){.id width=50%}


### Medii statistice

* V.a. sunt caracterizate prin medii statistice ("*momente*")

* Valoarea medie (momentul de ordin 1)

* Pentru v.a. continue:
$$\overline{A} = E\{A\} = \int_{-\infty}^{\infty} x \cdot w_A(x) dx$$

* Pentru v.a. discrete:
$$\overline{A} = E\{A\} = \sum_{x=-\infty}^{\infty} x \cdot w_A(x)$$

* (Exemplu: entropia H(X) = valoarea medie a informației)

* Notație uzuală: $\mu$

### Proprietățile valorii medii

* Calculul valorii medii este o operație **liniară**
    * pentru că, la bază, integrala / suma este o operație liniară

* Liniaritate
$$E\{c_1A + c_2B\} = c_1E\{A\} + c_2E\{B\}$$

* Sau:
$$E\{cA\} = c E\{A\}, \forall c \in \mathbb{R}$$
$$E\{A + B\} = E\{A\} + E\{B\}$$

* Fără demonstrație

### Valoarea pătratică medie

* Valoarea pătratică medie = valoarea medie a pătratelor valorilor

* Momentul de ordin 2

* Pentru v.a. continue:
$$\overline{A^2} = E\{A^2\} = \int_{-\infty}^{\infty} x^2 \cdot w_A(x) dx$$

* Pentru v.a. discrete:
$$\overline{A^2} = E\{A^2\} = \sum_{-\infty}^{\infty} x^2 \cdot w_A(x)$$

* Interpretare: media pătratelor = energia medie a unui semnal

### Varianța

* Varianța = valoarea pătratică medie a abaterii față de valoarea medie :)

* V.a. continue:
$$\sigma^2 = \overline{\left\{ A - \mu \right\}^2} = \int_{-\infty}^{\infty} (x-\mu)^2 \cdot w_A(x) dx$$

* V.a. discrete:
$$\sigma^2 = \overline{\left\{ A - \mu \right\}^2} = \sum_{-\infty}^{\infty} (x-\mu)^2 \cdot w_A(x)$$

* Interpretare: cât de mult variază valorile în jurul mediei
    * $\sigma^2 =$ mare: abateri mari față de medie
    * $\sigma^2 =$ mic: valori concentrate în jurul mediei

### Legătura între cele trei mărimi

* Legătura între medie, valoarea pătratică medie și varianță:
$$\begin{split}
\sigma^2 &= \overline{\left\{ A - \mu \right\}^2} \\
&= \overline{A^2 - 2 \cdot A \cdot \mu + \mu^2} \\
&= \overline{A^2} - 2 \mu \overline{A} + \mu^2 \\
&= \overline{A^2} - \mu^2
\end{split}$$

### Suma variabilelor aleatoare

* Suma a două sau mai multe v.a. **independente** este tot o v.a.

* Distribuția ei = **convoluția** distribuțiilor v.a. componente

* Dacă $C = A + B$, atunci:
$$w_C(x) = w_A(x) \star w_B(x)$$

* Caz particular: dacă $A$ și $B$ sunt v.a. normale, cu $\mathcal{N}(\mu_A, \sigma_A^2)$ și $\mathcal{N}(\mu_B, \sigma_B^2)$, atunci:
    * $C$ este tot o v.a. cu distribuție normală, $\mathcal{N}(\mu_C, \sigma_C^2)$, având:
    * media = suma mediilor: $\mu_C = \mu_A + \mu_B$
    * varianța = suma varianțelor: $\sigma_C^2 = \sigma_A^2 + \sigma_B^2$
    
## II.2 Procese aleatoare

### Procese aleatoare

* Un **proces aleator** = o secvență de variabile aleatoare indexate (înșiruite) în timp

* Proces aleator **în timp discret** $f[n]$ = o secvență de v.a. la momente de timp discrete
    * ex: o secvență de 50 aruncări de zar, cotația zilnică a unor acțiuni la bursă

* Proces aleator **în timp continuu** $f(t)$ = o secvență de v.a. la orice moment de timp
    * ex: un semnal tip zgomot de tensiune

* Fiecare eșantion dintr-un proces aleator este o v.a. de sine stătătoare
    * ex:. $f(t_0)$  = valoarea la momentul $t_0$ este o v.a.

### Realizări ale proceselor aleatoare

* **Realizare** a unui p.a. = o secvență particulară de realizări ale v.a. componente
    * ex: un anume semnal de zgomot măsurat cu un osciloscop; dar am fi putut
    măsura orice altă realizare

* Când considerăm un p.a., considerăm întregul set de realizări posibile
    * la fel ca atunci când considerăm o v.a.

### Distribuții de ordin 1 ale proceselor aleatoare

* Fiecare eșantion $f(t_1)$ dintr-un proces aleator este o v.a.
    - descris de o **distribuție de ordin 1**
    - are FR $F_1(x;t_1)$
    - are FDP / FMP $w_1(x;t_1) = \frac{dF_1(x;t_1)}{dx}$
    - distribuția depinde de momentul $t_1$

* Un eșantion la alt moment $t_2$ este o v.a. diferită, cu funcții posibil diferite
    * altă FR $F_1(x;t_2)$
    * altă FDP / FMP $w_2(x;t_2) = \frac{dF_1(x;t_2)}{dx}$

* Aceste funcții descriu distribuția valorilor unui eșantion

* Indicele $w_1$ arată că considerăm o singură v.a. din proces (distribuții *de ordin 1*)

* Similar pentru p.a. discrete

### Distribuții de ordin 2

* O pereche de v.a. $f(t_1)$ și $f(t_2)$ formează un sistem de 2 v.a.:
    - sunt descrise de o **distribuție de ordin 2**
    - au FR comună $F_2(x_i, x_j; t_1, t_2)$
    - au FDP / FMP comună $w_2(x_i, x_j; t_1, t_2) = \frac{\partial^2 F_2(x_i, x_j;t_1, t_2)}{\partial x_i \partial x_j}$
    - distribuția depinde de momentele $t_1$ și $t_2$

* Aceste funcții descriu cum sunt distribuite valorile perechilor (distribuții *de ordin 2*)

* Similar pentru p.a. discrete

### Distribuții de ordin n

* Generalizare la $n$ eșantioane ale unui p.a.

* Un set de $n$ v.a. $f(t_1), ...f(t_n)$ dintr-un proces aleator $f(t)$:
    - sunt descrise de o **distribuție de ordin n**
    - au FR comună $F_n(x_1,... x_n; t_1,... t_n)$
    - au FDP / FMP comună $w_n(x_1,... x_n; t_1,... t_n) = \frac{\partial^2 F_n(x_1,... x_n;t_1,... t_n)}{\partial x_1 ... \partial x_n}$
    - depind de momentele de timp $t_1$, $t_2$, ... $t_n$

* Aceste funcții descriu cum sunt distribuite valorile seturilor de $n$ valori (distribuții *de ordin n*)

* Similar pentru p.a. discrete

### Medii statistice

Procesele aleatoare sunt caracterizate de medii statistice și temporale

Pentru procese continue:

1. Valoarea medie
$$\overline{f(t_1)} = \mu(t_1) = \int_{-\infty}^{\infty} x \cdot w_1(x; t_1) dx$$

2. Valoarea pătratică medie
$$\overline{f^2(t_1)} = \int_{-\infty}^{\infty} x^2 \cdot w_1(x; t_1) dx$$

### Medii statistice - varianța

3. Varianța
$$\sigma^2(t_1) = \overline{\left\{ f(t_1) - \mu(t_1) \right\}^2} = \int_{-\infty}^{\infty} (x-\mu(t_1)^2 \cdot w_1(x; t_1) dx$$

* Varianța se poate calcula pe baza celorlalte două:
$$\begin{split}
\sigma^2(t_1) =& \overline{\left\{ f(t_1) - \mu(t_1) \right\}^2} \\
=& \overline{f(t_1)^2 - 2f(t_1)\mu(t_1) + \mu(t_1)^2} \\
=& \overline{f^2(t_1)} - \mu(t_1)^2
\end{split}$$

* Observații:
    * aceste trei valori sunt calculate pentru toate realizările, la momentul $t_1$
    * ele caracterizează doar eșantionul de la momentul $t_1$
    * la alt moment de timp $t_2$, v.a. $f(t_2)$ este diferită, și valorile medii pot diferi

### Medii statistice - autocorelația

4. Funcția de autocorelație
$$R_{ff}(t_1,t_2) = \overline{f(t_1) f(t_2)} = \int_{-\infty}^\infty \int_{-\infty}^\infty x_1 x_2 w_2(x_1, x_2; t_1, t_2) dx_1 dx_2$$

5. The correlation function (for different random processes $f(t)$ and $g(t)$)
$$R_{fg}(t_1,t_2) = \overline{f(t_1) g(t_2)} = \int_{-\infty}^\infty \int_{-\infty}^\infty x_1 y_2 w_2(x_1, y_2; t_1, t_2) dx_1 dy_2$$

* Observații:
    * aceste funcții au valori diferite pentru diverse perechi de valori ($t_1$,$t_2$)

### Procese aleatoare discrete

Pentru **procese aleatoare discrete**, se înlocuiește $\int$ cu $\sum$:

1. $\overline{f[t_1]} = \mu(t_1) = \sum_{x=-\infty}^{\infty} x \cdot w_1(x; t_1)$

2. $\overline{f^2[t_1]} = \sum_{x=-\infty}^{\infty} x^2 \cdot w_1(x; t_1)$

3. $\sigma^2(t_1) = \overline{\left\{ f[t_1] - \mu(t_1) \right\}^2} = \sum_{x=-\infty}^{\infty} (x-\mu(t_1)^2 \cdot w_1(x; t_1)$

4. $R_{ff}(t_1,t_2) = \overline{f[t_1] f[t_2]} = \sum_{x_1=-\infty}^\infty \sum_{x_2=-\infty}^\infty x_1 x_2 w_2(x_1, x_2; t_1, t_2)$

5. $R_{fg}(t_1,t_2) = \overline{f[t_1] g[t_2]} = \sum_{x_1=-\infty}^\infty \sum_{x_2=-\infty}^\infty x_1 y_2 w_2(x_1, y_2; t_1, t_2)$


### Medii temporale

* Dacă avem acces doar la o singură realizare $f^{(k)}(t)$ a procesului?
* Calculăm valorile medii **pentru o singură realizare $f^{(k)(t)}$, în timp**
* Pentru procese continue:

1. Valoarea medie temporală
$$\overline{f^{(k)}(t)} = \mu^{(k)} = \lim_{T \to \infty} \frac{1}{T} \int_{T/2}^{T/2} f^{(k)}(t) dt$$

2. Valoarea medie pătratică temporală 
$$\overline{[f^{(k)}(t)]^2} = \lim_{T \to \infty} \frac{1}{T} \int_{-T/2}^{T/2} [f^{(k)}(t)]^2 dt$$

### Varianța temporală
3. Varianța temporală
$$\sigma^2 = \overline{\left\{ f^{(k)}(t) - \mu^{(k)} \right\}^2} = \lim_{T \to \infty} \frac{1}{T} \int_{-T/2}^{T/2} (f^{(k)}(t)-\mu^{(k)})^2 dt$$

* Poate fi calculată ca:
$$\sigma^2 = \overline{[f^{(k)}(t)]^2} - [\mu^{(k)}]^2$$

* Observație:
    * aceste valori nu mai depind de timpul $t$

### Autocorelația temporală

4. Funcția de autocoreație temporală
$$\begin{split}
R_{ff}(t_1,t_2) =& \overline{f^{(k)}(t_1 + t) f^{(k)}(t_2+t)} \\
=& \lim_{T \to \infty} \frac{1}{T} \int_{-T/2}^{T/2} f^{(k)}(t_1+t) f^{(k)}(t_2 + t) dt
\end{split}$$

5. Funcția de corelație temporală (pentri două procese diferite $f(t)$ și $g(t)$)
$$\begin{split}
R_{fg}(t_1,t_2) =& \overline{f^{(k)}(t_1 + t) g^{(k)}(t_2+t)}\\
=& \lim_{T \to \infty} \frac{1}{T} \int_{-T/2}^{T/2} f^{(k)}(t_1+t) g^{(k)}(t_2 + t) dt
\end{split}$$

### Procese aleatoare discrete

Pentru **procese aleatoare discrete**, se înlocuiește $\int$ cu $\sum$, $T$ cu $N$,
și se împarte la $2N+1$ în loc de $2T$

1. $\overline{f^{(k)}[t]} = \mu^{(k)} = \lim_{N \to \infty} \frac{1}{2N+1} \sum_{t=-N}^{N} f^{(k)}[t]$

2. $\overline{[f^{(k)}[t]]^2} = \lim_{N \to \infty} \frac{1}{2N+1} \sum_{t=-N}^{N} (f^{(k)}[t])^2$

3. $\sigma^2 = \overline{\left\{ f^{(k)}[t] - \mu^{[k]} \right\}^2} = \lim_{N \to \infty} \frac{1}{2N+1} \sum_{t=-N}^{N} (f^{(k)}[t]-\mu^{(k)})^2$

### Procese aleatoare discrete

4. Autocorelația temporală:

$$\begin{split}
R_{ff}(t_1,t_2) =& \overline{f^{(k)}[t_1 + t] f^{(k)}[t_2+t]} \\
=& \lim_{N \to \infty} \frac{1}{2N+1} \sum_{t=-N}^{N} f^{(k)}[t_1+t] f^{(k)}[t_2 + t]
\end{split}$$

5. Corelația temporală:

$$\begin{split}
R_{fg}(t_1,t_2) =& \overline{f^{(k)}[t_1 + t] g^{(k)}[t_2+t]}\\
=& \lim_{N \to \infty} \frac{1}{2N+1} \sum_{t=-N}^{N} f^{(k)}[t_1+t] g^{(k)}[t_2 + t]
\end{split}$$

### Realizări de lungime finită

Dacă o realizare nu se întinde de la timpul $-\infty$ la $\infty$, 
ci doar de la un $t_{min}$ la $t_{max}$,
se folosește $\int_{t_{min}}^{t_{max}}$ sau $\sum_{t_{min}}^{t_{max}}$ pentru mediile temporale

* Exemplu: calculați mediile temporale pentru realizarea de lungime finită
$$\{1,-1,2,-2,3,-3,4,-4,5,-5\}$$


### Medii statistice și temporale

* Mediile statistice sunt, de obicei, cele de interes
    - dar necesită cunoașterea distribuțiilor
* În practică, pentru semnale necunoscute, se poate măsura doar o singură realizare
    - putem calcula doar mediile temporale
* Din fericire, în multe cazuri mediile statistice și temporale sunt identice ("*ergodicitate*")

### Procese aleatoare staționare

* În general, mediile statistice depind de timp
    * pot fi diferite la alt moment de timp $t_2$

* Proces aleator **staționar** = mediile statistice rămân aceleași 
la modificarea originii timpului (întârzierea semnalului)

* Echivalent: Distribuțiile (FDP/FMP) eșantioanelor rămân identice la modificarea originii timpului
$$w_n(x_1,...x_n; t_1,...t_n) = w_n(x_1,...x_n; t_1+\tau,... t_n + =tau)$$

* Practic, mediile nu trebuie să mai depindă de timp $t$

### Staționar în sens strict sau larg

* Proces aleator **staționar în sens strict**:
    * relația e valabilă pentru toți $n$

* Proces aleator **staționar în sens larg**:
    * relația e valabilă doar pentru $n=1$ și $n=2$  (cele mai folosite)

### Consecințe ale staționarității

* Pentru $n=1$:
$$w_1(x_i;t_1) = w_1(x_i; t_2) = w_1(x_i)$$

* Valoarea medie, valoarea medie pătratică, varianța
unui eșantion sunt **aceleași** la orice moment de timp $t$
$$\overline{f(t)} = constant, \forall t$$
$$\overline{f^2(t)} = constant, \forall t$$
$$\sigma^2(t) = constant, \forall t$$

### Consecințe ale staționarității

* Pentru $n=2$:
$$w_2(x_i,x_j;t_1,t_2) = w_2(x_i,x_j;0, t_2-t_1) = w_2(x_i,x_2; t_2-t_1)$$

* Funcția de autocorelație depinde doar de **diferența de timp**
$\tau = t_2 - t_1$ dintre eșantioane
$$R_{ff}(t_1,t_2) = R_{ff}(0, t_2 - t_1) = R_{ff}(\tau) = \overline{f(t) f(t + \tau)}$$

* Depinde doar de valoarea $\tau$ = diferența de timp dintre cele două eșantioane

### Consecințe ale staționarității

* Definiția funcției de autocorelație pentru p.a. **staționare**:
    * funcția depinde numai de $\tau = t_2 - t_1$, în loc de $t_1$ și $t_2$

* Autocorelația statistică: formula rămâne aceeași

* Autocorelația temporală:
    * pentru p.a. continue
    $$\begin{split}
    R_{ff}(\tau) =& \overline{f(t) f(t + \tau)} \\
    =& \lim_{T \to \infty} \frac{1}{T} \int_{-T/2}^{T/2} f^{(k)}(t) f^{(k)}(t + \tau) dt
    \end{split}$$

    * pentru p.a. discrete
    $$\begin{split}
    R_{ff}(\tau) =& \overline{f(t) f(t + \tau)} \\
    =& \lim_{N \to \infty} \frac{1}{2N+1} \sum_{t=-N}^{N} f^{(k)}[t] f^{(k)}[t + \tau]
    \end{split}$$
    
    * lungime finită: se limitează integralele / sumele la intervalul avut la dispoziție, $\int_{t_{min}}^{t_{max}}$ sau $\sum_{t_{min}}^{t_{max}}$


### Consecințe ale staționarității

* Idem pentru funcția de corelație dintre procese aleatoare diferite

* Depinde doar de **diferența de timp** $\tau = t_2 - t_1$ dintre două eșantioane
$$R_{fg}(t_1,t_2) = R_{fg}(0, t_2 - t_1) = R_{fg}(\tau) = \overline{f(t) g(t + \tau)}$$

* Definiția este similară cu formulele de la f. de autocorelație de pe slide-ul anterior

### Interpretarea autocorelației

- $R_{ff}(\tau)$ = media produsului a două eșantioane situate la distanță de $\tau$
    - ne spune dacă eșantioanele variază în același sens sau nu

- Idem pentru corelație, doar că eșantioanele provin din p.a. diferite, $f$ și $g$

- Exemplu:
    - $R_{ff}(0.5) > 0$: două eșantioane decalate cu $0.5$ secunde tind să varieze în aceeași direcție
(ambele pozitive, ambele negative => produsele sunt majoritar pozitive)
    - $R_{ff}(1) < 0$: două eșantioane decalate cu 1 secundă tind să varieze în direcții opuse
(când unul e pozitiv, celălalt e negativ => produsele sunt majoritar negative)
    - $R_{ff}(2) = 0$: două eșantioane decalate cu 2 secunde sunt necorelate
(produsele sunt în medie 0, deci la fel de multe pozitive cât negative)

### Procese aleatoare ergodice

* În practică, avem acces la o singură realizare

* Proces aleator **ergodic** = mediile temporale pe orice realizare sunt **identice** cu mediile statistice

* Ergodicitatea înseamnă:
    * Se pot calcule toate mediile pe baza unei singure realizări
        * dar realizarea trebuie să fie foarte lungă (lungimea $\to \infty$) pentru valori precise
    * Toate realizările sunt similare unele cu altele, dpdv statistic
        * o realizare este caracteristică pentru întreg procesul aleator

### Procese aleatoare ergodice

* Majoritatea proceselor aleatoare de interes sunt ergodice și staționare
    * de ex. zgomote de tensiune

* Exemplu de proces ne-ergodic:
    * se aruncă un zar, următoarele 50 valori sunt identice cu prima valoare
    * o singură realizare nu e caracteristică pentru tot procesul


## I.3 Proprietăți ale autocorelației

### Densitatea spectrală de putere

* Densitatea spectrală de putere (DSP) $S_{ff}(\omega)$ reprezintă 
puterea procesului aleator la fiecare frecvență $f$ ($\omega = 2 \pi f$)

* DSP descrie cum este distribuită puterea semnalului în frecvență
    * de ex. unele procese au mai multă putere la frecvențe joase, altele la frecvențe înalte

* Puterea în banda de frecvență $[f_1, f_2]$ este $\int_{f_1}^{f_2} S_{ff}(\omega) d\omega$

* Puterea totală a procesului aleator este $P = \int_{-\infty}^{\infty} S_{ff}(\omega) d\omega$

* DSP este o funcție măsurabilă practic
    * poate fi determinată experimental
    * este importantă în aplicații practice (inginerești)

### Teorema Wiener-Hincin

Teoremă:

* **Densitatea spectrală de putere = transformata Fourier a funcției de autocorelație**
$$S_{ff}(\omega) = \int_{-\infty}^{\infty} R_{ff}(\tau) e^{- j \omega \tau} d\tau$$
$$R_{ff}(\tau) = \frac{1}{2 \pi}\int_{-\infty}^{\infty} S_{ff}(\omega) e^{j \omega \tau} d\omega$$

* Fără demonstrație

* Leagă două concepte de natură diferită
    * funcția de autocorelație: o proprietate *statistică*
    * DSP: o proprietate *fizică* (ține de energia semnalului; importantă în aplicații practice)

### Zgomot alb

* Zgomot alb = proces aleator cu funcția de autocorelație egală cu un Dirac
$$R_{ff}(\tau) = \delta(\tau)$$

    - este proces aleator: orice eșantion este o variabilă aleatoare
    - autocorelația este un Dirac: este 0 pentru orice $\tau \neq 0$
    - oricare două eșantioane diferite ($\tau \neq 0$) au corelație zero (necorelate)
        - valorile a două eșantioane nu au legătură între ele
    
* Densitatea spectrală de putere = transf. Fourier a unui Dirac = constantă $\forall \omega$
    * putere constantă la toate frecvențele, până la $f = \infty$

* Zgomotul alb poate avea orice distribuție (normală, uniformă etc.)
    - termenul "zgomot alb" nu se referă la distribuția eșantioanelor,
    ci la faptul că valorile eșantioanele sunt necorelate
    
### Zgomot alb de bandă limitată    
    
* În practică, puterea scade la 0 la frecvențe foarte înalte
    - pentru că puterea totală $P = \int_{-\infty}^{\infty} S_{ff}{\omega}$ nu poate fi infinită
    - zgomot alb "*de bandă limitată*"
    
* În acest caz, autocorelația = aproximativ un Dirac, dar nu infinit de "subțire"
    * eșantioane foarte apropiate sunt totuși corelate
    * de ex. din cauza unor mici capacități parazite

### AWGN

- **AWGN** = Additive White Gaussian Noise
    - Zgomot alb, Gaussian, aditiv
    - tipul de zgomot cel mai frecvent întâlnit în aplicații

- Înseamnă:
    - aditiv: zgomotul se adună cu semnalul original (de ex. nu se multiplică cu acesta)
    - gaussian: eșantioanele au distribuția normală
    - alb: valorile eșantioanelor sunt necorelate între ele 

### Examen 2018-2019

- Până aici s-a făcut în 2018-2019. Celelalte slide-uri din acest fișier nu se cer.

### Proprietățile funcției de autocorelație

1. Este o funcție pară
$$R_{ff}(\tau) = R_{ff}(-\tau)$$

    * Demonstrație: Schimbare de variabilă în definiție

2. La infinit, tinde la o valoare constantă
$$R_{ff}(\infty) = \overline{f(t)}^2 = const$$

    * Dem.: două eșantioane la un interval $\infty$ sunt necesar independente

3. Are valoarea maximă în 0
$$R_{ff}(0) \geq R_{ff}(\tau)$$

    * Dem.: se pornește de la $\overline{(f(t) - f(t + \tau))^2} \geq 0$
    * Interpretare: eșantioane diferite mai pot varia diferit, dar un eșantion variază întotdeauna identic cu sine însuși

### Proprietățile funcției de autocorelație

4. Valoarea în 0 = puterea procesului aleator
$$R_{ff}(0) = \frac{1}{2 \pi} \int_{-\infty}^{\infty} S_{ff}(\omega) d\omega$$

    * Dem.: Se pune $\tau = 0$ în transf. Fourier inversă din teorema Wiener-Hincin

5. Varianța = diferența între valoarea din 0 și cea de la $\infty$
$$\sigma^2 = R_{ff}(0) - R_{ff}(\infty)$$

    * Dem.: $R_{ff}(0) = \overline{f(t)^2}$, $R_{ff}(\infty) = \overline{f(t)}^2$

### Autocorelația unui proces aleator filtrat

* Fie un proces aleator aplicat la intrarea unui sistem
    * fie în timp continuu: intrarea $x(t)$, sistemul $H(s)$, ieșirea $y(t)$
    * fie în timp discret: intrarea $x[n]$, sistemul $H(z)$, ieșirea $y[n]$
    
* Cum depinde autocorelația ieșirii $y$ de cea a intrării $x$?

* Se știe că $y$ este convoluția lui $x$ cu răspunsul la impuls $h$

### Dezvoltare matematică

* Pentru un proces aleator în timp discret
$$\begin{split}
R_{yy}(\tau) =& \overline{y[n] y[n + \tau]}\\
=& \overline{\sum_{k_1=-\infty}^\infty h[k_1] x[n-k_1] \sum_{k_2=-\infty}^\infty h[k_2] x[n+\tau-k_2]}\\
=& \sum_{k_1=-\infty}^\infty \sum_{k_2=-\infty}^\infty h[k_1] h[k_2] \overline{x[n-k_1] x[n+\tau-k_2]}\\
=& \sum_{k_1=-\infty}^\infty \sum_{k_2=-\infty}^\infty h[k_1] h[k_2] R_{xx}[\tau - k_1 + k_2]
\end{split}$$

* Din teorema Wiener-Hincin se știe că:
$$S_{ff}(\omega) = \sum_{\tau = -\infty}^{\infty} R_{ff}(\tau) e^{- j \omega \tau}$$


### Dezvoltare matematică

* Așadar
$$
S_{yy}(\omega) = \sum_{\tau=-\infty}^{\infty} \sum_{k_1=-\infty}^\infty \sum_{k_2=-\infty}^\infty h[k_1] h[k_2] R_{xx}[\tau - k_1 + k_2] e^{- j \omega \tau}
$$

* Schimbare de variabilă $\tau - k_1 + k_2 = u$
    * rezultă $\tau = u + k_1 - k_2$ 

$$\begin{split}
S_{yy}(\omega) =& \sum_{u=-\infty}^{\infty} \sum_{k_1=-\infty}^\infty \sum_{k_2=-\infty}^\infty h[k_1] h[k_2] R_{xx}[u] e^{- j \omega (u + k_1 + k_2)}\\
=& \sum_{u=-\infty}^{\infty} R_{xx}[u] e^{- j \omega u} \sum_{k_1=-\infty}^\infty h[k_1] e^{- j \omega k_1} \sum_{k_2=-\infty}^\infty h[k_2]  e^{ j \omega k_2}\\
=& S_{xx}(\omega) \cdot H(\omega) \cdot H*^(\omega)\\
=& S_{xx}(\omega) \cdot |H(\omega)|^2\\
\end{split}$$

### Rezultat

$$S_{yy}(\omega) = S_{xx}(\omega) \cdot |H(\omega)|^2$$

* DSP a lui $y$ = DSP a lui $x$ multiplicată cu răspunsul în amplitudine, la pătrat, al filtrului

* Relația este valabilă și pentru procese aleatoare continue

### Aplicații ale (auto)corelației

* Căutarea unei anume porțiuni într-un semnal mai mare

* Corelația a două semnale = o măsura a **similarității** celor două semnale
    * Funcția de corelație măsoară similaritatea unui semnal cu toate versiunile decalate ale celuilalt
    * Exemplu numeric la tablă, semnale de lungime finită
    
* Corelația poate fi utilizată pentru localizare
    * Funcția de (auto)corelație are valori mari atunci când cele două semnale se potrivesc
    * Valori mari sunt atunci când valorile pozitive / negative ale semnalelor se potrivesc
    * Valori mici atunci când nu se potrivesc
    
### Semnalul căutat

```
/home/ncleju/.local/bin/pweave:6: UserWarning: In Matplotlib 3.3
individual lines on a stem plot will be added as a LineCollection
instead of individual lines. This significantly improves the
performance of a stem plot. To remove this warning and switch to the
new behaviour, set the "use_line_collection" keyword argument to True.
  from pweave.scripts import weave
```

![](figures/01_SemnaleAleatoare_figure12_1.png)\



### Semnalul de dimensiuni mari


```
/home/ncleju/.local/bin/pweave:6: UserWarning: In Matplotlib 3.3
individual lines on a stem plot will be added as a LineCollection
instead of individual lines. This significantly improves the
performance of a stem plot. To remove this warning and switch to the
new behaviour, set the "use_line_collection" keyword argument to True.
  from pweave.scripts import weave
```

![](figures/01_SemnaleAleatoare_figure13_1.png)\


### Rezultatul corelației


```
/home/ncleju/.local/bin/pweave:6: UserWarning: In Matplotlib 3.3
individual lines on a stem plot will be added as a LineCollection
instead of individual lines. This significantly improves the
performance of a stem plot. To remove this warning and switch to the
new behaviour, set the "use_line_collection" keyword argument to True.
  from pweave.scripts import weave
```

![](figures/01_SemnaleAleatoare_figure14_1.png)\


### Identificare de sistem

* Determinarea răspunsului la impuls al unui sistem necunoscut, liniar și invariant în timp

* Se bazează pe corelația intrării cu ieșirea sistemlui

![System identification setup](img/SystemIdentif.png){#id .class width=60%}

### Identificare de sistem

$$\begin{split}
R_{fg}(\tau) =& \overline{f[n] g[n + \tau]}\\
=& \overline{f[n] \sum_{k=-\infty}^\infty h[k] f[n+\tau-k]}\\
=& \sum_{k=-\infty}^\infty h[k] \overline{f[n] f[n+\tau-k]}\\
=& \sum_{k=-\infty}^\infty h[k] R_{ff}[\tau - k]\\
=& h[\tau] \star R_{ff}[\tau]
\end{split}$$

* Dacă intrarea $f$ este **zgomot alb** cu puterea $A$, $R_{ff}[n] = A \cdot \delta[n]$, și
$$R_{fg}(\tau) = h[\tau] \star R_{ff}[\tau] = A \cdot h[\tau] \star \delta[\tau] = A \cdot h[\tau]$$

* Corelația măsurată este proporțională cu răspunsul la impuls al sistemului necunoscut
