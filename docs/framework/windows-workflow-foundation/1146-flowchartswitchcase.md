---
description: 了解详细信息： 1146-FlowchartSwitchCase
title: 1146 - FlowchartSwitchCase
ms.date: 03/30/2017
ms.assetid: 274e9209-1720-4512-a615-e742f00895f4
ms.openlocfilehash: f6e9b33f9c068b51695d3ac46cda51fb6d9f8b3f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99667065"
---
# <a name="1146---flowchartswitchcase"></a><span data-ttu-id="c9b37-103">1146 - FlowchartSwitchCase</span><span class="sxs-lookup"><span data-stu-id="c9b37-103">1146 - FlowchartSwitchCase</span></span>

## <a name="properties"></a><span data-ttu-id="c9b37-104">属性</span><span class="sxs-lookup"><span data-stu-id="c9b37-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="c9b37-105">ID</span><span class="sxs-lookup"><span data-stu-id="c9b37-105">ID</span></span>|<span data-ttu-id="c9b37-106">1146</span><span class="sxs-lookup"><span data-stu-id="c9b37-106">1146</span></span>|  
|<span data-ttu-id="c9b37-107">关键字</span><span class="sxs-lookup"><span data-stu-id="c9b37-107">Keywords</span></span>|<span data-ttu-id="c9b37-108">WFActivities</span><span class="sxs-lookup"><span data-stu-id="c9b37-108">WFActivities</span></span>|  
|<span data-ttu-id="c9b37-109">级别</span><span class="sxs-lookup"><span data-stu-id="c9b37-109">Level</span></span>|<span data-ttu-id="c9b37-110">信息</span><span class="sxs-lookup"><span data-stu-id="c9b37-110">Information</span></span>|  
|<span data-ttu-id="c9b37-111">通道</span><span class="sxs-lookup"><span data-stu-id="c9b37-111">Channel</span></span>|<span data-ttu-id="c9b37-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="c9b37-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="c9b37-113">说明</span><span class="sxs-lookup"><span data-stu-id="c9b37-113">Description</span></span>  

 <span data-ttu-id="c9b37-114">指示在 Flowchart 开关中已选择的大小写。</span><span class="sxs-lookup"><span data-stu-id="c9b37-114">Indicates which case has been selected in a Flowchart switch.</span></span>  
  
## <a name="message"></a><span data-ttu-id="c9b37-115">消息</span><span class="sxs-lookup"><span data-stu-id="c9b37-115">Message</span></span>  

 <span data-ttu-id="c9b37-116">Flowchart“%1”/FlowSwitch - 选择了 Case“%2”。</span><span class="sxs-lookup"><span data-stu-id="c9b37-116">Flowchart '%1'/FlowSwitch - Case '%2' was selected.</span></span>  
  
## <a name="details"></a><span data-ttu-id="c9b37-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="c9b37-117">Details</span></span>  
  
|<span data-ttu-id="c9b37-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="c9b37-118">Data Item Name</span></span>|<span data-ttu-id="c9b37-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="c9b37-119">Data Item Type</span></span>|<span data-ttu-id="c9b37-120">说明</span><span class="sxs-lookup"><span data-stu-id="c9b37-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="c9b37-121">FlowChart</span><span class="sxs-lookup"><span data-stu-id="c9b37-121">FlowChart</span></span>|<span data-ttu-id="c9b37-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="c9b37-122">xs:string</span></span>|<span data-ttu-id="c9b37-123">FlowChart 的显示名称。</span><span class="sxs-lookup"><span data-stu-id="c9b37-123">The display name of the FlowChart.</span></span>|  
|<span data-ttu-id="c9b37-124">案例</span><span class="sxs-lookup"><span data-stu-id="c9b37-124">Case</span></span>|<span data-ttu-id="c9b37-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="c9b37-125">xs:string</span></span>|<span data-ttu-id="c9b37-126">所选的开关大小写。</span><span class="sxs-lookup"><span data-stu-id="c9b37-126">The switch case that selected.</span></span>|  
|<span data-ttu-id="c9b37-127">应用程序域</span><span class="sxs-lookup"><span data-stu-id="c9b37-127">AppDomain</span></span>|<span data-ttu-id="c9b37-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="c9b37-128">xs:string</span></span>|<span data-ttu-id="c9b37-129">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="c9b37-129">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
