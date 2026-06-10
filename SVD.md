# Singular Value Decomposition (SVD)



## Definisi Matematis

Dekomposisi nilai singular dari matriks riil $A$ berukuran $m \times n$ adalah faktorisasi berbentuk:



$$A = U \Sigma V^T$$



dengan:

* **$U$** adalah matriks **ortogonal** berukuran $m \times m$ (yaitu, kolom dan barisnya adalah vektor ortonormal). Kolom-kolom $U$ disebut **vektor singular kiri** dari $A$.

* **$\Sigma$** adalah matriks diagonal persegi panjang berukuran $m \times n$ dengan bilangan riil non-negatif pada diagonalnya. Entri diagonal $\sigma_i = \Sigma_{ii}$ dikenal sebagai **nilai singular** dari $A$ dan biasanya disusun dalam urutan menurun, yaitu $\sigma_1 \geq \sigma_2 \geq \dots \geq \sigma_n \geq 0$. Jumlah nilai singular yang tidak nol sama dengan rank dari $A$.

* **$V$** adalah matriks ortogonal berukuran $n \times n$. Kolom-kolom $V$ disebut **vektor singular kanan** dari $A$.



---



## Algoritma SVD

Berikut adalah langkah-langkah algoritma SVD:



### Langkah 1: Menghitung Vektor Singular Kiri

* Hitung matriks $AA^T$ (berukuran $m \times m$).

* Cari **nilai-nilai eigen** dari $AA^T$.

* **Rank(A)** = $k$ = banyaknya nilai eigen yang **tidak nol**.

* Nilai eigen ini akan digunakan untuk mendapatkan vektor-vektor kiri.



### Langkah 2: Membentuk Matriks $U$

* Tentukan **vektor eigen** $\mathbf{u}_1, \mathbf{u}_2, \dots, \mathbf{u}_m$ yang berkorespondensi dengan nilai eigen dari $AA^T$.

* **Normalisasi** setiap vektor eigen:

  $$\mathbf{u}_i = \frac{\mathbf{u}_i}{\|\mathbf{u}_i\|}$$

  *(dibagi dengan panjang/norm vektor).*

* Susun vektor-vektor ini sebagai kolom matriks $U$ (berukuran $m \times m$).



### Langkah 3: Menghitung Vektor Singular Kanan dan Nilai Singular

* Hitung matriks $A^TA$ (berukuran $n \times n$).

* Cari **nilai-nilai eigen** dari $A^TA$.

* **Nilai singular** $\sigma_i$ adalah akar dari nilai eigen:

  $$\sigma_i = \sqrt{\lambda_i}$$

  di mana $\lambda_i$ adalah nilai eigen dari $A^TA$.



### Langkah 4: Membentuk Matriks $V$

* Tentukan **vektor eigen** $\mathbf{v}_1, \mathbf{v}_2, \dots, \mathbf{v}_n$ dari $A^TA$.

* **Normalisasi** setiap vektor eigen.

* Susun sebagai kolom matriks $V$ (berukuran $n \times n$).

* Transpose menjadi $V^T$.



### Langkah 5: Membentuk Matriks $\Sigma$ (Sigma)

* Buat matriks $\Sigma$ berukuran $m \times n$.

* Elemen diagonal berisi **nilai singular** $\sigma_1, \sigma_2, \dots, \sigma_k$.

* Urutkan dari besar ke kecil: $\sigma_1 \geq \sigma_2 \geq \dots \geq \sigma_k > 0$.

* Elemen di luar diagonal $= 0$.



### Langkah 6: Hasil Dekomposisi

* Matriks $A$ dapat direkonstruksi sebagai:

  $$A = U \Sigma V^T$$



**Catatan Penting:**

1. Nilai eigen $AA^T$ dan $A^TA$ adalah sama.

2. Nilai singular selalu **non-negatif** dan **real**.

3. $U$ dan $V$ adalah matriks ortogonal: $U^TU = I$ dan $V^TV = I$.



---



## Contoh Perhitungan SVD

Diberikan matriks $A$ berukuran $2 \times 3$:



$$A = \begin{bmatrix} 3 & 1 & 1 \\ -1 & 3 & 1 \end{bmatrix}$$



Carilah SVD dari matriks di atas.



### 1. Menghitung $AA^T$ (untuk vektor singular kiri)

$$AA^T = \begin{bmatrix} 3 & 1 & 1 \\ -1 & 3 & 1 \end{bmatrix} \begin{bmatrix} 3 & -1 \\ 1 & 3 \\ 1 & 1 \end{bmatrix} = \begin{bmatrix} 11 & 1 \\ 1 & 11 \end{bmatrix}$$



