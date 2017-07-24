---
author: doganzorlu
layout: post
title: "WINDOWS 7 GENEL BAKIŞ"
date: 2009-01-25 20:30
comments: false
category: İŞLETİM SİSTEMİ
tags:
- Windows 7
---

Microsoft üretimi işletim sistemi kullanıcılarının oldukça büyük bir bölümü, Vista işletim sisteminin yavaşlık ve uyumsuzluk problemleri nedeni ile  XP işletim sistemi ile yoluna devam etmeyi tercih ediyor.

Her ne kadar Microsoft Vista’yı kullandırmak için bastırsa bile (değişik yöntemler deniyor) kullanıcılar çalışma konforlarından taviz vermek istemiyorlar.

Windows 7, aslında Microsoft’un Vista bataklığından bir nevi kurtulma çabası olarak görülebilir. Vista ile ilgili en can alıcı problemler;

* Yavaşlık
* Aygıt sürücü eksikleri

olarak ön plana çıkıyor. Özellikle yavaşlık çok ciddi bir problem. Windows 7 ile bu problemin aşıldığı, biraz daha şekli değiştirilmiş bir arayüze sahip, yeni özellikler eklenmiş bir Vista ile karşılaşılacağını söylemek yanlış olmayacaktır.

Bu makalede test sürümünün internetten indirilip kurulduğu bir makinada, sıklıkla kullanılan uygulamaların test sonuçları, okuyucuya bir fikir verebilmek adına sunulmuştur. Windows 7 ile gelen yenilikler bu makalenin kapsamı dışındadır.

Metod;

Test makinasında kurulu bulunan Windows XP üzerindeki uygulamalar, ikinci bölüme kurulan Windows 7 ye de yüklenip, konfigürasyonları eşitlenmiş ve her iki sistemdeki duraylılıkları incelenmiştir. Performans değerlerinde ölçümler yapılan gözlemlere ve uygulamaların verdiği değerlere göre yapılmıştır.

Kullanılan sistem;

* HP nx6325 AMD Turion x2, 2GB RAM, 40GB disk, notebook
* Windows 7 Test Sürümü Build 7000, 64 bit

Donanım Algılaması;

Texas Intruments Card Reader hariç tüm donanımlar otomatik olarak tanımlandı. Card reader, HP sitesinden bir başka notebook a ait 64bit Vista sürücüsü indirilerek çalıştırıldı. ATI control center tüm denemelere rağmen yüklenemedi. Bununla birlikte ekran kartı sürücüsü çalışıyor. Fakat AA gibi 3D değerleri yönetilemiyor. Çift ekran kullanımında ekranların konumlarını kapatılıp açıldığında kaybediyor. Bunun dışında sorun yok.

Yazılımlar;

* Firefox, sorunsuz
* Total Commander, ana icon grubu görünmüyor. Sistem dizinlerinde işlem yapılmaya kalkıldığında explorer tarafından istenen onay gelmediği için işlem yapılamıyor
* OpenOffice 3.0, sorunsuz
* Lyx 1.5 ve Miktex, sorunsuz
* Inkscape, sorunsuz
* GIMP, sorunsuz
* Python 2.5 ve PyQT, sorunsuz
* MinGW Developer Studio, sorunsuz
* SUPER Multimedia Converter, sorunsuz
* ORACLE 10g Express Edition, sorunsuz
* PHP5 + IIS7, IIS7 içinden 32bit desteği açılmalı, sorunsuz
* Winamp, kurulum sırasında sonic recorder devre dışı bırakılmalı, sorunsuz
* Multimedia CODEC, Win7Codecs adlı 64bit paket FLV hariç pekçok decoder içeriyor. FLV için ayrıca codec gerekiyor, sorunsuz

Bu çalışma sonucunda uyumluluk konusuda, hele hele 64bit bir sistem olarak Windows 7 oldukça başarılı bir profil sergiliyor. Henüz tst aşamasında olduğu gerçeği gözönünde tutulduğunda pencereler için Z-Order takibinde yaşadığı problem gibi ufak tefek problemlerin final sürüme kadar giderileceği düşünülebilir.

Video performansı konusunda, ATI CCC çalıştırılamadığından AA ayarlaması yapılmaksızın yapılan bir testte, XP de 18-22 frame/sec hız sağlanabilen Flight Simulator 2004, Windows 7 de 18-40 aralığında değerler sağlıyor. Genel olarak bakıldığında DirectX uygulamalarında gözle görülür bir performans iyileştirilmesi sözkonusu. Üstelik test platformu DirectX 8 bir kart barındırdığı halde.

Genel performans ise değişkenlik gösteriyor. Kullanıcı talimatlarını cevaplamada bazen çok gecikebiliyor ve hatta bazen yokmuş gibi davranabiliyor. Uygulamaların bekleme durumunda CPU ya getirdiği yük kabul edilebilir düzeyde.

Sonuç;

Windows 7, oluşturduğu kötü şöhreti yüzünden -ki haksız bir şöhret değil- ikinci Windows ME vakası olan Vista’dan sonra Microsoft’u bayağı rahatlatacağa benziyor. Gerek Vista’ya geçmekten korkanlar ve gerekse Vista kullananlar için kısa vadede bile kullanılabilesi bir işletim sistemi olmaya aday olan Windows 7, işletim sistemi dünyasında kendisine iyi bir yer edinebilecek performans ve uyumluluğa sahip.
