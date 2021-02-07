---
description: 了解详细信息：如何：访问预定义 UTC 和本地时区对象
title: 如何：访问预定义 UTC 和本地时区对象
ms.date: 04/10/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- time zones [.NET], local
- predefined time zones
- UTC times, predefined
- local time zone access
- time zones [.NET], retrieving
- time zones [.NET], UTC
ms.assetid: 961fb70b-83f0-4dab-a042-cb5fcd817cf5
ms.openlocfilehash: 74e3ca601ac0b3a6a684569b0931f8566b5d5d26
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99702751"
---
# <a name="how-to-access-the-predefined-utc-and-local-time-zone-objects"></a><span data-ttu-id="37192-103">如何：访问预定义 UTC 和本地时区对象</span><span class="sxs-lookup"><span data-stu-id="37192-103">How to: Access the predefined UTC and local time zone objects</span></span>

<span data-ttu-id="37192-104"><xref:System.TimeZoneInfo>类提供了两个属性： <xref:System.TimeZoneInfo.Utc%2A> 和，可 <xref:System.TimeZoneInfo.Local%2A> 让你的代码访问预定义的时区对象。</span><span class="sxs-lookup"><span data-stu-id="37192-104">The <xref:System.TimeZoneInfo> class provides two properties, <xref:System.TimeZoneInfo.Utc%2A> and <xref:System.TimeZoneInfo.Local%2A>, that give your code access to predefined time zone objects.</span></span> <span data-ttu-id="37192-105">本主题介绍如何访问这些属性返回的 <xref:System.TimeZoneInfo> 对象。</span><span class="sxs-lookup"><span data-stu-id="37192-105">This topic discusses how to access the <xref:System.TimeZoneInfo> objects returned by those properties.</span></span>

### <a name="to-access-the-coordinated-universal-time-utc-timezoneinfo-object"></a><span data-ttu-id="37192-106">访问协调世界时 (UTC) TimeZoneInfo 对象</span><span class="sxs-lookup"><span data-stu-id="37192-106">To access the Coordinated Universal Time (UTC) TimeZoneInfo object</span></span>

