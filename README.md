# KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau
# Cara Menginstall Apache2, Wordpress, Nginx, Tableau menggunakan Ubuntu Server
# Daftar Isi
- [Cara Menginstall Apache2 dan Cara Remote](#cara-menginstall-apache2-dan-cara-remote)
- [Cara Menginstall Wordpress](#cara-menginstall-wordpress)
- [Cara Menginstall Nginx](#cara-instalasi-nginx)
- [Cara Menginstall Tableau Desktop Dari Windows](#cara-menginstal-tableau-dekstop-dari-windows)
# Cara Menginstall Apache2 dan cara remote
## Instalasi Apache2
1. perbarui daftar paket
   ```
   sudo apt update
2. Langkah selanjutnya dalam menyiapkan tumpukan LAMP adalah menginstal dan mengkonfigurasi Apache2, server web. Jalankan perintah di bawah ini untuk menginstal Apache 2 di Ubuntu
   ```
   sudo apt install apache2
3. Apache2 harus diizinkan untuk memulai pada waktu boot sistem dan memulai layanan untuk memverifikasi statusnya juga.
   ```
   sudo systemctl aktifkan apache2
   sudo systemctl status apache2
  ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/00258aff-e922-4979-8875-20bcc5fb6e4b)

4. Buka browser web, dan ketik localhost di kotak alamat untuk memverifikasi bahwa  server Apache  telah dimulai.
Jika server web Apache2 berjalan, maka akan menampilkan halaman indeks default Apache2.
  ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/c03c9ef3-0fdd-4761-9021-7fe7b0bef177)

## Cara remote Ubuntu ke Putty melalui alamat IP
1. Pastikan ubuntu server dalam keadaan “online”. Install putty dari internet dan lanjutkan hingga tampilan awal putty.
2. Ketik pada terminal ubuntu server “ip addr” untuk mengetahui IP dari ubuntu server. IP tadi ketik kembali dalam tabel “Host Name (or IP address) ”.
   ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/f79b5898-9e41-45f9-a6b8-bd6e132f4bb7)

3. Klik “Open” dan masukkan username beserta password dari ubuntu servernya sendiri.
4. jika berhasil, akan tampil pesan yang sama saat login ke ubuntu server.
   ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/6f9c7515-b0ea-4dfd-bf5d-58a704a6fd81)

## Cara menghubungkan server ke CMD menggunakan SSH
1. hubungkan ubuntu server dengan CMD menggunakan ssh. Buka CMD di windows, kemudian ketikkan “ssh <nama_user@IP_user>”.
2. Masukkan password ubuntu. Jika muncul pesan selamat datang pada CMD, maka CMD siap digunakan untuk mengontrol ubuntu server.
   ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/c52a1475-9b09-4cde-8678-6d9a83326d4b)

# Cara Menginstall Nginx
 1. Update terlebih dahulu sistem ubuntu server dengan perintah
     ```
     sudo apt update
  2. Install nginx dengan perintah berikut
     ```
     sudo apt install nginx
  ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/89e697a6-1753-4f10-9e9c-47bd19b0f397)
  
  3. Mengecek apk yang diinstal
     ```
     sudo ufw app list
   ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/84575ec3-c40b-4d19-ab2e-f9f8300fc5ae)

4. Selanjutnya pengecekan status dari nginx
     ```
     sudo systemctl status nginx
  ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/45793ab5-f17e-460e-8bb7-27cbc901ff47)

5. Mencari alamat IP server
   ```
   curl -4 icanhazip.com
 ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/996e4be7-cea6-4e3c-8bc2-2fcbf2494dec)

6. Pengecekan diweb browser dengan mengetik IP diweb
 ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/65838e36-e7de-4f22-b101-8e412521f89a)

# Cara Menginstall Wordpress
1. Memperbarui dan mengupgrade paket di sistem
   ```
   sudo apt update && sudo apt upgrade
  ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/ff451697-5c7a-40d7-ae65-860af887b719)

2. Menginstal server web Apache
   ```
   sudo apt install apache2
  ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/4c66682a-8b83-4183-9df3-1afbf3446cfd)

3. Memeriksa status layanan Apache
   ```
   systemctl status apache2
  ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/2cf69485-36f5-4645-a764-0456bce6317d)

4. menginstal server basis data MariaDB
   ```
   apt install mariadb-server mariadb-client
  ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/2d50cbe7-6c69-4d7a-9843-e391bd73b0f3)

5. Menjalankan skrip keamanan untuk mengamankan instalasi MariaDB
   ```
   mysql_secure_installation
  ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/175746de-f19a-460b-abcd-263e8bd19f92)

 6. Menginstal PHP dan ekstensi MySQL
    ```
    apt install php php-mysql
   ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/7ff44f86-52ce-47b1-ab67-ba76a4fd1c7f)

7. Membuat berkas info.php untuk memeriksa konfigurasi PHP
   ```
   nano /var/www/html/info.php
8. Menginstal modul PHP untuk Apache dan koneksi PHP ke MySQL
   ```
   sudo apt install php libapache2-mod-php php-mysql
  ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/bfa3f670-a1c5-4d59-b7df-952e12f224f4)
  
  ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/40b57ca5-6455-426a-a092-9f5127edb753)

9. Mengakses shell MySQL sebagai pengguna root
   ```
    mysql -u root -p
  ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/f0c8682e-6990-45f6-a875-0c684d69026b)

10. Unduh paket terbaru Wordpress
    ```
    cd /tmp && wget https://wordpress.org/latest.tar.gz
  ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/d3f3fd8e-683a-40b5-8697-ba197bd12314)

11. Mengekstrak paket WordPress yang telah diunduh
    ```
    tar -xvf latest.tar.gz
  ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/3fc1130e-9e1a-4378-aadd-316b4b7ebcdc)

12. Izinkan izin yang dapat dieksekusi diberikan ke folder WordPress
     ```
     sudo chmod -R 777 wordpress
  ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/8165f898-a991-4c6c-8e17-8cf90476cd8d)

13. Konfigurasikan WordPress
     ```
     cd wordpress/
     mv wp-config-sample.php wp-config.php
     nano wp-config.php

   Ubahlah pada baris define( 'DB_NAME', 'Nama Database' ); dan diganti sampai kebawah sesuai perintahnya, lalu simpan file CTRL + X

14. Setelah selesai melakukannya, Anda dapat mengakses halaman WordPress Anda untuk menyelesaikan instalasi. Buka browser
     ```
     https://localhost/wordpress/
   ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/3cafa9dc-2ad3-438e-9f48-0eaf289f23eb)
   
   ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/4ad35718-b61e-4643-b803-dd90d902788d)
   
   ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/92a1bb7a-7699-498c-bdd0-c50c28ce103b)
   
   ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/a218afdc-afcd-4762-8676-7cb9751c67a8)

# Cara Menginstal Tableau Dekstop dari Windows
1. Langkah pertama untuk menginstal tableau yaitu cari tableau di chrom kemudian pilih tableau public
   ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/f843cd13-4bfd-4bd3-b6b8-218fce7b46b0)

2.	Pilih Platform yang akan gunakan, seperti Windows atau macOS lalu download Tableau tersebut
    ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/bea5fcf8-169e-4fe5-9cb9-29b8e20a387c)

3.	Instalasi tableau, aktivasi dan registrasi
    ![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/e30ef02b-c2ce-4404-9cf0-3723140d1fe4)

  	![image](https://github.com/KhairunnisaJunaidi/KhairunnisaJunaidi-Apache2-Wordpress-Nginx-tableau/assets/150565586/d88df18f-ffcc-4dca-8220-a4facd6b4e7a)
