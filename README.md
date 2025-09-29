Nama : Vivi Alydia
Nim : 312410224
Kelas : TI.24.A.2


<img width="970" height="552" alt="Screenshot 2025-09-29 150220" src="https://github.com/user-attachments/assets/1752f31b-0fe4-486a-9128-5d63ef836478" />







2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan
penjelasannya!


3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada
elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan
penjelasan dan contohnya!


4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut
terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser?
Berikan penjelasan dan contohnya! ( <p id="paragraf-1" class="text-paragraf"> )

# 📘 Ringkasan Materi CSS Dasar

## 1. Perbedaan `h1 {...}` dengan `#intro h1 {...}`
- **`h1 {...}`** → berlaku untuk **semua elemen `<h1>`** di halaman.
- **`#intro h1 {...}`** → hanya berlaku untuk `<h1>` yang berada di dalam elemen dengan `id="intro"`.

### Contoh:
```html
<h1>Judul Umum</h1>
<div id="intro">
  <h1>Judul di Intro</h1>
</div>
```

```css
h1 {
  color: blue;
}
#intro h1 {
  color: red;
}
```
👉 Hasil:  
- "Judul Umum" = biru  
- "Judul di Intro" = merah  

---

## 2. Urutan Prioritas CSS (Internal, Eksternal, Inline)
Urutan kekuatan CSS (dari terkuat → terlemah):
1. **Inline CSS** (`style=""`)
2. **Internal CSS** (`<style>...</style>`)
3. **Eksternal CSS** (file `.css` terpisah)

### Contoh:
```html
<head>
  <link rel="stylesheet" href="style.css"> <!-- eksternal -->
  <style>
    p { color: green; } <!-- internal -->
  </style>
</head>
<body>
  <p style="color: red;">Hello World</p> <!-- inline -->
</body>
```

- Eksternal: `color: blue;`
- Internal: `color: green;`
- Inline: `color: red;`

👉 Hasil di browser = **merah** (karena inline paling kuat).

---

## 3. ID vs Class (Siapa yang menang?)
- **ID (`#id`)** lebih kuat daripada **Class (`.class`)**.
- Jika elemen punya **ID dan Class** dengan aturan CSS yang berbeda, maka **ID akan menang**.

### Contoh:
```html
<p id="paragraf-1" class="text-paragraf">Halo Dunia!</p>
```

```css
.text-paragraf {
  color: blue;
}
#paragraf-1 {
  color: red;
}
```

👉 Hasil di browser = **merah**, karena selector **ID lebih spesifik** dibanding Class.

---

## 4. Tabel Urutan Prioritas CSS

| Selector / Jenis CSS | Kekuatan (Spesifisitas) |
|-----------------------|-------------------------|
| Inline CSS            | Paling kuat 🔥          |
| ID (`#id`)            | Sangat kuat             |
| Class (`.class`)      | Menengah                |
| Elemen (`h1`, `p`)    | Lemah                   |
| Eksternal vs Internal | Internal lebih kuat     |

---

✍️ **Catatan:**  
- Gunakan **ID** untuk elemen unik.  
- Gunakan **Class** untuk elemen yang berulang.  
- Sebaiknya hindari terlalu banyak **inline CSS**, karena sulit dirawat.  
