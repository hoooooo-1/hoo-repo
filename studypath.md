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
- 编译代码
colcon build --packages-select status_interface status_publisher
- 刷新环境变量（每个新终端都要执行）
source install/setup.bash
- 终端 A：启动发布者（持续发数据）
ros2 run status_publisher sys_status_pub
- 终端 B：启动订阅者（实时接收打印）
ros2 run status_publisher sys_status_sub  


---
- 如何查看和选择标准消息？
>- 列出所有可用消息：`ros2 interface list --only-msgs`
>- 查看某个消息的具体结构：`ros2 msg show geometry_msgs/Twist`    

| 消息包 | 核心用途 | 典型消息类型 | 使用场景举例 |
| :--- | :--- | :--- | :--- |
| `std_msgs.msg` | 基础数据类型 | `StringMsg`, `Int32`, `Float64`, `Bool`, `Header` | 发送简单的调试信息、状态标志、基础数值 |
| `geometry_msgs` | 几何与运动控制 | `Twist`, `Pose`, `Point`, `Quaternion` | 控制机器人移动速度、描述位姿、发送坐标点 |
| `sensor_msgs` | 传感器数据 | `Image`, `LaserScan`, `Imu`, `JointState` | 接收摄像头图像、激光雷达点云、IMU数据 |
| `nav_msgs` | 导航与定位 | `Odometry`, `Path`, `OccupancyGrid` | 发布里程计信息、规划路径、传输地图数据 |
| `visualization_msgs` | 可视化 | `Marker`, `MarkerArray` | 在 RViz 中显示箭头、立方体等调试标记 |<websource>source_group_web_2</websource>
### 5.2 话题——自定义消息（通信接口）
#### 5.2.1 整体流程

1.  新建专门放消息的功能包（`status_interface`）  
   进入工作空间 `src` 目录：

```bash
cd ~/topic_practices_ws/src
ros2 pkg create --build-type ament_cmake status_interface
```  
> **⚠️ 注意**：消息包只能用 `ament_cmake`，不能用 `ament_python`。  

2.  在包内创建 `msg` 文件夹，写 `.msg` 消息文件  
   ```bash
cd status_interface
mkdir msg
cd msg
nano SystemStatus.msg
```  
写入你自定义的数据（示例）：

```text
# 自定义状态消息
int32 cpu_temp
float64 memory_usage
string device_name
bool is_normal
```

保存退出（`Ctrl+O` 回车，`Ctrl+X`）。
3.  修改 `package.xml`、`CMakeLists.txt` 配置编译规则  
   将以下内容添加到文件中：

```xml
<buildtool_depend>rosidl_default_generators</buildtool_depend>
<exec_depend>rosidl_default_runtime</exec_depend>
<member_of_group>rosidl_interface_packages</member_of_group>
```  
修改 `status_interface/CMakeLists.txt`

在文件末尾添加：

```cmake
find_package(rosidl_default_generators REQUIRED)

rosidl_generate_interfaces(${PROJECT_NAME}
  "msg/SystemStatus.msg"
  DEPENDENCIES std_msgs
)

ament_export_dependencies(rosidl_default_runtime)
```
4.  编译消息包  
   回到工作空间根目录：

```bash
cd ~/topic_practices_ws
colcon build --packages-select status_interface
source install/setup.bash
```
5.  在业务包（`status_publisher`）里导入自定义消息使用  
```python
from status_interface.msg import SystemStatus
```
业务包（`status_publisher`）配置依赖，即打开 `status_publisher/package.xml`，添加依赖：

```xml
<depend>status_interface</depend>
```  
#### 5.2.2 信息接口支持的数据类型  

1. 基本类型（标量）

这是编程中常见的底层数据类型，包括：

    布尔值： bool 

    整型： int8 ,  uint8 ,  int16 ,  uint16 ,  int32 ,  uint32 ,  int64 ,  uint64 （分为有符号和无符号）

    浮点型： float32 ,  float64 

    字符串： string （默认 UTF-8 编码）、 wstring （宽字符）

    时间相关： time （时间戳）、 duration （持续时间）

    字符型： char ,  byte  
