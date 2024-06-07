## 科林四阶段高级Linux

### 1.Github

#### 1.github查询关键字

关键字查询 awesome，去此标签类别中查询项目

python tutorial,查询资料，书籍，文档

socket sample，查询对应技术的代码样本

#### 2.github 三要素

##### Repository 仓库

仓库是github项目管理存储基本单位

一个仓库中存储一个项目， 一个用户可以拥有多个仓库，一般仓库分为public，private

##### Commit 提交

程序员在整个开发周期， 有大量的对代码资源的迭代和修改， 都可以通过commit的方式进行记录，便于程序员回溯代码, 即使这些代码被删除，提交便于使用者观察整个工程的开发流程以及设计流程

##### Branch 分支

在仓库中可以包含多个分支，分支才是代码文件的第一存储单位，默认的仓库主分支为master/main

不仅可以管理代码存储， 便于多人协作开发

#### 3.仓库内容

Code，资源存储，代码资源，二进制, 项目管理脚本，许可证等等

issues、使用时遇到的bug 或 进行提交，等待反馈

README，使用markdown语言编写，工程自述文件，开发进度，版本更新使用介绍等等

LICENSE 许可证

GPL2.0,3.0，Apahce2.0,Mit,这些许可证，给使用者最大使用权限以及最少的限制。

#### 4.Git 软件,分布式版本控制系统

仓库管理软件，使用git管理私人代码或企业代码

![image-20240605222804273](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20240605222804273.png)

#### 5.设备认证

##### 1.如何让网站的账户与设备绑定，后续完成代码的管理，上传下载

git init 创建本地仓库						后续对仓库的操作，都要在仓库位置(master)

git config --list //查看git的配置文件

git config --global user.email “邮箱” 配置邮箱

git config --global user.name “name” 配置名字

ssh-keygen -t rsa -C “注册邮箱”//创建本地密文				SSH 远程访问
*去对应的目录查找密文文件

![image-20240606185322806](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20240606185322806.png)

ssh -T git@github.com// 测试关联密钥是否成功

##### 2.为目标仓库起别名， 定位目标仓库， 后续上传

git remote add origin "ssh地址”//为ssh仓库地址创建别名为origin

git remote remove origin //测除origin别名

#### 6.本地设备与云端仓库的交互逻辑

![image-20240606193507034](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20240606193507034.png)

##### 流程如下图所示

![image-20240606193532336](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20240606193532336.png)

git add code.c代表将代码传送到git缓冲区中

git commit -m “first upload” 代表将代码传送到本地仓库并且提交修改说明

git push origin master 将代码传送到云端仓库 如果云端分支和本地仓库主分支名字一样就合并，如果云端仓库和本地仓库主分支名字不一样就再云端仓库新创建一个新分支。

git add  //添加内容

git rm //删除本地文件并删除仓库数据

git restore //回复被删除仓库存在)

#### 7.代码更新的依赖关系被破坏

本地内容要比云端新，完成更新替换，但是如果直接修改云端内容，导致，本地内容无法再次提交

先拉取 git pull 云端内容 与本地内容合并或操作，而后再次推即可

git pull --rebase origin master 吧云端更新的数据拉出来先

git rebase --skip“忽路本地内容 保留云端内容“

git rebase --abort

git rebase --comtinue

#### 8.下载开源代码

git clone "https仓库地址”//下载开源项目code资源，下载的代码直接下载到桌面创建的库文件夹中。

#### 9.分支Branch

关于分支的相关命令， 创建分支、选择分支、 合幷分支等等 

#### 10.Markdown 语言
github可以编写readme，文本修饰语言
![image-20240607193928067](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20240607193928067.png)
![image-20240607194027112](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20240607194027112.png)

Markdown,文本修饰语言

/# 一级标题

/## 二级标题

/### 三级标题

/#### 四级标题

正文内容直接在标题下方写即可

修饰正文中的符号

/**/斜体

/*/* /*/* 粗体

三对就是粗斜体<br>

/~/~ /~/~ 划杠 <br>
