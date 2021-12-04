---
title: | 
       | Seminar 5
       | Decizie cu mai multe eșantioane
subtitle: DEDP
documentclass: scrartcl
fontsize: 12pt
---

1.	Fie detecția unui semnal $s_1(t) = 3 \sin(2 \pi f_1 t)$ care poate fi prezent (ipoteza $H_1$) sau absent ($s_0(t)=0$, ipoteza $H_0$).
Semnalul este afectat de zgomot gaussian  $\mathcal{	N}(0, \sigma^2=1)$.
Valoarea lui $f_1 = 1$.
La recepție se iau două eșantioane la momentele de timp $t_1$ și $t_2$.
    
	a. Care sunt cele mai bune moment de eșantionare $t_1$ și $t_2$ pentru a maximiza performanțele detecției(depending on $f_1$)? Dar cele mai nepotrivite momente de timp?
    b. La recepție se iau citesc două eșantioane cu valorile $\left\{ 1.1, 4.4 \right\}$, la momentele de timp $t_1 = 0.125$ și $t_2 = 0.625$.
    Ce decizie se ia cu criteriul Maximum Likelihood?
    c. În aceleași condiții, cer decizie se ia cu criteriul Minimum Probability of Error, dacă
    $P(H_0) = 2/3$ and $P(H_1) = 1/3$?
    d. În aceleași condiții, cer decizie se ia cu criteriul Minimum Risk, dacă
    $P(H_0) = 2/3$ and $P(H_1) = 1/3$, și $C_{00} = 0$, $C_{10} = 10$, $C_{01} = 20$, $C_{11} = 5$?
    e. Dacă la recepție se ia un al treilea eșantion la momentul $t_3 = 0.5$, vor crește performanțele detecției?

	\smallskip


3. Un semnal poate avea două valori, $0$ (ipoteza $H_0$) sau $6$ (ipoteza $H_1$). 
Semnalul este afectat de zgomot gaussian $\mathcal{N}(0, \sigma^2=1)$.
La recepție se iau 5 eșantioane, cu valorile $\left\{ 1.1, 4.4, 3.7, 4.1, 3.8 \right\}$.
    a. Ce decizie se ia cu criteriul Maximum Likelihood?
    b. Ce decizie se ia cu criteriul Minium Probability of Error, dacă
    $P(H_0) = 2/3$ and $P(H_1) = 1/3$?
    c. Ce decizie se ia cu criteriul Minimum Risk, dacă
    $P(H_0) = 2/3$ and $P(H_1) = 1/3$, and $C_{00} = 0$, $C_{10} = 10$, $C_{01} = 20$, $C_{11} = 5$?
    d. Care e intervalul de valori posibile ale lui $P(H_0)$ pentru ca decizia cu criteriul MPE este $D_0$?

	\smallskip


2. Un semnal transmis poate avea forma $s_0(t)$ sau $s_1(t)$, conform figurilor. 
La recepție se primește semnalul $r(t)$ reprezentat în figură. 
Semnalul este afectat de zgomot gaussian $\mathcal{N}(0, \sigma^2=2)$.
Se consideră $P(H_0) = \frac{1}{4}$ și $P(H_0) = \frac{3}{4}$.
Găsiți decizia conform criteriului MPE, în două cazuri distincte:
    a. folosind trei eșantioane luate la momentele de timp $t_1 = 0.5$, $t_2 = 1.5$ și $t_2 = 3.5$
    b. folosind metoda observației continue (fără eșantionare)

	\ ![](fig/SIG_Haar1.png){.id width=25%} \      ![](fig/SIG_Haar2.png){.id width=25%} \      ![](fig/SIG_Rec.png){.id width=25%}  

	\smallskip

1. Fie următorul set de 10 vectori, compus din 5 vectori din clasa A și 5 vectori din clasa B:
    * Clasa A:
$$\vec{v}_1 = \begin{bmatrix}2 \\ -4\end{bmatrix}\;
\vec{v}_2 = \begin{bmatrix}1 \\ -5\end{bmatrix}\;
\vec{v}_3 = \begin{bmatrix}-2 \\ 6\end{bmatrix}\;
\vec{v}_4 = \begin{bmatrix}-3 \\ 4\end{bmatrix}\;
\vec{v}_5 = \begin{bmatrix}2 \\ -5\end{bmatrix}$$
    * Clasa B:
$$\vec{v}_6 = \begin{bmatrix}3 \\ 1\end{bmatrix}\;
\vec{v}_7 = \begin{bmatrix}-1 \\ 1\end{bmatrix}\;
\vec{v}_8 = \begin{bmatrix}-4 \\ -3\end{bmatrix}\;
\vec{v}_9 = \begin{bmatrix}-3 \\ 0\end{bmatrix}\;
\vec{v}_{10} = \begin{bmatrix}-2 \\ 3\end{bmatrix}$$

    Calculați clasa vectorului $\vec{x} = \begin{bmatrix}-2 \\ 5 \end{bmatrix}$
folosind algoritmul k-NN, pentru diverse valori ale lui $k$: $k=1$, $k=3$, $k=5$, $k=7$ and $k=9$
