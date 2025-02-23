<div align="center">

# TUGAS SISTEM OPERASI

## **SISTEM BILANGAN**

![Pens Logo](https://belajargiat.id/wp-content/uploads/2020/10/logo-PENS.png)

**Dosen Pengampu:**

Dr. Ferry Astika Saputra, S.T., M.Sc.

**Disusun Oleh:**

Pius Purba (3124521015)

## **PROGRAM STUDI D3 TEKNIK INFORMATIKA PSDKU LAMONGAN**  
DEPARTEMEN TEKNIK INFORMATIKA DAN KOMPUTER  
POLITEKNIK ELEKTRONIKA NEGERI SURABAYA  
2025

</div>

## 1. Basis Bilangan


## 1. Basis Bilangan
  ```
  1. bilangan yang dipakai biner adalah bilangan yang berbasis 2
  ```

## 2. Konversi Bilangan Desimal ke Biner

| Bilangan | Pembagi | Sisa |
|----------|---------|------|
| 1234     | 2       | 0    |
| 617      | 2       | 1    |
| 308      | 2       | 0    |
| 154      | 2       | 0    |
| 77       | 2       | 1    |
| 38       | 2       | 0    |
| 19       | 2       | 1    |
| 9        | 2       | 1    |
| 4        | 2       | 0    |
| 2        | 2       | 0    |
| 1        | 2       | 1    |
| 0        | 2       |      |

dengan hasil 10011010010

## 3. Konversi Bilangan Biner ke Desimal
  |Perhitungan: |
  |:-----------:|
  |1 × 2^7 = 128|
  |0 × 2^6 = 0|
  |1 × 2^5 = 32|
  |0 × 2^4 = 0|
  |1 × 2^3 = 8|
  |0 × 2^2 = 0|
  |1 × 2^1 = 2|
  |0 × 2^0 = 0|
  |Total = 170|
  ```
  Hasil: 170
  ```

## 4. Konversi Bilangan Biner ke Oktal
  |Konversi: |
  |:-----:|
  |101 = 5|
  |011 = 3|  
  |111 = 7|  
  |001 = 1|
  ```
  Hasil: 5371
  ```

## 5. Konversi Bilangan Oktal ke Biner
  |Konversi:|
  |:-----:|
  |2 = 010|
  |1 = 001|  
  |7 = 111|  
  |0 = 000|  
  ```
  Hasil: 2170 = 010001111000
  ```

## 6. Konversi Bilangan Desimal ke Heksadesimal
  |Langkah-langkah:         |
  |:-----------------------:|
  | 1780 ÷ 16 = 111 sisa 4  |
  | 111 ÷ 16 = 6 sisa 15 (F)| 
  | ÷ 16 = 0 sisa 6  |
  ```
  Hasil: 178010 = 06F4
  ```

## 7. Konversi Bilangan Heksadesimal ke Desimal
  |Langkah-langkah:         |
  |:-----------------------:|
  |A × 16^3 + B × 16^2 + C × 16^1 + D × 16^0 |
  |= 10 × 4096 + 11 × 256 + 12 × 16 + 13 × 1 |
  |= 40960 + 2816 + 192 + 13 |
  |= 43981|
  ```
  Hasil: ABCD16 = 43981 
  ```

## 8. Konversi Bilangan Pecahan Desimal ke Biner
  | Angka – 1 dari belakang koma | Kalikan 2 | Hasil | Binernya dibaca dari bawah |
|------------------------------|-----------|-------|----------------------------|
| 0,3125                       | X2        | 0,6250| 0                          |
| 0,625                        | X2        | 1,25  | 1                          |
| 0,25                         | X2        | 0,5   | 0                          |
| 0,5                          | X2        | 1     | 1                          |

  ```
  Hasil: 0,312510 = 0,0101
  ```

## 9. Konversi Bilangan Desimal ke Biner
## 11,62510

### Angka Didepan Koma
| Angka Didepan Koma | Dibagi 2 | Sisa |
|--------------------|----------|------|
| 11                 | :2       | 1    |
| 5                  | :2       | 1    |
| 2                  | :2       | 0    |
| 1                  | :2       | 1    |

### Angka Dibelakang Koma
| Angka Dibelakang Koma | Dikali 2 | Hasil |
|-----------------------|----------|-------|
| 0,625                 | X2       | 1,250 |
| 0,25                  | X2       | 0,5   |
| 0,5                   | X2       | 1     |

### Cara Pembacaan
1011,101

*NOTES:* 1. Untuk angka didepan koma, baca angkanya dari bawah. Jika belakang koma maka bacanya dari atas.

  ```
  Hasil: 11,625(10) = 1011,101(2)
  ```

## 10. Konversi Bilangan Desimal ke Heksadesimal
## 348.65410

### Angka Didepan Koma
| Angka Didepan Koma | Dibagi 16 | Hasil | Sisa |
|--------------------|-----------|-------|------|
| 348                | :16       | 21    | 12 = C |
| 21                 | :16       | 1     | 5    |
| 1                  | :16       | 0     | 1    |

### Angka Dibelakang Koma
| Angka Dibelakang Koma | Dikali 16 | Hasil |
|-----------------------|-----------|-------|
| 0,654                 | X16       | 10,464 = A |
| 0,464                 | X16       | 7,424 = 7 |
| 0,424                 | X16       | 6,784 = 6 |
| 0,784                 | X16       | 12,544 = C |

### Cara Pembacaan
15C,A76...

  ```
  Hasil: 348,654(10) = 15C,A76(16) 
  ```

## 11. Konversi Bilangan ke Desimal
  
  ```
  Hasil: 010100011,001111101(2) = 163,245(10)  
  ```

## 12. Konversi Bilangan Biner ke BCD
  |Langkah-langkah:         |
  |:-----------------------:|
  |Pisahkan menjadi digit desimal: , |
  |1010 (10) = 10|
  |0110 (6) = 6|
  |0001 (1) = 1|
  |0111 (7) = 7|
  ```
  Hasil: 10100110000111(2) = 2987(BCD)
  ```

## 13. Rubahlah bentuk BCD di bawah ini ke dalam bilangan biner
  |Langkah-langkah:         |
  |:-----------------------:|
  | 1 = 0001|
  | 9 = 1001|
  | 8 = 1000|
  | 7 = 0111|
  ```
  Hasil: 1987 = 0001100100000111(2)
  ```

## 14. Rubahlah bilangan biner di bawah ini ke dalam BCO.
  ### Konversi Kode

| Kode          | Nilai |
|---------------|-------|
| 011 111 101 001 | 3 7 5 1 |
| 011 111 101 001 | 5 6 2 4 |
| 101 110 010 100 | 1 4 0 2 |

  ```
  Hasil: 11111101001(2) = 3751(BCO) 
  ```

## 15. Rubahlah bilangan biner di bawah ini ke dalam BCH
 ### Konversi Kode ke Heksadesimal

| Kode Biner         | Nilai Desimal | Heksadesimal |
|--------------------|---------------|--------------|
| 1101 1111 0010 1110| 13 15 2 14    | CF2E         |
| 0110 1001 1000     | 6 9 8         | 698          |

  ```
  Hasil: 1101111100101110 (2) = CF2E(BCH)
  ```

## 16. Rubahlah Bentuk BCH di bawah ini ke dalam bilangan heksadesimal
 ### Konversi Kode ke Heksadesimal dan Biner

| Heksadesimal | Desimal | Biner  |
|--------------|---------|--------|
| F            | 15      | 1111   |
| 1            | 1       | 0001   |
| 8            | 8       | 1000   |
| 0            | 0       | 0000   |
| C            | 12      | 1100   |
| 3            | 3       | 0011   |
| D            | 13      | 1101   |
| A            | 10      | 1010   |
| 4            | 4       | 0100   |
| E            | 14      | 1110   |
| B            | 11      | 1011   |

  ```
  Hasil: F0DE = 1111000011011110(2) 
  ```

## 17. Nyatakan positip atau negatip bilangan biner di bawah ini
  | Biner Expression                            | Perhitungan |         
  |:-------------------------------------------:|:-----------:|
  | (0×2^7) + (1×2^6) + (1×2^5) + (1×2^4) + (1×2^3) + (1×2^2) + (1×2^1) + (1×2^0) | 0 + 64 + 32 + 16 + 8 + 4 + 2 + 1 |
  ```
  Hasil: 01111111 → Positip 127
  ```

## 18. Nyatakan bilangan biner negatip di bawah ini ke dalam bilangan decimal
 
Karena semuanya berawalan 1, nilainya semua adalah negative lalu
10001000 
11110111 
10000101 
10011100 

### Konversi Kode ke Heksadesimal dan Biner

| Heksadesimal | Desimal | Biner    |
|--------------|---------|----------|
| F            | 15      | 1111     |
| 1            | 1       | 0001     |
| 8            | 8       | 1000     |
| 0            | 0       | 0000     |
| C            | 12      | 1100     |
| 3            | 3       | 0011     |
| D            | 13      | 1101     |
| A            | 10      | 1010     |
| 4            | 4       | 0100     |
| E            | 14      | 1110     |
| B            | 11      | 1011     |

  ```
  Hasil: 10001000 → -120
  ```

## 19. Nyatakan ASCII Code di bawah ini dalam bentuk karakter

41 = 4×16^1+1×16^0=64+1 = 65 yang sama dengan A


## 20. Nyatakan Karakter di bawah ini dalam ASCII code
  | Karakter | Desimal | Langkah-langkah       | Heksadesimal |
  |:--------:|:-------:|:---------------------:|:------------:|
  | a        | 97      | 97 ÷ 16 = 6 sisa 1    | 61(16)        |
  ```
  Hasil: Hexadesimal = 61(16)
  ```

## 21. Dengan Keyboard standard ASCII, pada layar monitor nampak tulisan sebagai berikut:
  PRINT X
  |Karakter |Biner   |
  |:-------:|:------:|
  |P        |101 0000|
  |R        |101 0010|
  |I        |100 1001|
  |N        |100 1110|
  |T        |101 0100|
  |Space    |010 0000|
  |X        |101 1000|