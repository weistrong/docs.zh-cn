---
description: 了解详细信息： PeerTransportBindingElement
title: PeerTransportBindingElement
ms.date: 03/30/2017
ms.assetid: 40bf6be2-8087-4cb3-a66c-408d53eb9269
ms.openlocfilehash: b1ca8020f51a5f9b121f7d238d82b9971d13cdd4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99757327"
---
# <a name="peertransportbindingelement"></a><span data-ttu-id="b1d15-103">PeerTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="b1d15-103">PeerTransportBindingElement</span></span>

<span data-ttu-id="b1d15-104">PeerTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="b1d15-104">PeerTransportBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b1d15-105">语法</span><span class="sxs-lookup"><span data-stu-id="b1d15-105">Syntax</span></span>  
  
```csharp
class PeerTransportBindingElement : TransportBindingElement  
{  
  string ListenIPAddress;  
  sint32 Port;  
  PeerSecuritySettings Security;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="b1d15-106">方法</span><span class="sxs-lookup"><span data-stu-id="b1d15-106">Methods</span></span>  

 <span data-ttu-id="b1d15-107">PeerTransportBindingElement 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="b1d15-107">The PeerTransportBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="b1d15-108">属性</span><span class="sxs-lookup"><span data-stu-id="b1d15-108">Properties</span></span>  

 <span data-ttu-id="b1d15-109">PeerTransportBindingElement 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="b1d15-109">The PeerTransportBindingElement class has the following properties:</span></span>  
  
### <a name="listenipaddress"></a><span data-ttu-id="b1d15-110">ListenIPAddress</span><span class="sxs-lookup"><span data-stu-id="b1d15-110">ListenIPAddress</span></span>  

 <span data-ttu-id="b1d15-111">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="b1d15-111">Data type: string</span></span>  
  
 <span data-ttu-id="b1d15-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="b1d15-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b1d15-113">对等节点在其上侦听消息的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="b1d15-113">The IP address on which the peer node listens for messages.</span></span>  
  
### <a name="port"></a><span data-ttu-id="b1d15-114">Port</span><span class="sxs-lookup"><span data-stu-id="b1d15-114">Port</span></span>  

 <span data-ttu-id="b1d15-115">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="b1d15-115">Data type: sint32</span></span>  
  
 <span data-ttu-id="b1d15-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="b1d15-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b1d15-117">网络接口端口，此绑定在该端口上处理对等通道消息。</span><span class="sxs-lookup"><span data-stu-id="b1d15-117">The network interface port on which this binding processes peer channel messages.</span></span>  
  
### <a name="security"></a><span data-ttu-id="b1d15-118">安全</span><span class="sxs-lookup"><span data-stu-id="b1d15-118">Security</span></span>  

 <span data-ttu-id="b1d15-119">数据类型：PeerSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="b1d15-119">Data type: PeerSecuritySettings</span></span>  
  
 <span data-ttu-id="b1d15-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="b1d15-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b1d15-121">对等传输安全设置。</span><span class="sxs-lookup"><span data-stu-id="b1d15-121">Peer transport security settings.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b1d15-122">要求</span><span class="sxs-lookup"><span data-stu-id="b1d15-122">Requirements</span></span>  
  
|<span data-ttu-id="b1d15-123">MOF</span><span class="sxs-lookup"><span data-stu-id="b1d15-123">MOF</span></span>|<span data-ttu-id="b1d15-124">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="b1d15-124">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="b1d15-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="b1d15-125">Namespace</span></span>|<span data-ttu-id="b1d15-126">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="b1d15-126">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b1d15-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="b1d15-127">See also</span></span>

- <xref:System.ServiceModel.Channels.PeerTransportBindingElement>
