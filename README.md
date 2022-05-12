# PARDUS repository

To use this repository on your own pardus;

```bash
$ curl -s --compressed "https://doganzorlu.github.io/pardus-ppa/KEY.gpg" | gpg --dearmor - > doganzorlu-pardus.gpg
$ sudo install -o root -g root -m 644 doganzorlu-pardus.gpg /etc/apt/trusted.gpg.d/
$ sudo curl -s --compressed -o /etc/apt/sources.list.d/doganzorlu-pardus.list  "https://doganzorlu.github.io/pardus-ppa/doganzorlu-pardus.list"
$ sudo apt update
```