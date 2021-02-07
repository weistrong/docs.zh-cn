---
description: 了解详细信息：查找本地系统上定义的时区
title: 查找本地系统上定义的时区
ms.date: 04/10/2017
helpviewer_keywords:
- time zones [.NET], local
- time zones [.NET], finding local system time zones
- time zone identifiers [.NET]
- local time zone access
- time zones [.NET], retrieving
- UTC times, finding local system time zones
- time zones [.NET], UTC
ms.assetid: 3f63b1bc-9a4b-4bde-84ea-ab028a80d3e1
ms.openlocfilehash: 1b7a4d1962adac42b47cda42d4d1223c4b79852a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99702634"
---
# <a name="finding-the-time-zones-defined-on-a-local-system"></a><span data-ttu-id="56778-103">查找本地系统上定义的时区</span><span class="sxs-lookup"><span data-stu-id="56778-103">Finding the time zones defined on a local system</span></span>

<span data-ttu-id="56778-104"><xref:System.TimeZoneInfo> 类不公开公共构造函数。</span><span class="sxs-lookup"><span data-stu-id="56778-104">The <xref:System.TimeZoneInfo> class does not expose a public constructor.</span></span> <span data-ttu-id="56778-105">因此，`new` 关键字不能用于创建新的 <xref:System.TimeZoneInfo> 对象。</span><span class="sxs-lookup"><span data-stu-id="56778-105">As a result, the `new` keyword cannot be used to create a new <xref:System.TimeZoneInfo> object.</span></span> <span data-ttu-id="56778-106">相反，<xref:System.TimeZoneInfo> 对象通过从注册表检索关于预定义时区的信息或通过创建自定义时区而完成实例化。</span><span class="sxs-lookup"><span data-stu-id="56778-106">Instead, <xref:System.TimeZoneInfo> objects are instantiated either by retrieving information on predefined time zones from the registry or by creating a custom time zone.</span></span> <span data-ttu-id="56778-107">本主题讨论从存储在注册表中的数据实例化时区。</span><span class="sxs-lookup"><span data-stu-id="56778-107">This topic discusses instantiating a time zone from data stored in the registry.</span></span> <span data-ttu-id="56778-108">此外，<xref:System.TimeZoneInfo> 类的 `static`（Visual Basic 中的 `shared`）属性提供对协调世界时 (UTC) 和本地时区的访问。</span><span class="sxs-lookup"><span data-stu-id="56778-108">In addition, `static` (`shared` in Visual Basic) properties of the <xref:System.TimeZoneInfo> class provide access to Coordinated Universal Time (UTC) and the local time zone.</span></span>

> [!NOTE]
> <span data-ttu-id="56778-109">对于在注册表中未定义的时区，可以通过调用 <xref:System.TimeZoneInfo.CreateCustomTimeZone%2A> 方法的重载创建自定义时区。</span><span class="sxs-lookup"><span data-stu-id="56778-109">For time zones that are not defined in the registry, you can create custom time zones by calling the overloads of the <xref:System.TimeZoneInfo.CreateCustomTimeZone%2A> method.</span></span> <span data-ttu-id="56778-110">[如何：创建不带调整规则的时区](create-time-zones-without-adjustment-rules.md)和[如何：创建带有调整规则的](create-time-zones-with-adjustment-rules.md)时区主题中讨论了如何创建自定义时区。</span><span class="sxs-lookup"><span data-stu-id="56778-110">Creating a custom time zone is discussed in the [How to: Create time zones without adjustment rules](create-time-zones-without-adjustment-rules.md) and [How to: Create time zones with adjustment rules](create-time-zones-with-adjustment-rules.md) topics.</span></span> <span data-ttu-id="56778-111">此外，可以通过使用 <xref:System.TimeZoneInfo.FromSerializedString%2A> 方法将 <xref:System.TimeZoneInfo> 对象从序列化字符串还原来对其实例化。</span><span class="sxs-lookup"><span data-stu-id="56778-111">In addition, you can instantiate a <xref:System.TimeZoneInfo> object by restoring it from a serialized string with the <xref:System.TimeZoneInfo.FromSerializedString%2A> method.</span></span> <span data-ttu-id="56778-112">序列化和反序列化 <xref:System.TimeZoneInfo> 对象在 [如何：将时区保存到嵌入的资源](save-time-zones-to-an-embedded-resource.md) 和 [如何：从嵌入的资源还原时区](restore-time-zones-from-an-embedded-resource.md) 主题中进行了讨论。</span><span class="sxs-lookup"><span data-stu-id="56778-112">Serializing and deserializing a <xref:System.TimeZoneInfo> object is discussed in the [How to: Save time zones to an embedded resource](save-time-zones-to-an-embedded-resource.md) and [How to: Restore Time Zones from an Embedded Resource](restore-time-zones-from-an-embedded-resource.md) topics.</span></span>

