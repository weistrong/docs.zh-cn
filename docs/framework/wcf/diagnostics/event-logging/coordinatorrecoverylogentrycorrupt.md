---
description: 了解详细信息： CoordinatorRecoveryLogEntryCorrupt
title: CoordinatorRecoveryLogEntryCorrupt
ms.date: 03/30/2017
ms.assetid: 3cd0c3e3-84c8-4d43-a561-a8851c78e565
ms.openlocfilehash: 3a848c634a226b34023a24898f9827162b4dafc7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99771335"
---
# <a name="coordinatorrecoverylogentrycorrupt"></a><span data-ttu-id="4b4a6-103">CoordinatorRecoveryLogEntryCorrupt</span><span class="sxs-lookup"><span data-stu-id="4b4a6-103">CoordinatorRecoveryLogEntryCorrupt</span></span>

<span data-ttu-id="4b4a6-104">Id：139</span><span class="sxs-lookup"><span data-stu-id="4b4a6-104">Id: 139</span></span>  
  
 <span data-ttu-id="4b4a6-105">严重性：错误</span><span class="sxs-lookup"><span data-stu-id="4b4a6-105">Severity: Error</span></span>  
  
 <span data-ttu-id="4b4a6-106">类别：TransactionBridge</span><span class="sxs-lookup"><span data-stu-id="4b4a6-106">Category: TransactionBridge</span></span>  
  
## <a name="description"></a><span data-ttu-id="4b4a6-107">说明</span><span class="sxs-lookup"><span data-stu-id="4b4a6-107">Description</span></span>  

 <span data-ttu-id="4b4a6-108">此事件指示协调程序恢复日志条目已损坏，无法进行反序列化。</span><span class="sxs-lookup"><span data-stu-id="4b4a6-108">This event indicates that a  coordinator recovery log entry was corrupt and could not be deserialized.</span></span> <span data-ttu-id="4b4a6-109">此错误可能导致数据丢失。</span><span class="sxs-lookup"><span data-stu-id="4b4a6-109">Data loss may result from this error.</span></span> <span data-ttu-id="4b4a6-110">此事件列出了事务 ID、恢复数据（Base64 编码）、异常、进程名称和进程 ID。</span><span class="sxs-lookup"><span data-stu-id="4b4a6-110">The event lists the Transaction ID, Recovery data (Base64 encoded), exception, process name and process ID.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4b4a6-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="4b4a6-111">See also</span></span>

- [<span data-ttu-id="4b4a6-112">事件日志记录</span><span class="sxs-lookup"><span data-stu-id="4b4a6-112">Event Logging</span></span>](index.md)
- [<span data-ttu-id="4b4a6-113">事件常规参考</span><span class="sxs-lookup"><span data-stu-id="4b4a6-113">Events General Reference</span></span>](events-general-reference.md)
