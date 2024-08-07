# 平衡小车项目分工【理想情况】



## 电赛训练时间安排

```
7月9日后，开始各自任务的基础学习【同步进行器材的整理】

7月15日左右，开始实现往年赛题【送药小车】。


```



## 四天三夜分配【7月29日8点---8月1日20点】【8月3日或4日线下作品评选】

```
硬件负责人在一天之内完成硬件工作，其余时间编写设计报告；

电控负责人与视觉负责人先尽快完成各自的基础功能实现，然后匹配通信，进行比赛功能实现。
```



### 电控

```
1、STM32HAL库  【STM32CubeMX软件使用】【熟悉各种协议，能灵活移植模块代码】

2、Freertos实时操作系统  【基于STM32CubeMX】

3、MSP432P401R系列单片机  【与STM32标准库类似】【熟悉各种协议，能灵活移植代码】
```

###### 代码封装

```
将各模块封装成API接口文件，通过宏定义或sysconfig修改gpio口进行调用
```

###### 所需模块

```
oled，mpu6050，直流减速电机、lcd、继电器、模拟电机、数字舵机、步进电机
```



### 视觉

```
1、OpenMV  【识别色块等各类物品或颜色】【与STM32通信】

2、k210  【同OpenMV】

3、树莓派  【学会基础配置】【调用OpenMV库】
```

###### 基础视觉

```
1、巡线识别（走线识）

2、色块识别（激光识别）

3、形状识别（矩形，多边形）
```



###### 神经网络

```
数字识别、物体特征识别
```



###### 通信协议

```
openmv，k210等视觉模块与MSPM0以及STM32的两方通信代码
```



### 硬件

```
1、嘉立创PCB 【设计电机驱动板、稳压模块、洞洞板焊接】

2、cad 【熟悉各类零件（尺寸，型号等）】【亚克力板雕刻】

3、soliworks 【设计舵机云台、小车支架等】【3D打印】

4、论文编写  【依靠AI形成初版，然后自行修改成逻辑分明，得分点明确的设计报告】【熟悉设计报告的格式与流程】【设计流程图】
```

##### 1、小车框架搭建

```
1、基于MSPM0G3507的两驱亚克力小车底板

2、基于MSPM0G3507的四驱亚克力小车底板

3、基于STM32F407ZGT6的两驱亚克力小车底板

4、基于STM32F407ZGT6的两驱亚克力小车底板
```



##### 2、基于MSPM0G3507的PCB小车通用板

###### 线路要求

```
1、信号线10mil

2、3V3电源线20mil

3、5V电源线25mil

4、12V电源线80mil
```

###### 可直插模块

```
k210，openmv，oled，mpu6050，3个左右舵机接口，可选择5伏电源线输入端口(跳线帽）(防止供电不足)，，oled
```

###### 引出排线

```
全部排线引出，置于PCB外围
```



##### 3、搭建激光笔放置平台

```
为激光笔搭建可固定支架
```

