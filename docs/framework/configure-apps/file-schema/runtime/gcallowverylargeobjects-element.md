---
title: gcAllowVeryLargeObjects 元素
ms.date: 03/30/2017
helpviewer_keywords:
- gcAllowVeryLargeObjects element
- <gcAllowVeryLargeObjects> element
ms.assetid: 5c7ea24a-39ac-4e5f-83b7-b9f9a1b556ab
ms.openlocfilehash: 1e54b0780ffb5bbe81ab1be2b376ff7a038ee05c
ms.sourcegitcommit: 0273f8845eb1ea8de64086bef2271b4f22182c91
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/09/2021
ms.locfileid: "98058124"
---
# <a name="gcallowverylargeobjects-element"></a><span data-ttu-id="c96a4-102">\<gcAllowVeryLargeObjects> 元素</span><span class="sxs-lookup"><span data-stu-id="c96a4-102">\<gcAllowVeryLargeObjects> element</span></span>

<span data-ttu-id="c96a4-103">在 64 位平台上，启用总大小大于 2 千兆字节 (GB) 的数组。</span><span class="sxs-lookup"><span data-stu-id="c96a4-103">On 64-bit platforms, enables arrays that are greater than 2 gigabytes (GB) in total size.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<gcAllowVeryLargeObjects>**  
  
## <a name="syntax"></a><span data-ttu-id="c96a4-104">语法</span><span class="sxs-lookup"><span data-stu-id="c96a4-104">Syntax</span></span>  
  
```xml  
<gcAllowVeryLargeObjects enabled="true|false" />  
```  
  
## <a name="attributes"></a><span data-ttu-id="c96a4-105">特性</span><span class="sxs-lookup"><span data-stu-id="c96a4-105">Attributes</span></span>
  
|<span data-ttu-id="c96a4-106">属性</span><span class="sxs-lookup"><span data-stu-id="c96a4-106">Attribute</span></span>|<span data-ttu-id="c96a4-107">描述</span><span class="sxs-lookup"><span data-stu-id="c96a4-107">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="c96a4-108">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="c96a4-108">Required attribute.</span></span><br /><br /> <span data-ttu-id="c96a4-109">指定是否在64位平台上启用了总大小中大于 2 GB 的数组。</span><span class="sxs-lookup"><span data-stu-id="c96a4-109">Specifies whether arrays that are greater than 2 GB in total size are enabled on 64-bit platforms.</span></span>|  
  
### <a name="enabled-attribute"></a><span data-ttu-id="c96a4-110">enabled 属性</span><span class="sxs-lookup"><span data-stu-id="c96a4-110">enabled attribute</span></span>  
  
|<span data-ttu-id="c96a4-111">“值”</span><span class="sxs-lookup"><span data-stu-id="c96a4-111">Value</span></span>|<span data-ttu-id="c96a4-112">描述</span><span class="sxs-lookup"><span data-stu-id="c96a4-112">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="c96a4-113">总大小中大于 2 GB 的数组未启用。</span><span class="sxs-lookup"><span data-stu-id="c96a4-113">Arrays greater than 2 GB in total size are not enabled.</span></span> <span data-ttu-id="c96a4-114">这是默认值。</span><span class="sxs-lookup"><span data-stu-id="c96a4-114">This is the default.</span></span>|  
|`true`|<span data-ttu-id="c96a4-115">在64位平台上，总大小中已启用大于 2 GB 的数组。</span><span class="sxs-lookup"><span data-stu-id="c96a4-115">Arrays greater than 2 GB in total size are enabled on 64-bit platforms.</span></span>|  
  
## <a name="child-elements"></a><span data-ttu-id="c96a4-116">子元素</span><span class="sxs-lookup"><span data-stu-id="c96a4-116">Child elements</span></span>  

<span data-ttu-id="c96a4-117">无。</span><span class="sxs-lookup"><span data-stu-id="c96a4-117">None.</span></span>  
  
## <a name="parent-elements"></a><span data-ttu-id="c96a4-118">父元素</span><span class="sxs-lookup"><span data-stu-id="c96a4-118">Parent elements</span></span>
  
