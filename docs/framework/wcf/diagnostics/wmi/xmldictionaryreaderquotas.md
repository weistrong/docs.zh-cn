---
description: 了解详细信息： XmlDictionaryReaderQuotas
title: XmlDictionaryReaderQuotas
ms.date: 03/30/2017
ms.assetid: 9b4ca8b4-0a89-4758-97ab-528a8ce18f07
ms.openlocfilehash: d1450051e7107e9b92f848d26e6b182bfd2f2340
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99756859"
---
# <a name="xmldictionaryreaderquotas"></a><span data-ttu-id="07f5f-103">XmlDictionaryReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="07f5f-103">XmlDictionaryReaderQuotas</span></span>

<span data-ttu-id="07f5f-104">XmlDictionaryReaderQuotas</span><span class="sxs-lookup"><span data-stu-id="07f5f-104">XmlDictionaryReaderQuotas</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="07f5f-105">语法</span><span class="sxs-lookup"><span data-stu-id="07f5f-105">Syntax</span></span>  
  
```csharp
class XmlDictionaryReaderQuotas  
{  
  sint32 MaxArrayLength;  
  sint32 MaxBytesPerRead;  
  sint32 MaxDepth;  
  sint32 MaxNameTableCharCount;  
  sint32 MaxStringContentLength;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="07f5f-106">方法</span><span class="sxs-lookup"><span data-stu-id="07f5f-106">Methods</span></span>  

 <span data-ttu-id="07f5f-107">XmlDictionaryReaderQuotas 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="07f5f-107">The XmlDictionaryReaderQuotas class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="07f5f-108">属性</span><span class="sxs-lookup"><span data-stu-id="07f5f-108">Properties</span></span>  

 <span data-ttu-id="07f5f-109">XmlDictionaryReaderQuotas 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="07f5f-109">The XmlDictionaryReaderQuotas class has the following properties:</span></span>  
  
### <a name="maxarraylength"></a><span data-ttu-id="07f5f-110">MaxArrayLength</span><span class="sxs-lookup"><span data-stu-id="07f5f-110">MaxArrayLength</span></span>  

 <span data-ttu-id="07f5f-111">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="07f5f-111">Data type: sint32</span></span>  
  
 <span data-ttu-id="07f5f-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="07f5f-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="07f5f-113">允许的最大数组长度。</span><span class="sxs-lookup"><span data-stu-id="07f5f-113">The maximum allowed array length.</span></span>  
  
### <a name="maxbytesperread"></a><span data-ttu-id="07f5f-114">MaxBytesPerRead</span><span class="sxs-lookup"><span data-stu-id="07f5f-114">MaxBytesPerRead</span></span>  

 <span data-ttu-id="07f5f-115">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="07f5f-115">Data type: sint32</span></span>  
  
 <span data-ttu-id="07f5f-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="07f5f-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="07f5f-117">允许为每次读取返回的最大字节数。</span><span class="sxs-lookup"><span data-stu-id="07f5f-117">The maximum allowed bytes returned for each read.</span></span>  
  
### <a name="maxdepth"></a><span data-ttu-id="07f5f-118">MaxDepth</span><span class="sxs-lookup"><span data-stu-id="07f5f-118">MaxDepth</span></span>  

 <span data-ttu-id="07f5f-119">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="07f5f-119">Data type: sint32</span></span>  
  
 <span data-ttu-id="07f5f-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="07f5f-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="07f5f-121">每次读取的最大嵌套节点深度。</span><span class="sxs-lookup"><span data-stu-id="07f5f-121">The maximum nested node depth for each read.</span></span>  
  
### <a name="maxnametablecharcount"></a><span data-ttu-id="07f5f-122">MaxNameTableCharCount</span><span class="sxs-lookup"><span data-stu-id="07f5f-122">MaxNameTableCharCount</span></span>  

 <span data-ttu-id="07f5f-123">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="07f5f-123">Data type: sint32</span></span>  
  
 <span data-ttu-id="07f5f-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="07f5f-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="07f5f-125">表名称中允许的最大字符数。</span><span class="sxs-lookup"><span data-stu-id="07f5f-125">The maximum characters allowed in a table name.</span></span>  
  
### <a name="maxstringcontentlength"></a><span data-ttu-id="07f5f-126">MaxStringContentLength</span><span class="sxs-lookup"><span data-stu-id="07f5f-126">MaxStringContentLength</span></span>  

 <span data-ttu-id="07f5f-127">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="07f5f-127">Data type: sint32</span></span>  
  
 <span data-ttu-id="07f5f-128">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="07f5f-128">Access type: Read-only</span></span>  
  
 <span data-ttu-id="07f5f-129">XML 元素内容中允许包含的最大字符数。</span><span class="sxs-lookup"><span data-stu-id="07f5f-129">The maximum characters allowed in XML element content.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="07f5f-130">要求</span><span class="sxs-lookup"><span data-stu-id="07f5f-130">Requirements</span></span>  
  
|<span data-ttu-id="07f5f-131">MOF</span><span class="sxs-lookup"><span data-stu-id="07f5f-131">MOF</span></span>|<span data-ttu-id="07f5f-132">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="07f5f-132">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="07f5f-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="07f5f-133">Namespace</span></span>|<span data-ttu-id="07f5f-134">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="07f5f-134">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="07f5f-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="07f5f-135">See also</span></span>

- <xref:System.Xml.XmlDictionaryReaderQuotas>
- <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>
