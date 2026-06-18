# Tugas Dekomposisi QR 

Diberikan matriks:

$$
A=
\begin{bmatrix}
3 & 4 & 2 & 1 \\
1 & 5 & 3 & 2 \\
2 & 1 & 4 & 3 \\
1 & 2 & 1 & 5
\end{bmatrix}
$$

Kolom-kolom matriks $(A)$$ adalah:

$$
a_1=
\begin{bmatrix}
3\\
1\\
2\\
1
\end{bmatrix},
\qquad
a_2=
\begin{bmatrix}
4\\
5\\
1\\
2
\end{bmatrix},
\qquad
a_3=
\begin{bmatrix}
2\\
3\\
4\\
1
\end{bmatrix},
\qquad
a_4=
\begin{bmatrix}
1\\
2\\
3\\
5
\end{bmatrix}
$$

---

## Langkah 1: Menentukan $(q_1)$

Gunakan rumus:
$
q_1=\frac{a_1}{\|a_1\|}
$

Hitung norma $\(a_1\)$:
$
\|a_1\| = \sqrt{3^2+1^2+2^2+1^2} = \sqrt{15}
$

Sehingga:
$
q_1 = \frac{1}{\sqrt{15}}
\begin{bmatrix}
3\\
1\\
2\\
1
\end{bmatrix}
$

---

## Langkah 2: Menentukan $(q_2)$

### Menghitung $(a_2 \cdot q_1)&
$
a_2 \cdot q_1 = \frac{1}{\sqrt{15}}(12+5+2+2) = \frac{21}{\sqrt{15}}
$

### Menghitung $(v_2)$
$
v_2 = a_2 - (a_2 \cdot q_1)q_1 = \begin{bmatrix} 4 \\ 5 \\ 1 \\ 2 \end{bmatrix} - \begin{bmatrix} 21/5 \\ 7/5 \\ 14/5 \\ 7/5 \end{bmatrix} = \begin{bmatrix} -1/5 \\ 18/5 \\ -9/5 \\ 3/5 \end{bmatrix}
$

### Norma $(v_2)$
$
\|v_2\| = \frac{\sqrt{415}}{5} \implies q_2 = \frac{1}{\sqrt{415}} \begin{bmatrix} -1 \\ 18 \\ -9 \\ 3 \end{bmatrix}
$

---

## Langkah 3: Menentukan $(q_3)$

$
v_3 = a_3 - (a_3 \cdot q_1)q_1 - (a_3 \cdot q_2)q_2 = \begin{bmatrix} -129/83 \\ 81/83 \\ 167/83 \\ -28/83 \end{bmatrix}
$

Norma $\(v_3\)$:
$
\|v_3\| = \frac{25}{\sqrt{83}} \implies q_3 = \frac{1}{25\sqrt{83}} \begin{bmatrix} -129 \\ 81 \\ 167 \\ -28 \end{bmatrix}
$

---

## Matriks (Q)$ dan (R)$

$
Q=
\begin{bmatrix}
\frac{3}{\sqrt{15}} & \frac{-1}{\sqrt{415}} & \frac{-129}{25\sqrt{83}} \\
\frac{1}{\sqrt{15}} & \frac{18}{\sqrt{415}} & \frac{81}{25\sqrt{83}} \\
\frac{2}{\sqrt{15}} & \frac{-9}{\sqrt{415}} & \frac{167}{25\sqrt{83}} \\
\frac{1}{\sqrt{15}} & \frac{3}{\sqrt{415}} & \frac{-28}{25\sqrt{83}}
\end{bmatrix}
$

$
R=
\begin{bmatrix}
\sqrt{15} & \frac{21}{\sqrt{15}} & \frac{18}{\sqrt{15}} \\
0 & \frac{\sqrt{415}}{5} & \frac{19}{\sqrt{415}} \\
0 & 0 & \frac{25}{\sqrt{83}}
\end{bmatrix}
$

---

## Kesimpulan
$
A = QR
$