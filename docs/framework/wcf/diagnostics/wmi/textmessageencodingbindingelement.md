---
description: 了解详细信息： TextMessageEncodingBindingElement
title: TextMessageEncodingBindingElement
ms.date: 03/30/2017
ms.assetid: 885e2d7a-3436-4093-bc5f-0a404c62acdc
ms.openlocfilehash: 9848f1660642f92c4bce3542fbd404f463b8c84d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99757340"
---
# <a name="textmessageencodingbindingelement"></a><span data-ttu-id="87404-103">TextMessageEncodingBindingElement</span><span class="sxs-lookup"><span data-stu-id="87404-103">TextMessageEncodingBindingElement</span></span>

<span data-ttu-id="87404-104">TextMessageEncodingBindingElement</span><span class="sxs-lookup"><span data-stu-id="87404-104">TextMessageEncodingBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="87404-105">语法</span><span class="sxs-lookup"><span data-stu-id="87404-105">Syntax</span></span>  
  
```csharp
class TextMessageEncodingBindingElement : MessageEncodingBindingElement  
{  
  string Encoding;  
  sint32 MaxReadPoolSize;  
  sint32 MaxWritePoolSize;  
  XmlDictionaryReaderQuotas ReaderQuotas;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="87404-106">方法</span><span class="sxs-lookup"><span data-stu-id="87404-106">Methods</span></span>  

 <span data-ttu-id="87404-107">TextMessageEncodingBindingElement 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="87404-107">The TextMessageEncodingBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="87404-108">属性</span><span class="sxs-lookup"><span data-stu-id="87404-108">Properties</span></span>  

 <span data-ttu-id="87404-109">TextMessageEncodingBindingElement 类具有下列属性：</span><span class="sxs-lookup"><span data-stu-id="87404-109">The TextMessageEncodingBindingElement class has the following properties:</span></span>  
  
### <a name="encoding"></a><span data-ttu-id="87404-110">编码</span><span class="sxs-lookup"><span data-stu-id="87404-110">Encoding</span></span>  

 <span data-ttu-id="87404-111">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="87404-111">Data type: string</span></span>  
  
 <span data-ttu-id="87404-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="87404-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="87404-113">要用来在绑定上发出消息的字符集编码。</span><span class="sxs-lookup"><span data-stu-id="87404-113">The character set encoding to be used for emitting messages on the binding.</span></span>  
  
### <a name="maxreadpoolsize"></a><span data-ttu-id="87404-114">MaxReadPoolSize</span><span class="sxs-lookup"><span data-stu-id="87404-114">MaxReadPoolSize</span></span>  

 <span data-ttu-id="87404-115">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="87404-115">Data type: sint32</span></span>  
  
 <span data-ttu-id="87404-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="87404-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="87404-117">一个整数，指定在无需分配新读取器的情况下可以同时读取的消息数。</span><span class="sxs-lookup"><span data-stu-id="87404-117">An integer that defines how many messages can be read simultaneously without allocating new readers.</span></span>  
  
### <a name="maxwritepoolsize"></a><span data-ttu-id="87404-118">MaxWritePoolSize</span><span class="sxs-lookup"><span data-stu-id="87404-118">MaxWritePoolSize</span></span>  

 <span data-ttu-id="87404-119">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="87404-119">Data type: sint32</span></span>  
  
 <span data-ttu-id="87404-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="87404-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="87404-121">一个整数，指定在无需分配新编写器的情况下可以同时发送的消息数。</span><span class="sxs-lookup"><span data-stu-id="87404-121">An integer that defines how many messages can be sent simultaneously without allocating new writers.</span></span>  
  
### <a name="readerquotas"></a><span data-ttu-id="87404-122">ReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="87404-122">ReaderQuotas</span></span>  

 <span data-ttu-id="87404-123">数据类型：XmlDictionaryReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="87404-123">Data type: XmlDictionaryReaderQuotas</span></span>  
  
 <span data-ttu-id="87404-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="87404-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="87404-125">读取器的配额。</span><span class="sxs-lookup"><span data-stu-id="87404-125">The quotas of the readers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="87404-126">要求</span><span class="sxs-lookup"><span data-stu-id="87404-126">Requirements</span></span>  
  
|<span data-ttu-id="87404-127">MOF</span><span class="sxs-lookup"><span data-stu-id="87404-127">MOF</span></span>|<span data-ttu-id="87404-128">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="87404-128">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="87404-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="87404-129">Namespace</span></span>|<span data-ttu-id="87404-130">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="87404-130">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="87404-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="87404-131">See also</span></span>

- <xref:System.ServiceModel.Channels.TextMessageEncodingBindingElement>
