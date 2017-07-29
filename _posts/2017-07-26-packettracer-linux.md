---
author: doganzorlu
layout: post
title: "Linux Üzerinde PacketTracer"
date: 2017-07-26 20:30
comments: true
category: İşletim Sistemleri
tags:
- Cisco
- Packettracer
- Linux
- MINT
---

Cisco PacketTracer network konusunda çalışanların oldukça fazla kullandıkları bir uygulamadır.

Temel işletim sistemi olarak Linux kullanan birisi olarak bu ürünü doğal olarak bu platformda kullanıyorum. Her kurulumdan sonra eksik library bulup düzeltmekten yorulduğumdan kısa yoldan kurulum sonrası ne yapılacağını burada yazayım istedim. Temel olarak sorun KDE desktop'ta çıkıyor gibi geliyor ama tam da emin değilim. Belki diğer desktop'larda da işe yarıyor olabilir.

Efendim, ana sorun libQTWebkit.so dosyasının kullanılması gerekmesi ve standart kurulumda bunun kullanılamaması olarak karşımıza çıkıyor. Kısa yoldan bu kütüphaneyi alıp bir dizine koymak ve pt startupında da bu dizini kütüphane dizisi göstermek yetiyor.

{% highlight bash %}
mkdir /opt/pt/libwebkit
cp /opt/pt/lib/libQTWebkit.so /opt/pt/libQTWebkit
{% endhighlight %}

Ardından **/opt/pt/packettracer** içerisinde

{% highlight bash %}
export LIB=/opt/pt/libwebkit
{% endhighlight %}

hepi bu kadar. Artık kütüphaneye bağıl bir sorun ortaya çıkmayacaktır.

Not: Bu uygulama Linux MINT 18 KDE distro'sunda gerçeklenmiştir. Ubuntu dağıtımlarında da işe yarayacaktır.
