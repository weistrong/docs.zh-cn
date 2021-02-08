---
description: 了解详细信息： NamedPipeConnectionPoolSettings
title: NamedPipeConnectionPoolSettings
ms.date: 03/30/2017
ms.assetid: 079bccb8-54b5-4436-a43d-5567763f72ce
ms.openlocfilehash: 8d724c7a24f62a8d48797125528eb8a194ece660
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803108"
---
# <a name="namedpipeconnectionpoolsettings"></a><span data-ttu-id="64e90-103">NamedPipeConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="64e90-103">NamedPipeConnectionPoolSettings</span></span>

<span data-ttu-id="64e90-104">NamedPipeConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="64e90-104">NamedPipeConnectionPoolSettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="64e90-105">语法</span><span class="sxs-lookup"><span data-stu-id="64e90-105">Syntax</span></span>  
  
```csharp
class NamedPipeConnectionPoolSettings  
{  
  string GroupName;  
  datetime IdleTimeout;  
  sint32 MaxOutboundConnectionsPerEndpoint;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="64e90-106">方法</span><span class="sxs-lookup"><span data-stu-id="64e90-106">Methods</span></span>  

 <span data-ttu-id="64e90-107">NamedPipeConnectionPoolSettings 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="64e90-107">The NamedPipeConnectionPoolSettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="64e90-108">属性</span><span class="sxs-lookup"><span data-stu-id="64e90-108">Properties</span></span>  

 <span data-ttu-id="64e90-109">NamedPipeConnectionPoolSettings 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="64e90-109">The NamedPipeConnectionPoolSettings class has the following properties:</span></span>  
  
### <a name="groupname"></a><span data-ttu-id="64e90-110">GroupName</span><span class="sxs-lookup"><span data-stu-id="64e90-110">GroupName</span></span>  

 <span data-ttu-id="64e90-111">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="64e90-111">Data type: string</span></span>  
  
 <span data-ttu-id="64e90-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="64e90-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="64e90-113">绑定元素使用的连接池的组名。</span><span class="sxs-lookup"><span data-stu-id="64e90-113">The group name of the connection pool used by the binding element.</span></span>  
  
### <a name="idletimeout"></a><span data-ttu-id="64e90-114">IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="64e90-114">IdleTimeout</span></span>  

 <span data-ttu-id="64e90-115">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="64e90-115">Data type: datetime</span></span>  
  
 <span data-ttu-id="64e90-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="64e90-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="64e90-117">连接在断开前可以空闲的最长时间。</span><span class="sxs-lookup"><span data-stu-id="64e90-117">The maximum time the connection can be idle before being disconnected.</span></span>  
  
### <a name="maxoutboundconnectionsperendpoint"></a><span data-ttu-id="64e90-118">MaxOutboundConnectionsPerEndpoint</span><span class="sxs-lookup"><span data-stu-id="64e90-118">MaxOutboundConnectionsPerEndpoint</span></span>  

 <span data-ttu-id="64e90-119">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="64e90-119">Data type: sint32</span></span>  
  
 <span data-ttu-id="64e90-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="64e90-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="64e90-121">客户端上每个终结点的最大出站连接数。</span><span class="sxs-lookup"><span data-stu-id="64e90-121">The maximum number of outbound connections for each endpoint on the client.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="64e90-122">要求</span><span class="sxs-lookup"><span data-stu-id="64e90-122">Requirements</span></span>  
  
|<span data-ttu-id="64e90-123">MOF</span><span class="sxs-lookup"><span data-stu-id="64e90-123">MOF</span></span>|<span data-ttu-id="64e90-124">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="64e90-124">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="64e90-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="64e90-125">Namespace</span></span>|<span data-ttu-id="64e90-126">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="64e90-126">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="64e90-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="64e90-127">See also</span></span>

- <xref:System.ServiceModel.Channels.NamedPipeConnectionPoolSettings>
