---
layout: post
title:  "向量空间"
categories: "linear-algebra"
---

开始看机器学习，才发现数学严重不够用了，十分有必要重温一下。

主要用这两本参考书：Sheldon Axler的[《线性代数应该这样学》](http://book.douban.com/subject/3715623/)和Steven J. Leon的[《线性代数》](http://book.douban.com/subject/2016789/).  Sheldon的书侧重于向量空间，内积空间，线性变换，算子等线性代数中最重要概念的构建，开篇即直接导入向量空间的概念，只是在最后一章提了一点行列式的东西。对于掌握线性空间的本质很有好处。但没有任何实际应用的例子。Steven的书英文名为&lt;Linear Algebra with Applications&gt;, 举了很多例子，不限于数学和物理，生态社会经济等方面都有所涉猎。看完这本书，就不会问出[线性代数有什么用?](http://www.zhihu.com/question/36845076) 这样的问题了。



##**[域]**

很多教材上只提到了标量和向量，标量通常为实数或复数，但没有说为什么不能是整数。然后我碰到这个命题:$$av=0 => a= 0 \vee v=0 $$就死活证不出来，因为教材上没有给出标量都有乘法逆的假设。
关于群，环，域等抽象代数的概念不是本笔记重点，就不列出来了，直接给出域的性质：
域是集合$$F$$和其上定义的两种运算$$+$$和$$*$$,若满足如下公理

1.**封闭性**

$$\forall a,b \in F, a+b \in F, a*b\in F$$

2.**结合律**

$$ \forall a,b,c \in F, (a+b)+c = a+(b+c), (a*b)*c=a*(b*c)$$

3.**交换律**

$$ \forall a,b \in F, a+b = b+a, a*b=b*a$$

4.**乘法对加法的分配律**

$$ \forall a,b,c \in F, a*(b+c)=(a*b)+(a*c) $$

5.**加法单位元**

$$ \exists 0 \in F, \forall a \in F, 0+a=a $$

6.**乘法单位元**

$$ \exists 0\in F \wedge 1\neq 0, \forall a \in F, 1*a=a $$

7.**加法逆**

$$ \forall a \in F, \exists (-a)\in F, a+(-a)=0 $$

8.**乘法逆**

$$ \forall a \in F, \exists a^{-1}\in F, a*a^{-1}=1$$


## **[向量空间]**

向量空间的基本定义：
给定集合$$V$$和数域$$F$$,称$$V$$上元素为向量,$$F$$上元素为标量,在其上定义有两种二元运算:

1.**向量加法**

$$\forall u,v \in V, u+v \in V $$

2.**标量乘法**

$$\forall v \in V, a \in F, a\cdot v \in V $$


若$$V,F, +, \cdot$$满足如下公理, 即为一个向量空间


1.**加法交换律(commutativity)**

$$\forall u,v \in V, u+v=v+u $$

2.**加法结合律(assiociativity)**

$$\forall u,v,w \in V, (u+w)+v=u+(w+v) $$

3.**加法单位元**

$$\exists 0\in V, \forall v \in V, 0+v=v$$ 

4.**加法逆元**

$$\forall v \in V, \exists (-v)\in V, v+(-v)=0$$

5.**标量乘法对向量加法的分配律**

$$\forall u,v \in V, a \in F, a\cdot(u+v)=(a\cdot u)+(a\cdot v)$$

6.**标量乘法对标量加法的分配律**

$$\forall v \in V, a,b \in F, (a+b)\cdot v = (a\cdot v)+(b\cdot v)$$

7.**标量乘法对标量域乘法相容**

$$\forall v \in V, a,b \in F, a\cdot(b\cdot v )= (a*b)\cdot v$$

8.**乘法单位元**

$$ \forall v \in V, 1\cdot v = v $$

## **向量空间基本性质**

* 零向量唯一
* :$$\forall a\in F, a\cdot 0=0$$
* :$$\forall v\in V, 0\cdot v=0$$
* :$$ a \in F, v \in V, a\cdot v=0 => a=0 \vee v=0$$
* 向量加法逆唯一
* :$$ \forall v\in V, -1 \cdot v = -v $$

[域]: https://zh.wikipedia.org/wiki/%E5%9F%9F_(%E6%95%B8%E5%AD%B8)
[向量空间]: https://zh.wikipedia.org/wiki/%E5%90%91%E9%87%8F%E7%A9%BA%E9%97%B4
