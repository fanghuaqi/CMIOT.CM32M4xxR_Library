1、功能说明
	1、通过设定唤醒时间触发中断。
        2、通过唤醒标志位来配置IO输出


2、使用环境

	软件开发环境：  NucleiStudio IDE for C/C++ 2021-02
	硬件环境：      CM32M4xxR_LQFP128_STB


3、使用说明
	
	系统配置；
		1、周期性唤醒时钟源：RTCCLK（1HZ）
                2、唤醒输出口：PC13
		3、串口配置：
			- 串口为UART5（TX：PE8  RX：PE9）,可通过跳针连接U转串芯片后直接使用Micro USB与 MCU 进行串口通信
			- 数据位：8
			- 停止位：1
			- 奇偶校验：无
			- 波特率： 115200 


	使用方法：
		1、设定RTC_ALARM_TEST_TYPE = RTC_ALARM_TEST_TYPE_IRQ，编译后烧录到评估板，上电后，串口每隔5s会打印唤醒信息。
        2、设定RTC_ALARM_TEST_TYPE = RTC_ALARM_TEST_TYPE_OUTPUT，编译后烧录到评估板，上电后，PC13每隔5S翻转一次。
                


4、注意事项
	当配置PC13输出模式为开漏模式时需要外置上拉电路。