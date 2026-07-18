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
## 二、WSL及GitHub SSH Key下载安装过程常见问题及解决方案
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

### 2.5 问题：直接输入SSH地址提示 No such file or directory
- 原因：把仓库地址当成文件路径执行，语法错误，不能直接粘贴SSH链接运行
- 解决：使用 `git clone 仓库SSH地址` 命令拉取仓库

### 2.6 问题：在 /d/gitcode 执行 git remote 提示 fatal: not a git repository
- 原因：gitcode 是外层文件夹，未进入带 .git 仓库根目录，Git无法识别仓库
- 解决：`cd hoo-repo` 进入克隆生成的仓库文件夹后，再执行remote相关命令

### 2.7 问题：克隆仓库后切换目录才能正常查看远程地址
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
-  1. git add 文件名               #将文件添加到缓冲区        
     git add .                     #把所有文件添加到缓冲区  
-  2. git reset 文件名             #将文件从缓冲区删掉  
-  3. git commit -m "文字说明"     #将文件提交到git   
-  4. git add 忽略文件.gitignore   #在此文件中添加要忽略掉的文件，再上传，此时再 git add . 的时候就不会再提交忽略掉的文件了

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
- **nano : 文本编辑工具，输入nano 文件名，编辑完成后，摁Ctrl+O键，再摁回车键将内容写进文件，再摁Ctrl+X退出编辑**
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
## 四、Python 基础语法（核心语法速通）

### 4.1 变量、常量与数据类型

#### 4.1.1 变量
- 无需声明类型，直接赋值即创建
- 命名规则：字母/下划线开头，区分大小写，避开关键字
- 动态类型：同一变量可被赋值为不同类型

```python
name = "Alice"   # 字符串
age = 25         # 整数
score = 95.5     # 浮点数
is_pass = True   # 布尔值
name = 100       # 合法，变量类型动态改变
```

#### 4.1.2 常量（约定）
- Python 没有真正的常量，用全大写命名表示“不应改变”

```python
PI = 3.14159
MAX_CONNECTIONS = 100
```

#### 4.1.3 基本数据类型

| 类型 | 说明 | 示例 |
|------|------|------|
| `int` | 整数（任意精度） | `42`, `-7`, `0` |
| `float` | 浮点数（双精度） | `3.14`, `-0.5`, `2.0` |
| `bool` | 布尔值 | `True`, `False` |
| `str` | 字符串（不可变序列） | `"hello"`, `'world'` |
| `NoneType` | 空值 | `None` |

#### 4.1.4 类型转换

```python
int("123")        # 123
float("3.14")     # 3.14
str(100)          # "100"
bool(0)           # False（0、空字符串、空列表等为 False）
bool(1)           # True
```

#### 4.1.5 类型检查

```python
type(42)          # <class 'int'>
isinstance(3.14, float)  # True
```

### 4.2 运算符与表达式

#### 4.2.1 算术运算符

| 运算符 | 含义 |
|--------|------|
| `+` | 加 |
| `-` | 减 |
| `*` | 乘 |
| `/` | 除（浮点数） `5 / 2` = `2.5`|  
| `//` | 整除（向下取整）`5 / 2` = `2` |
| `%` | 取余 | 
| `**` | 幂运算 | 

#### 4.2.2 比较运算符（返回布尔值）

| 运算符 | 含义 |
|--------|------|
| `==` | 等于 |
| `!=` | 不等于 |
| `>` | 大于 |
| `<` | 小于 | 
| `>=` | 大于等于 | 
| `<=` | 小于等于 | 

#### 4.2.3 逻辑运算符（短路运算）

| 运算符 | 含义 | 示例 |
|--------|------|------|
| `and` | 与 | `True and False` → `False` |
| `or` | 或 | `True or False` → `True` |
| `not` | 非 | `not True` → `False` |

#### 4.2.4 成员运算符

```python
"a" in "abc"       # True
"x" not in "abc"   # True
3 in [1, 2, 3]     # True
```
#### 4.2.5 身份运算符（与 `==` 的区别）

