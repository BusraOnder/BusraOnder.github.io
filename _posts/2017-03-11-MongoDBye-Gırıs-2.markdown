---
layout: post
title:  "MongoDB'ye Giriş-2"
subtitle: "MongoDB"
author: "Büşra Önder"
image: ''
date:   2017-02-26 13:59:12
---
<img src="/img/mongodb.png">

# MongoDB Nedir? (Çeviri)

	MongoDB, çapraz platformda, belge tabanlı bir veritabanı olup,yüksek kapasiteli,yüksek performanslı ve kolay ölçeklenebilirdir.MongoDB kavram üzerinde çalışır.

## VERİTABANI
	
	Veritabanı veri toplamak için fiziksel konteynerdır.Her bir veritabanı  dosya sisteminden kendi dosyasını alır.Tek bir MongoDB sunucusu genellikle birden fazla veritabanına sahiptir.

## KOLEKSİYON

	Koleksiyon,bir grup MongoDB belgesidir.Bir RDBMS(İlişkisel Veritabanı Yönetim Sistemleri) tablosuna eşdeğerdir.Bir koleksiyon,tek bir veritabanı içerisinde bulunur.Koleksiyonlar bir şemayı zorunlu kılmazlar.Belgeler bir koleksiyonun içinde farklı alanlara sahip olabilirler.Genellikle,bir koleksiyondaki tüm belgeler benzer veya ilgili amaçlıdır.

## DOKÜMAN

	Bir doküman,bir anahtar-değer çifti grubudur.Dokümanlar dinamik şemaya sahiptirler.Dinamik şemanın anlamı aynı koleksiyondaki belgelerde  aynı kümeye ihtiyaç duyulmadığı anlamına gelir.Alanları veya yapıları ve bir koleksiyonun belgelerindeki ortak alanlar farklı veri türleri içerebilir.

	Aşağıdaki tabloda RDBMS termonolojisi ile MongoDB arasındaki ilişki gösterilmekdir.

![RDBMS / MongoDB](/img/rdbms-mongodb.png)

## MongoDB’nin  RDBMS’ye göre avantajları

-> MongoDB collectionlarında birbirinden farklı documentler tutar.Belgenin alanları diğer belgelerden içerik ve boyut olarak farklı olabilir.
-> Tek bir objenin yapısı açıktır.
-> Kompleks değildir.
-> Derin sorgulama yeteneği vardır.MongoDB belgeleri(document) kullanarak dinamik sorgulamayı destekler.Belge tabanlı sorgulama SQL kadar güçlüdür.
-> Ayarlanabilir.
-> Ölçeklendirilmesi kolaydır.
-> Uygulama nesnelerinin ihtiyaç duyulmayan veritabanı nesnelerine dönüştürür.
-> Veriye daha hızlı erişmek için dahili hafızayı çalışma kümesini depolamak için kullanır.

## MongoDB niçin kullanılır?

-> Veriler JSON tarzı belge biçiminde depolanır.
-> Bir dizin üzerinde herhangi bir özellik vardır.?
-> Kopyalanabilirlik ve yüksek kullanılabilirlik.
-> Otomatik frenleme.?
-> Çoklu sorgulama
-> Yerinde hızlı güncellemeler
-> MongoDB tarafından profesyonel destek sağlanır.

## MongoDB nerelerde kullanılır?
-> Big-Data (Büyük-veri)
-> Content Managment and Delivery (İçerik yönetimi ve teslim)
-> Mobil ve sosyal altyapılar
-> User daat management (Kullanıcı veri yönetimi)
-> Data hub (veri merkezi)

### MongoDB Başlatma

<b> $ sudo service mongodb start </b>

### MongoDB Durdurma

<b>	$ sudo service mongodb stop </b>

###MongoDB Yeniden Başlatma

<b>	$ sudo service mongodb restart </b>

###MongoDB Çalıştırma

<b>	$ mongo </b>


### MongoDB Help
	MongoDB’ işimize yarayacak olan sorguları bize sıralar.

<b>	>db.help() </b>

![db.help() ](/img/dbhelp.png)

## MongoDB İstatistiği
	Veritabanımızın ismini,document sayısını,collection sayısını ve veritabanının diğer özelliklerini bize gösterir.

<b>	>db.stats() </b>

![db.status()](img/dbstats.png)

#MongoDB-Data Modelling
	
MongoDB’deki veriler aynı koleksiyonda (tablo) esnek bir şema belgesine(tablodaki satırlara) sahiptir.

MongoDB’de şema hazırlarken bazı hususlar:
Şema kullanıcının isteklerine uygun oluşturulmalıdır.
Birlikte kullanılacak nesneleri bir belgeye yerleştirin.Kullanmayacaksanız ayrı belgelere yerleştirin.
Verilerinizi kopyalayınız (fakat sınırlı ) çünkü disk alanı hesaplama zamanı ile karşılaştırıldığında ucuzdur.
Yazarken birleştirin okurken değil.
Şemanızı en sık kullanılan durumlar için en uygun hale getirin.
Şemada karmaşık birliştirmeleri yapın.

ÖRNEK

Varsayalım   müşterinizin blog web sitesi için bir veritabanına ihtiyacı var.RDMS ve MongoDB şemaları arasında kaldınız.Websitenin şartları şunlardır.
Her yayın benzersiz başlık,açıklama ve url ye sahiptir.
Her yayın bir veya daha fazla etikete sahip olabilir.
Her yayın, yayıncısının adı ve sevdiği toplam sayısı vardır.
Her yayında kullanıcıların kendi adlarıyla yaptıkları yorumları,mesajları,veri süreleri,ve sevdikleri vardır.
Her yayında sıfır veya fazla yorum olabilir.
Eğer RDBMS’ye göre bu veritabanı oluşturulacak olursa en en 3 tablo yapılmalıdır.

![RDBMS'de oluşturursak](img/dbRDBMS.png)

Ama MongoDB’de tasarlarsak sadece bir koleksiyonla halledebiliriz.

![MongoDB'de oluşturursak](img/dbMongo.png)

Devamı diğer yazımda ...
