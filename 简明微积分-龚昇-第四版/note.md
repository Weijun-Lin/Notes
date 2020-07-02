# 简明微积分 龚昇 第四版

## 第一章 微积分的概念

### 1.1 函数与极限

#### 数列极限和函数极限

数列极限：对于无穷序列$a_1,a_2,\dots,a_n$，极限表示为：$\lim_{n\to \infty} a_n = A$，首先要A存在

如果两个数列有极限，它们对应的和、差、积、商组成的数列的极限，分别位对应的和、差、积、商

函数极限：对于函数$y=f(x)$，当自变量x无限接近a时，f(x)趋向于一个固定的常数A，A即为极限，即$\lim_{n\to \infty}f(x) = A$

#### 连续函数

函数$f(t)$在$t=t_0$连续，即$\lim_{t\to t_0} = f(t_0)$成立

**闭区间**$[a,b]$上的连续函数一定存在两点$\xi,\eta$，使$f(\xi)=M,f(\eta)=m$，M，m分别为最大最小值

### 1.2 定积分

#### 定义

函数$f(x)$在区间$[a,b]$上的定积分记作：$I = \int_a^bf(x)dx$，更实质的表示形式：$\sigma = \Sigma_{i=1}^nf(\xi_i)\Delta x_i$，其中$\Delta x_i = x_i - x_{i-1}$，$\xi_i$就是区间$[x_{i-1},x_i]$中任一点。对切分法T，令$\lambda(T) = \max_{1\leq i \leq n}\Delta x_i$，当$\lambda(T)\to 0$时取得的极限就是定积分

#### 性质

定积分对应了函数在对应区间内图像和x轴形成的面积

<img src="./img/1-1.png" style="zoom:60%;" />

<img src="./img/1-2.png" style="zoom:60%;" />

#### 积分中值定理

对于在$[a,b]$连续的函数$f(x)$，在此闭区间上存在一点$\xi$使得：
$$
\int_a^bf(x)dx=f(\xi)(b-a)
$$
证明如下：**使用最值证明**

设此区间上最大最小值分别为：M，m可得：
$$
m(b-a)\le \int_a^bf(x)dx \le M(b-a) \\
即：m \le \frac{\int_a^bf(x)dx}{b-a} \le M \\
令，\mu = \frac{\int_a^bf(x)dx}{b-a}
$$
因为$f(x)$是闭区间上的连续函数，且m，M为两个最值，所以存在点$\xi$满足$f(\xi) = \mu$，即：
$$
\int_a^bf(x)dx=f(\xi)(b-a)
$$

书本补充：

积分第二中值定理：

函数$f(x),\varphi(x)$都在闭区间连续，且$\varphi(x)$在闭区间内不变号，则有以下式子成立
$$
\int_a^b f(x)\varphi(x)dx = \varphi(\xi)\int_a^b f(x)dx
$$


### 1.3 微商与微分

#### 微商

微商的定义：$\lim_{\Delta x \to o} \frac{f(x_0+\Delta x)-f(x_0)}{\Delta x}$

$y=f(x)$是定义在$[a,b]$上的函数，$x_0$是区间内一点，上式的极限存在说明函数在点$x_0$处可微，称为微商或者导数

记作：$f'(x_0)或\frac{d_y}{d_x}\bigg{|}_{x=x_0}$

如果$f(x)$在区间内处处可微，那么$f'(x)$则为函数的导函数

从微商的定义出发，可以得出：**如果函数$y=f(x)$在一点$x_0$可微，则在这点一定连续**，证明如下：
$$
f(x+\Delta x)-f(x)=\frac{f(x+\Delta x)-f(x)}{\Delta x} \times \Delta x
$$
令$\Delta x \to 0$，因为可微，所以$\lim_{\Delta x \to o} \frac{f(x+\Delta x)-f(x)}{\Delta x}$存在，所以可得$\lim_{\Delta x \to 0}[f(x+\Delta x)-f(x)]=0$，即$f(x)$在点$x_0$处连续

常数的微商为0

#### 微分

微分和微商密不可分，设函数$y=f(x)$在点x处有微商$f'(x)$，则在点x的微分为：$dy = f'(x)\Delta x$

