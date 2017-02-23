---
title:  "Jekyll ile Web Site Yapımı"
subtitle: "Jekyll"
author: "Büşra Önder"
avatar: "img/authors/tb.jpg"
image: "img/jekyll.jpg"
date:   2017-02-23 16:32:12
---

## Ubuntu Üzerine Jekyll Kurulumu

Jekyll Ruby dili ile yazılmış,site oluşturucu bir yazılımdır.Jekyll ile Github Page Sayesinde web sitenizi oluşturabilirsiniz.Veritabanı kullanımı yoktur.Onun yerine MARKDOWN ile yazılarımızı formatlı bir şekilde yazıp web sitemize ekleyebiliyoruz.Jekyll kurmadan önce bilgisayarınızda Ruby yüklü olması gerekmektedir.

İlk önce update işlemini yapalım.

 	<b>$ sudo apt-get update</b>

Daha sonra Ruby kurulumu gerçekleştirelim.

	<b>$ sudo apt-get install ruby ruby-dev make gcc</b>

En son olarak da Jekyll Bundle kurulumu yapalım.

	<b>$ sudo gem install jekyll bundler</b>

Web sitemizi oluşturmamız için herşey şimdi diğer aşamalara geçelim.

Oluşturmak istediğimiz dizinin içerisine gidip (Örneğin : <b> $ cd /Home </b> )

	<b>$ jekyll new site_ismi </b> 

yazıyoruz.

	>ÇIKTI:
	![jekyll new](/img/jekyllnew.png "Jekyll New")

Klasörümüz hazır durumda.Kalsörümüzün içini açıp bakarsak 

	> ![jekyll before serve](/img/jekyllbeforeserve.png "Jekyll Serve Öncesi")

bunlarla karşılaşacaksınızdır.Ama bu sitenin çalışması için > _site  adlı klasörün mutlaka olması gerekiyor yoksa hata alırsınız.
Burada dikkat edilmesi gereken kısım ( Benim başımı çok ağrıttı için )
bu kalsörü oluşturduktan 

	<b> $ cd  site_ismi (Klasörün içine girip aşağıda kodu yazıyoruz) </b>
	<b> $ jekyll serve </b>

Komutunu vermenizdir.

	>ÇIKTI:
	![jekyll serve](/img/jekyllserve.png "Jekyll Serve")


jekyll serve yaptıktan sonra klasörümüzün içeriğine bakacak olursak

	> ![jekyll after serve](img/after.png "Jekyll Serve Sonrası")

İşte bizim için en önemli _site klasörü geldi.Şimdi [http://localhost:4000](http://localhost:4000) adresine gidip bakarsanız sizi şöyle bir site karşılayacak

	[id]: http://busraonder.me/img/youraxesome.png "Welcome to Jekylll"
	> ![Welcome to jekyll][id]

	
Bu ekranla karşılaşmışsanız jekyll çalışıyor demektir.

Bundan sonrası ise  beğendiğiniz bir jekyll teması indirip içindeki klasörleri bu oluşturduğumuz klasörün içine atmaktır.(_site dosyasının değişmemesine veya silinmemesine dikkat edin).Bu işlemde hallolduktan sonra tekrar  jekyll serve yapıp localhostunuza bakarak yeni temanızın nasıl göründüğüne bakabilirsiniz.Eğer hoşunuza gittiyse şimdi asıl geçelim.

[Github](https://github.com/)’a üye değilseniz üye olmalısınız.Porfilinize geldiğinizde sağ taraftaki + işaretine tıklayarak 
new Repository tıklayarak yeni alanınız oluşturun.İleriki aşamalarda elinizde .github.io uzantılı bir adres olacaktır.Bu alanı oluşturduktan sonra tekrar web sitemizi yöneteceğimiz bir dizine gidip 

  	 <b>$ git clone alanadınız.github.io </b>

komutu vermeniz gerekmekte bu komut verildikten sonra içerisinde bulunduğunuz dizinde alanadınız.github.io adlı bir klasör oluşmuş olacaktır.Biraz önce tema indirip içine attığımız klasördekileri alıp bu klasörün içine atmanız gerekiyor.İşlemler tamamsa son kısma geçiyoruz.


Şimdi terminalden alanadı.github.io klasörüne giriyoruz (Örneğin : $ cd busraonder.github.io)
ve 

	 <b> $ git config --global user.name "githubadınız" </b>
	 <b> $ git config --global user.email "emailadresiniz" </b>

işlemleriyle bağlantınızı yapıyoruz.Sonra

	 <b> $ git init  </b>

komutunu vererek repository’mizi başlatmış oluyoruz.Ardından

	 <b> $ git status </b>
 
ile repository’nizin durumunu öğreniyorsunuz.(Hangi dosyalar eklenmiş, kaldırılmış).Devamında ise

	<b> $ git add .  </b>
	<b> $ git commit -m  “düzenleme nedeninizi yazıyorsunuz (size kolaylık olsun diye)”  </b>
	<b> $ git push origin master  </b> 

bu işlemlerden sonra sizden github username’iniz ve parolanız istenecektir.Sorunsuz olarak bu aşamalar tamamlandıktan sonra alanadınız.github.io adresine girdiğinizde yeni temanız sizi karşılıyor olacaktır.Sonra gerekli düzenlemeleri yaparak yukarıda belirttiğim > git init 
kısmından sonrasını tekrarlayınız bu şekilde websiteniz güncellenerek yaptığınız değişiklikler görünecektir. Güle güle kullanın :)





