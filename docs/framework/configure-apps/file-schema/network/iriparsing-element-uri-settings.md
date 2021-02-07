---
description: '了解详细信息： <iriParsing> 元素 (Uri 设置) '
title: <iriParsing> 元素（Uri 设置）
ms.date: 03/30/2017
ms.assetid: 953d0b53-445e-41f9-b302-77c4030852ce
ms.openlocfilehash: 460216b64056cd9c9f769c5bcd1b651d249e98b4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99740296"
---
# <a name="iriparsing-element-uri-settings"></a><span data-ttu-id="d3069-103">\<iriParsing> 元素（Uri 设置）</span><span class="sxs-lookup"><span data-stu-id="d3069-103">\<iriParsing> Element (Uri Settings)</span></span>

<span data-ttu-id="d3069-104">指定是否对 <xref:System.Uri> 应用国际资源标识符 (IRI) 分析以及是否应该应用 IRI 分析规则。</span><span class="sxs-lookup"><span data-stu-id="d3069-104">Specifies if International Resource Identifier (IRI) parsing is applied to a <xref:System.Uri> and whether IRI parsing rules should be applied.</span></span>  
  
[**\<configuration>**](../configuration-element.md)  
&nbsp;&nbsp;[**\<uri>**](uri-element-uri-settings.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<iriParsing>**  
  
## <a name="syntax"></a><span data-ttu-id="d3069-105">语法</span><span class="sxs-lookup"><span data-stu-id="d3069-105">Syntax</span></span>  
  
```xml  
<iriParsing  
  enabled="true|false"  
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d3069-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="d3069-106">Attributes and Elements</span></span>  

 <span data-ttu-id="d3069-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d3069-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d3069-108">特性</span><span class="sxs-lookup"><span data-stu-id="d3069-108">Attributes</span></span>  
  
|<span data-ttu-id="d3069-109">**元素**</span><span class="sxs-lookup"><span data-stu-id="d3069-109">**Element**</span></span>|<span data-ttu-id="d3069-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="d3069-110">**Description**</span></span>|  
|-----------------|---------------------|  
|`enabled`|<span data-ttu-id="d3069-111">指定是否启用 IRI 分析。</span><span class="sxs-lookup"><span data-stu-id="d3069-111">Specifies whether IRI parsing is enabled.</span></span> <span data-ttu-id="d3069-112">默认值是 `false`。</span><span class="sxs-lookup"><span data-stu-id="d3069-112">The default value is `false`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d3069-113">子元素</span><span class="sxs-lookup"><span data-stu-id="d3069-113">Child Elements</span></span>  

 <span data-ttu-id="d3069-114">无</span><span class="sxs-lookup"><span data-stu-id="d3069-114">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="d3069-115">父元素</span><span class="sxs-lookup"><span data-stu-id="d3069-115">Parent Elements</span></span>  
  
|<span data-ttu-id="d3069-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="d3069-116">**Element**</span></span>|<span data-ttu-id="d3069-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="d3069-117">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="d3069-118">uri</span><span class="sxs-lookup"><span data-stu-id="d3069-118">uri</span></span>](uri-element-uri-settings.md)|<span data-ttu-id="d3069-119">包含指定 .NET Framework 如何处理使用统一资源标识符 (Uri) 表示的 web 地址的设置。</span><span class="sxs-lookup"><span data-stu-id="d3069-119">Contains settings that specify how the .NET Framework handles web addresses expressed using uniform resource identifiers (URIs).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d3069-120">备注</span><span class="sxs-lookup"><span data-stu-id="d3069-120">Remarks</span></span>  

 <span data-ttu-id="d3069-121">已 <xref:System.Uri> 在 .NET Framework 3.5 中扩展了现有的类。</span><span class="sxs-lookup"><span data-stu-id="d3069-121">The existing <xref:System.Uri> class has been extended in .NET Framework 3.5.</span></span> <span data-ttu-id="d3069-122">3.0 SP1 和 2.0 SP1， (IRI) 和国际化域名 (IDN) 提供对国际资源标识符的支持。</span><span class="sxs-lookup"><span data-stu-id="d3069-122">3.0 SP1, and 2.0 SP1 to provide support for International Resource Identifiers (IRI) and Internationalized Domain Names (IDN).</span></span> <span data-ttu-id="d3069-123">当前用户将看不到 .NET Framework 2.0 行为中的任何更改，除非它们专门启用 IRI 和 IDN 支持。</span><span class="sxs-lookup"><span data-stu-id="d3069-123">Current users will not see any change from the .NET Framework 2.0 behavior unless they specifically enable IRI and IDN support.</span></span> <span data-ttu-id="d3069-124">这确保了 NET Framework 以前版本的应用程序兼容性。</span><span class="sxs-lookup"><span data-stu-id="d3069-124">This ensures application compatibility with prior versions of the .NET Framework.</span></span>  
  
 <span data-ttu-id="d3069-125">若要启用对 IRI 的支持，需要以下两项更改：</span><span class="sxs-lookup"><span data-stu-id="d3069-125">To enable support for IRI, the following two changes are required:</span></span>  
  
1. <span data-ttu-id="d3069-126">将以下行添加到 .NET Framework 2.0 目录下的 machine.config 文件</span><span class="sxs-lookup"><span data-stu-id="d3069-126">Add the following line to the machine.config file under the .NET Framework 2.0 directory</span></span>  
  
    ```xml  
    <section name="uri" type="System.Configuration.UriSection, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
    ```  
  
2. <span data-ttu-id="d3069-127">指定是否应该应用 IRI 分析规则。</span><span class="sxs-lookup"><span data-stu-id="d3069-127">Specify whether IRI parsing rules should be applied.</span></span> <span data-ttu-id="d3069-128">这可以在 machine.config 或应用配置文件中完成。</span><span class="sxs-lookup"><span data-stu-id="d3069-128">This can be done in the machine.config or in the app.config file.</span></span>  
  
 <span data-ttu-id="d3069-129">启用 IRI 分析 (Iriparsing> enabled = `true`) 将根据 RFC 3987 中的最新 IRI 规则执行规范化和字符检查。</span><span class="sxs-lookup"><span data-stu-id="d3069-129">Enabling IRI parsing (iriParsing enabled = `true`) will do normalization and character checking according to the latest IRI rules in RFC 3987.</span></span> <span data-ttu-id="d3069-130">默认值为 `false` ，将根据 rfc 2396 和 rfc 3986 (为 IPv6 文本) 执行规范化和字符检查。</span><span class="sxs-lookup"><span data-stu-id="d3069-130">The default value is `false` and will do normalization and character checking according to RFC 2396 and RFC 3986 (for IPv6 literals).</span></span>  
  
### <a name="configuration-files"></a><span data-ttu-id="d3069-131">配置文件</span><span class="sxs-lookup"><span data-stu-id="d3069-131">Configuration Files</span></span>  

 <span data-ttu-id="d3069-132">此元素可在应用程序配置文件或计算机配置文件 (Machine.config) 中使用。</span><span class="sxs-lookup"><span data-stu-id="d3069-132">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="d3069-133">示例</span><span class="sxs-lookup"><span data-stu-id="d3069-133">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="d3069-134">说明</span><span class="sxs-lookup"><span data-stu-id="d3069-134">Description</span></span>  

 <span data-ttu-id="d3069-135">下面的示例演示类使用的配置， <xref:System.Uri> 以支持 IRI 分析和 IDN 名称。</span><span class="sxs-lookup"><span data-stu-id="d3069-135">The following example shows a configuration used by the <xref:System.Uri> class to support IRI parsing and IDN names.</span></span>  
  
### <a name="code"></a><span data-ttu-id="d3069-136">代码</span><span class="sxs-lookup"><span data-stu-id="d3069-136">Code</span></span>  
  
```xml  
<configuration>  
  <uri>  
    <idn enabled="All" />  
    <iriParsing enabled="true" />  
  </uri>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="d3069-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="d3069-137">See also</span></span>

- <xref:System.Configuration.IriParsingElement?displayProperty=nameWithType>
- <xref:System.Configuration.UriSection?displayProperty=nameWithType>
- [<span data-ttu-id="d3069-138">网络设置架构</span><span class="sxs-lookup"><span data-stu-id="d3069-138">Network Settings Schema</span></span>](index.md)