```python
a = [1, 2]
b = [1, 2]
c = a
a == b      # True（值相等）
a is b      # False（不同对象）
a is c      # True（同一对象）
```

#### 4.2.6 赋值运算符

```python
= += -= *= /=     
```

#### 4.2.7 运算符优先级（从高到低）
1. `**`
2. `+x, -x`（正负号）
3. `* , /, //, %`
4. `+, -`
5. `==, !=, >, <, >=, <=`
6. `not`
7. `and`
8. `or`

> 不确定优先级时，用 `( )` 明确表达意图

### 4.3 输入与输出

#### 4.3.1 `print()` 输出

```python
print("Hello")                    # 自动换行
print(1, 2, 3, sep="-")           # 1-2-3（指定分隔符）
print("Hello", end="")            # 不换行
print("World")                    # HelloWorld（同行输出）  
print('''hhh
ooo''')                           #会直接换行，不用手动输出\n  
print(""" hello                   
world""")                         #用 " 或者 ' 都行
```
    
#### 4.3.2 格式化输出
**1. `%` 占位符**

```python
name = "Alice"
age = 25
print("姓名：%s，年龄：%d" % (name, age))
```

**2. `str.format()` 方法**

```python
print("姓名：{}，年龄：{}".format(name, age))
print("姓名：{n}，年龄：{a}".format(n=name, a=age))
```

**3. f-string（Python 3.6+）**

```python
print(f"姓名：{name}，年龄：{age}")
print(f"年龄×2 = {age * 2}")          # 支持表达式
```
   

#### 4.3.3 `input()` 输入

```python
name = input("请输入你的姓名：")    # 返回字符串
age = int(input("请输入年龄："))    # 需手动转类型
```

### 4.4 流程控制

#### 4.4.1 `if` / `elif` / `else` 条件判断

```python
score = 85

if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"
elif score >= 70:
    grade = "C"
else:
    grade = "D"

print(f"等级：{grade}")
```

#### 4.4.2 三元运算符（条件表达式）

```python
# 语法：值1 if 条件 else 值2
age = 18
status = "成年" if age >= 18 else "未成年"
```

#### 4.4.3 `while` 循环

```python
i = 1
while i <= 5:
    print(i)
    i += 1          # 注意更新条件，避免死循环
```

#### 4.4.4 `for` 循环（遍历可迭代对象）

```python
# 遍历字符串
for ch in "Python":
    print(ch)

# 遍历列表
for item in [1, 2, 3]:
    print(item)

# 使用 range()
for i in range(5):        # 0, 1, 2, 3, 4
    print(i)

for i in range(1, 10, 2): # 1, 3, 5, 7, 9（起始，结束步长）
    print(i)
```

#### 4.4.5 循环控制：`break` / `continue` / `pass`

```python
# break：提前终止循环
for i in range(10):
    if i == 5:
        break
    print(i)          # 输出 0~4

# continue：跳过本次循环
for i in range(5):
    if i == 2:
        continue
    print(i)          # 输出 0,1,3,4

# pass：占位符，什么都不做
if x > 0:
    pass              # 后续再实现
```

#### 4.4.6 `for` / `while` 中的 `else` 子句

```python
# 循环未被 break 中断时，执行 else
for i in range(3):
    print(i)
else:
    print("循环正常结束")    # 会被执行

for i in range(3):
    if i == 1:
        break
    print(i)
else:
    print("循环正常结束")    # 不会执行（被 break 打断）
```

### 4.5 数据结构（容器）

#### 4.5.1 列表（list）—— 可变、有序

