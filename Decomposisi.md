# Dekomposisi QR Matriks A dengan Metode Gram-Schmidt

Diberikan matriks:
$$A = \begin{bmatrix} 3 & 4 & 2 \\ 1 & 5 & 3 \\ 2 & 1 & 4 \\ 1 & 2 & 1 \end{bmatrix} = [a_1 \ a_2 \ a_3]$$

## Langkah 1: Menentukan $q_1$
Norma vektor $a_1$:
$$|a_1| = \sqrt{3^2+1^2+2^2+1^2} = \sqrt{15}$$

Vektor ortonormal $q_1$:
$$q_1 = \frac{a_1}{|a_1|} = \frac{1}{\sqrt{15}} \begin{bmatrix} 3 \\ 1 \\ 2 \\ 1 \end{bmatrix}$$
Elemen matriks $R$: $r_{11} = a_1 \cdot q_1 = \sqrt{15}$

## Langkah 2: Menentukan $q_2$
Proyeksi $a_2$ terhadap $q_1$:
$$r_{12} = a_2 \cdot q_1 = \frac{21}{\sqrt{15}}$$

Vektor residu $v_2$:
$$v_2 = a_2 - r_{12}q_1 = \frac{1}{5} \begin{bmatrix} -1 \\ 18 \\ -9 \\ 3 \end{bmatrix}, \quad |v_2| = \frac{\sqrt{415}}{5}$$

Vektor ortonormal $q_2$:
$$q_2 = \frac{v_2}{|v_2|} = \frac{1}{\sqrt{415}} \begin{bmatrix} -1 \\ 18 \\ -9 \\ 3 \end{bmatrix}, \quad r_{22} = a_2 \cdot q_2 = \frac{\sqrt{415}}{5}$$

## Langkah 3: Menentukan $q_3$
Hitung proyeksi:
$$r_{13} = a_3 \cdot q_1 = \frac{18}{\sqrt{15}}, \quad r_{23} = a_3 \cdot q_2 = \frac{19}{\sqrt{415}}$$

Vektor residu $v_3$:
$$v_3 = a_3 - r_{13}q_1 - r_{23}q_2 = \frac{1}{125} \begin{bmatrix} -129 \\ 81 \\ 167 \\ -28 \end{bmatrix}, \quad |v_3| = \frac{25}{\sqrt{83}}$$

Vektor ortonormal $q_3$:
$$q_3 = \frac{v_3}{|v_3|} = \frac{1}{25\sqrt{83}} \begin{bmatrix} -129 \\ 81 \\ 167 \\ -28 \end{bmatrix}$$

## Hasil Akhir $A = QR$

$$Q = \begin{bmatrix} 
\frac{3}{\sqrt{15}} & -\frac{1}{\sqrt{415}} & -\frac{129}{25\sqrt{83}} \\ 
\frac{1}{\sqrt{15}} & \frac{18}{\sqrt{415}} & \frac{81}{25\sqrt{83}} \\ 
\frac{2}{\sqrt{15}} & -\frac{9}{\sqrt{415}} & \frac{167}{25\sqrt{83}} \\ 
\frac{1}{\sqrt{15}} & \frac{3}{\sqrt{415}} & -\frac{28}{25\sqrt{83}} 
\end{bmatrix}$$

$$R = \begin{bmatrix} 
\sqrt{15} & \frac{21}{\sqrt{15}} & \frac{18}{\sqrt{15}} \\ 
0 & \frac{\sqrt{415}}{5} & \frac{19}{\sqrt{415}} \\ 
0 & 0 & \frac{25}{\sqrt{83}} 
\end{bmatrix}$$