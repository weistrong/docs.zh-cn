---
description: 了解详细信息： 4806-DiscoveryMessageWithInvalidRelatesToOrOperationCompleted
title: 4806 - DiscoveryMessageWithInvalidRelatesToOrOperationCompleted
ms.date: 03/30/2017
ms.assetid: 19e9a660-25f3-4332-b716-a12a59f2cbbb
ms.openlocfilehash: 51c1dd9e4478f53098a8087cb4c2e2efdceeaa2a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99788379"
---
# <a name="4806---discoverymessagewithinvalidrelatestooroperationcompleted"></a><span data-ttu-id="498c2-103">4806 - DiscoveryMessageWithInvalidRelatesToOrOperationCompleted</span><span class="sxs-lookup"><span data-stu-id="498c2-103">4806 - DiscoveryMessageWithInvalidRelatesToOrOperationCompleted</span></span>

## <a name="properties"></a><span data-ttu-id="498c2-104">属性</span><span class="sxs-lookup"><span data-stu-id="498c2-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="498c2-105">ID</span><span class="sxs-lookup"><span data-stu-id="498c2-105">ID</span></span>|<span data-ttu-id="498c2-106">4806</span><span class="sxs-lookup"><span data-stu-id="498c2-106">4806</span></span>|  
|<span data-ttu-id="498c2-107">关键字</span><span class="sxs-lookup"><span data-stu-id="498c2-107">Keywords</span></span>|<span data-ttu-id="498c2-108">发现</span><span class="sxs-lookup"><span data-stu-id="498c2-108">Discovery</span></span>|  
|<span data-ttu-id="498c2-109">级别</span><span class="sxs-lookup"><span data-stu-id="498c2-109">Level</span></span>|<span data-ttu-id="498c2-110">警告</span><span class="sxs-lookup"><span data-stu-id="498c2-110">Warning</span></span>|  
|<span data-ttu-id="498c2-111">通道</span><span class="sxs-lookup"><span data-stu-id="498c2-111">Channel</span></span>|<span data-ttu-id="498c2-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="498c2-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="498c2-113">说明</span><span class="sxs-lookup"><span data-stu-id="498c2-113">Description</span></span>  

 <span data-ttu-id="498c2-114">当因为相应的操作已完成或 relatesTo 值无效而导致发现消息已被 DiscoveryClient 丢弃时，发出此事件。</span><span class="sxs-lookup"><span data-stu-id="498c2-114">This event is emitted when the discovery message was dropped by the DiscoveryClient because either the corresponding operation was completed or the relatesTo value is invalid.</span></span>  
  
## <a name="message"></a><span data-ttu-id="498c2-115">消息</span><span class="sxs-lookup"><span data-stu-id="498c2-115">Message</span></span>  

 <span data-ttu-id="498c2-116">messageId 为“%2”且 relatesTo 为“%3”的 %1 消息已被 DiscoveryClient 丢弃，因为相应的 %4 操作已完成或 relatesTo 值无效。</span><span class="sxs-lookup"><span data-stu-id="498c2-116">A %1 message with messageId='%2' and relatesTo='%3' was dropped by the DiscoveryClient because either the corresponding %4 operation was completed or the relatesTo value is invalid.</span></span>  
  
## <a name="details"></a><span data-ttu-id="498c2-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="498c2-117">Details</span></span>
