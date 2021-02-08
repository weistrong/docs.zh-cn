---
description: 了解详细信息： OneWayBindingElement
title: OneWayBindingElement
ms.date: 03/30/2017
ms.assetid: 5c7e17c3-39b9-4214-ae08-9e6141734305
ms.openlocfilehash: 9c2ccc301bd854c7b85fcc53551ed6def329a8fa
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803082"
---
# <a name="onewaybindingelement"></a><span data-ttu-id="2137d-103">OneWayBindingElement</span><span class="sxs-lookup"><span data-stu-id="2137d-103">OneWayBindingElement</span></span>

<span data-ttu-id="2137d-104">OneWayBindingElement</span><span class="sxs-lookup"><span data-stu-id="2137d-104">OneWayBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2137d-105">语法</span><span class="sxs-lookup"><span data-stu-id="2137d-105">Syntax</span></span>  
  
```csharp
class OneWayBindingElement : BindingElement  
{  
  ChannelPoolSettings ChannelPoolSettings;  
  sint32 MaxAcceptedChannels;  
  boolean PacketRoutable;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="2137d-106">方法</span><span class="sxs-lookup"><span data-stu-id="2137d-106">Methods</span></span>  

 <span data-ttu-id="2137d-107">OneWayBindingElement 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="2137d-107">The OneWayBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="2137d-108">属性</span><span class="sxs-lookup"><span data-stu-id="2137d-108">Properties</span></span>  

 <span data-ttu-id="2137d-109">OneWayBindingElement 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="2137d-109">The OneWayBindingElement class has the following properties:</span></span>  
  
### <a name="channelpoolsettings"></a><span data-ttu-id="2137d-110">ChannelPoolSettings</span><span class="sxs-lookup"><span data-stu-id="2137d-110">ChannelPoolSettings</span></span>  

 <span data-ttu-id="2137d-111">数据类型：ChannelPoolSettings</span><span class="sxs-lookup"><span data-stu-id="2137d-111">Data type: ChannelPoolSettings</span></span>  
  
 <span data-ttu-id="2137d-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="2137d-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="2137d-113">通道池设置。</span><span class="sxs-lookup"><span data-stu-id="2137d-113">The channel pool settings.</span></span>  
  
### <a name="maxacceptedchannels"></a><span data-ttu-id="2137d-114">MaxAcceptedChannels</span><span class="sxs-lookup"><span data-stu-id="2137d-114">MaxAcceptedChannels</span></span>  

 <span data-ttu-id="2137d-115">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="2137d-115">Data type: sint32</span></span>  
  
 <span data-ttu-id="2137d-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="2137d-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="2137d-117">接受的最大通道数。</span><span class="sxs-lookup"><span data-stu-id="2137d-117">The maximum number of accepted channels.</span></span>  
  
### <a name="packetroutable"></a><span data-ttu-id="2137d-118">PacketRoutable</span><span class="sxs-lookup"><span data-stu-id="2137d-118">PacketRoutable</span></span>  

 <span data-ttu-id="2137d-119">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="2137d-119">Data type: boolean</span></span>  
  
 <span data-ttu-id="2137d-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="2137d-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="2137d-121">一个值，该值指示数据包是否可路由。</span><span class="sxs-lookup"><span data-stu-id="2137d-121">A value that indicates whether the packet is routable.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2137d-122">要求</span><span class="sxs-lookup"><span data-stu-id="2137d-122">Requirements</span></span>  
  
|<span data-ttu-id="2137d-123">MOF</span><span class="sxs-lookup"><span data-stu-id="2137d-123">MOF</span></span>|<span data-ttu-id="2137d-124">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="2137d-124">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="2137d-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="2137d-125">Namespace</span></span>|<span data-ttu-id="2137d-126">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="2137d-126">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="2137d-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="2137d-127">See also</span></span>

- <xref:System.ServiceModel.Channels.OneWayBindingElement>
