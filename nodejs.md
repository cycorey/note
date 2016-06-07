# oracledb 在windows下的安装
安装visual studio 2015，然后记得执行： `npm config set msvs_version 2015 `。

oracle官网下载并解压 instantclient-basic-windows.x64-12.1.0.2.0.zip， instantclient-sdk-windows.x64-12.1.0.2.0.zip 到 c:\oracle\instantclient

编辑path环境变量，把 c:\oracle\instantclient 放在最前。
在编译cmd命令行窗口中，设置

`set OCI_LIB_DIR=C:\oracle\instantclient\sdk\lib\msvc`

`set OCI_INC_DIR=C:\oracle\instantclient\sdk\include`

然后执行 `npm install -g oracledb`
不报错的话，就说明安装成功了。

# https://github.com/bodyno/react-starter-kit 在windows下的安装

