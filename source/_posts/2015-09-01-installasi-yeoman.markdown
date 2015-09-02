---
layout: post
title: "Installasi Yeoman"
date: 2015-09-01 10:29:33 +0700
comments: true
categories: 
---

Apa sih yeoman itu ? mengenai penjelasan yeoman itu apa silahkan cek 
[disini](http://yeoman.io/) hehehe...
Intinya sih yeoman itu sebuah generator untuk membuat sebuah project, dalam hal ini saya gunakan untuk membuat project menggunakan framework [AngularJS](https://angularjs.org/) dan [Twitter Bootstrap](http://getbootstrap.com/). 

Sebelum bisa menggunakan yeoman ini, pertama-tama rekan kerja kita (laptop atau pc) sudah terinstall [NodeJS](https://nodejs.org/download/). Versi berapa ? ambil aja versi terakhir di website resmi nya NodeJS. Karena jika menggunakan versi yang terlalu lama, ntar malah sering kena error ketika generate project atau waktu compile project. 

Gimana kalo diinstall lewat package manager atau ```apt-get``` (Khusus Linux User)? Sebenernya nggak jadi masalah, asalkan versinya ikut update juga. Untuk yang pake cara download dari website resminya [NodeJS](https://nodejs.org/download/) silahkan ikuti langkah-langkah berikut :

1. download nodejs versi terakhir disini
   https://nodejs.org/download/
2. copy file ```node-xxx.tar.gz``` ke directory ```/opt```
3. buka terminal kemudian masuk menjadi user ```root```	
   ```$sudo su```
4. extract file ```node-xxx.tar.gz``` di directory ```/opt``` tersebut dengan cara dibawah ini 
   ```cd /usr/local && tar --strip-components 1 -xzf /opt/node-v0.12.7-linux-x86.tar.gz```
5. setelah sukses meng-ekstrak file ```node-xxx.tar.gz```, selanjutnya keluar dari user ```root```
6. kemudian cek versi node dan npm-nya 	
   ```$ node -v```	
   ```v0.12.7```	

   ```$ npm -v```	
   ```2.11.3```	
7. kemudian lakukan perintah berikut ini, agar versi npm nya terupdate	
   ````sudo npm -g update npm```	

   Cek lagi versi npm-nya	
   ```$ node -v```	
   ```2.14.1```	
8. kemudian install paket bower, yo, generator-angular, grunt-cli
   ```sudo npm -g install bower yo grunt-cli generator-angular```
9. setelah sukses generate aplikasi dengan perintah ```yo angular``` dan kira-kira akan muncul tampilan seperti berikut : 	
![tampilan ketika generate aplikasi angular menggunakan yeoman](images/install-yeoman/yeoman_generate.png "Generator Angular")

Karena aplikasi yang digenerate adalah anggular dan bootstrap, maka ```sass with compass``` di isi ```no```. dan pilihan ```Bootstrap``` di isi ```yes```.

Jika proses generate angular dengan perintah ```yo angular``` sukses tanpa error, langkah terakhir yaitu test dengan melakukan perintah ```grunt serve```. Jika sukses maka akan muncul tampilan seperti berikut dibrowser anda 
![tampilan ketika generate aplikasi angular menggunakan yeoman](images/install-yeoman/preview.png "Generator Angular")