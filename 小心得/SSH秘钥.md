## 秘钥生成

终端中输入以下指令，**不要设置密码！** 不然会被输密码弄疯了！
```language
ssh-keygen -t rsa -C "xxxxxx@xxxx.com"
```

## Github免密码

将.ssh文件夹中的id_rsa.pub文件里的公钥粘贴到github的SSH keys里即可
