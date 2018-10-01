
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

### Realizări

- **Realizare** a unei v.a. = o valoare particulară posibilă 

- **Spațiul realizărilor** $\Omega$ = mulțimea valorilor posibile ale unei v.a
    - mulțimea tuturor realizărilor

- Exemplu: aruncarea unui zar
    - V.a. se notează $X$
    - Se poate obține o realizare $X = 3$
    - Dar s-ar fi putut obține orice valoare din spațiul realizărilor
    $$\Omega = \left\{1, 2, 3, 4, 5, 6\right\}$$

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
$$F_A(x) = \sum_{all \;\; t \le x} w_A(t)$$

- Exemplu pentru zar: grafic, la tablă

### Funcția densitate de probabilitate

- Fie o v.a. **continuă** $A$

- **Funcția densitate de probabilitate (FDP)** 
= probabilitatea ca valoarea lui $A$ să fie într-o vecinătate $\epsilon$ mică în jurul lui $x$, totul supra $\epsilon$

- Se notează $w_A(x)$, se mai numește **distribuția** variabilei A

- Informal: FDP reprezintă probabilitatea ca valoarea lui $A$ să fie **în jurul lui** $x$

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


### Distribuția normală

* Densitatea de probabilitate:

$$w_A(x) = \frac{1}{\sigma \sqrt{2 \pi}} e^{-\frac{(x-\mu)^2}{2 \sigma^2}}$$


![](figures/01_SemnaleAleatoare_figure1_1.png){width=8cm}\


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

### The normal distribution - 

- Distribuția descrește pe măsură ce $x$ se îndepărtează de centrul $\mu$
    - Datorită termenului $-(x - \mu)^2$ de la exponent
    - Valorile cele mai probabile sunt în jurul lui $\mu$ ($x - \mu = 0$)
    - Valorile apropiate de $\mu$ sunt mai probabile, valorile mai depărtate de $\mu$ sunt mai puțin probabile

- Distribuția exprimă o preferință pentru valori apropiate de $\mu$, 
cu probabilitate din ce în ce mai scăzută la valori mai depărtate de $\mu$

### Distribuția uniformă

* Densitatea de probabilitate = constantă între două limite 

$$w_A(x) = 
\begin{cases}
\frac{1}{b-a}, & x \in [a, b] \\
 0, &elsewhere
\end{cases}$$


![](figures/01_SemnaleAleatoare_figure2_1.png){width=8cm}\


### Distribuția uniformă

* Are doi parametri: limitele $a$ și $b$ ale intervalului

* "Înălțimea" funcției este $\frac{1}{b-a}$ pentru normalizare
    - pentru ca integrala (aria) să fie 1
    
* Sunt posibile doar valori din intervalul $[a, b]$
    - valorile din afara intervalului au probabilitatea 0

* Se notează cu $\mathcal{U} \;[a, b]$

### Alte distribuții

* Nenumărate variante, apar în diverse aplicații

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

* O funcție aplicată unei v.a. produce o altă v.a.

* Exemple: dacă $X$ este o v.a. distribuită $\mathcal{U}\;[0,10]$, atunci
    * $Y = 5 + X$ este o altă v.a., distribuită $\mathcal{U}\;[5,15]$
    * $Z = X^2$ este de asemenea o v.a.
    * $T = cos(X)$ este de asemenea o v.a.
    
* Motivație: dacă $X$ este aleatoare, și valorile $Y$, $Z$, $T$ sunt aleatoare

* X, Y, Z, T nu sunt independente
    * O anumită valoare a uneia implică automat și valoarea celorlalte


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

  * Fie $X$ o v.a. cu distribuția $\mathcal{N}(3, 2)$. 
Calculați probabilitatea ca $X \in [2, 4]$

### Sisteme de mai multe variabile aleatoare

* Fie un sistem cu două v.a. continue $X$ și $Y$

* Există funcția de repartiție comună:
$$F(x, y) = P\left\{ X \leq x \cap Y \leq y \right\}$$

