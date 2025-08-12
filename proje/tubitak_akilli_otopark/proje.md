---
page->layout = "post";
page->title  = "Kablosuz Şarj Destekli Akıllı Otopark Sistemi";
page->description = "Tübitak 2209-A Kapsamında Desteklenen Proje";
page->date ="2025-08-12";
SET_PROJECT();
---


Bu proje ile Tübitak 2209-A kapsamında "1919B012424414" başvuru numaralı projeyle destek alınmıştır. Bu projede yürütücü görevini üstlenmekteyim. Aynı zamanda Lisans bitirme tezi ve Lisans bitirme ödevi olarak bu proje Kayseri Üniversitesinde jürilere sunulmuştur. Bu proje ile Erciyes Üniversitesinde düzenlenen 4.AR-GE Proje Pazarı etkinliğine katılınmıştır.


<figure>
<img src="tubitak.png" alt="tubitak logo">
<figcaption>Tubitak</figcaption>
</figure>


Bu projenin amacı otoparklarda yaşanan problemlere çözüm getirmektir. En sık karşılaşılan problemlerden biri olan hatalı parkı önleyerek hem otopark kapasitesinin tamamını kullanmak hem de verimi en üst noktaya taşımaktır. Bir diğer sık karşılaşılan problem olan kolon ve kirişlere araçların sürtmesini veya çarpmasını engellemektir. Karbon ayak izini azaltmak ve çevreyi daha temiz bırakmak için elektrikli araç kullanımında sorun olan şarj istasyonları ve şarj desteklerini arttırarak elektrikli araç kullanımını yaygınlaştırmaktır. Elektrikli araç kullanıcılarının araçları otoparkta iken zaman tasarrufu sağlamak ve daha konforlu bir şarj deneyimi yaşatmak için kablosuz araç şarjı desteklenmektedir. Kablosuz şarj ile elektrikli araç kullanıcılarının otopark ve şarj deneyimini en iyi şekilde hissetmelerini amaçlanmıştır.

Bu projede otoparklarda oluşan yakıt ve zaman kaybını azaltarak araç kullanıcılarının en verimli şekilde park yeri bulmasını hedeflenmiştir. Elektrikli araç kullanıcılarına zaman ve yakıt tasarrufunun yanında kablosuz şarj desteği sunularak araçlarını en iyi şekilde kullanmaları hedeflenmiştir. Projemizin amaçlarından biri olan kablosuz şarj desteği ile elektrikli araç kullanımının arttırılması hedeflenmiştir. 

 <figure>
<img src="sekil1.1.png" alt="akıllı_otopark_genel_hali">
<figcaption><strong>Şekil 1.1</strong> Kablosuz Şarj Destekli Akıllı Otoparkın Genel Hali</figcaption>
</figure>

Şekil 1.1’de yer alan görselde Kablosuz Şarj Destekli Akıllı Otoparkın genel hali verilmiştir. Otopark prototipi beş araç için hazırlanmıştır. Park alanlarından bir tanesi engelli park alanı olarak ayrılmıştır. Bu ayrılan alanda engelli araç sahipleri için normal bir park alanının yaklaşık 1.2 katı genişliğe sahiptir. Engelli park alanına daha geniş bir alan bırakılarak daha rahat manevra hakkı sunulmuştur. Aynı zamanda bu alan sayesinde araçta bulunan tekerlekli sandalye vb. gibi eşyalar daha rahat araca yüklenip alınabilmektedir.
Otoparkta yer alan park alanları boş iken mavi ışık yanmaktadır.
 
  Şekil 1.2 Kablosuz Şarj Destekli Akıllı Otoparkın Doluluk Oranı Hakkında Bilgi Veren Giriş Ekranı
Şekil 1.2’de yer alan ekran üzerinden araç kullanıcılarına park alanlarının doluluğu hakkında bilgi verilmektedir. Bu ekran boş park alanlarını sayısal olarak kullanıcılara sunmaktadır. Kapının girişinde yer alan IR sensör aracı algılar ve giriş kapısının açılması için Arduino MEGA’ya sinyali gönderir. Arduino MEGA gelen sinyalle servo motoru harekete geçirir. Servo motor araçların girişi için 90 derece açılır, tanımlanan süre kapsamında açık kalır ve geri eski konumuna dönmektedir. 







 
	  Şekil 1.3 Kablosuz Şarj Destekli Akıllı Otoparkın Genel Çalışması
 
	  Şekil 1.4 Kablosuz Şarj Destekli Akıllı Otoparkın Genel Çalışmasının Blok Diyagramı
Kablosuz Şarj Destekli Akıllı Otopark yapısında aşağıda yer alan elektronik komponentleri kapsamaktadır.
- Arduino Mega 2560 R3
- HC-SR04 Ultrasonik Mesafe Sensörü
- Ağırlık Sensörü- Load Sensor
- HX-711 ADC Modülü
- XKT-408 Kablosuz Şarj Modülü
- 16×2 LCD Ekran
- MG90S Servo Motor
- RC522 RFID NFC Modülü, Kart ve Anahtarlık Kiti 
- ESP32-WROOM-32D Wifi Bluetooth Geliştirme Modülü
- ESP8266 Ekonomik Wifi Serail Transceiver Module
- TP4056 Type-C Korumalı Şarj Modülü
- Li-ion Batarya
- RGB Led
- Buzzer


