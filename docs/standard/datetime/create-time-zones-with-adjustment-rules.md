---
description: 了解详细信息：如何：创建带有调整规则的时区
title: 如何：创建含调整规则的时区
ms.date: 04/10/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- time zones [.NET], creating
- time zones [.NET], and adjustment rules
- adjustment rule [.NET]
ms.assetid: c52ef192-13a9-435f-8015-3b12eae8c47c
ms.openlocfilehash: d581d01d9f9386adf99079f4f8f8e09585b06848
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99702764"
---
# <a name="how-to-create-time-zones-with-adjustment-rules"></a><span data-ttu-id="9f514-103">如何：创建含调整规则的时区</span><span class="sxs-lookup"><span data-stu-id="9f514-103">How to: Create time zones with adjustment rules</span></span>

<span data-ttu-id="9f514-104">由于以下几个原因，应用程序所需的确切时区信息在特定系统上可能不存在：</span><span class="sxs-lookup"><span data-stu-id="9f514-104">The precise time zone information that is required by an application may not be present on a particular system for several reasons:</span></span>

- <span data-ttu-id="9f514-105">本地系统的注册表中从未定义过该时区。</span><span class="sxs-lookup"><span data-stu-id="9f514-105">The time zone has never been defined in the local system's registry.</span></span>

- <span data-ttu-id="9f514-106">已修改或删除注册表中有关时区的数据。</span><span class="sxs-lookup"><span data-stu-id="9f514-106">Data about the time zone has been modified or removed from the registry.</span></span>

- <span data-ttu-id="9f514-107">对于特定的历史时间段，时区没有有关时区调整的准确信息。</span><span class="sxs-lookup"><span data-stu-id="9f514-107">The time zone does not have accurate information about time zone adjustments for a particular historic period.</span></span>

<span data-ttu-id="9f514-108">在这些情况下，可以调用 <xref:System.TimeZoneInfo.CreateCustomTimeZone%2A> 方法来定义应用程序所需的时区。</span><span class="sxs-lookup"><span data-stu-id="9f514-108">In these cases, you can call the <xref:System.TimeZoneInfo.CreateCustomTimeZone%2A> method to define the time zone required by your application.</span></span> <span data-ttu-id="9f514-109">您可以使用此方法的重载来创建具有或不带调整规则的时区。</span><span class="sxs-lookup"><span data-stu-id="9f514-109">You can use the overloads of this method to create a time zone with or without adjustment rules.</span></span> <span data-ttu-id="9f514-110">如果时区支持夏令时，则可以用固定或浮动调整规则定义调整。</span><span class="sxs-lookup"><span data-stu-id="9f514-110">If the time zone supports daylight saving time, you can define adjustments with either fixed or floating adjustment rules.</span></span> <span data-ttu-id="9f514-111"> (这些术语的定义，请参阅时区 [概述](time-zone-overview.md)中的 "时区术语" 部分。 ) </span><span class="sxs-lookup"><span data-stu-id="9f514-111">(For definitions of these terms, see the "Time Zone Terminology" section in [Time zone overview](time-zone-overview.md).)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9f514-112">通过调用方法创建的自定义时区 <xref:System.TimeZoneInfo.CreateCustomTimeZone%2A> 未添加到注册表中。</span><span class="sxs-lookup"><span data-stu-id="9f514-112">Custom time zones created by calling the <xref:System.TimeZoneInfo.CreateCustomTimeZone%2A> method are not added to the registry.</span></span> <span data-ttu-id="9f514-113">相反，只能通过方法调用返回的对象引用来访问这些对象 <xref:System.TimeZoneInfo.CreateCustomTimeZone%2A> 。</span><span class="sxs-lookup"><span data-stu-id="9f514-113">Instead, they can be accessed only through the object reference returned by the <xref:System.TimeZoneInfo.CreateCustomTimeZone%2A> method call.</span></span>

