Menggunakan CodeIgniter Version 3 Web Company Profile.
CARA INSTALLASI via VPS Linux LAMP.
1. Buat database MySQL atau PHPMyAdmin dengan nama "fipmoweb".
2. Import database "fipmoweb-export.sql" ke dalam database yang telah Anda buat.
3. Buka file "database.php" di folder "application/config".
4. Sesuaikan nama database, username dan password database yang Anda miliki.
5. install phpversion 5.6 or 7.4
SET UP VIRTUALHOST APACHE
1. masuk /etc/apache2/site-available
2. buat virtualhost baru nano name.conf
3. Masukkan config berikut :
<ul>
  <li>
  <IfModule mod_ssl.c>
<VirtualHost *:443>
        ServerName domain.tld
        ServerAlias www.domain.tld
        ServerAdmin domain@gmail.tld
        DocumentRoot /var/www/web/

        ErrorLog ${APACHE_LOG_DIR}/error.log
        CustomLog ${APACHE_LOG_DIR}/access.log combined

Include /etc/letsencrypt/options-ssl-apache.conf
SSLCertificateFile /etc/letsencrypt/live/fipmo.id/fullchain.pem
SSLCertificateKeyFile /etc/letsencrypt/live/fipmo.id/privkey.pem

</VirtualHost>
</IfModule>

<Directory /var/www/web/> folder file codeinetter3
    Options Indexes FollowSymLinks
    AllowOverride All
    Require all granted
</Directory>
</li>
</ul>
4. Restart service apache2.

USERNAME DAN PASSWORD:
Username: admin@gmail.com
Password: admin

HALAMAN LOGIN
http://localhost/login
