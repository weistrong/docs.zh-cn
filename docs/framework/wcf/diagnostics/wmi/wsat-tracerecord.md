---
description: 了解详细信息： WSAT_TraceRecord
title: WSAT_TraceRecord
ms.date: 03/30/2017
ms.assetid: 99bc7f66-1335-40d8-aa68-e754d569dc0d
ms.openlocfilehash: 67202c5d2910783c40b934d2da6108e6b514a728
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99756872"
---
# <a name="wsat_tracerecord"></a><span data-ttu-id="6cf36-103">WSAT_TraceRecord</span><span class="sxs-lookup"><span data-stu-id="6cf36-103">WSAT_TraceRecord</span></span>

<span data-ttu-id="6cf36-104">WSAT_TraceRecord</span><span class="sxs-lookup"><span data-stu-id="6cf36-104">WSAT_TraceRecord</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6cf36-105">语法</span><span class="sxs-lookup"><span data-stu-id="6cf36-105">Syntax</span></span>  
  
```csharp
class WSAT_TraceRecord : WSAT_TraceEvent  
{  
  object ActivityID;  
  sint32 EventID;  
  string TraceRecord;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="6cf36-106">方法</span><span class="sxs-lookup"><span data-stu-id="6cf36-106">Methods</span></span>  

 <span data-ttu-id="6cf36-107">WSAT_TraceRecord 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="6cf36-107">The WSAT_TraceRecord class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="6cf36-108">属性</span><span class="sxs-lookup"><span data-stu-id="6cf36-108">Properties</span></span>  

 <span data-ttu-id="6cf36-109">WSAT_TraceRecord 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="6cf36-109">The WSAT_TraceRecord class has the following properties:</span></span>  
  
### <a name="activityid"></a><span data-ttu-id="6cf36-110">ActivityID</span><span class="sxs-lookup"><span data-stu-id="6cf36-110">ActivityID</span></span>  

 <span data-ttu-id="6cf36-111">数据类型：object</span><span class="sxs-lookup"><span data-stu-id="6cf36-111">Data type: object</span></span>  
<span data-ttu-id="6cf36-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="6cf36-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6cf36-113">跟踪记录的活动 ID。</span><span class="sxs-lookup"><span data-stu-id="6cf36-113">The activity ID of the trace record.</span></span>  
  
### <a name="eventid"></a><span data-ttu-id="6cf36-114">EventID</span><span class="sxs-lookup"><span data-stu-id="6cf36-114">EventID</span></span>  

 <span data-ttu-id="6cf36-115">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="6cf36-115">Data type: sint32</span></span>  
<span data-ttu-id="6cf36-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="6cf36-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6cf36-117">跟踪记录的事件 ID。</span><span class="sxs-lookup"><span data-stu-id="6cf36-117">The event ID of the trace record.</span></span>  
  
### <a name="tracerecord"></a><span data-ttu-id="6cf36-118">TraceRecord</span><span class="sxs-lookup"><span data-stu-id="6cf36-118">TraceRecord</span></span>  

 <span data-ttu-id="6cf36-119">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="6cf36-119">Data type: string</span></span>  
<span data-ttu-id="6cf36-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="6cf36-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6cf36-121">跟踪记录</span><span class="sxs-lookup"><span data-stu-id="6cf36-121">Trace Record</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6cf36-122">要求</span><span class="sxs-lookup"><span data-stu-id="6cf36-122">Requirements</span></span>  
  
|<span data-ttu-id="6cf36-123">MOF</span><span class="sxs-lookup"><span data-stu-id="6cf36-123">MOF</span></span>|<span data-ttu-id="6cf36-124">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="6cf36-124">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="6cf36-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="6cf36-125">Namespace</span></span>|<span data-ttu-id="6cf36-126">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="6cf36-126">Defined in root\ServiceModel</span></span>|
