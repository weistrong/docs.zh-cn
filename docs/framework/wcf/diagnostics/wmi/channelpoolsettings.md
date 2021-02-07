---
description: 了解详细信息： ChannelPoolSettings
title: ChannelPoolSettings
ms.date: 03/30/2017
ms.assetid: d3f475bd-f780-4bbe-b291-339387322964
ms.openlocfilehash: b08c5483e7a0c918393795b4608b9eef16b18341
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99757678"
---
# <a name="channelpoolsettings"></a><span data-ttu-id="f93d2-103">ChannelPoolSettings</span><span class="sxs-lookup"><span data-stu-id="f93d2-103">ChannelPoolSettings</span></span>

<span data-ttu-id="f93d2-104">ChannelPoolSettings</span><span class="sxs-lookup"><span data-stu-id="f93d2-104">ChannelPoolSettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f93d2-105">语法</span><span class="sxs-lookup"><span data-stu-id="f93d2-105">Syntax</span></span>  
  
```csharp
class ChannelPoolSettings  
{  
  datetime IdleTimeout;  
  datetime LeaseTimeout;  
  sint32 MaxOutboundChannelsPerEndpoint;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="f93d2-106">方法</span><span class="sxs-lookup"><span data-stu-id="f93d2-106">Methods</span></span>  

 <span data-ttu-id="f93d2-107">ChannelPoolSettings 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="f93d2-107">The ChannelPoolSettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="f93d2-108">属性</span><span class="sxs-lookup"><span data-stu-id="f93d2-108">Properties</span></span>  

 <span data-ttu-id="f93d2-109">ChannelPoolSettings 类具有下列属性：</span><span class="sxs-lookup"><span data-stu-id="f93d2-109">The ChannelPoolSettings class has the following properties:</span></span>  
  
### <a name="idletimeout"></a><span data-ttu-id="f93d2-110">IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="f93d2-110">IdleTimeout</span></span>  

 <span data-ttu-id="f93d2-111">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="f93d2-111">Data type: datetime</span></span>  
  
 <span data-ttu-id="f93d2-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="f93d2-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f93d2-113">连接在断开前可以空闲的最长时间。</span><span class="sxs-lookup"><span data-stu-id="f93d2-113">The maximum time the connection can be idle before being disconnected.</span></span>  
  
### <a name="leasetimeout"></a><span data-ttu-id="f93d2-114">LeaseTimeout</span><span class="sxs-lookup"><span data-stu-id="f93d2-114">LeaseTimeout</span></span>  

 <span data-ttu-id="f93d2-115">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="f93d2-115">Data type: datetime</span></span>  
  
 <span data-ttu-id="f93d2-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="f93d2-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f93d2-117">超时前完成租约操作的最大时间。</span><span class="sxs-lookup"><span data-stu-id="f93d2-117">The maximum time for a lease operation to complete before timing out.</span></span>  
  
### <a name="maxoutboundchannelsperendpoint"></a><span data-ttu-id="f93d2-118">MaxOutboundChannelsPerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f93d2-118">MaxOutboundChannelsPerEndpoint</span></span>  

 <span data-ttu-id="f93d2-119">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="f93d2-119">Data type: sint32</span></span>  
  
 <span data-ttu-id="f93d2-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="f93d2-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f93d2-121">每个终结点的最大出站通道数。</span><span class="sxs-lookup"><span data-stu-id="f93d2-121">The maximum number of outbound channels for each endpoint.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f93d2-122">要求</span><span class="sxs-lookup"><span data-stu-id="f93d2-122">Requirements</span></span>  
  
|<span data-ttu-id="f93d2-123">MOF</span><span class="sxs-lookup"><span data-stu-id="f93d2-123">MOF</span></span>|<span data-ttu-id="f93d2-124">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="f93d2-124">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="f93d2-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="f93d2-125">Namespace</span></span>|<span data-ttu-id="f93d2-126">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="f93d2-126">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f93d2-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="f93d2-127">See also</span></span>

- <xref:System.ServiceModel.Channels.ChannelPoolSettings>