对于$\Delta y = f(x_0+\Delta x) - f(x_0)$，根据微商定义有下式成立：
$$
\lim_{\Delta x \to 0}\frac{\Delta y}{\Delta x}=\lim_{\Delta x \to 0}\frac{f(x_0+\Delta x) - f(x_0)}{\Delta x} = f'(x_0) \\
若令，\frac{\Delta y}{\Delta x} - f'(x_0) = \alpha \\
即，\Delta y = f'(x_0)\Delta x + \alpha \Delta x
$$
因为当$\Delta x \to 0$，$\alpha \to 0$，所以$\alpha \Delta x$比$f'(x_0)\Delta x$更快趋于0，也就是说**可以使用微分近似代替函数的改变量**

函数$y=x$的微分为$dx = \Delta x$，即自变量的微分就是自变量的该变量，所以，微分也可表示为：$dy = f'(x) dx$

所以微商的另一种表示法：$\frac{dy}{dx} = f'(x)$，即因变量和自变量的微分商

#### 微分中值定理

##### 拉格朗日中值定理（微分中值定理）

若函数$f(x)$在$[a,b]$上连续，在开区间可微，则在$(a,b)$中存在一点$\xi$，使得：$\frac{f(b)-f(a)}{b-a}=f'(\xi)$

证明上述定理需要引入**极值概念，费马定理，罗尔定理**

1. **极值概念**

	存在正数$\xi$使得对区间$(x_0-\xi,x_0+\xi)$内的任意点x，都有$f(x) \le f(x_o)$，则说明$f(x)$在$x_0$取到极大值，极小值定义相似

2. **费马定理**

	**如果函数在$x_0$可微，并在此处取得极值，那么必有$f'(x_0)=0$**

	<img src="./img/1-3.png" style="zoom:60%;" />

3. **罗尔定理**

	**若函数在$[a,b]$连续，开区间可微，且$f(a) = f(b)$，则存在点$\xi$，满足$f'(\xi) = 0$**

	连续推导出存在最大最小值，然后讨论相等不相等的情况即可证明

证明拉格朗日中值定理：

<img src="./img/1-4.png" style="zoom:60%;" />

对于微分中值定理只需要，取$F(x) = \int_a^xf(t)dt$，带入微分中值定理，便可导出积分中值定理，**说明微分的一条定理和公式，在积分中应有相应的定理或公式，反之亦然，对立统一**。

##### 柯西中值定理

设$f(x)$和$g(x)$都是$[a,b]$上连续，开区间可微，并且对任一点$x\in(a,b),g'(x) \ne 0$，使得：
$$
\frac{f(b)-f(a)}{g(b)-g(a)} = \frac{f'(\xi)}{g'(\xi)}
$$
<img src="./img/1-5.png" style="zoom:60%;" />

### 1.4 微积分基本定理

#### 微分形式

函数$f(t)$在区间$[a,b]$连续，x是区间内一固定点，令:
$$
\Phi(x) = \int_a^xf(t)dt(a\le x \le b)
$$
则$\Phi(x)$在区间内可微，并且
$$
\Phi '(x) = f(x) (a \le x \le b) \\
即, d\Phi(x) = f(x)dx
$$
证明如下：

<img src="./img/1-6.png" style="zoom:65%;" />

####　积分形式

设$\Phi(x)$在区间$[a,b]$可微，且$\frac{d\Phi(x)}{dx}$等于连续函数$f(x)$，那么成立着：
$$
\int_a^xf(t)dt=\Phi(x)-\Phi(a)(a\le x\le b)
$$
证明如下：

<img src="./img/1-7.png" style="zoom:65%;" />

## 第二章 微积分的运算

### 2.1 微分法

#### 微商与微分的计算

假设$u(x)，v(x)$都是可微函数，那么它们的和、差、积、商都是可微的，有以下式子成立：

1. $[u(x)\pm v(x)]' = u'(x) \pm v'(x)$

2. $[u(x)v(x)]'=u'(x)v(x)+u(x)v'(x)$

3. $[\frac{u(x)}{v(x)}]'=\frac{u'(x)v(x)-u(x)v'(x)}{[v(x)]^2}$