* Densitatea de probabilitate comună:
$$w(x,y) = \frac{\partial^2 F(x,y)}{\partial x \partial y}$$

* FDP comună descrie probabilitatea ca $X$ și $Y$
să se găsească într-o vecinătate a lui $x$ și $y$, **simultan**

* Similar pentru v.a discrete: funcția masă de probabilitate comună
$$w(x,y) = P\left\{ X = x \cap Y = y \right\}$$


### Variabile independente

* Două v.a. $X$ și $Y$ sunt **independente** dacă valoarea uneia nu 
influențează în nici un fel valoarea celeilalte

* Pentru v.a. independente, probabilitatea ca $X=x$ și $Y=y$ este produsul
celor două probabilități

* V.a. discrete:
$$w(x,y) = w(x) \cdot w(y)$$
$$P\left\{ X = x \cap Y = y \right\} = P\left\{ X = x\right\} \cdot P\left\{ Y = y \right\}$$

* Valabilă pentru FR / FDP / FMP, v.a. continue sau aleatoare

* Idem pentru mai mult de două v.a.

### Variabile independente

Exercițiu: 

  * Calculați probabilitatea ca trei v.a. $X$, $Y$ și $Z$ i.i.d. $\mathcal{N}(-1,1)$
  să fie toate pozitive
      * ***i.i.d*** = "independente și identic distribuite"

### Medii statistice

* V.a. sunt caracterizate prin medii statistice ("*momente*")

* Valoarea medie (momentul de ordin 1)

* Pentru v.a. continue:
$$\overline{X} = E\{X\} = \int_{-\infty}^{\infty} x \cdot w(x) dx$$

* Pentru v.a. discrete:
$$\overline{X} = E\{X\} = \sum_{x=-\infty}^{\infty} x \cdot w(x) dx$$

* (Exemplu: entropia H(X) = valoarea medie a informației)

* Notație uzuală: $\mu$

### Proprietățile valorii medii

* Calculul valorii medii este o operație **liniară**
    * pentru că, la bază, integrala / suma este o operație liniară

* Liniaritate
$$E\{aX + bY\} = aE\{X\} + bE\{Y\}$$

* Sau:
$$E\{aX\} = a E\{X\}, \forall a \in \mathbb{R}$$
$$E\{X + Y\} = E\{X\} + E\{Y\}$$

* Fără demonstrație

### Valoarea pătratică medie

* Valoarea pătratică medie = valoarea medie a pătratelor valorilor

* Momentul de ordin 2

* Pentru v.a. continue:
$$\overline{X^2} = E\{X^2\} = \int_{-\infty}^{\infty} x^2 \cdot w(x) dx$$

* Pentru v.a. discrete:
$$\overline{X^2} = E\{X^2\} = \sum_{-\infty}^{\infty} x^2 \cdot w(x) dx$$

* Interpretare: media pătratelor = energia medie a unui semnal

### Dispersia (varianța)

* Dispersia (varianța) = valoarea pătratică medie a abaterii față de valoarea medie :)

* V.a. continue:
$$\sigma^2 = \overline{\left\{ X - \mu \right\}^2} = \int_{-\infty}^{\infty} (x-\mu)^2 \cdot w(x) dx$$

* V.a. discrete:
$$\sigma^2 = \overline{\left\{ X - \mu \right\}^2} = \sum_{-\infty}^{\infty} (x-\mu)^2 \cdot w(x) dx$$

* Interpretare: cât de mult variază valorile în jurul mediei
    * $\sigma^2 =$ mare: abateri mari față de medie
    * $\sigma^2 =$ mic: valori concentrate în jurul mediei

### Legătura între cele trei mărimi

* Legătura între medie, valoarea pătratică medie și dispersie:
$$\begin{split}
\sigma^2 &= \overline{\left\{ X - \mu \right\}^2} \\
&= \overline{X^2 - 2 \cdot X \cdot \mu + \mu^2} \\
&= \overline{X^2} - 2 \mu \overline{X} + \mu^2 \\
&= \overline{X^2} - \mu^2
\end{split}$$

