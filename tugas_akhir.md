# Tugas Determinan, Dekomposisi, Invers

## A. Determinan Matriks 3×3
$$\det(A) = \sum_{k=1}^{3} (-1)^{1+k} a_{1k} M_{1k}$$

$$\det(A) = a_{11}(a_{22}a_{33} - a_{23}a_{32}) - a_{12}(a_{21}a_{33} - a_{23}a_{31}) + a_{13}(a_{21}a_{32} - a_{22}a_{31})$$

$$\det(A) = a_{11} \det \begin{bmatrix} a_{22} & a_{23} \\ a_{32} & a_{33} \end{bmatrix} - a_{12} \det \begin{bmatrix} a_{21} & a_{23} \\ a_{31} & a_{33} \end{bmatrix} + a_{13} \det \begin{bmatrix} a_{21} & a_{22} \\ a_{31} & a_{32} \end{bmatrix}$$

#### Soal 1
$$A=
\begin{bmatrix}
2 & 1 & 3 \\
0 & 4 & 5 \\
1 & 2 & 1
\end{bmatrix}$$

**Pembahasan:**

$\det(A) = 2 \det \begin{bmatrix} 4 & 5 \\ 2 & 1 \end{bmatrix} - 1 \det \begin{bmatrix} 0 & 5 \\ 1 & 1 \end{bmatrix} + 3 \det \begin{bmatrix} 0 & 4 \\ 1 & 2 \end{bmatrix}$

$\det(A) = 2(4 - 10) - 1(0 - 5) + 3(0 - 4)$

$\det(A) = 2(-6) - 1(-5) + 3(-4)$

$\det(A) = -12 + 5 - 12 = \mathbf{-19}$

#### Soal 2

$$B = \begin{bmatrix} 3 & 2 & 1 \\ 1 & 0 & 4 \\ 2 & 5 & 1 \end{bmatrix}$$

**Pembahasan:**

$\det(B) = 3 \det \begin{bmatrix} 0 & 4 \\ 5 & 1 \end{bmatrix} - 2 \det \begin{bmatrix} 1 & 4 \\ 2 & 1 \end{bmatrix} + 1 \det \begin{bmatrix} 1 & 0 \\ 2 & 5 \end{bmatrix}$

$\det(B) = 3(0 - 20) - 2(1 - 8) + 1(5 - 0)$

$\det(B) = 3(-20) - 2(-7) + 1(5)$

$\det(B) = -60 + 14 + 5 = \mathbf{-41}$

#### Soal 3
$$C = \begin{bmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 1 & 1 & 1 \end{bmatrix}$$

**Pembahasan:**

$\det(C) = 1 \det \begin{bmatrix} 4 & 6 \\ 1 & 1 \end{bmatrix} - 2 \det \begin{bmatrix} 2 & 6 \\ 1 & 1 \end{bmatrix} + 3 \det \begin{bmatrix} 2 & 4 \\ 1 & 1 \end{bmatrix}$

$\det(C) = 1(4 - 6) - 2(2 - 6) + 3(2 - 4)$

$\det(C) = 1(-2) - 2(-4) + 3(-2)$

$\det(C) = -2 + 8 - 6 = \mathbf{0}$

## B. Dekomposisi Matriks (LU Decomposition)

# Tugas: Dekomposisi Matriks LU

$$A = LU$$.

**Rumus:**

$$l_{ij} = \frac{a_{ij}}{pivot}$$

$$\begin{split}
L=
\begin{bmatrix}
1 & 0 & 0\\
l_{21} & 1 & 0\\
l_{31} & l_{32} & 1
\end{bmatrix}
\end{split}$$

#### Soal 4

$$A = \begin{bmatrix} 2 & 4 & 2 \\ 1 & 5 & 2 \\ 1 & 2 & 4 \end{bmatrix}$$

**Eliminasi Baris 2 ($R_2$):**

$$l_{21} = \frac{1}{2} = 0.5$$

$$R_2 \leftarrow R_2 - 0.5R_1$$

$$[1, 5, 2] - 0.5[2, 4, 2] = [1 - 1, 5 - 2, 2 - 1] = [0, 3, 1]$$

**Eliminasi Baris 3 ($R_3$):**

$$l_{31} = \frac{1}{2} = 0.5$$

$$R_3 \leftarrow R_3 - 0.5R_1$$

$$[1, 2, 4] - 0.5[2, 4, 2] = [1 - 1, 2 - 2, 4 - 1] = [0, 0, 3]$$

**Hasil:** 

$$L = \begin{bmatrix} 1 & 0 & 0 \\ 0.5 & 1 & 0 \\ 0.5 & 0 & 1 \end{bmatrix}, \quad U = \begin{bmatrix} 2 & 4 & 2 \\ 0 & 3 & 1 \\ 0 & 0 & 3 \end{bmatrix}$$

---

#### Soal 5
$$B = \begin{bmatrix} 1 & 2 & 1 \\ 2 & 5 & 3 \\ 4 & 10 & 8 \end{bmatrix}$$

**Eliminasi Baris 2 ($R_2$):**

$$l_{21} = \frac{2}{1} = 2$$

$$R_2 \leftarrow R_2 - 2R_1$$

$$[2, 5, 3] - 2[1, 2, 1] = [2 - 2, 5 - 4, 3 - 2] = [0, 1, 1]$$

**Eliminasi Baris 3 ($R_3$):**

$$l_{31} = \frac{4}{1} = 4$$

$$R_3 \leftarrow R_3 - 4R_1$$

$$[4, 10, 8] - 4[1, 2, 1] = [4 - 4, 10 - 8, 8 - 4] = [0, 2, 4]$$

**Eliminasi Lanjutan Baris 3 ($R_3$):**

$$l_{32} = \frac{2}{1} = 2$$

$$R_3 \leftarrow R_3 - 2R_2$$

$$[0, 2, 4] - 2[0, 1, 1] = [0 - 0, 2 - 2, 4 - 2] = [0, 0, 2]$$

**Hasil:** 

$$L = \begin{bmatrix} 1 & 0 & 0 \\ 2 & 1 & 0 \\ 4 & 2 & 1 \end{bmatrix}, \quad U = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 1 & 1 \\ 0 & 0 & 2 \end{bmatrix}$$

#### Soal 6
$$C = \begin{bmatrix} 4 & 2 & 0 \\ 2 & 5 & 1 \\ 0 & 1 & 3 \end{bmatrix}$$

**Eliminasi Baris 2 ($R_2$):**

$$l_{21} = \frac{2}{4} = 0.5$$

$$R_2 \leftarrow R_2 - 0.5R_1$$

$$[2, 5, 1] - 0.5[4, 2, 0] = [2 - 2, 5 - 1, 1 - 0] = [0, 4, 1]$$

**Eliminasi Baris 3 ($R_3$):**

$$l_{31} = \frac{0}{4} = 0$$

**Eliminasi Lanjutan Baris 3 ($R_3$):**

$$l_{32} = \frac{1}{4} = 0.25$$

$$R_3 \leftarrow R_3 - 0.25R_2$$

$$[0, 1, 3] - 0.25[0, 4, 1] = [0 - 0, 1 - 1, 3 - 0.25] = [0, 0, 2.75]$$

**Hasil:** 

$$L = \begin{bmatrix} 1 & 0 & 0 \\ 0.5 & 1 & 0 \\ 0 & 0.25 & 1 \end{bmatrix}, \quad U = \begin{bmatrix} 4 & 2 & 0 \\ 0 & 4 & 1 \\ 0 & 0 & 2.75 \end{bmatrix}$$