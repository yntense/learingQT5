

#### 动态链接版本：

1. 找到 windeployqt ，其存在于 ：

   ```
   $DIR\5.12.10\mingw73_64\bin
   ```

2. 将 QT 生成的 release 版本的 .exe文件，复制到一个新的文件夹（如：`C:\Users\cai\Desktop\serial`）下：

3. 执行:

   ```
   windeployqt serial.exe
   
   ```

4. 执行之后将生成，拷贝很多链接库过来，之后在当前环境电脑里打开可用，但是移植到别的电脑就不可用，会缺少很多链接库, 这些链接库都在 `windeployqt ` 所在目录，因此可以根据提示去该目录下寻找链接库，可复制一份出来，以备后续使用。在 win10 下，有缺少如下链接库。

   ```
   libgcc_s_seh-1.dll
   libstdc++-6.dll
   libwinpthread-1.dll
   ```

5. 之后可以用 `Inno Setup Compiler` 制作程序的安装包