### 2. Mencari Nilai Eigen dari $AA^T$

Persamaan karakteristik:

$$\det(AA^T - \lambda I) = 0$$

$$\det \begin{bmatrix} 11-\lambda & 1 \\ 1 & 11-\lambda \end{bmatrix} = 0$$

$$(11-\lambda)^2 - 1 = 0$$

$$\lambda^2 - 22\lambda + 120 = 0$$

$$(\lambda - 12)(\lambda - 10) = 0$$



Nilai eigen: $\lambda_1 = 12$ dan $\lambda_2 = 10$.  

**Rank(A) = 2** karena ada 2 nilai eigen tidak nol.



### 3. Menentukan Matriks $U$ (vektor eigen dari $AA^T$)

Untuk mencari vektor eigen, selesaikan $(\lambda I - AA^T)\mathbf{x} = 0$.



* **Untuk $\lambda_1 = 12$:**

  $$\begin{bmatrix} 1 & -1 \\ -1 & 1 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \end{bmatrix} \implies x_1 = x_2 \implies \mathbf{u}_1 = \begin{bmatrix} 1 \\ 1 \end{bmatrix}$$

  Normalisasi: $\|\mathbf{u}_1\| = \sqrt{2} \implies \hat{\mathbf{u}}_1 = \begin{bmatrix} 1/\sqrt{2} \\ 1/\sqrt{2} \end{bmatrix}$



* **Untuk $\lambda_2 = 10$:**

  $$\begin{bmatrix} -1 & -1 \\ -1 & -1 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \end{bmatrix} \implies x_1 = -x_2 \implies \mathbf{u}_2 = \begin{bmatrix} 1 \\ -1 \end{bmatrix}$$

  Normalisasi: $\|\mathbf{u}_2\| = \sqrt{2} \implies \hat{\mathbf{u}}_2 = \begin{bmatrix} 1/\sqrt{2} \\ -1/\sqrt{2} \end{bmatrix}$



* **Matriks $U$:**

  $$U = \begin{bmatrix} 1/\sqrt{2} & 1/\sqrt{2} \\ 1/\sqrt{2} & -1/\sqrt{2} \end{bmatrix}$$



### 4. Singular Kanan ($A^TA$)

$$A^TA = \begin{bmatrix} 3 & -1 \\ 1 & 3 \\ 1 & 1 \end{bmatrix} \begin{bmatrix} 3 & 1 & 1 \\ -1 & 3 & 1 \end{bmatrix} = \begin{bmatrix} 10 & 0 & 2 \\ 0 & 10 & 4 \\ 2 & 4 & 2 \end{bmatrix}$$



* **Nilai Eigen dari $A^TA$**: $\lambda_1 = 12, \lambda_2 = 10, \lambda_3 = 0$.

* **Nilai Singular**:

  $$\sigma_1 = \sqrt{12} = 2\sqrt{3} \approx 3.464$$

  $$\sigma_2 = \sqrt{10} \approx 3.162$$



#### Vektor-Vektor Eigen $\mathbf{v}_1, \mathbf{v}_2, \mathbf{v}_3$:

* **a. Untuk $\lambda_1 = 12$**:

  $$\begin{bmatrix} -2 & 0 & 2 \\ 0 & -2 & 4 \\ 2 & 4 & -10 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix} \implies \mathbf{v}_1 = \begin{bmatrix} 1 \\ 2 \\ 1 \end{bmatrix}$$

* **b. Untuk $\lambda_2 = 10$**:

  $$\begin{bmatrix} 0 & 0 & 2 \\ 0 & 0 & 4 \\ 2 & 4 & -8 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix} \implies \mathbf{v}_2 = \begin{bmatrix} 2 \\ -1 \\ 0 \end{bmatrix}$$

* **c. Untuk $\lambda_3 = 0$**:

  $$\begin{bmatrix} 10 & 0 & 2 \\ 0 & 10 & 4 \\ 2 & 4 & 2 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix} \implies \mathbf{v}_3 = \begin{bmatrix} 1 \\ 2 \\ -5 \end{bmatrix}$$

### 5. Normalisasi dan Pembentukan Matriks $V$

