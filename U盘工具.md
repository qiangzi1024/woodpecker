# WIN10-U盘启动盘复原为普通U盘

1. 使用Cmd打开diskpart
2. 使用list disk找到需要复原的U盘序号
3. 选择该U盘 select disk $id
4. 重置该U盘 clean
5. 使用磁盘管理新建简单卷