2.  数组与序列类型

用于存放多个相同类型的数据，支持固定长度和动态长度：
> 动态长度序列（可变数组）：在类型后加  [] ，例如  float32[] ranges  或  string[]  
> 
> 固定长度数组：在类型后加  [N] （N为具体整数），例如  float32 position  或  int32
  
  ---
### 5.3 ROS2 服务通信——客户端与服务端完整实现
- 服务端（Server）：提供特定功能，等待并处理客户端的请求，返回响应结果。
- 客户端（Client）：向服务端发送请求，并等待接收响应。
- 服务接口（Service Interface）：定义请求和响应的数据结构，使用 .srv 文件描述  
#### 5.3.1   自定义服务接口
- **创建服务接口包**
服务接口必须使用 `ament_cmake` 构建类型，与消息接口包类似。

```bash
cd ~/ros2_ws/src
ros2 pkg create --build-type ament_cmake my_service_interface
```
- **编写 .srv 文件**
在包内创建 `srv` 目录，并定义服务文件 `AddTwoInts.srv`。

```bash
cd my_service_interface
mkdir srv
cd srv
touch AddTwoInts.srv
nano AddTwoInts.srv
摁Ctrl+O,回车，Ctrl+X保存
```

文件内容如下，`---` 上方为请求部分，下方为响应部分：

```text
int64 a
int64 b
---
int64 sum
```

- **配置编译规则**

修改 `package.xml`添加以下依赖：

```xml
<buildtool_depend>rosidl_default_generators</buildtool_depend>
<exec_depend>rosidl_default_runtime</exec_depend>
<member_of_group>rosidl_interface_packages</member_of_group>
```

修改 `CMakeLists.txt`在文件末尾添加：

```cmake
find_package(rosidl_default_generators REQUIRED)

rosidl_generate_interfaces(${PROJECT_NAME}
  "srv/AddTwoInts.srv"
)

ament_export_dependencies(rosidl_default_runtime)
```

- **编译服务接口包**
```bash
cd ~/ros2_ws
colcon build --packages-select my_service_interface
source install/setup.bash
```  
#### 5.3.2 服务端代码实现  
```python
import rclpy
from rclpy.node import Node
from my_service_interface.srv import AddTwoInts

class AddTwoIntsServer(Node):
    def __init__(self):
        super().__init__('add_two_ints_server')
        # 创建服务端：接口类型、服务名、回调函数
        self.srv = self.create_service(
            AddTwoInts,
            'add_two_ints',
            self.add_two_ints_callback
        )
        self.get_logger().info('AddTwoInts 服务端已启动')

    def add_two_ints_callback(self, request, response):
        """服务回调函数：处理请求并返回响应"""
        response.sum = request.a + request.b
        self.get_logger().info(f'收到请求: {request.a} + {request.b} = {response.sum}')
        return response  # 必须返回响应对象

def main(args=None):
    rclpy.init(args=args)
    node = AddTwoIntsServer()
    rclpy.spin(node)  # 保持节点运行，持续等待请求
    node.destroy_node()
    rclpy.shutdown()

if __name__ == '__main__':
    main()
```  
#### 5.3.3 客户端代码实现  
```python
import sys
import rclpy
from rclpy.node import Node
from my_service_interface.srv import AddTwoInts

class AddTwoIntsClient(Node):
    def __init__(self):
        super().__init__('add_two_ints_client')
        # 创建客户端：接口类型、服务名
        self.cli = self.create_client(AddTwoInts, 'add_two_ints')
        # 等待服务端上线
        while not self.cli.wait_for_service(timeout_sec=1.0):
            self.get_logger().info('服务端未就绪，等待中...')
        self.get_logger().info('服务端已就绪')

    def send_request(self, a, b):
        """发送异步请求并等待响应"""
        request = AddTwoInts.Request()
        request.a = a
        request.b = b
        # 异步调用服务
        future = self.cli.call_async(request)
        # 阻塞等待响应完成
        rclpy.spin_until_future_complete(self, future)
        return future.result()

def main(args=None):
    rclpy.init(args=args)
    client = AddTwoIntsClient()

    # 从命令行参数获取两个整数
    if len(sys.argv) != 3:
        client.get_logger().error('用法: ros2 run my_service_pkg service_client <a> <b>')
        client.destroy_node()
        rclpy.shutdown()
        return

    a = int(sys.argv)
    b = int(sys.argv)
    response = client.send_request(a, b)

    if response is not None:
        client.get_logger().info(f'结果: {a} + {b} = {response.sum}')
    else:
        client.get_logger().error('服务调用失败')

    client.destroy_node()
    rclpy.shutdown()

if __name__ == '__main__':
    main()
```  
- `wait_for_service()`：客户端启动后需等待服务端上线，避免请求丢失。
- `call_async()`：ROS2 服务调用是异步的，返回一个 `future` 对象。
- `spin_until_future_complete()`：阻塞当前线程直到响应返回，实现同步调用效果。  
#### 5.3.4 业务包配置与编译  
- **创建业务包**
```bash
cd ~/ros2_ws/src
ros2 pkg create --build-type ament_python my_service_pkg \
  --node-name service_server \
  --node-name service_client \
  --dependencies rclpy my_service_interface
```