```python
# 创建
lst = [1, 2, 3, 4]
empty = []

# 增
lst.append(5)          # [1,2,3,4,5]
lst.insert(0, 0)       # [0,1,2,3,4,5]
lst.extend([6, 7])     # [0,1,2,3,4,5,6,7]

# 删
lst.pop()              # 移除最后一项并返回
lst.pop(0)             # 移除索引0
lst.remove(3)          # 移除第一个值为3的元素
del lst[0]             # 删除索引0

# 改
lst[0] = 100

# 查
lst[0]                 # 索引访问
lst[-1]                # 最后一项
lst[1:4]               # 切片（索引1~3）

# 其他
len(lst)               # 长度
max(lst) / min(lst)    # 最大/最小
sum(lst)               # 求和
sorted(lst)            # 返回新排序列表
lst.sort()             # 原地排序
lst.reverse()          # 反转

# 列表推导式（生成新列表）
squares = [x**2 for x in range(5)]           # [0,1,4,9,16]
evens = [x for x in range(10) if x % 2 == 0] # [0,2,4,6,8]
```

#### 4.5.2 元组（tuple）—— 不可变、有序

```python
# 创建
t = (1, 2, 3)
t2 = 1, 2, 3           # 括号可省略
single = (5,)          # 单元素元组必须有逗号

# 访问（同列表）
t[0]                   # 1
t[-1]                  # 3
t[1:3]                 # (2,3)

# 不可变性
# t[0] = 100           # 报错 TypeError

# 用途：函数返回多个值、作为字典键
a, b, c = t            # 元组解包
```

#### 4.5.3 字典（dict）—— 键值对、3.7+ 有序
```python
字典名.keys()         #返回所有键  
字典名.values()       #返回所有值 
字典名.itms()         #返回所有键值组
```


```python
# 创建
d = {"name": "Alice", "age": 25}
d2 = dict(name="Bob", age=30)

# 增/改
d["city"] = "Beijing"   # 新增
d["age"] = 26           # 修改

# 删
del d["city"]
age = d.pop("age")      # 删除并返回值
d.clear()               # 清空

# 查
d["name"]               # 键不存在会报错 KeyError
d.get("name")           # 键不存在返回 None
d.get("gender", "未知") # 键不存在返回默认值

# 遍历
for key in d:
    print(key, d[key])

for value in d.values():
    print(value)

for key, value in d.items():
    print(key, value)

# 字典推导式
squares_dict = {x: x**2 for x in range(5)}   
```  
#### 4.5.4 类与对象  
- **类** 是创建对象的蓝图或模板。它定义了一组属性和方法。
- **对象** 是根据类创建出来的具体实例。  

  ---  
- 使用 `class` 关键字定义类，使用 `__init__` 方法（构造函数）初始化属性。
   ```python  
  class people:
    #实例初始化方法（构造函数）
    def __init__(self, name, age):
        self.name = name   
        self.age = age  
    #实例方法
    def play(self,参数···)
         print(f"{self.name}在开心的玩")  
   ```  
#### 4.5.5 封装  
- **定义**  
  封装是将对象的内部状态（属性）隐藏起来，仅通过公开的方法（接口）与外界交互。这防止了外部代码直接修改内部数据，保证了数据的安全性和完整性。  
- **公有成员：**   
  默认所有属性和方法都是公有的，可以直接访问。
- **私有成员：**   
  在名称前加`双下划线`__（如 __age），Python 会进行名称修饰（Name Mangling），使其不易被外部直接访问。  
  ```python
  class BankAccount:
    def __init__(self, owner, balance):
        self.owner = owner          # 公有属性
        self.__balance = balance    # 私有属性（名义上保护）
    
    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount
            self.__log_transaction(amount)
    
    def get_balance(self):          # 通过公有方法访问私有属性
        return self.__balance
    
    def __log_transaction(self, amt):  # 私有方法（内部使用）
        print(f"Log: ${amt} deposited.")
  acc = BankAccount("Alice", 1000)
  print(acc.__balance)   # 报错：AttributeError
  print(acc.get_balance()) # 1000
  ```  
- 使用 @property 可以将方法当作属性来调用  
  ```python  
  class Person:
    def __init__(self, name, age):
        self._name = name
        self._age = age
    @property
    def age(self):          # 相当于 getter
        return self._age  
        p = Person("Bob", 25)
  print(p.age)    # 25（调用方法，但像访问属性一样）
  p.age = 30 
  ```
