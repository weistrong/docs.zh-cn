---
description: 了解有关以下内容的详细信息： TransactionBridge. RegistrationCoordinatorResponseInvalidMetadata
title: Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorResponseInvalidMetadata
ms.date: 03/30/2017
ms.assetid: a174bbf5-0ffe-4fda-969d-e7fbd1996123
ms.openlocfilehash: 2eeb5955f2d0bf3afd01ebfc7474cbccbcb70980
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99635683"
---
# <a name="microsofttransactionstransactionbridgeregistrationcoordinatorresponseinvalidmetadata"></a><span data-ttu-id="7db7d-103">Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorResponseInvalidMetadata</span><span class="sxs-lookup"><span data-stu-id="7db7d-103">Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorResponseInvalidMetadata</span></span>

<span data-ttu-id="7db7d-104">WS-Atomic Transaction 协议服务接收到来自其协调程序的 RegisterResponse 消息，其中包含带有无效或不兼容元数据的终结点引用。</span><span class="sxs-lookup"><span data-stu-id="7db7d-104">The WS-Atomic Transaction protocol service received a RegisterResponse message from its coordinator that contains an endpoint reference with invalid or incompatible metadata.</span></span>  
  
## <a name="description"></a><span data-ttu-id="7db7d-105">说明</span><span class="sxs-lookup"><span data-stu-id="7db7d-105">Description</span></span>  

 <span data-ttu-id="7db7d-106">在本地事务管理器尝试向其上级事务管理器进行注册并且上级在 RegisterResponse 消息中返回无效地址时被跟踪。</span><span class="sxs-lookup"><span data-stu-id="7db7d-106">Traced when the local Transaction Manager tries to register with its superior Transaction Manager and the superior returns an invalid address within the RegisterResponse message.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7db7d-107">请参阅</span><span class="sxs-lookup"><span data-stu-id="7db7d-107">See also</span></span>

- [<span data-ttu-id="7db7d-108">跟踪</span><span class="sxs-lookup"><span data-stu-id="7db7d-108">Tracing</span></span>](index.md)
- [<span data-ttu-id="7db7d-109">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="7db7d-109">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="7db7d-110">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="7db7d-110">Administration and Diagnostics</span></span>](../index.md)
