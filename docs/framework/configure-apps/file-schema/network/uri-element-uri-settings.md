---
description: '了解详细信息： <uri> 元素 (Uri 设置) '
title: <uri> 元素（Uri 设置）
ms.date: 03/30/2017
ms.assetid: c22bab8b-477c-4ae4-8498-65ad409e0847
ms.openlocfilehash: dc30778fdf5babfb87da0e32829ed9a3ae412c2e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99740114"
---
# <a name="uri-element-uri-settings"></a><span data-ttu-id="37820-103">\<uri> 元素（Uri 设置）</span><span class="sxs-lookup"><span data-stu-id="37820-103">\<uri> Element (Uri Settings)</span></span>

<span data-ttu-id="37820-104">包含指定 .NET Framework 如何处理使用统一资源标识符 (Uri) 表示的 web 地址的设置。</span><span class="sxs-lookup"><span data-stu-id="37820-104">Contains settings that specify how the .NET Framework handles web addresses expressed using uniform resource identifiers (URIs).</span></span>  
  
[**\<configuration>**](../configuration-element.md)  
&nbsp;&nbsp;**\<uri>**  
  
## <a name="syntax"></a><span data-ttu-id="37820-105">语法</span><span class="sxs-lookup"><span data-stu-id="37820-105">Syntax</span></span>  
  
```xml  
<uri>  
</uri>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="37820-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="37820-106">Attributes and Elements</span></span>  

 <span data-ttu-id="37820-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="37820-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="37820-108">特性</span><span class="sxs-lookup"><span data-stu-id="37820-108">Attributes</span></span>  

 <span data-ttu-id="37820-109">无。</span><span class="sxs-lookup"><span data-stu-id="37820-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="37820-110">子元素</span><span class="sxs-lookup"><span data-stu-id="37820-110">Child Elements</span></span>  
  
|<span data-ttu-id="37820-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="37820-111">**Element**</span></span>|<span data-ttu-id="37820-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="37820-112">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="37820-113">idn</span><span class="sxs-lookup"><span data-stu-id="37820-113">idn</span></span>](idn-element-uri-settings.md)|<span data-ttu-id="37820-114">指定是否对域名应用国际化域名 (IDN) 分析。</span><span class="sxs-lookup"><span data-stu-id="37820-114">Specifies if Internationalized Domain Name (IDN) parsing is applied to domain names.</span></span>|  
|[<span data-ttu-id="37820-115">Iriparsing></span><span class="sxs-lookup"><span data-stu-id="37820-115">iriParsing</span></span>](iriparsing-element-uri-settings.md)|<span data-ttu-id="37820-116">指定是否将国际化资源标识符 (IRI) 分析应用到 <xref:System.Uri> ，以及是否应该应用 iri 分析规则。</span><span class="sxs-lookup"><span data-stu-id="37820-116">Specifies if International Resource Identifier (IRI) parsing is applied to <xref:System.Uri> and whether IRI parsing rules should be applied.</span></span>|  
|[<span data-ttu-id="37820-117">schemeSettings</span><span class="sxs-lookup"><span data-stu-id="37820-117">schemeSettings</span></span>](schemesettings-element-uri-settings.md)|<span data-ttu-id="37820-118">指定如何分析特定方案的 <xref:System.Uri>。</span><span class="sxs-lookup"><span data-stu-id="37820-118">Specifies how a <xref:System.Uri> will be parsed for specific schemes.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="37820-119">父元素</span><span class="sxs-lookup"><span data-stu-id="37820-119">Parent Elements</span></span>  
  
|<span data-ttu-id="37820-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="37820-120">**Element**</span></span>|<span data-ttu-id="37820-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="37820-121">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="37820-122">configuration</span><span class="sxs-lookup"><span data-stu-id="37820-122">configuration</span></span>](../configuration-element.md)|<span data-ttu-id="37820-123">包含所有命名空间的设置。</span><span class="sxs-lookup"><span data-stu-id="37820-123">Contains settings for all namespaces.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="37820-124">备注</span><span class="sxs-lookup"><span data-stu-id="37820-124">Remarks</span></span>  

 <span data-ttu-id="37820-125">`uri`元素包含 <xref:System.Uri> 由命名空间中的类使用的类的成员设置 <xref:System.Net> 。</span><span class="sxs-lookup"><span data-stu-id="37820-125">The `uri` element contains settings for members of the <xref:System.Uri> class used by classes in the <xref:System.Net> namespace.</span></span> <span data-ttu-id="37820-126">设置配置对 IRI 和 IDN 的支持。</span><span class="sxs-lookup"><span data-stu-id="37820-126">The settings configure support for IRI and IDN.</span></span>  
  
## <a name="example"></a><span data-ttu-id="37820-127">示例</span><span class="sxs-lookup"><span data-stu-id="37820-127">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="37820-128">说明</span><span class="sxs-lookup"><span data-stu-id="37820-128">Description</span></span>  

 <span data-ttu-id="37820-129">下面的示例演示类使用的配置， <xref:System.Uri> 以支持 IRI 分析和 IDN 名称。</span><span class="sxs-lookup"><span data-stu-id="37820-129">The following example shows a configuration used by the <xref:System.Uri> class to support IRI parsing and IDN names.</span></span> <span data-ttu-id="37820-130">该示例还会清除所有方案设置，然后添加对 http 方案不转义百分号编码路径分隔符的支持。</span><span class="sxs-lookup"><span data-stu-id="37820-130">The example also clears all scheme settings and then adds support for not escaping percent-encoded path delimiters for the http scheme.</span></span>  
  
### <a name="code"></a><span data-ttu-id="37820-131">代码</span><span class="sxs-lookup"><span data-stu-id="37820-131">Code</span></span>  
  
```xml  
<configuration>  
  <uri>  
    <idn enabled="All" />  
    <iriParsing enabled="true" />  
    <schemeSettings>  
      <clear/>  
      <add name="http" genericUriParserOptions="DontUnescapePathDotsAndSlashes"/>  
    </schemeSettings>  
  </uri>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="37820-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="37820-132">See also</span></span>

- [<span data-ttu-id="37820-133">网络设置架构</span><span class="sxs-lookup"><span data-stu-id="37820-133">Network Settings Schema</span></span>](index.md)