<span data-ttu-id="9f514-114">本主题说明如何创建具有调整规则的时区。</span><span class="sxs-lookup"><span data-stu-id="9f514-114">This topic shows how to create a time zone with adjustment rules.</span></span> <span data-ttu-id="9f514-115">若要创建不支持夏令时调整规则的时区，请参阅 [如何：创建不带调整规则的时区](create-time-zones-without-adjustment-rules.md)。</span><span class="sxs-lookup"><span data-stu-id="9f514-115">To create a time zone that does not support daylight saving time adjustment rules, see [How to: Create Time Zones Without Adjustment Rules](create-time-zones-without-adjustment-rules.md).</span></span>

### <a name="to-create-a-time-zone-with-floating-adjustment-rules"></a><span data-ttu-id="9f514-116">创建具有浮动调整规则的时区</span><span class="sxs-lookup"><span data-stu-id="9f514-116">To create a time zone with floating adjustment rules</span></span>

1. <span data-ttu-id="9f514-117">对于每个调整 (也就是说，对于每个从特定时间间隔转换到标准时间) ，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="9f514-117">For each adjustment (that is, for each transition away from and back to standard time over a particular time interval), do the following:</span></span>

    1. <span data-ttu-id="9f514-118">定义时区调整的开始转换时间。</span><span class="sxs-lookup"><span data-stu-id="9f514-118">Define the starting transition time for the time zone adjustment.</span></span>

       <span data-ttu-id="9f514-119">您必须调用 <xref:System.TimeZoneInfo.TransitionTime.CreateFloatingDateRule%2A?displayProperty=nameWithType> 方法并向其传递一个 <xref:System.DateTime> 值，用于定义转换时间、定义转换月份的整数值、定义转换发生的周的整数值，以及 <xref:System.DayOfWeek> 定义发生转换的周中某天的值。</span><span class="sxs-lookup"><span data-stu-id="9f514-119">You must call the <xref:System.TimeZoneInfo.TransitionTime.CreateFloatingDateRule%2A?displayProperty=nameWithType> method and pass it a <xref:System.DateTime> value that defines the time of the transition, an integer value that defines the month of the transition, an integer value that defines the week on which the transition occurs, and a <xref:System.DayOfWeek> value that defines the day of the week on which the transition occurs.</span></span> <span data-ttu-id="9f514-120">此方法调用对对象进行实例化 <xref:System.TimeZoneInfo.TransitionTime> 。</span><span class="sxs-lookup"><span data-stu-id="9f514-120">This method call instantiates a <xref:System.TimeZoneInfo.TransitionTime> object.</span></span>

    2. <span data-ttu-id="9f514-121">为时区调整定义结束转换时间。</span><span class="sxs-lookup"><span data-stu-id="9f514-121">Define the ending transition time for the time zone adjustment.</span></span> <span data-ttu-id="9f514-122">这需要对方法的另一次调用 <xref:System.TimeZoneInfo.TransitionTime.CreateFloatingDateRule%2A?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="9f514-122">This requires another call to the <xref:System.TimeZoneInfo.TransitionTime.CreateFloatingDateRule%2A?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="9f514-123">此方法调用将实例化第二个 <xref:System.TimeZoneInfo.TransitionTime> 对象。</span><span class="sxs-lookup"><span data-stu-id="9f514-123">This method call instantiates a second <xref:System.TimeZoneInfo.TransitionTime> object.</span></span>

    3. <span data-ttu-id="9f514-124">调用 <xref:System.TimeZoneInfo.AdjustmentRule.CreateAdjustmentRule%2A> 方法并向其传递调整的有效开始日期和结束日期、 <xref:System.TimeSpan> 定义转换中的时间量的对象和两个 <xref:System.TimeZoneInfo.TransitionTime> 对象，这些对象定义在夏令时发生转换的时间。</span><span class="sxs-lookup"><span data-stu-id="9f514-124">Call the <xref:System.TimeZoneInfo.AdjustmentRule.CreateAdjustmentRule%2A> method and pass it the effective start and end dates of the adjustment, a <xref:System.TimeSpan> object that defines the amount of time in the transition, and the two <xref:System.TimeZoneInfo.TransitionTime> objects that define when the transitions to and from daylight saving time occur.</span></span> <span data-ttu-id="9f514-125">此方法调用对对象进行实例化 <xref:System.TimeZoneInfo.AdjustmentRule> 。</span><span class="sxs-lookup"><span data-stu-id="9f514-125">This method call instantiates a <xref:System.TimeZoneInfo.AdjustmentRule> object.</span></span>

    4. <span data-ttu-id="9f514-126">将 <xref:System.TimeZoneInfo.AdjustmentRule> 对象分配给对象的数组 <xref:System.TimeZoneInfo.AdjustmentRule> 。</span><span class="sxs-lookup"><span data-stu-id="9f514-126">Assign the <xref:System.TimeZoneInfo.AdjustmentRule> object to an array of <xref:System.TimeZoneInfo.AdjustmentRule> objects.</span></span>

