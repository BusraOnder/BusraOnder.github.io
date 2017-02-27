---
title:  "MongoDB Kurulumu
subtitle: "MongoDB"
author: "Büşra Önder"
avatar: "img/authors/wferr.png"
image: "img/mongodb2.png"
date:   2017-02-26 15:10:12
---

### Ubuntu 16.04 Üzerine MongoDB Kurulumu

	MongoDB Kurulumumuzu gerçekleştirmek için terminalimizi ( Ctrl+alt+T ) açıyoruz.Daha sonra bilgisayarımıza MongoDB'nin repository'sini ekliyoruz.

<b> $ sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv EA312927 </b>

Çıktımızın şu şekilde olması gerekiyor.

>gpg: Total number processed: 1
>gpg: imported: 1  (RSA: 1)

Daha sonra MongoDb için liste dosyasını oluşturalım.Ve ardından bilgisayarımızı güncelleyelim.

<b> $ echo "deb http://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.2.list </b>
<b> $ sudo apt-get update </b>

Sıra MongoDB paketini indirmeye 
	
<b> $ sudo apt-get install -y mongodb-org </b>

Şimdi de MongoDB yapılandırmak için bir dosya oluşturacağız.

<b> $ sudo nano /etc/systemd/system/mongodb.service </b>

Açılan dosyaya şu verileri yapıştırınız.

> [Unit]
	Description=High-performance, schema-free document-oriented database
	After=network.target

>[Service]
	User=mongodb
	ExecStart=/usr/bin/mongod --quiet --config /etc/mongod.conf

>[Install]
	WantedBy=multi-user.target

MongoDB'yi başlatalım

<b> $ sudo systemctl start mongodb </b>


MongoDb'nin ne durumda olduğunu kontrol edelim.

<b> $ sudo systemctl status mongodb </b> 


Aşağıdaki gibi bir çıktı alırsanız güzel bir kurulum yapmışsınız demektir.

>>	● mongodb.service - High-performance, schema-free document-oriented database
   Loaded: loaded (/etc/systemd/system/mongodb.service; enabled; vendor preset: enabled)
   Active: active (running) since Mon 2016-04-25 14:57:20 EDT; 1min 30s ago
 Main PID: 4093 (mongod)
    Tasks: 16 (limit: 512)
   Memory: 47.1M
      CPU: 1.224s
   CGroup: /system.slice/mongodb.service
           └─4093 /usr/bin/mongod --quiet --config /etc/mongod.conf


Şimdi terminalden MongoDB'yi açalım.

<b> $ mongo </b>

Artık veritabanımızı oluşturabiliriz.Diğer yazılarda görüşmek üzere...