#### 4.5.6 继承  
- 语法：`class Child(Parent):`
- 使用 `super()` 调用父类方法（通常是 `__init__`）。
- 子类可重写父类方法，或新增方法。  
```python  
class Employee:
    def __init__(self,name,id):
        self.name=name
        self.id=id
    def printdetails(self):
        print(f"name:{self.name},id={self.id}")
class PartTimeemployee(Employee):
    def __init__(self,name,id,daily_salay,workdays):
        super().__init__(name,id)
        self.daily_salsry=daily_salay
        self.workdays=workdays
    def cal_slary(self):
        print(f"monthly salary of {self.name} is {self.daily_salsry*self.workdays}")
class Fulltimeemployee(Employee):
    def __init__(self,name,id,month_salay):
        super().__init__(name,id)
        self.month_salsy=month_salay
    def cal_slary(self):
        print(f"monthly salary of {self.name} is {self.month_salsy}")

```  
- **isinstance(obj, Class)：判断 obj 是否是 Class 或其子类的实例。**  
- **issubclass(Sub, Parent)：判断 Sub 是否是 Parent 的子类。**
#### 4.5.7 多态  
- **多态**指不同的对象对同一消息（方法调用）做出不同的响应。它让程序变得更加灵活和可扩展。
- **方法重写**：子类提供与父类同名但逻辑不同的方法。
- **统一调用**：遍历不同类的对象列表，调用相同方法名，自动执行各自逻辑。
### 4.6 文件  
#### 4.6.1 固定流程：
1. **打开文件** → 建立程序与文件之间的连接，获得文件对象。  
   `f = open("文件的相对路径或者是绝对路径","模式，如r/w/a/r+等等")`  
   `with open("文件的相对路径或者是绝对路径","模式，如r/w/a/r+等等") as f:`
2. **读写操作** → 从文件读取数据或将数据写入文件。
3. **关闭文件** → 释放文件资源，确保数据完整写入磁盘。  
   `f.close()`
#### 4.6.2 主要模式  
- **只读（`r`）**：只能读取，文件必须已存在。
- **只写（`w`）**：只能写入，文件不存在则创建，存在则清空原有内容。
- **追加（`a`）**：只能写入，文件不存在则创建，数据追加到末尾。
- **读写模式（`+`）**：可读可写，可与其他模式组合（如 `r+`、`w+`、`a+`）。
---
- **独占创建（`x`）**：写入模式，但要求文件不存在，否则报错。  
- **文本模式（`t`）**：默认模式，处理文本数据，有编码转换。
- **二进制模式（`b`）**：处理二进制数据，不进行编码转换。  
#### 4.6.3 文件指针  
- 文件指针指示当前读写操作的起始位置，是一个整数（字节偏移量）。
- 每次读写操作后，指针会自动后移相应字节数。  
- 获取当前位置：tell()  `pos = f.tell()`
- 移动指针：seek()  `f.seek(0)移动到文件开头的位置`  
- f.write("Hello, World!")
- print(f.read())   #输出文件中的全部内容    
  >read(size=-1) 不传参数或传入 -1，则一次性读取整个文件直到 EOF（文件末尾）  

  >readline(size=-1)  每次只读取一行内容（以换行符 \n 为界）。如果文件结束，返回空字符串 ''。  

  >readlines(hint=-1)   
  >一次性读取文件的所有行，并将它们放入一个列表中。
参数：hint 用于控制读取的行数。默认读取全部。如果指定了 hint，它会读取大约 hint 个字节/字符对应的行数（它不是按行数截断，而是按字节数估算）。
#### 4.6.4 异常错误捕捉  
  <img src="https://s3.bmp.ovh/2026/07/16/qZARpdXv.png" width="350">  


