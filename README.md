﻿


# zigbee-time

## 总体进度安排

| 时间                 | 任务                                   | 完成度 |
| :-------------       |:-------------                          |:-----  |
| 2016/11-2016-12      | zibee路由协议的论文查看和算法成果研究  | 作废    |
| -                    | 门锁程序和基站程序的设计(前期先进行实验数据的获取,不实现应用部分)   |   80%  |
| -                    | express和tcp编写                    |    80%  |
| 2016/12-2017/01      | 设计zigbee路由算法  | 作废    |
| -                    | 实现门锁离线程序,基站和pc通信程序   |  100%  |
| -                    | 实现总通信协议                      |    10%  |
| 2016/01-2017/03      | 实现总体设计  | 70%     |
| -                    | 编写论文  |   30%  |

## 日进度

| 时间          | 类型           | 进度    |
|:------------- |:-------------  |:-----   |
| 2016/10/31    | zigbee-http    | socket.io成功 |
| 2016/11/01    | zigbee-http    | 添加mongodb配置 |
| 2016/11/02    | zigbee-http    | 添加redis配置 |
| 2016/11/03    | zigbee-http    | 添加登录功能 |
| 2016/11/04    | zigbee-tcp     | 添加进程和错误日志,开启多进程,添加守护进程,添加tcp服务 |
| 2016/11/05    | zigbee-tcp     | 添加tcp服务日志,模拟socket连接成功 |
| 2016/11/06    | zigbee-tcp     | socket连接状态通过redis发布成功 |
|               | zigbee-http    | 成功订阅tcp服务的socket连接状态  |
| 2016/11/07    | zigbee-http    | redis订阅数据成功通过socket.io发送至浏览器 |
|               | zigbee-tcp     | 增加基站数据字段,至此,tcp -> redis -> http -> browser路线走通  |
| 2016/11/08    | zigbee-http    | 添加图表曲线插件,引入angular |
|               | zigbee-tcp     | 连接真实设备两台成功  |
| 2016/11/09    | zigbee-http    | zigbee路由协议研究,决定使用RSSI作为路由算法的主参数 |
| 2016/11/10    | zigbee-lock    | IAR环境的配置,zigbee嗅探器工具的使用 |
| 2016/11/11    | zigbee-lock    | sysclk,led,pcf8563等驱动层和外设层的程序编写和测试,使用PM2休眠一秒钟并唤醒,增加射频模块 |
| 2016/11/17    | zigbee-lock    | ad检测和定时器模块和测试，他人论文的查看，研究了Leach路由算法，但是并不是zigbee协议的路由，重新考虑论文的侧重点 |   
| 2016/11/22    | zigbee-lock    | zigbee方面的论文查看，zigbee协议栈的研究，论文侧重点定论为z-stack协议栈的研究以及RFID读卡器的研究，低功耗仍然作为侧重点，加入zigbee安全机制说明，z-stack协议栈的研究，准备从门锁开始传输电池电量数据构建一整套回路，准备开始写论文框架 |   
| 2016/11/23    | 论文    	 | 编写论文，写出第一章绪论第一小节研究背景和意义。研究了z-stack协议栈通信的点播，组播和广播，仍然有很多不清楚的地方需要深入研究。 |  
| 2016/11/24    | 论文   	 | 编写论文，写出第一章绪论第二小节国内外研究现状，参考了大量的国外文献。|  
| 2016/11/25    | 论文   	 | 编写论文，写出第二章绪论第一二三小节，参考了大量的国外文献。|  
| 2016/11/28    | 论文    	 | 编写论文，写出第三章一二小节。测试了系统移动式设备如手机的访问可行性。|  
| 2016/11/29    | 论文    	 | 编写论文，写出第三章三小节第一小点。|  
| 2016/12/01    | 论文    	 | 编写论文，写出第三章三小节第二三小点以及第四小节，调整章节顺序。|  
| 2016/12/02    | 论文    	 | 编写论文，调整第二章的章节，新增2.4小节，编写2.4小节的一二两小点。|  
| 2016/12/03    | 论文    	 | 编写论文，编写2.4小节第三小节。|  
| 2016/12/05    | 论文    	 | 编写论文，编写2.4小节第4,5小节，新增安全服务第6小节，感觉论文写的有点糅杂，顺便参考论文的质量也参差不齐，论文的口语化偏重，仍然需要大量的查阅别人的论文，之后需要标记写的好的章节以及需要重新修改较多的章节。之前的论文框架写完第二次修改重新审阅。|  
| 2016/12/06    | 论文    	 | 第二章和第三章写完，重新安排时间规划，白天编写门锁和基站以及上位机的通信程序，晚上撰写论文。| 
| 2016/12/07    | zigbee-tcp/http| windows环境运行修复，准备使用z-stack上传数据，建立tcp服务器和客户端的通信机制。| 
| 2016/12/08    | zigbee-ztack	 | Z-Stack协议栈的深入研究，包括函数的作用和数据的传输。| 
| 2016/12/09    | zigbee-ztack   | Z-Stack协议栈的深入研究，包括函数的作用和数据的传输，基本了解的应用层协议的机制，接下来可能会分析如何新建Z-Stack的工程和应用。| 
|               | zigbee-docs    | 编写了PPT,对阶段性工作了做了一个小结，同时整理了一份Z-Stack的分析笔记。| 
| 2016/12/13    | zigbee-ztack   | Z-Stack工程的建立，加入了基站和门锁的应用层程序。 | 
| 2016/12/14    | zigbee-ztack   | 门锁低功耗模式，设计为PM2功耗模式,采用休眠-唤醒-休眠的工作模式。每1s向基站发送data request，获取基站的命令数据。 | 
|               | zigbee-docs    | Z-stack笔记中加入理论书籍中的理论知识点。 | 
|               | 论文           | 根据Z-Stack的协议栈，重新修改了前三章的部分理论知识点，规划第四章基站和门锁的硬件设计。 | 
| 2016/12/15    | zigbee-ztack   | 设置门锁离线定时程序，每隔1s启动离线程序，修改了LED底层驱动，目前只是实现了LED 1s闪烁，后期需要加入RFID读卡程序。 | 
|               | zigbee-docs    | Z-stack笔记中加入理论书籍中的理论知识点。 | 
|               | 论文           | 根据Z-Stack的协议栈，重新修改了前三章的部分理论知识点和结构图，规划第四章基站和门锁的硬件设计。 | 
| 2016/12/16    | zigbee-ztack   | 修改底层按键硬件驱动，测试了按键的轮询扫描模式和中断触发模式成功。 | 
|               | zigbee-docs    | Z-stack笔记中加入理论书籍中的理论知识点，底层硬件硬件按键驱动的修改以及事件触发的流程机制研究。 | 
| 2016/12/17    | zigbee-ztack   | 添加了延时函数和蜂鸣器应用。 |   
| 2016/12/18    | zigbee-ztack   | 添加了i2c驱动程序，添加了电机端口驱动程序，添加了电机设备程序，添加了EEPROM存储和读取程序，可以做到开门电机正反转和蜂鸣器LED提示音效果，配置了锁扣的中断触发初始化程序，可以做到检测开门动作并及时关门处理。 |
|               | zigbee-docs    | Z-stack笔记中加入低功耗说明。 | 
| 2016/12/19    | zigbee-ztack   | 添加了门锁反锁识别，添加了RFID刷卡读写卡程序，可以利用RFID卡开门。 |
|               | 论文  	 | 修改了3.3节，添加了摘要。  | 
| 2016/12/20    | zigbee-ztack   | 修改了EEPROM读取数据的BUG，添加了RFID卡的权限功能，包括普通进出卡，授权卡，删权卡，总卡等，可以对门锁进行离线的授权和删权以及初始化处理，增加了普通卡列表存储，保存在EEPROM中。对Z-Stack中信道的修改和信标帧的请求周期做了测试，并利用Packet Sniffer抓包工具对网络的建立过程进行了深入分析。 |
|               | zigbee-docs  	 | 添加了Packet Sniffer对于网络建立过程的数据帧的分析说明。  | 
| 2016/12/21    | zigbee-ztack   | 改写了基站的LED驱动，增加了基站的串口驱动，实现了基站和门锁之间的广播和点播通信，利用串口助手增加了点对点通信数据丢包率的测试，明天可以根据地形、距离和电池电量进行丢包率测试。 |
|               | zigbee-docs  	 | 增加了基站和门锁各种可能断网和连网的抓包情况说明。  | 
| 2016/12/22    | zigbee-ztack   | 使用两把门锁点对点通信的方式实现和基站的通信，进行了丢包率测试，分别测试了10，15，20，25，30，35，40米平均三次，每次发送100帧数据，每帧数据3s发送一次，丢包率测试情况，正对的测试效果好，侧对的效果略差，误差率一般都在2%以内。 |
|               | zigbee-docs  	 | 增加了修改发射功率的说明。|
| 2016/12/23    | zigbee-ztack   | 基站添加了关联表用来关联连接的门锁设备信息，基站实现了通过网络地址点对点发送数据给门锁，基站添加了串口驱动程序，实现了TCP客户端和上位机Node的Tcp服务端通信。 |
|               | zigbee-docs  	 | 增加了基站和上位机之间的通信协议文档，3.0版本，后期可能还需要修改。|
| 2016/12/26    | zigbee-ztack   | 编写了和上位机通信的协议程序。|
|               | zigbee-http  	 | 添加了获取门锁关联列表页面。|
| 2016/12/27    | zigbee-ztack   | 获取关联列表 |
|               | zigbee-http  	 | redis发布，socket通信 |
|               | zigbee-tcp  	 | redis订阅，发送数据给基站 |
| 2016/12/28    | zigbee-ztack   | 反馈基站的门锁关联列表数据给tcp服务器，通过接接收上位机的命令发送点播信息给门锁，门锁开门并反馈开门命令信息 |
|               | zigbee-http  	 | 可以发送命令给基站，并从基站获取数据显示到网页客户端，通过socket和redis实现，添加了开门命令，可以远程进行开门 |
|               | zigbee-tcp  	 | 成功解析基站发送的数据帧，并通过redis发布给http服务器，实现了远程开门和获取基站列表数据 |
|               | zigbee-docs  	 | 修改了串口通信协议，升级至3.1版本 |
| 2016/12/29    | zigbee-ztack   | 添加Adc配置，检测电池电量，上传给上位机，开门时上传电池电量和信号强度 |
|               | zigbee-http  	 | 远程开门得到反馈或者超时触发开门失败，更新了协议的实现，获取关联地址时获取了MAC地址和网络地址，获取基站下每一把门锁的信号强度，电池电量以及MAC地址等 |
|               | zigbee-tcp  	 | 优化基站的数据结构 |
|               | zigbee-docs  	 | 修改了通信协议的命令传输数据|
| 2016/12/30    | zigbee-http    | 添加了操作员账号注册功能，添加了操作的删除和修改功能 |



