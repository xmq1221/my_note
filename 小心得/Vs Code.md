# 插件

## Markdown
* markdownlint

## LaTeX 
* LaTeX Workshop

## SSH
* Remote - SSH

## Python
* Python
* Prettier 

# Python

## Flake8

## 环境
在项目目录下下 `.vscode` 文件夹里  `settings.json` 文件，设置 python 路径与是否在终端里自动激活环境
```language
    "python.pythonPath": "/user/bin/python",
    "python.terminal.activateEnvironment": true
```



# Bug

## 无法跳转到定义处
* 删掉服务器用户路径下的这个文件夹
```language
.vscode-server
```
* 删掉vscode客户端以及它所有的设置重装，包括用户文件夹下的
```language
.vscode
```
文件夹，以及用户文件夹下的
```language
AppData\Roaming\Code
```

> 删掉重装解决了，虽然不知为何