---
## 五、ROS2 学习  
### 5.1 项目创建  
#### 5.1.1 基础学习  
- **节点 ：** 只负责一个单独的模块化的功能（比如一个节点负责控制车轮转动，一个节点负责从激光雷达获取数据、一个节点负责处理激光雷达的数据、一个节点负责定位等等）  
- **节点交互**  
  >-  话题-topics (多对多,异步通信)   发布者、订阅者
  >-  服务-services (一对多,你问我答的同步通信)   客户端，服务端
  >-  动作-Action (一对多,同步通信)
  >-  参数-parameters    
  ---
  >- 节点命令行常用操作
   `$ ros2 node list                  # 查看节点列表 ` 
   `$ ros2 node info <node_name>       # 查看节点信息`   

  >- 话题命令常用操作  
   `$ ros2 topic list                # 查看话题列表 ` 
   `$ ros2 topic info <topic_name>   # 查看话题信息`
   `$ ros2 topic hz <topic_name>     # 查看话题发布频率`
   `$ ros2 topic bw <topic_name>     # 查看话题传输带宽`
   `$ ros2 topic echo <topic_name>   # 查看话题数据`
   `$ ros2 topic pub <topic_name> <msg_type> <msg_data>   # 发布话题消息`   

  >- 服务命令的常用操作  
  `$ ros2 service list                  # 查看服务列表`
  `$ ros2 service type <service_name>   # 查看服务数据类型`
  `$ ros2 service call <service_name> <service_type> <service_data>   # 发送服务请求`  

  >- 接口命令的常用操作 
  `$ ros2 interface list                    # 查看系统接口列表`
  `$ ros2 interface show <interface_name>   # 查看某个接口的详细定义`
  `$ ros2 interface package <package_name>  # 查看某个功能包中的接口定义`   

  >- 动作命令的常用操作  
  `$ ros2 action list                  # 查看服务列表`
  `$ ros2 action info <action_name>    # 查看服务数据类型`
  `$ ros2 action send_goal <action_name> <action_type> <action_data>   # 发送服务请求`
  ---
- **通信接口**
  给传递的数据定义的一个标准结构

  - 话题通信接口的定义使用的是.msg文件
  - 服务通信接口的定义使用的是.srv文件
  - 动作是另外一种通信机制，用来描述机器人的一个运动过程，使用.action文件定义


- **工作空间**      
   
  工作空间是包含若干个功能包的目录，可以把工作空间理解成一个文件夹。这个文件夹包含下有src   

  > 创建工作空间  
  mkdir -p dev_ws/src  
- **功能包**  
  功能包可以理解为存放节点的地方，ROS2中功能包根据编译方式的不同分为三种类型。  
  |功能包|程序类型|  
  |------|--------|  
  |ament_python|python程序|  
  |cmake|C++|  
  |ament_cmake|C++程序,是cmake的增强版|  
  
  创建功能包 : 
  >ros2 pkg create   --build-type  {cmake,ament_cmake,ament_python}  --dependencies <依赖名字>  
  >ros2 pkg create --build-type <build-type> <package_name>
- **pkg**：表示功能包相关的功能；
- **create**：表示创建功能包；  
- **build-type**：表示新创建的功能包是C++还是Python的，如果使用C++或者C，那这里就跟ament_cmake，如果使用 Python，就跟ament_python；  
- **package_name**：新建功能包的名字。  
  ```python  
  ros2 pkg create --build-type ament_cmake learning_pkg_c               # C++
  ros2 pkg create --build-type ament_python learning_pkg_python # Python
  ```
#### 5.1.2 构建流程  
- **创建工作空间**  
  >建立一个项目文件夹   
  <mark>mkdir -p 文件名/src</mark>  
- **创建功能包**  
  >进入src里
  >>- cpp : ros2 pkg create pkg01_hello_cpp --build-type ament_cmake --dependencies rclcpp --node-name hello_node  
  >>- py :  ros2 pkg create pkg02_hello_py --build-type ament_python --dependencies rclpy --node-name hello_node
