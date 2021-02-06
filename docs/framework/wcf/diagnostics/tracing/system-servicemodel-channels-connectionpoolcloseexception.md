---
description: 了解有关以下方面的详细信息： ConnectionPoolCloseException
title: System.ServiceModel.Channels.ConnectionPoolCloseException
ms.date: 03/30/2017
ms.assetid: 8358898e-129e-4fac-a6bf-bf3aa4293ae2
ms.openlocfilehash: a65739cc872f3cd175d76e9113380f9f4185d498
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99644627"
---
# <a name="systemservicemodelchannelsconnectionpoolcloseexception"></a>System.ServiceModel.Channels.ConnectionPoolCloseException

关闭此连接池中的连接时发生异常。  
  
## <a name="description"></a>说明  

 此错误级别跟踪表明关闭 Windows Communication Foundation (WCF) 的连接池功能所使用的连接池时出错。 一种可能的原因是一个池连接或一组池连接在 CloseTimeout 内未成功关闭。 当引发此异常时，将中止该池内所有剩余的未关闭连接，并放弃其他池内的未关闭连接。  
  
## <a name="see-also"></a>请参阅

- [跟踪](index.md)
- [使用跟踪来排除应用程序故障](using-tracing-to-troubleshoot-your-application.md)
- [管理和诊断](../index.md)
