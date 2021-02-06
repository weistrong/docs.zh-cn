---
description: 了解详细信息： WS-MetadataExchange 绑定
title: WS-MetadataExchange 绑定
ms.date: 03/30/2017
ms.assetid: 10f8de5d-b81d-4ea7-b37e-7f2c00c39714
ms.openlocfilehash: 3bcea573ad436a85285fab5657e58defa9113d9c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99643938"
---
# <a name="ws-metadataexchange-bindings"></a><span data-ttu-id="c2bbd-103">WS-MetadataExchange 绑定</span><span class="sxs-lookup"><span data-stu-id="c2bbd-103">WS-MetadataExchange Bindings</span></span>

<span data-ttu-id="c2bbd-104">本主题说明如何为各种传输构造默认的元数据交换绑定。</span><span class="sxs-lookup"><span data-stu-id="c2bbd-104">This topic describes how the default metadata exchange bindings are constructed for various transports.</span></span>  
  
## <a name="the-default-bindings"></a><span data-ttu-id="c2bbd-105">默认绑定</span><span class="sxs-lookup"><span data-stu-id="c2bbd-105">The Default Bindings</span></span>  
  
|<span data-ttu-id="c2bbd-106">默认绑定名称</span><span class="sxs-lookup"><span data-stu-id="c2bbd-106">Default Binding Name</span></span>|<span data-ttu-id="c2bbd-107">绑定的构造方式</span><span class="sxs-lookup"><span data-stu-id="c2bbd-107">How the binding is constructed</span></span>|  
|--------------------------|------------------------------------|  
|<span data-ttu-id="c2bbd-108">mexHttpBinding</span><span class="sxs-lookup"><span data-stu-id="c2bbd-108">mexHttpBinding</span></span>|<span data-ttu-id="c2bbd-109">一个禁用传输级安全性的 <xref:System.ServiceModel.WSHttpBinding>。</span><span class="sxs-lookup"><span data-stu-id="c2bbd-109">A <xref:System.ServiceModel.WSHttpBinding> with transport-level security disabled.</span></span>|  
|<span data-ttu-id="c2bbd-110">mexHttpsBinding</span><span class="sxs-lookup"><span data-stu-id="c2bbd-110">mexHttpsBinding</span></span>|<span data-ttu-id="c2bbd-111">一个支持传输级安全性的 <xref:System.ServiceModel.WSHttpBinding>。</span><span class="sxs-lookup"><span data-stu-id="c2bbd-111">A <xref:System.ServiceModel.WSHttpBinding> that supports transport-level security.</span></span>|  
|<span data-ttu-id="c2bbd-112">mexNamedPipeBinding</span><span class="sxs-lookup"><span data-stu-id="c2bbd-112">mexNamedPipeBinding</span></span>|<span data-ttu-id="c2bbd-113">一个 <xref:System.ServiceModel.Channels.CustomBinding>，它具有使用默认值的 <xref:System.ServiceModel.Channels.NamedPipeTransportBindingElement>。</span><span class="sxs-lookup"><span data-stu-id="c2bbd-113">A  <xref:System.ServiceModel.Channels.CustomBinding> with a <xref:System.ServiceModel.Channels.NamedPipeTransportBindingElement> using the default values.</span></span>|  
|<span data-ttu-id="c2bbd-114">mexTcpBinding</span><span class="sxs-lookup"><span data-stu-id="c2bbd-114">mexTcpBinding</span></span>|<span data-ttu-id="c2bbd-115">一个 <xref:System.ServiceModel.Channels.CustomBinding>，它具有使用默认值的 <xref:System.ServiceModel.Channels.TcpTransportBindingElement>。</span><span class="sxs-lookup"><span data-stu-id="c2bbd-115">A <xref:System.ServiceModel.Channels.CustomBinding> with a <xref:System.ServiceModel.Channels.TcpTransportBindingElement> using default values.</span></span>|