- **编写源代码**  
    
  **cpp :** 
    |功能|代码|
    |----|-----|  
    |编程接口初始化|rclcpp::init(argc, argv);| 
    |创建节点并初始化|auto node = rclcpp::Node::make_shared("hello_node");|  
    |实现节点功能|RCLCPP_INFO(node->get_logger(), "hello world!");|  
    |销毁节点并关闭接口|rclcpp::shutdown();|

  <img src="https://s3.bmp.ovh/2026/07/14/Cv8HnqBs.png" width="490"> 
   
  **py :**  

   |功能|代码|
    |----|-----|  
    |编程接口初始化|rclpy.init()| 
    |创建节点并初始化|node = rclpy.create_node("helloworld")|  
    |实现节点功能|node.get_logger().info("hello_py")|  
    |销毁节点并关闭接口|rclpy.shutdown()|  

  <img src="https://s3.bmp.ovh/2026/07/15/keCSnQCz.png" width="450">  
- **设置编译规则**  
- **编译与测试**  
  >colcon build  
  - 如果说要构建工作空间下的单独功能包:  
  `colcon build --packages-select 包名`  
  - 如果一个工作空间各个包有某种依赖关系，构建顺序是一定的，也就是说需要先构建一个，然后再构建另一个  
  `就在后构建包的package.xml文件里加上依赖关系：<depend>先构建的包名</depend>`  
  `然后在该工作空间下进行colcon build时，就会先构建一个，再构建另一个`
- **功能运行**  
  >. install/setup.bash (.后有空格)   
  ros2 run pkg01_hello_cpp hello_node (ros2 run 包 节点)  
  <img src="https://s3.bmp.ovh/2026/07/15/MK2XvDgK.png" width="430">  
---  
#### 5.1.3 ros2查看话题的基本信息  
- 1. 列出所有话题，找到目标
 ros2 topic list 
​
- 2. 查看话题基础信息（发布/订阅数量+消息类型）
 ros2 topic info /话题名 (-v)
​
- 3. 查看消息完整结构/定义
 ros2 interface show （消息类型）status_interface/msg/SystemStatus   
  先通过topic info 拿到`消息类型`，也就是 Topic type 后面的内容
​
- 4. 实时打印消息内容
 ros2 topic echo /话题名  
#### 5.1.4 ros2命令行手动发布消息
- **ros2 topic pub --once /话题名 消息类型 "{数据键值对}"**
参数说明：
> 
      --once ：只发1条，去掉会持续循环发消息
    ​
      /话题名 ：你要发布的频道
    ​
     消息类型：你的自定义消息/系统自带消息
    ​
      {} ：里面填你消息里所有字段的值  
