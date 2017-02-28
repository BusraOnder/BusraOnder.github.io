---

layout: post
title:  "MongoDB Kaldırma"
subtitle: "MongoDB"
author: "Büşra Önder"
image: ""
date:   2017-02-26 15:10:12
---

<img src="/img/mongodb4.jpeg">



MongoDB'yi kaldırmak mı istiyorsunuz? O zaman hadi kaldıralım.

MongoDB kaldırma için ilk önce MongoDB'yi durdurmamız gerekmektedir.

---->
	$ sudo service mongod stop

MongoDB'yi kaldırdığımıza göre şimdi paketleri silebiliriz.

---->
	$ sudo apt-get purge mongodb-org*

Şimdi sırada MongoDB veritabanlarını ve dosyalarını kaldırmak var.

---->
	$ sudo rm -r /var/log/mongodb
	$ sudo rm -r /var/lib/mongodb

İşte bu kadar MongoDB'yi bilgisayarımızdan kaldırmış bulunuyoruz.Eğer tekrar indirmek ve öğrenmek  isterseniz diğer yazılarıma bakmayı unutmayınız.


	