- **配置 `setup.py`**
确保入口点正确注册：

```python
entry_points={
    'console_scripts': [
        'service_server = my_service_pkg.service_server:main',
        'service_client = my_service_pkg.service_client:main',
    ],
},
```

- **编译业务包**
```bash
cd ~/ros2_ws
colcon build --packages-select my_service_interface my_service_pkg
source install/setup.bash
```  
- **启动服务端**
```bash
ros2 run my_service_pkg service_server
```

- **启动客户端**
```bash
ros2 run my_service_pkg service_client 5 10  
```  
### 5.4 动作通信   
动作通信由三个核心部分构成，对应 `.action` 文件的三个段落：
1.  **目标 (Goal)**：客户端发送给服务端的任务指令（如“移动到坐标 (1.0, 2.0)”）。
2.  **反馈 (Feedback)**：服务端在执行过程中周期性发送给客户端的进度信息（如“当前进度 50%”）。
3.  **结果 (Result)**：任务完成后服务端发送给客户端的最终结果（如“到达目标，耗时 10 秒”）。  
#### 5.4.1 自定义动作接口  
- **创建动作接口包**

动作接口包必须使用 `ament_cmake` 构建类型：

```bash
cd ~/ros2_ws/src
ros2 pkg create --build-type ament_cmake my_action_interface
```

- **编写 .action 文件**

在包内创建 `action` 目录，并定义动作文件 `MoveCircle.action`：

```bash
cd my_action_interface
mkdir action
cd action
touch MoveCircle.action
nano MoveCircle.action
摁Ctrl+O,回车，Ctrl+X保存
```

文件内容如下，使用 `---` 分隔三个部分：

```text
# 目标：是否启用转圈
bool enable
---
# 反馈：当前旋转角度（0-360）
int32 state
---
# 结果：是否成功完成
bool finish
```
- **配置编译规则**
修改 `package.xml`添加以下依赖：
```xml
<buildtool_depend>rosidl_default_generators</buildtool_depend>
<exec_depend>rosidl_default_runtime</exec_depend>
<member_of_group>rosidl_interface_packages</member_of_group>
```

修改 `CMakeLists.txt`在文件末尾添加：

```cmake
find_package(rosidl_default_generators REQUIRED)

rosidl_generate_interfaces(${PROJECT_NAME}
  "action/MoveCircle.action"
)

ament_export_dependencies(rosidl_default_runtime)
```

- **编译动作接口包**

```bash
cd ~/ros2_ws
colcon build --packages-select my_action_interface
source install/setup.bash
```  
#### 5.4.2 业务包配置与编译
- **创建业务包**
```bash
cd ~/ros2_ws/src
ros2 pkg create --build-type ament_python my_action_pkg \
  --dependencies rclpy my_action_interface
```
- **配置 `setup.py`（依据实际代码文件名称书写）**

