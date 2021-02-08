---
description: 了解详细信息： MsmqTransportBindingElement
title: MsmqTransportBindingElement
ms.date: 03/30/2017
ms.assetid: 1c89f073-9ed3-4025-a8c5-13535a0f526b
ms.openlocfilehash: 4b6f363d979972c6ff0a2a378906feeece2ff6b2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803147"
---
# <a name="msmqtransportbindingelement"></a><span data-ttu-id="89af7-103">MsmqTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="89af7-103">MsmqTransportBindingElement</span></span>

<span data-ttu-id="89af7-104">MsmqTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="89af7-104">MsmqTransportBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="89af7-105">语法</span><span class="sxs-lookup"><span data-stu-id="89af7-105">Syntax</span></span>  
  
```csharp
class MsmqTransportBindingElement : MsmqBindingElementBase  
{  
  sint32 MaxPoolSize;  
  string QueueTransferProtocol;  
  boolean UseActiveDirectory;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="89af7-106">方法</span><span class="sxs-lookup"><span data-stu-id="89af7-106">Methods</span></span>  

 <span data-ttu-id="89af7-107">MsmqTransportBindingElement 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="89af7-107">The MsmqTransportBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="89af7-108">属性</span><span class="sxs-lookup"><span data-stu-id="89af7-108">Properties</span></span>  

 <span data-ttu-id="89af7-109">MsmqTransportBindingElement 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="89af7-109">The MsmqTransportBindingElement class has the following properties:</span></span>  
  
### <a name="maxpoolsize"></a><span data-ttu-id="89af7-110">MaxPoolSize</span><span class="sxs-lookup"><span data-stu-id="89af7-110">MaxPoolSize</span></span>  

 <span data-ttu-id="89af7-111">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="89af7-111">Data type: sint32</span></span>  
  
 <span data-ttu-id="89af7-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="89af7-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="89af7-113">包含内部 MSMQ 消息对象的池的最大大小。</span><span class="sxs-lookup"><span data-stu-id="89af7-113">The maximum size of the pool that contains internal MSMQ message objects.</span></span>  
  
### <a name="queuetransferprotocol"></a><span data-ttu-id="89af7-114">QueueTransferProtocol</span><span class="sxs-lookup"><span data-stu-id="89af7-114">QueueTransferProtocol</span></span>  

 <span data-ttu-id="89af7-115">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="89af7-115">Data type: string</span></span>  
  
 <span data-ttu-id="89af7-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="89af7-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="89af7-117">一个枚举值，指示此绑定使用的排队通信通道传输。</span><span class="sxs-lookup"><span data-stu-id="89af7-117">An enumeration value that indicates the queued communication channel transport that this binding uses.</span></span>  
  
### <a name="useactivedirectory"></a><span data-ttu-id="89af7-118">UseActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="89af7-118">UseActiveDirectory</span></span>  

 <span data-ttu-id="89af7-119">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="89af7-119">Data type: boolean</span></span>  
  
 <span data-ttu-id="89af7-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="89af7-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="89af7-121">返回一个布尔值，该值指示是否应该使用 Active Directory 来转换队列地址。</span><span class="sxs-lookup"><span data-stu-id="89af7-121">Returns a Boolean value that indicates whether queue addresses should be converted using Active Directory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="89af7-122">要求</span><span class="sxs-lookup"><span data-stu-id="89af7-122">Requirements</span></span>  
  
|<span data-ttu-id="89af7-123">MOF</span><span class="sxs-lookup"><span data-stu-id="89af7-123">MOF</span></span>|<span data-ttu-id="89af7-124">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="89af7-124">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="89af7-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="89af7-125">Namespace</span></span>|<span data-ttu-id="89af7-126">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="89af7-126">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="89af7-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="89af7-127">See also</span></span>

- <xref:System.ServiceModel.Channels.MsmqTransportBindingElement>
