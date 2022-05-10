# pgadmin3for12
pgadmin3 for postgresql 12


windows10 下编译pgadmin III


​
下载 pgadmin3 源码  https://ftp.postgresql.org/pub/pgadmin/pgadmin3/v1.22.2/src/pgadmin3-1.22.2.tar.gz

下载wxWidgets 源码  https://github.com/wxWidgets/wxWidgets/releases/download/v2.8.12/wxMSW-2.8.12.zip

下载 openssl 开发包 http://slproweb.com/download/Win32OpenSSL-1_0_2t.exe

下载pgsql zip包 https://get.enterprisedb.com/postgresql/postgresql-9.4.25-2-windows-binaries.zip

解压 wxWidgets-2.8.12.tar.gz 到 C:\wxWidgets-2.8.12

设置环境变量WXWIN = C:\wxWidgets-2.8.12

进入C:\wxWidgets-2.8.12\build\msw 选择wx.dsw 用vs2013打开（或vs2010），转换完成后， 选DLL Unicode Realse,然后编译需要模块。

，编译有顺序，需要注意。解决方案添加已存在项目添加C:\wxWidgets-2.8.12\utils下面的hhp2cached和wxrc，转换后，编译。

打开C:\wxWidgets-2.8.12\contrib\build\stc\stc.dsw转换后编译。

打开C:\wxWidgets-2.8.12\contrib\build\ogl\ogl.dsw转换后编译。

wxWidgets-2.8.12编译完成。



安装Win32OpenSSL-1_0_2t.exe，到C:\OpenSSL-Win32

设置环境变量OPENSSL = C:\OpenSSL-Win32



解压pgsql

设置环境变量PGDIR = D:\pgsql


vs2013打开pgadmin3 修改 realse win32编译成功

https://blog.csdn.net/st780206/article/details/103473552


pgadmin\utils\sysSettings.cpp 此文件中设置日志文件 pgadmin.log  路径是home或者文档文件夹





