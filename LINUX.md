<!--
 * @Author: Qiang
 * @Date: 2021-04-25 10:41:03
 * @LastEditTime: 2021-10-11 16:46:06
 * @LastEditors: Qiang
 * @Description: 
 * @FilePath: \woodpecker\LINUX.md
-->
# LINUX

## 网卡驱动

1. 驱动目录

   ```shell
   /lib/modules/$(uname -r)/kernel/drivers/net/wireless
   ```

## Windows与Linux的回车换行转换

```shell
最初"\r"（return）表示“回车”即回到行首，“\n”（next）表示“换行”即定位到下一行；UNIX和Linux使用“\n”换行，而Windows用“\r\n”(不是\n\r，已验证)，macOS用“\r”。

Linux文本传到Windows一般少了一个换行；Windows传到Linux的文件，如果是一般文本文档显示正常可不用处理。（这是一般情况，也可能随编缉器的配置而出现别的情况）

但如果是要用来执行的shell脚本，我们会看到显示完全正常语法再三检查也没问题但执行时就是提示“syntax error near unexpected token `do”等错误，这正是回车换行符的原因。
```
 
#### Windows-to-Linux:

```shell
1. sed -i 's/.$//' filename      #.表示不是\n的任意其他字符，$表示行尾匹配；匹配行尾字符不是\n的行，将该字符删除，在我们的上下文中指删除\r
2. sed -i 's/\r$//' filename
```

#### Linux-to-Windows:

```shell
sed -i 's/$/\r/' filename　　#$表示行尾，整句意思是在行尾追加\r
```
