---
description: 了解详细信息： <EnableAmPmParseAdjustment> 元素
title: <EnableAmPmParseAdjustment> 元素
ms.date: 03/30/2017
ms.assetid: fda998a5-f538-4f8b-a18c-ee7f35e16938
ms.openlocfilehash: 86fd04ab536f44f0cffdb5a37f4718fc03698485
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99787053"
---
# <a name="enableampmparseadjustment-element"></a><span data-ttu-id="15d3d-103">\<EnableAmPmParseAdjustment> 元素</span><span class="sxs-lookup"><span data-stu-id="15d3d-103">\<EnableAmPmParseAdjustment> Element</span></span>

<span data-ttu-id="15d3d-104">确定日期和时间分析方法是否使用经过调整的规则集来分析包含 day、month、hour 和 AM/PM 指示符的日期字符串。</span><span class="sxs-lookup"><span data-stu-id="15d3d-104">Determines whether date and time parsing methods use an adjusted set of rules to parse date strings that contain a day, month, hour, and AM/PM designator.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<runtime>**](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<EnableAmPmParseAdjustment>**  
  
## <a name="syntax"></a><span data-ttu-id="15d3d-105">语法</span><span class="sxs-lookup"><span data-stu-id="15d3d-105">Syntax</span></span>  
  
```xml  
<EnableAmPmParseAdjustment enabled="0"|"1" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="15d3d-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="15d3d-106">Attributes and Elements</span></span>  

 <span data-ttu-id="15d3d-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="15d3d-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="15d3d-108">特性</span><span class="sxs-lookup"><span data-stu-id="15d3d-108">Attributes</span></span>  
  
|<span data-ttu-id="15d3d-109">属性</span><span class="sxs-lookup"><span data-stu-id="15d3d-109">Attribute</span></span>|<span data-ttu-id="15d3d-110">描述</span><span class="sxs-lookup"><span data-stu-id="15d3d-110">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="15d3d-111">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="15d3d-111">Required attribute.</span></span><br /><br /> <span data-ttu-id="15d3d-112">指定日期和时间分析方法是否使用经过调整的规则集来分析只包含 day、month、hour 和 AM/PM 指示符的日期字符串。</span><span class="sxs-lookup"><span data-stu-id="15d3d-112">Specifies whether date and time parsing methods use an adjusted set of rules to parse date strings that contain only a day, month, hour, and AM/PM designator.</span></span>|  
  
### <a name="enabled-attribute"></a><span data-ttu-id="15d3d-113">enabled 特性</span><span class="sxs-lookup"><span data-stu-id="15d3d-113">enabled Attribute</span></span>  
  
|<span data-ttu-id="15d3d-114">值</span><span class="sxs-lookup"><span data-stu-id="15d3d-114">Value</span></span>|<span data-ttu-id="15d3d-115">说明</span><span class="sxs-lookup"><span data-stu-id="15d3d-115">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="15d3d-116">0</span><span class="sxs-lookup"><span data-stu-id="15d3d-116">0</span></span>|<span data-ttu-id="15d3d-117">日期和时间分析方法不使用调整的规则来分析日期字符串，这些字符串只包含日、月、小时和 AM/PM 指示符。</span><span class="sxs-lookup"><span data-stu-id="15d3d-117">Date and time parsing methods do not use adjusted rules for parsing date strings that contain only a day, month, hour, and AM/PM designator.</span></span>|  
|<span data-ttu-id="15d3d-118">1</span><span class="sxs-lookup"><span data-stu-id="15d3d-118">1</span></span>|<span data-ttu-id="15d3d-119">日期和时间分析方法使用经过调整的规则，用于分析日期字符串，这些字符串只包含日、月、小时和 AM/PM 指示符。</span><span class="sxs-lookup"><span data-stu-id="15d3d-119">Date and time parsing methods use adjusted rules for parsing date strings that contain only a day, month, hour, and AM/PM designator.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="15d3d-120">子元素</span><span class="sxs-lookup"><span data-stu-id="15d3d-120">Child Elements</span></span>  

 <span data-ttu-id="15d3d-121">无。</span><span class="sxs-lookup"><span data-stu-id="15d3d-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="15d3d-122">父元素</span><span class="sxs-lookup"><span data-stu-id="15d3d-122">Parent Elements</span></span>  
  
|<span data-ttu-id="15d3d-123">元素</span><span class="sxs-lookup"><span data-stu-id="15d3d-123">Element</span></span>|<span data-ttu-id="15d3d-124">说明</span><span class="sxs-lookup"><span data-stu-id="15d3d-124">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="15d3d-125">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="15d3d-125">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="15d3d-126">包含有关运行时初始化选项的信息。</span><span class="sxs-lookup"><span data-stu-id="15d3d-126">Contains information about runtime initialization options.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="15d3d-127">备注</span><span class="sxs-lookup"><span data-stu-id="15d3d-127">Remarks</span></span>  

 <span data-ttu-id="15d3d-128">`<EnableAmPmParseAdjustment>`元素控制以下方法如何分析包含数字日和月后跟一个小时和 AM/PM 指示符的日期字符串， (例如 "4/10 6 AM" ) ：</span><span class="sxs-lookup"><span data-stu-id="15d3d-128">The `<EnableAmPmParseAdjustment>` element controls how the following methods parse a date string that contains a numeric day and month followed by an hour and an AM/PM designator (such as "4/10 6 AM"):</span></span>  
  
- <xref:System.DateTime.Parse%2A?displayProperty=nameWithType>  
  
- <xref:System.DateTimeOffset.Parse%2A?displayProperty=nameWithType>  
  
- <xref:System.DateTime.TryParse%2A?displayProperty=nameWithType>  
  
- <xref:System.DateTimeOffset.TryParse%2A?displayProperty=nameWithType>  
  
- <xref:System.Convert.ToDateTime%2A?displayProperty=nameWithType>  
  
 <span data-ttu-id="15d3d-129">其他模式不受影响。</span><span class="sxs-lookup"><span data-stu-id="15d3d-129">No other patterns are affected.</span></span>  
  
 <span data-ttu-id="15d3d-130">`<EnableAmPmParseAdjustment>`元素对 <xref:System.DateTime.ParseExact%2A?displayProperty=nameWithType> 、 <xref:System.DateTime.TryParseExact%2A?displayProperty=nameWithType> 、 <xref:System.DateTimeOffset.ParseExact%2A?displayProperty=nameWithType> 和方法不起作用 <xref:System.DateTimeOffset.TryParseExact%2A?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="15d3d-130">The `<EnableAmPmParseAdjustment>` element has no effect on the  <xref:System.DateTime.ParseExact%2A?displayProperty=nameWithType>,  <xref:System.DateTime.TryParseExact%2A?displayProperty=nameWithType>, <xref:System.DateTimeOffset.ParseExact%2A?displayProperty=nameWithType>, and <xref:System.DateTimeOffset.TryParseExact%2A?displayProperty=nameWithType> methods.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="15d3d-131">在 .NET Core 和 .NET Native 中，将默认启用调整后的 AM/PM 分析规则。</span><span class="sxs-lookup"><span data-stu-id="15d3d-131">In .NET Core and .NET Native, the adjusted AM/PM parsing rules are enabled by default.</span></span>  
  
 <span data-ttu-id="15d3d-132">如果未启用解析调整规则，则会将字符串的第一个数字解释为12小时制的小时，而除 AM/PM 指示符之外的字符串的其余部分将被忽略。</span><span class="sxs-lookup"><span data-stu-id="15d3d-132">If the parsing adjustment rule is not enabled, the first digit of the string is interpreted as the hour of the 12-hour clock, and the remainder of the string except for the AM/PM designator is ignored.</span></span> <span data-ttu-id="15d3d-133">解析方法返回的日期和时间由当前日期和从日期字符串提取的日期中的小时组成。</span><span class="sxs-lookup"><span data-stu-id="15d3d-133">The date and time returned by the parsing method consists of the current date and the hour of the day extracted from the date string.</span></span>  
  
 <span data-ttu-id="15d3d-134">如果启用了解析调整规则，则分析方法会将日期和月份解释为属于当前年份，并将时间解释为12小时制的小时。</span><span class="sxs-lookup"><span data-stu-id="15d3d-134">If the parsing adjustment rule is enabled, parsing method interpret the day and month as belonging to the current year, and interpret the time as the hour of the 12-hour clock.</span></span>  
  
 <span data-ttu-id="15d3d-135">下表说明了 <xref:System.DateTime> 当 <xref:System.DateTime.Parse%28System.String%29?displayProperty=nameWithType> 使用方法分析字符串 "4/10 6 AM" （ `<EnableAmPmParseAdjustment>` 元素的 `enabled` 属性设置为 "0" 或 "1"）时，值中的差异。</span><span class="sxs-lookup"><span data-stu-id="15d3d-135">The following table illustrates the difference in the <xref:System.DateTime> value when the <xref:System.DateTime.Parse%28System.String%29?displayProperty=nameWithType> method is used to parse the string ""4/10 6 AM" with the `<EnableAmPmParseAdjustment>` element's `enabled` property  set to "0" or "1".</span></span> <span data-ttu-id="15d3d-136">它假定今天的日期为2017年1月5日，并使用指定的区域性的 "G" 格式字符串来显示日期。</span><span class="sxs-lookup"><span data-stu-id="15d3d-136">It assumes that today's date is January 5, 2017, and displays the date as if it is formatted using the specified culture's "G" format string.</span></span>  
  
|<span data-ttu-id="15d3d-137">区域性名称</span><span class="sxs-lookup"><span data-stu-id="15d3d-137">Culture name</span></span>|<span data-ttu-id="15d3d-138">enabled = "0"</span><span class="sxs-lookup"><span data-stu-id="15d3d-138">enabled="0"</span></span>|<span data-ttu-id="15d3d-139">enabled = "1"</span><span class="sxs-lookup"><span data-stu-id="15d3d-139">enabled="1"</span></span>|  
|------------------|------------------|------------------|  
|<span data-ttu-id="15d3d-140">zh-CN</span><span class="sxs-lookup"><span data-stu-id="15d3d-140">en-US</span></span>|<span data-ttu-id="15d3d-141">上午 1/5/2017 4:00:00</span><span class="sxs-lookup"><span data-stu-id="15d3d-141">1/5/2017 4:00:00 AM</span></span>|<span data-ttu-id="15d3d-142">上午 4/10/2017 6:00:00</span><span class="sxs-lookup"><span data-stu-id="15d3d-142">4/10/2017 6:00:00 AM</span></span>|  
|<span data-ttu-id="15d3d-143">en-GB</span><span class="sxs-lookup"><span data-stu-id="15d3d-143">en-GB</span></span>|<span data-ttu-id="15d3d-144">5/1/2017 6:00:00</span><span class="sxs-lookup"><span data-stu-id="15d3d-144">5/1/2017 6:00:00</span></span>|<span data-ttu-id="15d3d-145">10/4/2017 6:00:00</span><span class="sxs-lookup"><span data-stu-id="15d3d-145">10/4/2017 6:00:00</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="15d3d-146">请参阅</span><span class="sxs-lookup"><span data-stu-id="15d3d-146">See also</span></span>

- [<span data-ttu-id="15d3d-147">\<runtime> 元素</span><span class="sxs-lookup"><span data-stu-id="15d3d-147">\<runtime> Element</span></span>](runtime-element.md)
- [<span data-ttu-id="15d3d-148">\<configuration> 元素</span><span class="sxs-lookup"><span data-stu-id="15d3d-148">\<configuration> Element</span></span>](../configuration-element.md)
