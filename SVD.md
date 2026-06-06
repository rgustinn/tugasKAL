# Singular Value Decomposition (SVD)

## Definisi Matematis
Dekomposisi nilai singular dari matriks riil A berukuran m x m  adalah faktorisasi berbentuk:

$$A = U \Sigma V^T$$

Keterangan:
- U adalah matriks ortogonal berukuran m x m (yaitu, kolom dan barisnya adalah vektor ortonormal). Kolom-kolom U disebut vektor singular kiri dari A.
- $$\Sigma$$ adalah matriks diagonal persegi panjang berukuran m x n dengan bilangan riil non-negatif pada diagonalnya. Entri diagonal $$\sigma_i=\Sigma_{ii}$$ dikenal sebagai nilai singular dari A dan biasanya disusun dalam urutan menurun, yaitu $$\sigma_1\ge\sigma_2\ge\dots\ge\sigma_n\ge 0$$. Jumlah nilai singular yang tidak nol sama dengan rank dari A.
- V adalah matriks ortogonal berukuran n x n. Kolom-kolom V disebut vektor singular kanan dari A.

## Algoritma SVD 
Langkah algoritma SVD:

## Langkah 1 Menghitung Vektor Singular Kiri
