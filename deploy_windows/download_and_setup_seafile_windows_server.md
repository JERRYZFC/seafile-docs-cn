# 下载安装 Windows 版 Seafile 服务器

### 安装 Python 2.7.11 32 位版本

- 下载并安装 [python 2.7.11 32 位版本](http://python.org/ftp/python/2.7.11/python-2.7.11.msi)
- 将 python2.7 的安装路径添加到系统的环境变量中 (PATH 变量)。比如：如果您将 python 2.7.11 安装在`C:\Python27`路径下，那么就将`C:\Python27`添加到环境变量中。

**注意**：一定要使用 Python 2.7.11 32 位版本。64 位版本或不是 2.7.11 的版本不能工作。

### 下载并解压 Seafile 服务器
- 获取 [Seafile 服务器](http://seafile.com/download/)的最新版本。
- 为 Seafile 服务器程序创建一个新的文件夹，比如`C:\SeafileProgram\`。请记住此文件夹的位置，我们将在以后用到它。
- 将**seafile-server_5.0.3_win32.tar.gz**解压到`C:\SeafileProgram\`目录下。

现在，您的目录结构应该像如下这样：
```
C:\SeafileProgram
         |__ seafile-server-5.0.3
```

## 启动与初始化

### 启动 Seafile 服务器

在`C:\SeafileProgram\seafile-server-5.0.3\`文件夹下，找到**run.bat**文件并双击，以启动 Seafile 服务器。此时，您应该注意到 Seafile 服务器的图标已经出现在您的系统托盘中。

### 选择一个磁盘作为 Seafile 服务器数据的存储位置

现在，您可以在弹出的对话框中选择一个磁盘，以便存储 Seafile 服务器的数据：  

- 请确保选择的磁盘拥有足够的剩余空间
- 点击*确认*按钮后， Seafile 将会在您选择的磁盘下为您创建一个名为`seafile-server`的文件夹。这个文件夹就是  Seafile 服务器的数据文件夹。如果您选择*D*盘，那么数据文件夹为`D:\seafile-server`

### 添加管理员帐号

右击 Seafile 服务器的系统托盘图标， 选择"**添加管理员帐号**"选项。在弹出的对话框中输入您的管理员用户名和密码。

如果操作成功， Seafile 服务器托盘图标处会弹出一个气泡提示您"添加 Seahub 管理员账户成功"

### 配置 Seafile 服务器

初始化服务器之后，还需配置以下选项，否则不能进行文件的上传下载:

- 访问服务器的 Web 界面 (打开 `http://<您的 IP 地址>:8000`)，用管理员账号登录
- 点击左上角的扳手图标，进入管理员界面，在进入"设置"标签
- 将**SERVICE_URL**的值配置成`http://<您的 IP 地址>:8000`。比如您的 Windows 服务器地址为 *192.168.1.100*， 那么配置成`SERVICE_URL = http://192.168.1.100:8000`
- 将**FILE_SERVER_ROOT**的值配置成`http://<您的 IP 地址>:8082`。比如您的 Windows 服务器地址为 *192.168.1.100*， 那么配置成`SERVICE_URL = http://192.168.1.100:8082`


## 配置完成

Seafile 服务器的配置到此已经完成。如果您想了解如何使用 Seafile 客户端，请参考 [Seafile 客户端手册](http://www.seafile.com/help/)  

您可能还会想要了解以下信息：  

- [Seafile LDAP配置](../deploy/using_ldap.md)
- [安装 Seafile 为 Windows 服务](install_seafile_server_as_a_windows_service.md)
- [所用端口说明](ports_used_by_seafile_windows_server.md)
- [升级](upgrading_seafile_windows_server.md)
- [个性化配置](../deploy/server_configuration.md)