### Suma variabilelor aleatoare

* Suma a două sau mai multe v.a. **independente** este tot o v.a.

* Distribuția ei = **convoluția** distribuțiilor v.a. componente

* Dacă $Z = X + Y$
$$w(z) = w(x) \star w(y)$$

* Caz particular: dacă $X$ și $Y$ sunt v.a. normale, cu $\mathcal{N}(\mu_X, \sigma_X^2)$ și $\mathcal{N}(\mu_Y, \sigma_Y^2)$, atunci:
    * $Z$ este tot o v.a. cu distribuție normală, $\mathcal{N}(\mu_Z, \sigma_Z^2)$, având:
    * media = suma mediilor: $\mu_Z = \mu_X + \mu_Y$
    * dispersia = suma dispersiilor: $\sigma_Z^2 = \sigma_X^2 + \sigma_Y^2$
    
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

* Fiecare eșantion $f(t_1)$ ($f[n_1]$) dintr-un p.a. este o v.a.
    * cu FR $F_1(x;t_1)$
    * cu FDP / FMP $w_1(x;t_1) = \frac{dF_1(x;t_1)}{dx}$

* Eșantionul de la momentul $t_2$ este o v.a. diferită, cu funcții posibil diferite
    * cu FR $F_1(x;t_2)$
    * cu FDP / FMP $w_2(x;t_2) = \frac{dF_1(x;t_2)}{dx}$

* Indicele $w_1$ arată că considerăm o singură v.a. din proces (distribuții *de ordin 1*)

* Similar pentru p.a. discrete

### Distribuții de ordin 2

* O pereche de v.a. $f(t_1)$ and $f(t_2)$ dintr-un proces aleator $f(t)$ au:
    * FR comună $F_2(x_i, x_j; t_1, t_2)$
    * FDP / FMP comună $w_2(x_i, x_j; t_1, t_2) = \frac{\partial^2 F_2(x_i, x_j;t_1, t_2)}{\partial x_i \partial x_j}$

* Aceste funcții descriu cum sunt distribuite valorile perechilor (distribuții *de ordin 2*)

* Similar pentru p.a. discrete

### Distribuții de ordin n

* Generalizare la $n$ eșantioane ale unui p.a.

* Un set de $n$ v.a. $f(t_1), ...f(t_n)$ dintr-un proces aleator $f(t)$ au:
    * FR comună $F_n(x_1,... x_n; t_1,... t_n)$
    * FDP / FMP comună $w_n(x_1,... x_n; t_1,... t_n) = \frac{\partial^2 F_n(x_1,... x_n;t_1,... t_n)}{\partial x_1 ... \partial x_n}$

* Aceste funcții descriu cum sunt distribuite valorile seturilor de $n$ valori (distribuții *de ordin n*)

* Similar pentru p.a. discrete

### Medii statistice

Procesele aleatoare sunt caracterizate de medii statistice sau temporale (*momente*)

1. Valoarea medie
$$\overline{f(t_1)} = \mu(t_1) = \int_{-\infty}^{\infty} x \cdot w_1(x; t_1) dx$$

2. Valoarea pătratică medie
$$\overline{f^2(t_1)} = \int_{-\infty}^{\infty} x^2 \cdot w_1(x; t_1) dx$$

### Medii statistice - dispersia

