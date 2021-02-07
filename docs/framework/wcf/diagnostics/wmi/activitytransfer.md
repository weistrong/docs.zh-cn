---
description: 了解详细信息： ActivityTransfer
title: ActivityTransfer
ms.date: 03/30/2017
ms.assetid: fc40ef17-2a92-4ce2-853c-6ba8e5d571f3
ms.openlocfilehash: 28f7d1c0d1056327313e7aa6be293eb325d8f265
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99758003"
---
# <a name="activitytransfer"></a><span data-ttu-id="eb7ad-103">ActivityTransfer</span><span class="sxs-lookup"><span data-stu-id="eb7ad-103">ActivityTransfer</span></span>

<span data-ttu-id="eb7ad-104">活动传输事件</span><span class="sxs-lookup"><span data-stu-id="eb7ad-104">Activity Transfer Event</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eb7ad-105">语法</span><span class="sxs-lookup"><span data-stu-id="eb7ad-105">Syntax</span></span>  
  
```csharp
class ActivityTransfer : WSAT_TraceEvent  
{  
  object ActivityID;  
  object RelatedActivityID;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="eb7ad-106">方法</span><span class="sxs-lookup"><span data-stu-id="eb7ad-106">Methods</span></span>  

 <span data-ttu-id="eb7ad-107">ActivityTransfer 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="eb7ad-107">The ActivityTransfer class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="eb7ad-108">属性</span><span class="sxs-lookup"><span data-stu-id="eb7ad-108">Properties</span></span>  

 <span data-ttu-id="eb7ad-109">ActivityTransfer 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="eb7ad-109">The ActivityTransfer class has the following properties:</span></span>  
  
### <a name="activityid"></a><span data-ttu-id="eb7ad-110">ActivityID</span><span class="sxs-lookup"><span data-stu-id="eb7ad-110">ActivityID</span></span>  
  
- <span data-ttu-id="eb7ad-111">数据类型：object</span><span class="sxs-lookup"><span data-stu-id="eb7ad-111">Data type: object</span></span>  
    <span data-ttu-id="eb7ad-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="eb7ad-112">Access type: Read-only</span></span>  
  
- <span data-ttu-id="eb7ad-113">活动 ID</span><span class="sxs-lookup"><span data-stu-id="eb7ad-113">Activity ID</span></span>  
  
### <a name="relatedactivityid"></a><span data-ttu-id="eb7ad-114">RelatedActivityID</span><span class="sxs-lookup"><span data-stu-id="eb7ad-114">RelatedActivityID</span></span>  
  
- <span data-ttu-id="eb7ad-115">数据类型：object</span><span class="sxs-lookup"><span data-stu-id="eb7ad-115">Data type: object</span></span>  
    <span data-ttu-id="eb7ad-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="eb7ad-116">Access type: Read-only</span></span>  
  
- <span data-ttu-id="eb7ad-117">相关活动 ID</span><span class="sxs-lookup"><span data-stu-id="eb7ad-117">Related Activity ID</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eb7ad-118">要求</span><span class="sxs-lookup"><span data-stu-id="eb7ad-118">Requirements</span></span>  
  
|<span data-ttu-id="eb7ad-119">MOF</span><span class="sxs-lookup"><span data-stu-id="eb7ad-119">MOF</span></span>|<span data-ttu-id="eb7ad-120">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="eb7ad-120">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="eb7ad-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="eb7ad-121">Namespace</span></span>|<span data-ttu-id="eb7ad-122">已在 root\ServiceModel 中定义。</span><span class="sxs-lookup"><span data-stu-id="eb7ad-122">Defined in root\ServiceModel.</span></span>|
