## 自上而下逐步求精
    A top-down approach (also known as stepwise design and in some cases used as a synonym of decomposition) is essentially the breaking down of a system to gain insight into its compositional sub-systems in a reverse engineering fashion.
    自上而下的方法（也称为逐步设计，在某些情况下用作分解的同义词）实质上是系统分解，以逆向工程的方式深入了解其组成子系统。
    (来自维基百科)

简单来说，自上而下逐步求精的方法就是将一个庞大棘手的程序逐步拆解成一个个小模块，然后一步步完成。
这要求我们对问题的本质理解透彻，然后将小模块逐步细化，使整个系统便于理解掌握。
显而易见，这个方法的核心在于“拆分”。
下面，我们以洗衣机的运作为例来进行一次应用。
## 洗衣机的运作示例
![](images\洗衣机.png)

同学们对洗衣机的操作步骤应该是很熟悉了，那么洗衣机具体是怎么运作的呢？
让我们用Top-down方法来解释一下吧。
### 伪代码分解“正常洗衣”
选择模式、水位、启动洗衣机>>注水>>浸泡>>洗涤>>漂洗>>脱水>>停止运转
### 基本操作、控制语句描述

READ 选择模式、水位

注水：
----
turn on the water_in_switch 

   set the 水位 

   while(水量<水位)

    keep the water_in_switch open 

   while(水量 >水位) 

    stop input water 

浸泡：
----
set the 浸泡时间 

   for(set the left time is zero ;the left time is less than the setting time; increase the left time) 

    keep the clothes soaping 

   if(the left time is equal to the setting time) 
    begin to wash 


洗涤和漂洗
----
set the 洗涤次数 to 3 

   set the 洗涤时间 to 20 

   for(set a to zero; a is less than setting times; add 1 to a;) 

if(洗涤次数不是第一次) 

注水

   注入新的清水

 do 

电机运转洗涤

while(经过的时间少于洗涤时间) 

注水 

脱水
-----
set 电机运转频率 

   set 电机运转时间 

   while 经过的时间<电机运转时间

  使电机继续以设定频率运转

 END