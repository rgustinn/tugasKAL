# Dekomposisi QR Matriks 

Diberikan matriks $A$ dengan vektor kolom $a_1, a_2, a_3,$ dan $a_4$:

$$A = \begin{bmatrix} 3 & 4 & 2 & 1 \\ 1 & 5 & 3 & 2 \\ 2 & 1 & 4 & 3 \\ 1 & 2 & 1 & 5 \end{bmatrix} = [a_1 \ a_2 \ a_3 \ a_4]$$

dengan:

$$a_1 = \begin{bmatrix} 3 \\ 1 \\ 2 \\ 1 \end{bmatrix}, \quad a_2 = \begin{bmatrix} 4 \\ 5 \\ 1 \\ 2 \end{bmatrix}, \quad a_3 = \begin{bmatrix} 2 \\ 3 \\ 4 \\ 1 \end{bmatrix}, \quad a_4 = \begin{bmatrix} 1 \\ 2 \\ 3 \\ 5 \end{bmatrix}$$

## Langkah 1: Menentukan $q_1$

Vektor $q_1$ diperoleh dengan menormalisasi vektor $a_1$:

$$q_1 = \frac{a_1}{\|a_1\|}$$

Hitung norma dari $a_1$:

$$\|a_1\| = \sqrt{3^2 + 1^2 + 2^2 + 1^2} = \sqrt{15}$$

Sehingga:

$$q_1 = \frac{1}{\sqrt{15}} \begin{bmatrix} 3 \\ 1 \\ 2 \\ 1 \end{bmatrix}$$

## Langkah 2: Menentukan $q_2$

Gunakan rumus Gram-Schmidt:

$$v_2 = a_2 - (a_2 \cdot q_1)q_1$$

Hitung hasil kali titik:

$$a_2 \cdot q_1 = \begin{bmatrix} 4 & 5 & 1 & 2 \end{bmatrix} \frac{1}{\sqrt{15}} \begin{bmatrix} 3 \\ 1 \\ 2 \\ 1 \end{bmatrix} = \frac{21}{\sqrt{15}}$$

Substitusi ke rumus:

$$v_2 = \begin{bmatrix} 4 \\ 5 \\ 1 \\ 2 \end{bmatrix} - \frac{21}{15} \begin{bmatrix} 3 \\ 1 \\ 2 \\ 1 \end{bmatrix} = \begin{bmatrix} -0.2 \\ 3.6 \\ -1.8 \\ 0.6 \end{bmatrix} = \frac{1}{5} \begin{bmatrix} -1 \\ 18 \\ -9 \\ 3 \end{bmatrix}$$

Hitung norma $\|v_2\|$:

$$\|v_2\| = \frac{\sqrt{415}}{5}$$

Maka:

$$q_2 = \frac{v_2}{\|v_2\|} = \frac{1}{\sqrt{415}} \begin{bmatrix} -1 \\ 18 \\ -9 \\ 3 \end{bmatrix}$$

## Langkah 3: Menentukan $q_3$

Gunakan rumus Gram-Schmidt:

$$v_3 = a_3 - (a_3 \cdot q_1)q_1 - (a_3 \cdot q_2)q_2$$

Hitung hasil kali titik:

$$a_3 \cdot q_1 = \frac{18}{\sqrt{15}}, \quad a_3 \cdot q_2 = \frac{19}{\sqrt{415}}$$

Substitusi ke rumus:

$$v_3 = \begin{bmatrix} 2 \\ 3 \\ 4 \\ 1 \end{bmatrix} - \frac{18}{15} \begin{bmatrix} 3 \\ 1 \\ 2 \\ 1 \end{bmatrix} - \frac{19}{415} \begin{bmatrix} -1 \\ 18 \\ -9 \\ 3 \end{bmatrix} = \frac{1}{415} \begin{bmatrix} -235 \\ 167 \\ 345 \\ -58 \end{bmatrix}$$

Hitung norma $\|v_3\|$:

$$\|v_3\| = \frac{25}{\sqrt{83}}$$

Maka:

$$q_3 = \frac{v_3}{\|v_3\|} = \frac{1}{25\sqrt{83}} \begin{bmatrix} -129 \\ 81 \\ 167 \\ -28 \end{bmatrix}$$

## Langkah 4: Menentukan $q_4$

$$v_4 = a_4 - (a_4 \cdot q_1)q_1 - (a_4 \cdot q_2)q_2 - (a_4 \cdot q_3)q_3$$

Setelah perhitungan proyeksi:

$$q_4 = \frac{1}{\sqrt{83}} \begin{bmatrix} 7 \\ -2 \\ -1 \\ 3 \end{bmatrix}$$

---

### Membentuk Matriks $Q$
$$Q = [q_1 \ q_2 \ q_3 \ q_4]$$
$$Q = \begin{bmatrix}
\frac{3}{\sqrt{15}} & -\frac{1}{\sqrt{415}} & -\frac{129}{25\sqrt{83}} & \frac{7}{\sqrt{83}} \\
\frac{1}{\sqrt{15}} & \frac{18}{\sqrt{415}} & \frac{81}{25\sqrt{83}} & -\frac{2}{\sqrt{83}} \\
\frac{2}{\sqrt{15}} & -\frac{9}{\sqrt{415}} & \frac{167}{25\sqrt{83}} & -\frac{1}{\sqrt{83}} \\
\frac{1}{\sqrt{15}} & \frac{3}{\sqrt{415}} & -\frac{28}{25\sqrt{83}} & \frac{3}{\sqrt{83}}
\end{bmatrix}$$

### Membentuk Matriks $R$
$$R = \begin{bmatrix}
a_1\cdot q_1 & a_2\cdot q_1 & a_3\cdot q_1 & a_4\cdot q_1 \\
0 & a_2\cdot q_2 & a_3\cdot q_2 & a_4\cdot q_2 \\
0 & 0 & a_3\cdot q_3 & a_4\cdot q_3 \\
0 & 0 & 0 & a_4\cdot q_4
\end{bmatrix}$$
$$R = \begin{bmatrix}
\sqrt{15} & \frac{21}{\sqrt{15}} & \frac{18}{\sqrt{15}} & \frac{16}{\sqrt{15}} \\
0 & \frac{\sqrt{415}}{5} & \frac{19}{\sqrt{415}} & \frac{21}{\sqrt{415}} \\
0 & 0 & \frac{25}{\sqrt{83}} & \frac{50}{\sqrt{83}} \\
0 & 0 & 0 & \frac{4}{\sqrt{83}}
\end{bmatrix}$$

### Hasil Akhir
$$\boxed{A = QR}$$