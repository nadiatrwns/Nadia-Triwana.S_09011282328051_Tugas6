## 1. Eksekusi seluruh profile yang ada :  
## a.	Edit file profile /etc/profile dan tampilkan pesan sebagai berikut : 
## echo “Profile dari /etc/profile”  
![1](https://github.com/user-attachments/assets/9ddd6fd0-81e2-4d8a-b253-b9d3b60a7206)
![2](https://github.com/user-attachments/assets/175293a5-f368-41a3-bd38-97d5a9db3050)
![3](https://github.com/user-attachments/assets/2d76c56b-3c80-4782-851a-a4e7b28640c8)
# /etc/profile adalah file konfigurasi global yang dijalankan untuk semua pengguna saat login. Dengan menambahkan perintah echo, pesan akan ditampilkan setiap kali pengguna masuk ke sesi login, memberikan feedback bahwa file ini telah dijalankan.

## b.	Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu :  
## /home/stD02001/.bash_profile  
## /home/. stD02001/.bash_login  
## /home/mahasiswa/.profile  /home/mahasiswa/.bashrc  
## Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap  file tersebut, cantumkan instruksi echo, misalnya pada /home/ mahasiswa/.bash_profile :  
## echo “Profile dari .bash_profile”  
## Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang bersangkutan.  
![4](https://github.com/user-attachments/assets/f3b8fc9c-d10d-4a23-9eed-c9337409f1b2)
![5](https://github.com/user-attachments/assets/ba54c434-03dd-4f3f-866f-2011f028d236)
![6](https://github.com/user-attachments/assets/9f593884-2c40-4513-932c-79ca8a6a9a24)
![7](https://github.com/user-attachments/assets/7455db8b-a49c-4db2-a408-2757314a66b5)
![8](https://github.com/user-attachments/assets/533845dc-ba81-4d1c-812b-b2c367c36cdf)
![9](https://github.com/user-attachments/assets/16e1520b-3c3f-4e22-b0e5-07d808f26707)
![10](https://github.com/user-attachments/assets/5a543fd5-2c38-47ec-bb7a-83e1ab6c1013)
![11](https://github.com/user-attachments/assets/51ddf5be-3b3f-4662-a13c-406694562934)
![12](https://github.com/user-attachments/assets/8cffacb2-ef97-4418-84f4-fb6114c41d14)
![13](https://github.com/user-attachments/assets/35ec66d6-6e98-4461-8539-50194ed15acc)
![14](https://github.com/user-attachments/assets/74f34c6d-f77a-41b6-9e8f-56c4f2c8bc50)
![15](https://github.com/user-attachments/assets/8f6dc2aa-d12f-44d8-a376-8caabacc8e2a)
# Setiap pengguna memiliki file profile sendiri, seperti .bash_profile, .bash_login, .profile, dan .bashrc. File ini digunakan untuk mengatur variabel lingkungan, alias, dan pengaturan sesi login khusus untuk pengguna tersebut. Menambahkan echo ke setiap file akan menampilkan pesan konfirmasi bahwa masing-masing file tersebut dijalankan saat sesi dimulai.

## c.	Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut:  
## $ su mahasiswa  
## $ exit  
## kemudian gunakan opsi – sebagai berikut :  
## $ su – mahasiswa  
## $ exit  
## Jelaskan perbedaan kedua utilitas tersebut. 
![16](https://github.com/user-attachments/assets/843b5f04-ebfb-435f-9ed6-86f22c76f48f)
# •	su [user]: Mengganti pengguna tanpa menjalankan file profile pengguna tersebut. Ini artinya Anda mengganti user tapi tetap berada dalam lingkungan shell pengguna sebelumnya.
# •	su - [user]: Mengganti pengguna dan memulai lingkungan shell baru dari pengguna tersebut, menjalankan semua file profile yang sesuai (seperti .bash_profile), sehingga environment benar-benar sesuai dengan pengguna baru tersebut.

## 2. Prompt String (PS)  
# PS1 adalah variabel lingkungan yang menentukan bagaimana prompt shell ditampilkan. Prompt adalah teks yang muncul di terminal sebelum Anda memasukkan perintah.

## a.	Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell  
## PS1=‟> „  export PS1  
![18](https://github.com/user-attachments/assets/8c678910-e463-4dd3-8a9d-6034523ae174)
# Mengubah prompt default menjadi > sehingga hanya tanda > yang muncul di awal baris perintah.

## b.	Eksperimen hasil PS1 :  
## $ PS1=“\! > “  
## 69 > PS1=”\d > “  
## Mon Sep 23 > PS1=”\t > “  
## 10:10:20 > PS1=”Saya=\u > “  
## Saya=mahasiswa > PS1=”\w >”  ~ > PS1=\h >”  
![17](https://github.com/user-attachments/assets/bb89cdb7-eb93-4cd4-8646-d9db265384cc)
# •	\! menampilkan nomor history command.
# •	\d menampilkan tanggal saat ini.
# •	\t menampilkan waktu (jam, menit, detik).
# •	\u menampilkan nama pengguna (user).
# •	\w menampilkan direktori kerja saat ini.
# •	\h menampilkan hostname.

## 3.	Logout  
## Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout  
## Echo “Terima kasih atas sesi yang diberikan”  Sleep 5  clear  
![19](https://github.com/user-attachments/assets/aa54f313-224a-4cc7-be38-fa067a41f959)
# File .bash_logout dieksekusi ketika pengguna keluar dari sesi shell. Dalam kasus ini, perintah echo menampilkan pesan, sleep 5 menunggu 5 detik, dan clear membersihkan layar terminal sebelum logout. Ini berguna untuk memberikan pesan akhir dan memastikan tampilan bersih sebelum keluar.

## 4.	Bash script  
## a.	Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing :  
## p1.sh
## #! /bin/bash  
## echo “Program p1”  
## ls –l  
## p2.sh  
## #! /bin/bash  
## echo “Program p2”  
## who  p3.sh  
## #! /bin/bash  
## echo “Program p3”  
## ps x  
![20](https://github.com/user-attachments/assets/574077fb-328e-4770-8f2f-cf80dbbedfb1)
![21](https://github.com/user-attachments/assets/957cd8b1-a52a-4cad-a6e3-85a19c35f7df)
![22](https://github.com/user-attachments/assets/14c821cb-145b-426d-a2ab-c3a1a73e84b1)
![23](https://github.com/user-attachments/assets/9a4deb3c-93e5-4b44-a6c7-703f6fbe065f)
![24](https://github.com/user-attachments/assets/05bdf845-271f-4182-88de-9666c2592b85)
![25](https://github.com/user-attachments/assets/34d6852a-1261-4f02-b912-eec2be3372b1)
![26](https://github.com/user-attachments/assets/e5b9ebab-ec98-453c-b30e-f6269885de5f)
# •	p1.sh: Menampilkan pesan “Program p1” dan menampilkan daftar file di direktori saat ini dengan format panjang.
# •	p2.sh: Menampilkan pesan “Program p2” dan menunjukkan siapa yang sedang login ke sistem.
# •	p3.sh: Menampilkan pesan “Program p3” dan menampilkan proses yang sedang berjalan.

## b.	Jalankan script tersebut sebagai berikut :  
## $  ./p1.sh ; ./p3.sh ; ./p2.sh  
## $  ./p1.sh &  
## $  ./p1.sh $ ./p2.sh & ./p3.sh &  
## $  ( ./p1.sh ; ./p3.sh ) &  
![27](https://github.com/user-attachments/assets/852e7d48-382f-446f-8c2e-a7016f192567)
# •	./p1.sh ; ./p3.sh ; ./p2.sh: Menjalankan ketiga script satu per satu secara berurutan.
![28](https://github.com/user-attachments/assets/b23443b7-1ed7-4ccd-b751-419d702e662d)
# •	./p1.sh &: Menjalankan p1.sh di background, memungkinkan Anda menjalankan perintah lain di foreground.
![29](https://github.com/user-attachments/assets/e3972d66-fb6d-4f3c-b64e-d1f4abc838e0)
# •	./p1.sh $ ./p2.sh & ./p3.sh &: Menjalankan p1.sh di foreground, lalu p2.sh dan p3.sh secara bersamaan di background.
![30](https://github.com/user-attachments/assets/ce60b933-6b86-48eb-bed3-6121651a35d5)
# •	( ./p1.sh ; ./p3.sh ) &: Menjalankan p1.sh dan p3.sh di dalam subshell dan menjalankannya di background.

## 5.	Jobs  
# Mengelola proses yang berjalan di background (background jobs).

## a.	Buat shell-script yang melakukan loop dengan nama pwaktu.sh,  setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil.  #!/bin/bash  while [ true ]  do   date >> hasil   sleep 10  done  
![31](https://github.com/user-attachments/assets/9ec1063b-75be-44ef-a9f6-f59e61ef3950)
![32](https://github.com/user-attachments/assets/a39a631f-5460-4d4b-8e5b-8a472c432e26)
# Script ini menjalankan loop yang setiap 10 detik menyimpan waktu saat ini ke dalam file hasil. Ini dapat digunakan untuk memonitor waktu secara berkala di background.

## b.	Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background sebagai berikut :  
## $ jobs  
## $ find / -print > files 2>/dev/null &  
## $ jobs  
![33](https://github.com/user-attachments/assets/257bac95-3498-4961-827b-8e37471f72c3)
# •	jobs: Menampilkan daftar proses yang sedang berjalan di background.
# •	find / -print > files 2>/dev/null &: Mencari semua file di sistem dan menyimpan hasilnya ke file files. Perintah dijalankan di background.

## c.	Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke background  
## $ fg %1  
## $ bg  
![34](https://github.com/user-attachments/assets/72aab7f2-fe10-4541-aeaa-7cf3c1b7f571)
# •	fg %1: Membawa job dengan nomor 1 ke foreground.
# •	bg %1: Melanjutkan eksekusi job nomor 1 di background setelah dihentikan sementara dengan Ctrl+Z.

## d.	Stop program background dengan utilitas kil  
## $ ps x  
## $ kill [Nomor PID]  
![35](https://github.com/user-attachments/assets/a6a4fc9e-f05c-4c87-a20b-41c882c075b3)
![36](https://github.com/user-attachments/assets/9831ac01-2a3c-4d73-ab97-10cab7b12174)
# •	ps x: Menampilkan daftar proses yang sedang berjalan.
# •	kill [PID]: Menghentikan proses berdasarkan nomor PID (Process ID).

## 6.	History  
## a.	Ganti nilai HISTSIZE dari 1000 menjadi 20  
## $ HISTSIZE=20  
## $ h  
![37](https://github.com/user-attachments/assets/0f2126c8-9124-4b6a-9f52-a55e6622ffa8)
# HISTSIZE mengontrol jumlah perintah yang disimpan dalam buffer history. Mengatur nilai ke 20 berarti hanya 20 perintah terakhir yang akan disimpan.

## b.	Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir dilakukan  
## $ !-5  
![38](https://github.com/user-attachments/assets/b60241ff-2b93-4bf3-8042-ffffb77d9812)
# !-5: Menjalankan ulang perintah yang dilakukan 5 perintah sebelumnya.

## c.	Ulangi instruksi yang terakhir.  Gunakan juga ^P dan ^N untuk bernavigasi pada history bufer  
## $ !!  
![39](https://github.com/user-attachments/assets/c62e1eef-37b1-437d-bcd4-5fdce36ba934)
# •	!!: Menjalankan ulang perintah terakhir.
# •	^P: Menavigasi ke perintah sebelumnya dalam buffer history.
# •	^N: Menavigasi ke perintah berikutnya dalam buffer history.

## d.	Ulangi instruksi pada history bufer nomor 150  
## $ !150  
![40](https://github.com/user-attachments/assets/654ec4bb-6f3a-4dea-b622-6f880991680c)
# !150: Menjalankan perintah nomor 150 dari buffer history.

## e.	Ulangi instruksi dengan prefix “ls”  
## $ !ls  
![41](https://github.com/user-attachments/assets/84ff3019-4fb4-4138-a737-7b16fa991dbb)
# !ls: Menjalankan perintah terakhir yang dimulai dengan ls.
