---
description: 了解详细信息： DeliveryRequirementsAttribute
title: DeliveryRequirementsAttribute
ms.date: 03/30/2017
ms.assetid: 40c5435c-a325-4cf8-9dd0-d6e24b4a56a3
ms.openlocfilehash: ee27ada1c1fb447de3d7a108a4a285ca106e4e8e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99757496"
---
# <a name="deliveryrequirementsattribute"></a><span data-ttu-id="d51df-103">DeliveryRequirementsAttribute</span><span class="sxs-lookup"><span data-stu-id="d51df-103">DeliveryRequirementsAttribute</span></span>

<span data-ttu-id="d51df-104">DeliveryRequirementsAttribute</span><span class="sxs-lookup"><span data-stu-id="d51df-104">DeliveryRequirementsAttribute</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d51df-105">语法</span><span class="sxs-lookup"><span data-stu-id="d51df-105">Syntax</span></span>  
  
```csharp
class DeliveryRequirementsAttribute : Behavior  
{  
  string QueuedDeliveryRequirements;  
  boolean RequireOrderedDelivery;  
  string TargetContract;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="d51df-106">方法</span><span class="sxs-lookup"><span data-stu-id="d51df-106">Methods</span></span>  

 <span data-ttu-id="d51df-107">DeliveryRequirementsAttribute 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="d51df-107">The DeliveryRequirementsAttribute class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="d51df-108">属性</span><span class="sxs-lookup"><span data-stu-id="d51df-108">Properties</span></span>  

 <span data-ttu-id="d51df-109">DeliveryRequirementsAttribute 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="d51df-109">The DeliveryRequirementsAttribute class has the following properties:</span></span>  
  
### <a name="queueddeliveryrequirements"></a><span data-ttu-id="d51df-110">QueuedDeliveryRequirements</span><span class="sxs-lookup"><span data-stu-id="d51df-110">QueuedDeliveryRequirements</span></span>  

 <span data-ttu-id="d51df-111">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="d51df-111">Data type: string</span></span>  
  
 <span data-ttu-id="d51df-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="d51df-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d51df-113">指定服务的绑定是否支持协定。</span><span class="sxs-lookup"><span data-stu-id="d51df-113">Specifies whether the binding for a service supports contracts.</span></span>  
  
### <a name="requireordereddelivery"></a><span data-ttu-id="d51df-114">RequireOrderedDelivery</span><span class="sxs-lookup"><span data-stu-id="d51df-114">RequireOrderedDelivery</span></span>  

 <span data-ttu-id="d51df-115">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="d51df-115">Data type: boolean</span></span>  
  
 <span data-ttu-id="d51df-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="d51df-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d51df-117">指定绑定是否支持已排序消息。</span><span class="sxs-lookup"><span data-stu-id="d51df-117">Specifies whether the binding supports ordered messages.</span></span>  
  
### <a name="targetcontract"></a><span data-ttu-id="d51df-118">TargetContract</span><span class="sxs-lookup"><span data-stu-id="d51df-118">TargetContract</span></span>  

 <span data-ttu-id="d51df-119">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="d51df-119">Data type: string</span></span>  
  
 <span data-ttu-id="d51df-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="d51df-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d51df-121">该类应用到的协定。</span><span class="sxs-lookup"><span data-stu-id="d51df-121">The contract to which it applies.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d51df-122">要求</span><span class="sxs-lookup"><span data-stu-id="d51df-122">Requirements</span></span>  
  
|<span data-ttu-id="d51df-123">MOF</span><span class="sxs-lookup"><span data-stu-id="d51df-123">MOF</span></span>|<span data-ttu-id="d51df-124">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="d51df-124">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="d51df-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="d51df-125">Namespace</span></span>|<span data-ttu-id="d51df-126">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="d51df-126">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d51df-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="d51df-127">See also</span></span>

- <xref:System.ServiceModel.DeliveryRequirementsAttribute>
