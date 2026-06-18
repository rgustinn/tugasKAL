# Dekomposisi QR Matriks 

Diberikan matriks

$$
A=
\begin{bmatrix}
3 & 4 & 2\
1 & 5 & 3\
2 & 1 & 4\
1 & 2 & 1
\end{bmatrix}

[a_1\ a_2\ a_3]
$$

dengan

$$
a_1=
\begin{bmatrix}
3\1\2\1
\end{bmatrix},
\qquad
a_2=
\begin{bmatrix}
4\5\1\2
\end{bmatrix},
\qquad
a_3=
\begin{bmatrix}
2\3\4\1
\end{bmatrix}
$$

## Langkah 1: Menentukan $q_1$

Hitung norma vektor $a_1$

$$
|a_1|
=====

# \sqrt{3^2+1^2+2^2+1^2}

\sqrt{15}
$$

Sehingga

$$
q_1
===

# \frac{a_1}{|a_1|}

\frac{1}{\sqrt{15}}
\begin{bmatrix}
3\1\2\1
\end{bmatrix}
=============

\begin{bmatrix}
\frac{3}{\sqrt{15}}\
\frac{1}{\sqrt{15}}\
\frac{2}{\sqrt{15}}\
\frac{1}{\sqrt{15}}
\end{bmatrix}
$$

Elemen pertama matriks $R$

$$
r_{11}
======

# a_1\cdot q_1

\sqrt{15}
$$

## Langkah 2: Menentukan $q_2$

Hitung proyeksi $a_2$ terhadap $q_1$

$$
r_{12}
======

# a_2\cdot q_1

\frac{4(3)+5(1)+1(2)+2(1)}
{\sqrt{15}}
===========

\frac{21}{\sqrt{15}}
$$

Vektor residu

$$
v_2
===

a_2-r_{12}q_1
$$

# $$

\begin{bmatrix}
4\5\1\2
\end{bmatrix}
-\frac{21}{15}
\begin{bmatrix}
3\1\2\1
\end{bmatrix}
$$

# $$

\begin{bmatrix}
-\frac15\
\frac{18}{5}\
-\frac95\
\frac35
\end{bmatrix}
=============

\frac15
\begin{bmatrix}
-1\18\-9\3
\end{bmatrix}
$$

Normanya

$$
|v_2|
=====

\frac15
\sqrt{(-1)^2+18^2+(-9)^2+3^2}
=============================

\frac{\sqrt{415}}5
$$

Maka

$$
q_2
===

# \frac{v_2}{|v_2|}

\frac1{\sqrt{415}}
\begin{bmatrix}
-1\18\-9\3
\end{bmatrix}
$$

atau

$$
q_2=
\begin{bmatrix}
-\frac1{\sqrt{415}}\
\frac{18}{\sqrt{415}}\
-\frac9{\sqrt{415}}\
\frac3{\sqrt{415}}
\end{bmatrix}
$$

Elemen diagonal kedua matriks $R$

$$
r_{22}
======

# a_2\cdot q_2

\frac{\sqrt{415}}5
$$

## Langkah 3: Menentukan $q_3$

Hitung

$$
r_{13}
======

# a_3\cdot q_1

\frac{2(3)+3(1)+4(2)+1(1)}
{\sqrt{15}}
===========

\frac{18}{\sqrt{15}}
$$

dan

$$
r_{23}
======

# a_3\cdot q_2

\frac{-2+54-36+3}
{\sqrt{415}}
============

\frac{19}{\sqrt{415}}
$$

Bentuk vektor residu

$$
v_3
===

a_3-r_{13}q_1-r_{23}q_2
$$

Substitusi nilai-nilai di atas menghasilkan

$$
v_3=
\frac1{125}
\begin{bmatrix}
-129\
81\
167\
-28
\end{bmatrix}
$$

Normanya

$$
|v_3|
=====

\frac{25}{\sqrt{83}}
$$

Sehingga

$$
q_3
===

# \frac{v_3}{|v_3|}

\begin{bmatrix}
-\frac{129}{25\sqrt{83}}\
\frac{81}{25\sqrt{83}}\
\frac{167}{25\sqrt{83}}\
-\frac{28}{25\sqrt{83}}
\end{bmatrix}
$$

## Membentuk Matriks $Q$

Kolom-kolom matriks $Q$ adalah $q_1,q_2,q_3$

$$
Q=
\begin{bmatrix}
\frac{3}{\sqrt{15}} &
-\frac1{\sqrt{415}} &
-\frac{129}{25\sqrt{83}}
\
\frac1{\sqrt{15}} &
\frac{18}{\sqrt{415}} &
\frac{81}{25\sqrt{83}}
\
\frac2{\sqrt{15}} &
-\frac9{\sqrt{415}} &
\frac{167}{25\sqrt{83}}
\
\frac1{\sqrt{15}} &
\frac3{\sqrt{415}} &
-\frac{28}{25\sqrt{83}}
\end{bmatrix}
$$

## Membentuk Matriks $R$

Elemen-elemen $R$ diperoleh dari hasil proyeksi

$$
R=
\begin{bmatrix}
a_1\cdot q_1 & a_2\cdot q_1 & a_3\cdot q_1\
0 & a_2\cdot q_2 & a_3\cdot q_2\
0 & 0 & a_3\cdot q_3
\end{bmatrix}
$$

sehingga

$$
R=
\begin{bmatrix}
\sqrt{15} &
\dfrac{21}{\sqrt{15}} &
\dfrac{18}{\sqrt{15}}
\
0 &
\dfrac{\sqrt{415}}5 &
\dfrac{19}{\sqrt{415}}
\
0 &
0 &
\dfrac{25}{\sqrt{83}}
\end{bmatrix}
$$

## Hasil Akhir

$$
\boxed{A=QR}
$$

dengan

$$
Q=
\begin{bmatrix}
\frac{3}{\sqrt{15}} &
-\frac1{\sqrt{415}} &
-\frac{129}{25\sqrt{83}}
\
\frac1{\sqrt{15}} &
\frac{18}{\sqrt{415}} &
\frac{81}{25\sqrt{83}}
\
\frac2{\sqrt{15}} &
-\frac9{\sqrt{415}} &
\frac{167}{25\sqrt{83}}
\
\frac1{\sqrt{15}} &
\frac3{\sqrt{415}} &
-\frac{28}{25\sqrt{83}}
\end{bmatrix}
$$

dan

$$
R=
\begin{bmatrix}
\sqrt{15} &
\dfrac{21}{\sqrt{15}} &
\dfrac{18}{\sqrt{15}}
\
0 &
\dfrac{\sqrt{415}}5 &
\dfrac{19}{\sqrt{415}}
\
0 &
0 &
\dfrac{25}{\sqrt{83}}
\end{bmatrix}
$$
