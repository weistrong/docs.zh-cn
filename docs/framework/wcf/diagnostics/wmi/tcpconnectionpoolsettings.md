---
description: 了解详细信息： TcpConnectionPoolSettings
title: TcpConnectionPoolSettings
ms.date: 03/30/2017
ms.assetid: 19acfba3-c057-4dbc-bac7-8674d7844d83
ms.openlocfilehash: 927fcba7f94bcbfa80e06479e79bf20986a661e3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99715192"
---
# <a name="tcpconnectionpoolsettings"></a><span data-ttu-id="91688-103">TcpConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="91688-103">TcpConnectionPoolSettings</span></span>

<span data-ttu-id="91688-104">TcpConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="91688-104">TcpConnectionPoolSettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="91688-105">语法</span><span class="sxs-lookup"><span data-stu-id="91688-105">Syntax</span></span>  
  
```csharp
class TcpConnectionPoolSettings  
{  
  string GroupName;  
  datetime IdleTimeout;  
  datetime LeaseTimeout;  
  sint32 MaxOutboundConnectionsPerEndpoint;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="91688-106">方法</span><span class="sxs-lookup"><span data-stu-id="91688-106">Methods</span></span>  

 <span data-ttu-id="91688-107">TcpConnectionPoolSettings 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="91688-107">The TcpConnectionPoolSettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="91688-108">属性</span><span class="sxs-lookup"><span data-stu-id="91688-108">Properties</span></span>  

 <span data-ttu-id="91688-109">TcpConnectionPoolSettings 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="91688-109">The TcpConnectionPoolSettings class has the following properties:</span></span>  
  
### <a name="groupname"></a><span data-ttu-id="91688-110">GroupName</span><span class="sxs-lookup"><span data-stu-id="91688-110">GroupName</span></span>  

 <span data-ttu-id="91688-111">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="91688-111">Data type: string</span></span>  
  
 <span data-ttu-id="91688-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="91688-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="91688-113">绑定元素使用的连接池的组名。</span><span class="sxs-lookup"><span data-stu-id="91688-113">The group name of the connection pool used by the binding element.</span></span>  
  
### <a name="idletimeout"></a><span data-ttu-id="91688-114">IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="91688-114">IdleTimeout</span></span>  

 <span data-ttu-id="91688-115">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="91688-115">Data type: datetime</span></span>  
  
 <span data-ttu-id="91688-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="91688-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="91688-117">连接在断开前可以空闲的最长时间。</span><span class="sxs-lookup"><span data-stu-id="91688-117">The maximum time the connection can be idle before being disconnected.</span></span>  
  
### <a name="leasetimeout"></a><span data-ttu-id="91688-118">LeaseTimeout</span><span class="sxs-lookup"><span data-stu-id="91688-118">LeaseTimeout</span></span>  

 <span data-ttu-id="91688-119">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="91688-119">Data type: datetime</span></span>  
  
 <span data-ttu-id="91688-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="91688-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="91688-121">超时前完成租约操作的最大时间。</span><span class="sxs-lookup"><span data-stu-id="91688-121">The maximum time for the lease operation to complete before timing out.</span></span>  
  
### <a name="maxoutboundconnectionsperendpoint"></a><span data-ttu-id="91688-122">MaxOutboundConnectionsPerEndpoint</span><span class="sxs-lookup"><span data-stu-id="91688-122">MaxOutboundConnectionsPerEndpoint</span></span>  

 <span data-ttu-id="91688-123">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="91688-123">Data type: sint32</span></span>  
  
 <span data-ttu-id="91688-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="91688-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="91688-125">每个终结点的最大出站连接数。</span><span class="sxs-lookup"><span data-stu-id="91688-125">The maximum outbound connections for each endpoint.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="91688-126">要求</span><span class="sxs-lookup"><span data-stu-id="91688-126">Requirements</span></span>  
  
|<span data-ttu-id="91688-127">MOF</span><span class="sxs-lookup"><span data-stu-id="91688-127">MOF</span></span>|<span data-ttu-id="91688-128">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="91688-128">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="91688-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="91688-129">Namespace</span></span>|<span data-ttu-id="91688-130">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="91688-130">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="91688-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="91688-131">See also</span></span>

- <xref:System.ServiceModel.Channels.TcpConnectionPoolSettings>