Otopark alanlarında kullanılan mesafe sensörü araç kullanıcılarının park alanlarına doğru park etmeleri için yaklaşması gereken mesafeyi belirtmektedir. Mesafe sensörleri sayesinde araç sahiplerinin duvara ve kolonlara çarpmaması hedeflenmiştir. Belirlenen sınırların dışında yaklaşan araçlar sistemde kullanılan buzzer sayesinde uyarılmaktadır. Park alanlarında kullanılan RGB ledler ağırlık sensörleri ile koordine çalışmaktadır. Park alanlarında iki adet ağırlık sensörü bulunur. Bu sensörlerin amacı park alanında araç olup olmadığını algılamak ve araçların doğru park etmesine yardımcı olmaktır. Kullanılan ağırlık sensörlerinin üzerine araçların tekerlekleri doğru bir şekilde getirilmesi gerekmektedir. Araçların doğru park işlemini gerçekleştirmesi için iki tekerinde ağırlık sensörüne kuvvet uygulaması gerekir. Eğer tekerlerden sadece biri ağırlık sensörüne kuvvet uygularsa hatalı park olarak değerlendirilir. Ağırlık sensörlerinin yerleştirildiği konum ve alan, park alanına girecek araçların boyutları dikkate alınarak tasarlanmıştır. Tekerleğin kuvvet uygulayacağı alan ortalama bir tekerin eninin yaklaşık 3 katı kadardır. Bu alanın herhangi bir yüzeyine uygulanan kuvvet algılanmaktadır. Ağırlık sensörlerinin ikisine de uygulanan kuvvet yoksa park alanında yer alan led mavi, ikisinden birine uygulanan kuvvet algılanırsa kırmızı, ikisinde de kuvvet algılanırsa yeşil ışık yanmaktadır. Hatalı park işleminin olduğu park alanlarının bilgisi otoparktaki görevli tarafından görülmektedir. Otopark görevlisi hatalı park düzeltilmezse gerekli uyarıları araç sahibine yapmaktadır.




 
	  Şekil 1.5 Kablosuz Şarj Destekli Akıllı Otoparkta Yer Alan Kablosuz Şarj İstasyonu
 
Şekil 1.6 Kablosuz Şarj Destekli Akıllı Otoparkta Yer Alan Kablosuz Şarj İstasyonunun Blok Diyagramı

Şekil 1.5’te yer alan görselde elektrikli araçlar için kablosuz şarj istasyonu verilmiştir. Görselde yer alan araç bir elektrikli araç prototipidir. Araç üzerinde yer alan batarya TP-4056 Şarj Modülü ile şarj olmaktadır. Park alanında kullanılan XKT-408 Kablosuz Şarj Modülü alıcı ve verici olarak iki modülden oluşmaktadır. Verici modül Arduino Mega üzerinden 5V ile beslenmektedir, bu modül park alanına sabitlenmiştir. Alıcı modül ise aracın alt kısmına yerleştirilmiştir. Kablosuz şarj işleminin başlaması için iki kıstas vardır. Birincisi araç park alanına doğru park işlemini gerçekleştirecek, ikincisi araç sahibi yetkili kart ile şarj işlemini başlatacaktır. Şarj işleminin mevcut durumu ve bataryanın doluluk oranı park alanında yer alan ekran üzerinden verilmiştir. Bataryanın doluluk oranını öğrenmek için ESP8266 kullanılmıştır. Kullanılan ESP8266 bataryadan aldığı voltaj bilgisini ESP-NOW sayesinde kablosuz olarak park alanında kullanılan ESP-WROOM-32 ye göndermektedir. ESP-WROOM-32 aldığı voltaj bilgisini içerisindeki referans voltaj değerine göre hesaplayıp ekran üzerinden kullanıcılara yansıtmaktadır.
 
Şekil 1.7 Şarj İşlemi Tamamlanmış Elektrikli Araca Ait Ekran 

Araç sahipleri istedikleri zaman şarj işlemini sonlandırmaktadırlar. Eğer araç %100 batarya kapasitesine ulaşırsa istasyon şarj işlemini otomatik olarak sonlandırmaktadır. Aynı zamanda Kablosuz Şarj İstasyonu kendine ait simge ile kullanıcılara yardımcı olmaktadır.
Proje fikrimizi destekleyen TÜBİTAK’a teşekkürlerimi sunarım. Proje aşamasında gerekli bilgi ve desteği sağlayan Doç. Dr. Rıdvan DEMİR’e teşekkürlerimi sunarım. Bu projede çalışma arkadaşlarım olan Tarık Talha KILIF ve Ali YALÇIN’a teşekkür ederim.

<a href="Bitirme_Projesi_Tezi.pdf" target="_blank">Bitirme Tezi</a>
