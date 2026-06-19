# Tugas Determinan, Dekomposisi, Invers

## A. Determinan Matriks 3×3
$$\det(A) = \sum_{k=1}^{3} (-1)^{1+k} a_{1k} M_{1k}$$

$$\det(A) = a_{11}(a_{22}a_{33} - a_{23}a_{32}) - a_{12}(a_{21}a_{33} - a_{23}a_{31}) + a_{13}(a_{21}a_{32} - a_{22}a_{31})$$

### Soal 1
$$A=
\begin{bmatrix}
2 & 1 & 3 \\
0 & 4 & 5 \\
1 & 2 & 1
\end{bmatrix}$$

**Pembahasan:**
$\det(A) = 2(4 \cdot 1 - 5 \cdot 2) - 1(0 \cdot 1 - 5 \cdot 1) + 3(0 \cdot 2 - 4 \cdot 1)$
$\det(A) = 2(4 - 10) - 1(0 - 5) + 3(0 - 4)$
$\det(A) = 2(-6) - 1(-5) + 3(-4)$
$\det(A) = -12 + 5 - 12 = \mathbf{-19}$

---

#### Soal 2

$$B = \begin{bmatrix} 3 & 2 & 1 \\ 1 & 0 & 4 \\ 2 & 5 & 1 \end{bmatrix}$$

**Pembahasan:**
$\det(B) = 3(0 \cdot 1 - 4 \cdot 5) - 2(1 \cdot 1 - 4 \cdot 2) + 1(1 \cdot 5 - 0 \cdot 2)$
$\det(B) = 3(0 - 20) - 2(1 - 8) + 1(5 - 0)$
$\det(B) = 3(-20) - 2(-7) + 1(5)$
$\det(B) = -60 + 14 + 5 = \mathbf{-41}$

### Soal 3
$$C = \begin{bmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 1 & 1 & 1 \end{bmatrix}$$

**Pembahasan:**
$\det(C) = 1(4 \cdot 1 - 6 \cdot 1) - 2(2 \cdot 1 - 6 \cdot 1) + 3(2 \cdot 1 - 4 \cdot 1)$
$\det(C) = 1(4 - 6) - 2(2 - 6) + 3(2 - 4)$
$\det(C) = 1(-2) - 2(-4) + 3(-2)$
$\det(C) = -2 + 8 - 6 = \mathbf{0}$