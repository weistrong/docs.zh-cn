---
description: '了解详细信息： <schemeSettings> 元素 (Uri 设置) '
title: <schemeSettings> 元素（Uri 设置）
ms.date: 03/30/2017
ms.assetid: 0ae45c6e-8c4c-4c0d-8b9f-a93824648890
ms.openlocfilehash: 218676c10a8acaa79c2eb2146214e77beee9a972
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698435"
---
# <a name="schemesettings-element-uri-settings"></a><span data-ttu-id="05288-103">\<schemeSettings> 元素（Uri 设置）</span><span class="sxs-lookup"><span data-stu-id="05288-103">\<schemeSettings> Element (Uri Settings)</span></span>

<span data-ttu-id="05288-104">指定如何分析特定方案的 <xref:System.Uri>。</span><span class="sxs-lookup"><span data-stu-id="05288-104">Specifies how a <xref:System.Uri> will be parsed for specific schemes.</span></span>  
  
[**\<configuration>**](../configuration-element.md)  
&nbsp;&nbsp;[**\<uri>**](uri-element-uri-settings.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<schemeSettings>**  
  
## <a name="syntax"></a><span data-ttu-id="05288-105">语法</span><span class="sxs-lookup"><span data-stu-id="05288-105">Syntax</span></span>  
  
```xml  
<schemeSettings>
</schemeSettings>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="05288-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="05288-106">Attributes and Elements</span></span>  

 <span data-ttu-id="05288-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="05288-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="05288-108">特性</span><span class="sxs-lookup"><span data-stu-id="05288-108">Attributes</span></span>  

 <span data-ttu-id="05288-109">无</span><span class="sxs-lookup"><span data-stu-id="05288-109">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="05288-110">子元素</span><span class="sxs-lookup"><span data-stu-id="05288-110">Child Elements</span></span>  
  
|<span data-ttu-id="05288-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="05288-111">**Element**</span></span>|<span data-ttu-id="05288-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="05288-112">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="05288-113">add</span><span class="sxs-lookup"><span data-stu-id="05288-113">add</span></span>](add-element-for-schemesettings-uri-settings.md)|<span data-ttu-id="05288-114">为方案名称添加方案设置。</span><span class="sxs-lookup"><span data-stu-id="05288-114">Adds a scheme setting for a scheme name.</span></span>|  
|[<span data-ttu-id="05288-115">clear</span><span class="sxs-lookup"><span data-stu-id="05288-115">clear</span></span>](clear-element-for-schemesettings-uri-settings.md)|<span data-ttu-id="05288-116">清除所有现有方案设置。</span><span class="sxs-lookup"><span data-stu-id="05288-116">Clears all existing scheme settings.</span></span>|  
|[<span data-ttu-id="05288-117">删除</span><span class="sxs-lookup"><span data-stu-id="05288-117">remove</span></span>](remove-element-for-schemesettings-uri-settings.md)|<span data-ttu-id="05288-118">删除方案名称的方案设置。</span><span class="sxs-lookup"><span data-stu-id="05288-118">Removes a scheme setting for a scheme name.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="05288-119">父元素</span><span class="sxs-lookup"><span data-stu-id="05288-119">Parent Elements</span></span>  
  
|<span data-ttu-id="05288-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="05288-120">**Element**</span></span>|<span data-ttu-id="05288-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="05288-121">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="05288-122">uri</span><span class="sxs-lookup"><span data-stu-id="05288-122">uri</span></span>](uri-element-uri-settings.md)|<span data-ttu-id="05288-123">包含指定 .NET Framework 如何处理使用统一资源标识符 (Uri) 表示的 web 地址的设置。</span><span class="sxs-lookup"><span data-stu-id="05288-123">Contains settings that specify how the .NET Framework handles web addresses expressed using uniform resource identifiers (URIs).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="05288-124">备注</span><span class="sxs-lookup"><span data-stu-id="05288-124">Remarks</span></span>  

 <span data-ttu-id="05288-125">默认情况下，在 <xref:System.Uri?displayProperty=nameWithType> 执行路径压缩之前，类会取消转义编码的路径分隔符。</span><span class="sxs-lookup"><span data-stu-id="05288-125">By default, the <xref:System.Uri?displayProperty=nameWithType> class un-escapes percent encoded path delimiters before executing path compression.</span></span> <span data-ttu-id="05288-126">这是作为一种安全机制实现的，针对以下攻击：</span><span class="sxs-lookup"><span data-stu-id="05288-126">This was implemented as a security mechanism against attacks like the following:</span></span>  
  
 `http://www.contoso.com/..%2F..%2F/Windows/System32/cmd.exe?/c+dir+c:\`  
  
 <span data-ttu-id="05288-127">如果将此 URI 向下传递到模块，而不是正确处理百分号编码字符，则可能会导致服务器执行以下命令：</span><span class="sxs-lookup"><span data-stu-id="05288-127">If this URI gets passed down to modules not handling percent encoded characters correctly, it could result in the following command being executed by the server:</span></span>  
  
 `c:\Windows\System32\cmd.exe /c dir c:\`  
  
 <span data-ttu-id="05288-128">出于此原因， <xref:System.Uri?displayProperty=nameWithType> 类首先取消转义路径分隔符，然后应用路径压缩。</span><span class="sxs-lookup"><span data-stu-id="05288-128">For this reason, <xref:System.Uri?displayProperty=nameWithType> class first un-escapes path delimiters and then applies path compression.</span></span> <span data-ttu-id="05288-129">将上述恶意 URL 传递到 <xref:System.Uri?displayProperty=nameWithType> 类构造函数的结果将生成以下 URI：</span><span class="sxs-lookup"><span data-stu-id="05288-129">The result of passing the malicious URL above to <xref:System.Uri?displayProperty=nameWithType> class constructor results in the following URI:</span></span>  
  
 `http://www.microsoft.com/Windows/System32/cmd.exe?/c+dir+c:\`  
  
 <span data-ttu-id="05288-130">使用特定方案的 schemeSettings 配置选项，可以将此默认行为修改为不取消转义百分号编码的路径分隔符。</span><span class="sxs-lookup"><span data-stu-id="05288-130">This default behavior can be modified to not un-escape percent encoded path delimiters using the schemeSettings configuration option for a specific scheme.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="05288-131">配置文件</span><span class="sxs-lookup"><span data-stu-id="05288-131">Configuration Files</span></span>  

 <span data-ttu-id="05288-132">此元素可在应用程序配置文件或计算机配置文件 (Machine.config) 中使用。</span><span class="sxs-lookup"><span data-stu-id="05288-132">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="05288-133">示例</span><span class="sxs-lookup"><span data-stu-id="05288-133">Example</span></span>  

 <span data-ttu-id="05288-134">下面的示例演示类使用的配置 <xref:System.Uri> ，以支持不转义 http 方案的百分号编码的路径分隔符。</span><span class="sxs-lookup"><span data-stu-id="05288-134">The following example shows a configuration used by the <xref:System.Uri> class to support not escaping percent-encoded path delimiters for the http scheme.</span></span>  
  
```xml  
<configuration>  
  <uri>  
    <schemeSettings>  
      <add name="http" genericUriParserOptions="DontUnescapePathDotsAndSlashes"/>  
    </schemeSettings>  
  </uri>  
</configuration>  
```  
  
## <a name="element-information"></a><span data-ttu-id="05288-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="05288-135">Element Information</span></span>  
  
|||
|-|-|  
|<span data-ttu-id="05288-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="05288-136">Namespace</span></span>|<span data-ttu-id="05288-137">系统</span><span class="sxs-lookup"><span data-stu-id="05288-137">System</span></span>|  
|<span data-ttu-id="05288-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="05288-138">Schema Name</span></span>||  
|<span data-ttu-id="05288-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="05288-139">Validation File</span></span>||  
|<span data-ttu-id="05288-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="05288-140">Can be Empty</span></span>||  
  
## <a name="see-also"></a><span data-ttu-id="05288-141">请参阅</span><span class="sxs-lookup"><span data-stu-id="05288-141">See also</span></span>

- <xref:System.Configuration.SchemeSettingElement?displayProperty=nameWithType>
- <xref:System.Configuration.SchemeSettingElementCollection?displayProperty=nameWithType>
- <xref:System.Configuration.UriSection?displayProperty=nameWithType>
- <xref:System.Configuration.UriSection.SchemeSettings%2A?displayProperty=nameWithType>
- <xref:System.GenericUriParserOptions?displayProperty=nameWithType>
- <xref:System.Uri?displayProperty=nameWithType>
- [<span data-ttu-id="05288-142">网络设置架构</span><span class="sxs-lookup"><span data-stu-id="05288-142">Network Settings Schema</span></span>](index.md)
