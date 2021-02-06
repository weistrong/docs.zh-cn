---
description: 了解有关以下方面的详细信息：终结点：未授权的安全调用
title: 终结点：未授权的安全调用次数
ms.date: 03/30/2017
ms.assetid: d25095ff-9ff0-4c69-a674-4e6a9fe3f4dc
ms.openlocfilehash: 258c984e8a7986594b6da6f5c2a8c030907f82ca
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99655469"
---
# <a name="endpoint-security-calls-not-authorized"></a><span data-ttu-id="e8fee-103">终结点：未授权的安全调用次数</span><span class="sxs-lookup"><span data-stu-id="e8fee-103">Endpoint: Security Calls Not Authorized</span></span>

<span data-ttu-id="e8fee-104">计数器名称：Security Calls Not Authorized（未授权的安全调用次数）。</span><span class="sxs-lookup"><span data-stu-id="e8fee-104">Counter Name: Security Calls Not Authorized.</span></span>  
  
## <a name="description"></a><span data-ttu-id="e8fee-105">说明</span><span class="sxs-lookup"><span data-stu-id="e8fee-105">Description</span></span>  

 <span data-ttu-id="e8fee-106">当 <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccess%2A> 方法返回 `false` 时，此计数器将递增。</span><span class="sxs-lookup"><span data-stu-id="e8fee-106">This counter is incremented when the <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccess%2A> method returns `false`.</span></span> <span data-ttu-id="e8fee-107">它指示传入的消息来自有效的用户并得到了良好保护，但该用户没有获得执行特定任务的授权。</span><span class="sxs-lookup"><span data-stu-id="e8fee-107">It indicates that the incoming message is from a valid user and protected properly, but the user is not authorized to do specific tasks.</span></span>
