---
description: 了解详细信息： Forward-Compatible 数据协定
title: 向前兼容的数据协定
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data contracts [WCF], forward compatibility
ms.assetid: 413c9044-26f8-4ecb-968c-18495ea52cd9
ms.openlocfilehash: 70256449d405290e9c32eebdc5b8e3a78b76ed56
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99793852"
---
# <a name="forward-compatible-data-contracts"></a><span data-ttu-id="b8210-103">向前兼容的数据协定</span><span class="sxs-lookup"><span data-stu-id="b8210-103">Forward-Compatible Data Contracts</span></span>

<span data-ttu-id="b8210-104">Windows Communication Foundation (WCF) 数据协定系统的一项功能是，协定可以在不间断的情况随时间发展。</span><span class="sxs-lookup"><span data-stu-id="b8210-104">A feature of the Windows Communication Foundation (WCF) data contract system is that contracts can evolve over time in nonbreaking ways.</span></span> <span data-ttu-id="b8210-105">也就是说，具有旧版本数据协定的客户端可以与具有相同数据协定的新版本的服务进行通信，或者具有新版本数据协定的客户端可以与相同数据协定的旧版本进行通信。</span><span class="sxs-lookup"><span data-stu-id="b8210-105">That is, a client with an older version of a data contract can communicate with a service with a newer version of the same data contract, or a client with a newer version of a data contract can communicate with an older version of the same data contract.</span></span> <span data-ttu-id="b8210-106">有关详细信息，请参阅 [最佳做法：数据协定版本控制](../best-practices-data-contract-versioning.md)。</span><span class="sxs-lookup"><span data-stu-id="b8210-106">For more information, see [Best Practices: Data Contract Versioning](../best-practices-data-contract-versioning.md).</span></span>  
  
 <span data-ttu-id="b8210-107">如果创建了现有数据协定的新版本，您可以根据需要来应用大多数版本管理功能。</span><span class="sxs-lookup"><span data-stu-id="b8210-107">You can apply most of the versioning features on an as-needed basis when new versions of an existing data contract are created.</span></span> <span data-ttu-id="b8210-108">但是，必须将一个版本控制功能从第一个版本内置到类型 *中，才能* 正常工作。</span><span class="sxs-lookup"><span data-stu-id="b8210-108">However, one versioning feature, *round-tripping*, must be built into the type from the first version in order to work properly.</span></span>  
  
## <a name="round-tripping"></a><span data-ttu-id="b8210-109">往返</span><span class="sxs-lookup"><span data-stu-id="b8210-109">Round-Tripping</span></span>  

 <span data-ttu-id="b8210-110">当数据从数据协定的新版本传递到旧版本，然后传递回新版本时，就发生了往返。</span><span class="sxs-lookup"><span data-stu-id="b8210-110">Round-tripping occurs when data passes from a new version to an old version and back to the new version of a data contract.</span></span> <span data-ttu-id="b8210-111">往返保证了数据不会丢失。</span><span class="sxs-lookup"><span data-stu-id="b8210-111">Round-tripping guarantees that no data is lost.</span></span> <span data-ttu-id="b8210-112">如果启用往返功能，则可以使类型向前兼容于数据协定版本管理模型所支持的任何未来更改。</span><span class="sxs-lookup"><span data-stu-id="b8210-112">Enabling round-tripping makes the type forward-compatible with any future changes supported by the data contract versioning model.</span></span>  
  
 <span data-ttu-id="b8210-113">若要对某一特定类型启用往返功能，该类型必须实现 <xref:System.Runtime.Serialization.IExtensibleDataObject> 接口。</span><span class="sxs-lookup"><span data-stu-id="b8210-113">To enable round-tripping for a particular type, the type must implement the <xref:System.Runtime.Serialization.IExtensibleDataObject> interface.</span></span> <span data-ttu-id="b8210-114">该接口包含一个属性，即 <xref:System.Runtime.Serialization.IExtensibleDataObject.ExtensionData%2A>（由 <xref:System.Runtime.Serialization.ExtensionDataObject> 类型返回）。</span><span class="sxs-lookup"><span data-stu-id="b8210-114">The interface contains one property, <xref:System.Runtime.Serialization.IExtensibleDataObject.ExtensionData%2A> (returning the <xref:System.Runtime.Serialization.ExtensionDataObject> type).</span></span> <span data-ttu-id="b8210-115">该属性存储数据协定未来版本中对当前版本未知的所有数据。</span><span class="sxs-lookup"><span data-stu-id="b8210-115">The property stores any data from future versions of the data contract that is unknown to the current version.</span></span>  
  