1. <span data-ttu-id="37192-107">使用 `static` `Shared` Visual Basic) 属性中的 (<xref:System.TimeZoneInfo.Utc%2A?displayProperty=nameWithType> 访问协调世界时。</span><span class="sxs-lookup"><span data-stu-id="37192-107">Use the `static` (`Shared` in Visual Basic) <xref:System.TimeZoneInfo.Utc%2A?displayProperty=nameWithType> property to access Coordinated Universal Time.</span></span>

2. <span data-ttu-id="37192-108">不是将 <xref:System.TimeZoneInfo> 属性返回的对象分配给对象变量，而是继续通过属性访问协调世界时 <xref:System.TimeZoneInfo.Utc%2A?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="37192-108">Rather than assigning the <xref:System.TimeZoneInfo> object returned by the property to an object variable, continue to access Coordinated Universal Time through the <xref:System.TimeZoneInfo.Utc%2A?displayProperty=nameWithType> property.</span></span>

### <a name="to-access-the-local-time-zone"></a><span data-ttu-id="37192-109">访问本地时区</span><span class="sxs-lookup"><span data-stu-id="37192-109">To access the local time zone</span></span>

1. <span data-ttu-id="37192-110">使用 `static` `Shared` Visual Basic) 属性中的 (<xref:System.TimeZoneInfo.Local%2A?displayProperty=nameWithType> 访问本地系统时区。</span><span class="sxs-lookup"><span data-stu-id="37192-110">Use the `static` (`Shared` in Visual Basic) <xref:System.TimeZoneInfo.Local%2A?displayProperty=nameWithType> property to access the local system time zone.</span></span>

2. <span data-ttu-id="37192-111">不是将 <xref:System.TimeZoneInfo> 属性返回的对象分配给对象变量，而是继续通过属性访问本地时区 <xref:System.TimeZoneInfo.Local%2A?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="37192-111">Rather than assigning the <xref:System.TimeZoneInfo> object returned by the property to an object variable, continue to access the local time zone through the <xref:System.TimeZoneInfo.Local%2A?displayProperty=nameWithType> property.</span></span>

## <a name="example"></a><span data-ttu-id="37192-112">示例</span><span class="sxs-lookup"><span data-stu-id="37192-112">Example</span></span>

<span data-ttu-id="37192-113">下面的代码使用 <xref:System.TimeZoneInfo.Local%2A?displayProperty=nameWithType> 和 <xref:System.TimeZoneInfo.Utc%2A?displayProperty=nameWithType> 属性转换美国和加拿大东部标准时区的时间，并将时区名称显示到控制台。</span><span class="sxs-lookup"><span data-stu-id="37192-113">The following code uses the <xref:System.TimeZoneInfo.Local%2A?displayProperty=nameWithType> and <xref:System.TimeZoneInfo.Utc%2A?displayProperty=nameWithType> properties to convert a time from the U.S. and Canadian Eastern Standard time zone, as well as to display the time zone name to the console.</span></span>

[!code-csharp[System.TimeZone2.Concepts#13](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.TimeZone2.Concepts/CS/TimeZone2Concepts.cs#13)]
[!code-vb[System.TimeZone2.Concepts#13](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.TimeZone2.Concepts/VB/TimeZone2Concepts.vb#13)]

<span data-ttu-id="37192-114">应始终通过属性访问本地时区， <xref:System.TimeZoneInfo.Local%2A?displayProperty=nameWithType> 而不是将本地时区分配给 <xref:System.TimeZoneInfo> 对象变量。</span><span class="sxs-lookup"><span data-stu-id="37192-114">You should always access the local time zone through the <xref:System.TimeZoneInfo.Local%2A?displayProperty=nameWithType> property rather than assigning the local time zone to a <xref:System.TimeZoneInfo> object variable.</span></span> <span data-ttu-id="37192-115">同样，应始终通过属性访问协调世界时， <xref:System.TimeZoneInfo.Utc%2A?displayProperty=nameWithType> 而不是将 UTC 时区分配给 <xref:System.TimeZoneInfo> 对象变量。</span><span class="sxs-lookup"><span data-stu-id="37192-115">Similarly, you should always access Coordinated Universal Time through the <xref:System.TimeZoneInfo.Utc%2A?displayProperty=nameWithType> property rather than assigning the UTC zone to a <xref:System.TimeZoneInfo> object variable.</span></span> <span data-ttu-id="37192-116">这可防止 <xref:System.TimeZoneInfo> 对象变量被调用 <xref:System.TimeZoneInfo.ClearCachedData%2A?displayProperty=nameWithType> 方法无效。</span><span class="sxs-lookup"><span data-stu-id="37192-116">This prevents the <xref:System.TimeZoneInfo> object variable from being invalidated by a call to the <xref:System.TimeZoneInfo.ClearCachedData%2A?displayProperty=nameWithType> method.</span></span>

## <a name="compiling-the-code"></a><span data-ttu-id="37192-117">编译代码</span><span class="sxs-lookup"><span data-stu-id="37192-117">Compiling the code</span></span>

<span data-ttu-id="37192-118">此示例需要：</span><span class="sxs-lookup"><span data-stu-id="37192-118">This example requires:</span></span>

- <span data-ttu-id="37192-119"><xref:System>要导入的命名空间与 `using` c # 代码) 中 (必需的语句一起导入。</span><span class="sxs-lookup"><span data-stu-id="37192-119">That the <xref:System> namespace be imported with the `using` statement (required in C# code).</span></span>

## <a name="see-also"></a><span data-ttu-id="37192-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="37192-120">See also</span></span>

- [<span data-ttu-id="37192-121">日期、时间和时区</span><span class="sxs-lookup"><span data-stu-id="37192-121">Dates, times, and time zones</span></span>](index.md)
- [<span data-ttu-id="37192-122">查找本地系统上定义的时区</span><span class="sxs-lookup"><span data-stu-id="37192-122">Finding the time zones defined on a local system</span></span>](finding-the-time-zones-on-local-system.md)
- [<span data-ttu-id="37192-123">如何：实例化 TimeZoneInfo 对象</span><span class="sxs-lookup"><span data-stu-id="37192-123">How to: Instantiate a TimeZoneInfo object</span></span>](instantiate-time-zone-info.md)
