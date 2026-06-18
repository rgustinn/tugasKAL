# Dekomposisi QR Matriks A dengan Metode Gram-Schmidt

Diberikan

$$
A=
\begin{bmatrix}
3&4&2\
1&5&3\
2&1&4\
1&2&1
\end{bmatrix}
=============

[a_1\ a_2\ a_3]
$$

dengan

$$
a_1=
\begin{bmatrix}
3\1\2\1
\end{bmatrix},
\quad
a_2=
\begin{bmatrix}
4\5\1\2
\end{bmatrix},
\quad
a_3=
\begin{bmatrix}
2\3\4\1
\end{bmatrix}
$$

---

# Langkah 1 : Menentukan $q_1$

$$
q_1=\frac{a_1}{|a_1|}
$$

Hitung norma:

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

\frac1{\sqrt{15}}
\begin{bmatrix}
3\1\2\1
\end{bmatrix}
$$

---

# Langkah 2 : Menentukan $q_2$

Gunakan

$$
v_2=a_2-(a_2\cdot q_1)q_1
$$

Hitung hasil kali titik:

$$
a_2\cdot q_1
============

\begin{bmatrix}
4&5&1&2
\end{bmatrix}
\frac1{\sqrt{15}}
\begin{bmatrix}
3\1\2\1
\end{bmatrix}
$$

# $$

\frac{12+5+2+2}{\sqrt{15}}
$$

# $$

\frac{21}{\sqrt{15}}
$$

Substitusi ke rumus:

$$
v_2
===

\begin{bmatrix}
4\5\1\2
\end{bmatrix}
-------------

\frac{21}{\sqrt{15}}
\left(
\frac1{\sqrt{15}}
\begin{bmatrix}
3\1\2\1
\end{bmatrix}
\right)
$$

# $$

\begin{bmatrix}
4\5\1\2
\end{bmatrix}
-------------

\frac{21}{15}
\begin{bmatrix}
3\1\2\1
\end{bmatrix}
$$

# $$

\begin{bmatrix}
4\5\1\2
\end{bmatrix}
-------------

\begin{bmatrix}
\frac{21}{5}\
\frac75\
\frac{14}{5}\
\frac75
\end{bmatrix}
$$

# $$

\begin{bmatrix}
-\frac15\
\frac{18}{5}\
-\frac95\
\frac35
\end{bmatrix}
$$

Hitung normanya:

$$
|v_2|
=====

\sqrt{
\left(-\frac15\right)^2
+
\left(\frac{18}{5}\right)^2
+
\left(-\frac95\right)^2
+
\left(\frac35\right)^2
}
$$

# $$

\sqrt{
\frac1{25}
+
\frac{324}{25}
+
\frac{81}{25}
+
\frac9{25}
}
$$

# $$

\sqrt{\frac{415}{25}}
$$

# $$

\frac{\sqrt{415}}5
$$

Normalisasi:

$$
q_2
===

\frac{v_2}{|v_2|}
$$

# $$

\frac{
\begin{bmatrix}
-\frac15\
\frac{18}{5}\
-\frac95\
\frac35
\end{bmatrix}
}
{\frac{\sqrt{415}}5}
$$

# $$

\frac1{\sqrt{415}}
\begin{bmatrix}
-1\18\-9\3
\end{bmatrix}
$$

---

# Langkah 3 : Menentukan $q_3$

Gunakan

$$
v_3
===

## a_3

## (a_3\cdot q_1)q_1

(a_3\cdot q_2)q_2
$$

Hitung

$$
a_3\cdot q_1
============

\begin{bmatrix}
2&3&4&1
\end{bmatrix}
\frac1{\sqrt{15}}
\begin{bmatrix}
3\1\2\1
\end{bmatrix}
$$

# $$

\frac{6+3+8+1}{\sqrt{15}}
$$

# $$

\frac{18}{\sqrt{15}}
$$

Hitung

$$
a_3\cdot q_2
============

\begin{bmatrix}
2&3&4&1
\end{bmatrix}
\frac1{\sqrt{415}}
\begin{bmatrix}
-1\18\-9\3
\end{bmatrix}
$$

