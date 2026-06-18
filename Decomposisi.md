# Dekomposisi QR Matriks
Diberikan

$$
A=
\begin{bmatrix}
3 & 4 & 2 \\
1 & 5 & 3 \\
2 & 1 & 4 \\
1 & 2 & 1
\end{bmatrix}
=
[a_1\ a_2\ a_3]
$$

dengan

$$
a_1=
\begin{bmatrix}
3\\
1\\
2\\
1
\end{bmatrix}
,\qquad
a_2=
\begin{bmatrix}
4\\
5\\
1\\
2
\end{bmatrix}
,\qquad
a_3=
\begin{bmatrix}
2\\
3\\
4\\
1
\end{bmatrix}
$$

## Langkah 1: Menentukan $q_1$

$$
q_1=\frac{a_1}{\|a_1\|}
$$

$$
\|a_1\|
=
\sqrt{3^2+1^2+2^2+1^2}
=
\sqrt{15}
$$

$$
q_1
=
\frac{1}{\sqrt{15}}
\begin{bmatrix}
3\\
1\\
2\\
1
\end{bmatrix}
$$

## Langkah 2: Menentukan $q_2$

$$
v_2=a_2-(a_2\cdot q_1)q_1
$$

$$
a_2\cdot q_1
=
\begin{bmatrix}
4&5&1&2
\end{bmatrix}
\frac{1}{\sqrt{15}}
\begin{bmatrix}
3\\
1\\
2\\
1
\end{bmatrix}
=
\frac{21}{\sqrt{15}}
$$

$$
v_2=
\begin{bmatrix}
4\\
5\\
1\\
2
\end{bmatrix}
-
\frac{21}{15}
\begin{bmatrix}
3\\
1\\
2\\
1
\end{bmatrix}
$$

$$
=
\begin{bmatrix}
-\frac15\\
\frac{18}{5}\\
-\frac95\\
\frac35
\end{bmatrix}
$$

$$
\|v_2\|
=
\frac{\sqrt{415}}5
$$

$$
q_2
=
\frac1{\sqrt{415}}
\begin{bmatrix}
-1\\
18\\
-9\\
3
\end{bmatrix}
$$

## Langkah 3: Menentukan $q_3$

$$
v_3
=
a_3
-
(a_3\cdot q_1)q_1
-
(a_3\cdot q_2)q_2
$$

$$
a_3\cdot q_1
=
\frac{18}{\sqrt{15}}
$$

$$
a_3\cdot q_2
=
\frac{19}{\sqrt{415}}
$$

$$
v_3
=
\begin{bmatrix}
2\\
3\\
4\\
1
\end{bmatrix}
-
\frac{18}{15}
\begin{bmatrix}
3\\
1\\
2\\
1
\end{bmatrix}
-
\frac{19}{415}
\begin{bmatrix}
-1\\
18\\
-9\\
3
\end{bmatrix}
$$

$$
=
\begin{bmatrix}
-\frac{645}{415}\\
\frac{399}{415}\\
\frac{735}{415}\\
-\frac{141}{415}
\end{bmatrix}
$$

$$
\|v_3\|
=
\frac{25}{\sqrt{83}}
$$

$$
q_3=
\begin{bmatrix}
-\frac{129}{25\sqrt{83}}\\
\frac{81}{25\sqrt{83}}\\
\frac{167}{25\sqrt{83}}\\
-\frac{28}{25\sqrt{83}}
\end{bmatrix}
$$

## Matriks Q

$$
Q=
\begin{bmatrix}
\frac3{\sqrt{15}} &
-\frac1{\sqrt{415}} &
-\frac{129}{25\sqrt{83}}
\\
\frac1{\sqrt{15}} &
\frac{18}{\sqrt{415}} &
\frac{81}{25\sqrt{83}}
\\
\frac2{\sqrt{15}} &
-\frac9{\sqrt{415}} &
\frac{167}{25\sqrt{83}}
\\
\frac1{\sqrt{15}} &
\frac3{\sqrt{415}} &
-\frac{28}{25\sqrt{83}}
\end{bmatrix}
$$

## Matriks R

$$
R=
\begin{bmatrix}
\sqrt{15} &
\frac{21}{\sqrt{15}} &
\frac{18}{\sqrt{15}}
\\
0 &
\frac{\sqrt{415}}5 &
\frac{19}{\sqrt{415}}
\\
0 &
0 &
\frac{25}{\sqrt{83}}
\end{bmatrix}
$$

## Hasil Akhir

$$
A=QR
$$