3. Dispersia
$$\sigma^2(t_1) = \overline{\left\{ f(t_1) - \mu(t_1) \right\}^2} = \int_{-\infty}^{\infty} (x-\mu(t_1)^2 \cdot w_1(x; t_1) dx$$

* Disperia se poate calcula pe baza celorlalte două:
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

### Medii temporale

* Dacă avem acces doar la o singură realizare a procesului?
* Calculăm valorile medii **pentru o singură realizare $f^{(k)(t)}$, în timp**

1. Valoarea medie temporală
$$\overline{f^{(k)}(t)} = \mu^{(k)} = \lim_{T \to \infty} \frac{1}{T} \int_{T/2}^{T/2} f^{(k)}(t) dt$$

2. Valoarea medie pătratică temporală 
$$\overline{[f^{(k)}(t)]^2} = \lim_{T \to \infty} \frac{1}{T} \int_{-T/2}^{T/2} [f^{(k)}(t)]^2 dt$$

### Dispersia temporală
3. Dispersia temporală
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

### Medii statistice și temporale

* Mediile statistice sunt, de obicei, cele de interes
* Dar, în practică, putem calcula doar mediile temporale
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

* Valoarea medie, valoarea medie pătratică, dispersia
unui eșantion sunt **aceleași** la orice moment de timp $t$
$$\overline{f(t)} = constant, \forall t$$
$$\overline{f^2(t)} = constant, \forall t$$
$$\sigma^2(t) = constant, \forall t$$

### Consecințe ale staționarității

* Pentru $n=2$:
$$w_2(x_i,x_j;t_1,t_2) = w_2(x_i,x_j;0, t_2-t_1) = w_2(x_i,x_2; t_2-t_1)$$

* Funcția de autocorelație depinde doar de **diferența de timp**
$\tau = t_2 - t_1$ dintre eșantioane, oriunde ar fi localizate
$$R_{ff}(t_1,t_2) = R_{ff}(0, t_2 - t_1) = R_{ff}(\tau) = \overline{f(t) f(t + \tau)}$$

* Este valoarea medie a produsului dintre două eșantioane separate de un interval de timp $\tau$

* Depinde doar de valoarea $\tau$ = diferența de timp dintre cele două eșantioane

### Consecințe ale staționarității

* Idem pentru funcția de corelație dintre procese aleatoare diferite

* Depinde doar de **diferența de timp** $\tau = t_2 - t_1$ dintre două eșantioane
$$R_{fg}(t_1,t_2) = R_{fg}(0, t_2 - t_1) = R_{fg}(\tau) = \overline{f(t) g(t + \tau)}$$

* Este valoarea medie a produsului dintre două eșantioane separate de un interval de timp $\tau$


### Procese aleatoare ergodice

* În practică, avem acces la o singură realizare

* Proces aleator **ergodic** = mediile temporale pe orice realizare sunt **identice** cu mediile statistice

* Se pot calcule toarte mediile pe baza unei singure realizări
    * realizarea trebuie să fie foarte lungă (lungimea $\to \infty$) pentru valori precise
    * o realizare este caracteristică pentru întreg procesul aleator
    * realizările sunt similare unele cu altele, dpdv statistic

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

* Puterea totală a procesului aleator este $\int_{-\infty}^{\infty} S_{ff}(\omega) d\omega$

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

* Zgomot alb = proces aleator cu funcția de autocorelație egală cu o funcție Dirac
$$R_{ff}(\tau) = \delta(\tau)$$

* Două eșantioane diferite ($\tau \neq 0$) au corelație zero (necorelate)
    * adică nu variază în mod similar
    
* Densitatea spectrală de putere = transf. Fourier a unui Dirac = constantă
    * putere constantă la toate frecvențele, până la $f = \infty$
    
* În practică, puterea scade la 0 la frecvențe foarte înalte
    * zgomot alb "*de bandă limitată*"
    * eșantioane foarte apropiate sunt totuși corelate

* Zgomotul alb poate avea diverse distribuții
    * normală, uniformă etc.


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

5. Dispersia = diferența între valoarea din 0 și cea de la $\infty$
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

![](figures/01_SemnaleAleatoare_figure3_1.png)\



### Semnalul de dimensiuni mari


![](figures/01_SemnaleAleatoare_figure4_1.png)\


### Rezultatul corelației


![](figures/01_SemnaleAleatoare_figure5_1.png)\


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