### <a name="example"></a><span data-ttu-id="b8210-116">示例</span><span class="sxs-lookup"><span data-stu-id="b8210-116">Example</span></span>  

 <span data-ttu-id="b8210-117">下面的数据协定不向前兼容于未来的更改。</span><span class="sxs-lookup"><span data-stu-id="b8210-117">The following data contract is not forward-compatible with future changes.</span></span>  
  
 [!code-csharp[C_DataContract#7](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_datacontract/cs/source.cs#7)]
 [!code-vb[C_DataContract#7](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_datacontract/vb/source.vb#7)]  
  
 <span data-ttu-id="b8210-118">若要使该类型兼容于未来的更改（例如添加名为“phoneNumber”的新数据成员），应实现 <xref:System.Runtime.Serialization.IExtensibleDataObject> 接口。</span><span class="sxs-lookup"><span data-stu-id="b8210-118">To make the type compatible with future changes (such as adding a new data member named "phoneNumber"), implement the <xref:System.Runtime.Serialization.IExtensibleDataObject> interface.</span></span>  
  
 [!code-csharp[C_DataContract#8](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_datacontract/cs/source.cs#8)]
 [!code-vb[C_DataContract#8](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_datacontract/vb/source.vb#8)]  
  
 <span data-ttu-id="b8210-119">在 WCF 基础结构遇到的数据不是原始数据协定的一部分时，数据存储在属性中并保留。</span><span class="sxs-lookup"><span data-stu-id="b8210-119">When the WCF infrastructure encounters data that is not part of the original data contract, the data is stored in the property and preserved.</span></span> <span data-ttu-id="b8210-120">除非是临时存储，否则不会以任何其他方式处理该数据。</span><span class="sxs-lookup"><span data-stu-id="b8210-120">It is not processed in any other way except for temporary storage.</span></span> <span data-ttu-id="b8210-121">如果对象返回到它的起始位置，则原始（未知）数据也将返回。</span><span class="sxs-lookup"><span data-stu-id="b8210-121">If the object is returned back to where it originated, the original (unknown) data is also returned.</span></span> <span data-ttu-id="b8210-122">由此，数据完成了从起始终结点又回到起始终结点的往返过程而没有丢失。</span><span class="sxs-lookup"><span data-stu-id="b8210-122">Therefore, the data has made a round trip to and from the originating endpoint without loss.</span></span> <span data-ttu-id="b8210-123">但请注意，如果起始终结点要求处理数据，则不会满足这一期望，该终结点必须以某种方式检测并调整更改。</span><span class="sxs-lookup"><span data-stu-id="b8210-123">Note, however, that if the originating endpoint required the data to be processed, that expectation is unmet, and the endpoint must somehow detect and accommodate the change.</span></span>  
  
 <span data-ttu-id="b8210-124"><xref:System.Runtime.Serialization.ExtensionDataObject> 类型不包含公共方法或属性。</span><span class="sxs-lookup"><span data-stu-id="b8210-124">The <xref:System.Runtime.Serialization.ExtensionDataObject> type contains no public methods or properties.</span></span> <span data-ttu-id="b8210-125">因此，无法直接访问存储在 <xref:System.Runtime.Serialization.IExtensibleDataObject.ExtensionData%2A> 属性内部的数据。</span><span class="sxs-lookup"><span data-stu-id="b8210-125">Thus, it is impossible to get direct access to the data stored inside the <xref:System.Runtime.Serialization.IExtensibleDataObject.ExtensionData%2A> property.</span></span>  
  
 <span data-ttu-id="b8210-126">通过在 `ignoreExtensionDataObject` 构造函数中将 `true` 设置为 <xref:System.Runtime.Serialization.DataContractSerializer>，或者在 <xref:System.ServiceModel.ServiceBehaviorAttribute.IgnoreExtensionDataObject%2A> 中将 `true` 属性设置为 <xref:System.ServiceModel.ServiceBehaviorAttribute>，可以关闭往返功能。</span><span class="sxs-lookup"><span data-stu-id="b8210-126">The round-tripping feature may be turned off, either by setting `ignoreExtensionDataObject` to `true` in the <xref:System.Runtime.Serialization.DataContractSerializer> constructor or by setting the <xref:System.ServiceModel.ServiceBehaviorAttribute.IgnoreExtensionDataObject%2A> property to `true` on the <xref:System.ServiceModel.ServiceBehaviorAttribute>.</span></span> <span data-ttu-id="b8210-127">当该功能关闭时，反序列化程序将不填充 <xref:System.Runtime.Serialization.IExtensibleDataObject.ExtensionData%2A> 属性，序列化程序也不发出该属性的内容。</span><span class="sxs-lookup"><span data-stu-id="b8210-127">When this feature is off, the deserializer will not populate the <xref:System.Runtime.Serialization.IExtensibleDataObject.ExtensionData%2A> property, and the serializer will not emit the contents of the property.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b8210-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="b8210-128">See also</span></span>

- <xref:System.Runtime.Serialization.IExtensibleDataObject>
- <xref:System.Runtime.Serialization.ExtensionDataObject>
- [<span data-ttu-id="b8210-129">数据协定版本管理</span><span class="sxs-lookup"><span data-stu-id="b8210-129">Data Contract Versioning</span></span>](data-contract-versioning.md)
- [<span data-ttu-id="b8210-130">最佳做法：数据协定版本管理</span><span class="sxs-lookup"><span data-stu-id="b8210-130">Best Practices: Data Contract Versioning</span></span>](../best-practices-data-contract-versioning.md)
