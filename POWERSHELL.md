# POWERSHELL

## 代理（PROXY）

```powershell
# 设置proxy
netsh winhttp set proxy http://localhost:8889
# 取消proxy
netsh winhttp reset proxy
# 查看proxy
netsh winhttp show proxy
```

## 查找命令版本及路径（与where(Win)、which(Linux)类似)

```powershell
Get-Command git
```

## 遍历删除当前文件夹下的文件(cmd)

```shell
del /a /f /s /q  "*.meta"
```
