---
description: 了解详细信息： ServiceTimeoutsBehavior
title: ServiceTimeoutsBehavior
ms.date: 03/30/2017
ms.assetid: 4412525d-a3cc-4eae-b3e8-a50ce766d09d
ms.openlocfilehash: 147d249af0e87bc41da93a4a31355da7053caaf6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99715413"
---
# <a name="servicetimeoutsbehavior"></a><span data-ttu-id="3a555-103">ServiceTimeoutsBehavior</span><span class="sxs-lookup"><span data-stu-id="3a555-103">ServiceTimeoutsBehavior</span></span>

<span data-ttu-id="3a555-104">ServiceTimeoutsBehavior</span><span class="sxs-lookup"><span data-stu-id="3a555-104">ServiceTimeoutsBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3a555-105">语法</span><span class="sxs-lookup"><span data-stu-id="3a555-105">Syntax</span></span>  
  
```csharp
class ServiceTimeoutsBehavior : Behavior  
{  
  datetime TransactionTimeout;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="3a555-106">方法</span><span class="sxs-lookup"><span data-stu-id="3a555-106">Methods</span></span>  

 <span data-ttu-id="3a555-107">ServiceTimeoutsBehavior 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="3a555-107">The ServiceTimeoutsBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="3a555-108">属性</span><span class="sxs-lookup"><span data-stu-id="3a555-108">Properties</span></span>  

 <span data-ttu-id="3a555-109">ServiceTimeoutsBehavior 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="3a555-109">The ServiceTimeoutsBehavior class has the following property:</span></span>  
  
### <a name="transactiontimeout"></a><span data-ttu-id="3a555-110">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="3a555-110">TransactionTimeout</span></span>  

 <span data-ttu-id="3a555-111">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="3a555-111">Data type: datetime</span></span>  
  
 <span data-ttu-id="3a555-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3a555-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a555-113">事务必须在此期间完成的时间段。</span><span class="sxs-lookup"><span data-stu-id="3a555-113">The period within which a transaction must complete.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3a555-114">要求</span><span class="sxs-lookup"><span data-stu-id="3a555-114">Requirements</span></span>  
  
|<span data-ttu-id="3a555-115">MOF</span><span class="sxs-lookup"><span data-stu-id="3a555-115">MOF</span></span>|<span data-ttu-id="3a555-116">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="3a555-116">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="3a555-117">命名空间</span><span class="sxs-lookup"><span data-stu-id="3a555-117">Namespace</span></span>|<span data-ttu-id="3a555-118">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="3a555-118">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3a555-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="3a555-119">See also</span></span>

- <xref:System.ServiceModel.Configuration.ServiceTimeoutsElement>
