# 手动安装MYSQL服务(Install [Mysql](https://dev.mysql.com/doc/refman/8.0/en/windows-extract-archive.html) Manually

## 2.3.4.1 解压缩安装包-Extracting the Install Archive

按照下列步骤手动安装Mysql：
<details>
<summary>Original Text</summary>
To install MySQL manually, do the following:
</details>


If you are upgrading from a previous version please refer to Section 2.11.10, “Upgrading MySQL on Windows”, before beginning the upgrade process.

Make sure that you are logged in as a user with administrator privileges.

Choose an installation location. Traditionally, the MySQL server is installed in C:\mysql. If you do not install MySQL at C:\mysql, you must specify the path to the install directory during startup or in an option file. See Section 2.3.4.2, “Creating an Option File”.

Note
The MySQL Installer installs MySQL under C:\Program Files\MySQL.

Extract the install archive to the chosen installation location using your preferred file-compression tool. Some tools may extract the archive to a folder within your chosen installation location. If this occurs, you can move the contents of the subfolder into the chosen installation location.
