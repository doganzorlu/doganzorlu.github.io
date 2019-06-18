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

# PLATFORM

Yazılım geliştirme işi neredeyse sürekli olarak devam eden bir iştir. Bu nedenle geliştirme yapılacak platformun;

* Hızlı kapanıp açılabilmesi ve mümkünse bunu her durumda yapabilmesi
* İyi bir pil ömrüne sahip olması, pilin ansızın bitmemesi ve idle durumda minimum enerji harcayabilmesi
* Cep telefonu kadar hızlı erişebilir olması 

uzun günler ve geceler boyu çalışacak geliştiriciler için çok ciddi zaman kazandıracaktır. Şahsi olarak sırf donanım stabilitesi nedeni ile Macbook Pro kullanıyorum. Aslında en sevdiğim platform Linux MINT dağıtımının KDE masaüstü sürümü fakat normal notebook platformlarında istediğim performansta bir cihaz bulamadım. (Bir sürü book lar -- Microsoft, Lenovo vs -- da denedim bu arada) Bu tarafta en iyi seçenek SSD takılı bir Windows 10 64bit makine gibi görünüyor.

Her ne kadar kendim Macos kullanıyor olsamda yaygın bir şekilde kullanıldığı için windows makine üzerinde kurulum yapılmasını anlatıyor olacağım. Zaman bulabilirsem eğer Mac ve Linux için de hazırlayabilirim[^1].

## KURULUM

Elimizde temiz kurulmuş, firewall ı aktif, en az bir tane antivirus yüklü ve tüm güncellemeleri yapılmış Windows işletim sistemi olduğu varsayımı ile başlıyoruz. Bu saydıklarım neden önemli ? Geliştiricinin ürettiği kodlar biriciktir. Kaybolması durumunda bir yerden parasıyla bile olsa almak mümkün değildir. Bu nedenle kaybına ya da varsa gizliliğine bir halel gelmesine tahammül edilmez, edilemez.

### İNDİRME LİSTESİ

Kurulum için gerekli olan yazılımların tam listesi burada;

