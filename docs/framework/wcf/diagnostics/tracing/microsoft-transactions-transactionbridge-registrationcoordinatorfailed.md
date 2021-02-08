---
description: 了解有关以下内容的详细信息： TransactionBridge. RegistrationCoordinatorFailed
title: Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorFailed
ms.date: 03/30/2017
ms.assetid: 96474056-0418-41e4-8c75-bbc0a853eaba
ms.openlocfilehash: f522fb91db6c721c43d2768a9eb79d627fbc2a59
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99770607"
---
# <a name="microsofttransactionstransactionbridgeregistrationcoordinatorfailed"></a><span data-ttu-id="f075a-103">Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorFailed</span><span class="sxs-lookup"><span data-stu-id="f075a-103">Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorFailed</span></span>

<span data-ttu-id="f075a-104">WS-AT 协议服务无法向其协调程序发送注册消息</span><span class="sxs-lookup"><span data-stu-id="f075a-104">The WS-AT protocol service failed to send a Register message to its coordinator</span></span>  
  
## <a name="description"></a><span data-ttu-id="f075a-105">说明</span><span class="sxs-lookup"><span data-stu-id="f075a-105">Description</span></span>  

 <span data-ttu-id="f075a-106">在本地 TransactionManager 由于不能发送消息而无法向其上级 TransactionManager 注册时跟踪。</span><span class="sxs-lookup"><span data-stu-id="f075a-106">Traced if the local TransactionManager is not able to Register with its superior TransactionManager due to the inability to send a message.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="f075a-107">疑难解答</span><span class="sxs-lookup"><span data-stu-id="f075a-107">Troubleshooting</span></span>  

 <span data-ttu-id="f075a-108">检查跟踪消息以查找导致消息发送失败的异常</span><span class="sxs-lookup"><span data-stu-id="f075a-108">Inspect the trace message for the exception causing the message send failure</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f075a-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="f075a-109">See also</span></span>

- [<span data-ttu-id="f075a-110">跟踪</span><span class="sxs-lookup"><span data-stu-id="f075a-110">Tracing</span></span>](index.md)
- [<span data-ttu-id="f075a-111">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="f075a-111">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="f075a-112">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="f075a-112">Administration and Diagnostics</span></span>](../index.md)
