---
author: doganzorlu
layout: post
title: "12. Ege Bilgi Güvenliği Toplantısı"
date: 2017-09-16 20:30
comments: true
category: Bilgi Güvenliği
tags:
- İzmir
- Bilgi Güvenliği
- KVKK
- Microsoft
- IoT
---

Düzenli bir şekilde sürdürülen **"Ege Bilgi Güvenliği"** toplantılarının 12. si TEMA VAKFI İZMİR ŞUBESİ salonunda yogun bir katılımla gerçekleştirildi.

![](/images/14_bg_meeting.jpeg){: width:100%; class="notepad-post-content post tag-simple"}
Toplantı oldukça zengin bir içeriğe sahipti. Bazı konular daha önceki toplantıdan devam eden konuları da içeriyordu. Bu toplantıdaki özel bölüm **Incident Response** olarak seçilmişti.

Toplantıda dikkatimi çeken ve sizlerle de paylaşmak istediğim konuları aşağıda bulabilirsiniz. Şayet **"Bilgi Güvenliği"** ilginizi çekiyorsa gruba katılabilir ve toplantıları izleyebilirsiniz. Bunun için;

  [**Resmi Web Sitesi**](http://www.egebilgiguvenligi.com/)<br>
  [**Resmi Facebook Sayfası**](https://www.facebook.com/egebilgisec)<br>
  [**Resmi Twitter Hesabı**](https://twitter.com/egebilgisec)<br>
  [**Resmi Linkedin Hesabı**](https://www.linkedin.com/groups/13507089/profile)<br>
  [**Resmi Instagram Hesabı**](https://www.instagram.com/cagripolatmsc)<br>

adreslerinden grubu takip edebilir, etkinliklere, duyurulara ve haberlere ulaşabilirsiniz.
<hr>
Evet ilk konu Equifax firmasında meydana gelen sızıntı ile ilgiliydi. Firma bir kredi kruluşu ve 143 milyon kredi hesabı sızdırıldı. Hesaplar deepweb de satışa çıkarıldı bile. Bilgiler içinde sosyal güvenlik numarasından kredi kartı numarasına kadar bilgilerin olduğu belirtiliyor. Firma olay sonrası bir online hizmet devreye alıp bazı bilgiler girildikten sonra hesabınızın etkilenip etkilenmediği ile ilgili bilgi veriyor. Son dönemin oldukça ilginç bir vakası olarak kayda geçen olayla 18 yaş üstü Amerikan vatandaşlarının yarısının bilgileri sızdırılmış oldu. GDPR bu durumların duyurulması ve kurbanların aksiyon alabilmesine olanak sağlanmasını istiyor. Bu arada firma yöneticilerinden üçünün olayın duyurulmasından hemen önce şirket hisselerini sattıkları da gelen haberler arasında. Bu gibi olaylarda insider hack çokça görülen bir durum. Bakalım bu vaka için yapılan incelemenin sonucu ne çıkacak.
<hr>
Daha dumanı üzerinde bir konu olarak **Yama Yönetimi** oldukça önemli bir konu olarak etraflıca değerlendirildi. Bilindiği gibi salı günü Microsoft tarafından yayınlanan yamalar içerisinde outlook 2007 için olan güvenlik yaması, dil dosyalarında soruna sebep olarak dünya genelinde kullanıcı arayüzlerinin farklı dillerde çıkmasına sebep olmuştu. Bu durum merkezi güncelleme sistemlerinin güvenilirliği konusunda endişe verici bulunmakla birlikte, üreticiye bir şekilde güvenmek zorunda olduğumuz gerçeğini değiştirmedi. Bu arada son salı güncellmesi ile 27 tane güvenlik güncellemesi geldiğini ve 4 tanesinin etki seviyesinin 10 olduğunu hatırlatmakta yarar var. Bunlar;

* CVE-2017-8759 - .NET Framework 3.5.1 (exploit toolkiti bile yayınlandı) İlginç bir not eğer bu güncelleme sonrası dil paketi yüklenirse güncellemenin tekrar yüklenmesi gerekiyor. Takip et edebilirsen.
* CVE-2017-8746 - Yerel guvenlik atlatma zaafiyeti
* CVE-2017-8723 - Windows 10 Edge CSP den kaynaklı güvenlik katmanı zaafiyeti
* CVE-2017-9417 - Broadcom Wifi Driver

Tabi güncellenmesi gereken yegane şey MS ürünleri değil. Bu nedenle her toplantıda değinildiği gibi diğer uygulamaları da izleyen ve güvenlik açıkları ile ilgili yönetim olanakları sağlayan sistemlerin acilen kurulmasının önemine değinildi. Günün ödülü: [**'All CVE in one place'**](https://www.saucs.com/)
<hr>
BlueBorn güzel bir isim gibi geliyor kulağa. Fakat hayatı zehir edebilesi bir Bluetooth stack zaafiyeti ve man-in-middle ile bluetooth haberleşmesi esnasında cihazınıza uzaktan erişimi olanaklı sağlıyor. Bluetooth 5 de Mesh de var biliyorsunuz. Sadece yakındaki bir cihazdan söz etmiyor olabilirsiniz. Daha şimdiden birçok vaka rapor edilmiş durumda. İşte soru;

"Cihaz üreticiniz güncelleme yayınlamazsa ne yapacaksınız ?"

üzülerek söylemek gerekir ki artık bluetooth kapalı olarak yaşamınıza devam edeceksiniz. Bu konu önemli ve önümüzdeki günlerde çokça konuşulacak. Sahi, mobil cihazınızda hangi antivirus uygulamasını kullanıyorsunuz ?
<hr>
Geçtiğimiz günlerde meşhur The Shadow Brokers tarafından yeni bir exploit yayınlandı. Bilindiği gibi NSA tarafından kullanılan pekçok hacking aracını çalan grup bunları aralıklarla sızdırıyor. En son olarak **"United Rake"** olarak kodlanmış ve **"fully extensible remote collection system"** adında bir hacking aracını sızdırdı. Söz konusu aracın fiyatı da 100 ZEC (ZCash elektronik para birimlerinden birisidir 1 ZCash 248 USD ediyor) olarak belirlemiş. Plugin yapısı bile var uygulamada daha ne diyeyim. Bu hacking grubu daha önce eternalblue sızıntısını da yapmış ve sonucunda wannacry benzeri ransomware ler tüm dünyada etkili olmuştu.
<hr>
Hazır elektronik paradan konuşulmuşken bu paranın üretiminden kaynaklı gelirlerin vergilendirilmesi ile ilgili sorunlar ve vergilendirilemediği için suç haline gelen gelirlerle ilgili de bir etkinlik duyurusu yapıldı. Bu etkinlik 29 Eylül tarihinde baro tarafından düzenlenecek ve belirli bir miktar dış katılımcının katılımı mümkün olabilecek gibi görünüyor. İlgililerine şimdiden duyurulur.
<hr>
FDA'yi duyan var mı ? Ben bugün duydum. Hoş herbir şeyin Federal i olduğuna göre ilaçlarla ilgilisinin olmaması şaşırtıcı olurdu doğrusu. İşte en bomba konulardan birisi bu ajansın **Kalp Pillerini** geri çağırması ile ilgili ortaya çıkan durumdu. Bir grup pil (ki şu ana kadar 465.000 kişiye takılmış) bir cihaz sayesinde uzaktan yeniden programlanabiliyor, yani enerji kesilebiliyor veya kalp atış hızı değiştirilebiliyor. Üretici kalp pili için bir firmware yayınlamış durumda ve sağlık personeli bu yamayı pile uygulayabiliyor. Bu pil nerelerde kullanılıyor ülkemizde var mı, varsa firmware ini kim güncelleyecek bunları bilemiyorum. Ha bu arada söz konusu açığı kullananarak pili yeniden programlayabilen cihazlar  15 dolardan başlayan fiyatlarla (kampanya gibi oldu) dolardan bulunabiliyormuş. Üstelik cihazlar normal ticari ürünler. Bu noktada geldiğimiz aşama insan hayatını doğrudan kontrol eden ürünlerin firmware yönetimi noktasıdır ki artık tehlikenin şekli oldukça değişiyor.
<hr>
Bir diğer ilgi çekici konu ise sağlık sektöründen. ICS-CERT tarafından duyurulan bir zaafiyet oldukça ilginçti. Medifusion 4000 serisi şırınga enjeksiyon pompası kablosuz bağlantı için oldukça zayıf bir yapı barındırıyor ve uzaktan rahatlıkla sızılabiliyor. ICS sitesinde detaylıca anlatılan [**"Smiths Medical Medfusion 4000 Wireless Syringe Infusion Pump Vulnerabilities"**](https://ics-cert.us-cert.gov/advisories/ICSMA-17-250-02) zaafiyet oldukça kritik bir soruyu aklımıza getiriyor. Hastanelerdeki donanımlar saldırılara karşı ne kadar korunuyor ? L2 ağ ayırımı yapılmayan veya bu zaafiyette olduğu gibi kablosuz yapısı sorunlu olan cihazların bulunduğu kurumlarda can güvenliği nasıl sağlanacak ? Bu tip cihazlara uzaktan erişim çok ciddi avantajlar sağlıyor. Bununla birlikte gereken güvenlik tedbirleri alınmaz ise bu avantaj kabusa çok hızlı dönüşebilir. Tıpkı enerji sektöründe olduğu gibi sağlık sektöründe hastanelerin de **"ISO 27001 Bilgi Güvenliği Yönetim Sistemi"** bulundurmaları zorunlu olmalı diye düşünüyorum. Tabii ki sektöre özel bir yönetmelikle detayları ve usulleri de tanımlanarak.
<hr>
Apache Struts çok güzel bir MVC framework. Java2EE developer larının yoğun kullandığı bu framework ile ilgili yeni çıkan zaafiyet özellikle katılımcılar arasında yer alan yazılımcıların ve sistem yöneticilerinin ilgisini çekmiş görünüyordu. Zayıflık kabaca REST servisinde deserialisation için kullanılan XStream ın herhangi bir filtreye tabi tutulmadan kullanımı sonucu RCE olanağı sağlaması olarak tanımlanmış. Sorun 2.5.13 ve 2.3.34 sürümlerinde giderilmiş. Peki soru şu, bu durumun kim farkında ve tüm bir sistem içinde söz konusu kütüphaneyi bağımlılıklarını koruyarak nasıl güncelleyeceğiz ? Burası önemli zira eğer üretici bununla ilgili bir patch yayınlamaz ise pekçok uygulama için tek başına bu kütüphaneyi güncellemek mümkün olmayabilir. Detaylar için [**'A RCE attack is possible when using the Struts REST plugin with XStream handler to deserialise XML requests'**](https://struts.apache.org/docs/s2-052.html) adresi ziyaret edilebilir. Bu zaafiyetten bazı Cisco ürünleri de etkilenmiş.
<hr>
Gün geçmiyor ki bir son kullanıcı ürününde zaafiyet çıkmasın. Aslında iş yerlerinde de sıkça karşımıza çıkan "Yahu kardeşim, 100 USD ye cihaz var gidip bu 1000 USB lik cihazları niye kullanıyorsun" sorusu ve soruda gizli sorunu da bir nebze göz önüne seren bir durum bu. Evet yine D-Link ve yine zaafiyet. 850L serisi router cihazlarında MyDLink protokolü ile herhangi bir authentication olmadan cihaza yetkili kullanıcı girişi yapılabiliyor. İşin ilginci Amazon üzerindeki bir sunucudan verilen MyDLink servisi şifrelenmemiş trafik üstünden çalışıyor. Ondan fazla açık tespit edilmiş burada yazacak kadar yer yok. Kullandığımız cihazları tanımamız hayati önemdedir. Bu iş başkalarına transfer edilebilecek bir iş değildir.
<hr>
SafeCopy nin trojanı olarak çıkan XafeCopy mobile tarafındaki ilk konu olarak gündeme geldi. Google markette orjinal ürün yerine benzer isimde paket yayınlayarak mobil cihazlara sızılması sıkça görülen bir durum. Özellikle android marketin bir ön inceleme mekanizması kurmasının ne kadar elzem olduğu konusunda hemfikir olduk diyebilirim. Tabi olayı abartıp Apple daki gibi aylara sari onay süreçlerine ulaşılması da üretkenliği düşürecektir.
<hr>
Dönüp dolaşıp geldiğimiz bir diğer konu ise KVKK. Nasıl olacak nasıl uygulanacak diye ciddi endişelerim olmakla bilikte oldukça ciddi bir yol alınmış sahada. Çağrı Bey'e önceki toplantıda bir framework oluşturmasının yararlı olacağını belirtmiştim, sanırım üzerinde çalışıyor. Güzel bir ekip kurmuşlar KVKK ile ilgili uyumlulukta rehberlik hizmeti veriyorlar. Biliyorsunuz şayet uzatılmaz ise kanun 2018 ikinci çeyrekte yürürlükte olacak. Zaman giderek azalıyor. Bu arada İzmir Barosu ve Ticaret Odası ile bir eğitim/bilgilendirme etkinliği yapacaklarmış kaçırmamak gerek.
<hr>
Microsoft **bash** kabuğunu Windows 10 için uyarladı biliyorsunuz. Tabi bir sürü de açığıyla beraber. Henüz bir CVE ile raporlanmamış ama bu katman kullanılarak zararlı uygulamaların gizlenebildiği rapor ediliyormuş, benden söylemesi.
<hr>
Instagramdan 6 milyon populer hesabın çalındığını duyunca bu tip olayları ne kadar kanıksadığımızı düşündüm. Başlarla "Abouvv", "Vaayy" gibi ünlemler gelirken şimdilerde artık "Aaa, o da mı ?" boyutunda. Bu sıkıntılı bir durum zira bunun sıradanlaşması iyi değil.
<hr>
MongoDB object database olarak acayip güzel bir ürün ve çok severek kullanıyorum. Bununla birlikte bir zaafiyet tespit edildiğinden bahsedilince nedir diye araştırayım dedim. Temel sorun database sunucunun internete açılması ve temel güvenlik tedbirleri alınmadan kutudan çıktığı gibi production a alınması gördüğüm kadarıyla. Anlamıyorum, hangi çılgın veritabanının portunu internete açar ki ? Üstelik söz konusu veritabanının güvenlik katmanında yapılandırma yapmadan ? Burada MongoDB ye değil onu bu şekilde çırılçıplak internete açanlara kızmak gerek. Bir kez daha uzmanından servis almanın önemini görmüş oluyor dünya. 26.000 den fazla sistem hacklenmiş. Docker platformuna bir göz atmanızı salık veriyorum. Yönetsel ve kaynak yönetimi özelliklerinin yanında bunun gibi güvenlikle ilgili de oldukça iyi bir ortam sağladığını göreceksiniz. Bir haber, Azure da dahil olmak üzere MS platformunun da **Container** (Bakınız: [Microsoft Containers](https://docs.microsoft.com/en-us/virtualization/windowscontainers/about/), [Docker Resmi Web Sitesi](https://www.docker.com/)) desteklediğini biliyor muydunuz ?
<hr>
Site phishing işinin b**ku çıkmış diyebileceğimiz bir aşamaya gelindiğini görmek şaşırtıcı olmadı. Bir bankanın web sitesinin 300'e yakın taklidi çıkmışsa daha ne denebilir ki. Aman dikkat.
<hr>
Incident Response nedir nasıl yapılır günün eğitsel olduğu kadar önemli bir konusu olarak sürpriz oldu. Temelde bir olay söz konusu olduğunda önceden planlanmış bir stratejinin uygulanması önemlidir. Böyle bir strateji yoksa panik ve kargaşada kritik hukuki verilerin kaybı ya da kullanılamaz hale gelmesi bile söz konusu olabilir. Kabaca adımları şu şekilde kurulur;

1. **Hazırlık:** Bu aşamada olay olduğunda kimler müdahale edeceki bu kişlere nasıl ulaşılacak gibi konular belirlenmiş olmalıdır.
2. **Tanımlama:** Olayın tanımlanması, kategorisinin belirlenmesi, yapılacak işlemler önceliklendirilmelidir.
3. **Kapsamın Belirlenmesi:** Olay müdahale ekibi devreye girmeli ve olaydan etkilenen sistem izole edilmelidir.
4. **Analiz ve Çözüm:** Olay nasıl, ne zaman nerede meydana geldi belirlenmesi ve kök nedenin belirlenmesi bu aşamada gerçekleştirilir.
5. **Onar:** Soruna neden olan zaafiyetin giderilmesi ve kök nedenin ortadan kaldırılması bu aşamda gerçekleştirilir. Akabinde işleyiş normale döndürülür.
6. **Ders Al:** Bu aşamda bir rapor hazırlanarak bu tip olaylarla karşılaşmamak için yapılacaklar tanımlanır ve üst yönetimle paylaşılır.
<hr>
Güzel bir etkinliğin ardından sonrakinde buluşmak üzere ayrıldık. Unutmadan sonraki etkinlik 04.11.2017 de yapılacak. Salon şimdiden belli değil, muhtemelen o zaman kadar duyurulmuş olur.

Neyse şimdilik bu kadar. Ege Bilgi Güvenliği Grubu'ndan muhabiriniz Doğan ZORLU bildirdi :)