```python
entry_points={
    'console_scripts': [
        'action_server = my_action_pkg.action_server:main',
        'action_client = my_action_pkg.action_client:main',
    ],
},
```

- **编译业务包**  
```bash
cd ~/ros2_ws
colcon build --packages-select my_action_interface my_action_pkg
source install/setup.bash
```
#### 5.4.3 服务端与客户端代码实现  
- **服务端(模版)**  
```python
import time
import rclpy
from rclpy.node import Node
from rclpy.action import ActionServer
from my_action_interface.action import MoveCircle

class MoveCircleActionServer(Node):
    def __init__(self):
        super().__init__('move_circle_server')
        # 创建动作服务端：接口类型、动作名、执行回调
        self._action_server = ActionServer(
            self,
            MoveCircle,
            'move_circle',
            self.execute_callback
        )
        self.get_logger().info('动作服务端已启动')

    def execute_callback(self, goal_handle):
        """执行收到目标后的处理函数"""
        self.get_logger().info('开始执行转圈任务...')

        # 创建反馈消息对象
        feedback_msg = MoveCircle.Feedback()

        # 模拟转圈过程，每30度发送一次反馈
        for i in range(0, 360, 30):
            # 检查任务是否被取消
            if goal_handle.is_cancel_requested:
                goal_handle.canceled()
                self.get_logger().info('任务被取消')
                return MoveCircle.Result(finish=False)

            # 更新并发送反馈
            feedback_msg.state = i
            self.get_logger().info(f'当前角度: {i}°')
            goal_handle.publish_feedback(feedback_msg)
            time.sleep(0.5)  # 模拟耗时操作

        # 任务成功完成
        goal_handle.succeed()
        result = MoveCircle.Result()
        result.finish = True
        self.get_logger().info('转圈任务完成')
        return result

def main(args=None):
    rclpy.init(args=args)
    node = MoveCircleActionServer()
    rclpy.spin(node)
    node.destroy_node()
    rclpy.shutdown()

if __name__ == '__main__':
    main()
```
- **客户端（模版）**
```python
import rclpy
from rclpy.node import Node
from rclpy.action import ActionClient
from my_action_interface.action import MoveCircle

class MoveCircleActionClient(Node):
    def __init__(self):
        super().__init__('move_circle_client')
        # 创建动作客户端：接口类型、动作名
        self._action_client = ActionClient(
            self,
            MoveCircle,
            'move_circle'
        )
        self.get_logger().info('动作客户端已启动')

    def send_goal(self, enable=True):
        """发送动作目标"""
        # 等待服务端上线
        self._action_client.wait_for_server()

        # 创建目标消息
        goal_msg = MoveCircle.Goal()
        goal_msg.enable = enable

        self.get_logger().info('发送目标...')

        # 异步发送目标，注册反馈和结果回调
        send_goal_future = self._action_client.send_goal_async(
            goal_msg,
            feedback_callback=self.feedback_callback
        )
        send_goal_future.add_done_callback(self.goal_response_callback)

    def goal_response_callback(self, future):
        """目标响应回调：服务端是否接受目标"""
        goal_handle = future.result()
        if not goal_handle.accepted:
            self.get_logger().info('目标被拒绝')
            return

        self.get_logger().info('目标被接受')
        # 注册结果回调
        result_future = goal_handle.get_result_async()
        result_future.add_done_callback(self.result_callback)

    def feedback_callback(self, feedback_msg):
        """反馈回调：接收进度信息"""
        feedback = feedback_msg.feedback
        self.get_logger().info(f'收到反馈: 当前角度 {feedback.state}°')

    def result_callback(self, future):
        """结果回调：接收最终结果"""
        result = future.result().result
        self.get_logger().info(f'任务完成: finish={result.finish}')
        rclpy.shutdown()

def main(args=None):
    rclpy.init(args=args)
    client = MoveCircleActionClient()
    client.send_goal(enable=True)
    rclpy.spin(client)

if __name__ == '__main__':
    main()
```
#### 5.4.5 运行  
- **启动服务端**

```bash
ros2 run my_action_pkg action_server
```

- **启动客户端**

```bash
ros2 run my_action_pkg action_client
```

