---
description: 了解详细信息： WF 中的运行时活动
title: WF 中的运行时活动
ms.date: 03/30/2017
ms.assetid: e5ae8c31-19bc-4655-88b3-6b75cd6a1bd5
ms.openlocfilehash: 5ff164539b9efd7b2b8a4e7cffd5239eae6145fe
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792630"
---
# <a name="runtime-activities-in-wf"></a><span data-ttu-id="58530-103">WF 中的运行时活动</span><span class="sxs-lookup"><span data-stu-id="58530-103">Runtime Activities in WF</span></span>

[!INCLUDE[netfx_current_short](../../../includes/netfx-current-short-md.md)] <span data-ttu-id="58530-104">为访问工作流运行时的功能提供若干系统提供的活动，如持久性和终止。</span><span class="sxs-lookup"><span data-stu-id="58530-104">provides several system-provided activities for accessing the features of the workflow runtime, such as persistence and termination.</span></span>  
  
|<span data-ttu-id="58530-105">活动</span><span class="sxs-lookup"><span data-stu-id="58530-105">Activity</span></span>|<span data-ttu-id="58530-106">说明</span><span class="sxs-lookup"><span data-stu-id="58530-106">Description</span></span>|  
|--------------|-----------------|  
|<xref:System.Activities.Statements.Persist>|<span data-ttu-id="58530-107">显式请求工作流持久保存其状态。</span><span class="sxs-lookup"><span data-stu-id="58530-107">Explicitly requests that the workflow persist its state.</span></span>|  
|<xref:System.Activities.Statements.TerminateWorkflow>|<span data-ttu-id="58530-108">终止运行工作流实例。</span><span class="sxs-lookup"><span data-stu-id="58530-108">Terminates the running workflow instance.</span></span>|  
|<xref:System.Activities.Statements.NoPersistScope>|<span data-ttu-id="58530-109">可防止子活动持久化的容器活动。</span><span class="sxs-lookup"><span data-stu-id="58530-109">A container activity that prevents child activities from persisting.</span></span>|
