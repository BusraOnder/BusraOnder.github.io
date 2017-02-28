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

<b> $ sudo service mongod stop </b>

MongoDB'yi kaldırdığımıza göre şimdi paketleri silebiliriz.

<b>$ sudo apt-get purge mongodb-org*</b>

Şimdi sırada MongoDB veritabanlarını ve log dosyalarını kaldırmak var.

<b>$ sudo rm -r /var/log/mongodb</b>
<b> $ sudo rm -r /var/lib/mongodb</b>

İşte bu kadar MongoDB'yi bilgisayarımızdan kaldırmış bulunuyoruz.Eğer tekrar indirmek ve öğrenmek  isterseniz diğer yazılarıma bakmayı unutmayınız.


	