- **预期输出:**

**服务端终端**：
```
[INFO] 动作服务端已启动
[INFO] 开始执行转圈任务...
[INFO] 当前角度: 0°
[INFO] 当前角度: 30°
...
[INFO] 当前角度: 330°
[INFO] 转圈任务完成
```

**客户端终端**：
```
[INFO] 动作客户端已启动
[INFO] 发送目标...
[INFO] 目标被接受
[INFO] 收到反馈: 当前角度 0°
[INFO] 收到反馈: 当前角度 30°
...
[INFO] 收到反馈: 当前角度 330°
[INFO] 任务完成: finish=True
```  
- **命令行测试**
无需编写客户端代码，可使用 ROS2 内置命令测试动作：
```bash
# 发送目标并查看反馈
ros2 action send_goal /move_circle my_action_interface/action/MoveCircle "{enable: true}" --feedback
```
| 命令部分 | 含义 | 作用 |
| :--- | :--- | :--- |
| `ros2 action send_goal` | 发送动作目标 | 固定命令，告诉 ROS2 你要执行一个动作 |
| `/move_circle` | 动作名称 | 指定要调用哪个动作（必须与服务端注册的名称完全一致） |
| `my_action_interface/action/MoveCircle` | 动作接口类型 | 告诉 ROS2 这个动作的数据结构是什么（用于验证目标格式） |
| `"{enable: true}"` | 目标数据 | 以 YAML 格式传入 Goal 参数（对应 `.action` 文件中 `---` 上方的字段） |
| `--feedback` | 显示反馈 | 可选参数，加上后会实时打印执行过程中的 Feedback 信息 |

### 5.5 参数

ROS2 参数（Parameter）是一种用于**动态配置和管理节点行为**的机制。与话题（Topic）的持续数据流和服务（Service）的请求-响应不同，参数是节点内部的“配置字典”，允许在运行时修改节点设置而无需重新编译或重启。


#### 5.5.1 参数类型

ROS2 支持以下参数类型：

- `bool` / `bool[]`：布尔类型，用于开关控制
- `int64` / `int64[]`：整数类型，用于数值配置
- `float64` / `float64[]`：浮点类型，用于小数配置
- `string` / `string[]`：字符串类型，用于文本配置
- `byte[]`：字节数组，用于图片、点云等二进制数据

#### 5.5.2 命令行工具

ROS2 提供了完整的 `ros2 param` 命令集，用于参数的查询、修改和持久化。

- 列出参数

```bash
# 列出所有节点的参数
ros2 param list

# 列出指定节点的参数
ros2 param list /turtlesim
```

输出示例：
```
/turtlesim:
  background_b
  background_g
  background_r
  use_sim_time
```

- 查看参数详情

```bash
ros2 param describe /turtlesim background_b
```

- 获取参数值

```bash
ros2 param get /turtlesim background_b
```
- 设置参数值

```bash
# 设置单个参数
ros2 param set /turtlesim background_r 150
```

- 导出参数

```bash
# 导出节点参数到 YAML 文件
ros2 param dump /turtlesim > turtlesim_params.yaml
```

生成的 YAML 文件内容：
```yaml
/turtlesim:
  ros__parameters:
    background_b: 255
    background_g: 86
    background_r: 150
    use_sim_time: false
```

- 加载参数

```bash
# 从 YAML 文件加载参数到运行中的节点
ros2 param load /turtlesim turtlesim_params.yaml

# 启动节点时加载参数文件
ros2 run turtlesim turtlesim_node --ros-args --params-file turtlesim_params.yaml
```

- 删除参数

```bash
ros2 param delete /turtlesim background_b
```

####  5.5.3 Python 节点中的参数使用

- **声明与获取参数**

