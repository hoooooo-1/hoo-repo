# STUDY PATH  
用于记录和保存学习笔记  
记录人：玉子怡  
时间：2026.7.13--2026.7.25
## 一、markdown
### 1.1 标题
``` 
# 一级标题 (在文本下方添加任意数量的==号来标识一级标题)
## 二级标题(在文本下方添加任意数量的--号来标识一级标题)
### 三级标题  
```
### 1.2 换行
  - 要在一行的末尾加两个或多个空格，然后再按回车键  
### 1.3  粗体  
  - 前后添加两个星号    **hh**
### 1.4 斜体
  - 前后添加一个星号    *hh*  
### 1.5 同时使用**粗体和斜体**
  - 前后各加三个*号   ***hhh***  
### 1.6 引用
  - 在段落前添加一个 > 符号 
>      hello world  
>      hi world  
### 1.7 高亮
  - ```前添加//<mark>号，后添加</mark>号```
  - <mark>哈哈哈哈</mark>   
### 1.8 下划线 
  - <u>下划线</u>
### 1.9 嵌套块引用
  - 要嵌套的段落前添加一个 >> 符号  
>   hello  
>>world  
### 1.10 有序列表
```
    1. First item
    2. Second item
    3. Third item
        1. Indented item
    4. Fourth item
```
### 1.11 无序列表  

>- First item
>- Second item
>- Third item
>    - Indented item  

### 1.12 删除线
  - 在单词前后使用两个波浪号 ~~  
  - ~~hheelllloo~~  
### 1.13 任务列表语法  
  - 在任务列表项之前添加破折号-和方括号[ ]，并在[ ]前面加上空格。要选择一个复选框，请在方括号[x]之间添加 x  
