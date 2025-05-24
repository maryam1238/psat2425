# Penilaian Sumatif Akhir Tahun
## Mapil DevOps XI TJKT 1 - Penilaian Praktek
### SMKN 1 Banyumas - TA. 2024 2025


#
# Cara mendeploy Aplikasi
- download file paknux di repositorinya paknux 
- ekstrak file yang sudah di download ke folder (data D)       
- ke vscode (untuk membuat terminal)
- klik file pada menu atas kiri    -pilih open folder 
- pilih folder yang sudah terinstall 
- lalu simpan per file (ctrl+s)     -buat file ".env" enter 
- buat repository name masuk ke git hub dan sign in
- lalu create
- masuk ke vscode
- new terminal 
- $  git  --version 
- $  git  config  --global  user.name 
- $  git  config  --global  user.email 
- $  git  init 
- $  git  remote add origin 
- $  git  branch  -M  main 
- $  git  add  . 
- $  git  commit  -m  "first commit" 
- $  git  push  -u  origin  main -login aws academy canvas menggunakan akun yang sudah di miliki 
- pada dasboard klik aws academy learnebleb 
- klik moduls 
- klik meluncurkan aws 
- start leb 
- lalu pilih aurora dan RDS  
- ke database (jika sudah ada database tidak perlu membuat lagi) 
- lalu ke EC2 
- ke instances 
- launch an instances 
- isi name and tags sesuai yang diinginkan 
- pilih ubuntu 
- biarkan t2.micro 
- keypair pilih vockey 
- pada network setting ganti yang firewall (security group) klik select existing security group 
- scroll lalu ubah pada common security groups pilih SGServerWeb 
- scroll klik advanced details 
- isi bagian user data-optional 
- masukkan perintah untuk menjalankan script 

```
#!/bin/bash
echo '#!/bin/bash
sudo apt update -y
sudo apt install -y apache2 php php-mysql libapache2-mod-php mysql-client
sudo rm -rf /var/www/html/{,.}
sudo git clone [repository githubmu] /var/www/html
sudo chmod -R 777 /var/www/html
echo DB_USER=[username rds] > /var/www/html/.env
echo DB_PASS=[password rds]  >> /var/www/html/.env
echo DB_NAME=[nama database]  >> /var/www/html/.env
echo DB_HOST=[endpoint rds] >> /var/www/html/.env
sudo apt install -y openssl
sudo a2enmod ssl
sudo a2ensite default-ssl.conf
sudo systemctl reload apache2' > /home/ubuntu/otomatis.sh

chmod +x /home/ubuntu/otomatis.sh
```  
- lalu isi yang didalam tanda kurung sesuai dengan milik masing-masing 
- lalu launch instance 
- jika sudah succes klik instances 
- klik instances id 
- klik connect -lalu Jalankan dengan $ ./otomatis.sh 
- lalu copy ip public xan buka di new tab 
- lalu isi bagian login dengan username dan password
- jika sudah muncul halaman penilaian sumatif akhir tahun isi bagian input data siswa sesuai dengan data diri masing-masing dan simpan.

kira kira seperti itu .