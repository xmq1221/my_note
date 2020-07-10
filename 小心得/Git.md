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

在 sources.list 中加入
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

### 参考

[Unable to install git - Unmet dependencies error (Ubuntu 11.10)](https://stackoverflow.com/questions/16820820/unable-to-install-git-unmet-dependencies-error-ubuntu-11-10)