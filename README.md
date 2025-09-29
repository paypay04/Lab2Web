Nama : Vivi Alydia
Nim : 312410224
Kelas : TI.24.A.2

Membuat dokumen HTML

<img width="970" height="552" alt="Screenshot 2025-09-29 150220" src="https://github.com/user-attachments/assets/1752f31b-0fe4-486a-9128-5d63ef836478" />

Mendeklarasikan CSS Internal

<img width="1920" height="1080" alt="Screenshot (718)" src="https://github.com/user-attachments/assets/5c91f411-18ab-4f40-aea8-4be1afea1616" />

Menambahkan Inline CSS

<img width="1920" height="1080" alt="Screenshot (719)" src="https://github.com/user-attachments/assets/29cad382-e4da-4084-bb8f-0843aabf84cc" />

Membuat CSS Eksternal

<img width="1920" height="1080" alt="Screenshot (720)" src="https://github.com/user-attachments/assets/e54044e7-c70a-454c-b118-9f5fb8727160" />

Menambahkan CSS Selector

<img width="1920" height="1080" alt="Screenshot (722)" src="https://github.com/user-attachments/assets/f26c2933-f49b-4411-b692-260cec6a261d" />











2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan
penjelasannya!


3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada
elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan
penjelasan dan contohnya!


4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut
terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser?
Berikan penjelasan dan contohnya! ( <p id="paragraf-1" class="text-paragraf"> )

# 📘 Ringkasan Materi CSS Dasar



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
