---
description: 了解详细信息： BinaryMessageEncodingBindingElement
title: BinaryMessageEncodingBindingElement
ms.date: 03/30/2017
ms.assetid: e2bb3cdd-3bbd-4bb5-85fe-570457500a66
ms.openlocfilehash: e2bc711416c61ca29a93fbf75e4e734137f2b4be
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99757873"
---
# <a name="binarymessageencodingbindingelement"></a><span data-ttu-id="0e746-103">BinaryMessageEncodingBindingElement</span><span class="sxs-lookup"><span data-stu-id="0e746-103">BinaryMessageEncodingBindingElement</span></span>

<span data-ttu-id="0e746-104">BinaryMessageEncodingBindingElement</span><span class="sxs-lookup"><span data-stu-id="0e746-104">BinaryMessageEncodingBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0e746-105">语法</span><span class="sxs-lookup"><span data-stu-id="0e746-105">Syntax</span></span>  
  
```csharp  
class BinaryMessageEncodingBindingElement : MessageEncodingBindingElement  
{  
  sint32 MaxReadPoolSize;  
  sint32 MaxSessionSize;  
  sint32 MaxWritePoolSize;  
  XmlDictionaryReaderQuotas ReaderQuotas;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="0e746-106">方法</span><span class="sxs-lookup"><span data-stu-id="0e746-106">Methods</span></span>  

 <span data-ttu-id="0e746-107">BinaryMessageEncodingBindingElement 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="0e746-107">The BinaryMessageEncodingBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="0e746-108">属性</span><span class="sxs-lookup"><span data-stu-id="0e746-108">Properties</span></span>  

 <span data-ttu-id="0e746-109">BinaryMessageEncodingBindingElement 类具有下列属性。</span><span class="sxs-lookup"><span data-stu-id="0e746-109">The BinaryMessageEncodingBindingElement class has the following properties.</span></span>  
  
## <a name="maxreadpoolsize"></a><span data-ttu-id="0e746-110">MaxReadPoolSize</span><span class="sxs-lookup"><span data-stu-id="0e746-110">MaxReadPoolSize</span></span>  

 <span data-ttu-id="0e746-111">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="0e746-111">Data type: sint32</span></span>  
  
 <span data-ttu-id="0e746-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="0e746-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="0e746-113">一个整数，指定在无需分配新读取器的情况下可以同时读取的消息数。</span><span class="sxs-lookup"><span data-stu-id="0e746-113">An integer that defines how many messages can be read simultaneously without allocating new readers.</span></span>  
  
## <a name="maxsessionsize"></a><span data-ttu-id="0e746-114">MaxSessionSize</span><span class="sxs-lookup"><span data-stu-id="0e746-114">MaxSessionSize</span></span>  

 <span data-ttu-id="0e746-115">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="0e746-115">Data type: sint32</span></span>  
  
 <span data-ttu-id="0e746-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="0e746-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="0e746-117">一个值，指定用于编码的缓冲区的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="0e746-117">A value that specifies the size, in bytes, of the buffer used for encoding.</span></span>  
  
## <a name="maxwritepoolsize"></a><span data-ttu-id="0e746-118">MaxWritePoolSize</span><span class="sxs-lookup"><span data-stu-id="0e746-118">MaxWritePoolSize</span></span>  

 <span data-ttu-id="0e746-119">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="0e746-119">Data type: sint32</span></span>  
  
 <span data-ttu-id="0e746-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="0e746-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="0e746-121">一个整数，指定在无需分配新编写器的情况下可以同时发送的消息数。</span><span class="sxs-lookup"><span data-stu-id="0e746-121">An integer that defines how many messages can be sent simultaneously without allocating new writers.</span></span>  
  
## <a name="readerquotas"></a><span data-ttu-id="0e746-122">ReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="0e746-122">ReaderQuotas</span></span>  

 <span data-ttu-id="0e746-123">数据类型：XmlDictionaryReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="0e746-123">Data type: XmlDictionaryReaderQuotas</span></span>  
  
 <span data-ttu-id="0e746-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="0e746-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="0e746-125">读取器的配额。</span><span class="sxs-lookup"><span data-stu-id="0e746-125">The quotas of the readers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0e746-126">要求</span><span class="sxs-lookup"><span data-stu-id="0e746-126">Requirements</span></span>  
  
|<span data-ttu-id="0e746-127">MOF</span><span class="sxs-lookup"><span data-stu-id="0e746-127">MOF</span></span>|<span data-ttu-id="0e746-128">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="0e746-128">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="0e746-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="0e746-129">Namespace</span></span>|<span data-ttu-id="0e746-130">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="0e746-130">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0e746-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="0e746-131">See also</span></span>

- <xref:System.ServiceModel.Channels.BinaryMessageEncodingBindingElement>
