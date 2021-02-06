---
description: 了解详细信息： 3550-BufferOutOfOrderMessageNoInstance
title: 3550 - BufferOutOfOrderMessageNoInstance
ms.date: 03/30/2017
ms.assetid: 1299d294-99b8-430e-98b1-55f5f17002f3
ms.openlocfilehash: cb51f9fa32de1b56560f9593dae2ec82c100dc65
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99631445"
---
# <a name="3550---bufferoutofordermessagenoinstance"></a><span data-ttu-id="863d2-103">3550 - BufferOutOfOrderMessageNoInstance</span><span class="sxs-lookup"><span data-stu-id="863d2-103">3550 - BufferOutOfOrderMessageNoInstance</span></span>

## <a name="properties"></a><span data-ttu-id="863d2-104">属性</span><span class="sxs-lookup"><span data-stu-id="863d2-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="863d2-105">ID</span><span class="sxs-lookup"><span data-stu-id="863d2-105">ID</span></span>|<span data-ttu-id="863d2-106">3550</span><span class="sxs-lookup"><span data-stu-id="863d2-106">3550</span></span>|  
|<span data-ttu-id="863d2-107">关键字</span><span class="sxs-lookup"><span data-stu-id="863d2-107">Keywords</span></span>|<span data-ttu-id="863d2-108">WFServices</span><span class="sxs-lookup"><span data-stu-id="863d2-108">WFServices</span></span>|  
|<span data-ttu-id="863d2-109">级别</span><span class="sxs-lookup"><span data-stu-id="863d2-109">Level</span></span>|<span data-ttu-id="863d2-110">信息</span><span class="sxs-lookup"><span data-stu-id="863d2-110">Information</span></span>|  
|<span data-ttu-id="863d2-111">通道</span><span class="sxs-lookup"><span data-stu-id="863d2-111">Channel</span></span>|<span data-ttu-id="863d2-112">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="863d2-112">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="863d2-113">说明</span><span class="sxs-lookup"><span data-stu-id="863d2-113">Description</span></span>  

 <span data-ttu-id="863d2-114">指示缓冲接收已失败。</span><span class="sxs-lookup"><span data-stu-id="863d2-114">Indicates a buffered receive has failed.</span></span> <span data-ttu-id="863d2-115">服务实例准备好处理此特定操作时，将再次尝试该操作。</span><span class="sxs-lookup"><span data-stu-id="863d2-115">The operation will be attempted again when the service instance is ready to process this particular operation.</span></span>  
  
## <a name="message"></a><span data-ttu-id="863d2-116">消息</span><span class="sxs-lookup"><span data-stu-id="863d2-116">Message</span></span>  

 <span data-ttu-id="863d2-117">此时不能执行操作“%1”。</span><span class="sxs-lookup"><span data-stu-id="863d2-117">Operation '%1' cannot be performed at this time.</span></span> <span data-ttu-id="863d2-118">服务实例准备好处理此特定操作时，将进行另一个尝试。</span><span class="sxs-lookup"><span data-stu-id="863d2-118">Another attempt will be made when the service instance is ready to process this particular operation.</span></span>  
  
## <a name="details"></a><span data-ttu-id="863d2-119">详细信息</span><span class="sxs-lookup"><span data-stu-id="863d2-119">Details</span></span>  
  
|<span data-ttu-id="863d2-120">数据项名称</span><span class="sxs-lookup"><span data-stu-id="863d2-120">Data Item Name</span></span>|<span data-ttu-id="863d2-121">数据项类型</span><span class="sxs-lookup"><span data-stu-id="863d2-121">Data Item Type</span></span>|<span data-ttu-id="863d2-122">说明</span><span class="sxs-lookup"><span data-stu-id="863d2-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="863d2-123">OperationName</span><span class="sxs-lookup"><span data-stu-id="863d2-123">OperationName</span></span>|<span data-ttu-id="863d2-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="863d2-124">xs:string</span></span>|<span data-ttu-id="863d2-125">操作的名称。</span><span class="sxs-lookup"><span data-stu-id="863d2-125">The name of the operation.</span></span>|  
|<span data-ttu-id="863d2-126">应用程序域</span><span class="sxs-lookup"><span data-stu-id="863d2-126">AppDomain</span></span>|<span data-ttu-id="863d2-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="863d2-127">xs:string</span></span>|<span data-ttu-id="863d2-128">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="863d2-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
