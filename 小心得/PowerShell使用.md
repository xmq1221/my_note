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
[为 Windows PowerShell 设置 User Alias （命令别名）](https://blog.vvzero.com/2019/07/22/set-user-alias-for-windows-PowerShell/)
[【探索PowerShell 】【三】PowerShell下使用Aliases](https://blog.51cto.com/marui/290067)