```python
import rclpy
from rclpy.node import Node

class ParameterNode(Node):
    def __init__(self):
        super().__init__('parameter_node')

        # 声明参数：名称、默认值、描述、约束
        self.declare_parameter('robot_name', 'default_robot')
        self.declare_parameter('max_speed', 1.5)
        self.declare_parameter('enable_lidar', True)

        # 获取参数值
        robot_name = self.get_parameter('robot_name').value
        max_speed = self.get_parameter('max_speed').value
        enable_lidar = self.get_parameter('enable_lidar').value

        self.get_logger().info(f'Robot: {robot_name}, Speed: {max_speed}, Lidar: {enable_lidar}')

def main():
    rclpy.init()
    node = ParameterNode()
    rclpy.spin(node)
    node.destroy_node()
    rclpy.shutdown()

if __name__ == '__main__':
    main()
```

- **监听参数变化**

```python
import rclpy
from rclpy.node import Node
from rcl_interfaces.msg import SetParametersResult

class ParameterMonitor(Node):
    def __init__(self):
        super().__init__('parameter_monitor')

        # 声明参数
        self.declare_parameter('log_level', 20)  # INFO level

        # 注册参数回调函数
        self.add_on_set_parameters_callback(self.parameter_callback)

    def parameter_callback(self, params):
        """参数修改回调：验证并处理参数变更"""
        for param in params:
            if param.name == 'log_level':
                # 验证参数范围
                if param.value < 0 or param.value > 50:
                    return SetParametersResult(
                        successful=False,
                        reason='log_level must be between 0 and 50'
                    )
                # 应用新参数
                self.get_logger().set_level(param.value)
                self.get_logger().info(f'Log level changed to {param.value}')

        return SetParametersResult(successful=True)

def main():
    rclpy.init()
    node = ParameterMonitor()
    rclpy.spin(node)
    node.destroy_node()
    rclpy.shutdown()

if __name__ == '__main__':
    main()
```

- 参数回调返回值

>- `SetParametersResult` 用于控制参数修改是否成功：  
>- `successful=True`：参数修改成功
 >  - `successful=False`：参数修改被拒绝，`reason` 字段说明原因

#### 5.5.4 启动文件中的参数配置

- **YAML 参数文件**

创建 `params.yaml`：

```yaml
/robot_controller:
  ros__parameters:
    max_speed: 2.0
    enable_obstacle_avoidance: true
    sensor_topic: "/lidar_scan"
```


- **命令行启动时加载参数**

```bash
ros2 run my_robot_pkg robot_controller --ros-args --params-file params.yaml
```

- **参数组**

```python
# 声明参数组
self.declare_parameter('sensor.ip', '192.168.1.100')
self.declare_parameter('sensor.port', 8080)
self.declare_parameter('sensor.timeout', 5.0)
```

- **跨节点参数访问**

```python
# 从其他节点获取参数
from rclpy.parameter import Parameter

# 创建参数客户端
param_client = self.create_client(
    rcl_interfaces.srv.GetParameters,
    '/other_node/get_parameters'
)

# 发送请求
request = rcl_interfaces.srv.GetParameters.Request()
request.names = ['robot_name']
future = param_client.call_async(request)
```

---


-实战示例

- 启动 Turtlesim

```bash
ros2 run turtlesim turtlesim_node
```

- 查看背景颜色参数

```bash
ros2 param list /turtlesim
# 输出：background_b, background_g, background_r
```

- 修改背景颜色

```bash
# 设置红色通道为 200
ros2 param set /turtlesim background_r 200

# 设置绿色通道为 100
ros2 param set /turtlesim background_g 100

# 设置蓝色通道为 50
ros2 param set /turtlesim background_b 50
```

- 保存配置

```bash
ros2 param dump /turtlesim > background_config.yaml
```

- 恢复配置

```bash
ros2 param load /turtlesim background_config.yaml
```
---
### 5.6 使用launch文件启动多个节点  
- 1. 新建launch文件夹，再该文件夹下新建demo.launch.py文件
   ```
    from launch import LaunchDescription
    from launch_ros.actions import Node

    def generate_launch_description():(名字不可改)
        return LaunchDescription([
            # 在这里添加启动动作
        ])
   ```  