2. <span data-ttu-id="9f514-127">定义时区的显示名称。</span><span class="sxs-lookup"><span data-stu-id="9f514-127">Define the time zone's display name.</span></span> <span data-ttu-id="9f514-128">显示名称采用了一种非常标准的格式，其中，时区与协调世界时的时差 (UTC) 括在括号中，后面跟有标识时区的字符串、时区中的一个或多个城市，或者时区中的一个或多个国家或地区。</span><span class="sxs-lookup"><span data-stu-id="9f514-128">The display name follows a fairly standard format in which the time zone's offset from Coordinated Universal Time (UTC) is enclosed in parentheses and is followed by a string that identifies the time zone, one or more of the cities in the time zone, or one or more of the countries or regions in the time zone.</span></span>

3. <span data-ttu-id="9f514-129">定义时区标准时间的名称。</span><span class="sxs-lookup"><span data-stu-id="9f514-129">Define the name of the time zone's standard time.</span></span> <span data-ttu-id="9f514-130">通常，此字符串还用作时区的标识符。</span><span class="sxs-lookup"><span data-stu-id="9f514-130">Typically, this string is also used as the time zone's identifier.</span></span>

4. <span data-ttu-id="9f514-131">定义时区的夏令时的名称。</span><span class="sxs-lookup"><span data-stu-id="9f514-131">Define the name of the time zone's daylight time.</span></span>

5. <span data-ttu-id="9f514-132">如果要使用不同于时区的标准名称的标识符，请定义时区标识符。</span><span class="sxs-lookup"><span data-stu-id="9f514-132">If you want to use a different identifier than the time zone's standard name, define the time zone identifier.</span></span>

6. <span data-ttu-id="9f514-133">实例化 <xref:System.TimeSpan> 定义时区与 UTC 的偏移量的对象。</span><span class="sxs-lookup"><span data-stu-id="9f514-133">Instantiate a <xref:System.TimeSpan> object that defines the time zone's offset from UTC.</span></span> <span data-ttu-id="9f514-134">时间时区晚于 UTC 的时区具有正偏移量。</span><span class="sxs-lookup"><span data-stu-id="9f514-134">Time zones with times that are later than UTC have a positive offset.</span></span> <span data-ttu-id="9f514-135">其时间早于 UTC 的时区具有负偏移量。</span><span class="sxs-lookup"><span data-stu-id="9f514-135">Time zones with times that are earlier than UTC have a negative offset.</span></span>

7. <span data-ttu-id="9f514-136">调用 <xref:System.TimeZoneInfo.CreateCustomTimeZone%28System.String%2CSystem.TimeSpan%2CSystem.String%2CSystem.String%2CSystem.String%2CSystem.TimeZoneInfo.AdjustmentRule%5B%5D%29?displayProperty=nameWithType> 方法以实例化新时区。</span><span class="sxs-lookup"><span data-stu-id="9f514-136">Call the <xref:System.TimeZoneInfo.CreateCustomTimeZone%28System.String%2CSystem.TimeSpan%2CSystem.String%2CSystem.String%2CSystem.String%2CSystem.TimeZoneInfo.AdjustmentRule%5B%5D%29?displayProperty=nameWithType> method to instantiate the new time zone.</span></span>

