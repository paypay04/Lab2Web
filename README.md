Nama : Vivi Alydia
Nim : 312410224
Kelas : TI.24.A.2

1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS 
dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini. 
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
Jawab : Perbedaan antara h1 {...} dan #intro h1 {...} terletak pada jangkauan target dan prioritas penerapannya (spesifisitas).

  1. h1 {...} (Selektor Umum)
Deklarasi ini adalah selektor elemen dasar. Aturan gaya di dalamnya akan diterapkan ke semua elemen <h1> yang ada di seluruh halaman HTML Anda, tanpa peduli di mana elemen tersebut berada. Karena ini adalah selektor umum, ia memiliki prioritas rendah.

  2. #intro h1 {...} (Selektor Spesifik)
Ini adalah selektor turunan yang jauh lebih spesifik. Aturan gaya ini hanya akan diterapkan pada elemen <h1> yang merupakan keturunan (berada di dalam) dari elemen yang memiliki atribut id="intro". Karena mengandung Selektor ID (#intro), aturan ini memiliki prioritas sangat tinggi dan akan menimpa (meng-override) gaya dari h1 {...} jika keduanya diterapkan pada elemen yang sama.


3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada 
elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan 
penjelasan dan contohnya!
Jawab : Urutan prioritas sumber CSS dari yang terendah hingga yang tertinggi adalah:
     1.  CSS Eksternal
     2.  CSS Internal (di dalam tag <style>)
     3.  Inline CSS (di dalam atribut style elemen HTML)
Penjelasan Singkat
Inline CSS menang karena ia melekat langsung pada elemen HTML (menggunakan atribut style). Hal ini memberikannya spesifisitas tertinggi. Gaya ini dianggap paling spesifik dan paling relevan, sehingga akan menimpa (meng-override) semua deklarasi dari CSS Internal maupun Eksternal yang diterapkan pada properti yang sama.

Contoh
Jika Anda mendeklarasikan warna merah (Eksternal), hijau (Internal), dan biru (Inline) untuk sebuah paragraf, maka paragraf itu akan berwarna biru.

HTML

<p style="color: blue;">Paragraf ini akan berwarna biru.</p>

4. ada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut
terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser?
Berikan penjelasan dan contohnya! ( <p id="paragraf-1" class="text-paragraf"> )
jawab :Selektor ID (#myId): Memiliki bobot spesifisitas yang sangat tinggi (Bobot 0,1,0,0). Aturannya dianggap 10 kali lebih spesifik daripada Class dan Selektor Kelas (.myClass): Memiliki bobot sedang (Bobot 0,0,1,0).

Karena ID menang dalam perhitungan bobot spesifisitas, aturan CSS yang menggunakan ID akan selalu diterapkan jika terjadi konflik properti (misalnya, warna) pada elemen yang sama.

Contoh
Jika sebuah elemen memiliki ID yang mengatur warna menjadi biru dan Kelas yang mengatur warna menjadi merah, maka elemen itu akan berwarna biru.

CSS

/* Bobot 0,0,1,0 */
.merah { color: red; }

/* Bobot 0,1,0,0 (MENANG) */
#biru { color: blue; }
HTML

<p id="biru" class="merah">
    Teks ini akan berwarna biru.
</p>



