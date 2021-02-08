---
description: 了解详细信息： WCF 安全中的加密灵活性
title: WCF 安全中的加密灵活性
ms.date: 03/30/2017
ms.assetid: c2c549e5-ac19-40c5-b686-8f67f52b6dbf
ms.openlocfilehash: ab46034b16a846f7399220480fc928655d931be0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99778342"
---
# <a name="cryptographic-agility-in-wcf-security"></a>WCF 安全中的加密灵活性

此示例演示如何在标准/自定义算法中指定，以在 Windows Communication Foundation (WCF) 客户端和服务中提供加密敏捷实现。 该示例由下列项目组成：

**服务**

这是一个自承载的 WCF 服务，它可实现 `ICalculator` 接口，并使用启用了 <xref:System.ServiceModel.WSHttpBinding> 安全会话和可靠会话来保护终结点。 该服务定义一个自定义 `SecurityAlgorithmSuite` 类，以指定要用于消息安全的加密算法。

**客户端**

这是在身份验证成功后访问服务的 WCF 客户端。 该客户端调用由 `ICalculator` 接口公开并由服务实现的操作。 该客户端也定义相同的自定义 `SecurityAlgorithmSuite` 类，以指定要用于消息安全的加密算法。

## <a name="to-use-this-sample"></a>使用此示例

1. 在 Visual Studio 2012 中打开 CryptoAgility 解决方案。

2. 按 CTRL+SHIFT+B 生成解决方案。

3. 打开文件资源管理器并导航到 \WCF\Basic\Security\CryptoAgility\Service\bin 目录，并通过右键单击 service.exe 并选择 "以 **管理员身份运行**"，以管理员权限运行 service.exe 文件。

4. 导航到 \WCF\Basic\Security\CryptoAgility\Client\bin 目录并正常运行 client.exe 文件。

> [!IMPORTANT]
> 您的计算机上可能已安装这些示例。 在继续操作之前，请先检查以下（默认）目录：
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> 如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)] 此示例位于以下目录：
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Security\CryptoAgility`

## <a name="see-also"></a>请参阅

- [Windows Communication Foundation 安全性](../feature-details/security.md)