#### 5.1.5 ROS2 Python 发布者与订阅者  
- 发布者代码实现  
```python
# 1. 导入 ROS2 基础工具
import rclpy
from rclpy.node import Node
# 导入你自己写的消息类型（就像导入一张特制的信纸）
from status_interface.msg import SystemStatus

# 2. 创建节点类（广播员）
class StatusPublisher(Node):
    def __init__(self):
        # 固定写法：创建节点，名字叫 status_pub
        super().__init__("status_pub")
        
        # 3. 创建发布者
        # 参数1：消息类型 SystemStatus
        # 参数2：话题名字 /sys_status（频道号）
        # 参数3：队列长度 10（如果听众没空听，先存 10 条消息）
        self.publisher_ = self.create_publisher(SystemStatus, "/sys_status", 10)
        # create_publisher(消息类型, 话题名, 队列)

        # 4. 定时器：每隔 1 秒发一次消息
        timer_period = 1.0
        self.timer = self.create_timer(timer_period, self.timer_callback)

    # 定时器回调函数：每 1 秒自动执行，用来发消息
    def timer_callback(self):
        # 5. 创建一张空白消息纸条
        msg = SystemStatus()
        
        # 6. 给纸条填充数据（注意：float 类型必须带 .0）
        ---
        msg.cpu_percent = 15.6
        msg.memory_total = 4040810496.0
        msg.memory_available = 907255808.0
        ---
        
        # 7. 把纸条发送到 /sys_status 话题
        self.publisher_.publish(msg)
        
        # 终端打印日志，方便看有没有发成功
        self.get_logger().info(f"已发送：CPU占用 {msg.cpu_percent}%")

# 程序入口函数
def main(args=None):
    # 初始化 ROS2 系统
    rclpy.init(args=args)
    # 实例化发布节点
    status_pub = StatusPublisher()
    # 循环等待定时器触发，持续运行节点
    rclpy.spin(status_pub)
    # 关闭程序，释放资源
    status_pub.destroy_node()
    rclpy.shutdown()

if __name__ == "__main__":
    main()
```  
- 订阅者代码实现
```python
import rclpy
from rclpy.node import Node
# 导入自定义消息
from status_interface.msg import SystemStatus

class StatusSubscriber(Node):
    def __init__(self):
        # 创建订阅节点，名字 status_sub
        super().__init__("status_sub")
        
        # 1. 创建订阅者
        # 参数1：消息类型
        # 参数2：话题名称（必须和发布者一模一样 /sys_status）
        # 参数3：收到消息后自动执行的回调函数
        # 参数4：队列长度 10
        self.subscription = self.create_subscription(
            SystemStatus,
            "/sys_status",
            self.listener_callback,
            10
        )
        self.subscription  # 防止系统自动回收订阅器，固定写法

    # 收到消息自动触发这个函数，msg 就是收到的完整纸条
    def listener_callback(self, msg):
        # 直接读取消息里的所有数据
        cpu = msg.cpu_percent
        total_mem = msg.memory_total
        free_mem = msg.memory_available
        
        # 终端打印收到的内容
        self.get_logger().info(f"""
        收到设备状态：
        CPU使用率：{cpu}%
        总内存：{total_mem}
        可用内存：{free_mem}
        """)

def main(args=None):
    rclpy.init(args=args)
    status_sub = StatusSubscriber()
    # 循环监听话题，一直等消息过来
    rclpy.spin(status_sub)
    # 退出清理
    status_sub.destroy_node()
    rclpy.shutdown()

if __name__ == "__main__":
    main()
```  
- 如何查看和选择标准消息？
>- 列出所有可用消息：`ros2 interface list --only-msgs`
>- 查看某个消息的具体结构：`ros2 msg show geometry_msgs/Twist`    

| 消息包 | 核心用途 | 典型消息类型 | 使用场景举例 |
| :--- | :--- | :--- | :--- |
| `std_msgs` | 基础数据类型 | `String`, `Int32`, `Float64`, `Bool`, `Header` | 发送简单的调试信息、状态标志、基础数值 |
| `geometry_msgs` | 几何与运动控制 | `Twist`, `Pose`, `Point`, `Quaternion` | 控制机器人移动速度、描述位姿、发送坐标点 |
| `sensor_msgs` | 传感器数据 | `Image`, `LaserScan`, `Imu`, `JointState` | 接收摄像头图像、激光雷达点云、IMU数据 |
| `nav_msgs` | 导航与定位 | `Odometry`, `Path`, `OccupancyGrid` | 发布里程计信息、规划路径、传输地图数据 |
| `visualization_msgs` | 可视化 | `Marker`, `MarkerArray` | 在 RViz 中显示箭头、立方体等调试标记 |<websource>source_group_web_2</websource>


### 5. 遇到的问题  
- 报错  Conflicting values set for option Signed-By  + 疯狂打印PGP密钥块  
  
  <img src="https://s3.bmp.ovh/2026/07/15/GflRhfko.jpg" width="400"> 

  >目录里有 ros2.resources 和 ros2.list 两个文件，冲突了，用sudo rm /etc/apt/sources.list.d/ros2.list 删掉了 ros2.list 就好了  
- AttributeError: 类初始化漏写 super().init("节点名")，节点基础功能缺失  
- PyFloat_Check 浮点崩溃：msg定义float，代码赋值纯整数  
- ros2 run 找不到节点：新开终端没执行 source install/setup.bash