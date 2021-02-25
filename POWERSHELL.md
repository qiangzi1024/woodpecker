# POWERSHELL

## 代理（PROXY）

- 设置代理
netsh winhttp set proxy http://localhost:8889
- 取消代理
netsh winhttp reset proxy
- 查看代理
netsh winhttp show proxy

## 查找命令版本及路径（与where(Win)、which(Linux)类似)

```shell
Get-Command git
```
