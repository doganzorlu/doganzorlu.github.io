# PARDUS ppa Repository

To use this repository your own pardus;

```bash

curl -s --compressed "https://${GITHUB_USERNAME}.github.io/my_ppa/KEY.gpg" | sudo apt-key add -
sudo curl -s --compressed -o /etc/apt/sources.list.d/my_list_file.list "https://${GITHUB_USERNAME}.github.io/my_ppa/my_list_file.list"
sudo apt update

```