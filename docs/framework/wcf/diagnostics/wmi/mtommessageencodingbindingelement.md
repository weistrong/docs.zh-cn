---
description: 了解详细信息： MtomMessageEncodingBindingElement
title: MtomMessageEncodingBindingElement
ms.date: 03/30/2017
ms.assetid: 4a9c6c3d-e561-4b2d-a693-7e84bdd3534a
ms.openlocfilehash: f06e3d7266c4f7e6f9b4639f7d82941cbabb5dd3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803134"
---
# <a name="mtommessageencodingbindingelement"></a><span data-ttu-id="31043-103">MtomMessageEncodingBindingElement</span><span class="sxs-lookup"><span data-stu-id="31043-103">MtomMessageEncodingBindingElement</span></span>

<span data-ttu-id="31043-104">MtomMessageEncodingBindingElement</span><span class="sxs-lookup"><span data-stu-id="31043-104">MtomMessageEncodingBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="31043-105">语法</span><span class="sxs-lookup"><span data-stu-id="31043-105">Syntax</span></span>  
  
```csharp
class MtomMessageEncodingBindingElement : MessageEncodingBindingElement  
{  
  string Encoding;  
  sint32 MaxReadPoolSize;  
  sint32 MaxWritePoolSize;  
  XmlDictionaryReaderQuotas ReaderQuotas;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="31043-106">方法</span><span class="sxs-lookup"><span data-stu-id="31043-106">Methods</span></span>  

 <span data-ttu-id="31043-107">MtomMessageEncodingBindingElement 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="31043-107">The MtomMessageEncodingBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="31043-108">属性</span><span class="sxs-lookup"><span data-stu-id="31043-108">Properties</span></span>  

 <span data-ttu-id="31043-109">MtomMessageEncodingBindingElement 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="31043-109">The MtomMessageEncodingBindingElement class has the following properties:</span></span>  
  
### <a name="encoding"></a><span data-ttu-id="31043-110">编码</span><span class="sxs-lookup"><span data-stu-id="31043-110">Encoding</span></span>  

 <span data-ttu-id="31043-111">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="31043-111">Data type: string</span></span>  
  
 <span data-ttu-id="31043-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="31043-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="31043-113">要用来在绑定上发出消息的字符集编码。</span><span class="sxs-lookup"><span data-stu-id="31043-113">The character set encoding to be used for emitting messages on the binding.</span></span>  
  
### <a name="maxreadpoolsize"></a><span data-ttu-id="31043-114">MaxReadPoolSize</span><span class="sxs-lookup"><span data-stu-id="31043-114">MaxReadPoolSize</span></span>  

 <span data-ttu-id="31043-115">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="31043-115">Data type: sint32</span></span>  
  
 <span data-ttu-id="31043-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="31043-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="31043-117">一个整数，指定在无需分配新读取器的情况下可以同时读取的消息数。</span><span class="sxs-lookup"><span data-stu-id="31043-117">An integer that defines how many messages can be read simultaneously without allocating new readers.</span></span>  
  
### <a name="maxwritepoolsize"></a><span data-ttu-id="31043-118">MaxWritePoolSize</span><span class="sxs-lookup"><span data-stu-id="31043-118">MaxWritePoolSize</span></span>  

 <span data-ttu-id="31043-119">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="31043-119">Data type: sint32</span></span>  
  
 <span data-ttu-id="31043-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="31043-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="31043-121">一个整数，指定在无需分配新编写器的情况下可以同时发送的消息数。</span><span class="sxs-lookup"><span data-stu-id="31043-121">An integer that defines how many messages can be sent simultaneously without allocating new writers.</span></span>  
  
### <a name="readerquotas"></a><span data-ttu-id="31043-122">ReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="31043-122">ReaderQuotas</span></span>  

 <span data-ttu-id="31043-123">数据类型：XmlDictionaryReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="31043-123">Data type: XmlDictionaryReaderQuotas</span></span>  
  
 <span data-ttu-id="31043-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="31043-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="31043-125">读取器的配额。</span><span class="sxs-lookup"><span data-stu-id="31043-125">The quotas of the readers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="31043-126">要求</span><span class="sxs-lookup"><span data-stu-id="31043-126">Requirements</span></span>  
  
|<span data-ttu-id="31043-127">MOF</span><span class="sxs-lookup"><span data-stu-id="31043-127">MOF</span></span>|<span data-ttu-id="31043-128">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="31043-128">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="31043-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="31043-129">Namespace</span></span>|<span data-ttu-id="31043-130">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="31043-130">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="31043-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="31043-131">See also</span></span>

- <xref:System.ServiceModel.Channels.MtomMessageEncodingBindingElement>
