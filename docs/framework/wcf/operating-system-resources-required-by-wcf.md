---
description: 了解详细信息： WCF 所需的操作系统资源
title: WCF 所要求的操作系统资源
ms.date: 03/30/2017
ms.assetid: cdd9a331-53fe-4e0d-bdfe-782264aec5c9
ms.openlocfilehash: 717ab2074c0dcf840919c2bd8afa2641e106ac11
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99779213"
---
# <a name="operating-system-resources-required-by-wcf"></a>WCF 所要求的操作系统资源

Windows Communication Foundation (WCF) 依赖于操作系统提供的多个资源才能正常运行。 下表列出了这些资源：

|资源|说明|
|--------------|-----------------|
|Microsoft 分布式事务协调器 (MSDTC)|支持 OleTx 事务所必需。|
|Internet 信息服务 (IIS)|如果希望使用 IIS 来承载应用程序，则是必需的。|
|Windows 进程激活服务 (WAS)|如果希望使用 WAS 来承载应用程序，则是必需的。|
