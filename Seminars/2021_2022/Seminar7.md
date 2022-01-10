---
title: | 
       | Seminar 7
       | Estimare ML
subtitle: DEPI
documentclass: scrartcl
fontsize: 12pt
---
 
1. Un robot se deplasează pe o traiectorie liniară cu o viteză necunoscută $V$ centimetri/secundă,
pornind de la poziția $x_0 = 0$ la momentul inițial. 
La intervale de o secundă, robotul măsoară distanța parcursă folosind un senzor, afectat de zgomot gaussian $\mathcal{N}(0,\sigma^2=0.1)$.
Valorile măsurate la momentele $t_i = [1,2,3,4,5]$ sunt $r_i = [4.9, 9.8, 14.3, 21.2, 25.7]$

    a. Estimați viteza $v$ a robotului folosind estimarea ML.
	b. Preziceți poziția robotului la momentul $6$.
	c. Dacă presupunem că la momentul inițial poziția robotului nu este 0, ci o valoare necunoscută $x_0$, estimați perechea de parametri [v, $x_0$]
	folosind estimarea ML. Preziceți poziția robotului la momentul $6$.
	d. Scrieți sistemul de ecuații pentru estimarea ML presupunând că legea de mișcare este $x(t) = a \cdot t^2 + v_0 \cdot t + x_0$. 
	   (robotul are o accelerație constantă $a$, o viteză inițială $v_0$, și poziția inițială $x_0$).

    *Hint*: Dacă viteza e constantă, distanta parcursă este $x = v \cdot t$.
	
    \smallskip
    
3. Valorile măsurate ale unei funcții liniare $y = a \cdot x$, unde $a$ este necunoscut, sunt următoarele:
$(x_i, y_i) = {(1,1.8),(2,4.1),(2.5, 5.1),(4,7.9),(4.3, 8.5)}$. 
Presupunând că zgomotul are distribuția $\mathcal{N}(0,\sigma^2=1)$

    a. Estimați valoarea lui $a$ folosind estimarea ML

    \smallskip
    
4. Un semnal de forma $r(t) = A \cdot t^2 + 2 + zgomot$ este eșantionat la momentele  $t_i = [1,2,3,4,5]$,
 și valorile obținute sunt $r_i = [1.2, 3.7, 8.5, 18, 25.8]$. Distribuția zgomotului este 
 $\mathcal{N}(0,\sigma^2=1)$. 
 
    a. Estimați parametrul $A$ folosind estimarea ML
	b. Estimați parametrul $A$ folosind estimarea MAP și MMSE, considerând distribuția *a priori* $w(A) = \mathcal{N} (\mu = 1, \sigma^2 = 2)$

5. Un robot se deplasează pe o traiectorie liniară cu viteza $V = 10$ centimetri/secundă.
	La fiecare secundă, robotul își măsoară poziția folosind un senzor afectat de zgomot gaussian $\mathcal{N}(0,\sigma^2=0.5)$.

	La secunda $1$, poziția robotului este undeva în jurul valorii $x_{1} = 20$, fiind o variabilă aleatoare cu distribuția:
		
	  $$w(x_{1}) = \mathcal{N}(\mu = 20, \sigma = 0.5)$$
	
	a. Preziceți poziția la secunda $2$, $x_2$, și distribuția acestei poziții, $w(x_2)$.
	b. La secunda 2 se face o măsurătoare a poziției, și se obține valoarea $r = 19.5$. 
	   Folosiți estimarea Bayesiană pentru a estima poziția la acest moment, considerând ca distribuție *a priori* distribuția prezisă la punctul a). 
	
5. Dacă distribuția *a posteriori* a unui parametru $\Theta$ este $w(\Theta | r) = U[-3, 7]$, calculați estimatul MMSE și estimatul MAP.


**Notă**: 

- Se știe că produsul a două distribuții normale cu $\mu_1, \sigma^2_1$ și $\mu_2, \sigma^2_2$ 
este tot o fistribuție normală cu media $\mu = \frac{\mu_1 \sigma^2_2 + \mu_2 \sigma^2_1}{\sigma_1^2 + \sigma_2^2}$
și varianța $\sigma^2 = \frac{\sigma_1^2 \sigma_2^2}{\sigma_1^2 + \sigma_2^2}$