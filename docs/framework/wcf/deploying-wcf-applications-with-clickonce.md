---
description: 了解详细信息：用 ClickOnce 部署 WCF 应用程序
title: 使用 ClickOnce 部署 WCF 应用程序
ms.date: 03/30/2017
ms.assetid: 1a11feee-2a47-4d3e-a28a-ad69d5ff93e0
ms.openlocfilehash: f0a78bab6bbe7ddfd431e8e12bfe1ca9c9143143
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99646083"
---
# <a name="deploying-wcf-applications-with-clickonce"></a>使用 ClickOnce 部署 WCF 应用程序

可以使用 ClickOnce 技术部署使用 Windows Communication Foundation (WCF) 的客户端应用程序。 只要客户端应用程序已使用受信任的证书进行数据签名，此技术就允许它们充分利用代码访问安全机制所提供的运行时安全保护。 用于对 ClickOnce 应用程序签名的证书必须位于受信任的发行者存储中，并且必须将客户端计算机上的本地安全策略配置为对使用该发行者的证书签名的应用程序授予完全信任权限。  
  
 有关配置 ClickOnce 应用程序和受信任的发布者的信息，请参阅 [配置 Clickonce 受信任的发布者](/previous-versions/dotnet/articles/ms996418(v=msdn.10))。  
  
## <a name="see-also"></a>请参阅

- [受信任的应用程序部署概述](/visualstudio/deployment/trusted-application-deployment-overview)
- [Windows 窗体应用程序的 ClickOnce 部署](/previous-versions/visualstudio/visual-studio-2008/wh45kb66(v=vs.90))
