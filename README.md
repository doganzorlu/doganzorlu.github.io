# PARDUS ppa Repository

To use this repository on your own pardus;

```bash
$ curl -s --compressed "https://doganzorlu.github.io/pardus-ppa/KEY.gpg" | sudo apt-key add -
sudo curl -s --compressed -o /etc/apt/sources.list.d/doganzorlu-pardus.list "https://doganzorlu.github.io/pardus-ppa/doganzorlu-pardus.list"
$ sudo apt update
```