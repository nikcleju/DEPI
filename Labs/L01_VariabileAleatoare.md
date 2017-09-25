---
title: |
	   | Introducere în Matlab.
       | Variabile aleatoare
subtitle: Laborator 1, DEPI
documentclass: scrartcl
fontsize: 12pt
---

# Obiectiv

Familiarizarea studenților cu mediul de dezvoltare Matlab, și cu funcțiile 
de generare a unor variabile aleatoare.

# Noțiuni teoretice

Se vor urmări:

1. Introducere în Matlab
    
    1. Ferestre Matlab. Lucrul în linia de comandă și fișiere script
    
    2. Operații cu scalari
        - definirea unor variabile scalare
        - operații aritmetice cu scalari
        - operații logice (comparații etc)
        - funcții trigonometrice, constante trigonometrice (pi)
        - alte funcții (exponențiala, logaritm, etc)
    
    3. Operații cu tablouri (vectori / matrici)
        - definirea unor tablouri constante
        - definirea unor vectori cu expresia start:stop:pas
        - accesul la elemente, citirea / modificarea unor valori
        - operații aritmetice cu tablouri
        - operații element cu element
        - operații logice (comparații etc) cu tablouri
        - funcții aplicate tablourilor (trigonometrice, matematice, length/min/max/sum, etc)
        - concatenarea tablourilor
        - reprezentarea grafică a unui vector
        
2. Variabile aleatoare în Matlab
    1. Distribuția normală
        - generarea unui element sau vector cu elemente standard normale i.i.d., cu funcția `randn()`
        - generarea pentru o medie și dispersie precizate
        
    2. Distribuția uniformă
        - generarea unui element sau vector cu elemente uniforme i.i.d., cu funcția `rand()`
        - generarea pentru un interval precizat


# Exerciții

1. Definiți două variabile $a=5$ și $b=0.3$ și calculați $a+b$, $\frac{a}{b}$, $a^b$, $e^{a + ln(b)}$, $sin(a) + cos (b + \frac{\pi}{2})$

2. Definiți un vector $A$ cu 10 zerouri, o matrice $B$ cu $4 \times 6$ elemente egale cu 1, și un vector C cu numerele impare de la 1 la 21 inclusiv
    - Schimbați al treilea element din $A$ în valoarea 5
    - Schimbați elementul $B(2,4)$ în 7
    - Ridicați toate elementele din C la pătrat, și salvați-le într-un nou vector $D$.
    - Calculați $E = 4 * C - 50$.
    - Comparați, element cu element, vectorii $C$ și $E$. Câte elemente din $C$ sunt mai mari decât elementele de pe aceeași poziție din $E$?
    - Calculați $sin()$ pentru toate elementele din $D$
    
3. Definiți un vector $t$ cu 1000 elemente egal distribuite între 0 și 10. Calculați și reprezentați grafic expresia $cos(2 \pi f t)$, unde $f = 0.5$.

4. Generați un vector cu 1000 elemente cu distribuția normală $\mathcal{N}(2,2)$ și afișați-l grafic

5. Generați un vector cu 1000 elemente cu distribuția uniformă $\mathcal{U}[-4,10]$ și afișați-l grafic


# Întrebări finale

1. TBD
