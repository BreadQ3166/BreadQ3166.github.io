# 电子设计大赛计划书

> 起草：面包的起源

[>>操作指南](guide)



# 项目概况

#### 电子设计大赛省赛



## 成员概况

```
徐谦 2022级光电信息科学与工程

伍熠辉 2022级电子信息

霍泳贤 2022级通信工程
```



## 深圳大学往年电子设计大赛获奖情况

```
校赛：https://www1.szu.edu.cn/board/view.asp?id=496238

省赛：https://www1.szu.edu.cn/board/view.asp?id=502311
```



## 学习方向(侧重点)

```
软件与硬件都需要学：模电、数电

软件：stm32hal库、msp系列单片机、openmv或K210或树莓派、PID算法、滤波算法(基础滤波、卡尔曼滤波等)

硬件：嘉立创PCB设计、原理图绘制(抄)、焊接、亚克力板雕刻

附加：soliworks
```



### 小提示

```
不管软件硬件，上述知识尽可能都会一点，因为软硬件是互通的
```




# 基础信息与前提

1、选用STM32F103C8T6最小系统板  
2、代码基于STMCUBEMX(HAL库)编写  
3、引脚分配遵循分配表  



## 引脚分配(平衡小车参考)

| STM32引脚 | 引脚复用  | 模块引脚 |  模块名称   |
| :-------: | :-------: | :------: | :---------: |
|    PA6    |    ADC    |   ADC    | TB6612稳压  |
|    PB0    | TIM3_CH3  |   PWMB   | TB6612稳压  |
|   PB12    |   GPIO    |   BIN2   | TB6612稳压  |
|   PB13    |   GPIO    |   BIN1   | TB6612稳压  |
|    3V3    |    无     |   STBY   | TB6612稳压  |
|   PB14    |   GPIO    |   AIN1   | TB6612稳压  |
|   PB15    |   GPIO    |   AIN2   | TB6612稳压  |
|    PB1    | TIM3_CH3  |   PWMA   | TB6612稳压  |
|    PA1    | TIM2_CH2  |   E2B    | TB6612稳压  |
|    PA0    | TIM2_CH1  |   E2A    | TB6612稳压  |
|    PB7    | TIM4_CH2  |   E1B    | TB6612稳压  |
|    PB6    | TIM4_CH1  |   E1A    | TB6612稳压  |
|    PB8    |  I2C_SCL  |   SCL    | MPU6050重力 |
|    PB9    |  I2C_SDA  |   SDA    | MPU6050重力 |
|   PB10    |  I2C_SCL  |   SCL    |  OLED显示   |
|   PB11    |  I2C_SDA  |   SDA    |  OLED显示   |
|    PA9    | UART1_TXD |   RXD    | ATK-BLE蓝牙 |
|   PA10    | UART1_RXD |   TXD    | ATK-BLE蓝牙 |
|    PA2    | UART2_TXD |   RXD    |  串口助手   |
|    PA3    | UART2_RXD |   TXD    |  串口助手   |
|   PA14    |   GPIO    |   TRIG   | 超声波SR04  |
|   PA15    |   GPIO    |   ECHO   | 超声波SR04  |
|    无     |   TIM1    |    无    | 超声波SR04  |
|    PA4    |   GPIO    |    1     |    按键     |
|    PA5    |   GPIO    |    1     |    按键     |
|    PA7    |   GPIO    |    1     |    按键     |





