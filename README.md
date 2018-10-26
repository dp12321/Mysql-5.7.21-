# Mysql-5.7.21-
dong_peng_Repertory

### 1.MySQL免安装版，遇到MSVCR120.dll文件丢失错误的解决方案<br>
        在进行mysql zip版本的安装时，遇到以上错误，在网上找了相关的文件拷贝到相应目录下，但还是不行。 
        后来终于找到解决方法：下载 VC redist packages for x64，下载完成，点击运行即可。

        连接：https://www.microsoft.com/en-us/download/details.aspx?id=40784


### 2.安装详细过程<br>
        https://blog.csdn.net/weixin_38201936/article/details/81605640


### 3.bug<br>
         ini.文件中的data目录要建出来


### 4.Path to the database root<br>
        datadir="C:/ProgramData/MySQL/Data/"
        自己要建出来


### 5.改两个地方，一个是my.ini中的两个地址。还有mysql_config.pl文件中的地址内容。



  my $ldata   = 'E:/softInstall2/mysql/data';<br>
  my $execdir = 'E:/softInstall2/mysql/bin';<br>
  my $bindir  = 'E:/softInstall2/mysql/bin';<br>
  my $pkglibdir = fix_path('E:/softInstall2/mysql/lib',"libmysql/relwithdebinfo";<br>
                             "libmysql/release","libmysql/debug","lib/mysql","lib");<br>
  my $pkgincludedir = fix_path('E:/softInstall2/mysql/include', "include/mysql", "include");<br>


## 命令：

安装：mysqld -install

初始化：mysqld --initialize

开始网络：net start mysql / net stop mysql

卸载：mysqld -remove


设置密码：
set password for root@localhost = password('233')


