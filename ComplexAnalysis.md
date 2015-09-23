#复变函数的积分

[TOC]
<script type="text/javascript"
 src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>
##3.1复积分的概念

$$\int_{ c }{ f(z)dz=\int_{ c } (u+iv)(dx+idy) } =\int_{ c } udx-vdy+i\int_{ c } vdx+udy$$

###性质
>[设$f(z)$, $g(z)$在逐段光滑的有向曲线$C$上连续]

* 线性性$\int_c(af(z)+bg(z))dz=a\int_cf(z)dz+b\int_cg(z)dz$[a,b ~const]
* 设$C^-$为$C$的逆向曲线, 则$\int_{C^-}f(z)dz=-\int_Cf(z)dz$
* $\int_{C}f(z)dz=\int_{C_1}f(z)dz+\int_{C_2}f(z)dz$[$C=C_1+C_2$]
* $|\int_Cf(z)dz|\le \int_C|f(z)||dz|=\int_C|f(z)ds|\le ML$[若$f(z)$在$C$上有界:$|f(z)|\le M, L$为$C$的长度]

##3.2  柯西积分定理

如果函数$ f (z)$在`单连通域`$D$`内`处处解析, 则它在$D$内沿`任何一条封闭曲线`$C$ 的积分为零

>注1: 定理中的曲线$C$可以不是简单闭曲线
>注2: 如果曲线$C$是$D$的边界, $f (z)$在$D$内解析, 在边界$C$ 上连续, 则$ f (z)$在边界上的积分仍然有$\oint_c f(z)=0$
>推论: 若函数$ f (z)$在单连通域$D$内处处解析,曲线$C$属于$D$，$\int_c f(z)dz$与路径无关仅与起点和终点有关

###闭路变形原理

假设$C$和$C_1$为任意两条简单闭曲线, $C_1$在$C$内部,设函数 $f (z)$在$C$及$C_1$所围的二连域 D内解析, 在边界上连续，则$$\oint_Cf(z)dz=\oint_{C_1}f(z)dz$$

这说明解析函数沿简单闭曲线积分不因闭曲线在区域内作连续变形而改变它的值。

###复合闭路定理

设$C_1,C_2,...,C_n$为简单闭曲线(互不包含且不相交)，$C$为包含$C_1,C_2,...,C_n$的简单闭曲线。D由边界曲线$\Gamma =C\cup C_{ 1 }^{ - }\cup C_{ 2 }^{ - }\cup ...\cup C_{ n }^{ - }$所围成的闭连通区域，$f(z)$在$D$内解析, 在$\overline { D } =D\cup \Gamma $上连续，则$\oint_{ \Gamma  }{ f(z)dz}=0 $或者$\oint_{ C }{ f(z)dz } =\sum _{ i=1 }^{ n } \int_{ C_{ i } } f(z)dz$

##Applications

- 计算$$I=\oint_{ C }{ \frac { dz }{ (z-z_{ 0 })^{ n } }  }$$
[$C$为$|z-z_0|=r>0$]

>$z=z_0+re^{i\theta}(0\le \theta \le 2\pi)$
>带入得到
>$$I=0(n \neq 1)$$
>$$I=2\pi i(n=1)$$

-求$\oint_C \frac{1}{z^2-z}$, $C$为包含0与1的任何简单闭曲线
>Solution 1:闭路变形原理
>原式=$\oint_C \frac{dz}{z-1}-\oint_C \frac{dz}{z}=0[利用变形原理将这个闭曲线变成两个圆]$
>
>Solution2:复合闭路定理
>$\oint_C \frac{1}{z^2-z}=\oint_{C_1} \frac{dz}{z^2-z}+\oint_{c_2} \frac {dz}{z^2-z}$
>$=\oint_{C_1}\frac{dz}{z-1}-\oint_{C_1}\frac{dz}{z}+\oint_{C_2}\frac{dz}{z-1}-\oint_{C_2}\frac{dz}{z}=0$

##3.3  柯西积分公式

$f(z)$在简单闭曲线$C$所围成的区域$D$内解析，$\overline D = D\cup C$上连续，是$D$内任意一点，则$$f(z_0)=\frac{1}{2\pi i} \oint_C \frac{f(z)}{z-z_0}dz$$

