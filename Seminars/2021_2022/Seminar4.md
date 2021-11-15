---
title: | 
       | Seminar 4
       | Alte criterii de decizie
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
    a. Găsiți decizia pentru eșantionul $r$, cu criteriul ML / MPE / MR
    a. Găsiți regiunile de decizie $R_0$ și $R_1$ pentru toate cele trei criterii
    c. Dar dacă zgomotul este uniform $U[-3, 3]$?

2. O sursa de informație furnizeaza doua mesaje cu probabilitățile $p(a_0) = 2/3$, $p(a_1) = 1/3$.
Mesajele sunt codificate prin semnale constante cu valorile $s_0(t) = -5$ (a0), și $s_1(t) = 5$(a1). 
Semnalele sunt afectate de zgomot uniform cu distribuția U[-6, 6]. 
La recepție se ia un singur eșantion $r$ din semnal.
	a. Care sunt regiunile de decizie, conform criteriului Neyman-Pearson cu valoarea maximă a $P_{af}$ de $10^{-2}$?
	b. Care este probabilitatea detecției corecte în acest caz?