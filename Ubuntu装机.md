
## UEFI-BIOS

### Ubuntu分区

[comment]: <> (Ubuntu引导文件)
1. efi 200M
2. swap 物理内存*2
3. / 20G 可适当放大
4. /home 越大越牛逼

## 双系统时间差

1. Ubuntu把硬件时间当作UTC （版本大于等于16.04）

```shell
timedatectl set-local-rtc 1 --adjust-system-clock
```

2. Windows把硬件时间当作UTC

```shell
Reg add HKLM\SYSTEM\CurrentControlSet\Control\TimeZoneInformation /v RealTimeIsUniversal /t REG_DWORD /d 1
```
