## Huo管家 - 系统框架

🔥 ![系统框架图片](https://github.com/inkcat520/Huo_Butler/blob/master/Huo%E7%AE%A1%E5%AE%B6-%E7%B3%BB%E7%BB%9F%E6%A1%86%E5%9B%BE.jpg) 🔥

## 目录

- [简介](#简介)
- [演示视频](#演示视频)
- [系统架构](#系统架构)
- [应用场景](#应用场景)
- [注意事项](#注意事项)
- [致谢](#致谢)

## 简介

Huo管家是一种基于深度学习和物联网技术的火灾检测和仓库管理系统。系统利用高清摄像头图像的深度处理来准确判别火灾现场，同时利用火焰扩散增长率判断火势情况，并对火情火势进行分类。

该系统适用于仓库、家庭、公司等场景，特别是长时间无人看管的地方，主要功能包括火灾检测、火灾程度判断、火灾成因分析，以实现更快速的灭火和减小火灾的影响。

## 演示视频

▶️ [演示视频链接](https://www.bilibili.com/video/BV1wP411z7LJ/) ◀️

## 系统架构

本系统的架构包括以下模块：

1. **感知层**：采用小熊派作为终端节点，通过环境数据采集装置进行数据采集，包括温湿度、光照强度、烟雾浓度和电机状态等。通过WIFI通信将数据发送至树莓派进行统一集中处理。

2. **网关层**：采用自行设计的基于LiteOS的IOTBoard，搭载红外传感器、蜂鸣器和NFC读写模块，用于管理终端设备的注册、上网以及确认设备是否在线。树莓派作为网关连接网络，通过串口将空闲的网络端口发送给IOTBoard，并通过NFC模块与终端设备的NFC标签进行网络信息的读写。

3. **应用层**：树莓派作为MQTT协议的客户端和服务端，与应用层服务器进行数据的发送和接收。使用layUI前端开发框架和spring后端开发框架实现前后端的联动通信，保证数据页面的实时性和联动性。此外，还使用AndroidStudio开发APP，通过APP页面展示环境数据并可下发命令，实现系统的联动控制和异常状况处理。

4. **边缘计算**：本系统以基于NanoDet深度学习框架的AI边缘计算为基准，利用树莓派对拍摄的图像进行处理。通过图像形态学处理，描绘火焰图像的轮廓并计算出膨胀速率，作为火情等级的关键参数。这样能更好地管控火灾现场内容，并方便进行灭火处理。

## 应用场景

本系统适用于仓库、家庭、公司等存放贵重物品且在长时间内无人员看管的场景。它可以提供及时的火灾检测和灭火支持，帮助减小火灾造成的损失并保护人员和财产的安全。

## 注意事项

在使用本系统时，请注意以下事项：

⚠️ 遵循开源许可：确保系统的源代码按照相应开源许可证的规定进行使用和分发。

⚠️ 欢迎贡献者：鼓励其他开发者参与项目，并提供系统改进的建议、修复漏洞或添加新功能的代码。

💡 请在使用本系统前阅读注意事项，并遵守开源许可证和相关法律法规。

## 致谢

感谢团队成员的共同努力。对于Huo管家系统的开发和推进，团队内外的协作和支持不胜感激。特此致谢。

⭐ 如果您觉得本项目对您有帮助，请给我们一个星星支持！ ⭐️