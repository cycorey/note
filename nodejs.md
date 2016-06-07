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
PhantomJS 离线下载好，放在 path 环境变量中；

node-sass， node-gyp 需要注意，是否安装成功【node-sass没安装成功的话，会提示 node-sass\vendor 目录不存在，但实际上它需要找它下面的子目录下的native dll/lib，这时需配好环境变量，执行 npm rebuild node-sass，成功了才可以】
