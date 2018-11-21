# 用Python解决高数和线代问题
## 高数
### 求极限
原题见高数北大版
求sin(2x^2)/3x在x趋近于0时的极限
1) 首先调用函数
在命令操作行>>>输入from sympy import *
2) 然后定义x（>>>x=Symbol('x'))
3) 再进行求极限操作(如下图所示)

![](images\高数求极限.png)

得极限值为0

### 求定积分
求$$\int_0^1 {x^2} ,{\rm d}x$$

![](images\高数求定积分.png)

(*注意典型错误 from sympy import 不能缺少**)

得出结果为1/3

## 线代

线性代数需要调用另一函数库Numpy

  ">>>import numpy as np "
### 解方程组
x<sub>1</sub>+3x<sub>2</sub>-5x<sub>3</sub>=4

x<sub>1</sub>+4x<sub>2</sub>-8x<sub>3</sub>=7

-3x<sub>1</sub>-7x<sub>2</sub>+9x<sub>3</sub>=-6

具体过程如图

![](images\线代解方程组.png)


### 求逆矩阵

|1|-2|1|
|--|--|--|
|4|-7|3|
|-2|6|-4|

如图所示

![](images\线代求逆矩阵.png)

