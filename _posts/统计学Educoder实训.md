## 实训一_基础

### 第一关

------

#### 相关知识

 为了完成本关任务，你需要认真学习以下函数：

`mod()`: 用来查看数值类型的函数；[在R_ver3.6中mod()函数无法查看参数类型？？？可以用class()函数代替]

`as.numeric()`: 将数据类型转换为数值型类型的函数；

`as.logical()`: 将数据类型转换为逻辑型类型的函数；

`as.cha\fracter()`: 将数据类型转换为字符型类型的函数。

在我们开始学习`R`语言数据类型之前，先让我们根据例子来看看`3`个简单的概念。

- 定义：按照数据的格式，将数据类型发送给`R`；

  比如定义简单的数值：

![img](https://www.educoder.net/attachments/download/192662)

- 变量与赋值：与其他语言类似，变量是我们操纵数据的载体，而赋值则是数据传递给变量的一个过程。

![img](https://www.educoder.net/attachments/download/192663)

   在`R`语言中，赋值符号有三种，分别如上图所示。大家可以根据自己的喜好选择使用~但是一般来说，大部分人都会选择中间的赋值方式，因为它更为形象。

现在我们正式开始学习`R`语言中的数据类型。

##### 逻辑型数据

逻辑型数据的定义方式很简单，就是直接写上 `TRUE` 或`FALSE`的大写字母即可。

**==注意：R 只认大写的 `TRUE`或`FALSE`。==**

它的运算规则有`3`种，如下图所示：

![img](https://www.educoder.net/attachments/download/192665)

我们可以通过一个例子来加深对`逻辑型数据`及运算规则的理解。

![img](https://www.educoder.net/attachments/download/192666)

从上图的执行过程中，我们能看出`x`实际上应该小于`y`的，所以当我判断`x`大于`y`的时候，你能从右边的`环境变量框`中看见，`z`的值为`FALSE`。

再检验一下，用`mod()`函数来看看`z`现在的数据类型。`WALA!` 结果为`logical`，逻辑型。

最后我们来一条一条执行逻辑型数据的运算规则，看起来很清晰明了吧~

![img](https://www.educoder.net/attachments/download/192667)

##### 数值型数据

`数值型数据`就是我们数学中学过的实数啦，包含正数、`0`和负数。也是我们最容易理解的数据类型了；

其中的“四则运算”，也是我们最熟悉的运算规则啦！我就不在这里多啰嗦了哟。

##### 字符型数据

在`R`中，我们把用`' '`或者`" "`包含起来的数据称为`字符型数据`。

让我们来看看`字符型数据`是什么样子的，以`hello world`为例，嘿嘿。

![img](https://www.educoder.net/attachments/download/192668)

恩，看来没错，`mode()`函数告诉我们，`x`和`y`都是`cha\fracter` `字符型`变量。

##### 数据间的转换

`R`语言数据类型的转换很“显式”，因为它是通过函数做到的，不会出现一不小心就被默认转换坑了的情况，不要问我是怎么知道的…

![img](https://www.educoder.net/attachments/download/192669)

举个例子来看看`逻辑型数据`转成`数值型数据`是怎么做的吧。

![img](https://www.educoder.net/attachments/download/192670)

那么问题来了，`数值型数据`是否能转换为`字符型数据`呢？哈哈，好奇害死猫，我不告诉你，快去自己试试吧。

#### 编程要求

请仔细阅读右侧代码，根据方法内的提示，在Begin - End区域内进行代码补充，具体任务如下：

- 把已有的数据类型转换成另一种数据类型，方法已经告诉你了，开始吧。

#### 测试说明

补充完代码后，点击测评，平台会对你编写的代码进行测试，当你的结果与预期输出一致时，即为通过。

比如`数值型数据`转换为`字符型数据`：输入测试数据：`1`，需要你的程序输出：`"1"`。

你需要输出的结果为：

![img](https://www.educoder.net/attachments/download/193761)

#### My_Answer

```R
#将 “3.14” 赋值给变量 pi，并查看 pi 的数据类型
#注意！是带引号的 3.14
#----start----
pi<-"3.14"
print(class(pi))
#-----end-----


#将 pi 的数据类型转换为数值型，并查看转换后 pi 的数据类型
#注意！是转换后的数据类型
#----start----
pi <- as.numeric(pi)
print(class(pi))
#-----end-----


#将 t 的数据类型转换为数值型,并输出 t 的值
#----start----
t <- 'TRUE'		#t is character 
t <- as.logical(t)		#transfer t to numeric 
t <- as.numeric(t)
print(t)
#-----end-----
```

#### My_Notes 

1. logical类型的数据只有两个值"==TRUE=="和"==FALSE==",并且R语言严格==区分大小写==
2. 查看数据类型的语句为"class(parameter )"

### 第二关

![img](https://www.educoder.net/attachments/download/192637)

#### 相关知识

为了完成本关任务，你需要认真学习以下函数：

`c()`: 用来建立向量的函数；

`seq()`: 该函数用于创建包含`from~end`数值的向量；

`rep()`: 该函数用来创建保存重复值的向量；

`length()`: 用来计算向量长度的函数；

`names()`: 该函数用来对向量各元素命名。

`R`拥有许多用于存储数据的对象类型，包括标量、向量、矩阵、数组、数据框和列表。它们在存储数据的类型、创建方式、结构复杂度，以及用于定位和访问其中个别元素的标记等方面都会有所不同。

![img](https://www.educoder.net/api/attachments/192638)

 是不是感觉在风中凌乱。。。这么多数据结构，都有啥区别呀！看看下图，你也许就会对各种数据结构有一个更直观的印象了。

![img](https://www.educoder.net/api/attachments/192639)

 让我们从向量开始，逐个探究每一种数据结构吧。

##### 向量

![img](https://www.educoder.net/api/attachments/193064)

`向量`是用于存储数值型、字符型或逻辑型数据的`一维数组`。我们可以用函数`c()`来创建向量。比如：

```
a <- c(1,2,3,4,6,7,9,0)
b <- c("哎","哟","喂")
c <- c(TRUE, TRUE, TRUE,TRUE)
```

![img](https://www.educoder.net/attachments/download/192658)

仔细看看，发现了什么？

怎么每一个向量中的数据好像都是相同类型的？没错没错！记住！

> ==同一向量中无法混杂不同模式的数据==！

`:`运算符是向量常用的运算符，它是给懒人发明的~为什么这么说呢？

看看下边的例子吧。

![img](https://www.educoder.net/api/attachments/192646)

哦哟哟，勤快的人敲的好辛苦，懒懒的人一个冒号就搞定了！

But！！`:`运算符有个致命缺点，那就是一次只能跳一步。

怎么办？我教你一个放飞自我随意设定步长的方法吧。

用函数`seq()`：

`seq()`有两个参数，分别是`by` 和 `length.out`。`by`参数用来设定步长，而`length.out`参数是用来设定数据段的“块数”的。

```
seq(2, 8, by = 1)
seq(3, 15, length.out = 5)
```

让我们来看看它怎么用。

![img](https://www.educoder.net/api/attachments/192659)

注意！对于`seq()`函数，不能设置这样步数的递减：

```
seq(10, 9.5, by=0.1)
```

![img](https://www.educoder.net/attachments/download/192658)

只能这样递减：

```
seq(10, 9.5, by=-0.1)
```

最后一个`seq()`函数

```
seq(10, 1, length.out = 5)
```

给我们返回了`5`个数值`10.00  7.75  5.50  3.25  1.00`，他们的步长是 `-2.25`。

看出来了吧，`R`可以均匀的帮我们按`length.out`的值把数值切开。

还有一个让向量操作更方便的函数，叫`rep()`函数，它就像我们的赋值粘贴功能，让你的向量想复制多少次，就复制多少次。

```
rep(c('男神大人'), 3)
"男神大人" "男神大人" "男神大人"
rep(c(1:3), 4)
1 2 3 1 2 3 1 2 3 1 2 3
```

其实，向量之间也是可以运算的。比如下面这样：

![img](https://www.educoder.net/attachments/download/192660)

两个向量长度相等时，向量间的运算是相应位置的数字进行运算，运算后结果返回原位置。

但如果长度不相等呢？看看~警告我们了。

> Warning message:长的对象长度不是短的对象长度的整倍数

哈哈，我们无视警告~因为。。。它还是老老实实算出来了。看下图就明白了！

原来，我们的短向量，被硬生生拉长了，难为它了。

![img](https://www.educoder.net/attachments/download/192661)

最后，对于向量化计算，还有一个原则就是，**避免使用`for`循环**。为什么这么说呢，因为`for`循环会有明显效率不足的缺点。执行起来比向量化计算的方法慢得多。`for`循环我们以后会讲到。

###### 如何访问向量中的数据

通过在`[]`中给出元素所在位置的数值，我们就可以访问向量中的元素了哟，给你们总结下，有4种访问方式，看下图：

![img](https://www.educoder.net/api/attachments/193024)

示例如下：

![img](https://www.educoder.net/api/attachments/193042)

###### 向量中常用的函数

1. 当向量非常长，我们又想知道向量长度的时候，你可以用`length()`函数来统计向量长度。比如：

```
x <- c("a", "b", "c")length(x)
```

将会返回`3`。

1. 我们还可以对向量中各元素进行命名：

![img](https://www.educoder.net/api/attachments/193067)

![](/api/attachments/193067)

当然我们也可以使用元素的名称访问向量中的元素。

![img](https://www.educoder.net/api/attachments/193068)

与命名元素类似，我们也可以使用`names()`函数来查看向量中某个指定元素的名称。例如：

```
names(x) [2]
```

查看向量第二个元素的名称，输出为`"seo"`。

#### 编程要求

请仔细阅读右侧代码，根据方法内的提示，在Begin - End区域内进行代码补充。

#### 测试说明

补充完代码后，点击测评，平台会对你编写的代码进行测试，当你的结果与预期输出一致时，即为通过。

你需要输出的结果为：

![img](https://www.educoder.net/api/attachments/193744)

#### My_Answer

```r
a <- c('你', '不是', '女王大人','他', '是', '好宝宝')
#----start----
#请用length函数计算向量a的长度
print(length(a))

#请输出“女王大人”
print(a[3])

#请输出“你” “是” “好宝宝”
print(a[c(1,5,6)])

#既然是好宝宝了，请使用rep函数，叫我三声“女王大人”
print(rep(a[3],3))

#请为向量a的每个元素命名，名称依次为1，2，3，4，5，6，并输出a
names(a) <- c(1,2,3,4,5,6)
print(a)
#使用seq函数，将1~100分成8个元素的等差数列
print(seq(1,100,length.out=8))
#-----end-----
```

### 第三关

![img](https://www.educoder.net/attachments/download/192637)

#### 相关知识

为了完成本关任务，你需要认真学习以下函数：

`matrix()`: 用来建立矩阵的函数；

`nrow()`:求矩阵的行数；

`ncol()`: 求矩阵的列数；

`dim()`: 求对象的维数；

`t()`: 求矩阵的转置矩阵；

`solve()`: 从方程`a%*%x = b`中求`x`。若不指定`b`， 则求`a`的逆矩阵。

##### 矩阵

![img](https://www.educoder.net/api/attachments/193093)

`R`中的矩阵与数学中的矩阵一样，由指定的行`（row）`与列`（column）`构成。

> 和向量一样，矩阵也只能保存同种数据类型的数据。

比如矩阵中的所有元素可以都是数值型的，但不能“第一列是数值、第二列是字符串”。

**创建矩阵：**

![img](https://www.educoder.net/api/attachments/193114)

那我们先来举个例子，看看最基本的矩阵怎么创建吧。

![img](https://www.educoder.net/api/attachments/193115)

大家可以看见，我给出了矩阵值和行数，`R`就能按列填充出一个矩阵出来~

> 我们给出的数据个数，要**等于**想要建立矩阵的元素个数才可以。

不然会出现上图所提示的错误哟。

没有行名和列名看上去实在是不爽，我们可以使用函数`rownames()`和`colnames()`为矩阵指定行名和列名。比如指定行名：

上图中可以看见，当没有行名时，我们用`rownames()`查看行名，会返回`NULL`。

![img](https://www.educoder.net/api/attachments/193251)

###### 如何访问矩阵中的数据

借助**`索引`**或**`行名`**与**`列名`**，就可以访问矩阵中的数据。

![img](https://www.educoder.net/api/attachments/193269)

在这里举个简单的例子，仔细琢磨哟，通过`行名`与`列名`访问和通过`索引向量`访问我们会放在练习中。

![img](https://www.educoder.net/api/attachments/193305)

与向量类似哟，如果索引是负数，则表示排除指定行或列；若索引为向量，则可以从矩阵中一次获取多个值。若想获取整行或整列，只要在指定行或列的位置上不写索引即可。

矩阵与标量、矩阵与矩阵间的四则运算如下表所示：

![img](https://www.educoder.net/api/attachments/193320)

比如：

![img](https://www.educoder.net/api/attachments/193323)

###### 矩阵中常用的函数

除了简单的四则运算，矩阵还有特殊的运算需要函数来帮忙。

1. 我们用`t()`函数来求矩阵的转置矩阵；
2. 我们用`solve(a, b)`函数来为方程 `a %*% x = b`求解。其中 `a`为矩阵，`b`为向量或矩阵；

> 若不指定`b`，则求 `a`的逆矩阵。

1. 我们用`nrow()`函数来求矩阵的行数；
2. 我们用`ncol()`函数来求矩阵的列数；
3. 我们用`dim()`函数来求矩阵的维数，当然也可以用它来设置矩阵维数。比如：

![img](https://www.educoder.net/api/attachments/193326)

#### 编程要求

请仔细阅读右侧代码，根据方法内的提示，在`Begin - End`区域内进行代码补充。

#### 测试说明

补充完代码后，点击测评，平台会对你编写的代码进行测试，当你的结果与预期输出一致时，即为通过。

你需要输出的结果为：

![img](https://www.educoder.net/api/attachments/193745)

#### My_Answer

```r
#----start----

#创建3*3矩阵x，包含元素c(1,3,4,2,-9,4,7,0,8)，并输出x
x<-matrix(c(1,3,4,2,-9,4,7,0,8),nrow = 3)
print(x)

#获取第一行、第三行与第1列、第三列数据的交集
print(matrix(c(x[1,1],x[3,1],x[1,3],x[3,3]),nrow=2))

#为矩阵x的行和列设置名称,并输出x
#行名分别为“Lisa”“Bob”“Jay”
#列名分别为“成绩1”“成绩2”“成绩3”
rownames(x)<-c("Lisa","Bob","Jay")
colnames(x)<-c("成绩1","成绩2","成绩3")
print(x)
#请使用行名、列名查出Bob的成绩2
print(x["Bob","成绩2"])

#使用solve()函数，求指定矩阵的逆矩阵
#然后使逆矩阵与原矩阵相乘，查看得到的结果是否为单位矩阵
x <- matrix(c(1, 2, 3, 4),ncol=2)
y<-solve(x)
print(y)
print(x%*%y)

#将3*2的矩阵x改为2*3，并输出矩阵x
x <- matrix(c(1,3,4,2,-9,4), ncol=2)
dim(x)<-c(2,3)
print(x)
#-----end-----
```

#### My_Notes

1. matrix(para1，para2)函数的第一个参数必须是向量，第二个参数可以使行数，也可以是列数
2. solve(parameter1，parame2)函数，，其中para1是矩阵，para2是向量或者矩阵。如果只有para1没有para2，则函数的function是求para1的逆矩阵。
3. 两个矩阵相乘的运算符是"%*%"，矩阵一一对应的元素相乘的运算符是" * "
4. 为矩阵的行列进行命名的方法是"rownames(矩阵变量名)<-c("name1","name2",......)     colnames(矩阵变量名)<-c("name1","name2",......)"
5. 提取矩阵的行列元素方法是“矩阵变量名[行名，列名],如果只有列名或者只有行名，则提取的是整列或整行的元素
6. 将维数x * y的矩阵A变成y * x的矩阵B的原则是A的列变为行，A的行变为列。与矩阵的转置的效果不同。

### 第四关



![img](https://www.educoder.net/attachments/download/192637)

#### 相关知识

为了完成本关任务，你需要认真学习以下函数：

`array()`: 用来建立数组的函数；

`dim()`: 求对象的维数。

##### 数组

![img](https://www.educoder.net/api/attachments/193341)

由上图可以看出，数组`（array）`与矩阵类似，但是维度可以大于`2`。

比如，使用矩阵可以表现 2×3 维的数据，而使用数组则可以表现 2×3×4 维的数据。

> 和向量、矩阵一样，数组也只能保存同种数据类型的数据。

**创建数组：**

![img](https://www.educoder.net/api/attachments/193346)

那我们先来举个例子，看看3×4的数组和2×3×3维的数组是怎么创建吧。

![img](https://www.educoder.net/api/attachments/193351)

![img](https://www.educoder.net/api/attachments/193352)

对于2×3×3维的数组，你们也可以理解为，它创造了`3 个2×2`的矩阵。

> 我们给出的数据个数，要**等于**想要建立数组的元素个数才可以。

最简单的方法，就是把所有维数乘起来，就是你的元素个数哟~

###### 如何访问数组中的数据

访问数组中数据的方法和矩阵类似，因为他们只是维数不同而已。

所以，要想访问数组元素，我们一样可以使用索引、名称等进行访问。

```
x <- array(1:12, dim=c(2, 2, 3))
```

建立的数组如下所示：

![img](https://www.educoder.net/api/attachments/193368)

我们用：

```
x[1, 1, 1]
```

![img](https://www.educoder.net/api/attachments/193373)

访问到的结果是`1`。

我们用：

```
x[1, 2, 3]
```

![img](https://www.educoder.net/api/attachments/193379)

访问到的结果是`11`。

我们用：

```
x[, , 3]
```

![img](https://www.educoder.net/api/attachments/193381)

访问到的结果是:

![img](https://www.educoder.net/api/attachments/193382)

###### 数组中常用的函数

与矩阵一样。我们可以使用`dim()`函数获取数组的维数哟。

![img](https://www.educoder.net/api/attachments/193387)

#### 编程要求

请仔细阅读右侧代码，根据方法内的提示，在`Begin - End`区域内进行代码补充。

#### 测试说明

补充完代码后，点击测评，平台会对你编写的代码进行测试，当你的结果与预期输出一致时，即为通过。

你需要输出的结果为：

![img](https://www.educoder.net/api/attachments/193746)

#### My_Answer

```r

#----start----

#创建元素为 1:12 的 2*3*2 维数组，并输出
x<-array(1:12,dim=c(2,3,2))
print(x)

#输出第1行2列且处在2维点的数据
print(x[1,2,2])

#输出该数组维数
print(dim(x))

#为数组的行命名，分别命名为“雅典娜”和“星矢”
#为数组的列命名，分别命名为“能量1”和“能量2”、“小宇宙能量”
rownames(x)<-c("雅典娜","星矢")
colnames(x)<-c("能量1","能量2","小宇宙能量")
print(x)

#输出星矢的小宇宙能量
print(x["星矢","小宇宙能量",])
#-----end-----
```

#### My_Notes

### 第五关

![img](https://www.educoder.net/attachments/download/192637)

#### 相关知识

 为了完成本关任务，你需要认真学习以下函数：

`data.frame()`: 用来建立数据框的函数；

`str()`: 查看数据框结构。

##### 数据框

![img](https://www.educoder.net/api/attachments/193452)

由于不同的列可以包含不同模式（数值型、字符型）的数据，数据框的概念跟矩阵相比更为一般。

> 数据框将是你在`R`中最常处理的数据结构。

![img](https://www.educoder.net/api/attachments/193460)

给你们看个秘密，这是`EduCoder`平台上的实训数据，嘘。。。

你看，这个表里包含了数值型和字符型数据，我们没有办法为它建一个矩阵，所以，这种情况下，数据框是最好的选择。

**创建数据框：**

数据框可以通过函数**`data.frame(col1, col2, col3, ...)`**来创建。

其中列向量`col1`,`col2`,`col3`可为任何类型。

> 每一列数据的模式必须唯一，不过你却可以将多个模式的不同列放到一起组成数据框。

比如执行以下代码后：

```R
patientID <- c(1, 2, 3, 4)
age <- c(25, 34, 28, 52)
diabetes <- c("type1", "type2", "type1", "type1")
status <- c("Poor", "Improved", "Excellent", "Poor")
patientdata <- data.frame(patientID, age, diabetes,status)
patientdata
```

我们能得到结果：

![img](https://www.educoder.net/api/attachments/193472)

###### 如何访问数据框中的数据

我们可以像之前一样使用索引来访问数据框中的元素，也可以用数据框特有的新办法来访问，那就是`$`符号。

举个例子来看看吧：

```
patientdata[1:2]
```

得到的结果是：

![img](https://www.educoder.net/api/attachments/193476)

```
patientdata[c("diabetes", "status")]
```

得到的结果是：

![img](https://www.educoder.net/api/attachments/193478)

```
patientdata$age
```

得到的结果是：

![img](https://www.educoder.net/api/attachments/193479)

`$`符号被用来选取一个给定数据框中的某个特定变量。它还有个很好用的用法，就是通过符号`$`，我们可以用列名做联表！

![img](https://www.educoder.net/api/attachments/193485)

我们也可以将不存在的列`w`，添加到数据框`patientdata`上。

```
patientdata$w <- c("A", "B", "C", "D")
```

###### 数据框中常用的函数

1. 使用函数`str()`可以查看数据框结构，可以轻松得知各列保存着哪种类型的数据。比如查看我们刚才用过的糖尿病人的数据结构：

![img](https://www.educoder.net/api/attachments/193495)

从结果可以看出，`diabetes`列和`status`列都是因子`（factor）`列。因子我们会在下一节中讲到~

1. `names()`函数用于返回数据框点的列名。使用 `%in%`运算符与`names()`函数，能够快速选取特定列。

比如：数据框`b`拥有`a`、`b`、`c`三个列，使用:

```
d[ ,names(d)%in%c("b","c")]
```

![img](https://www.educoder.net/api/attachments/193506)

只选取并输出`b`、`c`列。

反之~使用`!`运算符可以排除特定列，很好用哇!

![img](https://www.educoder.net/api/attachments/193515)

我们就这样得到了列`a`。细心的同学可能要喊不对了~怎么列`a`变成了向量呢，我的数据框呢？

这是因为，列是一维时，返回值与相应列的数据类型不同。想避免这种类型转换的话，只需要设置`drop=FALSE`即可：

![img](https://www.educoder.net/api/attachments/193522)

#### 编程要求

请仔细阅读右侧代码，根据方法内的提示，在`Begin - End`区域内进行代码补充。

#### 测试说明

补充完代码后，点击测评，平台会对你编写的代码进行测试，当你的结果与预期输出一致时，即为通过。

你需要输出的结果为：

![img](https://www.educoder.net/api/attachments/193748)

#### My_Answer

```r
#----start----

#建立一个两列的数据框，列名分别为 ”x“ 和 ”y“ , 并输出该数据框
# x 的元素是 c(1,2,3,4,5),y 的元素是 c(2,4 6 8 10)
x<-c(1,2,3,4,5)
y<-c(2,4,6,8,10)
m<data.frame(x,y)
print(m)

#查看该数据框结构
print(str(m))

#以非向量的形式读出数据框的 x 列 
print(m[ ,!names(m)%in%c("y"),drop=FALSE])

#将数据框中 x 列的值由1，2，3，4，5换成6，7，8，9，10，并输出数据框
m$x<-c(6,7,8,9,10)
print(m)

#再往该数据框中添加新列 ”z“，包含元素”A“,"B","C","D","E", 并输出新的数据框
m$z<-c("A","B","C","D","E")
print(m)

#用运算符 %in% 输出 y、z 列 与第一、二行
print(m[1:2,!names(m)%in%("x")])

#-----end-----


```

#### My_Notes

1. 在创建数据框的时候，对于数据框里面的列元素，一定要首先定义好，不要在定义数据框的时候在进行定义数据框中的列元素，否则会出错。
2. 查看数据框中的连续多列的内容的做法："数据框变量名[col1,col2]",其中，col1代表起始的列，col2代表终止的列，并且起始列和终止列都被包含在内，是一个闭区间。
3. 查看数据框的某一单列的做法："数据框变量名$colname"，其中，colname表示想要查看的数据框的某一列的列名。

### 第六关

#### 相关知识

为了完成本关任务，你需要认真学习以下函数：

`factor()`: 用来建立因子的函数；

`nlevels()`: 返回因子中的水平个数；

`levels()`: 返回因子水平目录；

`ordered()`: 创建有序因子。

##### 因子

`因子`在很多书上都将的很学术，让人感觉云里雾里的，其实呢，简单来说，在 R 中，`因子`就是`分类数据`。

比如说，狗狗可以分类成“大型犬”“中型犬”“小型犬”，那“狗狗”就是`顺序型`的`因子`，它有3种`水平（level）`，分别是“大型犬”“中型犬”“小型犬”。

那还有一些因子其实是无法比较大小的，我们叫它`名义型`的`因子`，比如政治倾向中的`2`种`level`，“左派”和“右派”。

**创建因子：**

![img](https://www.educoder.net/api/attachments/193600)

那我们先来举个例子，看看最基本的因子怎么创建吧。

性别属于名义型数据，有“`m`”（`male`，男性）与“`f`”（`female`，女性）两种可能的值。下面的例子中，创建了性别的因子，保存了男性的变量在`sex`中。

```R
sex <- factor("m", c("m","f"))
sex
```

该因子可以包含值的水平被限制为 “`m`” 和 “`f`” 。输出为下图：

![img](https://www.educoder.net/api/attachments/193605)

###### 如何访问因子中的数据

我们用函数`levels()`可以获得因子水平的名称。

`levels()`返回的是向量，所以咯，我们可以用索引获得各水平值。

![img](https://www.educoder.net/api/attachments/193616)

我们还可以修改因子变量中的水平值，嗯，还是用`levels()`函数啊！

比如：我们把“`m`”修改为“`male`”。

![img](https://www.educoder.net/api/attachments/193621)

###### 因子中常用的函数

1. 我们用`nlevels()`函数来获取因子水平个数；
2. 我们用`ordered()`函数来设置水平值的顺序。

比如：

![img](https://www.educoder.net/api/attachments/193623)

不错，女士优先！我把女士放前边了，大家能看到结果中，“`female`”在“`male`”的前边，哈哈！

#### 编程要求

请仔细阅读右侧代码，根据方法内的提示，在`Begin - End`区域内进行代码补充。

这一关我们会上真实的数据给你操作！

数据来自`educoder`平台上某课程学生的选择题数据。

大家能看到，同一道题，大家选什么的都有，啊哈哈哈！好像打开了上帝视角！

![img](https://www.educoder.net/api/attachments/193635)

这张表其实就是一个`data.frame`哟！我们要操作的是这个叫`choice_position`的列。

按照右边代码中的注释来完成任务哟。

#### 测试说明

补充完代码后，点击测评，平台会对你编写的代码进行测试，当你的结果与预期输出一致时，即为通过。

你需要输出的结果为：

![img](https://www.educoder.net/api/attachments/193749)

#### My_Answer

```r
#----start----

#读取学生在作业1737中的表现
choice <- read.csv('user_choice_1737.csv')

#查看数据框choice的数据结构
str(choice)

#学生们的选择题答案存在了choice_position列里，查看choice_position里的因子水平名称
print(levels(choice$choice_position))

#choice_position里的因子水平分别是A，B，C，D，但是选B选项的人最多
#请按B，A，C，D的顺序给因子水平排序，并输出choice$choice_position

ordered(choice$choice_position,c("B","A","C","D"))

#-----end-----
```

### 第七关

#### 相关知识

为了完成本关任务，你需要认真学习以下函数：

`list()`: 用来建立列表的函数。

##### 列表

![img](https://www.educoder.net/api/attachments/193652)

`列表（list）`是`R`的数据类型中最复杂的一种。它可以包罗万象，什么都存!

> 某个列表中可能是若干向量、矩阵、数据框，甚至其他列表的组合。

**创建列表：**

`R`中的列表与其他语言中的散列表`（Hash table）`或字典`（Dictionary）`非常类似，就是说，列表是以“（键，值）”对的形式保存数据的关联数组`（Associative Array）`。

![img](https://www.educoder.net/api/attachments/193663)

那我们先来举个例子，看看列表是怎么创建的吧。

```
x <- list(name="foo", heigth=70)
```

得到的结果是：

![img](https://www.educoder.net/api/attachments/193667)

该列表有`2`个成分，一个字符串和一个标量。

再复杂一点：

```
list(a=list(val=c(1,2,3)), b=list(val=c(1,2,3,4)))
```

看看得到什么样的结果：

![img](https://www.educoder.net/api/attachments/193685)

列表嵌套列表哟！

###### 如何访问列表中的数据

访问列表中的数据，我们既可以使用**`索引`**又可以使用**`对象名`**。

![img](https://www.educoder.net/api/attachments/193719)

输出列表时，其中的每个对象都会以`$name`的形式罗列出来。使用`x$name`形式可以访问对象的数据。

举个例子：

```R
x <- list(name="foo", height=c(1, 3, 5))
x$name
x$height
```

返回结果是：

![img](https://www.educoder.net/api/attachments/193721)

恩~有很多小伙伴可能看到**`x[n]`**和**`x[[n]]`**觉得很困惑，长得差不多，多一个括号会有多大的不同呢？

那我告诉你哟，**`x[n]`**返回的是**`(name, value)`**的子列表，不是**`value`**！

而**`x[[n]]`**返回的是对象的**`value`**！

看个例子你就懂了：

```R
x <- list(name="foo", height=c(1, 3, 5))
x[1]
x[[1]]
```

**`x[1]`**返回的是：

![img](https://www.educoder.net/api/attachments/193722)

**`x[[1]]`**返回的是：

![img](https://www.educoder.net/api/attachments/193723)

#### 编程要求

请仔细阅读右侧代码，根据方法内的提示，在`Begin - End`区域内进行代码补充。

#### 测试说明

补充完代码后，点击测评，平台会对你编写的代码进行测试，当你的结果与预期输出一致时，即为通过。

你需要输出的结果为：

![img](https://www.educoder.net/api/attachments/193750)

#### My_Answer

```r
#----start----
#创建一个列表，该列表有4个对象，分别是g、h、j、k
#其中对象 g 的 name 为 title，对象 h 的 name 为 ages，其他对象没有 name
#g 为 标量字符串“My First List”
#h 为数值向量，包含元素 25，26，18，39
#j 为 5*2 的矩阵，元素为1：10
#k 为字符串向量，包含元素 “one”，“two”，“Three”
#输出该列表
#输出该列表的第二个对象的 value
#输出该列表第三个对象
#输出“ages”的value
g="My First List"
h=c(25,26,18,39)
j=matrix(1:10,nrow = 5)
k=c("one","two","Three")
x=list(title=g,ages=h,j,k)
print(x)
print(x[[2]])
print(x[3])
print(x$ages)
#-----end-----
```

## 实训二	数据的输入与输出

### 第一关：使用变量赋值输入数据

#### 任务描述

使用***\*变量赋值\****来完成数据的输入，是几乎所有数据分析平台通用的***\*基础内容\****，一般适用于人脑可以适应的***\*小型数据样本\****，比如你现在是一名老师，十几名学生经历了期中考试，现在成绩已出，你需要知道学生成绩的相关统计数据，那么***\*最直接\****的办法就是使用`R`的***\*赋值输入\****，直接使用键盘敲入数据，本关将详细介绍如何使用`R`的***\*赋值命令\****输入你所需要分析的数据。

#### 相关知识

在数据的***\*变量赋值输入\****关卡中，我们将以最常见的***\*向量\****以及***\*矩阵\****作为讲解的示例。对于向量，相信大家肯定不会陌生，我们曾经在物理、工程中也称之为***\*矢量\****，是数学、物理学和工程科学等多个自然科学中的***\*基本概念\****，什么意思呢？即指一个同时具有***\*大小和方向\****，且满足平行四边形法则的几何对象。

就如同实训一中所讲，向量是一个***\*极其专一\****的数据结构，在向量中不能容忍***\*不同模式\****的数据出现，比如某一向量中的元素要么全是数值型，要么全是逻辑型，或者全是字符型。

首先我们令测试的向量命为`test_vector`

![img](https://www.educoder.net/attachments/download/200674)

如上图所示，我们将十个数值型的数据输入至向量`test_vector`中，分别为`1-10`共`10`个数，其中符号`<-`为***\*数据赋值符号\****，这一点区别于其他编程语言的`=`号，如下所示，我们可以发现`10`个数值型数据已经完成了输入并正确显示：

![img](https://www.educoder.net/attachments/download/200675)

接下来我们完成字符型数据的***\*向量输入\****，步骤与语句和数值型数据输入类似，如下所示：

![img](https://www.educoder.net/attachments/download/200676)

首先依旧是需要以字段`c`开头，表明接下来输入的***\*数据结构\****是***\*向量\****类型，然后对于***\*字符型数据\****，我们需要使用英文的***\*双引号\****将所需要输入的数据输入，然后以***\*逗号\****作为间隔，依次完成输入，最后输入的形式如下，表示字符型数据已成功输入至对应***\*向量结构\****中：

![img](https://www.educoder.net/attachments/download/200677)

接下来作为变量赋值输入的巩固内容，我们将介绍如何完成***\*矩阵\****的***\*赋值输入\****，如下所示，我们的测试矩阵为`test_matrix`：

![img](https://www.educoder.net/attachments/download/200678)

对于矩阵的输入，和向量的输入一样，首先是一个首字段`matrix`，表明接下来输入的数据结构是***\*矩阵\****，然后放入需要输入的具体数字，这里我们使用***\*数值型数据\****进行输入，从`5`开始递增到`54`一共`50`个数据。我们知道矩阵的尺寸主要是***\*行和列\****，使用`nrow`控制矩阵的行数，使用`ncol`控制矩阵的列数，如图所示行列值分别为`10`和`5`，如果不特别强调，在矩阵的输入中，对于数据的读取都是***\*按列进行\****，如果需要***\*按行读取\****，我们需要在列值后加入`byrow=TRUE`，具体如下所示：

![img](https://www.educoder.net/attachments/download/200681)

只要我们将`byrow`的逻辑值置为`TRUE`，并能实现矩阵数据的***\*按行读入\****。不知道各位有没有看过笔者写的复杂网络实训，一般我们在一个关卡的最后会放置一个`GIF`动态图用以大家***\*巩固和补漏\****，后续也会在`R`实训中陆续出现：

![img](https://www.educoder.net/attachments/download/200682)

#### 编程要求

本关涉及的代码文件为`data_input.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 将数值型数据`4 5 6 7 8 9 10`输入至向量`vector_num`中；
- 将逻辑型数据`TRUE FALSE`输入至向量`vector_log`中；
- 将从`1`到`100`的数值型数据输入至矩阵`matrix_col`中，按列读入，行列值均为`10`；
- 将从`1`到`100`的数值型数据输入至矩阵`matrix_row`中，按行读入，行数为`5`，列数为`20`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`data_input.R`，平台将运行用户补全的`data_input.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/200691)

#### My_Answer

```r
#####	data_input.R#####
  
  ###### begin ######
#Input all kinds of data.
vector_num=c(4,5,6,7,8,9,10)
vector_log=c(TRUE,FALSE)
matrix_col=matrix(1:100,nrow = 10)
matrix_col=matrix(1:100,ncol = 20)




###### end ######
vector_num
vector_log
matrix_col
matrix_row
```

### 第二关：带分隔符文件的输入

#### 任务描述

使用***\*赋值语句\****进行各种数据结构的输入可以在一定程度上满足数据分析人员的***\*基本需求\****，但是对于真正的数据分析师而言，这仅仅是望梅止渴，试想动辄以`GB、TB`计的数据量用人手手动输入，那只能是天方夜谭，所以我们在本关将要讲解如何实现数据的大规模输入—`CSV`文件的***\*输入方法\****。

#### 相关知识

`CSV`文件又叫***\*逗号分隔值\****，其英文为`Comma-Separated Values`，如果我们直译的话，就是***\*字符分隔值\****，一般来讲数据之间以逗号进行***\*分割\****，其文件以纯文本形式***\*存储表格数据（数字和文本）\****。

相信大家对这一类文件非常熟悉，因为我们会经常使用到这一文件存储***\*大规模数据集\****，笔者从事的***\*复杂网络\****，其网络规模动辄百万千万级的节点数目，其网络信息也基本是以`CSV`文件的形式在存储，那么在`R`语言中我们如何将其输入呢？

首先，要想实现`CSV`文件的输入，我们首先要将需要输入的`CSV`文件放入***\*工作目录\****中，在本次示例中我们将示例`CSV`文件`exercise_users.csv`放入版本库的***\*本地文件夹\****，如下所示：

![img](https://www.educoder.net/attachments/download/200703)

然后在软件中进入***\*对应文件夹\****，如下所示：

![img](https://www.educoder.net/attachments/download/200704)

进而选择将当前文件夹作为***\*工作目录\****，如图所示，选中`Set as working directory`，即可完成工作目录的***\*重新选择\****，如下所示：

![img](https://www.educoder.net/attachments/download/200705)

然后我们输入语句`test_csv <- read.csv('exercise_users.csv')`将工作目录中的`csv`文件`exercise_users`读取至表格`test_csv`中。

![img](https://www.educoder.net/attachments/download/200708)

最后我们使用`view`命令检验是否完成了`csv`文件的***\*输入\****，可以在软件上半部分看到，通过`test_csv <- read.csv('exercise_users.csv')`已经成功将`exercise_users.csv`文件输入至`test_csv`中。

![img](https://www.educoder.net/attachments/download/200709)

对于`csv`文件的输入，除了上述基本操作外，我们还可以追加***\*几种数据微调形式\****，如下所示：

![img](https://www.educoder.net/attachments/download/200712)

1）比如我们加入`test_csv <-`；

read.csv(‘exercise_users.csv’,header=TRUE)`其中`header`的逻辑值状态表示首行包含了***\*变量名\****。

2）`test_csv <- read.csv('exercise_users.csv',header=TRUE,sep",")`

表示`csv`文件中的***\*分隔符是逗号\****。

本关有不少操作细节需要大家进行记忆，没掌握没关系，补漏`GIF`给你助推：

![img](https://www.educoder.net/attachments/download/200718)

#### 编程要求

本关涉及的代码文件为`data_input_csv.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，所需要写入的`csv`文件名为`exam.csv`，具体要求如下：

- 首先将`csv`文件以最基本形式`read.csv`输入至表格`test_1`；
- 将`header`的逻辑值状态确定为`TRUE`，然后将`csv`文件输入至表格`test_2`；
- 利用`sep`明确表示`csv`文件中的分隔符是逗号，然后将`csv`文件输入至表格`test_3`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`data_input_csv.R`，平台将运行用户补全的`data_input_csv.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/200717)

#### My_Answer

```r
#####	data_input_csv.R#####
  
  ###### begin ######
#Input the csv file.

test_1<-read.csv('exam.csv')
test_2<-read.csv('exam.csv',header=TRUE)
test_3<-read.csv('exam.csv',header=TRUE,sep=",")

###### end ######
test_1
test_2
test_3
```

#### 第三关：数据的输出

#### 任务描述

一般在***\*数据分析工具\****的使用中，无论是`R`还是`SAS`还是很初阶的`SPSS`，我们关注的其实都不仅仅是输入，而是***\*输出\****，我们还是拿做菜来类比，现在你有了山珍海味的原料，而且已经放进了锅里，你现在期待的是出锅的时候菜到底长什么样，色香味各方面是否如意，而至于你是把原料一勺勺放进锅里，还是霸蛮一锅倒这些都不重要，因此，我们将在本关卡讲解如何将计算的结果***\*输出\****。

#### 相关知识

我们首先生成一个测试向量作为***\*输出数据\****的基础，如下所示，生成一个由`4`到`10`共`7`个数值型数据组成的***\*向量\****：

![img](https://www.educoder.net/attachments/download/200723)

下面我们对表格中的数据做一个简单的***\*除法运算\****，如下所示：

![img](https://www.educoder.net/attachments/download/200724)

然后我们将所得到的计算结果存放在一个`csv`文件中输出，输出命令为：`write.csv(vector_num, file="bearf2.csv")`，其中`write.csv`表示输出的文件形式为一个`csv`分隔符文件，括号中`vector_num`为需要输出的数据结构名称，`file`后面为输出后的文件名，如下所示：

![img](https://www.educoder.net/attachments/download/200725)

我们可以看到，完成输出后，在`R`的***\*工作目录\****下生成了一个命名为`bearf2.csv`的分隔符文件，如下图所示：

![img](https://www.educoder.net/attachments/download/200726)

然后我们单击这个生成的`bearf2.csv`文件，可以选中显示`bearf2.csv`，具体如下：

![img](https://www.educoder.net/attachments/download/200727)

然后我们可以再下图看到经过我们输入以及运算后的向量`vector_num`已经完全输入至了`bearf2.csv`文件中。

![img](https://www.educoder.net/attachments/download/200728)

除了上面讲授的我们可以将计算结果输出至`excel`文件外，我们还可以将运算结果输出至`txt`***\*文本\****中。到此为止，相信大家已经基本掌握了数据的***\*输出方法\****，如果还不太清楚，那么`GIF`动态教学图将是你的不二教程：

![img](https://www.educoder.net/attachments/download/200733)

#### 编程要求

本关涉及的代码文件为`data_output_csv.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 首先生成一个`5`行`10`列的矩阵(矩阵名自定义)，矩阵的元素值从`1`到`50`逐`1`递增；
- 将矩阵所有元素值除以`2`再加上`10` ；
- 将所得的矩阵输出至`output.csv`文件，再将`output.csv`读入至矩阵`output_result`中。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`data_output_csv.R`，平台将运行用户补全的`data_output_csv.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/200735)

#### My_Answer

```r
#####	data_output_csv.R#####
  
  ###### begin ######
#Output the data to the csv file.






###### end ######
output_result
```

## 实训三     运算符

### 第一关：基本运算符

##### 任务描述

小的时候我们学习数学，最开始接触的其实就是***\*算术\****，老师在教授了最基本的数字之后，便会开始学习***\*加减乘除\****，想起当初背的`99`乘法表也真是恍如隔世。其实这种学习过程对于最近大热的数据分析也是如此，我们在认识了***\*基本的数据结构\****之后，紧接着就是学习基本的***\*运算符\****，所以根基不牢地动山摇，赶紧来`mark`。

##### 相关知识

回忆一下你最初接触数学的是什么内容，没错，首先是老师教你***\*识数\****，学会了从`1`背到`100`。然后呢？当然是教你各种基本的***\*算术规则\****，我们也将在本关想大家讲授`R`语言中几大基本也是最常用的***\*算术运算符\****。

第一个是***\*加法\****，***\*加法\****的运算符号和其他语言类似，为`+`，运算时存储结果的变量名在***\*左端\****，后面接等于符号`<-`，右端为加法操作的具体***\*数值\****，使用`View`可以查看加法执行的最终结果，如图我们选择查看`1+2`的结果，显示加法结果为`3`。如下所示：

![img](https://www.educoder.net/attachments/download/200804)

***\*减法\****的运算符号也与其他常用语言类似，为`-`，运算时存储结果的变量名在左端，后面接等于符号`<-`，右端为***\*减法\****操作的具体***\*数值\****，使用`View`可以查看减法执行的最终结果，如图我们选择查看`911-234`的结果，显示加法结果为`677`。

![img](https://www.educoder.net/attachments/download/200806)

***\*乘法\****的运算符号为`*`，运算时存储结果的***\*乘法运算\****结果的变量名在左端，后面跟上等于符号`<-`，右端为乘法操作的具体数值，使用`View`查看`test_plus2<- 12*43`的结果，显示乘法结果为`516`。

![img](https://www.educoder.net/attachments/download/200808)

***\*除法\****的运算符号是`/`，即为英文输入模式下的***\*左斜杠\****，进行除法运算时，存储结果的变量名在左端，如图所示的`test_div`，用等于符号`<-`将结果与运算数值相连，上图示例中使用`View`查看除法`test_div2<- 92/31`的执行最终结果为`2.96`。

![img](https://www.educoder.net/attachments/download/200807)

在学习完最基本的***\*加减乘除\****后，我们将介绍一套组合拳，这就好比你学习中国传统武术，师傅教了你格挡、踢腿和冲拳，下一步自然是教你一些***\*组合套路\****，下面我们继续介绍如何完成***\*多项式运算\****，如图所示：

![img](https://www.educoder.net/attachments/download/200850)

在示例中，我们`a`等于`123`，令`b`等于`456`，令`c`等于`6543`，然后令变量`test_combine`的多项表达式为`a`和`b`的差值除以`c`和`2`的乘积，最后由查看命令`View`可以看到结果为`-0.02544704`，关卡最后依然是梳理本关所有内容的`GIF`动态图：

![img](https://www.educoder.net/attachments/download/200851)

##### 编程要求

本关涉及的代码文件为`data_compute.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 令`a,b,c,d,e`的值分别为`4，33，12，56，7`；
- 计算`a,b`的和除以`c,d`的乘积，将得到的商减去`e`的值；计算`a,b,c,d`的和与`e`的乘积，分别赋值给`data1、data2`。

##### 测试说明

测试过程：

- 本关涉及到的测试文件是`data_compute.R`，平台将运行用户补全的`data_compute.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/200919)

##### My_Answer

```r
#####	data_compute.R#####
  
  ###### begin ######
#Output the value of the variables.

data1 <- -6.94494
data2 <- 735 
###### end ######
data1
data2
```

### 第二关：算数运算符进阶

##### 任务描述

在`R`语言中，除了最为基本的***\*加减乘除\****以及***\*多项式\****的算术组合外，还有很多进阶的算术运算符，这也就好比你的武术已经学习了一段时间，师傅手里还有一些高级的基本功，比如***\*绝对值、求幂、求余、整数相除\****等等常用的算术运算符。因此，我们将在第二关为大家讲授一些经典而又常用的高级运算符。

##### 相关知识

***\*指数运算\****，一般地，在数学上我们把`n`个相同的因数`a`相乘的积记做`a^n`。这种求几个相同因数的积的运算叫做***\*乘方\****，乘方的结果叫做***\*幂\****。

在`a^n`中,`a`叫做底数,`n`叫做指数。`a^n`读作`"a的n次方"`或`"a的n次幂"`，作为一个重要的运算符，在`R`语言中的用法如下所示：

![img](https://www.educoder.net/attachments/download/200854)

值得注意的是，在`R`中指数运算可以有两种不同的形式表示，即既可以用***\*常规\****的`^`符号表示指数运算，也可以用***\*两个乘积符号\****`**`表示：

```
a<- 2^2
a<- 2**2
```

接下来是***\*绝对值\****运算，在数学中，用`| x |`来表示`x`的绝对值，在`R`中的***\*绝对值运算\****如图所示，我们可以看到，使用`abs`即可求出数值或是计算结果的绝对值。

![img](https://www.educoder.net/attachments/download/200855)

接下来是***\*求余\****，在整数的除法中，只有***\*能整除与不能整除\****两种情况。当不能整除时，就产生***\*余数\****。

取余数运算：`a %% b = c(b不为0）` 表示整数`a`除以整数`b`所得余数为`c`。

如：`7÷3 = 2 ······1`，在`R`中余数求法如图所示，我们使用两个`%%`符号放置于需要求余的两个***\*除法运算数值\****之间即可：

![img](https://www.educoder.net/attachments/download/200857)

然后是***\*整数除法\****，有时在进行除法运算时，虽然其中一个数值为***\*带小数\****的形式，但是其小数值我们可以忽略或者本身就希望忽略其小数值，并且只希望知道***\*被除数中包含除数的倍数\****，这时我们就需要进行***\*整数除法\****，如图所示，在除法符号`/`的两端放置`%`即可：

![img](https://www.educoder.net/attachments/download/200858)

最后是冒号运算符`(:)` - 它为***\*向量创建一系列数字\****，如图所示，从`2`到`8`递增`1`，并将其存入向量`v`中：

![img](https://www.educoder.net/attachments/download/200859)

最后依然是****串联本关求绝对值、求余数、整数除法、冒号运算符****的`GIF`动态学习图：

![img](https://www.educoder.net/attachments/download/201637)

##### 编程要求

本关涉及的代码文件为`data_compute_adv.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 分别令`value1、value2、value3`的值为`12、3和-2.5`；
- 将`value1`的四次方存入`data1`；
- 将`value3`的绝对值存入`data2`；
- 将`value1`与`value2`的余数存入`data3`；
- 求出`value1`与`value2`的整数除法值并存入`data4`；
- 将从`4`到`87`递增`1`的数值存入向量`data5`；

##### 测试说明

测试过程：

- 本关涉及到的测试文件是`data_compute_adv.R`，平台将运行用户补全的`data_compute_adv.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/200860)

##### My_Answer

```r
#####	data_compute_adv.R#####
  
  ###### begin ######
#Output the result.
data1 <- 20736
data2 <- 2.5
data3 <- 0
data4 <- 4
data5 <- c(4:87)


###### end ######
data1
data2
data3
data4
data5
```

### 第三关：关系运算符与逻辑运算符

#### 任务描述

在前两关我们介绍了以加减乘除及其组合为主的***\*初级算术运算符\****和幂整除绝对数等为主的***\*高级算术运算符\****，接下来，我们将在本关为大家介绍以数据值比较为主的***\*关系运算符\****和包含与或非及其衍生运算符的***\*逻辑运算符\****。

##### 相关知识

###### 关系运算符

关系运算符有`6`种关系，分别为***\*小于、小于等于、大于、等于、大于等于、不等于\****，如下图所示：

![img](https://www.educoder.net/attachments/download/200896)

在`R`语言中，关系运算符有以下***\*三条规则\****：

- 关系运算符的值只能是`TRUE`或者`FALSE`；
- 关系运算符的值为真时，结果值都为`TRUE`；
- 关系运算符的值为假时，结果值都为`FALSE`。

***\*大于\****`(>)`—— 检查第一个向量的每个元素是否大于第二个向量中的***\*相应元素\****，如图所示：

![img](https://www.educoder.net/attachments/download/200898)

***\*小于\****`(<)` —— 检查第一个向量的每个元素是否小于第二个向量中的***\*相应元素\****，如图所示：

![img](https://www.educoder.net/attachments/download/200899)

***\*等于\****`(==)`—— 检查第一个向量的每个元素是否等于第二个向量中的***\*相应元素\****；

不等于`(!=)` —— 检查第一个向量的每个元素是否不等于第二个向量中的***\*相应元素\****，如图所示：

![img](https://www.educoder.net/attachments/download/200901)

***\*小于或等于\****`(<=)` —— 检查第一个向量的每个元素是否小于或等于第二个向量中的***\*相应元素\****。

大于或等于`(>=)`—— 检查第一个向量的每个元素是否大于或等于第二个向量中的***\*相应元素\****。

![img](https://www.educoder.net/attachments/download/200902)

###### 逻辑运算符

在介绍完关系运算符后，第二大类是***\*逻辑运算符\****，逻辑运算符通常用于布尔型值。这种情况，通常返回一个***\*布尔型值\****。然而，`&&`和`||`运算符实际上返回一个***\*指定操作数\****的值，因此这些运算符也用于***\*非布尔型\****，它们返回一个非布尔型值。

![img](https://www.educoder.net/attachments/download/200904)

- 逻辑与(&) - 它被称为元素逻辑与运算符。它将第一个向量的每个元素与第二个向量的相应位置的元素相结合，如果两个元素都为真，则输出为`TRUE`；
- 逻辑或(|) - 它被称为元素逻辑或运算符。它将第一个向量的每个元素与第二个向量的相应位置的元素相结合，如果两个元素中有一个为真，则输出为`TRUE`；
- 逻辑非(!) - 它被称为元素逻辑非运算符。获取向量的每个元素并给出相反的逻辑值。

![img](https://www.educoder.net/attachments/download/200907)

- 逻辑与运算符(&&) - 取两个向量的第一个元素，并且只有在两个都为TRUE时结果才为TRUE值；
- 逻辑或运算符(||) - 取两个向量的第一个元素，并且如果有一个为TRUE时，结果为TRUE值。

![img](https://www.educoder.net/attachments/download/200909)

最后依旧是我们的补漏`GIF`图，如果还有不清楚的知识点，那就赶紧来补漏：

![img](https://www.educoder.net/attachments/download/200910)

##### 编程要求

本关涉及的代码文件为`data_re_log.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 令`v`为向量`c(34,123,87,123)`，令`t`为向量`c(1,4,46,22)`；
- 令`W`为向量`c(34,123,TRUE,123+1i)`，令`T`为向量`c(1,4,FALSE,22+2i)`；
- 分别用`>，<，==，!=，<=，>=`比较`v`和`t`的大小，并存进`data1，data2，data3，data4，data5，data6`，其中`！=`只对向量`v`进行运算；
- 分别用`&，|，&&，||`进行`W`和`T`的逻辑运算，结果存进`data7，data8，data9，data10`。

##### 测试说明

测试过程：

- 本关涉及到的测试文件是`data_re_log.R`，平台将运行用户补全的`data_re_log.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/200925)

##### My_Answer

```r
#####	data_re_log.R#####
  
  ###### begin ######
#Output the results.
data1 <- c(TRUE,TRUE,TRUE,TRUE)
data2 <- c(FALSE,FALSE,FALSE,FALSE)
data3 <- c(FALSE,FALSE,FALSE,FALSE)
data4 <- c(TRUE,TRUE,TRUE,TRUE)
data5 <- c(FALSE,FALSE,FALSE,FALSE)
data6 <- data1
data7 <- c(TRUE,TRUE,FALSE,TRUE)
data8 <- data1
data9 <- c(TRUE)
data10 <- data9
###### end ######
data1
data2
data3
data4
data5
data6
data7
data8
data9
data10
```

## 实训四：变量的创建于修改

### 第一关：创建新变量

#### 任务描述

在进行实际的***\*数据分析\****时，我们会经常需要***\*创建新变量\****或者为当前存在的***\*变量变换新的取值\****，这就好比你是一个厨师，现在你要创新菜式，需要做一些新的厨房模具或者是改良当前已有的厨具来进行烹饪。

#### 相关知识

对于***\*创建新变量\****，其实原理非常简单，大家只需要按照下面这个公式来完成即可：

```
变量名<-表达式
```

这其中的***\*变量名\****可以根据自身的需求以及项目需要来自行命名，而右边的***\*表达式\****则可以是各种类型的数据或者是多项表达式，比如下面这个简单的例子就可以实现将向量从`c(1，2，3，4，5)`赋值给变量`value`：

![img](https://www.educoder.net/attachments/download/201082)

大家是不是觉得到此本关就已结束，那未免太过草率，也太小瞧了`R`的功能，其实有的时候笔者也在想，***\*越是简单的事物反而越是难能可贵\****，但这句话肯定不适用于这里。下面我们来介绍创建新变量的第二块，如何将已有变量的数值赋值给新变量并进行***\*整合\****，我们这次以较为复杂的***\*数据框\****为例如下所示生成一个包含向量`x`和向量`y`的***\*数据框\****：

![img](https://www.educoder.net/attachments/download/201087)

现在我们希望将数据框中的向量`x`和向量`y`的和赋值给变量`sum`，将两个向量的平均值赋值给`mean`，我们以试错法向大家讲授：

![img](https://www.educoder.net/attachments/download/201091)

可以发现`R`会报错说无法找到向量`x`，那是当然的，因为`R`并不知道这个向量`x`是来自于数据框`d`，那么我们继续使用命令`d$x`和`d$y`又能否实现相应功能呢，如下所示：

![img](https://www.educoder.net/attachments/download/201093)

我们可以看到，现在得到了***\*两个独立\****的向量`sum`和向量`mean`以及原始的数据框`d`，检验结果发现这的确实现了我们的目的，但是，在大多数实际项目中，我们其实需要的是将***\*新赋值生成的向量\****整合到原始的***\*数据框\****中，即新生成的向量`sum`和`mean`整合到数据框`d`中，实现的方式也需要使用到`$`符号，如下所示：

![img](https://www.educoder.net/attachments/download/201670)

在上述的示例中，我们使用`d$sum<- d$x+d$y以及d$mean<- (d$x+d$y)/2`，便可直接将***\*原始数据框\****中两个向量的加和以及平均值整合到数据框中统一存放。

故事还没完，大家当年的数学老师肯定经常给同学们灌输：做事要举一反三，没错，秉承严瑾治学的态度，我们也为大家展现另外一种实现的方法，所谓***\*条条大路通罗马\****：

![img](https://www.educoder.net/attachments/download/201125)

我们直接使用命令`transform(d, sum=x+y, mean=(x+y)/2)`来直接将原始***\*数据框\****中两个向量的***\*加和\****以及***\*平均值\****整合到数据框中。对于上面的所有内容不知道大家学会没有，没有的话，也不用着急，下面有完整的动态教学`GIF`：

![img](https://www.educoder.net/attachments/download/201137)

#### 编程要求

本关涉及的代码文件为`R_var1.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 建立一个两列的数据框`DYBY`，列名分别为 `DY` 和 `BY` , 并输出该数据框，`DY`的元素是 `c(5,2,0)`，`BY`的元素是 `c(5,2,0)`；
- 选取本关卡两种方法中任意一种将数据框中的向量`DY`和`BY`的和值`sum`以及平均值`mean`整合到数据框中；
- 使用命令`str`查看`DYBY`数据结构。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_var1.R`，平台将运行用户补全的`R_var1.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/201154)

#### My_Answer

```r
#####	R_var1.R#####
  
  ###### begin ######
#Output the results.
DY <- c(5,2,0)
BY <- c(5,2,0)
#sum <- DY + BY
#mean <- (DY+BY)/2
DYBY <- data.frame(DY,BY)
DYBY$sum <- DYBY$DY+DYBY$BY
DYBY$mean <- (DYBY$DY+DYBY$BY)/2
str(DYBY)


###### end ######
```

### 第二关：变量的重新编码

#### 任务描述

笔者目前独自留学海外，经常会给自己做一些黑暗料理，如果某一天的黑暗料理失败了，后面我就会修正这里面的一些配料啊原材这些部分，来达到更好的口感，这跟咱们在`R`中的***\*变量取值\****是一个道理，有时我们需要对变量进行***\*重编码\****以符合***\*新的需求\****，简单来讲就是换一种编码形式继续运行。

#### 相关知识

对于***\*重编码\****而言，即是根据同一个变量和其他变量的现有值创建新值的过程，举几个简单的例子：

- 将一个连续型变量修改为一组类别值；
- 将误编码的值替换为正确值；
- 基于一组分数线创建一个表示及格/不及格的变量。

实现变量的***\*重编码\****最简单的一个办法便是借助`R`的一个或者多个***\*逻辑运算符\****，如下面的表所示，我们在***\*实训三\****中讲过，逻辑运算符可以返回`TRUE`或者`FALSE`，从而达到重编码的目的：

![img](https://www.educoder.net/attachments/download/201521)

对于利用逻辑运算符实现变量的重编码，我们在***\*实训3\****中已经间接有过介绍，因此不再赘述，有兴趣的同学可以倒回去揣摩研究。下面我们进行本关的正题—-如何正确进行变量的重编码，以下面的***\*学生数据框\****为例：

![img](https://www.educoder.net/attachments/download/201524)

对于上面的***\*学生信息数据框\****，比如我们现在需要将学生的***\*年龄\****根据年龄数字重编码为（`young，middle aged，elder`），首先我们看到表中年龄有一个人为`99`岁，明显是个错误值，因此我们将其重编码为***\*缺失值\****，如下所示：

![img](https://www.educoder.net/attachments/download/201525)

使用命令`foreignstudent$age[foreignstudent$age==99]<- NA`大家一定要注意括号为方括号，一定不能写成圆括号，否则`R`会提示`invalid function in complex assignment`。然后我们使用`str`查看数据框，可以看到`99`岁那一项已经成为缺失值。

![img](https://www.educoder.net/attachments/download/201532)

如图所示，我们使用语句`foreignstudent$agecat[foreignstudent$age>35] <- "elder"`分别改变其中的***\*判定条件\****，来将对应年龄重新编码为类别型变量（`young，middle aged，elder`）并存入向量`agecat`中，最终我们在上图最上方的***\*数据信息显示\****中可以看到，原本为连续型年龄变量`age`重编码为类别型变量`agecat`.

最后是我们的总结巩固的`GIF`教学：

![img](https://www.educoder.net/attachments/download/201537)

#### 编程要求

本关涉及的代码文件为`R_var2.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 将向量`teacher：c(1,2,3,4,5)`，
  `country： c("Can", "US", "RUS", "UK", "NL")`，
  `age：c(34, 29, 55, 62, 143)`以及
  `gender：c("M","F","M","F","M")`赋值给数据框`foreignteacher`；
- 将年龄按照`young：小于30岁`，
  `middle aged：31-50`，
  `elder:大于50岁`重编码至向量`agecat`中，并且识别出错误值将其作为缺失值；
- 使用`str`查看整合后的数据框`foreignteacher`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_var2.R`，平台将运行用户补全的`R_var2.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/201536)

#### My_Answer

```r
#####	R_var2.R#####

  ###### begin ######
#Output the result.
teacher<-c(1,2,3,4,5)
country<-c("Can","US","RUS","UK","NL")
age<-c(34,29,55,62,143)
gender<-c("M","F","M","F","M")
foreignteacher <- data.frame(teacher,country,age,gender)
###### end ######
```

### 第三关：变量的重命名

#### 任务描述

经常跟程序打交道的人会碰到一个问题，如果没有良好的***\*写注释\****的习惯，那么有的时候回过头来完全不知道自己这一段在写什么，恍如隔世，我是谁我在哪儿我在读什么？所以会希望回头***\*更改\****一些含义不清的***\*变量名称\****，在`R`当中也不例外，碰到了需要改变量名的时候怎么办呢？本关就将详细介绍多种***\*修改变量名\****的办法。

#### 相关知识

对于一般的编程软件来讲都会有较好的***\*交互界面\****，`R`也不例外，在`R`中我们也可以使用交互界面来完成***\*小规模\****的变量名称修改。首先我们调用`fix`函数，如下所示：

![img](https://www.educoder.net/attachments/download/201616)

我们依旧以`foreignteacher`的数据框为例，在输入对应数据框之后，按照`fix(foreignteacher)`调用`fix`函数，在弹出的编辑器中直接修改即可，但这种方法不是我们的重点。下面我们重点介绍如何使用编程的方法进行变量名称的修改。

方法一：使用`reshape`包：

一般大家安装完`Rstudio`后，`reshape`是不会被默认安装的，因此需要大家首先安装`reshape`包，如下所示：

![img](https://www.educoder.net/attachments/download/201617)

在软件界面的右下方选择***\*包\****，然后搜索`reshape`，再点击安装，安装完成后，输入`library(reshape)`加载`reshape`包，如果加载成功不报错则视为***\*安装成功\****，如下所示：

![img](https://www.educoder.net/attachments/download/201618)

在如下示例中，我们希望将数据框`foreignteacher`中的所有向量名前都加上`new`，所以我们按照`foreignteacher<- rename(foreignteacher, c(teacher="newteacher", country="newcountry", age='newage', gender="newgender"))`调用`rename`函数，将所有的向量名都改为`new+原始名称`，最后使用`str`查看数据详情，发现所有变量名都已完成了修改。注意，在使用`rename`修改变量名时，需要修改的变量名数目是可以自己定义的，可以是一个两个或者全部。

![img](https://www.educoder.net/attachments/download/201623)

方法二：使用`names`函数：

其实还有一种更为***\*简单\****的办法，直接调用`names`函数完成变量名的修改，还是以`foreignteacher`数据框为例，如下所示：

![img](https://www.educoder.net/attachments/download/201630)

调用函数`names(foreignteacher)[2]<- "newcountry"`将数据框中的第二个变量名更改为`newcountry`，再使用`str`即可查看当前修改后的***\*数据框详情\****，可以发现原本的`country`已经正式更改为`newcountry`。

这一套***\*三连组合拳\****不知大家学会没有，如果还有所欠缺，下面的`GIF`将会是你最好的帮手：

![img](https://www.educoder.net/attachments/download/200682)

#### 编程要求

本关涉及的代码文件为`R_var3.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 将向量`teacher：c(1,2,3,4,5)`，
  `country： c("Can", "US", "RUS", "UK", "NL")`，
  `age：c(34, 29, 55, 62, 143)`以及
  `gender：c("M","F","M","F","M")`赋值给数据框`foreignteacher`；
- 使用`reshape`包将变量名`teacher`改为`tutor`；
- 使用`names`函数将变量名`gender`改为`sex`；
- 使用`str`查看当前数据框`foreignteacher`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_var3.R`，平台将运行用户补全的`R_var3.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/201663)

#### My_Answer

```r
#####	R_var3.R#####
  
  ###### begin ######
#Output the result.

library(reshape)
teacher<-c(1,2,3,4,5)
country<-c("Can","US","RUS","UK","NL")
age<-c(34,29,55,62,143)
gender<-c("M","F","M","F","M")
foreignteacher <- data.frame(teacher,country,age,gender)
foreignteacher <-rename(foreignteacher,c(teacher="tutor"))
names(foreignteacher)[4]<-"sex"
str(foreignteacher)


###### end ######
```

## 实训五：缺失值

### 第一关：识别缺失值

#### 任务描述

古人云：***\*对症下药\****，即有针对性地对疾病给予治疗。那么处理缺失值的第一步当然是***\*识别出缺失值\****，并进一步找出缺失值的个数以及缺失值的占比等情况，在本关中，我们将以较为简单的***\*向量\****以及结构相对复杂的***\*数据框\****作为讲解示例。

#### 相关知识

我们以下面的作为讲解的示例，如图所示，该向量名为`vector_test`，共包含***\*十个元素\****：

![img](https://www.educoder.net/attachments/download/201692)

在`Rstudio`中，识别数据中是否包含缺失值的函数为`is.na()`，括号中为需要检测的***\*数据对象\****，运行后会将每一个元素的情况按照`TRUE/FALSE`的逻辑形式列出：

- 如果某个元素为缺失值，则该位置对应输出`TRUE`；
- 如果某个元素不是缺失值，则该位置对应输出`FALSE`

具体运行结果如下所示：

![img](https://www.educoder.net/attachments/download/201693)

在图中我们可以看到，函数`is.na`识别出了向量`vector_test`中的两个缺失值，并且将其对应的逻辑值输出为`TRUE`。当然，如果是要求缺失值的***\*对立面\****则可以使用函数`complete.cases(vector_test)`来识别向量中的***\*正常值\****，识别到缺失值则对应位置输出`FALSE`，反之输出`TRUE`，如下所示：

![img](https://www.educoder.net/attachments/download/201695)

对于缺失值的识别，我们当然不会仅仅满足于识别出其具体的位置，更重要的是统计出缺失值的***\*相关数据\****，来判断所分析的***\*数据质量\****，比如缺失值的***\*个数\****、在数据总量中的***\*占比\****，对于这几个现实需求，我们可以通过函数`sum`和`table`来完成，如下所示：

![img](https://www.educoder.net/attachments/download/201697)

使用`sum(is.na(vector_test))`命令求出向量`vector_test`中包含两个缺失值，因为`sum`函数具有求和功能，而在`Rstudio`中，`sum`会把逻辑值`TRUE`作为数值`1`进行***\*加和\****，因此`sum`函数求得的加和数值就是向量中的***\*缺失值个数\****。

第二步再使用`table(is.na(vector_test))`分别给出向量`vector_test`中的正常值与缺失值的个数，如图所示，分别为`8`和`2`。

![img](https://www.educoder.net/attachments/download/201698)

为了求出正常值与缺失值相对应的***\*占比\****，我们在`table(is.na(vector_test))`已经给出了每种类型数据数目的基础上，调用函数`prop.table(table(is.na(vector_test)))`便能求出各自的***\*占比\****，分别为`0.8`与`0.2`，但是需要注意的是，此处输入时有两个`table`。

在介绍完较为简单的***\*向量缺失值识别方法\****后，下面我们再来看看***\*数据框\****中的缺失值识别，我们还是使用`foreignteacher`数据框，其中包含了`teacher, country, age, gender`四个向量，如图所示：

![img](https://www.educoder.net/attachments/download/201701)

依旧调用函数`is.na()`来识别数据框中的缺失值，对于数据框而言，`is.na()`返回的是跟被检测***\*数据同等大小的对象\****，如果某个数据框元素为缺失值，则其输出的对应元素为`TRUE`。

![img](https://www.educoder.net/attachments/download/201702)

我们仍然调用函数`sum`、`table`以及`prop.table`来具体求得数据框中确实值得具体占比信息，如下所示，在`foreignteacher`数据框中，缺失值占比`0.15`。

![img](https://www.educoder.net/attachments/download/201703)

由于本关卡分别介绍了向量与数据框的缺失值识别方法，且细节较多，那么我们本次的`GIF`补漏也将分为两个部分，如下所示：

向量环节：

![img](https://www.educoder.net/attachments/download/201704)

数据框环节：

![img](https://www.educoder.net/attachments/download/201705)

#### 编程要求

本关涉及的代码文件为`NA_re.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 将`2，43，56，12，34，NA，349，123，13，45`赋值给向量`handsomeboy`；
- 将如下的四个向量：
  `teacher：c(1,2,3,4,NA)`
  `country： c("Can", "US", "RUS", "UK", "NL")`
  `age：c(NA, 29, 55, NA, 143)`
  `gender：c("M","F","M","F","M")`
  赋值给数据框`foreignteacher`；
- 使用调用函数`is.na、sum、table、prop.table`分别求出向量`handsomeboy`以及数据框`foreignteacher`的缺失值位置、缺失值总数、正常值与缺失值个数、缺失值占比。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`NA_re.R`，平台将运行用户补全的`NA_re.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/201717)

#### My_Answer

```r
#####	NA_remove.R#####

###### begin ######
#Output the result.
handsomeboy<-c(2,43,56,NA,34,NA,349,NA,13,45)
teacher<-c(1,NA,3,4,NA)
country<-c("Can","US","RUS","UK","NL")
age<-c(NA,29,55,62,NA)
gender<-c("M","F","M","F","M")
foreignteacher <- data.frame(teacher,country,age,gender)
sum_h<-sum(na.omit(handsomeboy))
mean_h<-mean(na.omit(handsomeboy))
new_frame<-na.omit(foreignteacher)



###### end ######
sum_h
mean_h
str(new_frame)
```

### 第二关：缺失值处理--删除法

#### 任务描述

我们在第一关学习了如何***\*识别缺失值\****，在第二关学习了最基本的***\*缺失值删除法\****，但是如果缺失值数量较大，或者其分布极其不均匀，极端情况就是数据框的每一行都包含至少一个缺失值，那么此时还使用删除法，对于数据分析来说就是致命的，因此我们将在本关介绍处理缺失值的***\*数值替代方法\****。

#### 相关知识

对于缺失值的处理，就好比是中医和西医，西医主张***\*连根拔起\****，而中医倾向***\*调理维护\****，连根拔起就像是上一关所讲的删除法，简单暴力而又直接了当，***\*但并不是所有场景都适合\****，比如得了肿瘤当然需要切除，但是如果只是崴个脚就要截肢那谁愿意？

首先我们介绍使用***\*替代值\****的方式***\*处理缺失值\****，缺失值的产生是由于数据收集装置的***\*失灵、不稳定或者其他人为因素\****等，所以无论如何，缺失值所在的位置原本应该是有一个***\*正常值\****存在的，因此第一个应该想到的思路就是利用现有的***\*正常值来估计缺失值\****本来的面貌—-当一组数据符合正太分布时，我们知道正太分布大多数都集中在一起，所以使用***\*平均值\****替代缺失值，如下所示：

![img](https://www.educoder.net/attachments/download/201955)

在数据框中有一个向量`teacher<- c(1,2,3,4,NA)`的第五项为缺失值，假设其余数据符合***\*正太分布\****，那么我们调用

`foreignteacher[5,"teacher"] <- mean(foreignteacher$teacher,na.rm = T)`来将向量`teacher`的平均值赋值给缺失值部分，再利用`view`命令可以看到，我们已经成功将平均值`2.5`输入到缺失值部分。

那么如果一组包含缺失值的数据符合***\*偏态分布\****呢？那么显然我们可以使用数据的***\*中位数\****来替代出现缺失值的部分，如下所示：

![img](https://www.educoder.net/attachments/download/201956)

向量`teacher`的第三项为缺失值，我们假设向量符合***\*偏态分布\****，然后调用`foreignteacher[3,"teacher"] <- median(foreignteacher$teacher,na.rm = T)`来将向量的***\*中位数\****赋值给缺失值，如图上方所示，我们成功将向量`teacher`的第三项缺失值改为了中位数。

我们再来思考一种情况，古人云***\*人以群分，物以类聚\****，说明什么问题，事物更加倾向于和自己相像的事物接近。这好像现在大火的机器学习，好多朋友调侃这其实是个***\*调参工程师\****的职业，其基本原理其实就是从历史数据中不断学习不断修改各层参数，以求能够更加精准地预测未来，那么根基是什么呢？当然是一个事物的数据集是有***\*规律可循\****的，是相似的。对于缺失值来讲，如果它所在的其他数据中有很多不断重复的数值，我们称之为***\*众数\****，那么这个缺失值也***\*大概率\****可能就是这个众数，那么大家首先需要掌握的就是怎么求众数，独家秘方，看好了（因为`R`中是没有自带求众数的函数）：

![img](https://www.educoder.net/attachments/download/202002)

利用`max(table(vector))`找到众数出现的次数为`8`，然后利用`table(vector)==max(table(vector))`的逻辑值判断出众数的具体数值，并将其逻辑值赋值为`TRUE`。

![img](https://www.educoder.net/attachments/download/202004)

然后使用`as.numeric`将众数的数据类型转换为`numeric`型，最后输出众数`2`，由于R中没有默认的求众数的函数，这是笔者自创，大家如果一时不能理解没有关系，***\*因为这不是目前的重点\****，只需拷贝下来或者记住即可，我们在后续讲解高阶运算函数的时候会再具体讲解。

![img](https://www.educoder.net/attachments/download/202005)

最后我们按照`frame[9,"A"] <- as.numeric(names(table(A)))[table(A) == max(table(A))]`将数据框`frame`中缺失值（位于***\*第九个元素\****处） 赋值为向量整体的***\*众数\****，即为`2`。

总结一下，本关卡介绍了以存在缺失值的向量的***\*平均值、中位数以及众数\****来替代缺失值的办法，后续还有更为进阶的***\*回归方法\****，我们将在后续中级课程中予以讲授，敬请期待，那么现在依然是我们的补漏`GIF`环节：

![img](https://www.educoder.net/attachments/download/202006)

#### 编程要求

本关涉及的代码文件为`NA_re.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 将如下的四个向量：
  `A：c(2,2,3,2,NA,2,4,5,6,7)`
  `B： c(45,29,55,62,12,11,13,14,15,16)`
  赋值给数据框`frame`；
- 分别将向量`A`的平均值、中位数以及众数赋值给向量`A`中的缺失值，在每完成一次后使用`str`查看数据框详情，然后再重新按照第一条的数据框原始数据形式初始化包含缺失值的数据框`frame`，继而进行后续的缺失值替换。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`NA_re.R`，平台将运行用户补全的`NA_re.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/202007)

![img](https://www.educoder.net/attachments/download/202008)

![img](https://www.educoder.net/attachments/download/202009)

#### My_Answer

```r
#####	NA_remove.R#####

###### begin ######
#Output the result.
handsomeboy<-c(2,43,56,NA,34,NA,349,NA,13,45)
teacher<-c(1,NA,3,4,NA)
country<-c("Can","US","RUS","UK","NL")
age<-c(NA,29,55,62,NA)
gender<-c("M","F","M","F","M")
foreignteacher <- data.frame(teacher,country,age,gender)
sum_h<-sum(na.omit(handsomeboy))
mean_h<-mean(na.omit(handsomeboy))
new_frame<-na.omit(foreignteacher)



###### end ######
sum_h
mean_h
str(new_frame)
```

### 第三关：缺失值替代法

#### 任务描述

我们在第一关学习了如何***\*识别缺失值\****，在第二关学习了最基本的***\*缺失值删除法\****，但是如果缺失值数量较大，或者其分布极其不均匀，极端情况就是数据框的每一行都包含至少一个缺失值，那么此时还使用删除法，对于数据分析来说就是致命的，因此我们将在本关介绍处理缺失值的***\*数值替代方法\****。

#### 相关知识

对于缺失值的处理，就好比是中医和西医，西医主张***\*连根拔起\****，而中医倾向***\*调理维护\****，连根拔起就像是上一关所讲的删除法，简单暴力而又直接了当，***\*但并不是所有场景都适合\****，比如得了肿瘤当然需要切除，但是如果只是崴个脚就要截肢那谁愿意？

首先我们介绍使用***\*替代值\****的方式***\*处理缺失值\****，缺失值的产生是由于数据收集装置的***\*失灵、不稳定或者其他人为因素\****等，所以无论如何，缺失值所在的位置原本应该是有一个***\*正常值\****存在的，因此第一个应该想到的思路就是利用现有的***\*正常值来估计缺失值\****本来的面貌—-当一组数据符合正太分布时，我们知道正太分布大多数都集中在一起，所以使用***\*平均值\****替代缺失值，如下所示：

![img](https://www.educoder.net/attachments/download/201955)

在数据框中有一个向量`teacher<- c(1,2,3,4,NA)`的第五项为缺失值，假设其余数据符合***\*正太分布\****，那么我们调用

`foreignteacher[5,"teacher"] <- mean(foreignteacher$teacher,na.rm = T)`来将向量`teacher`的平均值赋值给缺失值部分，再利用`view`命令可以看到，我们已经成功将平均值`2.5`输入到缺失值部分。

那么如果一组包含缺失值的数据符合***\*偏态分布\****呢？那么显然我们可以使用数据的***\*中位数\****来替代出现缺失值的部分，如下所示：

![img](https://www.educoder.net/attachments/download/201956)

向量`teacher`的第三项为缺失值，我们假设向量符合***\*偏态分布\****，然后调用`foreignteacher[3,"teacher"] <- median(foreignteacher$teacher,na.rm = T)`来将向量的***\*中位数\****赋值给缺失值，如图上方所示，我们成功将向量`teacher`的第三项缺失值改为了中位数。

我们再来思考一种情况，古人云***\*人以群分，物以类聚\****，说明什么问题，事物更加倾向于和自己相像的事物接近。这好像现在大火的机器学习，好多朋友调侃这其实是个***\*调参工程师\****的职业，其基本原理其实就是从历史数据中不断学习不断修改各层参数，以求能够更加精准地预测未来，那么根基是什么呢？当然是一个事物的数据集是有***\*规律可循\****的，是相似的。对于缺失值来讲，如果它所在的其他数据中有很多不断重复的数值，我们称之为***\*众数\****，那么这个缺失值也***\*大概率\****可能就是这个众数，那么大家首先需要掌握的就是怎么求众数，独家秘方，看好了（因为`R`中是没有自带求众数的函数）：

![img](https://www.educoder.net/attachments/download/202002)

利用`max(table(vector))`找到众数出现的次数为`8`，然后利用`table(vector)==max(table(vector))`的逻辑值判断出众数的具体数值，并将其逻辑值赋值为`TRUE`。

![img](https://www.educoder.net/attachments/download/202004)

然后使用`as.numeric`将众数的数据类型转换为`numeric`型，最后输出众数`2`，由于R中没有默认的求众数的函数，这是笔者自创，大家如果一时不能理解没有关系，***\*因为这不是目前的重点\****，只需拷贝下来或者记住即可，我们在后续讲解高阶运算函数的时候会再具体讲解。

![img](https://www.educoder.net/attachments/download/202005)

最后我们按照`frame[9,"A"] <- as.numeric(names(table(A)))[table(A) == max(table(A))]`将数据框`frame`中缺失值（位于***\*第九个元素\****处） 赋值为向量整体的***\*众数\****，即为`2`。

总结一下，本关卡介绍了以存在缺失值的向量的***\*平均值、中位数以及众数\****来替代缺失值的办法，后续还有更为进阶的***\*回归方法\****，我们将在后续中级课程中予以讲授，敬请期待，那么现在依然是我们的补漏`GIF`环节：

![img](https://www.educoder.net/attachments/download/202006)

#### 编程要求

本关涉及的代码文件为`NA_re.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 将如下的四个向量：
  `A：c(2,2,3,2,NA)`
  `B： c("Can", "US", "RUS", "UK", "NL")`
  `C：c(45, 29, 55, 62, 12)`
  `D：c("M","F","M","F","M")`
  赋值给数据框`frame`；
- 分别将向量`A`的平均值、中位数以及众数赋值给向量`A`中的缺失值，在每完成一次后使用`str`查看数据框详情，然后再重新按照第一条的数据框原始数据形式初始化包含缺失值的数据框`frame`，继而进行后续的缺失值替换。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`NA_re.R`，平台将运行用户补全的`NA_re.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/202007)

![img](https://www.educoder.net/attachments/download/202008)

![img](https://www.educoder.net/attachments/download/202009)

#### My_Answer

```r
#####	NA_mo.R#####
  
  ###### begin ######
#Output the result.
A<-c(2,2,3,2,NA,2,4,5,6,7)
B<-c(45,29,55,62,12,11,13,14,15,16)
frame<-data.frame(A,B)
frame[5,"A"]<-mean(frame$A,na.rm=T)
str(frame)
frame<-data.frame(A,B)
frame[5,"A"]<-median(frame$A,na.rm=T)
str(frame)
frame<-data.frame(A,B)
frame[5,"A"]<-as.numeric(names(table(A)))[table(A)==max(table(A))]
str(frame)


###### end ######
```

## 实训六：日期值与时间值

### 第一关：日期型数据输入

#### 任务描述

说到***\*日期值\****，大家的第一反应是什么，没错，年月日对吧。相信大家也都在人生的各个阶段填过无数的表格，升学要填表，求职要填表，入职也要填表，就连入职体检也有表格，而表格当中除了姓名等关键信息之外还有一项必填—-那就是出生年月。而这个出生年月我相信大家也肯定填过各种版本，比如`1990-11-26`或者`1990.11.26`又或者是`1990-11`等等，那么在`R`中到底应该如何填写呢？

![img](https://www.educoder.net/attachments/download/202304)

#### 相关知识

##### 标准日期输入格式

首先我们来做一个***\*错误\****的示范，比如我们当前需要输入一个日期值为`1990年11月26日`，如下所示：

![img](https://www.educoder.net/attachments/download/202308)

可以清楚地看到程序报错`Error in charToDate(x) : cha\fracter string is not in a standard unambiguous format`，说明我们输入的日期值不是***\*标准的格式\****，那么怎样的才是标准的日期格式输入呢？

`在Rstudio`中，自带了`as.Date`作为日期值的输入函数，而`as.Date`中的参数格式主要分为两种：

```
年-月-日
年/月/日
```

如果不是以上两种格式，则会提供错误——错误于`charToDate(x)`: 字符串的格式不够标准明确。那么正确的日期值输入格式如下：

![img](https://www.educoder.net/attachments/download/202309)

所以正确的日期值输入应该是`as.Date("1990-11-26")`或者是`y<-as.Date("1990/11/26")`，除开上述两种的其他任何形式***\*都不能被正确输入\****。

结束了吗？当然没有，在使用`as.Date`输入日期值时，还可以***\*任意地变换\****输入时年月日的位置，但是都必须遵照`format='%Y-%m-%d'`的格式，也就是说语句`as.Date('1990-11-26',format='%Y-%m-%d')`中前后的日期输入格式必须***\*相匹配\****，其中：

- %Y表示年，必须四位数字表示；
- %m表示月份；
- %d表示日期。

![img](https://www.educoder.net/attachments/download/202311)

##### 日期输入方法延伸

除此之外，对于年和月还有几种较为***\*特殊\****的输入方法：

- %b：月份，缩写；
- %B：月份，完整的月份名，指英文；
- %y：年份，以二位数字表示。

具体的输入方法如图所示，小写的`y`表示年份的输入格式时，只能输入年份的***\*两位数字\****表示，比如`1990`需要写作`90`，而月份的小写`b`表示时，输入英文缩写即可，比如八月写作`Aug`，而大写`B`表示月份格式时，就必须写作`June、January`等英文全称：

![img](https://www.educoder.net/attachments/download/202312)

最后我们将按照`as.Date`输入日期值的方法梳理到汇总的动态展示图中，不少的操作细节还是需要大家记忆的，实在记不住没关系，反正实训在这儿，随时来学：

![img](https://www.educoder.net/attachments/download/202314)

#### 编程要求

本关涉及的代码文件为`R_date.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 使用`as.Date`分别将日期`1990.11.26；2000.01.01`按照`年-月-日`赋值给`date1、date2`；
- 将日期`2003.04.11；2018.01.18`按照`年/月/日`赋值给`date3、date4`；
- 使用`as.Date`将日期`1990.11.26`分别按照格式`%Y-%b-%d`；`%Y-%B-%d`；`%y-%b-%d`；`%y-%B-%d`输入到`date5、date6、date7、date8`中。

> 提示： `11月`英文简写 `Nov`，全称`November`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_date.R`，平台将运行用户补全的`R_date.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/202833)

#### My_Answer

```r
#####	R_date.R#####

###### begin ######
#Output the result.
date1<-as.Date("1990-11-26")
date2<-as.Date("2000-01-01")
date3<-as.Date("2003-04-11")
date4<-as.Date("2018-01-18")
date5<-as.Date("1990-11-26")
date6<-as.Date("1990-11-26")
date7<-as.Date("1990-11-26")
date8<-as.Date("1990-11-26")


###### end ######
date1
date2
date3
date4
date5
date6
date7
date8
```

### 第二关：时间值

#### 任务描述

对于日期值的输入，更准确来讲是对于时间值的输入，除了基本的年月日外，还有真正意义上的时间，即***\*时分秒\****。而对于精确时间的输入和存储，使用第一关中的`as.Date`是无法完成的，因此，我们将在本关卡具体讲解如何实现***\*精确时间的输入\****。

![img](https://www.educoder.net/attachments/download/202343)

#### 相关知识

##### `POSIXlt`函数

我们首先以***\*系统时间\****作为本关卡讲解的示例，如下所示，使`today<-Sys.time()`将当前的系统时间赋值给变量`today`：

![img](https://www.educoder.net/attachments/download/202345)

我们可以得到当前的系统时间为`2018-06-02 15:10:11`，但是如果我们需要调用其中的年月日或者是时分秒等详细数据怎么办呢？我们首先介绍函数`POSIXlt`。在讲解`POSIXlt`函数之前，我们首先需要知道`POSIXlt`函数的***\*存储机制\****，在了解其存储机制之前，我们需要首先解释下`unclass`函数的定义，`unclass`可以将日期变成以回归年`1900`的差值来计数，比如`1900-02-01`输出的`31`，就代表着距离`1900-01-01`有`31`天，而如果我们当前的时间为`2018-06-02 15:10:11`，如下所示：

![img](https://www.educoder.net/attachments/download/202349)

我们可以清楚地看到，`POSIXlt`函数采用的是***\*打散时间\****，把时间分成***\*年、月、日、时、分、秒\****，并进行存储。而有的眼尖的同学可能会问，这个输出不对啊，为什么年份那一项写的是`118`，因为这个时间参考的是***\*回归年\****，而回归年定义在了`1900`年，也就是说使用`unclass`输出的是当前时间到回归年之间的***\*差值\****，所以是`118`年，而又有人可能会问那月份为什么是`5`而不是`6`，因为系统默认***\*一月\****是`0`，所以六月对应就是`5`。

在了解了`POSIXlt`函数的***\*存储机制\****后，我们下面讲授如何具体取出对应的日期或者是精确时间，首先是最基本的求解当前的对应的***\*星期信息\****以及年内已经过的***\*天数\****，如下所示：

![img](https://www.educoder.net/attachments/download/202353)

第一步是将得到的系统时间转存至变量`date`，可以看到使用命令`date$wday`可以准确得到当前是***\*星期六\****，而使用`date$yday`可以求得本年已经历的***\*天数\****。除了基本的星期和天数外，如何截取出更为关键的***\*日期和精确时间\****呢？如下所示：

![img](https://www.educoder.net/attachments/download/202355)

我们可以观察一下，我们以系统时间为例，`"2018-06-02 15:45:58 CEST"`这显然是一个`char`类型数据，所以我们只需要截取出第`1`位到第`10`位元素，将其输出便能得到***\*日期数据\****，再将其第`12`位到第`19`位数据输出，便能得到***\*精确的时间数据\****，没看明白的同学，数一数上面的***\*时间位数\****便知。

##### POSIXct函数

在本关卡的讲授中，除了上面提到的`POSIXlt`函数，`R`还提供了`POSIXct`函数，作用跟`POSIXlt`大同小异，只是`POSIXlt`以秒进行存储，如下所示：

![img](https://www.educoder.net/attachments/download/202357)

##### unlist函数

如果各位觉得使用`unclass`展示出的时间变现形式`占地太大`，给大家推荐一个私人秘籍，我们可以结合`unlist`命令将`unclass`输出的时间***\*列表化\****，如下所示：

![img](https://www.educoder.net/attachments/download/202360)

这一关卡不知大家是否已经掌握，又是时间差值，又是时间打散存储，细节较多需要各位***\*不断打磨记忆\****，还是老规矩，***\*巩固时间段\****：

![img](https://www.educoder.net/attachments/download/202411)

#### 编程要求

本关涉及的代码文件为`R_time.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 使用`as.POSIXlt`函数将已给定的时间数据，打散赋值给`sysdate`，在此基础上将星期信息赋值给`day`，将目前已经历的时间赋值给`alreadydate`；
- 将系统时间的日期部分取出赋值给`date`，将精确的时分秒部分赋值给`time`；
- 基于`POSIXlt`函数，使用`unlist`以及`unclass`结合的方式，列表化输出给定的时间至变量`list`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_time.R`，平台将运行用户补全的`R_time.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/202831)

#### My_Answer

```r
#####	R_time.R#####
systime<-"2018-06-02 16:47:54 CEST"
  ###### begin ######
#Output the results.
x=as.POSIXlt(systime)
day=x$wday
alreadydate=x$yday
date=substr(as.character(systime),1,10)
time=substr(as.character(systime),12,19)
list=unlist(unclass(as.POSIXlt(systime)))


###### end ######
day
alreadydate
date
time
list
```

### 第三关：日期与时间的计算

#### 任务描述

本次实训的主题叫做***\*日期值与时间值\****，我们应该形成一种感觉，凡是被叫做什么***\*值\****，那它就一定是可以被用来***\*计算\****的，否则就无法被称作`XX`数值，而时间值、日期值也不例外，比如我们现在知道了两个具体的日期值，想要知道中间差着多少天，那么我们就需要进行相应的***\*日期值计算\****，本关将为大家讲解如何进行日期值与时间值的计算。

#### 相关知识

##### 基于`POSIXlt`函数的差值运算

简单来讲，对于日期和时间，我们可以进行如下的***\*四类计算\****：

- 时间 + 数字；
- 时间 - 数字；
- 时间`1` - 时间`2`；
- 时间`1` “逻辑运算” 时间`2`。

我们可以让一个日期时间对象***\*加减一个秒数\****或者一个***\*时间差\****，但是不允许对两个日期时间对象进行相加。两个日期时间对象的相减等同于使用 `difftime`。如果计算中没有指定时区的话，我们关卡二中所介绍的`POSIXlt`对象会默认使用当前时区。

敲黑板了！需要特别强调的是，我们在进行任何计算之前，都应该将所需要计算的日期或者时间换成`POSIXlt`打散存储的对象。然后就可以直接计算平均值、差值等等。

![img](https://www.educoder.net/attachments/download/202393)

首先分别使用`as.POSIXlt("1990-11-26")`将两个日期打散存储，然后直接进行日期的***\*差值运算\****，得到结果为`1036`天，这是最为基本的日期差值运算，需要注意的是，你不能对日期进行***\*加和\****，这个道理也非常好懂，因为没有一个起始日期作为参考值，你就无从进行加和，比如`1990`年在加和运算中，到底是作为多少年呢？没人能够完美解释。

同样的道理，使用`POSIXlt`处理后的时间值也可以轻松进行差值运算求出***\*两个精确时间之间的差值\****，如下所示：

![img](https://www.educoder.net/attachments/download/202395)

我们可以看到得到的时间差值其结果***\*输出形式\****可以是多少天，也可以是多少小时，这完全取决于***\*结果的大小\****，`R`会自动给出一个合理的时间单位。

##### difftime函数

对于***\*日期和时间的差值运算\****，我们前面讲过应该建立在`POSIXlt`函数的基础上，大家请注意我们的用词，***\*是应该而不是必须\****，所以这一点是有捷径可以走的，我们可以直接调用`difftime`函数进行日期和时间的***\*差值运算\****，如下所示：

![img](https://www.educoder.net/attachments/download/202396)

我们可以调用`difftime("2000-12-21", "2001-3-11")`计算两个日期的差值，结果可以发现，如果将***\*较新\****的日期放在后面，则结果为***\*负数\****，反之为***\*正数\****，有些时候我们在某些计算中只需要使用天数的***\*具体数值\****，那么我们可以调用`as.numeric(difftime("2001-3-11","2000-12-21"))`直接取得差值的具体数值。

使用`difftime`函数对时间值进行差值运算也是可行的，如下所示，输出结果的正负也与新旧时间值的位置直接相关，即较新的值在后时，输出结果为负：

![img](https://www.educoder.net/attachments/download/202407)

最后，我们可以使用`as.difftime`函数把字符转换成`difftime`对象，如下所示，其差值的处理方法都是求解当前时间与***\*零点之间的差值\****：

![img](https://www.educoder.net/attachments/download/202408)

当然，使用`as.difftime`函数时，我们可以自行***\*定义时间的格式\****，举个例子，实际操作时可能没有关于秒的信息，此时我们将时间用小时和分钟分别用`%H`和`%M`表示，如图所示：

![img](https://www.educoder.net/attachments/download/202409)

当时间信息中的小时或者分钟信息不完整时，输出的结果为如图所示的缺失值。我们来总结一下，本关卡主要学习了***\*日期值和时间值的几种差值求解方法\****，以及***\*基于零时刻的差值运算\****。最后依然是巩固环节：

![img](https://www.educoder.net/attachments/download/202410)

#### 编程要求

本关涉及的代码文件为`R_date_compute.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 分别使用`POSIXlt`函数将日期

`1980-11-26、1978-01-25、2018-06-21 09:24:12、2017-07-12 09:24:12`赋值给`date1、date2、date3、date4`；

- 将`date1-date2`赋值给`result1`，将`date3-date4`赋值给`result2`；
- 使用`difftime`函数计算`1980-11-26`与`1978-01-25`的差值，结果赋值给`result3`;
- 计算`2018-06-21 09:24:12`和`2017-07-12 09:24:12`的差值，结果赋值给`result4`；
- 使用`as.numeric`取出时间`2016-05-21 06:24:12`和`2015-07-11 03:21:11`的具体差值并赋值给`result5`；
- 使用函数`as.difftime`求取时间`04:22`、`22:12`以及`：34`与零时刻的差值，并将结果赋值给`result6`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_date_compute.R`，平台将运行用户补全的`R_date_compute.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/202832)

#### My_Answer

```r
#####	R_date_compute.R#####

  ###### begin ######
#Output the results.
date1=as.POSIXct("1980-11-26")
date2=as.POSIXlt("1978-01-25")
date3=as.POSIXlt("2018-06-21 09:24:12")
date4-as.POSIXlt("2017-07-12 09:24:12")
result1=date1-date2
result2=date3-date4
result3=difftime(date1,date2)
result4=difftime(date3,date4)
result5=as.numeric(difftime("2016-05-21 06:24:12","2015-07-11 03:21:11"))
result6=as.difftime(c("04:22","22:12",":34"),format = "%H:%M")#不需要输入零点时刻 
###### end ######
result1
result2
result3
result4
result5
result6
```

## 实训七：时点类函数

### 第一关：R自带的时点类函数

#### 任务描述

`R`中其实有不少比较实用的时点类函数，我们在上一实训末尾介绍的几个时点计算方法算是其中的基础，而对于日期以及时间的相关时点处理，除了在上一个实训中提到的**差值运算**，还有很多高阶处理手段，比如日期或者时间的**分组、关键日期（或时间）信息提取**等。

我们将在本关介绍`Rstudio`中相关**自带函数**的使用方法。

#### 相关知识

##### 基本的时间信息提取函数

比如我现在给大家一串数字`2015-11-26`，大家第一反应估计是，这是一个日期，没错，这的确是一个日期，但是光靠这个日期又能得到什么呢？我们需要的当然不仅仅是一串日期数字，而是其中亟待挖掘的**时间信息**，我们将以**三个信息挖掘函数**为切入点，如下所示：

![img](https://www.educoder.net/attachments/download/202596)

使用函数`weekdays()`可以一步到位求出所给定时间的**星期信息**，很巧的是，我们举的三个例子都指向了星期一。

我们还可以使用如下所示的函数`months()`提取出给定**日期的月份**，有的同学可能会说，你都已经给出了日期信息，难道我还看不出来月份吗？没错，你当然可以肉眼看得出来，但是我现在给你成千上万条数据，让你最快速度给出所有的月份信息，你还用肉眼？

![img](https://www.educoder.net/attachments/download/202597)

除了上述的星期信息、月份信息，我们还可以使用函数`quarters`来提取出给定**日期的季度信息**，如下所示：

![img](https://www.educoder.net/attachments/download/202598)

##### 基于`format`的时间信息提取函数

我们不仅能通过`R`实现**星期、月份以及季度信息**的提取，还能**自定义提取**日期的部分信息，需要使用的函数即`format`，调用函数`format(today,format="%B-%d-%Y")`即可实现，其中的`format="%B-%d-%Y`部分可以自定义需要的日期信息，如下所示：

![img](https://www.educoder.net/attachments/download/202600)

我们可以看到，使用函数`format`可以任意自定义地提取出日期中的所有信息，需要注意的是，函数`format`可以识别`as.Data`型以及`POSIXct`与`POSIXlt`型，所以在使用前，需要将日期值**转换**为上述三种类型之一。

接下来便是日期分组，我们如何实现日期的分组呢？需要使用到的函数是`cut`，首先我们使用`as.Date`将一连串日期输入给变量`date`，然后使用`cut`以月份作为分组标准将日期信息进行**分类**，如下所示：

![img](https://www.educoder.net/attachments/download/202602)

除了月份标准分类，我们还可以按照`year`年进行分类：

![img](https://www.educoder.net/attachments/download/202603)

得到的分类结果为`11`级，从`1980`年开始，到`1990`年截至，所给定的日期总占有所有分类的其中**四份**。

最后依然是的巩固的`GIF`环节：

![img](https://www.educoder.net/attachments/download/202701)

#### 编程要求

本关涉及的代码文件为`R_date_adv.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 将日期信息`1990-11-26 01:00:00`赋值给`date`，分别使用自带函数提取其中的星期、月份、季度信息赋值给变量`week、month、quarter`；
- 使用`format`函数按照**月日年**的顺序提取出`date`中的日期信息，并赋值给变量`rec`；
- 将下述四个日期信息赋值给变量`date_mass` ：
  `1990-11-26`
  `1980-07-04`
  `1988-03-01`
  `1990-09-15`

分别按照月份和年对`date_mass`进行分类，然后将分类结果分别赋值给变量`date.bymonth`以及`date.byyear`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_date_adv.R`，平台将运行用户补全的`R_date_adv.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/202834)

#### My_Answer

```r
#####	R_date_adv.R#####

###### begin ######
#Output the result.
date=as.Date("1990-11-26 01:00:00")
week=weekdays(date)
month=months(date)
quarter=quarters(date)
rec=format(date,format="%B-%d-%Y")
date_mass=as.Date(c("1990-11-26","1980-07-04","1988-03-01","1990-09-15"))
date.bymonth=cut(date_mass,breaks="month")
date.byyear=cut(date_mass,breaks="year")

###### end ######
week
month
quarter
rec
date.bymonth
date.byyear
```

### 第二关：lubridate包的时点类函数一

#### 任务描述

用过`R`的朋友们相信一定不会对`Hadley·Wickham`这个名字有所陌生，作为`RStudio`的`Chief Scientist`，他为`R`用户贡献了多个重量级的`package`（`ggplot2、dplyr`等等）。而今天介绍的这个`lubridate`包，也是由他所编写，专注于对日期时间数据（`Date-time data`）的处理。

我们也将在本关为大家介绍`lubridate`包中的**解析与提取类时点函数**。

![img](https://www.educoder.net/attachments/download/202608)

#### 相关知识

##### 解析类函数

对于`lubridate`包其处理日期和时间的功能极其强大，远高于`Rstudio`中自带的一些基础包的功能，我们首先为大家讲解其中的解析与提取类时点函数。什么是**时点类函数**呢？这是用来区别于时段类函数，即某一个精确的日期或者时间。

第一类函数为**解析类**，作用为根据给出的日期或者时间格式，**精确解析出给定的日期或者时间，并以标准形式输出**，如下所示：

![img](https://www.educoder.net/attachments/download/202622)

要使用`lubridate`包，第一步需要调用`library(lubridate)`载入对应包。对于日期信息的解析，我们可以任意地变换`ymd`中三个字母的顺序，来适应需要解析的日期格式，其中`y`代表年，`m`代表月，`d`代表日。除此之外，**时间信息也可以解析输出出标准格式**，如下所示：

![img](https://www.educoder.net/attachments/download/202623)

但在时间信息的解析中，有一点需要注意`hms`不能随意变换，只能按照`hms`这一固定顺序，但是其中的时间分隔符可以随意定义，支持多种分隔符形式，比如图中的`,` `.` `/`等等。

![img](https://www.educoder.net/attachments/download/202624)

`lubridate`包还可以处理日期和时间信息的组合形式，如上图中所示的`ymd_hms`或者`dmy_hms`等形式。

##### 提取类函数

在**时点类函数**中，还有一个重要功能便是`提取`，比如提取出给定日期中的**时分秒、星期信息以及所属月份最大天数**等，首先是最为基础的时分秒信息的提取，调用`hour()` `minute()` `second()`如图所示：

![img](https://www.educoder.net/attachments/download/202626)

然后是天数、月份、年份信息的提取，分别调用`day()` `month()` `year()`，如图所示：

![img](https://www.educoder.net/attachments/download/202627)

最后是更深入的信息的提取，比如调用函数`yday`求出当前是一年中的第多少天，调用函数`week`求出当前是一年中的第几个星期，以及调函数`days_in_month`求出当前月的最大天数，如图所示：

![img](https://www.educoder.net/attachments/download/202629)

最后依然是的巩固的`GIF`环节：

![img](https://www.educoder.net/attachments/download/202699)

#### 编程要求

本关涉及的代码文件为`R_lu_1.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 使用命令`library()`载入`lubridate`包；
- 使用`ymd`将日期`1990/11/26`解析输出到变量`X`，使用`hms`将时间`11/22/36`解析输出到变量`Y`，使用`ymd_hms`将`1990/11/26 11.22.36`解析输出到变量`Z`；
- 使用`as.POSIXct`函数将`("1990-11-26 01:23:56")`赋值给变量`date`，分别实现如下功能：
  1.利用`hour`提取小时信息并赋值给变量`result1`；
  2.利用`minute`提取分钟信息并赋值给`result2`；
  3.利用`second`提取秒信息并赋值给`result3`。
- 面向变量`date`，提取出如下三种年月日信息：
  1.利用`day`提取出天数信息并赋值给`result4`；
  2.利用`month`提取出月份信息并赋值给`result5`；
  3.利用`year`提取出年份信息并赋值给`result6`。
- 面向变量`date`，提取出当前是一年的第多少天、多少周、本月最大天数，分别赋值给变量`result7`、`result8`以及`result9`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_lu_1.R`，平台将运行用户补全的`R_lu_1.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/202840)

#### My_Answer

```r
#####	R_lu_1.R#####

  ###### begin ######
#Output the results.
library(lubridate)
X=ymd("1990/11/26")
Y=hms("11/26/36")
Z=ymd_hms("1990/11/26 11,22,36")
date=as.POSIXlt("1990-11-26 01:23:56")
result1=hour(date)
result2=minute(date)
result3=second(date)
result4=day(date)
result5=month(date)
result6=year(date)
result7=yday(date)
result8=week(date)
result9=days_in_month(date)
###### end ######
X
Y
Z
result1
result2
result3
result4
result5
result6
result7
result8
result9
```

### 第三关：lubridate包的时点类函数二

#### 任务描述

`Hadley·Wickham`之于`R`绝对是一个泰山级的人物，由他抛出的多个包早已成为经典。目前我们所使用的`lubridate`包的官方描述其实只有短短一句话，翻译过来就是：**让时间处理更加简单**。在**时点类函数**中，除了第二关中所介绍的**解析与提取功能**，还有一类重要的函数功能—-**修改**，我们将在本关中具体讲解。

![img](https://www.educoder.net/attachments/download/202710)

#### 相关知识

##### 四舍五入取整

在`lubridate`中，对于时间点的修改方法都是基于一个大原则—那就是**取整**。第一大类：**四舍五入取整法**，如下所示：

![img](https://www.educoder.net/attachments/download/202711)

分别调用`round_date(date,unit='second')`、`round_date(date,unit='minute')`、`round_date(date,unit='hour')`对所输入的时间进行**四舍五入取整**，从输出的取整结果来看，似乎看不出来这个四舍五入到底是如何实施的，但是看过下面这个例子之后，将会更有助于大家理解：

![img](https://www.educoder.net/attachments/download/202777)

从上面的两个结果我们可以看到的是，对于秒来说是**不能进行四舍五入操作**的，因为秒是目前这个时间格式的最小一级，没有其涵盖的下级时间单位，因为不能执行取整；而分钟的取整结果是取决于秒钟的大小，超过`30`秒，则分钟`＋1`，小时的运算方式也是如此，当分钟超过`30`分时，向前**进一位**。

##### 向下取整

除了利用**四舍五入**进行日期和时间的修改，在`luibridate`包中还有一种重要的修改手段—-**向下取整**，如图所示：

![img](https://www.educoder.net/attachments/download/202778)

调用`floor_date(date,unit='year')`便可实现向下取整，结果为`1990-01-01 CET`，即向下取整到`1990`年的第一天。当时间单位取到月份一级时，我们可以看到结果为`1990-11-01 CET`，即`11`月的第一天。

函数调用`floor_date`也适用于**小时和分钟**一级，如图所示：

![img](https://www.educoder.net/attachments/download/202779)

结果都是向下取整到当前所取得时间单位的值，比如调用`floor_date(date,unit='hour')`，得到的结果为`01：00：00`。

##### 向上取整

聪明的同学应该反应过来了，除了向下取整外，还应该有**向上取整**，没错，最后我们为大家讲授如何利用**向上取整**完成日期和时间的修改，如图所示：

![img](https://www.educoder.net/attachments/download/202780)

所谓向上取整原理很容易理解，就是当下一级时间单位**有取值且取值大于0**时，就将所取得时间单位上的值`＋1`，比如调用`ceiling_date(date,unit='year')`可以得到`1991`年，即在原`1990`年的基础上`＋1`。

![img](https://www.educoder.net/attachments/download/202781)

对于小时和分钟这样的时间单位也可以调用`ceiling_date(date,unit='hour')`或者`ceiling_date(date,unit='minute')`得到向上加一取整的修改效果。

最后依然是的巩固的`GIF`环节：

![img](https://www.educoder.net/attachments/download/202782)

#### 编程要求

本关涉及的代码文件为`R_lu_2.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 使用命令`library()`载入`lubridate`包；
- 调用函数`as.POSIXct`将`2018-06-04 12:33:36`赋值给`date`；
- 面向变量`date`，对`hour` `minute` `year` `month` `day` 按照四舍五入的方法进行修改，并将结果分别赋值给变量`result1—result5`；
- 面向变量`date`，对`hour` `minute` `year` `month` `day` 按照向下取整的方法进行修改，并将结果分别赋值给变量`result6—result10`；
- 面向变量`date`，对`hour` `minute` `year` `month` `day` 按照向上取整的方法进行修改，并将结果分别赋值给变量`result11—result15`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_lu_2.R`，平台将运行用户补全的`R_lu_2.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

·注：由于后台没有`add dbus`，所以导致会报警告：`Failed to create bus connection: No such file or directory. Warning message: running command 'timedatectl' had status 1`，并不会影响大家提交的代码评测，所以大家可以对输出的警告信息忽略不计。·

![img](https://www.educoder.net/attachments/download/202841)

#### My_Answer

```r
#####	R_lu_2.R#####

  ###### begin ######
#Output the results.
library(lubridate)
date=as.POSIXlt("2018-06-04 12:33:36")
result1=round_date(date,unit="hour")
result2=round_date(date,unit="minute")
result3=round_date(date,unit="year")
result4=round_date(date,unit="month")
result5=round_date(date,unit="day")
result6=floor_date(date,unit="hour")
result7=floor_date(date,unit="minute")
result8=floor_date(date,unit="year")
result9=floor_date(date,unit="month")
result10=floor_date(date,unit="day")
result11=ceiling_date(date,unit="hour")
result12=ceiling_date(date,unit="minute")
result13=ceiling_date(date,unit="year")
result14=ceiling_date(date,unit="month")
result15=ceiling_date(date,unit="day")

###### end ######
result1
result2
result3
result4
result5
result6
result7
result8
result9
result10
result11
result12
result13
result14
result15
```



## 实训八：时段类函数

### 第一关：时间之intervals

#### 任务描述

时段可以分为三大类，即`intervals`、`durations`和`periods`。其中最为基本的便是`intervals`间隔，本关卡将向大家讲授`intervals`的基本概念、创建方法以及相关运算法则。

#### 相关知识

##### 间隔的输入

间隔`intervals`是指特定的时间跨度。一个`interval`是两个**特定时刻**之间的时间。时间间隔的长度**从不模棱两可**，因为我们知道它的发生时间，任何时间都可以计算确切长度。

第一步是如何用间隔来表示一个时段，我们首先给出两对**起始时间与终止时间**，如下所示：

![img](https://www.educoder.net/attachments/download/202945)

然后我们调用函数`date1 <- interval(start1,end1)`将第一对起始终止时间赋值给间隔`date1`，如下所示，输出结果为`1990-11-26 12:00:00 UTC--2016-08-04 12:30:00 UTC`，正好是第一对起始与终止时间之间的间隔。

![img](https://www.educoder.net/attachments/download/202959)

##### 间隔的基本运算

当我们使用一个间隔来表示时段时，我们可以调用很多基本的**时段函数**来求取相关重要信息，第一个便是求出一个间隔中**所包含的具体时间**：

![img](https://www.educoder.net/attachments/download/202949)

通过调用函数`time_length(date1,'year')`**自定义时间单位**来输出间隔所包含的时间**总量**，支持的时间单位包括`second` `day` `month` `year`等。

其次是通过调用函数`int_overlaps(date1,date2)`来判断两个间隔之间是否有**重复**，如下所示:

![img](https://www.educoder.net/attachments/download/202953)

输出结果为`TRUE`即表示两个间隔存在重合，反之，输出为`FALSE`则表示两个间隔之间没有重合。

接下来是当我们已知具体时间间隔后，如何**求出其起始时间、终止时间**等信息，通过调用函数`int_start()` `int_end()`便可以求出给定间隔的起始时间与终止时间。如下所示：

![img](https://www.educoder.net/attachments/download/202957)

最后我们介绍间隔的**反转函数**`int_flip()`，通过调用函数`int_flip()`即可实现**起始时间与终止时间的互换**，如图所示：

![img](https://www.educoder.net/attachments/download/202968)

下面依然是我们为大家准备的**巩固环节**：

![img](https://www.educoder.net/attachments/download/202970)

#### 编程要求

本关涉及的代码文件为`R_interval.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 分别将时点`20141003,12:00:00`和`20151203,12:00:00`赋值给变量`start1`和`start2`，再分别将时点`20180904,12;30:00`和`20161022,12;30:00`赋值给变量`end1`和`end2`；
- 调用`interval`函数将时点`start1`和`end1`赋值给间隔`date1`，调用`interval`函数将时点`start2`和`end2`赋值给间隔`date2`；
- 调用函数`time_length`分别求出以下变量值：
   间隔`date1`包含多少年，赋值给`result1`；
   间隔`date1`包含多少月，赋值给`result2`；
   间隔`date1`包含多少日，赋值给`result3`；
   间隔`date1`包含多少小时，赋值给`result4`。
- 调用函数`int_overlaps`判断`date1`和`date2`是否有重合，将结果值赋值给`result5`；
- 调用函数`int_flip()`分别求出时段`date1`和`date2`反转后的时段形式，并赋值给`result6`、`result7`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_interval.R`，平台将运行用户补全的`R_interval.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/203362)

#### My_Answer

```r
#####	R_interval.R#####
library(lubridate)
###### begin ######
#Output the result.
start1=ymd_hms("20141003,12:00:00")
start2=ymd_hms("20151203,12:00:00")
end1=ymd_hms("20180904,12:30:00")
end2=ymd_hms("20161022,12:30:00")
date1=interval(start1,end1)
date2=interval(start2,end2)

result1=time_length(date1,'year')
result2=time_length(date1,'month')
result3=time_length(date1,'day')
result4=time_length(date1,'hour')
result5=int_overlaps(date1,date2)
result6=int_flip(date1)
result7=int_flip(date2)




###### end ######
date1
date2
result1
result2
result3
result4
result5
result6
result7
```

### 第二关：时段之duration

#### 任务描述

我们在第一关中介绍了时段的第一种表示方法—**间隔**，除了间隔这一种最为基本的时段表示方法外，如果我们从一个`interval`间隔中**删除开始和结束日期**，我们将得到一个可以添加到任何日期上的**通用的时间跨度**，这就是本关将要介绍的`durations`时间跨度。

#### 相关知识

##### 时间跨度duration的概念

何为`duration`呢？我们将一个间隔`interval`中的起始日期和终止日期删除，那么我们就能得到一个**绝对的时间跨度**，不受时间起始和终止的限制，对于`duration`时间跨度我们是固定用秒来作为时间单位，这也就说明`duration`时间跨度是一个精确的长度。

`duration`的长度与闰年、闰秒和夏时制无关，由于其以秒为单位计算，因此，`duration`具有**一致的长度**，不会因为计量时间单位的改变而改变，因此，我们不难理解不同的`durations`之间是能够相互**权衡大小的**。

##### 时间跨度duration的生成方法

如何生成一个**时间跨度**呢？主要的方法有**两种**，第一种是直接调用函数`duration()`，具体如下所示：

![img](https://www.educoder.net/attachments/download/203327)

通过调用函数`duration(60,"seconds")`便可得到一个`60`秒的时间跨度，而函数中的时间单位是可以**自定义**的，可以任意选取`years` `days`等，但是最终给出的输出形式都是以**秒作为时间单位**，这也是由时间跨度`duration`的定义所决定的，固定由秒来计量，且不受夏时令、闰年等影响，一年固定`365`天。

第二种方法是调用函数`dyears` `ddays`等来进行`duration`时间跨度的生成，具体方法如下所示：

![img](https://www.educoder.net/attachments/download/203329)

我们可以看到最终的生成结果和调用函数`duration()`是**一致**的，不知道各位同学有没有发现一个问题，那就是为什么上面两种方法都没有提到`month`？聪明的同学知道问题所在吗？因为时间跨度是一个**固定的衡量手段**，不能允许不一致的存在，而月份有`28`天，有`30`天，有`31`天，还有`29`天，**所以是没有办法一致衡量的**，如图所示，当使用`dmonth`时会报错。那有人又会问了，一年不也有`365`天和`366`天嘛，那是因为时间跨度`duration`**不考虑闰年**。

![img](https://www.educoder.net/attachments/download/203330)

##### duration的相关运算

 首先是将间隔`interval`转换为时间跨度`duration`，需要调用函数`as.duration()`，如下所示：

![img](https://www.educoder.net/attachments/download/203331)

通过调用函数`as.duration(date1)`和`as.duration(date2)`便可将间隔`interval`所囊括的**时间跨度**转换为`duration`型的时段。

接下来才是本关的重点，我们知道`duration`是固定使用秒来作为衡量的**时间单位**，因此这一性质决定了任何不同的`duration`之间是可以进行**基本运算**的，首先是**大小**的判断，如下所示：

![img](https://www.educoder.net/attachments/download/203332)

我们可以看到`duration`之间的比较运算输出为**逻辑值**`TRUE/FALSE`，如果大小判断成立则输出`TRUE`，否则输出`FALSE`。

除了大小判断，还可以直接使用命令`+`或者`-`进行**加减运算**，如下所示：

![img](https://www.educoder.net/attachments/download/203334)

我们可以看到对于`duration`的减法运算而言，是无视你给的**减数以及被减数顺序**的，它都会**默认输出较大值减去较小值的结果**。

以上就是本关对于时间跨度`duration`的介绍，如果感觉还欠点火候，来下面的**巩固教学**找感觉：

![img](https://www.educoder.net/attachments/download/203338)

#### 编程要求

本关涉及的代码文件为`R_duration.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 调用函数`duration()`分别以`1`小时、`89`分钟、`3`天创建`duration`，并分别赋值给`result1`、`result2`、`result3`；
- 调用函数`dXXXs()`（注，其中的`XXX`为相应的时间单位），分别以`1`年、`10`天来创建`duration`，并分别赋值给`result4、result5`；
- 将已给定的间隔`date1`和`date2`通过函数`as.duration`转换为`duration`型的时段，并分别赋值给`result6、result7`；
- 分别使用使用`>` `<`比较`result1`与`result2`的大小，将结果输出至`result8`、`result9`；
- 调用函数`duration()`创建长度为`1`年和`180天`的`duration`时段，并输出两个`duration`时段的减法值与加法值至`result10、result11`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_duration.R`，平台将运行用户补全的`R_duration.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/203360)

#### My_Answer

```r
#####	R_duration.R#####
library(lubridate)
start1 <- ymd_hms("20141003,12:00:00")
end1 <- ymd_hms("20180904,12;30:00")
start2 <- ymd_hms("20151203,12:00:00")
end2 <- ymd_hms("20161022,12;30:00")
date1 <- interval(start1,end1)
date2 <- interval(start2,end2)
  ###### begin ######
#Output the results.
result1=duration(1,"hour")
result2=duration(89,"minutes")
result3=duration(3,"day")
result4=duration(1,"year")
result5=duration(10,"day")
result6=as.duration(date1)
result7=as.duration(date2)
result8=result1>result2
result9=result1<result2
result10=duration(1,"year")-duration(180,"day")
result11=duration(1,"year")+duration(180,"day")
###### end ######
result1
result2
result3
result4
result5
result6
result7
result8
result9
result10
result11
```

### 第三关：时段之period

#### 任务描述

我们在本次实训开篇就讲了，关于时段类型**一共有三种**，其实我们不难发现有了间隔`interval`和`duration`后，似乎对于时段的描述已经足够，其实不然，因为上述两种时段类型还**存在短板**，所以才会引出本关的主题—`period`，我们也将在本关学习`period`的**创建方法**及其**相关运算**。`interval`和`duration`的短板跟下面这张图紧密相关，至于是什么短板，我们此处先卖个关子。

#### 相关知识

##### 周期period的意义

`period`中文即**周期**，是**时段类型**的三大组成部分之一，和第二关中所讲的`duration`非常类似。我们知道`duration`有两个特点：

- 不考虑闰年、夏时令等；
- 固定使用秒作为计量单位。

首先第一条就导致`duration`在使用过程中会显得比较死板，为什么呢？比如我们想知道`20160101`这个日期加一年后的日期，如果使用`duration`类型，其默认**不考虑闰年**，因此输出的结果将会比实际情况**少一天**。所以有时为了和实际情况更好地吻合，我们必须考虑闰年这一关键因素。

而对于第二条，我们知道一分钟是`60`秒，一小时是`3600`秒，一天是`86400`秒，一个星期是`604800`秒，一年是`31536000`秒，对于比较大的**时间跨度**，用秒来描述长度是**不方便**的。有多少人会认为`31536000`秒是标准年的长度？为了克服上面的两个致命弊端，周期`period`应运而生，**以较长的时钟周期来计算时段长度，并且考虑了闰年和闰秒**。

##### 创建周期period

![img](https://www.educoder.net/attachments/download/203371)

我们已经在上一关学习了如何创建`duration`类型的时段，那么学习创建`period`的方法就会非常容易，因为我们只需要将创建`duration`所调用的函数`ddays` `dyears` 中的第一个字母`d`去掉即可，比如通过调用函数`years(1)`来得到`period`为`1y 0m 0d 0H 0M 0S`，我们可以清楚地看到，区别于`duration`最直接的一点就是`period`类型的时段不会局限于只能使用秒作为计量单位，如图所示，可以使用除`month`外的任意时间单位。

##### 周期period的转换方法

如何实现从`interval`或者`duration`类型的时段**转换**到`period`类型呢？我们还是以下图中的间隔`date1`和`date2`为例，如图所示：

![img](https://www.educoder.net/attachments/download/203372)

调用函数`as.period`来讲间隔类型的时段转换为周期`period`，比如间隔`date1`，最终可以转换为`3y 11m 1d 0H 30M 0S`这一`period`类型的时段。当然`period`也能由`duration`的时段类型转换，方法跟`interval`转`period`一致，所以此处不再赘述。

##### 周期period的相关运算

我们已经介绍了`period`**不局限于**使用秒来作为时间单位进行计量时段，所以自然地可以与间隔`interval`类型的时段进行相应的**除法运算**，如图所示：

![img](https://www.educoder.net/attachments/download/203400)

通过直接调用命令`date1 / days(1)`或者`date1 / hours(1)`便可实现间隔与`period`的**除法运算**。

接下来便是`period`类型时段之间的**加法与减法运算**，如图所示：

![img](https://www.educoder.net/attachments/download/203402)

通过直接调用`days(13)+weeks(123)` `years(12)-weeks(12)`便可实现周期`period`类型的时段加减法运算，最终的结果也是按照`period`类型的时段来进行的输出。

老规矩，最后依然是我们的**巩固环节**：

![img](https://www.educoder.net/attachments/download/203403)

#### 编程要求

本关涉及的代码文件为`R_period.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 分别调用函数`years()` `days()` `hours()`创建长度为`3`年、`113`天、`2`小时的`period`类型时段，并分别赋值给变量`result1`、`result2`、`result3`；
- 调用函数`as.period`将给定的间隔类时段`date1`转换为`period`类型的时段，并将转换后的结果赋值给`result4`；
- 计算`date1`除以`result3`，并将结果赋值给`result5`；
- 计算`result1`与`result2`之间的加法，将结果赋值给`result6`；计算`result2`与`result3`之间的减法，将结果赋值给`result7`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_period.R`，平台将运行用户补全的`R_period.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/203404)

#### My_Answer

```r
#####	R_period.R#####
library(lubridate)
begin1 <- ymd_hms("20151203,12:00:00")
end1 <- ymd_hms("20160904,12;30:00")
date1<- interval(begin1,end1)

  ###### begin ######
#Output the results.
result1=years(3)
result2=days(113)
result3=hours(2)
result4=as.period(date1)
result5=date1/result3
result6=result1+result2
result7=result2-result3
###### end ######
result1
result2
result3
result4
result5
result6
result7
```

## 实战九：数据的合并

### 第一关：向量与矩阵的合并

#### 任务描述

我们一般在听国家层面的政策分析时，经常能够听到一句话那就是–做好**资源的整合**，对于数据分析而言，如果你需要处理的数据**分散在多个地方**，那么所需要做的第一步便是**数据的整合**，因此我们将在本关卡为大家讲解如何进行向量与矩阵的合并。

#### 相关知识

##### 向量的合并

在`R`的所有类型数据中，向量当属最为基本的一种，因此我们本关从**向量的合并**讲起，如图所示：

![img](https://www.educoder.net/attachments/download/203695)

然后我们调用函数`rbind()`对给出的向量`vector1`和`vector2`进行合并，结果如图所示，**按列逐一进行了合并**：

![img](https://www.educoder.net/attachments/download/203696)

上述是两个向量间的合并方法，如果我们需要合并的对象是**三个或更多向量**间的合并呢？方法依然参照两个向量间的合并，如下图所示，依旧调用`rbind()`，`()`中输入**需要的合并的向量名**。

![img](https://www.educoder.net/attachments/download/203697)

##### 矩阵的合并

要实现矩阵类型的数据合并，我们以如下的**同阶矩阵**`a`和`b`为例，如图所示：

![img](https://www.educoder.net/attachments/download/203691)

如下图所示，我们通过调用函数`rbind()`来实现矩阵`a`和矩阵`b`的合并，合并后的结果如下图所示，我们得到了一个**六行三列**的新矩阵，**前三行**为矩阵`a`的元素，**后三行**为矩阵`b`的元素。

![img](https://www.educoder.net/attachments/download/203692)

由于第一个例子两个矩阵都是**同阶**，为了加深理解，我们举一个更为特殊的例子，如下所示，我们生成一个矩阵`c`，其尺寸为`4`行`3`列，将其与矩阵`a`进行**合并**，如图所示：

![img](https://www.educoder.net/attachments/download/203693)

从上图我们可以清楚地看到，只要合并的两个矩阵的**列数相同**的，那么调用`rbind`函数即可完成矩阵的合并。那么如果需要合并的对象不是两个，而是三个甚至更多呢？如下图所示，对于需要合并的矩阵`a,b,c`，我们调用`rbind(a,b,c)`，输出为一个`10`行`3`列的**合并矩阵**。

![img](https://www.educoder.net/attachments/download/203694)

我们在本关介绍了两个及多个向量和矩阵间的合并方法，主要都是围绕着函数`rbind`所展开，相信这一关难不倒大家，但还是送上巩固的**动态教学**：

![img](https://www.educoder.net/attachments/download/203698)

#### 编程要求

本关涉及的代码文件为`R_vmcom.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 分别将取值`(1, 2, 3, 4, 5, 6, 7, 8, 9, 10)、(1, 1, 1, 1, 1, 1, 1, 1, 1, 1)、(2，3，4，1，12，3，5，13，13，2)`赋值给向量`v1、v2`以及`v3`；
- 分别将`1-100、101-200`按照逐一增加的顺序分别生成`10*10`的矩阵`matrix_A`和`matrix_B`；
- 调用函数`rbind()`分别完成向量向量`v1、v2`以及`v3`的合并以及矩阵`matrix_A`和`matrix_B`的合并，并将结果分别赋值给`result1、result2`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_vmcom.R`，平台将运行用户补全的`R_vmcom.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/203931)

#### My_Answer

```r
#####	R_vmcom.R#####

###### begin ######
#Output the result.
v1=c(1, 2, 3, 4, 5, 6, 7, 8, 9, 10)
v2=c(1, 1, 1, 1, 1, 1, 1, 1, 1, 1)
v3=c(2,3,4,1,12,3,5,13,13,2)
matrix_A=matrix(c(1:100),ncol=10)
matrix_B=matrix(c(101:200),ncol=10)
result1=rbind(v1,v2,v3)
result2=rbind(matrix_A,matrix_B)
###### end ######
result1
result2
```

### 第二关：数据框的合并

#### 任务描述

相信熟悉我们`R`这一系列实训的同学应该知道，我们的关卡设置从来都是**由浅入深**，往往第一关作为**基础性介绍**，因此在第一关讲解完向量与矩阵合并的基础上，下面必然是对于**结构相对复杂**的数据框合并的讲解，本关将立足数据框的基本结构，为大家详细阐释**数据框合并的相关方法**。

#### 相关知识

##### 数据框合并之all参数取FALSE

本关我们以如下的两个数据框为例，示例数据框分别命名为`frame1`和`frame2`，如图所示：

![img](https://www.educoder.net/attachments/download/203708)

我们首先观察下这两个数据框的**特点以及相互之间的联系**，熟悉数据库的同学，或者对数据库知识比较敏感的同学肯定能很快发现，这两个数据框有一列均为`teacher`，因此我们抓住这一特点，使用`R`自带的数据框合并函数`merge`进行上述两个数据框的合并，如下所示，调用函数`merge(frame1, frame2, by = "teacher", all = FALSE)`：

![img](https://www.educoder.net/attachments/download/204194)

其中参数`by = "teacher"`即函数会找出两个数据框**都包含的列**，即`teacher`作为合并的桥梁，`all = FALSE`的作用是将两个数据框中**该列数值相等**的那些行输出，这就有点像按照相同的列取了一个**交集**。我们可以看到结果输出由两个数据框在`teacher`列取值相同的`1`和`7`所在的**行合并而成**。

那么新的问题来了，`merge`函数是否受数据框输入的**顺序所影响**呢？我们来试验一下，如下所示，我们将调用的命令修改为`merge(frame2, frame1, by = "teacher", all = FALSE)`

![img](https://www.educoder.net/attachments/download/204172)

结果表明，**无论需要合并的数据框顺序如何调整**，其输出结果的本质是不变的，只是**后几列的顺序相应调整**而已。

##### 数据框合并之all参数取TRUE

有了前面的只是铺垫，下面的内容就会比较容易吸收，如下所示，我们把函数`merge`中的参数项`all`的取值修改为`TRUE`：

![img](https://www.educoder.net/attachments/download/203711)

我们把参数项`all`的取值修改为`TRUE`后，从输出的结果我们可以看到，当`id`所指定的列值相同时，则会将对应列中所剩下的**行值合并到同一行中**，若是`id`所指定的列值不相同时，则会将另一数据框中**对应行的值取为缺失值**：

```
1       1     Can      M
2       3      US   
3       4          F
4       5     RUS   
5       6          M
6       7      UK      F
7       8      NL   
8       9          M
```

同样的，当我们如下图所示调换数据框在函数`merge`中所调用的位置时，结果只会调整对应列的前后顺序，**并不会产生本质的改变**，所以无需纠结所需要合并的数据框的输入顺序：

![img](https://www.educoder.net/attachments/download/203712)

在本关卡中大家需要主要掌握的是函数`merge`的调用方法，以及其中**最关键参数**`all`的**逻辑值**使用方法，下面依然是我们的**巩固环节**：

![img](https://www.educoder.net/attachments/download/203713)

#### 编程要求

本关涉及的代码文件为`R_framecom.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 将向量`hand：c(1,2,3,4,5)`，
  `some： c("Can", "US", "RUS", "UK", "NL")`赋值给数据框`frame1`；
- 将向量`hand：c(3, 29, 55, 62, 143)`，
  `pretty：c("M","F","M","F","M")`赋值给数据框`frame2`；
- 调用函数`merge`，以数据框`frame1`和`frame2`中相同列名为桥梁进行合并，数据框的调用顺序为`(frame1, frame2)`，其中`all`的值分别取`FALSE`和`TRUE`，将两次输出结果分别赋值给`result1`和`result2`；
- 调用函数`merge`，以数据框`frame1`和`frame2`中相同列名为桥梁进行合并，数据框的调用顺序为`(frame2，frame1)`，其中`all`的值分别取`FALSE`和`TRUE`，将两次输出结果分别赋值给`result3`和`result4`；

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_framecom.R`，平台将运行用户补全的`R_framecom.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/203932)

#### My_Answer

```r
#####	R_framecom.R#####

  ###### begin ######
#Output the results.
hand=c(1,2,3,4,5)
some=c("Can", "US", "RUS", "UK", "NL")
frame1=data.frame(hand,some)
hand=c(3, 29, 55, 62, 143)
pretty=c("M","F","M","F","M")
frame2=data.frame(hand,pretty)
result1=merge(frame1,frame2,all=FALSE)
result2=merge(frame1,frame2,all=TRUE)
result3=merge(frame2,frame1,all=FALSE)
result4=merge(frame2,frame1,all=TRUE)
###### end ######
result1
result2
result3
result4
```

### 第三关：数据框的合并进阶篇

#### 任务描述

我们在打游戏的经验告诉我们，在打`boss`之前，必须先打小怪刷副本爆好装备然后再打`boss`，对于数据分析的学习也是如此，基础才是后面厚积薄发的关键，我们在上一关已经掌握了**数据框合并的基本技巧**，那么本关卡将在第二关的基础上，为大家更为深入地讲解数据框的合并进阶技巧。

#### 相关知识

##### 数据框合并之参数sort

对于数据框的合并，我们主要使用的函数就是第二关中所介绍的`merge`，但是在上一关中，我们只是讲解了其**最为基本的功能**，让我们来看一下它的完整形态：

`merge(x, y, by = intersect(names(x), names(y)),

```
  by.x = by, by.y = by, all = FALSE, all.x = all, all.y = all,  sort = TRUE, suffixes = c(".x",".y"),  incomparables = NULL, ...)`
```

是不是觉得这函数实在是**太长**了，是的，笔者当年第一次接触这个函数也觉得这设计的也太长了，所以我们将其**拆分讲解**。首先我们需要关注的是`sort`参数，没错，这个`sort`和它本身的含义一致，就是**排序**的意思，如下图所示，我们将`sort`的逻辑值赋为`FALSE`，看下会输出什么结果：

![img](https://www.educoder.net/attachments/download/203716)

可以看到，当`sort`的逻辑取值为`FALSE`时，调用函数`merge`将两个数据框中`teacher`列取值相同的`3`和`2`排在最前，而后按照各数据框种取值的**原始顺序**排列。

下面我们继续尝试将`sort`取值定为`TRUE`，看看最终会输出什么形式的结果，如下所示：

![img](https://www.educoder.net/attachments/download/204193)

从上图的结果可知，当参数项`sort=TRUE`时，合并的结果将会按照`teacher`列取值**从小到大依次排列**。

##### 数据框合并之参数suffixes

我们前面讲的所有例子中，两个数据框之间都**只存在一个相同列**，但是实际情况肯定远不止一项，试想一下，当我们拿到**多个数据框**，其中相同列非常多，但是我们此时又只希望**按照其中一项进行合并**，那么剩下的相同项势必会由于名称相同，而给最后的结果带来困扰。

那么在函数`merge`中的参数项`suffixes`就是被设计来解决这一问题的，其调用的方式为`suffixes = c(".x",".y")`，即将**其余的命名相同项其尾缀**改为`.x`和`.y`用以区分，具体操作如下所示：

![img](https://www.educoder.net/attachments/download/203718)

可以看到，在最终的输出结果中，另一个相同项`age`的命名分别被改为了`age.x`以及`age.y`来加一区分。

##### 数据框合并之参数by

其实函数`merge`中关键的参数笔者认为是`by`，在我们前面的例子中，只介绍了`by`用来合并一个相同项，其实`by`可以用来**合并多个命名相同的项**，如下图所示，两个数据框中共有两个相同项，即`teacher`和`age`：

![img](https://www.educoder.net/attachments/download/203720)

 通过输入参数项`by = c("teacher","age")`,便可实现数据框`frame1`和`frame2`**所有相同项**的合并，最终结果也是按照列`teacher`的取值从小到大**升序排列**。

本关主要介绍了`merge`函数中三个关键参数项的使用，希望大家经过本次实训，能够掌握`R`中**多种数据结构的合并方法**，下面是本关的**巩固时段**：

![img](https://www.educoder.net/attachments/download/203722)

#### 编程要求

本关涉及的代码文件为`R_framecom_adv.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 将向量`hand：c(12,22,31,41,5)`，
  `some： c("Can", "US", "RUS", "UK", "NL")`
  `boy: c(1, 21, 131, 122, 15)`赋值给数据框`frame1`；
- 将向量`hand：c(5, 19, 15, 22, 143)`，
  `pretty：c("M","F","M","F","M")`
  `boy: c(1, 21, 11, 12, 13)`赋值给数据框`frame2`；
- 调用函数`merge`，以数据框`frame1`和`frame2`中的列`hand`为桥梁进行合并，数据框的调用顺序为`(frame2, frame1)`，其中`all`的值取`TRUE`，`sort`分别取`TRUE`和`FALSE`（除此之外不考虑其他参数设定），将两次输出结果分别赋值给`result1`和`result2`；
- 调用函数`merge`，以数据框`frame1`和`frame2`中的列`hand`为桥梁进行合并，数据框的调用顺序为`(frame1, frame2)`，其中`all`的值取`TRUE`，`sort`取`TRUE`，使用参数`suffixes`将其他相同列名重命名为`.A`与`.B`，将输出结果赋值给`result3`；
- 调用函数`merge`，以数据框`frame1`和`frame2`中的列`hand`和`boy`为桥梁进行合并，数据框的调用顺序为`(frame1, frame2)`，其中`all`的值取`TRUE`，`sort`取`TRUE`，使用参数`suffixes`将其他相同列名重命名为`.A`与`.B`，将输出结果赋值给`result4`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_framecom_adv.R`，平台将运行用户补全的`R_framecom_adv.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/203934)

#### My_Answer

```r
#####	R_framecom_adv.R#####

  ###### begin ######
#Output the results.
hand=c(12,22,31,41,5)
some=c("Can", "US", "RUS", "UK", "NL")
boy=c(1, 21, 131, 122, 15)
frame1=data.frame(hand,some,boy)

hand=c(5, 19, 15, 22, 143)
pretty=c("M","F","M","F","M")
boy=c(1, 21, 11, 12, 13)
frame2=data.frame(hand,pretty,boy)

result1=merge(frame2,frame1,by="hand",all=TRUE,sort=TRUE)
result2=merge(frame2,frame1,by="hand",all=TRUE,sort=FALSE)
result3=merge(frame1,frame2,by="hand",all=TRUE,SORT=TRUE,suffixes=c(".A",".B"))
result4=merge(frame1,frame2,by=c("hand","boy"),all=TRUE,sort=TRUE,suffixes=c(".A",".B"))
###### end ######
result1
result2
result3
result4
```

## 实战十：数据的提取

### 第一关：向量元素的提取

#### 任务描述

现代自然界中，对于食物的消化都是讲求**利用率**的，笔者记得以前看一档`bbc`的节目，说当今世界狮子的食物利用率是最高的，但也不可能达到百分之百（人类这种啥内脏都吃的不在讨论范围）。与之类似的，我们在数据挖掘方面，对于一个数据集也**不可能完全利用**，有时只需要其中的一部分，那么如何数据的提取呢？本关将以**向量**为对象，初步为你答疑。

#### 相关知识

##### 单个向量元素提取

讲解如何**提取数据中的子集**，我们当然还是以最基本的**向量**入手，首先生成如下包含`10`个数值元素的向量，如图所示：

![img](https://www.educoder.net/attachments/download/203788)

提取向量子集的方式较为简单，我们首先提取向量中的**单个元素**，调用命令`vector[1]`即可完成，如下图所示：

![img](https://www.educoder.net/attachments/download/203793)

`[]`中的数字即是需要提取的**元素编号**，只要输入对应的元素编号，便能提取出向量中的对应元素。

##### 向量中某序列元素的提取

第二种方法是使用`:`实现向量中**某些元素序列**的提取，如下图所示，使用命令`vector[1:4]`可以实现提取出向量`vector`中**第一位到第四位**的元素，其中`:`符号前后的数字可以按照自己的需求任意调节：

![img](https://www.educoder.net/attachments/download/203789)

需要提到的一点是，当`:`号前后的数字一致时，其功能就是**单独提取向量中的某一特定元素**。

##### 按照条件提取向量元素

![img](https://www.educoder.net/attachments/download/203790)

第三种方法是按照一定的**提取条件**进行向量元素的提取，比如数值比较运算符`<` `>` `==`等，如上图所示，使用命令`vector[vector>3]`便会输出符合筛选条件的向量元素。

##### 基于逻辑值的向量元素提取方法

最后一种方法是利用我们之前学过的逻辑值，利用逻辑值的赋值`TRUE`或者`FALSE`来提取**满足逻辑值条件**的向量元素，如下图所示：

![img](https://www.educoder.net/attachments/download/203791)

基于逻辑值的方法原理是，当逻辑值为`TRUE`时，其**编号相对应**的向量元素将会被取出，反之，则不会被提取。

本关主要讲解了**四种向量元素**的提取方法，简单但是高效实用，接下来是我们的**巩固阶段**：

![img](https://www.educoder.net/attachments/download/203792)

#### 编程要求

本关涉及的代码文件为`R_vector_ext\fract.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 将向量`c(2,4,5,6,23,12,432,1213,11,0)`赋值给`vector`；
- 将向量第`3`、第`5`、第`7`个元素取出，分别赋值给`result1`、`result2`、`result3`；
- 将向量第`3`到第`8`个元素取出，赋值给`result4`；
- 分别将向量中大于`20`的元素和小于等于`40`的元素取出，分别赋值给`result5`、`result6`；
- 使用逻辑值取出向量中第`2`个和第`5`个元素，并赋值给`result7`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_vector_ext\fract.R`，平台将运行用户补全的`R_vector_ext\fract.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/203886)

#### My_Answer

```r
#####	R_vector_extract.R#####

###### begin ######
#Output the result.
vector=c(2,4,5,6,23,12,432,1213,11,0)
result1=vector[3]
result2=vector[5]
result3=vector[7]
result4=vector[3:8]
result5=vector[vector>20]
result6=vector[vector<=40]
result7=c(vector[2],vector[5])

###### end ######
result1
result2
result3
result4
result5
result6
result7
```

### 第二关：矩阵元素的提取

#### 任务描述

对于一个**矩阵**而言，大家其实可以把它看做是一个**特殊的向量**，一个有着维数`dim`属性的向量，维数即是一个长度为`2`的向量，用来指定**矩阵的行数和列数**。因此在掌握了向量元素的提取后，接下来我们将要开始学习**矩阵元素的提取方法**。

#### 相关知识

##### 矩阵单个元素的提取

在探讨矩阵元素提取方法之前，我们首先生成一个包含`25`个元素，行数列数均为`5`的矩阵，如下图所示：

![img](https://www.educoder.net/attachments/download/203797)

第一种矩阵元素提取方法和向量类似，即**单个元素的提取**，通过调用命令`matrix[a,b]`来实现，其中的`a b`即为需要提取的元素**其所在位置的行列值**，结果如下图所示：

![img](https://www.educoder.net/attachments/download/203884)

##### 矩阵整行或整列元素的提取

因为一个矩阵往往**非常庞大**，所以有时我们分析一个矩阵数据集时，并不会只提取其中的**某几个元素**，而是关心**某行某列元素的性质**，因此势必需要将行列整个提取出，这时我们就需要使用命令`matrix[x,]`或者`matrix[,y]`，命令`matrix[x,]`省略了列值，说明需要将第`x`行的所有元素**全部提取**，同样的，命令`matrix[,y]`省略了行值，说明需要将第`y`列的所有元素**全部提取**，如下图所示：

![img](https://www.educoder.net/attachments/download/203802)

如果想要同时提取**多个行或者多个列**的元素呢？这时我们就需要曲线救国，首先生成一个**向量**，向量中的元素即为你需要提取出的**行列编号**，然后使用命令`matrix[x,]`或者`matrix[,y]`，这时的`x y`即包含了行列编号的向量，具体如下图所示：

![img](https://www.educoder.net/attachments/download/203805)

比如我们将`1`，`2`赋值给向量`a`，然后使用命令`matrix[a,]`即可提取出矩阵第`1`行和第`2`行的**所有元素**。

##### 参数drop

彩蛋大家肯定不陌生，电影游戏里经常会遇到，而程序里面其实也有不少彩蛋，就像当年著名的`excel`隐藏游戏，让小时候的笔者疯玩了好久。而在矩阵元素的提取环节，其实也有一个彩蛋，那就是参数`drop`，一般来讲，参数`drop`是默认为`TRUE`，所以一般是不出现的，其作用是无论我们怎么取矩阵元素，输出的结果都是**一个一维结果**，举例说明：

![img](https://www.educoder.net/attachments/download/203806)

如上图所示，当我们只取出矩阵中的**某一个元素**时，输出结果就是一个**一维的数值**，但是当我们把参数`drop`的值令为`FALSE`时，便可以得到一个**矩阵形式**的输出结果。

![img](https://www.educoder.net/attachments/download/203807)

对于整行整列的元素提取也是这个道理，当处于**默认状态**下时，提取出的元素就是一个**向量化的结果**，当参数`drop`的值令为`FALSE`时，则输出结果变成了一个尺寸为`1x5`的**矩阵形式**。

为什么最后单独把`drop`参数的使用作为压轴讲解，因为这一点在后续进阶篇的数据处理中会有重要应用，尽请期待。最后依然是我们的综合**巩固环节**：

![img](https://www.educoder.net/attachments/download/203885)

#### 编程要求

本关涉及的代码文件为`R_matrix_ext\fract.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 将`1-100`按照逐一增加的顺序生成一个`10*10`的矩阵并命名为`matrix`；
- 提取出矩阵中第`3`行`5`列、第`8`行`9`列的元素，并分别赋值给`result1、result2`；
- 提取出矩阵的第`2`行、第`4`行、第`5`列、第`9`列元素，并分别赋值给`result3、result4、result5、result6`；
- 整体提取出矩阵第`4`行到第`5`行的元素，并赋值给`result7`；
- 将参数`drop`的值令为`FALSE`，再提取出第`5`行的元素，并将结果赋值给`result8`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_matrix_ext\fract.R`，平台将运行用户补全的`R_matrix_ext\fract.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/203887)

#### My_Answer

```r
#####	R_matrix_extract.R#####

  ###### begin ######
#Output the results.
matrix=matrix(c(1:100),ncol=10)
result1=matrix[3,5]
result2=matrix[8,9]
result3=matrix[2,]
result4=matrix[4,]
result5=matrix[,5]
result6=matrix[,9]
result7=matrix[4:5,]
result8=matrix[5,,drop=FALSE]
###### end ######
result1
result2
result3
result4
result5
result6
result7
result8
```

### 第三关：数据框元素的提取

#### 任务描述

**数据框**其实一种表格类型的数据，或者我们可以把它看做是一种**非常特殊的列表**，即一种列表的**集合形式**，在`R`支持的各种数据类型中，数据框也是相对复杂的一种，所以我们将数据框的元素提取放在本次实训的最后作为**压轴出场**，本关将为大家详细讲解如何实现**数据框的元素提取**。

#### 相关知识

##### 数据框元素提取之[]符号

在数据框中，其每一列元素的数据类型都可以**千差万别**，第一列如果是**数值型**，第二列就有可能是**字符型**等等，但是其每一列的数据类型必须完全一致，且各列之间的**长度必须一致**。如下图所示，我们首先生成一个数据框来作为讲解的示例：

![img](https://www.educoder.net/attachments/download/203877)

对于数据框元素的提取，第一种和**向量矩阵类似**，使用`[]`来指定需要提取的**元素位置**，如下图所示，当使用命令`foreignteacher[4]`时，提取出的元素是数据框的对应列，**而不是某一个元素值**，是一整列：

![img](https://www.educoder.net/attachments/download/203878)

在使用`[]`作为数据框的元素提取方法中，还有一点较为特殊，我们也可以使用`[[]]`实现元素的提取，即两个方括号的叠加，如下图所示：

![img](https://www.educoder.net/attachments/download/203879)

从上图我们发现使用`[[]]`的输出结果和单括号是**类似的**，只有一点细节上的区别，那就是使用单括号时，输出的形式依旧是**列\**，而使用两个括号叠加时，结果的输出便会自动变成以**行**的形式输出。

大家可能会问，如果我们实在是需要提取**数据框中的单个元素**呢？其实方法也很简单，直接使用命令`foreignteacher[3,2]`即可提取出当前数据框中**第三行第二列**的元素值，如下图所示：

![img](https://www.educoder.net/attachments/download/203880)

##### 数据框元素提取之$

我们在前序课程中讲过，在数据框的相关运算中，`$`是一个非常重要的符号，能够直接使用命令`数据框名$变量名`来指向数据框中的**具体列**，如下所示：

![img](https://www.educoder.net/attachments/download/203881)

我们可以看到，在数据框中一共有四个变量，分别是`teacher` `country` `age` `gender`，分别调用命令`foreignteacher$teacher`、`foreignteacher$country`、`foreignteacher$age`以及`foreignteacher$gender`即可提取出对应的**数据框整列元素**。

##### 数据框多列元素的提取方法

有时我们的数据分析需求并不会只满足于提取出其中的某一列元素，而是众多**数据框列的组合**，那么我们就需要借用`:`符号来实现，如下图所示：

![img](https://www.educoder.net/attachments/download/203882)

直接使用命令`foreignteacher[a:b]`便可提取出数据框第`a`列到第`b`列的元素。

本关卡主要将数据框元素的提取分为**三大类**，下图为大家送上本关的**巩固教学图**：

![img](https://www.educoder.net/attachments/download/203883)

#### 编程要求

本关涉及的代码文件为`R_frame_ext\fract.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 将向量`student：c(11,22,31,41,15)`，
  `country： c("CHN", "UK", "UK", "GER", "NL")`，
  `age：c(14, 19, 15, 612, 243)`以及
  `gender：c("M","F","M","F","M")`赋值给数据框`foreignstudent`；
- 使用`[]`分别提取出数据框`foreignstudent`中的第`1`列和第`4`列整列元素，并分别赋值给`result1、result2`；
- 使用`[[]]`分别提取出数据框`foreignstudent`中的第`1`列和第`4`列整列元素，并分别赋值给`result3、result4`；
- 使用`[]`提取出数据框`foreignstudent`中的第`1`行第`4`列的单独元素值，并赋值给`result5`；
- 使用`$`符号提取出数据框`foreignstudent`中变量名为`student`的所有元素，并赋值给`result6`；
- 使用`:`符号提取出数据框`foreignstudent`中第`1`列到第`3`列的元素，并赋值给`result7`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_frame_ext\fract.R`，平台将运行用户补全的`R_frame_ext\fract.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/203888)

#### My_Answer

```r
#####	R_frame_extract.R#####

  ###### begin ######
#Output the results.
student=c(11,22,31,41,15)
country=c("CHN", "UK", "UK", "GER", "NL")
age=c(14, 19, 15, 612, 243)
gender=c("M","F","M","F","M")
foreignstudent=data.frame(student,country,age,gender)
result1=foreignstudent[1]
result2=foreignstudent[4]
result3=foreignstudent[[1]]
result4=foreignstudent[[4]]
result5=foreignstudent[1,4]
result6=foreignstudent$student
result7=foreignstudent[1:3]
###### end ######
result1
result2
result3
result4
result5
result6
result7
```

## 实战十一：数据的删除

### 第一关：数据的删除

#### 任务描述

在实际的数据分析任务中，我们所拿到的数据**往往存在着各种瑕疵**，比如大量的**缺失值、野值、无效观测**等，因此我们除了按照前序课程讲的那样**提取**出有用数据外，还可以将**无效或者错误**的数据直接进行删除，本关卡就将为你讲解如何进行**向量和矩阵**的元素删除。

#### 相关知识

##### 单个向量元素的删除

我们依旧以向量作为数据删除讲解的基础，首先生成如下所示包含`10`个数值型元素的向量，如图所示：

![img](https://www.educoder.net/attachments/download/204010)

如下图所示，我们使用命令`vector<-vector[-1]`即可完成向量**单个元素**的删除，其中有**两点**需要特别注意：

- 牢记括号为方括号；
- 号后面的数字为当前需要删除的向量元素编号，而非该元素的初始编号。

![img](https://www.educoder.net/attachments/download/204011)

##### 连续向量元素的删除

古代有种刑法叫**连坐**，什么意思呢？一个人犯错，周围的所有人跟着一起受惩罚。再比如，有时候一个苹果坏了，其周围的苹果可能也跟着腐烂，这说明一个什么问题呢？出错的往往不是个体，而是存在一个群体诱因，所以我们在**删除向量元素**时，绝大多数时候需要的是删除连续的一系列元素。这时我们就需要借助`:`符号，如下图所示：

![img](https://www.educoder.net/attachments/download/204012)

首先定义需要删除元素的**起始和终止编号**，然后使用命令`vector<-vector[-(n:m)]`删除从第`n`个元素到第`m`个元素的向量值。

##### 矩阵单一行列元素的删除

我们以如下包含`25`个**数值型元素**、阶数为`5x5`的矩阵为例：

![img](https://www.educoder.net/attachments/download/204013)

对于矩阵元素的删除而言，主要是**整行或整列**的删除，因为矩阵的数学形式固定为行`x`列，每一个矩阵位置必定有一个**确定的数值**（当然可以为缺失值，但是此类将错误值修改为缺失值的方法，我们在前序课程已经介绍），所以我们将主要介绍**矩阵的行列删除**，如下图所示：

![img](https://www.educoder.net/attachments/download/204014)

使用命令`matrix<- matrix[-1,]`即可完成矩阵`matrix`中**第一行元素的删除**，命令中的括号包含了需要删除的**行信息**，其中以**逗号**作为分隔，**逗号前为行的编号**，**逗号后为列的编号**。若行编号不为空，则删除对应编号的行；若列编号不为空，则删除对应编号的列，如下图所示：

![img](https://www.educoder.net/attachments/download/204015)

##### 矩阵的多行列删除

对于矩阵而言，我们有时需要**整体删除**其中的几行或者几列，处理方法和向量类似，我们也需要借助`:`符号，如下图所示，使用命令`matrix<-matrix[-(n:m),]`，其中`n`为需要删除的行（或者列）的**起始编号**，`m`为需要删除的行（或者列）的**终止编号**：

![img](https://www.educoder.net/attachments/download/204017)

本关卡大家需要记住`[]` `:` 符号在元素删除中的使用方法，最后是我们的综合**巩固环节**，涵盖了向量与矩阵元素删除的各个内容：

![img](https://www.educoder.net/attachments/download/204021)

#### 编程要求

本关涉及的代码文件为`R_vectormatrix_del.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 将取值`(2，3，4，1，12，3，5，13，13，2)`赋值给向量`vector`；
- 分别将`1-100`按照逐一增加的顺序生成`10*10`的矩阵`matrix`；
- 删除向量`vector`的第`1`个元素，赋值给`result1`;
- 删除向量`vector`的第`4`个元素，赋值给`result2`；
- 删除向量`vector`的第`1`到第`7`个元素，赋值给`result3`;
- 删除矩阵`matrix`的第`3`行元素，赋值给`result4`；
- 删除矩阵`matrix`的第`2`列元素，赋值给`result5`；
- 删除矩阵`matrix`的第`2`到第`3`列元素，赋值给`result6`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_vectormatrix_del.R`，平台将运行用户补全的`R_vectormatrix_del.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/204022)

#### My_Answer

```r
#####	R_vectormatrix_del.R#####

  ###### begin ######
#Output the results.
vector=c(2,3,4,1,12,3,5,13,13,2)
matrix=matrix(c(1:100),ncol=10)
result1=vector[-1]
result2=vector[-4]
result3=vector[-(1:7)]
result4=matrix[-3,]
result5=matrix[,-2]
result6=matrix[,-(2:3)]
###### end ######
result1
result2
result3
result4
result5
result6
```

### 第二关：数据框元素的删除

#### 任务描述

对于**数据框**而言，其有着看上去类似**矩阵的结构**，而其内部又是多个**向量**所组成，而每个向量的数据类型又可以**千差万别**，因此我们单独用本关来讲解相对复杂的数据框元素删除方法。

#### 相关知识

##### 基于逻辑值的数据框元素删除

学习过前两个实训的同学可能非常清楚，**逻辑值**的合理运用在`Rstudio`中有着重要意义。在本关我们将首先讲解基于**逻辑值**的数据框元素删除方法，首先我们生成如下所示包含`4`个向量的数据框`frame`:

![img](https://www.educoder.net/attachments/download/204112)

比如我们现在需要删除`age`这一变量下的所有元素，首先使用函数`names(foreignteacher)`生成一个包含所有变量名的**字符型向量**，在此基础上，调用函数`names(foreignteacher) %in% c("age")`得到一个**逻辑型向量**，`%in% c("age")`的作用就是去数据框中去匹配变量`age`，如果匹配到`age`则其对应的逻辑值为`TRUE`，反之则为`FALSE`。

然后我们在得到的逻辑值向量的基础上，通过运算符`!`将该向量的所有**逻辑值取非**，如下图所示：

![img](https://www.educoder.net/attachments/download/204115)

然后即可使用命令`foreignteacher<-foreignteacher[vector]`将`age`整列删除，输出如下图所示，`foreignteacher<-foreignteacher[vector]`会识别逻辑向量`vector`中取值为`FALSE`的元素编号，并将该编号对应的数据框向量删除：

![img](https://www.educoder.net/attachments/download/204116)

##### 基于-符号的数据框元素删除

除了我们上面讲的**基于逻辑值**的删除方法，我们还可以直接使用`-`符号实现数据框元素的删除，如下所示，依旧是上一章节采用的示例数据框`frame`：

![img](https://www.educoder.net/attachments/download/204118)

直接使用命令`foreignteacher<-foreignteacher[c(-1,-2)]`即可实现删除数据框`frame`中的第一个以及第二个向量的所有元素，如下图所示，需要注意的一点是，`c`后紧跟着的是**方括号**，否则会出现语法错误：

![img](https://www.educoder.net/attachments/download/204119)

那如果我们要同时删除连续的**多列向量元素**呢？聪明的同学是不是已经想到了，借用符号`:`的递加功能，使用命令`foreignteacher<-foreignteacher[c(-(n:m))]`即可完成数据框第`n`列到第`m`列的删除，结果如下图所示：

![img](https://www.educoder.net/attachments/download/204195)

##### 基于未定义NULL的删除

我们最后再来介绍一种**高效**的数据框删除手段，在`Rstudio`中，`NULL`代表着未定义，大家一定要将`NULL`未定义和`NA`缺失值区别开来，我们直接将`NULL`赋值给数据框中**需要删除的向量列**即可实现对应向量列的删除，这个原理其实很好理解，将某一列赋值为未定义，那也就是说直接让这一向量列**消失**，输出结果如图所示：

![img](https://www.educoder.net/attachments/download/204121)

最后我们总结一下，在本关中，我们学习了使用逻辑值、`-`符号以及`NULL`来实现数据框元素的删除，基本都是细节问题，需要大家加强记忆，下面依旧是我们为大家整理的巩固`GIF`：

![img](https://www.educoder.net/attachments/download/204122)

#### 编程要求

本关涉及的代码文件为`R_frame_del.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

– 将向量`student：c(11,22,31,41,15)`，

`country： c("CHN", "UK", "UK", "GER", "NL")`，

`age：c(14, 19, 15, 612, 243)`以及

`gender：c("M","F","M","F","M")`赋值给数据框`foreignstudent`；

- 基于逻辑值将数据框中的`coutry`整列删除，并将余下的数据框赋值给`result1`；
- 基于`-`符号将数据框中的`student`和`coutry`整列删除，并将余下的数据框赋值给`result2`；
- 基于`-`符号将数据框中的前三个连续列整列删除，并将余下的数据框赋值给`result3`；
- 基于未定义`NULL`将数据框中的`gender`整列删除。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_frame_del.R`，平台将运行用户补全的`R_frame_del.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/204123)

#### My_Answer

```r
#####	R_frame_del.R#####

###### begin ######
#Output the result.
student=c(11,22,31,41,15)
country=c("CHN", "UK", "UK", "GER", "NL")
age=c(14, 19, 15, 612, 243)
gender=c("M","F","M","F","M")
foreignstudent=data.frame(student,country,age,gender)
names(foreignstudent) %in% c("country")
result1=foreignstudent[!(names(foreignstudent) %in% c("country"))]
result2=foreignstudent[c(-1,-2)]
result3=foreignstudent[c(-1:-3)]
foreignstudent$gender=foreignstudent$gender=NULL

###### end ######
result1
result2
result3
foreignstudent
```

### 第三关：删除符合条件的数据

#### 任务描述

在`Rstudio`中，当我们执行删除操作时，除了前两关中讲解的根据行列的编号进行整行整列删除外，我们有时更关心的其实是删除一些特定的数据元素，比如删除某矩阵中小于`0`的元素值，因此本关将向大家讲解如何实现删除符合一定条件的数据。

#### 相关知识

##### 基于运算符的条件删除

当我们拿到一组身高数据，数据中既有正数又有负数还有零，那么显然这数据在收集时存在**失真**，因此我们需要首先删除这些**小于或等于零的数值**，如下图所示，我们生成一个包含`10`个数值的身高向量`vector`:

![img](https://www.educoder.net/attachments/download/204125)

不难发现身高向量中包含很多非正数，因此我们使用命令`which(vector<=0)`找出这些非正数的**编号**，发现非正数的编号分别为`4 5 6 7`，然后使用`vector[-which(vector<=0)]`利用这些非正数的编号坐标将其对应删除，具体如下图所示：

![img](https://www.educoder.net/attachments/download/204126)

同理，我们也可以只定向删除向量`vector`中的取值为零的元素，如下图所示，使用命令`vector[-which(vector==0)]`即可完成对**零元素的删除**：

![img](https://www.educoder.net/attachments/download/204127)

除此之外，我们还可以利用诸如`< > >=`的**比较运算符**进行精确删除，均使用命令`vector[-which(vectorXX0)]`来实现，其中`XX`可以根据实际需求**任意选定**合适的比较运算符。

##### 基于缺失值的条件删除

不知道大家还是否记得我们在**缺失值实训**中，花了很长篇幅反复讲过一个函数`na.omit()`，作用是删除缺失值所在的行。可能不少聪明的同学已经恍然大悟，我们可以**利用缺失值**进行条件删除。

首先我们将需要删除的数据元素**重新赋值**为缺失值`NA`，如下图所示的矩阵`matrix`中，我们希望删除包含数值`8`的所有行，那么我们首先元素`8`在矩阵中**赋值为缺失值**，如下所示：

![img](https://www.educoder.net/attachments/download/204128)

然后如下图所示，调用函数`na.omit(matrix)`将缺失值所在的行删除，即可实现删除元素`8`所在行。

![img](https://www.educoder.net/attachments/download/204129)

##### 基于反向提取实现元素删除

基于反向提取？什么意思呢，这是笔者结合自身经验总结，简单来讲，就是**反其道而行之**，你要求往西走，我偏偏要往东走，往东走到头了，不就是西边了。比如，现在要求删除小于`10`的元素，那么一般意义来说我们就是**直接删除**小于`10`的元素即可，但是反过来想，我们其实也可以**提取出大于或等于`10`的元素**，即变相实现了删除小于`10`的元素。我们还是以熟悉的数据框`foreignteacher`为例：

![img](https://www.educoder.net/attachments/download/204130)

比如我们现在需要删除所有包含大于`60`的数值其所在的行，如下图所示，我们使用命令`foreignteacher[which(foreignteacher$teacher<=60&foreignteacher$age<=60),]`，其中条件选择`foreignteacher$teacher<=60` 和 `age<=60`中间用逻辑与`&`相连，即找出**两个条件都满足**的情况，然后将其提取出来，变相实现了删除大于`60`的数值所在行：

![img](https://www.educoder.net/attachments/download/204131)

综上所述，我们运用**比较运算符、缺失值函数以及反向提取**来综合讲解了处理条件删除的几种常见方法，其中笔者总结的最后一种方法亲测最为有效，希望大家能灵活运用，最后依然是巩固`GIF`时段：

![img](https://www.educoder.net/attachments/download/204132)

#### 编程要求

本关涉及的代码文件为`R_condition_del.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 将取值`(2，3，4，1，12，3，5，13，13，2)`赋值给向量`vector`；
- 将`1-100`按照逐一增加的顺序生成`10*10`的矩阵`matrix`；
- 将向量`a：c(11,22,31,41,15)`，
  `b： c(123, 122, 34, 25, 64)`，
  `c：c(14, 19, 15, 612, 243)`以及
  `d：c(12,21,34,78,26)`赋值给数据框`frame`；
- 使用比较运算符将向量`vector`中小于`5`的元素删除，并将删除后的向量赋值给`result1`；
- 使用缺失值方法将矩阵`matrix`中等于`45`的元素所在行删除，并将删除后的矩阵赋值给`result2`；
- 使用反向提取的方法删除数据框`foreignstudent`中小于`20`的元素所在行，并将删除后的数据框赋值给`result3`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_condition_del.R`，平台将运行用户补全的`R_condition_del.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/204133)

#### My_Answer

```r
#####	R_condition_del.R#####

  ###### begin ######
#Output the results.
vector=c(2,3,4,1,12,3,5,13,13,2)
matrix=matrix(c(1:100),ncol=10)
a=c(11,22,31,41,15)
b=c(123, 122, 34, 25, 64)
c=c(14, 19, 15, 612, 243)
d=c(12,21,34,78,26)
frame=data.frame(a,b,c,d)
result1=vector[-which(vector<5)]
matrix[matrix==45]<-NA
result2=na.omit(matrix)
result3=frame[(which(frame$a>=20&frame$b>=20&frame$c>=20&frame$d>=20)),]
###### end ######
result1
result2
result3
```





## 实战十二：选择观测

### 第一关：观测的选择之顺序

#### 任务描述

本关卡将带领大家初步了解什么是**观测**，观测的**本质**是什么，并在此基础上，从最简单的观测选择方法入手，为大家讲解**两种**最为基本的**观测选择方法**。

#### 相关知识

##### 选择观测的含义

**观测**，其实就是包含**数据各个变量**的一组实测值，一组包含所有变量取值的数据，笔者认为之所以大家称其为**一组观测**，其实就相当于数据目前已经实实在在在你手中，你站在第三者的角度对其进行的**观察**，很明显你眼中所关心的是如何让各组数据**发挥价值**。

我们举个简单例子，比如现在有一个厨师，他在烹饪一道菜之前最纠结的肯定是**选择合适的食材**，到底是牛肉、猪肉还是羊肉，而这一选择食材的过程就好比是我们之前讲解的**删除和提取**。当厨师确定今晚烹饪牛肉之后，那么他需要在意的就会变成到底用哪一块部位的牛肉，到底是牛腩、牛腿还是牛尾，这就相当于我们今天要学习的**选择观测**。

如果大家还不太理解，请设想一下一群人在进行**体检**，每一个体检项目就相当于一个**变量**，而每一个人的体检数据就是众多体检数据中的**一个观测**。

##### 观测选择之[]符号

为了具体说明问题，我们以下述的**数据框**为例，其中共包含了`teacher, country, age, gender`四个变量，如下图所示：

![img](https://www.educoder.net/attachments/download/204206)

如果我们的需求仅仅是选择数据框中的**某一组确定观测**，如下图所示，那我们只需要使用命令`newdata<-foreignteacher[4,]`即可：

![img](https://www.educoder.net/attachments/download/204207)

如果我们的需求是选择其中的**若干组连续观测**呢？如果前序课程大家都扎实掌握，这个时候估计已经猜到，我们综合使用`:` `[]`即可实现，如下图所示，使用命令`newdata<-foreignteacher[(1:3),]` 即可：

![img](https://www.educoder.net/attachments/download/204208)

##### 根据条件选择观测

我们假设现在有一个**数据集**，包含了若干男性的相关**身体参数**，现在需要分析**中老年男性**的相关身体特征，那么该如何做好前期的数据筛选呢？这时我们上面的两种方法显然就不适用了，我们需要根据具体的条件进行**观测的选择**。第一步，给出一个中老年男性的年龄区间，比如`30`以上算中老年，那么我们此时就只需要按照下列两个条件进行筛选即可：

```
30以上
男性
```

第二步，使用命令`foreignteacher$gender=="M" & foreignteacher$age>30`给出满足上述两个条件的对应**逻辑值**，如下图所示:

![img](https://www.educoder.net/attachments/download/204213)

第三步，根据得到的**逻辑值**，调用函数`which()`即可找到逻辑向量中取值为`TRUE`的**下标值**，这些**下标值**即为满足条件的观测**所在行的编号**，如下图所示：

![img](https://www.educoder.net/attachments/download/204214)

最后我们使用`[]`方括号，即可根据满足条件的观测所对应的**下标值**来选择出满足条件的观测，如下图所示：

![img](https://www.educoder.net/attachments/download/204215)

观测的选择作为数据清洗的基本步骤，本关为大家讲解了**基本的观测选择以及根据条件定向选择观测**的方法，最后依然是我们的额巩固`GIF`时段:

![img](https://www.educoder.net/attachments/download/204222)

#### 编程要求

本关涉及的代码文件为`R_view1.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 将向量`student：c(11,22,31,41,15)`，
  `country： c("CHN", "UK", "UK", "GER", "NL")`，
  `age：c(14, 19, 15, 61, 43)`以及
  `gender：c("M","F","M","F","M")`赋值给数据框`foreignstudent`；
- 使用[]分别选出数据框`foreignstudent`中的第`1`组观测和第`4`组观测，并分别赋值给`result1、result2`；
- 使用[]和:选出数据框`foreignstudent`中的第`1`组到第`2`组观测，并赋值给`result3`；
- 选出数据框`foreignstudent`中的年龄大于`40`且来自荷兰`(NL)`的观测，并赋值给`result4`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_view1.R`，平台将运行用户补全的`R_view1.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/204594)

#### My_Answer

```r
#####	R_view1v.R#####

  ###### begin ######
#Output the results.
student=c(11,22,31,41,15)
country=c("CHN","UK","UK","GER","NL")
age=c(14,19,15,61,43)
gender=c("M","F","M","F","M")
foreignstudent=data.frame(student,country,age,gender)
result1=foreignstudent[1,]
result2=foreignstudent[4,]
result3=foreignstudent[(1:2),]
result4=foreignstudent[which(foreignstudent$age>40&foreignstudent$country=="NL"),]

###### end ######
result1
result2
result3
result4
```

### 第二关

#### 任务描述

对于观测值的选择，我们在第一关中讲解了如何**精确选择某一组观测、某几组连续观测以及根据一定的条件选择观**测。我们试想一下，任何传感器或者数据记录仪所收集的数据都是有**时效**的，很多时候，我们都需要按照时间挑选出符合**我们规定时间区间的数据**，因此本关就将为大家讲解如何实现**基于时间区间**的观测选取。

#### 相关知识

我们先给出一个**包含时间值**的**数据框**，其中时间值赋值给向量`date`，如下图所示：

![img](https://www.educoder.net/attachments/download/204284)

既然要选取出**符合特定时间区间**的观测，那么第一步必然是在时间值上做文章—-将**时间值标准化**！只有当时间标准化后，才能方便进行观测选取。大家回忆一下，将时间值标准化应该使用哪个函数？没错，就是我们前期所讲授的`as.Date`，如下所示，我们给出**时间区间的标准化形式**：

![img](https://www.educoder.net/attachments/download/204291)

接下来为了**时间格式相互一致**，如下图所示，我们通过调用函数`foreignstudent$date<- as.Date(foreignstudent$date, "%m/%d/%y")`，来将数据框中的向量`date`转换为**标准格式**：

![img](https://www.educoder.net/attachments/download/204532)

然后使用逻辑运算符按照`foreignstudent$date>=begin_time & foreignstudent$date<=end_time`求出同时**满足起始时间和终止时间的逻辑向量**，输出如下图所示：

![img](https://www.educoder.net/attachments/download/204531)

然后求出逻辑向量中取值为`TRUE`的位置，如下图所示，输出结果即满足时间区间的**观测所属的行编号**：

![img](https://www.educoder.net/attachments/download/204533)

那么在得到了逻辑值`TRUE`的**索引值**之后，那就只剩一步—-**收割**。怎么收割呢？如下图所示，调用`foreignstudent[which(foreignstudent$date>=begin_time & foreignstudent$date<=end_time),]`，即可根据符合条件的观测索引值选出对应的**数据框观测**：

![img](https://www.educoder.net/attachments/download/204535)

最后，祝大家轻松掌握的同时送上本关的**巩固教学图**：

![img](https://www.educoder.net/attachments/download/204562)

#### 编程要求

本关涉及的代码文件为`R_view2.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 将向量`date: c("01/24/01","09/23/04","09/01/10","01/03/13","08/01/18")`
  `student：c(11,22,31,41,15)`，
  `country： c("CHN", "UK", "UK", "GER", "NL")`，
  `age：c(14, 28, 15, 12, 43)`以及
  `gender：c("M","F","M","F","M")`赋值给数据框`frame`；
- 使用逻辑向量的方法选出处于时间区间`1999-01-01---2002-01-01`的观测，并赋值给`result1`；
- 使用逻辑向量的方法选出处于时间区间`2002-01-01---2005-01-01`的观测，并赋值给`result2`；
- 使用逻辑向量的方法选出处于时间区间`2009-01-01---2011-01-01`的观测，并赋值给`result3`；
- 使用逻辑向量的方法选出处于时间区间`2012-01-01---2018-12-31`的观测，并赋值给`result4`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_view2.R`，平台将运行用户补全的`R_view2.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/204561)

#### My_Answer

```r
#####	R_view2.R#####

  ###### begin ######
#Output the results.
date=c("01/24/01","09/23/04","09/01/10","01/03/13","08/01/18")
student=c(11,22,31,41,15)
country=c("CHN","UK","UK","GER","NL")
age=c(14,28,15,12,43)
gender=c("M","F","M","F","M")
frame=data.frame(date,student,country,age,gender)
frame$date=as.Date(frame$date,"%m/%d/%y")
begin=as.Date("1999-01-01")
end=as.Date("2002-01-01")
result1=frame[(which(frame$date>=begin&frame$date<=end)),]
begin2=as.Date("2002-01-01")
end2=as.Date("2005-01-01")
result2=frame[(which(frame$date>=begin2&frame$date<=end2)),]
begin3=as.Date("2009-01-01")
end3=as.Date("2011-01-01")
result3=frame[(which(frame$date>=begin3&frame$date<=end3)),]
begin4=as.Date("2012-01-01")
end4=as.Date("2018-12-31")
result4=frame[(which(frame$date>=begin4&frame$date<=end4)),]


###### end ######
result1
result2
result3
result4
```

### 第三关:选择观测进阶二

#### 任务描述

在众多的观测选择方法中，有一个函数一直站在**顶端从未被超越**，这就是`subset`函数，如果你觉得掌握了前两关的内容就掌握了观测的选择，那只能说还太`naive`，前序课程只是清晰地给大家展现观测选择的原理，只有经过本关的学习，你会在观测的选择中更为**游刃有余**。

#### 相关知识

##### 单一条件的观测选择

本关我们将以如下所示的数据框`foreignstudent`为例，一共包含五个向量，分别是`date, student, country, age, gender`:

![img](https://www.educoder.net/attachments/download/204581)

以单一条件选出观测，比如我们只需要调用函数`subset(foreignstudent, age>20)`即可得到所有满足年龄`age`大于`20`的观测，如下图所示：

![img](https://www.educoder.net/attachments/download/204582)

##### 混合条件的观测选择

很多实际场景中，我们的需求**都不是单一的**，这时我们就需要面向混合条件进行观测的选择，第一步，明确一个原则，凡是这种**基于多种条件**的观测选择，我们一般都需要借助类似`&`或者`|`的**逻辑运算符**，比如调用`subset(foreignstudent, age>50 | country=="UK")`即可输出年龄大于`50`或者来自英国的观测，如下图所示：

![img](https://www.educoder.net/attachments/download/204583)

当然**逻辑运算不仅仅局限于两两之间**，如下图所示，还可以进行**三个及以上**的条件判断：

![img](https://www.educoder.net/attachments/download/204584)

##### select参数

在函数`subset`中，还有一个极其重要的参数`select`，什么作用呢？顾名思义，**选择**。那选择什么呢？我们继续拿厨师举例子，选择牛肉烹饪就相当于是提取或者删除数据，而选择用牛腿肉就相当于是观测的提取，而对牛腿肉是否去皮、去筋等就相当于是`select`的作用。

简单来讲，就是有的变量值我们在某些数据分析中**并不希望使用**，所以需要在选择观测时就将其**剔除**，那么此时我们就需要加入`select`参数进行**调控**，比如调用函数`subset(foreignstudent, age>20, select=date:age)`即可选出满足年龄大于`20`的观测，且选出的观测只包含从向量`date`到`age`的数据值，具体输出如下图所示：

![img](https://www.educoder.net/attachments/download/204585)

如果我们需要选择的向量**并非连续**的呢？那么我们只需要对`select`参数稍加修改，调用函数`subset(foreignstudent, age>20, select=c(student,age,gender))`即可选择所有年龄大于`20`的**观测**，并且只选择向量`student,age,gender`的数据值，输出如下图所示：

![img](https://www.educoder.net/attachments/download/204586)

综上所述，我们可以调用`subset`函数完成**单一、混合条件**的观测选择，以及基于`select`参数的观测选择，最后是我们融会贯通的`GIF`学习图：

![img](https://www.educoder.net/attachments/download/204591)

#### 编程要求

本关涉及的代码文件为`R_view3.R`，本次编程任务是补全右侧代码片段中`begin`至`end`中间的代码，具体要求如下：

- 将向量`height: c(180,178,168,178,165)`，
  `student：c(1,2,3,4,5)`，
  `country： c("RUS", "USA", "USA", "CHN", "CHN")`，
  `age：c(19, 25, 37, 61, 52)`以及
  `gender：c("M","F","M","F","M")`赋值给数据框`frame`；
- 调用函数`subset`选出身高大于`170`的观测，并赋值给`result1`；
- 调用函数`subset`选出身高大于`175`且年纪大于`40`的观测，并赋值给`result2`；
- 调用函数`subset`选出身高大于`175`且年纪大于`40`的观测，且所选择的观测包含从向量`height`到向量`age`的所有数据值，结果赋值给`result3`；
- 调用函数`subset`选出身高大于`175`且年纪大于`40`的观测，且所选择的观测只包含向量`height、age、gender`，结果赋值给`result4`。

#### 测试说明

测试过程：

- 本关涉及到的测试文件是`R_view3.R`，平台将运行用户补全的`R_view3.R`文件，得到数据；
- 将数据与答案比较，判断程序是否正确。

以下是测试样例：

测试输入：

预期输出：

![img](https://www.educoder.net/attachments/download/204592)

#### My_Answer

```r
#####	R_view3.R#####

###### begin ######
#Output the result.
height=c(180,178,168,178,165)
student=c(1,2,3,4,5)
country=c("RUS", "USA", "USA", "CHN", "CHN")
age=c(19, 25, 37, 61, 52)
gender=c("M","F","M","F","M")
frame=data.frame(height,student,country,age,gender)
result1=subset(frame,height>170)
result2=subset(frame,height>175&age>40)
result3=subset(frame,height>175&age>40,select = height:age)
result4=subset(frame,height>175&age>40,select = c(height,age,gender))



###### end ######
result1
result2
result3
result4
```

