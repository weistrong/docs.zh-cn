---
description: 了解详细信息：信道类
title: Channel 类
ms.date: 03/30/2017
ms.assetid: d9fae2ca-209c-4341-a0f5-6b79d1a67776
ms.openlocfilehash: dcc92f78f09e9a73a24134c6c0685949f46f38dd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99757717"
---
# <a name="channel-class"></a><span data-ttu-id="f5833-103">Channel 类</span><span class="sxs-lookup"><span data-stu-id="f5833-103">Channel class</span></span>

<span data-ttu-id="f5833-104">通道</span><span class="sxs-lookup"><span data-stu-id="f5833-104">Channel</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f5833-105">语法</span><span class="sxs-lookup"><span data-stu-id="f5833-105">Syntax</span></span>  
  
```csharp
class Channel  
{  
  string LocalAddress;  
  Endpoint ref;  
  string RemoteAddress;  
  string SessionId;  
  string Type;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="f5833-106">方法</span><span class="sxs-lookup"><span data-stu-id="f5833-106">Methods</span></span>  

 <span data-ttu-id="f5833-107">Channel 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="f5833-107">The Channel class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="f5833-108">属性</span><span class="sxs-lookup"><span data-stu-id="f5833-108">Properties</span></span>  

 <span data-ttu-id="f5833-109">Channel 类具有以下属性。</span><span class="sxs-lookup"><span data-stu-id="f5833-109">The Channel class has the following properties.</span></span>  
  
### <a name="localaddress"></a><span data-ttu-id="f5833-110">LocalAddress</span><span class="sxs-lookup"><span data-stu-id="f5833-110">LocalAddress</span></span>  

 <span data-ttu-id="f5833-111">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="f5833-111">Data type: string</span></span>  
  
 <span data-ttu-id="f5833-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="f5833-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f5833-113">通道的本地终结点。</span><span class="sxs-lookup"><span data-stu-id="f5833-113">The local endpoint for the channel.</span></span>  
  
### <a name="ref"></a><span data-ttu-id="f5833-114">ref</span><span class="sxs-lookup"><span data-stu-id="f5833-114">ref</span></span>  

 <span data-ttu-id="f5833-115">数据类型：Endpoint</span><span class="sxs-lookup"><span data-stu-id="f5833-115">Data type: Endpoint</span></span>  
  
 <span data-ttu-id="f5833-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="f5833-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f5833-117">对通道所连接到的终结点的引用。</span><span class="sxs-lookup"><span data-stu-id="f5833-117">A reference to the endpoint the channel connects to.</span></span>  
  
### <a name="remoteaddress"></a><span data-ttu-id="f5833-118">RemoteAddress</span><span class="sxs-lookup"><span data-stu-id="f5833-118">RemoteAddress</span></span>  

 <span data-ttu-id="f5833-119">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="f5833-119">Data type: string</span></span>  
  
 <span data-ttu-id="f5833-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="f5833-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f5833-121">与通道相关联的远程地址。</span><span class="sxs-lookup"><span data-stu-id="f5833-121">The remote address associated with the channel.</span></span>  
  
### <a name="sessionid"></a><span data-ttu-id="f5833-122">SessionId</span><span class="sxs-lookup"><span data-stu-id="f5833-122">SessionId</span></span>  

 <span data-ttu-id="f5833-123">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="f5833-123">Data type: string</span></span>  
  
 <span data-ttu-id="f5833-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="f5833-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f5833-125">当前会话的 ID（如果有）。</span><span class="sxs-lookup"><span data-stu-id="f5833-125">The current session Id, if any.</span></span>  
  
### <a name="type"></a><span data-ttu-id="f5833-126">类型</span><span class="sxs-lookup"><span data-stu-id="f5833-126">Type</span></span>  

 <span data-ttu-id="f5833-127">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="f5833-127">Data type: string</span></span>  
  
 <span data-ttu-id="f5833-128">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="f5833-128">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f5833-129">通道的类型。</span><span class="sxs-lookup"><span data-stu-id="f5833-129">The type of the channel.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f5833-130">要求</span><span class="sxs-lookup"><span data-stu-id="f5833-130">Requirements</span></span>  
  
|<span data-ttu-id="f5833-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f5833-131">MOF</span></span>|<span data-ttu-id="f5833-132">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="f5833-132">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="f5833-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="f5833-133">Namespace</span></span>|<span data-ttu-id="f5833-134">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="f5833-134">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f5833-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="f5833-135">See also</span></span>

- <xref:System.ServiceModel.Channels.ChannelBase>
