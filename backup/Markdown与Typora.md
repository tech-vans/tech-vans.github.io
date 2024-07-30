# **Markdown与Typora**

## **1.什么是Markdown和Typora？**

### 1.1Markdown介绍

Markdown 是一种轻量级标记语言，使用易读易写的纯文本格式编写文档；Markdown 编写的文档可以导出 HTML 、Word、图像、PDF、Epub 等多种格式的文档；Markdown 编写的文档后缀为 .md ；.markdown。

### **1.2Typora介绍**

Typora编辑器让人们能更简单地用Markdown语言书写文字，解决了使用传统的Markdown编辑器写文的痛点，并且界面简洁优美，实现了实时预览等功能。

***

## **2.Markdown语法**

#### 2.1 标题

使用 # 可以表示标题，一级标题对应一个 # ，二级标题对应两个 # 号，最多至六级标题

在Typora中，# 后要紧接着一个空格才能表示标题，否则就是普通字符

在Typora中，也可以使用快捷键Ctrl+（1，2，3，4，5，6）表示相对应的标题

Ctrl+0表示段落。标题快捷键信息可在菜单栏中的段落选项下查看

#### 2.2 字体

用一对星号*括住的文本表示斜体文本,也可以用一对下划线_括住文本来表示斜体文本,使用Typora的快捷键Ctrl+I来表示斜体文本;

用一对**括住的文本表示粗体文本，也可以用一对__括住的文本来表示粗体文本,也可以使用Typora的快捷键Ctrl+B来表示粗体文本;

用一对括住的***或___文本表示粗斜体文本。

#### 2.3 各种线

分割线，可以使用三个及以上的 + 号或 * 号或 - 来表示一条分割线；
由三个*号表示的分割线：

***

由三个+号表示的分割线：

+++



由三个-号表示的分割线：

---

删除线，可以使用一对~~括住的文本来表示删除文本；在Typora中，也可以使用快捷键Alt+Shift+5来加删除线

~~Hello world ！~~

下划线，可以使用HTML的标签<u>和</u>表示增加下划线的文本，如：<u>要增加下划线的文本</u>，下划线；

在Typora中，也可以使用快捷键Ctrl+U来增加下划线，语法也是相同的，下划线。

***

#### 2.4 列表

无序列表：使用`*`，`+`或`-`标记符号来表示无序列表项，记住要在标记符号后添加一个空格

* 属性1

* 属性2

有序列表：可以使用数字加上`.`再加上空格来表示有序列表

1. 属性1
2. 属性2

***

#### 2.5 区块

（使用>加空格来表示区块）

> 区块1
>
> > 区块2
> >
> > > 区块3

#### 2.6 代码

如果是一行代码，可以使用段内代码块来表示，用一对 `（数字1旁边的符号）括住代码

``printf("Hello World!")``

如果是代码段，那么可以使用三个 ` 加Enter/空格+编程语言来表示(可以在代码块的右下角选择编程语言)

```java
include <stdio.h>

void main(){
	printf("Hello world!\n");
}package day12_Thread;

import java.util.concurrent.ArrayBlockingQueue;
import java.util.concurrent.Executors;
import java.util.concurrent.ThreadPoolExecutor;
import java.util.concurrent.TimeUnit;

public class ThreadPoll_demo2 {


    public static void main(String[] args) {
        //参数 七个  --------核心线程数量，最大线程数量，空闲线程最大存活时间,时间单位，
        //                  任务队列，创建线程工厂，任务的拒绝策略
        ThreadPoolExecutor pool = new ThreadPoolExecutor(
                3,
                6,
                20,
                 TimeUnit.SECONDS,
                 new ArrayBlockingQueue<>(3),
                 Executors.defaultThreadFactory(),
                 new ThreadPoolExecutor.AbortPolicy());


        // pool.submit();
    }

}

```

***

#### 2.7 链接

链接的使用方式有两种语法，如下：

[链接文字] (链接地址)  或 <链接地址>
例如

[百度](https://www.baidu.com/)     <https://www.baidu.com/>

当鼠标移到相应的链接文字时，按住Ctrl+鼠标左键点击访问；链接除了可以打开相应的网页外，还可以打开本地文件，使用方式类似，不过链接地址需要使用本地文件的地址，相对地址、绝对地址均可

我们也可以使用链接来实现页内跳转，语法为：[链接文字] (#标题文字)
示例：[跳转到第一章第一节] (#1.1Markdown介绍)
[跳转到第一章第一节](#1.1Markdown介绍)

#### 2.8 图片

我们也可以在Markdown文档中插入图片

在Typora中，也可以直接使用Ctrl+C，Ctrl+V来直接进行复制粘贴图片，但是，由于Markdown是需要图片的地址的，所以需要简单设置一下Typora：

（1）点击文件 --> 偏好设置 --> 图像，可以自行设置选择将图片复制到哪个文件夹

（2）选择复制到指定路径，然后在下面一栏中填写./img，表示将图片复制到你正在编辑的文档同一级的img文件夹下。在下面的选项中，勾选第一、二、三项。正因为勾选了第二项，所以当我们在插入网络图片时，Typora会自动帮我们将网络图片下载到指定的路径下，前面的"菜鸟教程"图片便是如此

（3）由于Markdown的特殊语法，故经常会出现图片加载失败的情况，很大的可能就是因为在指定的路径上找不到相应的图片，当然，有时候也是由于Typora的原因，重启Typora即可

#### 2.9 表格

Markdown 制作表格使用 | 来分隔不同的单元格，使用 - 来分隔表头和其他行。

|       | 属性1 | 属性2 |
| :---: | :---: | :---: |
| 记录1 |       |       |
| 记录2 |       |       |
| 记录3 |       |       |

我们可以设置对齐方式{  :-表示左对齐，-:表示右对齐，:-:表示中间对齐  } 

Typora中，我们可以使用快捷键Ctrl+T来插入表格，并选择行列，当选中表格某一单元格时，可以在表格左上角手动设置对齐方式，右上角选择更多操作。

## 3.Typora与数学公式

后续补充