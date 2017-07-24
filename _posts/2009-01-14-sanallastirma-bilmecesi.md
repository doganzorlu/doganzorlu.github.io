---
author: doganzorlu
layout: post
title: "SANALLAŞTIRMA BİLMECESİ"
date: 2009-01-14 20:30
comments: false
category: SANALLAŞTIRMA
tags:
- SANALLAŞTIRMA
---

x86 tabanlı sistemlerde sanallaştırma, son dönemde kullanım oranı hızla yükselen bir uygulama. Başlangıçta sadece guest bir işletim sistemini çalıştırabilmek sözkonusu iken, gelinen noktada host bir sistem üzerinde mevcut kaynakları paylaşan birden fazla guest sözkonusudur.

Bu ise, özellikle düşük sistem kaynağı tüketen sunucuların tek fiziksel makina üzerine toplanabilmesine olanak sağlamıştır. Temelde;

* Kaynakların birden fazla rol için paylaştırılması
* Kaynakların yönetilmesi
* Hata toleransı için bileşenler barındırması
* Sanal sistemlerin kolaylıkla taşınabilmesi/göç ettirilebilmesi
* Anlık sistem kopyalarının çıkarılabilmesi