1. [GIT](https://git-scm.com/downloads){:target="_blank"} - Git SCM
2. [VSCODE](https://code.visualstudio.com){:target="_blank"} - VSCode Editör
3. [PYTHON](https://www.python.org/){:target="_blank"} - Python Interpreter
4. [DOCKER](https://www.docker.com/get-started){:target="_blank"} - Docker Container

## SCM

Bu makale ve takip eden tüm yazılım geliştirme ile ilgili yazılarımda SCM den bahsettiğimde bunu lütfen git olarak okuyun. Uzun yıllar SVN kullanmış birisi olarak git in dağıtık mimarisi ve hızı nedeni ile size de önerim bu olacaktır.

SCM, en basit tabiri ile kaynak kod yönetimi yaptığımız yazılımın adıdır. Genellikle bir sunucu ve buna bağlanan işlemciler üzerinden çalışır. Görevi üretilen herbir satır kodu korumak ve tüm ekip tarafından ortak bir çalışma ortamı oluşturmaktır.

İşte download edebileceğiniz yer: [GIT Web Sitesi](https://git-scm.com/downloads){:target="_blank"}

Bu bağlantıdan sisteminize uygun kurulumu yapabilirsiniz. *nix işletim sistemlerinin çoğunda yerleşik olarak geliyor. İndirme sonrası normal bir windows uygulaması kurulumu gibi kurmak yeterli olacaktır. Kurulum uygulaması kendi kendini ortam değişkenlerinden **PATH** içine ekleyecektir. Bu sayede komut satırımdan kullanabilmek için ekstra bir işlem yapılması gerekmemektedir.

Temel birkaç git komutu örneği;

~~~ cmd
Microsoft Windows [Version 10.0.17134.590]
(c) 2018 Microsoft Corporation. Tüm hakları saklıdır.

C:\Users\Dev01> git clone -b https://github.com/doganzorlu/python-course-basic.git
C:\Users\Dev01> git push
C:\Users\Dev01> git pull
C:\Users\Dev01> git add .
C:\Users\Dev01> git commit -m "Test Drive"
~~~

Kullanım ile ilgili detaylara topluluk sitesinin [Dökümanlar](https://git-scm.com/doc) bölümünden ulaşarak detaylı bilgi alınabilir.

## IDE

Entegre geliştirme ortamı olarak VSCode oldukça popüler ve kullanışlı. Alternatif olarak çok beğendiğim atom da kullanılabilir.

İşte download edebileceğiniz yer: [VSCode Web Sitesi](https://code.visualstudio.com/)

![VSCode Web Site Capture](/images/vscode.jpg)

VSCode oldukça yaygın plugin seti ile birlikte kullanılabiliyor. Pluginler ide nin extensions bölümünden eklenip kaldırılabilir. Benim en çok kullandığım pluginleri;

1. GitLens
2. Angular Console
3. Angular Essential
4. KvLang
5. Python
6. Vetur
7. vue
8. YAML

Daha çok üzerinde çalıştığınız projeye bağlı olarak plugin seti değişiyor diyebilirim.

## PYTHON

Development araçları çalışılan projeye, platforma ve yapılacak işe göre seçilmekle beraber bu dökümanda python örneği verilmiştir.

İşte download edebileceğiniz yer: [Python Web Sitesi](https://www.python.org/)

![Python](/images/python.png)

Python çok amaçlı kullanılabileceği oldukça yaygın bir framework ve kütüphane ağına sahiptir. Birkaç örnek vermek gerekirse;

1. django
2. kivy
3. matplotlib
4. pony

Python içerisinde güzel bir kütüphane yönetim aracı geliyor **PIP**.

Packet installer for python adından mülhem bu araçla çok kolay şekilde bir kütüphane kurulup kaldırılabilir. Bir paket kurulacağı zaman;

~~~~ bash
$ pip install Paket
$ pip install Paket==1.1.1
$ pip install Paket>=1.0.0 
$ pip install -r prerequisities.txt
~~~~

şeklinde kullanılabilir. İlk paket in son versiyonunu, ikincisi belirtilen versiyonunu ve üçüncüsü ise en düşük kurulabilir paket sürümünü kullanarak kurulum yapacaktır. Dördüncü seçenek ise prerequisities.txt dosyası içinde yazılı paketleri kuracaktır.

Birkaç komut örneği vermek gerekirse;

**Arama yapmak için:**
~~~~ bash
$ git search "query"
~~~~
query örnekleri için [git search](https://pip.pypa.io/en/stable/reference/pip_search/#pip-search) bakılabilir.

**Paket listesi için:**
~~~~ bash
$ pip list
urllib3                       1.24.1    
virtualenv                    16.2.0    
webencodings                  0.5.1     
wheel                         0.33.1

$ pip show kivy
Name: Kivy
Version: 1.10.1
Summary: A software library for rapid development of hardware-accelerated multitouch applications.
Home-page: http://kivy.org
Author: Kivy Team and other contributors
Author-email: kivy-dev@googlegroups.com
License: MIT
Location: /usr/local/lib/python2.7/site-packages
Requires: pygments, Kivy-Garden, docutils
Required-by:
~~~~

kullanılabilir. Örnekler için [pip list](https://pip.pypa.io/en/stable/reference/pip_list/#pip-list) be [pip show](https://pip.pypa.io/en/stable/reference/pip_show/#pip-show) bölümlerine bakılabilir.

## DOCKER

Docker oldukça popüler bir container platformudur. Windows ve *nix ler için container ları ve/veya platformları desteklemektedir. Orkestrasyon için oldukça gelişmiş araçlar da bu alanda yer bulmaktadır. Örneğin swarm ve çok daha yetenekli kubernates gibi. Standalone bir kurulum acayip kolay olmaktadır. 

İşte download edebileceğiniz yer: [Dockerhub Web Sitesi](https://hub.docker.com/)

![Docker](/images/docker.png)

Docker kurulumu için gereken windows özellikleri otomatik olarak etkinleştirecektir. Kurulum aşamasında birkaç kez restart gerekebilir. Kurulum sonrası;

~~~~bash
$ docker version
Client: Docker Engine - Community
 Version:           18.09.2
 API version:       1.39
 Go version:        go1.10.8
 Git commit:        6247962
 Built:             Sun Feb 10 04:12:39 2019
 OS/Arch:           darwin/amd64
 Experimental:      false

Server: Docker Engine - Community
 Engine:
  Version:          18.09.2
  API version:      1.39 (minimum version 1.12)
  Go version:       go1.10.6
  Git commit:       6247962
  Built:            Sun Feb 10 04:13:06 2019
  OS/Arch:          linux/amd64
  Experimental:     true
~~~~

komutu ile kurulum teyit edilebilir.

~~~~bash
$ docker ps
CONTAINER ID        IMAGE                COMMAND                  CREATED             STATUS              PORTS                                         NAMES
6f564bf9a488        gitea/gitea:latest   "/usr/bin/entrypoint…"   3 weeks ago         Up 2 weeks          0.0.0.0:3000->3000/tcp, 0.0.0.0:222->22/tcp   gitea_server_1
~~~~

yukarıdaki komut ile çalışan container lar görülebilir. Pekçok container bir grup application group olarak çalıştığı için temel docker-compose aracı oldukça işe yaramaktadır.

İşte download edebileceğiniz yer: [Docker-compose download](https://docs.docker.com/compose/install/)

![Docker-compose](/images/docker-compose.png)

bu araç ile oluşturulan konfigürasyon dosyaları ile bir grup konteyner, bunlar arasındaki ağlar ve volume bağlantıları otomatik gerçekleştirilebilir. Örnek bir compose dosyası vermek gerekirse;

~~~~json
version: '3.3'

services:
   db:
     image: mysql:5.7
     volumes:
       - db_data:/var/lib/mysql
     restart: always
     environment:
       MYSQL_ROOT_PASSWORD: somewordpress
       MYSQL_DATABASE: wordpress
       MYSQL_USER: wordpress
       MYSQL_PASSWORD: wordpress

   wordpress:
     depends_on:
       - db
     image: wordpress:latest
     ports:
       - "8000:80"
     restart: always
     environment:
       WORDPRESS_DB_HOST: db:3306
       WORDPRESS_DB_USER: wordpress
       WORDPRESS_DB_PASSWORD: wordpress
       WORDPRESS_DB_NAME: wordpress
volumes:
    db_data: {}
~~~~

yukarıdaki örnek dosya çalıştırılacak olursa;

~~~~bash
$ docker-compose up -d
Creating network "my_wordpress_default" with the default driver
Pulling db (mysql:5.7)...
5.7: Pulling from library/mysql
efd26ecc9548: Pull complete
a3ed95caeb02: Pull complete
...
Digest: sha256:34a0aca88e85f2efa5edff1cea77cf5d3147ad93545dbec99cfe705b03c520de
Status: Downloaded newer image for mysql:5.7
Pulling wordpress (wordpress:latest)...
latest: Pulling from library/wordpress
efd26ecc9548: Already exists
a3ed95caeb02: Pull complete
589a9d9a7c64: Pull complete
...
Digest: sha256:ed28506ae44d5def89075fd5c01456610cd6c64006addfe5210b8c675881aff6
Status: Downloaded newer image for wordpress:latest
Creating my_wordpress_db_1
Creating my_wordpress_wordpress_1
~~~~

benzeri bir sonuç elde edilecektir. Container image leri hub dan indirilip deploy edilmiş olacaktır.

Yazarak anlatmak oldukça zor ve yetersiz. Bununla birlikte base bir kurulum gerçekleştirdik. Artık kodlarımızı yönetebilir ve birer sontainer olarak hazırlayıp deliver edebiliriz. 

Bu başlıkların her birinin detaylı kullanımını önümüzdeki günlerde ayrı birer makale olarak hazırlamayı düşünüyorum.

Kalın sağlıcakla...

*[SSD]: Solid State Disk
[^1]: Kurulumlar birbirine oldukça yakın.