|<span data-ttu-id="c96a4-119">元素</span><span class="sxs-lookup"><span data-stu-id="c96a4-119">Element</span></span>|<span data-ttu-id="c96a4-120">描述</span><span class="sxs-lookup"><span data-stu-id="c96a4-120">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="c96a4-121">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="c96a4-121">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="c96a4-122">包含有关运行时初始化选项的信息。</span><span class="sxs-lookup"><span data-stu-id="c96a4-122">Contains information about runtime initialization options.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c96a4-123">注解</span><span class="sxs-lookup"><span data-stu-id="c96a4-123">Remarks</span></span>  

 <span data-ttu-id="c96a4-124">在应用程序配置文件中使用此元素可启用大小大于 2 GB 的数组，但不会更改对象大小或数组大小的其他限制：</span><span class="sxs-lookup"><span data-stu-id="c96a4-124">Using this element in your application configuration file enables arrays that are larger than 2 GB in size, but does not change other limits on object size or array size:</span></span>  
  
- <span data-ttu-id="c96a4-125">数组中元素的最大数目为 <xref:System.UInt32.MaxValue?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="c96a4-125">The maximum number of elements in an array is <xref:System.UInt32.MaxValue?displayProperty=nameWithType>.</span></span>  
  
- <span data-ttu-id="c96a4-126">任何单个维度中的最大大小为 2147483591 (0x7FFFFFC7) 用于字节数组和单字节结构的数组，2146435071 (0X7FEFFFFF) 包含其他类型的数组。</span><span class="sxs-lookup"><span data-stu-id="c96a4-126">The maximum size in any single dimension is 2,147,483,591 (0x7FFFFFC7) for byte arrays and arrays of single-byte structures, and 2,146,435,071 (0X7FEFFFFF) for arrays containing other types.</span></span>  
  
- <span data-ttu-id="c96a4-127">字符串和其他非数组对象的最大大小不变。</span><span class="sxs-lookup"><span data-stu-id="c96a4-127">The maximum size for strings and other non-array objects is unchanged.</span></span>  
  
> [!CAUTION]
> <span data-ttu-id="c96a4-128">在启用此功能之前，请确保应用程序不包含不安全代码，该代码假定所有数组大小均小于 2 GB。</span><span class="sxs-lookup"><span data-stu-id="c96a4-128">Before enabling this feature, ensure that your application does not include unsafe code that assumes that all arrays are smaller than 2 GB in size.</span></span> <span data-ttu-id="c96a4-129">例如，使用数组作为缓冲区的不安全代码可能容易受到缓冲区溢出的攻击，因为假设数组不会超过 2 GB。</span><span class="sxs-lookup"><span data-stu-id="c96a4-129">For example, unsafe code that uses arrays as buffers might be susceptible to buffer overruns if it's written on the assumption that arrays will not exceed 2 GB.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c96a4-130">示例</span><span class="sxs-lookup"><span data-stu-id="c96a4-130">Example</span></span>  

 <span data-ttu-id="c96a4-131">下面的示例演示如何为应用程序启用此功能。</span><span class="sxs-lookup"><span data-stu-id="c96a4-131">The following example shows how to enable this feature for an application.</span></span>  
  
```xml  
<configuration>  
  <runtime>  
    <gcAllowVeryLargeObjects enabled="true" />  
  </runtime>  
</configuration>  
```  
  
## <a name="supported-in"></a><span data-ttu-id="c96a4-132">受以下版本支持：</span><span class="sxs-lookup"><span data-stu-id="c96a4-132">Supported in</span></span>

<span data-ttu-id="c96a4-133">.NET Framework 4.5 及更高版本</span><span class="sxs-lookup"><span data-stu-id="c96a4-133">.NET Framework 4.5 and later versions</span></span>

## <a name="see-also"></a><span data-ttu-id="c96a4-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c96a4-134">See also</span></span>

- [<span data-ttu-id="c96a4-135">运行时设置架构</span><span class="sxs-lookup"><span data-stu-id="c96a4-135">Runtime Settings Schema</span></span>](index.md)
- [<span data-ttu-id="c96a4-136">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="c96a4-136">Configuration File Schema</span></span>](../index.md)
