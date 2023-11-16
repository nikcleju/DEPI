---
title: | 
       | Seminar 4
       | Decizii, decizii
subtitle: DEPI
documentclass: scrartcl
fontsize: 12pt
---

1. Un sistem *airbag* detectează un accident prin eșantionarea semnalului de la un senzor 
cu 2 valori posibile: $s_0(t) = 0$ (OK) sau $s_1(t) = A$ (accident), unde $A = 5$.

   Semnalul este afectat de zgomot gaussian $\mathcal{N}\;(\mu=0, \sigma^2=2)$.

   Costurile scenariilor sunt: $C_{00} = 0$, $C_{01} = 100$, $C_{10} = 10$, $C_{11} = 0$.

   Probabilitățile celor două ipoteze sunt $P(H_0) = 2/3$, $P(H_1) = 1/3$.

   La recepție e ia un singur eșantion $r$ din semnal.

    a. Găsiți regiunile de decizie $R_0$ și $R_1$ pentru toate criteriile de mai jos:
       - ML 
       - MPE
       - MR
       - Neyman-Pearson cu probabilitatea (condiționată) de alarmă falsă $P_{fa} \leq 0.01$
       - Un prag $T$ ales arbitrar la valoarea $T=3$
       
    b. Calculați probabilitatea de pierdere, pentru toate criteriile de mai sus
       
    b. Care este decizia luată cu fiecare criteriu de mai sus, dacă $r = 3.1$?

    d. Considerând criteriul MR, care este valoarea minimă a lui $A$ pentru ca probabilitatea (necondiționată) de pierdere sa fie maxim $P_{p} \leq 10^{-6}$?
    
    c. Repetați cerințele considerând zgomot uniform $U[-3, 3]$


2. Un semnal poate avea două valori, $s_0(t) = 0$ (ipoteza $H_0$) sau $s_1(t) = 6$ (ipoteza $H_1$), 
   unde $A = 6$. 

   Semnalul este afectat de zgomot gaussian $\mathcal{N}(0, \sigma^2=1)$.
   
   La recepție se iau 5 eșantioane, cu valorile $\left\{ 1.1, 4.4, 3.7, 4.1, 3.8 \right\}$.
   
    a. Ce decizie se ia cu criteriul ML?
    b. Ce decizie se ia cu criteriul MPE, dacă $P(H_0) = 2/3$ and $P(H_1) = 1/3$?
    c. Care e intervalul de valori posibile ale lui $P(H_0)$ pentru ca decizia cu criteriul MPE să fie $D_0$?
