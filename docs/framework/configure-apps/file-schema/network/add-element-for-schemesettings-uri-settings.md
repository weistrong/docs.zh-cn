---
description: '详细了解： <add> schemeSettings 的元素 (Uri 设置) '
title: schemeSettings 的 <add> 元素（Uri 设置）
ms.date: 03/30/2017
ms.assetid: 594a7b3b-af23-4cfa-b616-0b2dddb1a705
ms.openlocfilehash: c372577af1c7fbfe669455b50c8b55c82da4fc52
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698613"
---
# <a name="add-element-for-schemesettings-uri-settings"></a><span data-ttu-id="8ee92-103">schemeSettings 的 \<add> 元素（Uri 设置）</span><span class="sxs-lookup"><span data-stu-id="8ee92-103">\<add> Element for schemeSettings (Uri Settings)</span></span>

<span data-ttu-id="8ee92-104">为方案名称添加方案设置。</span><span class="sxs-lookup"><span data-stu-id="8ee92-104">Adds a scheme setting for a scheme name.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<uri>**](uri-element-uri-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<schemeSettings>**](schemesettings-element-uri-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<add>**

## <a name="syntax"></a><span data-ttu-id="8ee92-105">语法</span><span class="sxs-lookup"><span data-stu-id="8ee92-105">Syntax</span></span>  
  
```xml  
<add
  name="http|https"
  genericUriParserOptions="DontUnescapePathDotsAndSlashes"
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8ee92-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="8ee92-106">Attributes and Elements</span></span>  

 <span data-ttu-id="8ee92-107">以下几节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8ee92-107">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8ee92-108">特性</span><span class="sxs-lookup"><span data-stu-id="8ee92-108">Attributes</span></span>  
  
|<span data-ttu-id="8ee92-109">属性</span><span class="sxs-lookup"><span data-stu-id="8ee92-109">Attribute</span></span>|<span data-ttu-id="8ee92-110">说明</span><span class="sxs-lookup"><span data-stu-id="8ee92-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="8ee92-111">name</span><span class="sxs-lookup"><span data-stu-id="8ee92-111">name</span></span>|<span data-ttu-id="8ee92-112">应用此设置的方案名称。</span><span class="sxs-lookup"><span data-stu-id="8ee92-112">The scheme name for which this setting applies.</span></span> <span data-ttu-id="8ee92-113">唯一受支持的值为 name = "http" 和 name = "https"。</span><span class="sxs-lookup"><span data-stu-id="8ee92-113">The only supported values are name="http" and name="https".</span></span>|  
  
## <a name="attribute-name-attribute"></a><span data-ttu-id="8ee92-114">{Attribute name}Attribute</span><span class="sxs-lookup"><span data-stu-id="8ee92-114">{Attribute name} Attribute</span></span>  
  
|<span data-ttu-id="8ee92-115">值</span><span class="sxs-lookup"><span data-stu-id="8ee92-115">Value</span></span>|<span data-ttu-id="8ee92-116">说明</span><span class="sxs-lookup"><span data-stu-id="8ee92-116">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="8ee92-117">genericUriParserOptions</span><span class="sxs-lookup"><span data-stu-id="8ee92-117">genericUriParserOptions</span></span>|<span data-ttu-id="8ee92-118">此方案的分析器选项。</span><span class="sxs-lookup"><span data-stu-id="8ee92-118">The parser options for this scheme.</span></span> <span data-ttu-id="8ee92-119">唯一受支持的值为 genericUriParserOptions = "DontUnescapePathDotsAndSlashes"。</span><span class="sxs-lookup"><span data-stu-id="8ee92-119">The only supported value is genericUriParserOptions= "DontUnescapePathDotsAndSlashes".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="8ee92-120">子元素</span><span class="sxs-lookup"><span data-stu-id="8ee92-120">Child Elements</span></span>  

 <span data-ttu-id="8ee92-121">无</span><span class="sxs-lookup"><span data-stu-id="8ee92-121">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="8ee92-122">父元素</span><span class="sxs-lookup"><span data-stu-id="8ee92-122">Parent Elements</span></span>  
  
|<span data-ttu-id="8ee92-123">元素</span><span class="sxs-lookup"><span data-stu-id="8ee92-123">Element</span></span>|<span data-ttu-id="8ee92-124">说明</span><span class="sxs-lookup"><span data-stu-id="8ee92-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8ee92-125">\<schemeSettings> 元素 (Uri 设置) </span><span class="sxs-lookup"><span data-stu-id="8ee92-125">\<schemeSettings> Element (Uri Settings)</span></span>](schemesettings-element-uri-settings.md)|<span data-ttu-id="8ee92-126">指定如何分析特定方案的 <xref:System.Uri>。</span><span class="sxs-lookup"><span data-stu-id="8ee92-126">Specifies how a <xref:System.Uri> will be parsed for specific schemes.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8ee92-127">备注</span><span class="sxs-lookup"><span data-stu-id="8ee92-127">Remarks</span></span>  

 <span data-ttu-id="8ee92-128">默认情况下，在 <xref:System.Uri?displayProperty=nameWithType> 执行路径压缩之前，类会取消转义编码的路径分隔符。</span><span class="sxs-lookup"><span data-stu-id="8ee92-128">By default, the <xref:System.Uri?displayProperty=nameWithType> class un-escapes percent encoded path delimiters before executing path compression.</span></span> <span data-ttu-id="8ee92-129">这是作为一种安全机制实现的，针对以下攻击：</span><span class="sxs-lookup"><span data-stu-id="8ee92-129">This was implemented as a security mechanism against attacks like the following:</span></span>  
  
 `http://www.contoso.com/..%2F..%2F/Windows/System32/cmd.exe?/c+dir+c:\`  
  
 <span data-ttu-id="8ee92-130">如果将此 URI 向下传递到模块，而不是正确处理百分号编码字符，则可能会导致服务器执行以下命令：</span><span class="sxs-lookup"><span data-stu-id="8ee92-130">If this URI gets passed down to modules not handling percent encoded characters correctly, it could result in the following command being executed by the server:</span></span>  
  
 `c:\Windows\System32\cmd.exe /c dir c:\`  
  
 <span data-ttu-id="8ee92-131">出于此原因， <xref:System.Uri?displayProperty=nameWithType> 类首先取消转义路径分隔符，然后应用路径压缩。</span><span class="sxs-lookup"><span data-stu-id="8ee92-131">For this reason, <xref:System.Uri?displayProperty=nameWithType> class first un-escapes path delimiters and then applies path compression.</span></span> <span data-ttu-id="8ee92-132">将上述恶意 URL 传递到 <xref:System.Uri?displayProperty=nameWithType> 类构造函数的结果将生成以下 URI：</span><span class="sxs-lookup"><span data-stu-id="8ee92-132">The result of passing the malicious URL above to <xref:System.Uri?displayProperty=nameWithType> class constructor results in the following URI:</span></span>  
  
 `http://www.microsoft.com/Windows/System32/cmd.exe?/c+dir+c:\`  
  
 <span data-ttu-id="8ee92-133">使用特定方案的 schemeSettings 配置选项，可以将此默认行为修改为不取消转义百分号编码的路径分隔符。</span><span class="sxs-lookup"><span data-stu-id="8ee92-133">This default behavior can be modified to not un-escape percent encoded path delimiters using the schemeSettings configuration option for a specific scheme.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="8ee92-134">配置文件</span><span class="sxs-lookup"><span data-stu-id="8ee92-134">Configuration Files</span></span>  

 <span data-ttu-id="8ee92-135">此元素可在应用程序配置文件或计算机配置文件 (Machine.config) 中使用。</span><span class="sxs-lookup"><span data-stu-id="8ee92-135">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="8ee92-136">示例</span><span class="sxs-lookup"><span data-stu-id="8ee92-136">Example</span></span>  

 <span data-ttu-id="8ee92-137">下面的示例演示类使用的配置 <xref:System.Uri> ，以支持不转义 http 方案的百分号编码的路径分隔符。</span><span class="sxs-lookup"><span data-stu-id="8ee92-137">The following example shows a configuration used by the <xref:System.Uri> class to support not escaping percent-encoded path delimiters for the http scheme.</span></span>  
  
```xml  
<configuration>  
  <uri>  
    <schemeSettings>  
      <add name="http" genericUriParserOptions="DontUnescapePathDotsAndSlashes"/>  
    </schemeSettings>  
  </uri>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="8ee92-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="8ee92-138">See also</span></span>

- <xref:System.Configuration.SchemeSettingElement?displayProperty=nameWithType>
- <xref:System.Configuration.SchemeSettingElementCollection?displayProperty=nameWithType>
- <xref:System.Configuration.UriSection?displayProperty=nameWithType>
- <xref:System.Configuration.UriSection.SchemeSettings%2A?displayProperty=nameWithType>
- <xref:System.GenericUriParserOptions?displayProperty=nameWithType>
- <xref:System.Uri?displayProperty=nameWithType>
- [<span data-ttu-id="8ee92-139">网络设置架构</span><span class="sxs-lookup"><span data-stu-id="8ee92-139">Network Settings Schema</span></span>](index.md)
