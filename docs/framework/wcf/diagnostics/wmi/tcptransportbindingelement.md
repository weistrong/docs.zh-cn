---
description: 了解详细信息： TcpTransportBindingElement
title: TcpTransportBindingElement
ms.date: 03/30/2017
ms.assetid: 33bbc1e5-44e4-4ee3-b7b5-801dc78956e4
ms.openlocfilehash: b52bb2eb4b40648808459f76e068a6f72f9476a4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99715140"
---
# <a name="tcptransportbindingelement"></a><span data-ttu-id="c5ba5-103">TcpTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="c5ba5-103">TcpTransportBindingElement</span></span>

<span data-ttu-id="c5ba5-104">TcpTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="c5ba5-104">TcpTransportBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c5ba5-105">语法</span><span class="sxs-lookup"><span data-stu-id="c5ba5-105">Syntax</span></span>  
  
```csharp
class TcpTransportBindingElement : ConnectionOrientedTransportBindingElement  
{  
  TcpConnectionPoolSettings ConnectionPoolSettings;  
  sint32 ListenBacklog;  
  boolean PortSharingEnabled;  
  boolean TeredoEnabled;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="c5ba5-106">方法</span><span class="sxs-lookup"><span data-stu-id="c5ba5-106">Methods</span></span>  

 <span data-ttu-id="c5ba5-107">TcpTransportBindingElement 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="c5ba5-107">The TcpTransportBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="c5ba5-108">属性</span><span class="sxs-lookup"><span data-stu-id="c5ba5-108">Properties</span></span>  

 <span data-ttu-id="c5ba5-109">TcpTransportBindingElement 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="c5ba5-109">The TcpTransportBindingElement class has the following properties:</span></span>  
  
### <a name="connectionpoolsettings"></a><span data-ttu-id="c5ba5-110">ConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="c5ba5-110">ConnectionPoolSettings</span></span>  

 <span data-ttu-id="c5ba5-111">数据类型：TcpConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="c5ba5-111">Data type: TcpConnectionPoolSettings</span></span>  
  
 <span data-ttu-id="c5ba5-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="c5ba5-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c5ba5-113">连接池设置。</span><span class="sxs-lookup"><span data-stu-id="c5ba5-113">The connection pool settings.</span></span>  
  
### <a name="listenbacklog"></a><span data-ttu-id="c5ba5-114">ListenBacklog</span><span class="sxs-lookup"><span data-stu-id="c5ba5-114">ListenBacklog</span></span>  

 <span data-ttu-id="c5ba5-115">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="c5ba5-115">Data type: sint32</span></span>  
  
 <span data-ttu-id="c5ba5-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="c5ba5-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c5ba5-117">可挂起的最大排队连接请求数。</span><span class="sxs-lookup"><span data-stu-id="c5ba5-117">The maximum number of queued connection requests that can be pending.</span></span>  
  
### <a name="portsharingenabled"></a><span data-ttu-id="c5ba5-118">PortSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="c5ba5-118">PortSharingEnabled</span></span>  

 <span data-ttu-id="c5ba5-119">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="c5ba5-119">Data type: boolean</span></span>  
  
 <span data-ttu-id="c5ba5-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="c5ba5-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c5ba5-121">一个布尔值，指定是否为此连接启用 TCP 端口共享。</span><span class="sxs-lookup"><span data-stu-id="c5ba5-121">A boolean value that specifies whether TCP port sharing is enabled for this connection.</span></span>  
  
### <a name="teredoenabled"></a><span data-ttu-id="c5ba5-122">TeredoEnabled</span><span class="sxs-lookup"><span data-stu-id="c5ba5-122">TeredoEnabled</span></span>  

 <span data-ttu-id="c5ba5-123">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="c5ba5-123">Data type: boolean</span></span>  
  
 <span data-ttu-id="c5ba5-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="c5ba5-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c5ba5-125">一个布尔值，指定是否启用 Teredo（一种用于对防火墙后的客户端进行寻址的技术）。</span><span class="sxs-lookup"><span data-stu-id="c5ba5-125">A boolean value that specifies whether Teredo (a technology for addressing clients that are behind firewalls) is enabled.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c5ba5-126">要求</span><span class="sxs-lookup"><span data-stu-id="c5ba5-126">Requirements</span></span>  
  
|<span data-ttu-id="c5ba5-127">MOF</span><span class="sxs-lookup"><span data-stu-id="c5ba5-127">MOF</span></span>|<span data-ttu-id="c5ba5-128">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="c5ba5-128">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="c5ba5-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="c5ba5-129">Namespace</span></span>|<span data-ttu-id="c5ba5-130">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="c5ba5-130">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c5ba5-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="c5ba5-131">See also</span></span>

- <xref:System.ServiceModel.Channels.TcpTransportBindingElement>
