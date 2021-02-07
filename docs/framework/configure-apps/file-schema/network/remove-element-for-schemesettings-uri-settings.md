---
description: '详细了解： <remove> schemeSettings 的元素 (Uri 设置) '
title: schemeSettings 的 <remove> 元素（Uri 设置）
ms.date: 03/30/2017
ms.assetid: 4095ba51-de20-4f87-b562-018abe422c91
ms.openlocfilehash: 125a347cfcbb1393ea70032b7e1b198a1a5a4ed0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99713021"
---
# <a name="remove-element-for-schemesettings-uri-settings"></a><span data-ttu-id="960c7-103">schemeSettings 的 \<remove> 元素（Uri 设置）</span><span class="sxs-lookup"><span data-stu-id="960c7-103">\<remove> Element for schemeSettings (Uri Settings)</span></span>

<span data-ttu-id="960c7-104">删除方案名称的方案设置。</span><span class="sxs-lookup"><span data-stu-id="960c7-104">Removes a scheme setting for a scheme name.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<uri>**](uri-element-uri-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<schemeSettings>**](schemesettings-element-uri-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<remove>**

## <a name="syntax"></a><span data-ttu-id="960c7-105">语法</span><span class="sxs-lookup"><span data-stu-id="960c7-105">Syntax</span></span>  
  
```xml  
<remove
  name="http|https"
/>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="960c7-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="960c7-106">Attributes and Elements</span></span>  

 <span data-ttu-id="960c7-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="960c7-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="960c7-108">特性</span><span class="sxs-lookup"><span data-stu-id="960c7-108">Attributes</span></span>  
  
|<span data-ttu-id="960c7-109">属性</span><span class="sxs-lookup"><span data-stu-id="960c7-109">Attribute</span></span>|<span data-ttu-id="960c7-110">说明</span><span class="sxs-lookup"><span data-stu-id="960c7-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="960c7-111">name</span><span class="sxs-lookup"><span data-stu-id="960c7-111">name</span></span>|<span data-ttu-id="960c7-112">应用此设置的方案名称。</span><span class="sxs-lookup"><span data-stu-id="960c7-112">The scheme name for which this setting applies.</span></span> <span data-ttu-id="960c7-113">唯一受支持的值为 name = "http" 和 name = "https"。</span><span class="sxs-lookup"><span data-stu-id="960c7-113">The only supported values are name="http" and name="https".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="960c7-114">子元素</span><span class="sxs-lookup"><span data-stu-id="960c7-114">Child Elements</span></span>  

 <span data-ttu-id="960c7-115">无。</span><span class="sxs-lookup"><span data-stu-id="960c7-115">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="960c7-116">父元素</span><span class="sxs-lookup"><span data-stu-id="960c7-116">Parent Elements</span></span>  
  
|<span data-ttu-id="960c7-117">元素</span><span class="sxs-lookup"><span data-stu-id="960c7-117">Element</span></span>|<span data-ttu-id="960c7-118">说明</span><span class="sxs-lookup"><span data-stu-id="960c7-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="960c7-119">\<schemeSettings> 元素 (Uri 设置) </span><span class="sxs-lookup"><span data-stu-id="960c7-119">\<schemeSettings> Element (Uri Settings)</span></span>](schemesettings-element-uri-settings.md)|<span data-ttu-id="960c7-120">指定如何分析特定方案的 <xref:System.Uri>。</span><span class="sxs-lookup"><span data-stu-id="960c7-120">Specifies how a <xref:System.Uri> will be parsed for specific schemes.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="960c7-121">备注</span><span class="sxs-lookup"><span data-stu-id="960c7-121">Remarks</span></span>  

 <span data-ttu-id="960c7-122">默认情况下，在 <xref:System.Uri?displayProperty=nameWithType> 执行路径压缩之前，类会取消转义编码的路径分隔符。</span><span class="sxs-lookup"><span data-stu-id="960c7-122">By default, the <xref:System.Uri?displayProperty=nameWithType> class un-escapes percent encoded path delimiters before executing path compression.</span></span> <span data-ttu-id="960c7-123">这是作为一种安全机制实现的，针对以下攻击：</span><span class="sxs-lookup"><span data-stu-id="960c7-123">This was implemented as a security mechanism against attacks like the following:</span></span>  
  
 `http://www.contoso.com/..%2F..%2F/Windows/System32/cmd.exe?/c+dir+c:\`  
  
 <span data-ttu-id="960c7-124">如果将此 URI 向下传递到模块，而不是正确处理百分号编码字符，则可能会导致服务器执行以下命令：</span><span class="sxs-lookup"><span data-stu-id="960c7-124">If this URI gets passed down to modules not handling percent encoded characters correctly, it could result in the following command being executed by the server:</span></span>  
  
 `c:\Windows\System32\cmd.exe /c dir c:\`  
  
 <span data-ttu-id="960c7-125">出于此原因， <xref:System.Uri?displayProperty=nameWithType> 类首先取消转义路径分隔符，然后应用路径压缩。</span><span class="sxs-lookup"><span data-stu-id="960c7-125">For this reason, <xref:System.Uri?displayProperty=nameWithType> class first un-escapes path delimiters and then applies path compression.</span></span> <span data-ttu-id="960c7-126">将上述恶意 URL 传递到 <xref:System.Uri?displayProperty=nameWithType> 类构造函数的结果将生成以下 URI：</span><span class="sxs-lookup"><span data-stu-id="960c7-126">The result of passing the malicious URL above to <xref:System.Uri?displayProperty=nameWithType> class constructor results in the following URI:</span></span>  
  
 `http://www.microsoft.com/Windows/System32/cmd.exe?/c+dir+c:\`  
  
 <span data-ttu-id="960c7-127">使用特定方案的 schemeSettings 配置选项，可以将此默认行为修改为不取消转义百分号编码的路径分隔符。</span><span class="sxs-lookup"><span data-stu-id="960c7-127">This default behavior can be modified to not un-escape percent encoded path delimiters using the schemeSettings configuration option for a specific scheme.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="960c7-128">配置文件</span><span class="sxs-lookup"><span data-stu-id="960c7-128">Configuration Files</span></span>  

 <span data-ttu-id="960c7-129">此元素可在应用程序配置文件或计算机配置文件 (Machine.config) 中使用。</span><span class="sxs-lookup"><span data-stu-id="960c7-129">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="960c7-130">示例</span><span class="sxs-lookup"><span data-stu-id="960c7-130">Example</span></span>  

 <span data-ttu-id="960c7-131">下面的示例演示了类使用的配置 <xref:System.Uri> ，该配置删除了 http 方案的任何方案设置。</span><span class="sxs-lookup"><span data-stu-id="960c7-131">The following example shows a configuration used by the <xref:System.Uri> class that removes any scheme settings for the http scheme.</span></span>  
  
```xml  
<configuration>  
  <uri>  
    <schemeSettings>  
      <remove name="http"/>  
    </schemeSettings>  
  </uri>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="960c7-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="960c7-132">See also</span></span>

- <xref:System.Configuration.SchemeSettingElement?displayProperty=nameWithType>
- <xref:System.Configuration.SchemeSettingElementCollection?displayProperty=nameWithType>
- <xref:System.Configuration.UriSection?displayProperty=nameWithType>
- <xref:System.Configuration.UriSection.SchemeSettings%2A?displayProperty=nameWithType>
- <xref:System.GenericUriParserOptions?displayProperty=nameWithType>
- <xref:System.Uri?displayProperty=nameWithType>
- [<span data-ttu-id="960c7-133">网络设置架构</span><span class="sxs-lookup"><span data-stu-id="960c7-133">Network Settings Schema</span></span>](index.md)
