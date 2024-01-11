---
title: |
       | Seminar 7
       | Estimare ML si Bayesiană, multiple eșantioane
subtitle: DEDP
documentclass: scrartcl
fontsize: 12pt
---


1. Un robot se deplasează pe o traiectorie liniară cu o viteză necunoscută $V$ centimetri/secundă,
pornind de la poziția $x = 0$ la momentul inițial. 
La intervale de o secundă, robotul măsoară distanța parcursă folosind un senzor, afectat de zgomot gaussian $\mathcal{N}(0,\sigma^2=0.1)$.
Valorile măsurate la momentele $t_i = [1,2,3,4,5]$ sunt $r_i = [4.9, 9.8, 14.3, 21.2, 25.7]$

   a. Estimați viteza $V$ a robotului folosind estimarea ML

      *Hint*: Dacă viteza e constantă, distanta parcursă ar trebui să fie $x = V \cdot t$ 

   c. Preziceți poziția robotului la momentul $6$.
   
   b. Dacă presupunem la momentul inițial poziția robotului nu este 0, ci o valoare necunoscută $x_0$, estimați perechea de parametri [V, $x_0$]
   folosind estimarea ML. Preziceți poziția robotului la momentul $6$.

   d. Știind că legea de mișcare este $x(t) = a \cdot t^2 + v_0 \cdot t + x_0$, scrieți sistemul de ecuații pentru găsirea necunoscutelor [a, $v_0$, $x_0$]. 
   (accelerația constantă $a$, viteza inițială $v_0$, poziția inițială$x_0$).

   \smallskip


2. Un robot se deplasează pe o traiectorie liniară cu o viteză constantă $V = 10$ cm/s.
	
	La intervale de o secundă, robotul măsoară distanța parcursă folosind un senzor, afectat de zgomot gaussian $\mathcal{N}(0,\sigma^2=0.5)$.

	La momentul $t_0 = 0$, poziția robotului este în jurul valorii $x_{0} = 20$, fiind a variabilă aleatoare cu distribuția:
		
	  $$w(x_{0}) = \mathcal{N}(\mu = 20, \sigma = 0.5)$$
	
	a. Find the distribution $w(x_1)$ of the robot's position at time $t_1 = 1$.
	b. Suppose at this time $t_1 = 1$ we have a new measurement of the position, with value $r = 29.5$. 
	
		Take this into account with Bayesian estimation and find the new position using MAP and MMSE estimators, considering the predicted distribution in a) as the prior distribution. 	
		
	c. What happens if the speed is not known precisely. Suppose $V$ is a random variable $\mathcal{N}(\mu = 10 \textrm{ cm/s}, \sigma^2 = 0.3)$?
	

3. Repetați exercițiul 1 în următoarele condiții:

   a. Considerând zgomotul de tip uniform $U[-2, 2]$. Se mai poate găsi o valoare precisă? Care este intervalul valorilor posibile?
   b. Considerând ca zgomotul are distribuție de forma următoare:
    
      $w(x) = \begin{cases}
      1.5 - \frac{x}{3}, &x \in [0,3 ]\\
      0, &elsewhere\\
      \end{cases}$

   c. Considerând ca zgomotul are distribuție de tip exponențial ($\lambda$ este doar o constantă)
    
      $w(x) = \begin{cases}
      \lambda \cdot e^{-\lambda \cdot x}, &x \geq 0\\
      0, &x < 0\\
      \end{cases}$
       
      Notă: Distribuția impune ca zgomotul să fie mereu pozitiv, adică valoarea originală e întotdeauna mai mică decât valoarea observată, afectată de zgomot

    \smallskip