## <a name="accessing-individual-time-zones"></a><span data-ttu-id="56778-113">访问单个时区</span><span class="sxs-lookup"><span data-stu-id="56778-113">Accessing individual time zones</span></span>

<span data-ttu-id="56778-114"><xref:System.TimeZoneInfo> 类提供两个预定义的时区对象，分别表示 UTC 时间和本地时区。</span><span class="sxs-lookup"><span data-stu-id="56778-114">The <xref:System.TimeZoneInfo> class provides two predefined time zone objects that represent the UTC time and the local time zone.</span></span> <span data-ttu-id="56778-115">它们分别可从 <xref:System.TimeZoneInfo.Utc%2A> 和 <xref:System.TimeZoneInfo.Local%2A> 属性获得。</span><span class="sxs-lookup"><span data-stu-id="56778-115">They are available from the <xref:System.TimeZoneInfo.Utc%2A> and <xref:System.TimeZoneInfo.Local%2A> properties, respectively.</span></span> <span data-ttu-id="56778-116">有关访问 UTC 或本地时区的说明，请参阅 [如何：访问预定义的 utc 和本地时区对象](access-utc-and-local.md)。</span><span class="sxs-lookup"><span data-stu-id="56778-116">For instructions on accessing the UTC or local time zones, see [How to: Access the predefined UTC and local time zone objects](access-utc-and-local.md).</span></span>

<span data-ttu-id="56778-117">还可以实例化表示注册表中定义的任何时区的 <xref:System.TimeZoneInfo> 对象。</span><span class="sxs-lookup"><span data-stu-id="56778-117">You can also instantiate a <xref:System.TimeZoneInfo> object that represents any time zone defined in the registry.</span></span> <span data-ttu-id="56778-118">有关实例化特定时区对象的说明，请参阅 [如何：实例化 TimeZoneInfo 对象](instantiate-time-zone-info.md)。</span><span class="sxs-lookup"><span data-stu-id="56778-118">For instructions on instantiating a specific time zone object, see [How to: Instantiate a TimeZoneInfo object](instantiate-time-zone-info.md).</span></span>

## <a name="time-zone-identifiers"></a><span data-ttu-id="56778-119">时区标识符</span><span class="sxs-lookup"><span data-stu-id="56778-119">Time zone identifiers</span></span>

<span data-ttu-id="56778-120">时区标识符是唯一标识时区的键字段。</span><span class="sxs-lookup"><span data-stu-id="56778-120">The time zone identifier is a key field that uniquely identifies the time zone.</span></span> <span data-ttu-id="56778-121">虽然大多数键都相对较短，但时区标识符相对较长。</span><span class="sxs-lookup"><span data-stu-id="56778-121">While most keys are relatively short, the time zone identifier is comparatively long.</span></span> <span data-ttu-id="56778-122">在大多数情况下，其值对应于 <xref:System.TimeZoneInfo.StandardName%2A?displayProperty=nameWithType> 属性，该属性用于提供时区标准时间的名称。</span><span class="sxs-lookup"><span data-stu-id="56778-122">In most cases, its value corresponds to the <xref:System.TimeZoneInfo.StandardName%2A?displayProperty=nameWithType> property, which is used to provide the name of the time zone's standard time.</span></span> <span data-ttu-id="56778-123">但是，有例外情况。</span><span class="sxs-lookup"><span data-stu-id="56778-123">However, there are exceptions.</span></span> <span data-ttu-id="56778-124">确保提供有效标识符最好的办法是枚举系统上可用的时区，并记下其关联的标识符。</span><span class="sxs-lookup"><span data-stu-id="56778-124">The best way to make sure that you supply a valid identifier is to enumerate the time zones available on your system and note their associated identifiers.</span></span>

## <a name="see-also"></a><span data-ttu-id="56778-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="56778-125">See also</span></span>

- [<span data-ttu-id="56778-126">日期、时间和时区</span><span class="sxs-lookup"><span data-stu-id="56778-126">Dates, times, and time zones</span></span>](index.md)
- [<span data-ttu-id="56778-127">如何：访问预定义的 UTC 和本地时区对象</span><span class="sxs-lookup"><span data-stu-id="56778-127">How to: Access the predefined UTC and local time zone objects</span></span>](access-utc-and-local.md)
- [<span data-ttu-id="56778-128">如何：实例化 TimeZoneInfo 对象</span><span class="sxs-lookup"><span data-stu-id="56778-128">How to: Instantiate a TimeZoneInfo object</span></span>](instantiate-time-zone-info.md)
- [<span data-ttu-id="56778-129">在时区之间转换时间</span><span class="sxs-lookup"><span data-stu-id="56778-129">Converting times between time zones</span></span>](converting-between-time-zones.md)