4. $[Cv(x)]'=Cv'(x)$

5. $y=f(u),u=\varphi(x)$，有$\frac{dy}{dx}=f'(u)\varphi'(x)$，可以由定义证明

6. 若$x=g(y)是y=f(x)的反函数，且f'(x)\neq 0$，有$g'(y) = \frac{1}{f'(x)}$

	这有一个数学上的解释：

	<img src="./img/2-1.png" style="zoom:60%;" />

常用初等函数微商表：

<img src="./img/2-2.png" style="zoom:70%;" />

其他一些必要的：

- $\ln(x+\sqrt{1+x^2})' = \frac{1}{\sqrt{1+x^2}}$

	<img src="./img/2-14.png" style="zoom:60%;" />

- <img src="./img/2-15.png" style="zoom:60%;" />

对应微商的运算法则，也有对应的微分运算法则，差不多是一致的，但是复合函数的微分有区别：

<img src="./img/2-3.png" style="zoom:65%;" />

即为**微分的形式不变性**

#### 高阶微商与高阶微分

如果函数$f'(x)$的微商存在，就把他称为函数$f(x)$的二阶微商，记作$f''(x)$或者$\frac{d^2f(x)}{dx^2}$，二阶微商的定义和微商的定义并无区别，同样的微分也有类似的定义：

<img src="./img/2-4.png" style="zoom:60%;" />

几种特别的高阶微分：

1. **三角函数**

	<img src="./img/2-5.png" style="zoom:60%;" />

2. 莱布尼兹公式（函数乘积的高阶微分）

	<img src="./img/2-6.png" style="zoom:65%;" />

**参数方程所确定**的函数的微分法：

<img src="./img/2-7.png" style="zoom:60%;" />

#### 微分的近似计算

函数$y=f(x)$的改变量$\Delta y$可以用微分$dy$来近似的表达，所以可得：
$$
f(x_0+\Delta x) \approx f(x_0)+f'(x_0)\Delta x
$$
利用这个还可以求近似方程的根

<img src="./img/2-8.png" style="zoom:60%;" />

$x_1$就是函数$y=f(x)$在点$(x_0,f(x_0)$的切线和x轴交点的坐标，所以这也叫**切线法**

### 2.2 积分法

#### 不定积分的计算

1. 换元法：对应与复合函数微分

	<img src="./img/2-9.png" style="zoom:60%;" />

	即将代求函数转换为另外一个容易求的函数

	有时候换元法可以反过来用，令$x=\varphi(t),dx=\varphi'(t)$，然后将待求函数转换为t的函数

2. 分部积分：对应微分乘法法则

	<img src="./img/2-10.png" style="zoom:60%;" />

**特别函数的不定积分**：

积分$J_n = \int\frac{dx}{(x^2+a^2)^n},a\neq0$，**主要是使用分部积分求出通项公式**

<img src="./img/2-11.png" style="zoom:60%;" />

特别的，当$n=1$时，有$J_1 = \int\frac{dx}{x^2+a^2}$，可得$J_1 = \frac{1}{a}arctan(\frac{x}{a})+C$

##### 有理函数的不定积分

将被积函数化为一个多项式和一个真分式之和，主要为求解真分式的积分：

对一般积分$\int\frac{mx+n}{x^2+px+q}dx$，可以将分母配方后，进行换元解决，有时候还可以对分母进行因式分解，然后化为多个低次项之和的形式。

##### 三角函数有理式的积分

> 三角函数以及无理数部分摘自 《四川大学高等数学第一册第四版物理类专用》

基本三角函数公式：

<img src="./img/2-16.png" style="zoom:50%;" />

万能代换：积分$\int R(\sin x,\cos x)dx$可以通过变量代换化为有理函数积分
$$
令\tan \frac{x}{2} = t,则x = 2\arctan t,dx = \frac{2dt}{1+t^2} \\
因为：\sin x = 2\sin \frac{x}{2} \cos \frac{x}{2} = \frac{2t}{1+t^2} \\
\cos x = \cos^2\frac{x}{2} - \sin ^2\frac{x}{2} = \frac{1-t^2}{1+t^2} \\
即\int R(\sin x, \cos x)dx = \int R(\frac{2t}{1+t^2},\frac{1-t^2}{1+t^2})\frac{2}{1+t^2}dt
$$
其他情况：

1. $\int R(\sin x)\cos x dx$或$\int R(\sin x,\cos^2 x)\cos x dx$ $\Rightarrow$ 做代换$\sin x = t$

2. $\int R(\cos x)\sin xdx$或$\int R(\cos x, \sin^2 x)\sin x dx$$\Rightarrow$做代换$\cos x = t$

3. $\int R(\tan x)dx$或$\int R([\sin^2 x], [\cos^2 x],[\tan x])dx \Rightarrow$做代换$\tan x = t$，

	可得：$\sin^2 x = \frac{\tan^2 x}{1+\tan^2 x} = \frac{t^2}{1+t^2}$和$\cos^2 x = \frac{1}{1+\tan^2 x} = \frac{1}{1+t^2}$

	有$x = \arctan t,dx = \frac{1}{1+t^2}dt$

##### 简单无理数的积分

以下代换称之为欧拉代换：

1. $\int R(x,\sqrt[n]{\frac{ax+b}{cx+e}})dx$令$\frac{ax+b}{cx+e} = t^n$
2. $\int R(x, \sqrt{ax^2+bx+c}dx)$
	- 如果$b^2-4ac > 0$，则可因式分解（存在两个根）可以设$\sqrt{a(x-\alpha)(x-\beta)}=t(x-\alpha)$
	- 如果$b^2-4ac < 0$，有以下两种策略
		1. $\sqrt{ax^2+bx+c} = \sqrt{a}x\pm t$
		2. $\sqrt{ax^2+bx+c} = xt \pm \sqrt{c}$
3. $\sqrt{x^2+a^2}$，令$x = a\tan t$
4. $\sqrt{x^2-a^2}$，令$x = a\sec t$
5. $\sqrt{a^2-x^2}$，令$x = a\sin t$
6. $\int \sqrt{x^2-1} dx=\frac{1}{2}(x\sqrt{x^2-1}-\ln (|x+\sqrt{x^2-1}|))$
7. $\int \frac{1}{\sqrt{x^2+1}} dx=\ln (|x+\sqrt{x^2+1}|)$

#### 定积分的计算

根据牛顿-莱布尼兹公式（微积分基本定理的积分形式）：

设$\Phi(x)$在区间$[a,b]$可微，且$\frac{d\Phi(x)}{dx}$等于连续函数$f(x)$，那么成立着：
$$
\int_a^xf(t)dt=\Phi(x)-\Phi(a)(a\le x\le b)\int_a^xf(t)dt=\Phi(x)-\Phi(a)(a\le x\le b)
$$
根据此公式，可得定积分和不定积分并无特别大的区别，只不过都加上了定限而已，**在换元的时候注意积分上下限对应的更改**

几种特别注意的例子：

1. 奇偶函数

	- 奇函数：$\int_{-l}^{l}f(x)dx = 0$
	- 偶函数：$\int_{-l}^{l}f(x)dx = 2\int_{0}^{l}f(X)dx$

2. 积分$J_m = \int_0^{\frac{\pi}{2}}\sin^m xdx和J'_m = \int_0^{\frac{\pi}{2}}\cos^m xdx$

	<img src="./img/2-12.png" style="zoom:60%;" />

	有以下结论：（双阶乘符号为不大于N且奇偶相同的乘积）

	<img src="./img/2-13.png" style="zoom:60%;" />

3. 几种三角积分的恒等式

	- $\int_0^{\frac{\pi}{2}}f(\sin x)dx = \int_0^{\frac{\pi}{2}}f(\cos x)dx$ 令 $x = \frac{\pi}{2} - t$可证
	- $\int_0^\pi xf(\sin x)dx = \frac{\pi}{2}\int_0^\pi f(\sin x)dx$令$x = \pi - t$可证

#### 定积分的近似计算

有梯形法和抛物线法两种，梯形法即为定义，而抛物线法则是取连续的三点，构造连接三点的多项式函数，用此函数替代原来的函数做积分

## 第三章 微积分的一些应用