###推论: 平均值公式

如果$C$是圆周$z=z_0+Re^{i\theta}$, 那么$$f(z_{ 0 })=\frac { 1 }{ 2\pi i } \int_{ 0 }^{ 2\pi  } \frac { f(z_{ 0 }+Re^{ i\theta  }) }{ Re^{ i\theta  } } iRe^{ i\theta  }d\theta =\frac { 1 }{ 2\pi  } \int_{ 0 }^{ 2\pi  }{ f(z_{ 0 }+Re^{ i\theta  }) } d\theta =f(z_{ 0 }+R{ e }^{ i\xi  })$$
一个解析函数在圆心处的值等于它在圆周上的平均值

###推论: 复区域应用

设$f (z)$在二连域 $D$内解析，在边界上连续，$z_0$属于二连域，那么$$f(z_{ 0 })=\frac { 1 }{ 2\pi i } \int_{ C_1 } \frac { f(z) }{z-z_0  } dz -\frac { 1 }{ 2\pi i } \int_{ C_2  }\frac { f(z) }{z-z_0  } dz$$

###最大模原理

设D为有界单连通或复闭路多连通区域，$f(z)$在$D$内解析,在$\overline { D } =D\cup \partial D$上连续，则$|f(z)|$在$\partial D$上取得最大值。
注: 当$f(z)\neq const$, $|f(z)|$在且仅在$\partial D$上取得最大值。

##Applications

- 求$\int_C \frac{1}{z^2}dz$
![3-1](3-1.png)
>存在 $f (z)$的解析单连通域D包含曲线 $C$ ，故积分与路径无关，仅与起点和终点有关。
>那么$\int_C\frac{1}{z^2}dz = -\frac{1}{z}|_{(0,i)}^{(0,-3i)}=\frac{4i}{3}$

- 计算$I=\oint_{ C } \frac { { e }^{ z } }{ z(z+1)(z-2) } dz\quad \quad C:|z|=r(r\neq 1,2)
![3-2](3-2.png)
>* $$0<r<1,I=\oint_{ C } \frac { \frac { { e }^{ z } }{ (z+1)(z-2) }  }{ z } dz=-\pi i $$
>* $$1<r<2,I=\oint_{ C_{ 1 } } +\oint_{ C_{ 2 } } =-\pi i+2\pi i\frac { e^{ z } }{ z(z-2) } |_{ z=-1 }=-\pi i+\frac { 2\pi i }{ 3e } $$
>* $$r>2,I=\oint_{ C_{ 1 } } +\oint_{ C_{ 2 } } +\oint_{ C_{ 3 } } =-\pi i+\frac { 2\pi i }{ 3e } +\frac { e^{ 2 }\pi  }{ 3 } i$$

##3.4 解析函数的高阶导数

一个解析函数不仅有一阶导数, 而且有各高阶导数, `它的值也可用函数在边界上的值通过积分来表示`. 这一点和实变函数完全不同

解析函数$f(z)$的导数仍为解析函数, 它的$n$阶导数为$$f^{ n }(z)=\frac { n! }{ 2\pi i } \oint_{ C } \frac { f(\varsigma ) }{ (\varsigma -z)^{ n+1 } } d\varsigma , (n=1,2,...)$$

其中$C$为在函数$f (z)$的解析区域 $D$内围绕$z_0$的任何一条正向简单闭曲线, 而且它的内部全含于$D$
高阶导数公式的作用, 不在于通过积分来求导, 而在于通过求导来求积分
$$\oint_{ C } \frac { f(z) }{ (z-z_{ 0 })^{ n+1 } } dz=\frac { 2\pi i }{ n! } f^{ n }(z_0)$$

###$Cauchy$不等式

$f(z)$在$C_R=\{|z-z_0|=R\}$内解析，在$C_R$上连续，则$$f^{ n }(z_{ 0 })\le \frac { Mn! }{ R^{ n } } (M=max|f(z)|)$$

- 注1: 解析函数的导数模的估计与区域的大小有关
- $n=0 \Rightarrow |f(z_0)|\le M=max|f(z)|$