>- [ ] 未完成
>- [x] 已完成 
### 1.14 自动网址链接  
  - 加单引号  
  - 'https://markdown.com.cn/extended-syntax/automatic-url-linking.html'
  - [你是《未来世界的幸存者》么？](https://mp.weixin.qq.com/s/s5IhxV2ooX3JN_X416nidA)  
### 1.15 插入图片  

  <img src="邹而邹之.png" width="210">  

### 1.16 表格  

  | 姓名 | 班级 | 学号 |  
  |------|------|------|  
  |张三|二班|28|  
  |李四|三班|11|  
---- 
### 1.17 数学公式
   - $E = mc^2$ 
   - 
   $$
  \int_{a}^{b} f(x) \, dx = F(b) - F(a)
  -$$  
### 1.18 Callout

> [!NOTE]  
> 这是一个信息提示框

> [!WARNING]
> 这是一个警告提示框

>[!TIP]
>小提示  

>[!CAUTION]
>严重警告  

>[!WARNING]
>警告  
## 二、WSL下载安装过程常见问题及解决方案
### 2.1 Windows功能开启失败
#### 2.1.1 现象
    执行开启虚拟机平台、WSL子系统命令报错；控制面板勾选对应功能无法保存。
#### 2.1.2 解决办法
    右键PowerShell，选择以管理员身份运行再执行启用命令；


### 2.2 WSL系统镜像下载缓慢、中断
#### 2.2.1 现象
    微软商店/`wsl --install`在线下载Ubuntu镜像速度极慢，下载中途断开重复重试。
#### 2.2.2 解决办法
    下载国内离线WSL镜像包，手动导入安装；

### 2.3 wsl命令无法识别
#### 2.3.1 现象
    终端输入wsl提示不是内部或外部命令。
#### 2.3.2 解决办法
    开启WSL相关Windows组件后重启电脑生效；

### 2.4 默认C盘安装，磁盘占用过大
#### 2.4.1 现象
    WSL镜像默认存放C盘，占用大量系统存储空间，无安装路径选择弹窗。
#### 2.4.2 解决办法
    使用`wsl --export`导出镜像、`wsl --import`导入，将子系统迁移至D盘。
---
---
## 三、Linux 入门命令教程  
### 3.1 常见命令  
 
- **echo : 输出**
  >echo -e
  >

- **read : 输入**  
  >read -p 变量名
  >eg. read -p name  
      输入后赋给变量  
---
- **pwd : 打印当前目录** (用于查看自己当前在系统中所处的绝对路径位置)  
- **ls : 列出当前目录下的文件与子目录**  
  >ls 路径（可以查看指定路径下的目录） 
- **cd : 切换或进入指定目录**  
- ---
- **mkdir : 创建新目录**  
- **touch : 创建空文件或更新文件时间**  
- **cat : 一并查看输出文件的全部内容**  
- **less : 分页查看大文件，不会一次性刷屏**  

  |交互快捷键|功能|
  |----------|----|   
  |space(空格键)|下一页|  
  |b|上一页|   
  |q|退出查看|
----
- **head : 默认查看文件的前 10 行**  
  >head -20 text.txt  
  查看指定前20行  
- **tail ： 默认查看文件的最后 10 行**  
  >tail -20text.txt  
  查看最后20行  
---
- **cp : 复制文件**  
  > - cp a.txt b.txt (将 a.txt 复制一份并命名为 b.txt)  
  >- cp -r project backup (复制整个目录,需要加 -r 参数表示递归)
-  **mv : 移动文件到指定目录**    
    >mv test.txt Documents/  
    >mv old.txt new.txt(重命名文件)  
- **rm : 删除文件**  
  >- rm text.txt  
  >- rm -r project (删除目录,需加 -r)  
  >- rm -rf project (强制删除目录及其下所有内容,无提示,非常危险)  
---
- **find : 搜索文件**  
  >- find . -name "*.txt" (在当前目录 . 及其子目录下，查找所有扩展名为 .txt 的文件)  
  >- find . -type f (仅查找普通文件类型)
- **grep ：搜索内容**
  >grep hello test.txt (在 test.txt 文件中搜索包含指定关键词 hello 的文本行)
---
- **查看系统信息** 
  >- whoami : 查看当前登录的用户名称  
  >- date : 查看当前日期与时间  
  >- uname -a : 查看内核版本与完整的系统详细信息  
---

- **软件安装**  
  >- sudo apt update : 更新本地包索引软件源  
  >- sudo apt upgrade : 升级所有已安装的软件包到最新版本  
  >- sudo apt install 软件名 : 安装指定的软件  
  >- sudo apt remove 软件名 : 卸载指定的软件  
---
- **网络命令**  
  > ip addr : 查看本机的网卡及 IP 地址信息  

  > ping www.baidu.com : 测试网络连通性  
  >>Linux 下 ping 会持续进行，可按 Ctrl + C 强行停止  

  > wget https://example.com/file.zip
  >>使用 wget 命令行下载文件  

  >curl -O https://example.com/file.zip  
  >>使用 curl 下载并保存文件  
- **重定向与管道**  
  >ls > list.txt  
  >>输出重定向 >  
  （覆盖模式：将命令结果写入文件，原内容会被清空）  

  >echo hello >> list.txt  
  >>追加重定向 >>  
  （追加模式：在文件末尾新起一行添加内容）  

  >ls | grep txt  
  >>管道 |  
  （将前一个命令的输出结果，作为下一个命令的输入来处理）  
---
- **快捷键**  
  
  |快捷键|功能|  
  | ------ | ---- |  
  |Ctrl + L / clear|	快速清屏 (保持当前状态)| 
  |Ctrl + D|退出当前终端会话 (等同于 exit)|  
  |Tab|	自动补全命令或文件路径 (连按两次列出匹配)|  
  |history|直接控制台打印查看所有的历史执行命令|  
  ---
## 四、GitHub SSH Key 配置问题及解决方法  
4.1 问题：直接输入SSH地址提示 No such file or directory
- 原因：把仓库地址当成文件路径执行，语法错误，不能直接粘贴SSH链接运行
- 解决：使用 `git clone 仓库SSH地址` 命令拉取仓库

4.2 问题：在 /d/gitcode 执行 git remote 提示 fatal: not a git repository
- 原因：gitcode 是外层文件夹，未进入带 .git 仓库根目录，Git无法识别仓库
- 解决：`cd hoo-repo` 进入克隆生成的仓库文件夹后，再执行remote相关命令

4.3 问题：克隆仓库后切换目录才能正常查看远程地址
- 现象：执行 git clone 下载仓库成功，切换到 hoo-repo 目录后 git remote -v 正常输出SSH远程地址  
- 实操图片  
  <img src="https://s3.bmp.ovh/2026/07/14/Vezyea8q.png" width="350">
- 正确流程：
```bash
# 1. 克隆线上仓库到本地
git clone git@github.com:hoooooo-1/hoo-repo.git
# 2. 进入仓库目录
cd hoo-repo
# 3. 查看远程SSH地址，验证绑定成功
git remote -v   
```
---