# $$

\frac{-2+54-36+3}{\sqrt{415}}
$$

# $$

\frac{19}{\sqrt{415}}
$$

Substitusi ke rumus:

$$
v_3
===

\begin{bmatrix}
2\3\4\1
\end{bmatrix}
-------------

\frac{18}{\sqrt{15}}
\left(
\frac1{\sqrt{15}}
\begin{bmatrix}
3\1\2\1
\end{bmatrix}
\right)
-------

\frac{19}{\sqrt{415}}
\left(
\frac1{\sqrt{415}}
\begin{bmatrix}
-1\18\-9\3
\end{bmatrix}
\right)
$$

# $$

\begin{bmatrix}
2\3\4\1
\end{bmatrix}
-------------

\frac{18}{15}
\begin{bmatrix}
3\1\2\1
\end{bmatrix}
-------------

\frac{19}{415}
\begin{bmatrix}
-1\18\-9\3
\end{bmatrix}
$$

# $$

\begin{bmatrix}
2\3\4\1
\end{bmatrix}
-------------

\begin{bmatrix}
\frac{18}{5}\
\frac65\
\frac{12}{5}\
\frac65
\end{bmatrix}
-------------

\begin{bmatrix}
-\frac{19}{415}\
\frac{342}{415}\
-\frac{171}{415}\
\frac{57}{415}
\end{bmatrix}
$$

# $$

\begin{bmatrix}
-\frac{645}{415}\
\frac{399}{415}\
\frac{735}{415}\
-\frac{141}{415}
\end{bmatrix}
$$

Norma:

$$
|v_3|
=====

\frac{25}{\sqrt{83}}
$$

Normalisasi:

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

---

# Membentuk Matriks $Q$

$$
Q=[q_1\ q_2\ q_3]
$$

$$
Q=
\begin{bmatrix}
\frac3{\sqrt{15}} &
-\frac1{\sqrt{415}} &
-\frac{129}{25\sqrt{83}}
[6pt]
\frac1{\sqrt{15}} &
\frac{18}{\sqrt{415}} &
\frac{81}{25\sqrt{83}}
[6pt]
\frac2{\sqrt{15}} &
-\frac9{\sqrt{415}} &
\frac{167}{25\sqrt{83}}
[6pt]
\frac1{\sqrt{15}} &
\frac3{\sqrt{415}} &
-\frac{28}{25\sqrt{83}}
\end{bmatrix}
$$

---

# Membentuk Matriks $R$

$$
R=
\begin{bmatrix}
a_1\cdot q_1 & a_2\cdot q_1 & a_3\cdot q_1\
0 & a_2\cdot q_2 & a_3\cdot q_2\
0 & 0 & a_3\cdot q_3
\end{bmatrix}
$$

$$
R=
\begin{bmatrix}
\sqrt{15} &
\frac{21}{\sqrt{15}} &
\frac{18}{\sqrt{15}}
[6pt]
0 &
\frac{\sqrt{415}}5 &
\frac{19}{\sqrt{415}}
[6pt]
0 &
0 &
\frac{25}{\sqrt{83}}
\end{bmatrix}
$$

---

# Hasil Akhir

$$
\boxed{A=QR}
$$

dengan

$$
Q=
\begin{bmatrix}
\frac3{\sqrt{15}} &
-\frac1{\sqrt{415}} &
-\frac{129}{25\sqrt{83}}
[6pt]
\frac1{\sqrt{15}} &
\frac{18}{\sqrt{415}} &
\frac{81}{25\sqrt{83}}
[6pt]
\frac2{\sqrt{15}} &
-\frac9{\sqrt{415}} &
\frac{167}{25\sqrt{83}}
[6pt]
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
\frac{21}{\sqrt{15}} &
\frac{18}{\sqrt{15}}
[6pt]
0 &
\frac{\sqrt{415}}5 &
\frac{19}{\sqrt{415}}
[6pt]
0 &
0 &
\frac{25}{\sqrt{83}}
\end{bmatrix}
$$
