---
description: 了解详细信息：在查询中使用批注
title: 在查询中使用批注
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 50855b30-d5fe-49a9-89d3-3f1bfd670958
ms.openlocfilehash: 97423fe8ea7d90522a5f469adda5f645aa7e4485
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698019"
---
# <a name="using-annotation-in-queries"></a><span data-ttu-id="c6676-103">在查询中使用批注</span><span class="sxs-lookup"><span data-stu-id="c6676-103">Using Annotation in Queries</span></span>

<span data-ttu-id="c6676-104">通过批注，可以使用可在生成时后配置的某个值任意标记跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="c6676-104">Annotations allow you to arbitrarily tag tracking records with a value that can be configured after build time.</span></span> <span data-ttu-id="c6676-105">例如，您可能希望多个工作流的多个跟踪记录都用 "Mail Server" = = "Mail Server1" 标记。</span><span class="sxs-lookup"><span data-stu-id="c6676-105">For example, you might want several tracking records across several workflows to be tagged with "Mail Server" == "Mail Server1".</span></span> <span data-ttu-id="c6676-106">这样便于在以后查询跟踪记录时查找带有此标记的所有记录。</span><span class="sxs-lookup"><span data-stu-id="c6676-106">This makes it easy to find all records with this tag when querying tracking records later.</span></span>  
  
## <a name="adding-annotations"></a><span data-ttu-id="c6676-107">添加批注</span><span class="sxs-lookup"><span data-stu-id="c6676-107">Adding Annotations</span></span>  

 <span data-ttu-id="c6676-108">可将批注添加到跟踪查询中，如下例所示。</span><span class="sxs-lookup"><span data-stu-id="c6676-108">An annotation can be added to a tracking query as shown in the following example.</span></span>  
  
```xml  
<activityStateQuery activityName="SendEmailActivity">  
  <states>  
    <state name="Closed"/>  
  </states>  
  <annotations>  
    <annotation name="MailServer" value="Mail Server1"/>  
  </annotations>  
</activityStateQuery>  
```  
  
> [!NOTE]
> <span data-ttu-id="c6676-109">可以使用这些跟踪查询元素创建跟踪配置文件。</span><span class="sxs-lookup"><span data-stu-id="c6676-109">These tracking query elements can be used to create a tracking profile.</span></span> <span data-ttu-id="c6676-110">可以通过配置或使用代码来创建跟踪配置文件。</span><span class="sxs-lookup"><span data-stu-id="c6676-110">A tracking profile can be created either in configuration or using code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c6676-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="c6676-111">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ProfileWorkflowElement>
- <xref:System.Activities.Tracking.TrackingProfile>
- [\<participants>](participants.md)
- [<span data-ttu-id="c6676-112">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="c6676-112">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="c6676-113">跟踪配置文件</span><span class="sxs-lookup"><span data-stu-id="c6676-113">Tracking Profiles</span></span>](../../../windows-workflow-foundation/tracking-profiles.md)