| Action | 作用 | 关键参数 |
| :--- | :--- | :--- |
| `Node` | 启动一个 ROS2 节点 | package, executable, name, namespace, parameters, remappings |
| `IncludeLaunchDescription` | 嵌套包含其他 Launch 文件 | launch_file_source, launch_arguments |
| `DeclareLaunchArgument` | 声明启动参数 | name, default_value, description, choices |
| `SetEnvironmentVariable` | 设置环境变量 | name, value |
| `LogInfo` | 输出日志信息 | msg |
| `TimerAction` | 延迟启动 | period, actions |
| `RegisterEventHandler` | 注册事件处理器 | event_handler (如 OnProcessExit) |

```python
#!/usr/bin/env python3
# ROS2 launch批量启动多节点模板
from launch import LaunchDescription
from launch.actions import DeclareLaunchArgument, ExecuteProcess, GroupAction
from launch_ros.actions import Node
from launch.substitutions import LaunchConfiguration, FindPackageShare
from launch_ros.parameter_descriptions import ParameterFile

def generate_launch_description():
    """
    这个函数是 Launch 文件的唯一入口。
    ros2 launch 命令执行时，会自动调用这个函数，
    并读取它返回的 LaunchDescription 对象来启动所有节点。
    """
    # 1. 定义启动参数
    robot_id_arg = DeclareLaunchArgument(
        "robot_id",   # 参数名
        default_value="01",  # 默认值
        description="机器人编号"  # 描述
    )
    robot_id = LaunchConfiguration("robot_id")

    # 加载yaml参数文件
    params_file = ParameterFile(
        FindPackageShare("your_package") + "/config/params.yaml"
    )

    # 2. 定义多个节点
    # 节点1：雷达驱动
    lidar_node = Node(
        package="your_package",
        executable="lidar_driver",
        name="lidar_node",
        output="screen",
        respawn=True,
        parameters=[params_file, {"lidar_port": "/dev/ttyUSB0"}],
        remappings=[("/scan", ["/", robot_id, "/scan"])]
    )

    # 节点2：图像识别
    camera_node = Node(
        package="your_package",
        executable="camera_detect",
        name="camera_node",
        namespace="camera_group",  # 命名空间
        output="log",
        parameters=[{"img_width": 640}],
        remappings=[("/image_raw", "/camera/image")]
    )

    # 节点3：运动控制
    control_node = Node(
        package="control_pkg",
        executable="move_controller",
        name="control_node",
        output="screen"
    )

    # 启动rviz可视化工具
    rviz = ExecuteProcess(
        cmd=["rviz2", "-d", FindPackageShare("your_package") + "/config/display.rviz"],
        output="screen"
    )

    # 汇总所有要启动的动作/节点
    ld = LaunchDescription()
    ld.add_action(robot_id_arg)
    ld.add_action(lidar_node)
    ld.add_action(camera_node)
    ld.add_action(control_node)
    ld.add_action(rviz)

    return ld
```
- **CMakeLists.txt 配置**  
  ```cmake
  install(
  DIRECTORY launch config
  DESTINATION share/${PROJECT_NAME}/
  )
    ```  
- **启动**
    ```bash
        # 启动
    ros2 launch your_package multi_node.launch.py

    # 传参启动
    ros2 launch your_package multi_node.launch.py robot_id:=02
    ```

### 5. 遇到的问题  
- 报错  Conflicting values set for option Signed-By  + 疯狂打印PGP密钥块  
  
  <img src="https://s3.bmp.ovh/2026/07/15/GflRhfko.jpg" width="400"> 

  >目录里有 ros2.resources 和 ros2.list 两个文件，冲突了，用sudo rm /etc/apt/sources.list.d/ros2.list 删掉了 ros2.list 就好了  
- AttributeError: 类初始化漏写 super().init("节点名")，节点基础功能缺失  
- PyFloat_Check 浮点崩溃：msg定义float，代码赋值纯整数   
- ros2 run 找不到节点：新开终端没执行 source install/setup.bash
- No executable found
  >1.package.xml没有注册  
  >  
  >2.setup.py的entry_points入口配置缺失
  '可执行文件的名字（可以自己起，亦可以与.py文件名字一样）=包名.节点名:main',(在引号后面要加一个逗号)
