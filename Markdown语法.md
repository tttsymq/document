# Markdown

Markdown是一种轻量级的标记语言，一般后缀为**.md**，**.markdown**

---

#### markdown常用的语法

#### 1.标题

> 标题使用#，##，###等设置为一级标题，二级标题，三级标题等，也可以使用对应的html标签来进行设置'<h1>一级标题</h1>'

```
# 一级标题    或者  <h1>一级标题</h1>
## 二级标题         <h2>二级级标题</h2>
### 三级标题
#### 四级标题
##### 五级标题
```



### 2.段落

> markdown没有段落特殊的段落格式，可以直接使用空格加换行的方式。

#### 3.字体

* *斜体* ： 在文本两侧加*或者加_
* **粗体**：  在文本两侧加**或者加__
* ***粗斜体***：在文本两侧加***或者加 ___
* ~~删除线~~：在文本两侧加~~
* <u>下划线</u>：直接使用html标签<u></u>

#### 4.分割线

~~~
使用3个或者3个以上的* - 等
***
---
————————
~~~

####  5.脚注[^1]

[^1]:注明显示的内容

#### 6.列表

~~~
列表分为有序列表和无序列表：
无序列表使用 * + - 
有序列表使用数字加.表示
~~~

* 1
* 2
* 3

1. 第一条
2. 第二条
3. 第三条

#### 7.代码块

> ~~~
> 使用~~~
> ~~~
>
> ```
> 使用```
> ```

#### 8.链接

~~~
使用[链接名](链接地址) :[百度地址](https://www.baidu.com)
~~~

[百度地址](https://www.baidu.com)

<https://www.baidu.com>

#### 9.图片

~~~
![](图片地址)
~~~



![](https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1589542563263&di=58269031d4a8bfb0c9b4a5303f6cc6ee&imgtype=0&src=http%3A%2F%2Fimg.yoyou.com%2Fuploadfile%2F2017%2F0727%2F20170727014939103.jpg)

<img src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1589542563263&di=58269031d4a8bfb0c9b4a5303f6cc6ee&imgtype=0&src=http%3A%2F%2Fimg.yoyou.com%2Fuploadfile%2F2017%2F0727%2F20170727014939103.jpg" width="50px">



| 表头 | 表头 | 表头 |
| :--: | :--: | :--: |
|      |      |      |
|      |      |      |

**1、横向流程图源码格式：**

```
​```mermaid
graph LR
A[方形] -->B(圆角)
    B --> C{条件a}
    C -->|a=1| D[结果1]
    C -->|a=2| E[结果2]
    F[横向流程图]
​```
```

**2、竖向流程图源码格式：**

```
​```mermaid
graph TD
A[方形] --> B(圆角)
    B --> C{条件a}
    C --> |a=1| D[结果1]
    C --> |a=2| E[结果2]
    F[竖向流程图]
​```
```

**3、标准流程图源码格式：**

```
​```flow
st=>start: 开始框
op=>operation: 处理框
cond=>condition: 判断框(是或否?)
sub1=>subroutine: 子流程
io=>inputoutput: 输入输出框
e=>end: 结束框
st->op->cond
cond(yes)->io->e
cond(no)->sub1(right)->op
​```
```

**4、标准流程图源码格式（横向）：**

```
​```flow
st=>start: 开始框
op=>operation: 处理框
cond=>condition: 判断框(是或否?)
sub1=>subroutine: 子流程
io=>inputoutput: 输入输出框
e=>end: 结束框
st(right)->op(right)->cond
cond(yes)->io(bottom)->e
cond(no)->sub1(right)->op
​```
```

**5、UML时序图源码样例：**

```
​```sequence
对象A->对象B: 对象B你好吗?（请求）
Note right of 对象B: 对象B的描述
Note left of 对象A: 对象A的描述(提示)
对象B-->对象A: 我很好(响应)
对象A->对象B: 你真的好吗？
​```
```

**6、UML时序图源码复杂样例：**

```
​```sequence
Title: 标题：复杂使用
对象A->对象B: 对象B你好吗?（请求）
Note right of 对象B: 对象B的描述
Note left of 对象A: 对象A的描述(提示)
对象B-->对象A: 我很好(响应)
对象B->小三: 你好吗
小三-->>对象A: 对象B找我了
对象A->对象B: 你真的好吗？
Note over 小三,对象B: 我们是朋友
participant C
Note right of C: 没人陪我玩
​```
```

**7、UML标准时序图样例：**

```
​```mermaid
%% 时序图例子,-> 直线，-->虚线，->>实线箭头
  sequenceDiagram
    participant 张三
    participant 李四
    张三->王五: 王五你好吗？
    loop 健康检查
        王五->王五: 与疾病战斗
    end
    Note right of 王五: 合理 食物 <br/>看医生...
    李四-->>张三: 很好!
    王五->李四: 你怎么样?
    李四-->王五: 很好!
​```
```

**8、甘特图样例：**

```
​```mermaid
%% 语法示例
        gantt
        dateFormat  YYYY-MM-DD
        title 软件开发甘特图
        section 设计
        需求                      :done,    des1, 2014-01-06,2014-01-08
        原型                      :active,  des2, 2014-01-09, 3d
        UI设计                     :         des3, after des2, 5d
    未来任务                     :         des4, after des3, 5d
        section 开发
        学习准备理解需求                      :crit, done, 2014-01-06,24h
        设计框架                             :crit, done, after des2, 2d
        开发                                 :crit, active, 3d
        未来任务                              :crit, 5d
        耍                                   :2d
        section 测试
        功能测试                              :active, a1, after des3, 3d
        压力测试                               :after a1  , 20h
        测试报告                               : 48h
​```
```