$$
\hat{\mathbf{v}}_1=
\frac{1}{\sqrt6}
\begin{bmatrix}
1\\
2\\
1
\end{bmatrix},
\qquad
\hat{\mathbf{v}}_2=
\frac{1}{\sqrt5}
\begin{bmatrix}
2\\
-1\\
0
\end{bmatrix},
\qquad
\hat{\mathbf{v}}_3=
\frac{1}{\sqrt{30}}
\begin{bmatrix}
1\\
2\\
-5
\end{bmatrix}
$$

Matriks $V$ diperoleh dengan menyusun vektor-vektor eigen ternormalisasi sebagai kolom:

$$
V=
\begin{bmatrix}
\dfrac{1}{\sqrt6} & \dfrac{2}{\sqrt5} & \dfrac{1}{\sqrt{30}}\\
\dfrac{2}{\sqrt6} & -\dfrac{1}{\sqrt5} & \dfrac{2}{\sqrt{30}}\\
\dfrac{1}{\sqrt6} & 0 & -\dfrac{5}{\sqrt{30}}
\end{bmatrix}
$$

Sehingga:

$$
V^T=
\begin{bmatrix}
\dfrac{1}{\sqrt6} & \dfrac{2}{\sqrt6} & \dfrac{1}{\sqrt6}\\
\dfrac{2}{\sqrt5} & -\dfrac{1}{\sqrt5} & 0\\
\dfrac{1}{\sqrt{30}} & \dfrac{2}{\sqrt{30}} & -\dfrac{5}{\sqrt{30}}
\end{bmatrix}
$$

### 6. Membentuk Matriks $\Sigma$

Karena ukuran matriks $A$ adalah $2 \times 3$, maka:

$$
\Sigma=
\begin{bmatrix}
2\sqrt3 & 0 & 0\\
0 & \sqrt{10} & 0
\end{bmatrix}
$$

Nilai singular:

$$
\sigma_1=\sqrt{12}=2\sqrt3 \approx 3.464
$$

$$
\sigma_2=\sqrt{10}\approx 3.162
$$

### 7. Hasil Akhir SVD

$$
A=U\Sigma V^T
$$

dengan

$$
U=
\begin{bmatrix}
\dfrac{1}{\sqrt2} & \dfrac{1}{\sqrt2}\\
\dfrac{1}{\sqrt2} & -\dfrac{1}{\sqrt2}
\end{bmatrix}
$$

$$
\Sigma=
\begin{bmatrix}
2\sqrt3 & 0 & 0\\
0 & \sqrt{10} & 0
\end{bmatrix}
$$

$$
V^T=
\begin{bmatrix}
\dfrac{1}{\sqrt6} & \dfrac{2}{\sqrt6} & \dfrac{1}{\sqrt6}\\
\dfrac{2}{\sqrt5} & -\dfrac{1}{\sqrt5} & 0\\
\dfrac{1}{\sqrt{30}} & \dfrac{2}{\sqrt{30}} & -\dfrac{5}{\sqrt{30}}
\end{bmatrix}
$$

Sehingga:

$$
\begin{bmatrix}
3 & 1 & 1\\
-1 & 3 & 1
\end{bmatrix}
=
\begin{bmatrix}
\dfrac{1}{\sqrt2} & \dfrac{1}{\sqrt2}\\
\dfrac{1}{\sqrt2} & -\dfrac{1}{\sqrt2}
\end{bmatrix}
\begin{bmatrix}
2\sqrt3 & 0 & 0\\
0 & \sqrt{10} & 0
\end{bmatrix}
\begin{bmatrix}
\dfrac{1}{\sqrt6} & \dfrac{2}{\sqrt6} & \dfrac{1}{\sqrt6}\\
\dfrac{2}{\sqrt5} & -\dfrac{1}{\sqrt5} & 0\\
\dfrac{1}{\sqrt{30}} & \dfrac{2}{\sqrt{30}} & -\dfrac{5}{\sqrt{30}}
\end{bmatrix}
$$

<script src="https://sagecell.sagemath.org/static/embedded_sagecell.js"></script>
<script>
sagecell.makeSagecell({inputLocation: '.sage'});
</script>

<div class="sage">

import numpy as np

A = np.array([[3, 1, 1], [-1, 3, 1]])

U, S_vektor, VT = np.linalg.svd(A)

S_matriks = np.zeros((2, 3))
S_matriks[:2, :2] = np.diag(S_vektor)

hasil = U @ S_matriks @ VT

print("Matriks U")
print(U)

print("\nMatriks S")
print(S_matriks)

print("\nMatriks VT")
print(VT)

print("\nMatriks Awal")
print(A)

print("\nHasil Rekonstruksi (U @ S @ VT)")
print(hasil)

</div>
