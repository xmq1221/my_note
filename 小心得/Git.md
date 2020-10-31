## Git install and update

### Windows

```language
git update-git-for-windows
```

### Linux

#### Ubuntu
```language
sudo apt-get install git
```
#### bug

升级git出现
```language
The following packages have unmet dependencies:
```

加入source
```language
cd /etc/apt
sudo vi sources.list
```

在 sources.list 中加入(国外的源，需要代理)
```language
deb http://ftp.ca.debian.org/debian/ jessie main contrib non-free
deb-src http://ftp.ca.debian.org/debian/ jessie main contrib non-free

deb http://security.debian.org/ jessie/updates main contrib non-free
deb-src http://security.debian.org/ jessie/updates main contrib non-free

deb http://ftp.ca.debian.org/debian/ jessie-updates main contrib non-free
deb-src http://ftp.ca.debian.org/debian/ jessie-updates main contrib non-free

deb http://ftp.ca.debian.org/debian/ jessie-backports main contrib non-free
```

保存
```language
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install git
```

输出
```language
Reading package lists... Done
Building dependency tree
Reading state information... Done
git is already the newest version (1:2.17.1-1ubuntu0.7).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
```

和现在官网的 2.27.0 不同
添加源
```language
sudo add-apt-repository ppa:git-core/ppa
sudo apt-get update
sudo apt-get install -y git
```

输出版本，可得 2.27.0



#### Git-all
> Git-all contains all sub-packages, whilst Git only includes main components with minimal dependencies.

#### update
```language
sudo add-apt-repository ppa:git-core/ppa
sudo apt update
sudo apt install git
```


### 参考

[Download for Linux and Unix](https://git-scm.com/download/linux)
[Pro Git book](https://git-scm.com/book/en/v2)
[Unable to install git - Unmet dependencies error (Ubuntu 11.10)](https://stackoverflow.com/questions/16820820/unable-to-install-git-unmet-dependencies-error-ubuntu-11-10)
[Difference between installing git vs installing git-all](https://askubuntu.com/questions/796600/difference-between-installing-git-vs-installing-git-all)
[如何在Ubuntu Hardy上升级Git？](https://ubuntuqa.com/article/7916.html)