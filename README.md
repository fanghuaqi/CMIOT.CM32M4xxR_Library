# CMIOT.CM32M4xxR_Library
芯昇科技MCU CM32M4xxR软件开发包，包括相关驱动代码、基于CM32M4xxR_LQFP128_STB开发板和CM32M433R开发板的样例代码，芯片及软硬件技术文档。
# CM32M4xxR
CM32M4xxR是芯昇科技首颗采用32位RISC-V内核（Nuclei N308）的混合信号MCU（支持FPU和DSP指令），主频高达144MHz，Flash最大512KB。
# 目录结构说明
-   Drivers：芯片驱动，包括NMSIS、外设驱动。

-   Project: 适配CM32M4xxR_LQFP128_STB开发板和CM32M433R-START开发板的BSP、参考例程和工程模板。

-   Doc: 包括芯片芯片手册、软硬件手册、开发板原理图等技术文档。

参考例程包括如下内容：

 **样例工程**                          | **功能描述**                                                                                                                                                                                                                       |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ├─ADC                                 |                                                                                                                                                                                                                                    |
| │ ├─4ADCs_DMA                         | [4通道通过DMA、连续转换、软件触发示例](Projects/CM32M4xxR_LQFP128_STB/Examples/ADC/4ADCs_DMA)                                                                                 |
| │ ├─ADC1_DMA                          | [1通道通过DMA、连续转换、扫描模式、软件触发示例](Projects/CM32M4xxR_LQFP128_STB/Examples/ADC/ADC_SingleRead)                                                                  |
| │ ├─ADC1_TEMP                         | [ADC1采样内部温度传感器的电压并算出温度值](Projects/CM32M4xxR_LQFP128_STB/Examples/ADC/ADC1_DMA)                                                                              |
| │ ├─ADC_SingleRead                    | [4通道通过软件触发转换示例](Projects/CM32M4xxR_LQFP128_STB/Examples/ADC/ADC1_TEMP)                                                                                            |
| │ ├─AnalogWatchdog                    | [模拟看门狗功能示例](Projects/CM32M4xxR_LQFP128_STB/Examples/ADC/AnalogWatchdog)                                                                                              |
| │ ├─ExtLinesTrigger                   | [ADC1通过DMA、扫描模式、外部触发示例](Projects/CM32M4xxR_LQFP128_STB/Examples/ADC/ExtLinesTrigger)                                                                            |
| │ ├─RegSimul_DualMode                 | [ADC1、2同步规则通道模式、连续扫描模式、软件触发示例](Projects/CM32M4xxR_LQFP128_STB/Examples/ADC/RegSimul_DualMode)                                                          |
| │ └─TIMTrigger_AutoInjection          | [ADC1规则转换通道开启、TIM1 CC2触发自动注入转换示例](Projects/CM32M4xxR_LQFP128_STB/Examples/ADC/TIMTrigger_AutoInjection)                                                    |
| ├─ALGO                                |                                                                                                                                                                                                                                    |
| │ ├─AES                               | [AES ECB/CBC/CTR模式加解密运算示例](Projects/CM32M4xxR_LQFP128_STB/Examples/ALGO/AES)                                                                                         |
| │ ├─DES                               | [DES/3DES ECB/CBC模式运算示例](Projects/CM32M4xxR_LQFP128_STB/Examples/ALGO/DES)                                                                                              |
| │ └─HASH                              | [MD5/SHA1/SHA224/SHA256运算示例](Projects/CM32M4xxR_LQFP128_STB/Examples/ALGO/HASH)                                                                                           |
| ├─BKP                                 |                                                                                                                                                                                                                                    |
| │ ├─BkpData                           | [对备份寄存器进行写入操作](Projects/CM32M4xxR_LQFP128_STB/Examples/BKP/BkpData)                                                                                               |
| │ └─TamperTest                        | [入侵检测自毁](Projects/CM32M4xxR_LQFP128_STB/Examples/BKP/TamperTest)                                                                                                        |
| ├─bxCAN                               |                                                                                                                                                                                                                                    |
| │ ├─Dual_CAN1_2                       | [CAN两个通道互相收发报文](Projects/CM32M4xxR_LQFP128_STB/Examples/bxCAN/Dual_CAN1_2)                                                                                          |
| │ └─LoopBack_CAN1                     | [单通道环回模式下收发报文](Projects/CM32M4xxR_LQFP128_STB/Examples/bxCAN/LoopBack_CAN1)                                                                                       |
| ├─COMP                                |                                                                                                                                                                                                                                    |
| │ ├─CompBreak                         | [比较器输出改变后触发tim刹车](Projects/CM32M4xxR_LQFP128_STB/Examples/COMP/CompBreak)                                                                                         |
| │ └─CompOut                           | [输入触发比较器输出改变](Projects/CM32M4xxR_LQFP128_STB/Examples/COMP/CompOut)                                                                                                |
| ├─CRC                                 |                                                                                                                                                                                                                                    |
| │ └─CalCRC                            | [硬件CRC的基本功能和算法](Projects/CM32M4xxR_LQFP128_STB/Examples/CRC/CalCRC)                                                                                                 |
| ├─DAC                                 |                                                                                                                                                                                                                                    |
| │ ├─DoubleModeDMASineWave             | [同时触发模式下DMA双通道输出正弦波示例](Projects/CM32M4xxR_LQFP128_STB/Examples/DAC/DoubleModeDMASineWave)                                                                                   |
| │ ├─OneChannelOutputNoiseWave         | [单通道输出噪音信号示例](Projects/CM32M4xxR_LQFP128_STB/Examples/DAC/OneChannelOutputNoiseWave)                                                                               |
| │ └─TwoChannelsTriangleWave           | [双通道输出三角波示例](Projects/CM32M4xxR_LQFP128_STB/Examples/DAC/TwoChannelsTriangleWave)                                                                                   |
| ├─DMA                                 |                                                                                                                                                                                                                                    |
| │ ├─FLASH_RAM                         | [使用DMA在FLASH与RAM之间传输数据](Projects/CM32M4xxR_LQFP128_STB/Examples/DMA/FLASH_RAM)                                                                                      |
| │ ├─I2C_RAM                           | [使用DMA在I2C外设与RAM之间传输数据](Projects/CM32M4xxR_LQFP128_STB/Examples/DMA/I2C_RAM)                                                                                      |
| │ └─SPI_RAM                           | [使用DMA在SPI外设与RAM之间传输数据](Projects/CM32M4xxR_LQFP128_STB/Examples/DMA/SPI_RAM)                                                                                      |
| ├─EXTI                                |                                                                                                                                                                                                                                    |
| │ └─KeyInterrupt                      | [按键触发外部中断](Projects/CM32M4xxR_LQFP128_STB/Examples/EXTI/KeyInterrupt)                                                                                                 |
| ├─Flash                               |                                                                                                                                                                                                                                    |
| │ ├─Flash_DMA_Program                 | [使用DMA将SRAM数据写入FLASH](Projects/CM32M4xxR_LQFP128_STB/Examples/Flash/Flash_DMA_Program)                                                                                 |
| │ ├─Flash_Program                     | [对FLASH进行读写操作](Projects/CM32M4xxR_LQFP128_STB/Examples/Flash/Flash_Program)                                                                                            |
| │ └─Flash_Write_Protection            | [FLASH写保护](Projects/CM32M4xxR_LQFP128_STB/Examples/Flash/Flash_Write_Protection)                                                                                           |
| ├─GPIO                                |                                                                                                                                                                                                                                    |
| │ ├─IORemap                           | [将JTAG口重定向为普通IO](Projects/CM32M4xxR_LQFP128_STB/Examples/GPIO/IORemap)                                                                                                |
| │ └─LedBlink                          | [通过GPIOK控制LED](Projects/CM32M4xxR_LQFP128_STB/Examples/GPIO/LedBlink)                                                                                                     |
| ├─I2C                                 |                                                                                                                                                                                                                                    |
| │ ├─EEPROM                            | [I2C EEPROM读写（AT24C02）](Projects/CM32M4xxR_LQFP128_STB/Examples/I2C/EEPROM)                                                                                               |
| │ ├─I2C_10bit                         | [I2C 10bit地址通信](Projects/CM32M4xxR_LQFP128_STB/Examples/I2C/I2C_10bit)                                                                                                    |
| │ ├─I2C_Master                        | [I2C 主机通信（查询方式）](Projects/CM32M4xxR_LQFP128_STB/Examples/I2C/I2C_Master)                                                                                            |
| │ ├─I2C_Master_Int                    | [I2C 主机通信（中断方式）](Projects/CM32M4xxR_LQFP128_STB/Examples/I2C/I2C_Master_Int)                                                                                        |
| │ ├─I2C_Master_Slave_Int              | [I2C 主从通信（中断方式）](Projects/CM32M4xxR_LQFP128_STB/Examples/I2C/I2C_Master_Slave_Int)                                                                                  |
| │ ├─I2C_Slave                         | [I2C 从机通信（查询方式）](Projects/CM32M4xxR_LQFP128_STB/Examples/I2C/I2C_Slave)                                                                                             |
| │ └─I2C_Slave_Int                     | [I2C 从机通信（中断方式）](Projects/CM32M4xxR_LQFP128_STB/Examples/I2C/I2C_Slave_Int)                                                                                         |
| ├─I2S                                 |                                                                                                                                                                                                                                    |
| │ ├─I2S_DMA                           | [I2S 通过 DMA 收发数据](Projects/CM32M4xxR_LQFP128_STB/Examples/I2S/I2S_DMA)                                                                                                  |
| │ ├─I2S_Interrupt                     | [I2S 通过中断收发数据](Projects/CM32M4xxR_LQFP128_STB/Examples/I2S/I2S_Interrupt)                                                                                             |
| │ └─SPI_I2S_Switch                    | [I2S 和 SPI 收发数据切换示例](Projects/CM32M4xxR_LQFP128_STB/Examples/I2S/SPI_I2S_Switch)                                                                                     |
| ├─iCache                              |                                                                                                                                                                                                                                    |
| │ └─CoreMark                          | [MCU跑分测试](Projects/CM32M4xxR_LQFP128_STB/Examples/iCache/CoreMark)                                                                                                        |
| ├─IWDG                                |                                                                                                                                                                                                                                    |
| │ └─IWDG_Reset                        | [IWDG复位功能](Projects/CM32M4xxR_LQFP128_STB/Examples/IWDG/IWDG_Reset)                                                                                                       |
| ├─OPA                                 |                                                                                                                                                                                                                                    |
| │ ├─OpaAdByTim                        | [TIM触发ADC同步注入采样OPA电压数据，并且TIM输出受COMP刹车控制，刹车发生后TIM停止pwm输出，ADC的注入采样停止。](Projects/CM32M4xxR_LQFP128_STB/Examples/OPA/OpaAdByTim)         |
| │ └─PGA                               | [PGA模式，放大输入电压2倍](Projects/CM32M4xxR_LQFP128_STB/Examples/OPA/PGA)                                                                                                   |
| ├─PWR                                 |                                                                                                                                                                                                                                    |
| │ ├─AlarmWakeUp                       | [通过RTC闹钟来唤醒STOP2](Projects/CM32M4xxR_LQFP128_STB/Examples/PWR/AlarmWakeUp)                                                                                             |
| │ ├─PVD                               | [PVD配置电压产生对应的中断](Projects/CM32M4xxR_LQFP128_STB/Examples/PWR/PVD)                                                                                                  |
| │ ├─SLEEP                             | [SLEEP模式的进入和退出。](Projects/CM32M4xxR_LQFP128_STB/Examples/PWR/SLEEP)                                                                                                  |
| │ ├─STANDBY                           | [STANDBY模式的进入和退出。](Projects/CM32M4xxR_LQFP128_STB/Examples/PWR/STANDBY)                                                                                              |
| │ └─STOP                              | [STOP2模式的进入和退出。](Projects/CM32M4xxR_LQFP128_STB/Examples/PWR/STOP)                                                                                                   |
| ├─QSPI                                |                                                                                                                                                                                                                                    |
| │ ├─QSPI_DMA                          | [通过QSPI接口操作板上的串行Flash（GD25Q40C）芯片，分别使用双线和四线模式在DMA方式下对Flash进行读写。](Projects/CM32M4xxR_LQFP128_STB/Examples/QSPI/QSPI_DMA)                  |
| │ ├─QSPI_QUAD                         | [通过QSPI接口操作板上的串行Flash（GD25Q40C）芯片，分别使用双线和四线模式对Flash进行读写。](Projects/CM32M4xxR_LQFP128_STB/Examples/QSPI/QSPI_QUAD)                            |
| │ └─QSPI_XIP                          | [通过QSPI接口操作板上的串行Flash（GD25Q40C）芯片，在四线XIP模式对Flash进行读取，在XIP操作前通过普通四线模式写入数据。](Projects/CM32M4xxR_LQFP128_STB/Examples/QSPI/QSPI_XIP) |
| ├─RCC                                 |                                                                                                                                                                                                                                    |
| │ └─RCC_ClockConfig                   | [设置不同的系统时钟](Projects/CM32M4xxR_LQFP128_STB/Examples/RCC/RCC_ClockConfig)                                                                                             |
| ├─RISC-V                              |                                                                                                                                                                                                                                    |
| │ ├─DSP                               | [FPU/DSP应用样例](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/DSP)                                                                                                         |
| │ │ ├─riscv_bayes_example             | [示例演示如何使用贝叶斯分类器](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/DSP/riscv_bayes_example)                                                                        |
| │ │ ├─riscv_class_marks_example       | [示例演示如何统计及矩阵计算](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/DSP/riscv_class_marks_example)                                                                    |
| │ │ ├─riscv_convolution_example       | [示例演示如何实现数据的卷积](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/DSP/riscv_convolution_example)                                                                    |
| │ │ ├─riscv_dotproduct_example        | [示例演示如何使用乘法和加法函数实现向量的点积。](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/DSP/riscv_dotproduct_example)                                                 |
| │ │ ├─riscv_fft_bin_example           | [示例演示如何计算输入信号的快速傅里叶变换](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/DSP/riscv_fft_bin_example)                                                          |
| │ │ ├─riscv_fir_example               | [示例演示了如何配置FIR低通滤波器](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/DSP/riscv_fir_example)                                                                       |
| │ │ ├─riscv_graphic_equalizer_example | [示例演示如何使用Biquad滤波器构建5波段图形均衡器](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/DSP/riscv_graphic_equalizer_example)                                         |
| │ │ ├─riscv_linear_interp_example     | [示例演示利用线性插值模块实现提升数据精度。](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/DSP/riscv_linear_interp_example)                                                  |
| │ │ ├─riscv_matrix_example            | [示例演示如何使用矩阵计算接口](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/DSP/riscv_matrix_example)                                                                       |
| │ │ ├─riscv_signal_converge_example   | [本示例将展示自适应滤波器的收敛](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/DSP/riscv_signal_converge_example)                                                            |
| │ │ ├─riscv_sin_cos_example           | [示例演示如何使用正弦与余弦计算](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/DSP/riscv_sin_cos_example)                                                                    |
| │ │ ├─riscv_svm_example               | [示例演示如何使用机器学习中的支持向量机计算](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/DSP/riscv_svm_example)                                                            |
| │ │ └─riscv_variance_example          | [本示例将采用基础的数学算子展示方差运算的基本操作](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/DSP/riscv_variance_example)                                                 |
| │ ├─Exception                         | [示例展示如何使用RISC-V的异常处理](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/Exception)                                                                                  |
| │ ├─IAP                               | [示例展示如何使用XMODEM协议实现在线应用编程](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/IAP)                                                                              |
| │ │ ├─IAP_Boot                        | [IAP的bootloader实现，实现XMODEM接收数据及应用跳转](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/IAP/IAP_Boot)                                                              |
| │ │ └─IAP_User                        | [IAP跳转示例的应用代码](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/IAP/IAP_User)                                                                                          |
| │ ├─Interrupt_Nesting                 | [示例展示ECLIC中断嵌套处理函数的编写](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/Interrupt_Nesting)                                                                       |
| │ ├─Interrupt_TailChaining            | [示例展示ECLIC中断咬尾特性](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/Interrupt_TailChaining)                                                                            |
| │ ├─Interrupt_Vector_NonVector        | [示例展示ECLIC中向量中断与非向量中断的配置及响应处理](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/Interrupt_Vector_NonVector)                                              |
| │ ├─ISA                               | [示例展示获取当前内核ISA架构](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/ISA)                                                                                             |
| │ ├─PMP                               | [示例展示PMP内存保护单元配置](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/PMP)                                                                                             |
| │ ├─PMP_Privacy_Protection            | [示例展示如何使用PMP保护敏感代码](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/PMP_Privacy_Protection)                                                                      |
| │ ├─PMP_RTOS_StackOverflow            | [示例展示如何使用PMP实现RTOS的堆栈溢出保护](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/PMP_RTOS_StackOverflow)                                                            |
| │ ├─Systick                           | [示例展示如何使用系统定时器](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/Systick)                                                                                          |
| │ └─UserMode                          | [示例展示如何进入用户模式](Projects/CM32M4xxR_LQFP128_STB/Examples/RISC-V/UserMode)                                                                                           |
| ├─RNGC                                |                                                                                                                                                                                                                                    |
| │ └─GetRand                           | [获取真随机数](Projects/CM32M4xxR_LQFP128_STB/Examples/RNGC/GetRand)                                                                                                          |
| ├─RTC                                 |                                                                                                                                                                                                                                    |
| │ ├─Alarm                             | [通过设定闹钟时间来触发闹钟中断，通过闹钟标志位来配置IO输出](Projects/CM32M4xxR_LQFP128_STB/Examples/RTC/Alarm)                                                               |
| │ ├─Calendar                          | [通过EXTI线来触发日历打印输出](Projects/CM32M4xxR_LQFP128_STB/Examples/RTC/Calendar)                                                                                          |
| │ ├─RtcAutoWakeUp                     | [通过设定唤醒时间触发中断，通过唤醒标志位来配置IO输出](Projects/CM32M4xxR_LQFP128_STB/Examples/RTC/RtcAutoWakeUp)                                                             |
| │ └─TimeStamp                         | [通过EXTI线来触发时间戳。](Projects/CM32M4xxR_LQFP128_STB/Examples/RTC/TimeStamp)                                                                                             |
| ├─SPI                                 |                                                                                                                                                                                                                                    |
| │ ├─CRC                               | [SPI 发送接收数据进行 CRC 校验](Projects/CM32M4xxR_LQFP128_STB/Examples/SPI/CRC)                                                                                              |
| │ ├─CRC_Remap                         | [SPI 重映射后发送接收数据进行 CRC 校验](Projects/CM32M4xxR_LQFP128_STB/Examples/SPI/CRC_Remap)                                                                                |
| │ ├─FullDuplex_SoftNSS                | [SPI 全双工软件 NSS 模式发送接收数据](Projects/CM32M4xxR_LQFP128_STB/Examples/SPI/FullDuplex_SoftNSS)                                                                         |
| │ ├─Simplex_Interrupt                 | [SPI 单线中断发送和接收数据](Projects/CM32M4xxR_LQFP128_STB/Examples/SPI/Simplex_Interrupt)                                                                                   |
| │ ├─SPI_DMA                           | [SPI DMA 单线接收数据](Projects/CM32M4xxR_LQFP128_STB/Examples/SPI/SPI_DMA)                                                                                                   |
| │ ├─SPI_DMA_TxRx                      | [SPI DMA 单线发送和单线接收数据](Projects/CM32M4xxR_LQFP128_STB/Examples/SPI/SPI_DMA_TxRx)                                                                                    |
| │ └─SPI_FLASH                         | [SPI 读、写、擦除 W25Q128](Projects/CM32M4xxR_LQFP128_STB/Examples/SPI/SPI_FLASH)                                                                                             |
| ├─TIM                                 |                                                                                                                                                                                                                                    |
| │ ├─6Steps                            | [6步PWM输出](Projects/CM32M4xxR_LQFP128_STB/Examples/TIM/6Steps)                                                                                                              |
| │ ├─7PWM_Output                       | [7路PWM输出（6路两两互补）](Projects/CM32M4xxR_LQFP128_STB/Examples/TIM/7PWM_Output)                                                                                          |
| │ ├─Cascade_Synchro                   | [多TIMER串行周期门控](Projects/CM32M4xxR_LQFP128_STB/Examples/TIM/Cascade_Synchro)                                                                                            |
| │ ├─ComplementarySignals              | [六路PWM互补输出](Projects/CM32M4xxR_LQFP128_STB/Examples/TIM/ComplementarySignals)                                                                                           |
| │ ├─DMA                               | [两路互补输出通过DMA改变占空比](Projects/CM32M4xxR_LQFP128_STB/Examples/TIM/DMA)                                                                                              |
| │ ├─DMABurst                          | [PWM输出并通过DMA同时改变周期和占空比](Projects/CM32M4xxR_LQFP128_STB/Examples/TIM/DMABurst)                                                                                  |
| │ ├─ExtTrigger_Synchro                | [外部触发多个串行TIMER同步计数](Projects/CM32M4xxR_LQFP128_STB/Examples/TIM/ExtTrigger_Synchro)                                                                               |
| │ ├─InputCapture                      | [通过输入捕获功能计算外部信号的频率值](Projects/CM32M4xxR_LQFP128_STB/Examples/TIM/InputCapture)                                                                              |
| │ ├─OCActive                          | [比较输出-计数达到比较值后输出有效电平](Projects/CM32M4xxR_LQFP128_STB/Examples/TIM/OCActive)                                                                                 |
| │ ├─OCInactive                        | [比较输出-计数达到比较值后输出无效电平](Projects/CM32M4xxR_LQFP128_STB/Examples/TIM/OCInactive)                                                                               |
| │ ├─OCToggle                          | [比较输出-计数达到比较值后翻转输出电平](Projects/CM32M4xxR_LQFP128_STB/Examples/TIM/OCToggle)                                                                                 |
| │ ├─OnePulse                          | [外部触发TIMER输出一个单脉冲](Projects/CM32M4xxR_LQFP128_STB/Examples/TIM/OnePulse)                                                                                           |
| │ ├─Parallel_Synchro                  | [多TIMER并行周期门控](Projects/CM32M4xxR_LQFP128_STB/Examples/TIM/Parallel_Synchro)                                                                                           |
| │ ├─PWM_Input                         | [输入捕获PWM波形并计算频率和占空比](Projects/CM32M4xxR_LQFP128_STB/Examples/TIM/PWM_Input)                                                                                    |
| │ ├─PWM_Output                        | [多路输出PWM，频率相同占空比不同](Projects/CM32M4xxR_LQFP128_STB/Examples/TIM/PWM_Output)                                                                                     |
| │ ├─TIM1_Synchro                      | [TIMER1的周期门控其他TIMER并进行PWM输出](Projects/CM32M4xxR_LQFP128_STB/Examples/TIM/TIM1_Synchro)                                                                            |
| │ ├─TimeBase                          | [利用比较中断控制IO输出](Projects/CM32M4xxR_LQFP128_STB/Examples/TIM/TimeBase)                                                                                                |
| │ ├─TimeBase1                         | [利用更新中断控制IO输出（TIMER1）](Projects/CM32M4xxR_LQFP128_STB/Examples/TIM/TimeBase1)                                                                                     |
| │ ├─TimeBase2                         | [利用更新中断控制IO输出（TIMER2）](Projects/CM32M4xxR_LQFP128_STB/Examples/TIM/TimeBase2)                                                                                     |
| │ └─TimeBase6                         | [利用更新中断控制IO输出（TIMER6）](Projects/CM32M4xxR_LQFP128_STB/Examples/TIM/TimeBase6)                                                                                     |
| ├─TSC                                 |                                                                                                                                                                                                                                    |
| │ ├─TSC_HW Mode wake up               | [TSC按键触发从多种低功耗模式下唤醒（硬件扫描）](Projects/CM32M4xxR_LQFP128_STB/Examples/TSC/TSC_HW%20Mode%20wake%20up)                                                        |
| │ └─TSC_SW Mode                       | [TSC按键检测（软件扫描+TIMER检测）](Projects/CM32M4xxR_LQFP128_STB/Examples/TSC/TSC_SW%20Mode)                                                                                |
| ├─USART                               |                                                                                                                                                                                                                                    |
| │ ├─DMA_Interrupt                     | [示例展示两个USART间通过DMA和中断实现基础通信](Projects/CM32M4xxR_LQFP128_STB/Examples/USART/DMA_Interrupt)                                                                   |
| │ ├─DMA_Polling                       | [示例展示两个USART间通过DMA和查询检测标识实现基础通信](Projects/CM32M4xxR_LQFP128_STB/Examples/USART/DMA_Polling)                                                             |
| │ ├─HalfDuplex                        | [示例展示两个USART间通过查询检测标识，实现半双工模式的基础通信](Projects/CM32M4xxR_LQFP128_STB/Examples/USART/HalfDuplex)                                                     |
| │ ├─HardwareFlowCtrl                  | [示例展示两个USART间使用硬件流控制实现的基础通信](Projects/CM32M4xxR_LQFP128_STB/Examples/USART/HardwareFlowCtrl)                                                             |
| │ │ ├─Receive_RTS                     | [流控制示例的接收端](Projects/CM32M4xxR_LQFP128_STB/Examples/USART/HardwareFlowCtrl/Receive_RTS)                                                                              |
| │ │ └─Transmit_CTS                    | [流控制示例的发送端](Projects/CM32M4xxR_LQFP128_STB/Examples/USART/HardwareFlowCtrl/Transmit_CTS)                                                                             |
| │ ├─Interrupt                         | [示例展示两个USART间通过中断实现的基础通信](Projects/CM32M4xxR_LQFP128_STB/Examples/USART/Interrupt)                                                                          |
| │ ├─IrDA_TxRx                         | [示例展示两个USART间实现串行IrDA红外解码功能的基础通信](Projects/CM32M4xxR_LQFP128_STB/Examples/USART/IrDA_TxRx)                                                              |
| │ ├─MultiProcessor                    | [示例展示如何使用USART多处理器模式](Projects/CM32M4xxR_LQFP128_STB/Examples/USART/MultiProcessor)                                                                             |
| │ ├─Polling                           | [示例展示两个USART间通过查询检测标识实现的基础通信](Projects/CM32M4xxR_LQFP128_STB/Examples/USART/Polling)                                                                    |
| │ ├─Printf                            | [示例展示USART与PC间通过查询检测标识实现的基础通信及printf重定向](Projects/CM32M4xxR_LQFP128_STB/Examples/USART/Printf)                                                       |
| │ └─Synchronous                       | [示例展示USART同步模式下与SPI间通过查询检测标识实现的基础通信](Projects/CM32M4xxR_LQFP128_STB/Examples/USART/Synchronous)                                                     |
| └─WWDG                                |                                                                                                                                                                                                                                    |
|   └─WWDG_Reset                        | [WWDG复位功能](Projects/CM32M4xxR_LQFP128_STB/Examples/WWDG/WWDG_Reset)                                                                                                       |

# 如何使用
请参考https://github.com/Nuclei-Software/nuclei-sdk/wiki/Nuclei-Studio-NPK-Introduction
# 芯昇科技有限公司
芯昇科技有限公司注册成立于2020年12月29日，是中移物联网有限公司出资成立的子公司。按照中国移动通信集团“科改示范行动”整体改革布局，芯昇科技围绕物联网芯片国产化，以促进国家集成电路产业振兴为目标，以“创芯驱动万物互联，加速社会数智化转型”为使命，致力于成为“最具创新力的物联网芯片及应用领航者”。
