# Singular Value Decomposition (SVD)

## Definisi Matematis
Dekomposisi nilai singular dari matriks riil A berukuran m x m  adalah faktorisasi berbentuk:

$$A = U \Sigma V^T$$

### Ilustrasi Dimensi

$A_{m \times n} = U_{m \times m} \cdot \Sigma_{m \times n} \cdot V^T_{n \times n}$

Keterangan:
- $U$ adalah matriks ortogonal berukuran $m \times m$ (yaitu, kolom dan barisnya adalah vektor ortonormal). Kolom-kolom $U$ disebut vektor singular kiri dari $A$.
- $\Sigma$ adalah matriks diagonal persegi panjang berukuran $m \times n$ dengan bilangan riil non-negatif pada diagonalnya. Entri diagonal $\sigma_i=\Sigma_{ii}$ dikenal sebagai nilai singular dari $A$ dan biasanya disusun dalam urutan menurun, yaitu $\sigma_1 \ge \sigma_2 \ge \dots \ge \sigma_n \ge 0$. Jumlah nilai singular yang tidak nol sama dengan rank dari $A$.
- $V$ adalah matriks ortogonal berukuran $n \times n$. Kolom-kolom $V$ disebut vektor singular kanan dari $A$.

## Algoritma SVD 

### Matriks
$A = \begin{bmatrix} 3 & 1 & 1 \\ -1 & 3 & 1 \end{bmatrix}$

Langkah algoritma SVD:

## Langkah 1 Menghitung Vektor Singular Kiri
- Hitung matriks $AA^T$ (berukuran m x m)

$AA^T = \begin{bmatrix} 3 & 1 & 1 \\ -1 & 3 & 1 \end{bmatrix} \begin{bmatrix} 3 & -1 \\ 1 & 3 \\ 1 & 1 \end{bmatrix}$

