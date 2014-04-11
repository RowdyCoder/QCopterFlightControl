﻿[QCopterFC](https://github.com/QCopter/QCopterFlightControl)
========
* Author  : [Hom](https://github.com/Hom-Wang)
* Version : v2.2 等待製作驗證...
* Update  : 2014/04/11

Description
========
QCopterFC 是一個基於 STM32F4 的飛行控制器，可以應用於固定翼、旋翼飛行器上面，用來實現濾波、平衡、控制等演算法的平台。感測器部分使用 SmartIMU，其集成微控制器 STM32F401C、9 DOF 慣性測量元件 MPU9250 以及氣壓計 MS5611，SmartIMU 提供了兩種操作模式，讀取感測器原始資料與讀取當下姿態角度，可以透過指令選擇，無線傳輸部分使用工作於 2.4GHz 頻段的無線傳輸模組 nRF24L01P，傳輸飛行器上相關資訊，同時也可以藉由該模組從外部接收飛行控制指令，另外板上還有 Micro USB 與 Micro SD，並且引出獨立的 UART、SPI、ADC、PWM、CAN，使的 QCopterFC 可以有更多的應用、擴充。

License
========
* 硬體(Hardware)採用 [CC BY-SA 3.0 TW](http://creativecommons.org/licenses/by-sa/3.0/tw/deed.zh_TW) 方式授權 
  
　　<a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/tw/"><img alt="創用 CC 授權條款" style="border-width:0" src="http://i.creativecommons.org/l/by-sa/3.0/tw/80x15.png" /></a>  
　　<span xmlns:dct="http://purl.org/dc/terms/" property="dct:title"> QCopterFlightControl </span>由<a xmlns:cc="http://creativecommons.org/ns#" href="https://plus.google.com/u/0/112822505513154783828/posts" property="cc:attributionName" rel="cc:attributionURL"> Hom </a>製作，以<a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/tw/deed.zh_TW"> 創用CC 姓名標示-相同方式分享 3.0 台灣 授權條款 </a>釋出。  

* 軟體(Software)採用 [MIT License](http://opensource.org/licenses/MIT) 方式授權  

Hardware
========
* 控制器　 : [STM32F405R](http://www.st.com/web/catalog/mmc/FM141/SC1169/SS1577/LN1035/PF252144) 64Pin 168MHz DSP FPU
* 感測器　 : [SmartIMU](https://github.com/Hom-Wang/SmartIMU) ( [STM32F401C](http://www.st.com/web/en/catalog/mmc/FM141/SC1169/SS1577/LN1810) + [MPU-9250](http://www.invensense.com/mems/gyro/mpu9250.html) + [MS5611](http://www.meas-spec.com/product/pressure/MS5611-01BA03.aspx) )
* 無線傳輸 : [nRF24L01P](http://www.nordicsemi.com/eng/Products/2.4GHz-RF/nRF24L01P) + PA + LNA
* 儲存紀錄 : Micro SD，使用 SDIO 操作
* 外接介面 : 1*UART、1*SPI ( FFCSPI )、2*ADC、1*USB ( Micro )、1*CAN、8*PWM
* PCB 尺寸 : 51.5 * 35mm ( Screws M3: 30 * 30mm )
* 設計軟體 [Altium Designer 14](http://www.altium.com/en/products/altium-designer) ( PcbLib use AD [PcbLib v0.10](https://github.com/OpenPCB/AltiumDesigner_PcbLibrary/releases/tag/v0.10) )

<img src="https://lh6.googleusercontent.com/-Fm7KUnImwko/UwPmkmbceOI/AAAAAAAAGj4/vCjmHYtTi_Q/s1200/QCopterFC_System%2520v2.2.png" />

Related Documents
========
* [Update Records - Hackpad](https://hom.hackpad.com/QCopterFC-EvK2EHj4bqH)
* [Datasheet & BOM - Google Drive](https://drive.google.com/folderview?id=0BzL2wwAot6oPS0thRUVrb0VadTQ&usp=sharing)

Software
========
* QCopterFC FlightControl
* QCopterFC FlightRecorder
* [QCopterFC ADC](https://github.com/QCopter/QCopterFlightControl/tree/master/Software/TEST_QCopterFC_ADC)
* [QCopterFC CamSPI-Master](https://github.com/QCopter/QCopterFlightControl/tree/master/Software/TEST_QCopterFC_CAMSPI_M)
* [QCopterFC CamSPI-Slave](https://github.com/QCopter/QCopterFlightControl/tree/master/Software/TEST_QCopterFC_CAMSPI_S)
* [QCopterFC FLASH](https://github.com/QCopter/QCopterFlightControl/tree/master/Software/TEST_QCopterFC_FLASH)
* [QCopterFC IMU](https://github.com/QCopter/QCopterFlightControl/tree/master/Software/TEST_QCopterFC_IMU) ( Use MPU-9150 + MS5611 )
* [QCopterFC LED](https://github.com/QCopter/QCopterFlightControl/tree/master/Software/TEST_QCopterFC_LED)
* [QCopterFC NRF](https://github.com/QCopter/QCopterFlightControl/tree/master/Software/TEST_QCopterFC_NRF) ( Use nRF24L01P )
* [QCopterFC PWM](https://github.com/QCopter/QCopterFlightControl/tree/master/Software/TEST_QCopterFC_PWM)
* [QCopterFC SDIO](https://github.com/QCopter/QCopterFlightControl/tree/master/Software/TEST_QCopterFC_SDIO) ( Use [Fatfs](http://elm-chan.org/fsw/ff/00index_e.html) 0.10 )
* [QCopterFC UART](https://github.com/QCopter/QCopterFlightControl/tree/master/Software/TEST_QCopterFC_UART)

View
========

<br />
更多圖片 [Google+ albums](https://plus.google.com/u/0/photos/+文宏王Hom/albums/5899377395636747681)

Config
========
．Vin 建議輸入 5v ~ 6v
<img src="https://lh6.googleusercontent.com/-Mm5N3Km3Rr8/UzPvcocAHnI/AAAAAAAAHIk/gn9Bi4dtfhk/s1600/QCopterFC_v2.2_Config_CHIP.png"/>
<img src="https://lh3.googleusercontent.com/-13L0NlzLRiA/UzPvdF87olI/AAAAAAAAHIo/WJWBeXCP40M/s1600/QCopterFC_v2.2_Config_PIN.png" />
<img src="https://lh3.googleusercontent.com/-oBVkDxgoOis/UzPvcoGxudI/AAAAAAAAHIc/Ho1CscRiN-k/s1600/QCopterFC_v2.2_Config_AF.png" />
<img src="https://lh6.googleusercontent.com/-J4Hzd_Yo5ms/UzPvcajRi3I/AAAAAAAAHIY/3TuR2PT7YGY/s1600/QCopterFC_v2.2_Config_DMA.png" />

*** 傳輸資料格式  
QRC_TO_QFC  
<img src="https://lh4.googleusercontent.com/-U3WhNPhTxHo/UsgUPnOV6bI/AAAAAAAAGJE/AayjWFXOgPI/s1600/QRC_TO_QFC.png" />
QFC_TO_QRC  
<img src="https://lh3.googleusercontent.com/-eIh5NvuE0aw/UrsPnzmAcZI/AAAAAAAAGDc/mu5YwwC-S1s/s1600/QFC_TO_QRC.png" />

Schematic
========
<img src="https://lh5.googleusercontent.com/-SEkE0ncr_9A/U0dqTPctvwI/AAAAAAAAHVI/mKdAyBnOoso/s1600/QCopterFC_v2.2_Sch_1.png" />
<img src="https://lh6.googleusercontent.com/-xdyTQ1MjYLE/U0dlT0cHfpI/AAAAAAAAHUk/pOKYWnrND6U/s1600/QCopterFC_v2.2_Sch_2.png" />