## <a name="example"></a><span data-ttu-id="9f514-137">示例</span><span class="sxs-lookup"><span data-stu-id="9f514-137">Example</span></span>

<span data-ttu-id="9f514-138">下面的示例为美国定义了一个中部标准时区，其中包括从1918到当前时间间隔内的各种时间间隔的调整规则。</span><span class="sxs-lookup"><span data-stu-id="9f514-138">The following example defines a Central Standard Time zone for the United States that includes adjustment rules for a variety of time intervals from 1918 to the present.</span></span>

[!code-csharp[System.TimeZone2.CreateTimeZone#5](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.TimeZone2.CreateTimeZone/cs/System.TimeZone2.CreateTimeZone.cs#5)]
[!code-vb[System.TimeZone2.CreateTimeZone#5](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.TimeZone2.CreateTimeZone/vb/System.TimeZone2.CreateTimeZone.vb#5)]

<span data-ttu-id="9f514-139">在此示例中创建的时区具有多个调整规则。</span><span class="sxs-lookup"><span data-stu-id="9f514-139">The time zone created in this example has multiple adjustment rules.</span></span> <span data-ttu-id="9f514-140">必须小心，以确保任何调整规则的有效开始日期和结束日期不会与另一个调整规则的日期重叠。</span><span class="sxs-lookup"><span data-stu-id="9f514-140">Care must be taken to ensure that the effective start and end dates of any adjustment rule do not overlap with the dates of another adjustment rule.</span></span> <span data-ttu-id="9f514-141">如果有重叠， <xref:System.InvalidTimeZoneException> 则会引发。</span><span class="sxs-lookup"><span data-stu-id="9f514-141">If there is an overlap, an <xref:System.InvalidTimeZoneException> is thrown.</span></span>

<span data-ttu-id="9f514-142">对于浮点调整规则，将值5传递给方法的 `week` 参数， <xref:System.TimeZoneInfo.TransitionTime.CreateFloatingDateRule%2A> 以指示在特定月份的最后一周发生转换。</span><span class="sxs-lookup"><span data-stu-id="9f514-142">For floating adjustment rules, the value 5 is passed to the `week` parameter of the <xref:System.TimeZoneInfo.TransitionTime.CreateFloatingDateRule%2A> method to indicate that the transition occurs on the last week of a particular month.</span></span>

<span data-ttu-id="9f514-143">在创建 <xref:System.TimeZoneInfo.AdjustmentRule> 要在方法调用中使用的对象数组 <xref:System.TimeZoneInfo.CreateCustomTimeZone%28System.String%2CSystem.TimeSpan%2CSystem.String%2CSystem.String%2CSystem.String%2CSystem.TimeZoneInfo.AdjustmentRule%5B%5D%29?displayProperty=nameWithType> 时，代码可以将数组初始化为要为时区创建的调整数所需的大小。</span><span class="sxs-lookup"><span data-stu-id="9f514-143">In creating the array of <xref:System.TimeZoneInfo.AdjustmentRule> objects to use in the <xref:System.TimeZoneInfo.CreateCustomTimeZone%28System.String%2CSystem.TimeSpan%2CSystem.String%2CSystem.String%2CSystem.String%2CSystem.TimeZoneInfo.AdjustmentRule%5B%5D%29?displayProperty=nameWithType> method call, the code could initialize the array to the size required by the number of adjustments to be created for the time zone.</span></span> <span data-ttu-id="9f514-144">相反，此代码示例调用 <xref:System.Collections.Generic.List%601.Add%2A> 方法将每个调整规则添加到对象的泛型 <xref:System.Collections.Generic.List%601> 集合 <xref:System.TimeZoneInfo.AdjustmentRule> 。</span><span class="sxs-lookup"><span data-stu-id="9f514-144">Instead, this code example calls the <xref:System.Collections.Generic.List%601.Add%2A> method to add each adjustment rule to a generic <xref:System.Collections.Generic.List%601> collection of <xref:System.TimeZoneInfo.AdjustmentRule> objects.</span></span> <span data-ttu-id="9f514-145">然后，该代码调用 <xref:System.Collections.Generic.List%601.CopyTo%2A> 方法将此集合的成员复制到数组。</span><span class="sxs-lookup"><span data-stu-id="9f514-145">The code then calls the <xref:System.Collections.Generic.List%601.CopyTo%2A> method to copy the members of this collection to the array.</span></span>

<span data-ttu-id="9f514-146">该示例还使用 <xref:System.TimeZoneInfo.TransitionTime.CreateFixedDateRule%2A> 方法定义固定日期调整。</span><span class="sxs-lookup"><span data-stu-id="9f514-146">The example also uses the <xref:System.TimeZoneInfo.TransitionTime.CreateFixedDateRule%2A> method to define fixed-date adjustments.</span></span> <span data-ttu-id="9f514-147">这类似于调用 <xref:System.TimeZoneInfo.TransitionTime.CreateFloatingDateRule%2A> 方法，只需要转换参数的时间、月份和日期。</span><span class="sxs-lookup"><span data-stu-id="9f514-147">This is similar to calling the <xref:System.TimeZoneInfo.TransitionTime.CreateFloatingDateRule%2A> method, except that it requires only the time, month, and day of the transition parameters.</span></span>

<span data-ttu-id="9f514-148">可以使用如下所示的代码测试该示例：</span><span class="sxs-lookup"><span data-stu-id="9f514-148">The example can be tested using code such as the following:</span></span>

[!code-csharp[System.TimeZone2.CreateTimeZone#7](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.TimeZone2.CreateTimeZone/cs/System.TimeZone2.CreateTimeZone.cs#7)]
[!code-vb[System.TimeZone2.CreateTimeZone#7](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.TimeZone2.CreateTimeZone/vb/System.TimeZone2.CreateTimeZone.vb#7)]

## <a name="compiling-the-code"></a><span data-ttu-id="9f514-149">编译代码</span><span class="sxs-lookup"><span data-stu-id="9f514-149">Compiling the code</span></span>

<span data-ttu-id="9f514-150">此示例需要：</span><span class="sxs-lookup"><span data-stu-id="9f514-150">This example requires:</span></span>

- <span data-ttu-id="9f514-151">导入以下命名空间：</span><span class="sxs-lookup"><span data-stu-id="9f514-151">That the following namespaces be imported:</span></span>

  [!code-csharp[System.TimeZone2.CreateTimeZone#6](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.TimeZone2.CreateTimeZone/cs/System.TimeZone2.CreateTimeZone.cs#6)]
  [!code-vb[System.TimeZone2.CreateTimeZone#6](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.TimeZone2.CreateTimeZone/vb/System.TimeZone2.CreateTimeZone.vb#6)]

## <a name="see-also"></a><span data-ttu-id="9f514-152">请参阅</span><span class="sxs-lookup"><span data-stu-id="9f514-152">See also</span></span>

- [<span data-ttu-id="9f514-153">日期、时间和时区</span><span class="sxs-lookup"><span data-stu-id="9f514-153">Dates, times, and time zones</span></span>](index.md)
- [<span data-ttu-id="9f514-154">时区概述</span><span class="sxs-lookup"><span data-stu-id="9f514-154">Time zone overview</span></span>](time-zone-overview.md)
- [<span data-ttu-id="9f514-155">如何：创建不带调整规则的时区</span><span class="sxs-lookup"><span data-stu-id="9f514-155">How to: Create time zones without adjustment rules</span></span>](create-time-zones-without-adjustment-rules.md)
