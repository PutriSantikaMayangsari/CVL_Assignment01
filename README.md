    Image Enhancement Documentation

1. Digital mammography Image 
Mammography biasanya punya latar belakang gelap dengan detail objek (tumor, kalsifikasi, atau jaringan abnormal) putih/abu-abu.
Dengan negative transform, detail yang tadinya samar di area terang bisa jadi lebih jelas.
Cocok untuk meningkatkan kontras struktur halus yang kadang sulit terlihat dokter radiologi.
Rumus negative image:
S = (L-1) -r

2. Salt and Pepper Image
Median filter efektif menghilangkan noise impulsif (salt & pepper) karena mengganti nilai piksel dengan nilai median dari jendela tetangganya,
sehingga lebih mampu menghilangkan noise tanpa merusak tepi (edges).

3. 
