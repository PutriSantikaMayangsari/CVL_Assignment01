    Image Enhancement Documentation

1. Digital mammography Image 
Mammography biasanya punya latar belakang gelap dengan detail objek (tumor, kalsifikasi, atau jaringan abnormal) putih/abu-abu.
Dengan negative transform, detail yang tadinya samar di area terang bisa jadi lebih jelas.
Cocok untuk meningkatkan kontras struktur halus yang kadang sulit terlihat dokter radiologi.
Rumus negative image:
S = (L-1) -r

2. Salt and Pepper Image
Median filter efektif menghilangkan noise impulsif (salt & pepper) karena mengganti 
nilai piksel dengan nilai median dari jendela tetangganya, sehingga lebih mampu 
menghilangkan noise tanpa merusak tepi (edges). Relatif sederhana dan cepat untuk 
ukuran kernel kecil (3×3). 

3. Low Light Image 
Untuk dataset log light image terdiri dari beberapa pendekatan, yaitu menggunakan 
log transform, histogram equalization, dan clahe, berikut penjelasannya. 
A. Log transform 
Prinsipnya menggunakan transformasi logaritmik untuk memperkuat nilai piksel 
rendah (area gelap) sehingga terlihat lebih terang. Cocok untuk citra dengan 
kontras rendah di area gelap, karena detail yang tadinya tersembunyi di bagian 
shadow bisa ditampilkan. Namun, bagian terang bisa jadi overexposed (terlalu 
terang) jika konstanta pengali tidak diatur dengan baik. 
B. Histogram Equalization 
Bekerja dengan cara meratakan distribusi intensitas piksel agar memanfaatkan 
seluruh rentang gray level. Sangat membantu pada citra low light karena 
meningkatkan kontras global secara otomatis. Kelemahannya, metode ini bisa 
membuat citra terlihat terlalu terang atau kehilangan detail lokal karena semua 
area diperlakukan sama. 
C. Clahe 
Merupakan pengembangan dari histogram equalization dengan bekerja secara 
lokal (per blok) dan membatasi kontras agar tidak berlebihan. Cocok untuk citra 
low light karena dapat meningkatkan kontras lokal tanpa membuat bagian terang 
terlalu overexposed. Biasanya menghasilkan citra yang lebih natural dan seimbang 
dibanding histogram equalization biasa.
