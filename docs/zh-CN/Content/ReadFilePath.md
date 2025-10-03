# 只读文件路径

_ReadFilePath_ 是 [沙箱配置文件（Sandboxie Ini）](SandboxieIni.md) 中的一个沙箱设置项。它用于指定一系列路径模式，使得对于这些模式所匹配的文件（夹），沙箱软件（Sandboxie）不会对其执行沙箱化隔离（也就是允许沙箱读取的意思），同时不允许写入操作。

可以指定 [Shell 文件夹](ShellFolders.md)；也可以指定 [程序名称前缀](ProgramNamePrefix.md)。

示例：
```ini
   .
   .
   .
   [DefaultBox]
   ReadFilePath=C:\WINDOWS
```

此示例强制规定，C:\WINDOWS 文件夹及其所有子文件夹对于沙箱内的程序是可读的，但不可写入（或删除）。

注意：_ReadFilePath_ 是 [OpenFilePath](OpenFilePath.md) 的一种受限形式。与 _OpenFilePath_ 一样，对于指定文件或文件夹位置中已存在的沙箱内容将被忽略。

相关的 [Sandboxie 经典版控制面板（Sandboxie Control）](SandboxieControl.md) 设置：[沙箱设置 > 资源访问 > 文件访问 > 只读访问](ResourceAccessSettings.md#file-access--read-only-access)

相关的 Sandboxie Plus 设置：沙箱选项 > 资源访问 > 文件 > 添加文件/文件夹 > 访问列 > 只读

