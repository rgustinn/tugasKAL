# Dekomposisi QR Matriks A dengan Metode Gram-Schmidt

Diberikan

$$
A=
\begin{bmatrix}
3&4&2&1\
1&5&3&2\
2&1&4&3\
1&2&1&5
\end{bmatrix}
=============

[a_1\ a_2\ a_3\ a_4]
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
\end{bmatrix},
\quad
a_4=
\begin{bmatrix}
1\2\3\5
\end{bmatrix}
$$

# Langkah 1

$$
q_1=\frac{a_1}{|a_1|}
$$

$$
|a_1|
=====

# \sqrt{3^2+1^2+2^2+1^2}

\sqrt{15}
$$

$$
q_1=
\frac1{\sqrt{15}}
\begin{bmatrix}
3\1\2\1
\end{bmatrix}
$$

# Langkah 2

$$
v_2=a_2-(a_2\cdot q_1)q_1
$$

$$
a_2\cdot q_1
============

\frac{21}{\sqrt{15}}
$$

$$
v_2=
\begin{bmatrix}
4\5\1\2
\end{bmatrix}
-------------

\frac{21}{15}
\begin{bmatrix}
3\1\2\1
\end{bmatrix}
=============

\frac15
\begin{bmatrix}
-1\18\-9\3
\end{bmatrix}
$$

$$
|v_2|
=====

\frac{\sqrt{415}}5
$$

$$
q_2=
\frac1{\sqrt{415}}
\begin{bmatrix}
-1\18\-9\3
\end{bmatrix}
$$

# Langkah 3

$$
v_3
===

a_3
-(a_3\cdot q_1)q_1
-(a_3\cdot q_2)q_2
$$

$$
a_3\cdot q_1
============

\frac{18}{\sqrt{15}}
$$

$$
a_3\cdot q_2
============

\frac{19}{\sqrt{415}}
$$

$$
v_3=
\frac1{83}
\begin{bmatrix}
-129\
81\
167\
-28
\end{bmatrix}
$$

$$
|v_3|
=====

\frac{25}{\sqrt{83}}
$$

$$
q_3=
\begin{bmatrix}
-\frac{129}{25\sqrt{83}}\
\frac{81}{25\sqrt{83}}\
\frac{167}{25\sqrt{83}}\
-\frac{28}{25\sqrt{83}}
\end{bmatrix}
$$

# Langkah 4

$$
v_4
===

a_4
-(a_4\cdot q_1)q_1
-(a_4\cdot q_2)q_2
-(a_4\cdot q_3)q_3
$$

$$
a_4\cdot q_1
============

\frac{16}{\sqrt{15}}
$$

$$
a_4\cdot q_2
============

\frac{23}{\sqrt{415}}
$$

$$
a_4\cdot q_3
============

\frac{394}{25\sqrt{83}}
$$

$$
v_4=
\frac1{1875}
\begin{bmatrix}
-2184\
-1274\
182\
7462
\end{bmatrix}
$$

$$
|v_4|
=====

\frac{182\sqrt3}{75}
$$

$$
q_4=
\begin{bmatrix}
-\frac{4}{25\sqrt3}\
-\frac{7}{75\sqrt3}\
\frac{1}{75\sqrt3}\
\frac{41}{75\sqrt3}
\end{bmatrix}
$$

# Matriks Q

$$
Q=
\begin{bmatrix}
\frac3{\sqrt{15}} &
-\frac1{\sqrt{415}} &
-\frac{129}{25\sqrt{83}} &
-\frac4{25\sqrt3}
[6pt]
\frac1{\sqrt{15}} &
\frac{18}{\sqrt{415}} &
\frac{81}{25\sqrt{83}} &
-\frac7{75\sqrt3}
[6pt]
\frac2{\sqrt{15}} &
-\frac9{\sqrt{415}} &
\frac{167}{25\sqrt{83}} &
\frac1{75\sqrt3}
[6pt]
\frac1{\sqrt{15}} &
\frac3{\sqrt{415}} &
-\frac{28}{25\sqrt{83}} &
\frac{41}{75\sqrt3}
\end{bmatrix}
$$

# Matriks R

$$
R=
\begin{bmatrix}
\sqrt{15} &
\frac{21}{\sqrt{15}} &
\frac{18}{\sqrt{15}} &
\frac{16}{\sqrt{15}}
[6pt]
0 &
\frac{\sqrt{415}}5 &
\frac{19}{\sqrt{415}} &
\frac{23}{\sqrt{415}}
[6pt]
0 &
0 &
\frac{25}{\sqrt{83}} &
\frac{394}{25\sqrt{83}}
[6pt]
0 &
0 &
0 &
\frac{182\sqrt3}{75}
\end{bmatrix}
$$

# Hasil Akhir

$$
\boxed{A=QR}
$$
