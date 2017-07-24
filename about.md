---
layout: page
permalink: /about/index.html
title: DOĞAN ZORLU
tags: [Dogan, Zorlu, Doğan]
chart: true
---

{% assign total_words = 0 %}
{% assign total_readtime = 0 %}
{% assign featuredcount = 0 %}
{% assign statuscount = 0 %}

{% for post in site.posts %}
    {% assign post_words = post.content | strip_html | number_of_words %}
    {% assign readtime = post_words | append: '.0' | divided_by:200 %}
    {% assign total_words = total_words | plus: post_words %}
    {% assign total_readtime = total_readtime | plus: readtime %}
    {% if post.featured %}
    {% assign featuredcount = featuredcount | plus: 1 %}
    {% endif %}
{% endfor %}

Hakkımda merak ettikleriniz ...!

Öncelikle merak edip benimle ilgili bilgileri kontrol ediyor olduğunuz için çok teşekkür ederim. İsmim **Doğan ZORLU**. Sitede bol miktarda kod, bilgisayar teknolojileri, müzik biraz da oyunlar hakkında içerikler buluyor olacaksınız. Zira bunlar benim ilgi alanlarım ve zamanımın çoğu bunlarla geçiyor. Yaklaşık 30 yıllık bilişim maceramın kronografisi sanırım şöyle;
* 2013-Bugün: Datacenter yöneticisi
* 2009-2013: Sistem yöneticisi
* 2004-2009: Oracle yazılım geliştirme & DBA
* 2000-2004: Progress 4GL yazılım geliştirme & DBA
* 1993-2000: C++ yazılım geliştirme & PervasiveSQL DBA
* 1989-1993: Mainframe yazılım geliştirme
* 1988-1989: QBasic geliştirme

Bu site içerisinde uzun yıllardır bir sürü yerde dağılmış olan bloglarımı toparlayıp bir araya getirdim. Sitede {{ site.categories | size }}
kategoride
{{ site.posts | size }}
gönderi yer alıyor. Siteyi ziyaret edenler şimdiye kadar yaklaşık
<span class="time">{{ total_readtime }}</span>
dakikalarını burada geçirmişler.
{% if featuredcount != 0 %}
Sizin için özellikle dikkat etmenizi istediğim gönderilerime
<a href="{{ site.url }}/featured">{{ featuredcount }}
linkinden erişebilirsiniz.
{% endif %}

<hr>
Bir önceki sitemde yer alan hakkımda bölümünü de kaybolup gitmesin diye buraya ekliyorum. Son 10 yıllık bölüm yok. Son 10 yılı başka bir yazıda uzun uzun anlatmak isterim
<hr>

Selamlar,

2000 yılından beri kişisel bir site olarak host ettiğim bu siteyi elden geçirmek için bir zaman bulmak oldukça güç oldu. Tam 8 sene olmuş. Bu yeni çehresi ile kişisel bilgilerin yanında, blog tabir edilen elektronik günlüklerimi de bu siteden yayınlamaya başlıyorum.

Doğan ZORLU kimdir ne iş yapar derseniz;

* Bilişim meraklısıdır
* Yazılım geliştirmek asli işidir.
* Yazılımların üzerinde koşacağı donanım ve ağ sistemleri de doğal olarak asli iş sınıfındadır.
* Bilişim teknolojilerini, iş alanlarına uygulamak üzere izler.
* Edindiği deneyim ve bilgileri değişik portallarda diğer insanlarla paylaşır. Anlatır ve anlaşılmak ister.
* Kullanılabildiği her yerde Linux kullanır, kullanımın yaygınlaşması için çalışır.
* Kızının engeli nedeni ile tanıştığı OTIZM ile ilgilenir.
* Çocukluktan gelen havacılık sevdasını sanal havacılık ile giderir, IVAO ve VATSIM ağlarında uçar.
* Halk müziği ile uğraşır, bağlama çalar.Tasavvuvla ilgilenir, ney üfler.
diyebilirim.

