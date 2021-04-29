# UmaMusume_Calculator 马娘相性计算器 v0.9.5.0

Currently only Chinese version. \(_w_)/

相性数据来源：

NGA(  https://bbs.nga.cn/read.php?tid=25778929  )；

Twitter(  https://twitter.com/gamedukedeatho  )；



数据库的项目：https://github.com/Kamijouko/UmaCalculatorAppLibrary


赛马娘相性计算器，目前仅有中文

当然也不保证准确性。写着玩的

全局权重暂时还没加，先晾着。

读取xml那些也还没，就是个摆设。

--------------------------------------------------------------------------------
--------------------------------------------------------------------------------

基础使用流程

1.在一世代模式的1号位选择需要养的马。

2.然后点补位计算。

3.根据补位结果，把二世代模式的123号位换成结果。

4.然后继续点补位计算算出4567位。

5.最后根据右下角的各种Plan选择自己有能力练的。

当然也可以反过来，根据已养成的4567位，补算最优的相性应该如何配。

--------------------------------------------------------------------------------
--------------------------------------------------------------------------------

0.9.5.0版本新增的阈值调整，是仅针对二世代 算法模式一的调整，每个阈值的详细说明将鼠标移上去后有tooltip；

![阈值](https://user-images.githubusercontent.com/59531368/116519603-a2257e80-a90c-11eb-93c5-b3e39e1c838e.png)

模式一与阈值相关算法的大致逻辑：（= =）【仅供参考】

    判断当前组合的一世代之和是否大于阈值；
    
    是： 判断当前组合的主要平均值是否在最大和最小阈值的区间之内；
          
         是： 判断当前组合的两个二世代和的和是否大于二世代和的最大和最小阈值之和；
               
              是： 判断当前组合的两个二世代和是否是一个大于最大阈值而另一个大于最小阈值；
         
                   是： 如果勾选了去除重复则判断不重复后加入候选列表；
              
                   否： 直接加入候选列表；
              
    否： 判断当前组合的主要平均值是否大于最大阈值；
     
         是： 判断当前组合的两个二世代和的和是否大于二世代和的最小阈值的两倍；
     
              是： 判断当前组合的两个二世代和是否都大于二世代和最小阈值；
          
                   是： 如果勾选了去除重复则判断不重复后加入候选列表；
              
                   否： 直接加入候选列表；

---------------------------------------------------------------------------------
---------------------------------------------------------------------------------

需要注意的有。

1.二世代补位计算的模式一推荐用在NGA的数据源。并且只建议补充4个空位以下的马娘。

2.接1，模式一也可用于其他数据源，但由于阈值可能对结果稍稍影响。

3.模式二可用于所有数据源，但只建议补充3个空位和3个空位以下的马娘。

4.左上角模式选择和数据源选择底下的是算法排列的优先度。

5.根据选择的优先属性得出的结果也不同。

6.由于并没有通过拆游戏得到真正的相性算法，本计算器算出结果仅供参考。

7.就算只补位计算4空位或3空位以下的马娘仍有可能程序未响应。所以常开任务管理器吧XD

---------------------------------------------------------------------------------
---------------------------------------------------------------------------------

下面的图是按照上面的功能说明截的，供参考。（下方图片为0.9.4.0版本截图，更新后的0.9.5.0会稍有差别）

![01](https://user-images.githubusercontent.com/59531368/112302121-0f2a7080-8cde-11eb-8998-360f13fa020a.png)
![02](https://user-images.githubusercontent.com/59531368/112302125-105b9d80-8cde-11eb-93c7-25895797508e.png)
![03](https://user-images.githubusercontent.com/59531368/112302129-118cca80-8cde-11eb-8172-0674b769932f.png)
![04](https://user-images.githubusercontent.com/59531368/112302131-12256100-8cde-11eb-8db0-7476f42e5e1c.png)
![05](https://user-images.githubusercontent.com/59531368/112302132-12bdf780-8cde-11eb-859e-fb302516a9c6.png)
![06](https://user-images.githubusercontent.com/59531368/112302134-13568e00-8cde-11eb-8afe-f1e475c57ed8.png)
![07](https://user-images.githubusercontent.com/59531368/112302136-13ef2480-8cde-11eb-935b-2189df8c2251.png)
![08](https://user-images.githubusercontent.com/59531368/112302138-1487bb00-8cde-11eb-8e5f-4ec6c5d94d34.png)
![09](https://user-images.githubusercontent.com/59531368/112302139-1487bb00-8cde-11eb-8342-bbbd3d0dfcc1.png)
![10](https://user-images.githubusercontent.com/59531368/112302140-15205180-8cde-11eb-8e7f-256c620e287a.png)


其他该注意的都写在程序里了

winform的图片是处理真的拉
