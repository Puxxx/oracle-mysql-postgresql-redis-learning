# 手动安装MYSQL服务(Install MySQL Manually)

## 2.3.4.1 解压缩安装包-[Extracting the Install Archive](https://dev.mysql.com/doc/refman/8.0/en/windows-extract-archive.html)

### 按照下列步骤手动安装Mysql：
1. 如果是旧版本升级，在开始升级之前，请跳转至 [2.11.10 章节](https://dev.mysql.com/doc/refman/8.0/en/windows-upgrading.html) 查看相关升级知识；
2. 确保操作账号为管理角色；
3. 选择一条安装路径。默认情况下，Mysql服务都是安装在C:\mysql 路径中，如果不想按照默认路径安装，你需要直接指定一个文件夹，或者参考[2.3.4.2 章节](https://dev.mysql.com/doc/refman/8.0/en/windows-create-option-file.html) ;
4. 将压缩包解压至安装目录，一些解压软件会将压缩包的名称作为根目录解压至目标文件中，你可以打开其文件名的文件夹进入子文件后，将此路径作为mysql的安装路径。
  * 注意：MySQL的安装程序会默认安装至C:\Program Files\MySQL中。

<details>
<summary>点击查看原文-Original Text</summary>
To install MySQL manually, do the following: </br>
1. If you are upgrading from a previous version please refer to Section 2.11.10, “Upgrading MySQL on Windows”, before beginning the upgrade process.</br>
2. Make sure that you are logged in as a user with administrator privileges.</br>
3. Choose an installation location. Traditionally, the MySQL server is installed in C:\mysql. If you do not install MySQL at C:\mysql, you must specify the path to the install directory during startup or in an option file. See Section 2.3.4.2, “Creating an Option File”.</br>
4. Extract the install archive to the chosen installation location using your preferred file-compression tool. Some tools may extract the archive to a folder within your chosen installation location. If this occurs, you can move the contents of the subfolder into the chosen installation location.</br>
* Note: The MySQL Installer installs MySQL under C:\Program Files\MySQL.
</details>

## 2.3.4.2 [Creating an Option File](https://dev.mysql.com/doc/refman/8.0/en/windows-create-option-file.html)


<details>
<summary>点击查看原文-Original Text</summary>
If you need to specify startup options when you run the server, you can indicate them on the command line or place them in an option file. For options that are used every time the server starts, you may find it most convenient to use an option file to specify your MySQL configuration. This is particularly true under the following circumstances:

* The installation or data directory locations are different from the default locations (C:\Program Files\MySQL\MySQL Server 8.0 and C:\Program Files\MySQL\MySQL Server 8.0\data).

* You need to tune the server settings, such as memory, cache, or InnoDB configuration information.

When the MySQL server starts on Windows, it looks for option files in several locations, such as the Windows directory, C:\, and the MySQL installation directory (for the full list of locations, see Section 4.2.2.2, “Using Option Files”). The Windows directory typically is named something like C:\WINDOWS. You can determine its exact location from the value of the WINDIR environment variable using the following command:

C:\> echo %WINDIR%
MySQL looks for options in each location first in the my.ini file, and then in the my.cnf file. However, to avoid confusion, it is best if you use only one file. If your PC uses a boot loader where C: is not the boot drive, your only option is to use the my.ini file. Whichever option file you use, it must be a plain text file.

Note
When using the MySQL Installer to install MySQL Server, it creates the my.ini at the default location, and the user executing MySQL Installer is granted full permissions to this new my.ini file.

In other words, be sure that the MySQL Server user has permission to read the my.ini file.

You can also make use of the example option files included with your MySQL distribution; see Section 5.1.2, “Server Configuration Defaults”.

An option file can be created and modified with any text editor, such as Notepad. For example, if MySQL is installed in E:\mysql and the data directory is in E:\mydata\data, you can create an option file containing a [mysqld] section to specify values for the basedir and datadir options:

[mysqld]
# set basedir to your installation path
basedir=E:/mysql
# set datadir to the location of your data directory
datadir=E:/mydata/data
Microsoft Windows path names are specified in option files using (forward) slashes rather than backslashes. If you do use backslashes, double them:

[mysqld]
# set basedir to your installation path
basedir=E:\\mysql
# set datadir to the location of your data directory
datadir=E:\\mydata\\data
The rules for use of backslash in option file values are given in Section 4.2.2.2, “Using Option Files”.

The ZIP archive does not include a data directory. To initialize a MySQL installation by creating the data directory and populating the tables in the mysql system database, initialize MySQL using either --initialize or --initialize-insecure. For additional information, see Section 2.10.1, “Initializing the Data Directory”.

If you would like to use a data directory in a different location, you should copy the entire contents of the data directory to the new location. For example, if you want to use E:\mydata as the data directory instead, you must do two things:

Move the entire data directory and all of its contents from the default location (for example C:\Program Files\MySQL\MySQL Server 8.0\data) to E:\mydata.

Use a --datadir option to specify the new data directory location each time you start the server.