**Bununla birlikte zaman içinde yaşadığım hayat serüvenini kısaca anlatmak isterim…**

Bolu Gerede’de 1971 yılında doğmuşum. Doğmuşum diyorum zira ben sadece 1974 den sonrasına ait şeyler hatırlıyorum. Üniversiteye kadar kasabanın ilkokulu, ortaokulu ve lisesinde okudum. Hayatımda o zamana kadar pek de değişken olmayan bir düzen vardı.

Aslında herşey 1988 yılında başladı. Okuduğum yüksek öğrenim kurumundan yeni ayrılmıştım ve yapacak birşeyim yoktu. Tekrar üniversitede okumak ve bir lisans eğitimi almak düşüncesiyle çalışırken birden ilçemizde açılan bir bilgisayar kursuyla hayatımın değişeceğini kim bilebilirdi ki ? İlk bilgisayar deneyimlerini kazandığım o kursun hala bende özel bir yeri vardır.

O yıllarda bilgisayar konusu acayip yeni bir konu ülkemizde. (pc ve 512 kb RAM 5.25″ disket sürücü ve DOS 2.0 hayal edin lütfen). Derken o yil sinavlara girip İzmir’de bir üniversiteye giriyorum. Sonuç tatmin edici fakat hala eksik birşeyler var ve bu eksikliğin ne olduğunu üniversiteye başlayınca fark ediyorum. Bir sabah küçük, depo gibi bir yerde 4 tane yeşil monitor ve demirden klavyeleri görünce dalıyorum içeri ve oda ne ? Bunların ne sistem ünitesi var ve nede disket sürücüleri. Acar açmaz bir yazı BAUM ve UserName/Password !!! Haydaa bu nasıl iştir diyor ve başlıyorum kurcalamaya ve ilk MainFrame deneyimlerim de oluşmaya başlıyor bu arada.

Yıllar yılları kovalıyor ve işte buradayım. O yıllardan geriye kalan bir sürü güzel anı ve sevgili eşim. Onunla EARN üzerinde tanışmıştık. Şimdi ne mi yapıyorum ? Değişik projelerde arge, tasarım ve uygulama gibi değişik görevlerde çalışıyorum. MainFrame kültürü almış olmanın verdiği vizyonla (ki ağ denen şey ile oldukça erken tanışmama sebep olmuştur) hep daha büyük ve daha yaygın uygulamalar geliştirme konusunda projeksiyonlarım oldu. Bugün internet/intranet boyutunda web tabanlı uygulamalardan, bölgesel ölçekli veritabanı uygulamalarına kadar geniş bir yelpazede bilgi ve deneyim sahibiyim. Ve geriye dönüp baktıkça, geçen zamana üzülmemek gelmiyor elimden. Zira emek yoğun bir işte çalışıyorum ve teknoloji çok ama çok hızlı gelişiyor.

Her seferinde, ne kadar çok şey öğrenirsem, o kadar az şey bildiğimi fark ediyorum. Tepeye çıktıkça daha uzağı görmek gibi birşey bu.

Geçen zaman içinde ağırlıklı olarak veritabanı ve buna bağlı uygulama yazılımlarının geliştirilmesi konusunda çalıştım. Oldukça değişik sektörlerde çalışma fırsatı buldum. ERP, turizm otomasyonu ve taşımacılık sistemleri gibi. Bir tarafta üretimi yönetirken bir tarafta rezervasyonları yönetmek… Hangi sektöre çalışıyorsanız, o sektörü öğreniyorsunuz başka çaresi yok. Bu işin belki de en büyük getirilerinden birisi bu. Götürdüklerini saymıyorum, zaten pekçok kişi tarafından malum.

Bu sitenin altyapısında WordPress CMS sistemini kullandım. Basit ve kullanışlı bir motor olarak oldukça yararlı oldu.

Hoş geldiniz…
