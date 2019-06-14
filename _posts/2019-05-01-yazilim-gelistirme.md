---
author: doganzorlu
layout: post
title: "YAZILIM GELİŞTİRME"
date: 2019-05-01 20:30
comments: true
category: Eğitim
tags:
- Manisa
- Manisaip
- Development
- Eğitim
- IoT
---

# BAŞLARKEN

Bu makale ile **"Yazılım Geliştirme"** konusunda çalışanların sıfırdan bir geliştirme ortamı nasıl oluşturabileceğini anlatmaya çalışacağım.

Temel olarak;

* SCM
* IDE (Faydalı Pluginleri)
* Python (Çok işe yarayan kütüphaneleri)
* Docker
* Geliştirici DevOps araçları

için kurulum tarif ediyor olacağım.

# İÇİNDEKİLER

1. TOC
{:toc}

# PLATFORM SEÇİMİ

Yazılım geliştirme işi neredeyse sürekli olarak devam eden bir iştir. Bu nedenle geliştirme yapılacak platformun;

* Hızlı kapanıp açılabilmesi ve mümkünse bunu her durumda yapabilmesi
* İyi bir pil ömrüne sahip olması, pilin ansızın bitmemesi ve idle durumda minimum enerji harcayabilmesi
* Cep telefonu kadar hızlı erişebilir olması 

uzun günler ve geceler boyu çalışacak geliştiriciler için çok ciddi zaman kazandıracaktır. Şahsi olarak sırf donanım stabilitesi nedeni ile Macbook Pro kullanıyorum. Aslında en sevdiğim platform Linux MINT dağıtımının KDE masaüstü sürümü fakat normal notebook platformlarında istediğim performansta bir cihaz bulamadım. (Bir sürü book lar -- Microsoft, Lenovo vs -- da denedim bu arada) Bu tarafta en iyi seçenek SSD takılı bir Windows 10 64bit makine gibi görünüyor.

Her ne kadar kendim Macos kullanıyor olsamda yaygın bir şekilde kullanıldığı için windows makine üzerinde kurulum yapılmasını anlatıyor olacağım. Zaman bulabilirsem eğer Mac ve Linux için de hazırlayabilirim. This is a text with a footnote[^1].

<div class="bs-callout bs-callout-danger">
  <h4>WARNING</h4>
  <p><b>Early-adopters</b>: the following steps will <b>NOT</b> work with the currently released Rhinoceros (5.x.x).  You will need to use WIP version of Rhinoceros.</p>
</div>

    1. KURULUM

Elimizde temiz kurulmuş, firewall ı aktif, en az bir tane antivirus yüklü ve tüm güncellemeleri yapılmış Windows işletim sistemi olduğu varsayımı ile başlıyoruz. Bu saydıklarım neden önemli ? Geliştiricinin ürettiği kodlar biriciktir. Kaybolması durumunda bir yerden parasıyla bile olsa almak mümkün değildir. Bu nedenle kaybına ya da varsa gizliliğine bir halel gelmesine tahammül edilmez, edilemez.

        1. İNDİRME LİSTESİ

Kurulum için gerekli olan yazılımların tam listesi burda 

## SCM

Bu makale ve takip eden tüm yazılım geliştirme ile ilgili yazılarımda SCM den bahsettiğimde bunu lütfen git olarak okuyun. Uzun yıllar SVN kullanmış birisi olarak git in dağıtık mimarisi ve hızı nedeni ile size de önerim bu olacaktır.

### Nedir ?

SCM, en basit tabiri ile kaynak kod yönetimi yaptığımız yazılımın adıdır. Genellikle bir sunucu ve buna bağlanan işlemciler üzerinden çalışır. Görevi üretilen herbir satır kodu korumak ve tüm ekip tarafından ortak bir çalışma ortamı oluşturmaktır.

İşte download edebileceğiniz yer: ![Download](/images/monitor-symbol-with-download-down-arrow.png){:height="24px" width="24px"} [GIT Web Sitesi](https://git-scm.com/downloads)


~~~ bash
doganzorlu# ls -lah
~~~

~~~ python

class A:
    def aa(self):
        print ("Test Drive")

~~~

*[SSD]: Solid State Disk
[^1]: Foot note 1