## 论文目录进度

```javascript

.
├── 基于Zigbee的无线门锁系统设计与实现 
├── 摘要
├── 第一章 绪论	
│   ├── 1.1 研究背景与意义   
│   ├── 1.2 国内外研究现状
│   │   ├── 1.2.1 公租房国内外发展状况
│   │   ├── 1.2.2 智能锁国内外发展现状
│   │   └── 1.2.3 Zigbee无线网络研究现状   
│   ├── 1.3 本文的主要工作(未完成)
│   └── 1.4 本文的组织机构(未完成)		
├── 第二章 短距离无线网络中的Zigbee无线网络
│   ├── 2.1 短距离无线网络的分类
│   ├── 2.2 几种短距离无线通信技术的特点比较
│   ├── 2.3 Zigbee无线网络简介
│   │   ├── 2.3.1 Zigbee无线网络组成
│   │   ├── 2.3.2 Zigbee无线网络特点
│   │   └── 2.3.3  Zigbee无线网络的设备类型和拓扑结构
│   ├── 2.4 Zigbee无线网络协议栈
│   │   ├── 2.4.1 Zigbee无线网络的协议层和数据帧
│   │   ├── 2.4.2 物理层(MAC)
│   │   ├── 2.4.3 介质访问控制层(PHY)
│   │   ├── 2.4.4 网络层(NWK)
│   │   ├── 2.4.5 应用层(APL)
│   │   └── 2.4.6 安全服务
│   └── 2.5 本章小节
├── 第三章 系统总体设计
│   ├── 3.1 需求分析
│   │   ├── 3.1.1 无线门锁需求分析
│   │   └── 3.1.2 管理系统需求分析
│   ├── 3.2 系统整体框架
│   ├── 3.3 系统硬件总体设计
│   │   ├── 3.3.1 系统硬件拓扑设计
│   │   ├── 3.3.2 门锁硬件结构
│   │   └── 2.3.3 基站硬件结构
│   ├── 3.3 系统软件层级设计
│   └── 3.4 本章小节
├── 第四章 门锁和基站设计(未完成)
├── 第五章 门锁通讯和管理软件设计(未完成)
├── 第六章 系统实现和测试(未完成)
├── 第七章 总结与展望(未完成)
├── 参考文献(未完成)
├── 附录(未完成)
├── 致献(未完成)
└── 攻读学位期间参加的科研项目和成果(未完成)

```
