---
description: 了解有关： TransportBindingElement 的详细信息
title: TransportBindingElement
ms.date: 03/30/2017
ms.assetid: 54ecfbee-53c0-410c-a7fa-a98f2e40c545
ms.openlocfilehash: de08feaf8abec3a0dfee97e92d68d5223cd0de44
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99757106"
---
# <a name="transportbindingelement"></a><span data-ttu-id="8bc3a-103">TransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="8bc3a-103">TransportBindingElement</span></span>

<span data-ttu-id="8bc3a-104">TransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="8bc3a-104">TransportBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8bc3a-105">语法</span><span class="sxs-lookup"><span data-stu-id="8bc3a-105">Syntax</span></span>  
  
```csharp
class TransportBindingElement : BindingElement  
{  
  boolean ManualAddressing;  
  sint64 MaxBufferPoolSize;  
  sint64 MaxReceivedMessageSize;  
  string Scheme;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="8bc3a-106">方法</span><span class="sxs-lookup"><span data-stu-id="8bc3a-106">Methods</span></span>  

 <span data-ttu-id="8bc3a-107">TransportBindingElement 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="8bc3a-107">The TransportBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="8bc3a-108">属性</span><span class="sxs-lookup"><span data-stu-id="8bc3a-108">Properties</span></span>  

 <span data-ttu-id="8bc3a-109">TransportBindingElement 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="8bc3a-109">The TransportBindingElement class has the following properties:</span></span>  
  
### <a name="manualaddressing"></a><span data-ttu-id="8bc3a-110">ManualAddressing</span><span class="sxs-lookup"><span data-stu-id="8bc3a-110">ManualAddressing</span></span>  

 <span data-ttu-id="8bc3a-111">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="8bc3a-111">Data type: boolean</span></span>  
  
 <span data-ttu-id="8bc3a-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="8bc3a-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8bc3a-113">一个布尔值，该值指定用户是否要控制消息寻址。</span><span class="sxs-lookup"><span data-stu-id="8bc3a-113">A boolean value that specifies whether the user wants to take control of message addressing.</span></span>  
  
### <a name="maxbufferpoolsize"></a><span data-ttu-id="8bc3a-114">MaxBufferPoolSize</span><span class="sxs-lookup"><span data-stu-id="8bc3a-114">MaxBufferPoolSize</span></span>  

 <span data-ttu-id="8bc3a-115">数据类型：sint64</span><span class="sxs-lookup"><span data-stu-id="8bc3a-115">Data type: sint64</span></span>  
  
 <span data-ttu-id="8bc3a-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="8bc3a-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8bc3a-117">绑定的最大缓冲池大小。</span><span class="sxs-lookup"><span data-stu-id="8bc3a-117">The maximum buffer pool size for the binding.</span></span>  
  
### <a name="maxreceivedmessagesize"></a><span data-ttu-id="8bc3a-118">MaxReceivedMessageSize</span><span class="sxs-lookup"><span data-stu-id="8bc3a-118">MaxReceivedMessageSize</span></span>  

 <span data-ttu-id="8bc3a-119">数据类型：sint64</span><span class="sxs-lookup"><span data-stu-id="8bc3a-119">Data type: sint64</span></span>  
  
 <span data-ttu-id="8bc3a-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="8bc3a-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8bc3a-121">此绑定所处理的消息的最大大小。</span><span class="sxs-lookup"><span data-stu-id="8bc3a-121">The maximum size for a message that is processed by this binding.</span></span>  
  
### <a name="scheme"></a><span data-ttu-id="8bc3a-122">Scheme</span><span class="sxs-lookup"><span data-stu-id="8bc3a-122">Scheme</span></span>  

 <span data-ttu-id="8bc3a-123">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="8bc3a-123">Data type: string</span></span>  
  
 <span data-ttu-id="8bc3a-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="8bc3a-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8bc3a-125">传输的 URI 方案。</span><span class="sxs-lookup"><span data-stu-id="8bc3a-125">The URI scheme for the transport.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8bc3a-126">要求</span><span class="sxs-lookup"><span data-stu-id="8bc3a-126">Requirements</span></span>  
  
|<span data-ttu-id="8bc3a-127">MOF</span><span class="sxs-lookup"><span data-stu-id="8bc3a-127">MOF</span></span>|<span data-ttu-id="8bc3a-128">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="8bc3a-128">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="8bc3a-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="8bc3a-129">Namespace</span></span>|<span data-ttu-id="8bc3a-130">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="8bc3a-130">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="8bc3a-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="8bc3a-131">See also</span></span>

- <xref:System.ServiceModel.Channels.TransportBindingElement>
