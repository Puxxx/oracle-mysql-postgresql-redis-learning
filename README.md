# 手动安装MYSQL服务(Install [Mysql](https://dev.mysql.com/doc/refman/8.0/en/windows-extract-archive.html) Manually

## 2.3.4.1 解压缩安装包-Extracting the Install Archive

按照下列步骤手动安装Mysql：
<details>
<summary>Original Text</summary>
To install MySQL manually, do the following:
</details>

1. 如果是旧版本升级，在开始升级之前，请跳转至[2.11.10 章节](https://dev.mysql.com/doc/refman/8.0/en/windows-upgrading.html)查看相关升级知识；
<details>
<summary>Original Text</summary>
If you are upgrading from a previous version please refer to Section 2.11.10, “Upgrading MySQL on Windows”, before beginning the upgrade process.
</details>
2. 确保操作账号为管理角色；
<details>
<summary>Original Text</summary>
Make sure that you are logged in as a user with administrator privileges.
</details>
3. 选择一条安装路径。默认情况下，Mysql服务都是安装在C:\mysql 路径中，如果不想按照默认路径安装，你需要直接指定一个文件夹，或者参考[2.3.4.2 章节](https://dev.mysql.com/doc/refman/8.0/en/windows-create-option-file.html)
<details>
<summary>Original Text</summary>
Choose an installation location. Traditionally, the MySQL server is installed in C:\mysql. If you do not install MySQL at C:\mysql, you must specify the path to the install directory during startup or in an option file. See Section 2.3.4.2, “Creating an Option File”.
</details>

[comment]: <> (注意：MySQL的安装程序会默认安装至C:\Program Files\MySQL中)

<details>
<summary>Original Text</summary>
Note
The MySQL Installer installs MySQL under C:\Program Files\MySQL.
</details>

4. 将压缩包解压至安装目录，一些解压软件会将压缩包的名称作为根目录解压至目标文件中，你可以打开其文件名的文件夹进入子文件后，将此路径作为mysql的安装路径。
<details>
<summary>Original Text</summary>
Extract the install archive to the chosen installation location using your preferred file-compression tool. Some tools may extract the archive to a folder within your chosen installation location. If this occurs, you can move the contents of the subfolder into the chosen installation location.
</details>
