---
title: | 
       | Seminar 4
       | Decizii, decizii
subtitle: DEPI
documentclass: scrartcl
fontsize: 12pt
---


1. Un sistem *airbag* detectează un accident prin eșantionarea semnalului de la un senzor
 cu 2 valori posibile: $s_0(t) = 0$ (OK) sau $s_1(t) = 5$ (accident).
Semnalul este afectat de zgomot gaussian$\mathcal{N}\;(\mu=0, \sigma^2=2)$.
Se ia un singur eșantion din semnal, cu valoarea $r = 3.1$.
Costurile scenariilor sunt: $C_{00} = 0$, $C_{01} = 100$, $C_{10} = 10$, $C_{11} = -100$.
Probabilitățile celor două ipoteze sunt $P(H_0) = 2/3$, $P(H_1) = 1/3$.
    a. Găsiți decizia pentru eșantionul $r$, cu criteriile ML / MPE / MR
    a. Găsiți regiunile de decizie $R_0$ și $R_1$ pentru toate cele trei criterii
    c. Dar dacă zgomotul este uniform $U[-3, 3]$?

1. Repetați exercițiul de mai sus, considerând un zgomot uniform $U[-3, 3]$.

   Pe lângă criteriile ML,MPE,MR, utilizați și criteriul Neyman-Pearson cu probabilitatea (condiționată) de alarmă falsă $P_{fa} = 0.01$



3. Un semnal poate avea două valori, $0$ (ipoteza $H_0$) sau $6$ (ipoteza $H_1$). 

   Semnalul este afectat de zgomot gaussian $\mathcal{N}(0, \sigma^2=1)$.
   
   La recepție se iau 5 eșantioane, cu valorile $\left\{ 1.1, 4.4, 3.7, 4.1, 3.8 \right\}$.
   
    a. Ce decizie se ia cu criteriul Maximum Likelihood?
    b. Ce decizie se ia cu criteriul Minium Probability of Error, dacă $P(H_0) = 2/3$ and $P(H_1) = 1/3$?
    c. Ce decizie se ia cu criteriul Minimum Risk, dacă $P(H_0) = 2/3$ and $P(H_1) = 1/3$, and $C_{00} = 0$, $C_{10} = 10$, $C_{01} = 20$, $C_{11} = 5$?
    d. Care e intervalul de valori posibile ale lui $P(H_0)$ pentru ca decizia cu criteriul MPE să fie $D_0$?
