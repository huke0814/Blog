---
title: my first
date: 2019-09-21 21:34:52
tags: 随记
categories: Software language
mathjax: true
---

# markdown教程

## 一、标题

```txt
# 一级标题
## 二级标题
### 三级标题
注意井号与标题之间有一个空格
按enter键可以退出各级操作的对齐，例如小黑点，数字序号，引用等
```

## 二、插入链接

```
[链接名字](链接地址)
```

- 例如

​                [百度](www.baidu.com)

## 三、插入图片

```
![]()
```

> 图片链接可以是本地的，也可以是网络上的，例如百度图片的链接，或者存在你的GitHub上的图片
>
> 括号内可以加图片标题。(即鼠标放在图片上可以显示内容)

- 图例

![插入图片](C:\Users\huke0\Desktop\代码速查表\sk.png "我的标题")

- Markdown 还没有办法指定图片的高度与宽度，如果你需要的话，你可以使用普通的 <img> 标签。

  <img src="C:\Users\huke0\Desktop\代码速查表\sk.png" width="60%" height="50">

## 四、文字引用

```
> 引用内容
>> 引用内容
>>> 引用内容
```

> 一切皆有可能 
>
> > 一切皆有可能 
> >
> > > 一切皆有可能 

> > 一切皆有可能

> > > - - - 一切皆有可能 

- > 一切皆有可能 

## 五、段落格式

#### 1、粗体和斜体

```
*斜体*
**粗体**
***粗斜体***
```

- 例如：   *斜体*  **粗体** ***粗斜体***

------

#### 2、分割线

```
***
* * *
```

------

#### 3、删除线

```
~~删除~~
```

- 例如：~~删除~~

------

#### 4、下划线

------

#### 5、脚注

[^master]: 每天都要保持战斗状态！

`master`

------

#### 6、列表

- 无序列表(`*` `+` `-`)

  ```
  - 第一项
  - 第二项
  ```

- ------

- 有序列表(序号+`.`)

  ```
  1. 第一项
  2. 第二项
  
  ```

  1. 第一
  2. 第二

  进入列表格式后，按`Enter`会延续列表格式，如果要退出该格式，则继续按一次`Enter`。

## 六、代码引用

```txt
单行引用：`hello world`
多行引用： ```python
注意：`是键盘左上角的~键
	加上语言名字后代码会高亮

```

- 例如：

  ​		单行引用：各种编程语言都习惯用`hello world`作为用例。

  ​		多行引用：

  ```python
  print('hello world')
  print(123456)
  
  ```

    

## 七、嵌入HTML

- 例如： 把网站的API嵌入
- 百度地图API：[http://api.map.baidu.com/lbsapi/createmap/index.html](http://api.map.baidu.com/lbsapi/createmap/index.html)  没有密钥搞不成
- 嵌入YouTube：找到视频地址，点击分享中的嵌入按钮，复制代码，在markdown文件中粘贴。
- 

<iframe width="560" height="415" src="https://www.youtube.com/embed/dA8Kea3cWXg" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


bilibili

<iframe src="//player.bilibili.com/player.html?aid=68142772&cid=118091292&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

# 八、表格

- Markdown 制作表格使用 `|`来分隔不同的单元格，使用 `-` 来分隔表头和其他行.

```
|  表头   | 表头  |
|  ----  | ----  |
| 单元格  | 单元格 |
| 单元格  | 单元格 |

```

|  表头  |  表头  |
| :----: | :----: |
| 单元格 | 单元格 |
| 单元格 | 单元格 |

# 九、插入数学公式

当你需要在编辑器中插入数学公式时，可以使用两个美元符 `$$ `包裹**TeX**或**LaTeX格式**的数学公式来实现。如:

```
$$
\mathbf{V}_1 \times \mathbf{V}_2 =  \begin{vmatrix} 
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial X}{\partial u} &  \frac{\partial Y}{\partial u} & 0 \\
\frac{\partial X}{\partial v} &  \frac{\partial Y}{\partial v} & 0 \\
\end{vmatrix}
$$

```

- 输出为：

$$
\mathbf{V}_1 \times \mathbf{V}_2 =  \begin{vmatrix} 
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial X}{\partial u} &  \frac{\partial Y}{\partial u} & 0 \\
\frac{\partial X}{\partial v} &  \frac{\partial Y}{\partial v} & 0 \\
\end{vmatrix}
$$