- 运行ros2 run turtlesim turtlesim_node 时没有可视化界面，捎带其他需要可视化界面的都不可以了 
  ```
  操作步骤:
    1、清空错误显示配置
    
    新开干净终端，只输这两行：
    unset DISPLAY
    echo $DISPLAY
    
    2、修复Qt缺失插件
    sudo apt update
    sudo apt reinstall qtbase5-plugin-platform-xcb libxcb-xkb1  
    3、设置WSLg图形渲染
    
    export QT_QPA_PLATFORM=xcb
    export QT_QPA_PLATFORM_PLUGIN_PATH=/usr/lib/x86_64-linux-gnu/qt5/plugins/platforms
     
    4、完全重启WSL
    
    1. 关掉所有VS Code窗口
    2. 管理员CMD执行：
    
    wsl --shutdown
     
    
    5、重新打开VS Code启动海龟
    pkill -f turtlesim
    ros2 run turtlesim turtlesim_node
    ```  
## 六、c++ 学习  
### 5.1 STL篇  
#### 5.1.1 vector(动态数组)  
```cpp
#include <vector>
vector<int> v;          //只是定义，没有分配内存
vector<int> v(10);      //定义并且分配了10个单位的内存，并且默认都是0
vector<int> v(10,2);        //定义并且分配了10个单位的内存，并且都赋值为2  
v.push_back(data);          // 尾部添加新的数据  
v[2] //随机访问，访问下标为2的数，默认从0开始 
v.erase(v.begin() + 1);  // 删除索引为 1 的元素
v.pop_back();            // 删除尾部元素
v.size();               //获取长度
v.resize();             //分配数组大小

```  
#### 5.1.2 set(集合) 元素互异，自动地按从小到大排 
```cpp
#include <set>  
set <int> p;        //p后不能加东西
p.insert(data);     //添加数据，仍然按照从小到大排
p.erase(2);         //删掉数值为data的数字
p.erase(迭代器);    //删除迭代器指向节点

auto q=p.begin();
q++;(可以q++多次但不能q+=2/3等等)
p.erase(迭代器，迭代器)//删除这个区间内的节点

for(auto l=p.begin();l!=p.end();l++)
        cout<<*l<<" ";  //迭代器
p.find(data)           //在p里面找数值为data的并返回其指针
cout<< (p.find(100) != p.end()) <<endl;//可以用来比较100是否在p里面，如果在，就返回1，否则就返回0
p.size();               //获取长度
---  
unordered_set(区别在不进行排序)
#include<unordered_set>
unordered_set<int>s;
```  
#### 5.1.3 map(键值对) 
自动地按键值对从小到大排
```cpp
#include<map>
map<string ,int>s;(键和值的类型都可以)  
s[键]=值;       //可以修改/赋数值
s["hello"]=1;  //eg.
for(auto i=s.begin();i!=s.end();i++)
        cout<< i->first(键)<<" "<<i->second(值)<<endl;  
s.size();               //获取长度
---  
unordered_map(区别在不进行排序)
#include<unordered_map>
unordered_map<string ,int>s;

```
#### 5.1.4 stack(栈)  
```cpp
#include<stack>
using namespace std;
stack<int>s;    //创建栈
s.push(data);   //压入栈
s.pop();    //出栈
s.top();    //取栈顶
s.size();   //获取长度
```
#### 5.1.5 queue(队列)  
```cpp
#include<queue>
queue<int>s;    //创建队列
s.push(data);       //入队
s.pop();        //出队
s.front();      //访问队首
s.back();       //访问队尾
s.size();   //获取长度
```  
#### 5.1.6 sort(排序)  
```cpp
#include<algorithm>
sort(可以放数组或者是vector)
是vector 的话vector<int>s;
sort(s.begin(),s.end(),cmp)
s.end是s里面最后一个元素的后一个位置[)左闭右开
是数组的话，int []arr;
sort(arr,arr+n,cmp)
cmp是自定义排序函数，如果不写的话默认从小到大排序
bool cmp(int x,int y)
如果返回值为真，那么x放在y前面
cmp返回值部分必须是>/<,而不能是>=/<=
```