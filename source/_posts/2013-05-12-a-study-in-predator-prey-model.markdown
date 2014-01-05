---
layout: post
title: "A study in predator prey model"
date: 2013-05-12 13:28
comments: true
categories: 
---
因为毕业论文的缘故，最近在学习*predator-prey model*，算是属于**evolutionary game theory**里面的吧。记得第二学期选*Advanced Microeconomics*的时候[Fabrizio Germano](http://www.econ.upf.edu/en/people/onefaculty.php?id=p2364)在讲heuristic就在说

>some ideas are from biology  

当时觉得那个天雷滚滚，三观尽毁，现在看来，感觉是那么的合乎情理，甚至显而易见。果然是沉淀了么，偷笑一个。

其实这个模型（two species case）的基本思路非常之简单，假设生态系统中存在扑食者（predator）跟猎物（prey），他们之间遵循这个一个常微分方程（[ordinary differential equation](http://en.wikipedia.org/wiki/Ordinary_differential_equation) ）:

$$
\begin{align*}
 &\dot{X}=gX-\mu XT \\
 &\dot{T}=\delta XT-\gamma T
\end{align*}
$$ 

这其中：

<!-- more -->

X 代表猎物的数量

T 代表扑食者的数量

g 代表猎物的增长率（缺少扑食者存在的条件下）

$\mu$ 代表扑食效率

$\delta$  代表消化效率

$\gamma$ 则代表扑食者的死亡率

整个方程组的不动点（？对应的英文是rest point,就是使$\dot{X}=0$, $\dot{T}=0$的点）有两对，第一队显而易见，$X=0$,$T=0$,但这并不是所需要的（扑食者跟猎物都灭绝了，还研究个鸟啊）另外一对则是：$T=\frac{g}{\mu}$ 以及 $X=\frac{\gamma}{\delta}$. 事实上，从图形的角度来看（以X为横坐标，T为纵坐标），运动轨迹正好是一个类圆形。

{% img http://ww4.sinaimg.cn/large/4d8a2fa9gw1e4lr36ckygj20at09f3yr.jpg 轨迹图 %}

如果出发点在第三象限，此时猎物的数量在不断的增长而扑食者的数量却在下降，自然地，当到达一定程度后，扑食者开始更加有效地扑食，且扑食者的扑食习惯已经更新并将会持续保持（第四象限）直到某一点上猎物的数量开始下降（第一象限），当扑食者的过度扑食造成猎物数量下降到一定程度后，猎物数量跟扑食者的数量都将下降（第二象限）。然后继续这样循环着。

[Lotka](http://en.wikipedia.org/wiki/Alfred_J._Lotka)跟[Volterra](http://en.wikipedia.org/wiki/Vito_Volterra)第一次提出这个模型，所以也叫[L-V predator-prey model](http://en.wikipedia.org/wiki/Lotka%E2%80%93Volterra_equation)。



