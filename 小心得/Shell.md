# PowerShell

## Windows Terminal 默认 Powershell
打开终端设置文件，将PS的guid填入 **"defaultProfile"**

## 更新
获取版本
```language
Get-Host | Select-Object Version
```

## Alias设置

### 策略
获取与修改策略级别（需要管理员权限）
```language
Get-ExecutionPolicy
Set-ExecutionPolicy Unrestricted
```

### 配置文件
配置文件应该位于
```language
C:\Users\user\Documents\WindowsPowerShell\Microsoft.PowerShell_profile.ps1
```

若无，生成配置文件，重复直到第一句输出为True
```language
test-path $Profile
New-Item -Path $Profile -ItemType file -Force
```
输入别名指令
```language
notepad $Profile
```
例如，在配置文件中输入
```language
function 别名 { 需要替代的命令，可以包含空格 }
```
重新打开PS，生效

### 参考
[Windows PowerShell 配置文件](https://forsenergy.com/zh-cn/windowspowershellhelp/html/9c82251c-6f0d-416a-9c3c-77838218531b.htm)

[为 Windows PowerShell 设置 User Alias （命令别名）](https://blog.vvzero.com/2019/07/22/set-user-alias-for-windows-PowerShell/)

[【探索PowerShell 】【三】PowerShell下使用Aliases](https://blog.51cto.com/marui/290067)

## 美化

### 安装oh-my-posh和posh-git
```language
# 阅读提示，正确选择y和n（会出现不受信任的存储库）
Install-Module posh-git -Scope CurrentUser
Install-Module oh-my-posh -Scope CurrentUser

```
打开配置文件
```language
if (!(Test-Path -Path $PROFILE )) { New-Item -Type File -Path $PROFILE -Force } notepad $PROFILE
```
写入，每次打开PS都生效
```language
Set-Prompt
Get-Theme
# 感觉这个主题最好看
Set-Theme Powerline
```
![PS主题效果](../.local/1593311570.png)

#### 更新oh-my-posh
需要加一个-Force来安装新版
```language
Install-Module -Force -Name oh-my-posh
```


### 安装ScreenFetch
```language
Install-Module windows-screenfetch -Scope CurrentUser
```
打开配置文件（此步骤同上），加入
```language
Screenfetch
```
使用这个打开会变慢，还有bug，先不用了。。。
![screenfetch效果](../.local/1593325708(1).png)

#### BUG
```language
尝试除以零。
所在位置 C:\Users\xmq\Documents\WindowsPowerShell\Modules\windows-screenfetch\1.0.2\Data.psm1:174 字符: 13
+             $FreeDiskPercent = ($FreeDiskSizeGB / $DiskSizeGB) * 100;
+             ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : NotSpecified: (:) [], RuntimeException
    + FullyQualifiedErrorId : RuntimeException

尝试除以零。
所在位置 C:\Users\xmq\Documents\WindowsPowerShell\Modules\windows-screenfetch\1.0.2\Data.psm1:178 字符: 13
+             $UsedDiskPercent = ($UsedDiskSizeGB / $DiskSizeGB) * 100;
+             ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : NotSpecified: (:) [], RuntimeException
    + FullyQualifiedErrorId : RuntimeException
```
screenfetch打开后会出现尝试除以零的bug，但上面的也显示，现在仍是一个bug，未解决

[Zero-sized disks cause divide by zero exception #14](https://github.com/JulianChow94/Windows-screenFetch/issues/14)

### 安装PSColor
```language
Install-Module PSColor -Scope CurrentUser
```
打开配置文件（此步骤同上），加入
```language
Import-Module PSColor
```
#### 参考
[PowerShell 美化指南](https://coolcode.org/2018/03/16/how-to-make-your-powershell-beautiful/)

### 安装更纱黑体
在[Sarasa-Gothic](https://github.com/be5invis/Sarasa-Gothic)下一个安装包安装，在PS的设置里设置一下即可


## 一些有用的脚本

### which
PS无which，配置linux中的which

#### 参考
[几个有用的 PowerShell 脚本](https://coolcode.org/2018/03/19/some-useful-scripts-of-powershell/)

## PS 实用的参考网站

[吴波的博客](https://blog.vichamp.com/)


# Shell

## Zsh

### 设置Zsh为默认Shell
如果不小心把zsh除去了默认了shell（哭了）
找到zsh
```language
which zsh
```
为自己设置默认的shell
```language
chsh -s /user/bin/zsh user
```

### oh-my-zsh

#### 更新
旧版
```language
upgrade_oh_my_zsh
```
 新版更新
```language
omz update
```

就是想把这个复制下来看一下
```language
         __                                     __
  ____  / /_     ____ ___  __  __   ____  _____/ /_
 / __ \/ __ \   / __ `__ \/ / / /  /_  / / ___/ __ \
/ /_/ / / / /  / / / / / / /_/ /    / /_(__  ) / / /
\____/_/ /_/  /_/ /_/ /_/\__, /    /___/____/_/ /_/
                        /____/
```





