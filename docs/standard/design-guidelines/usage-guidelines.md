---
description: 详细了解：使用准则
title: 使用准则
ms.date: 10/22/2008
helpviewer_keywords:
- class library design guidelines [.NET Framework], usage guidelines
ms.assetid: 42215ffa-a099-4a26-b14e-fb2bdb6f95b7
ms.openlocfilehash: a435fab2adb00f671dfde1619a3c1f8db719d9df
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99641793"
---
# <a name="usage-guidelines"></a><span data-ttu-id="9375a-103">使用准则</span><span class="sxs-lookup"><span data-stu-id="9375a-103">Usage guidelines</span></span>

<span data-ttu-id="9375a-104">本部分包含有关在可公开访问的 API 中使用常见类型的准则。</span><span class="sxs-lookup"><span data-stu-id="9375a-104">This section contains guidelines for using common types in publicly accessible APIs.</span></span> <span data-ttu-id="9375a-105">其中涉及内置框架类型（如序列化特性）的直接使用和常见运算符的重载。</span><span class="sxs-lookup"><span data-stu-id="9375a-105">It deals with direct usage of built-in Framework types (e.g., serialization attributes) and overloading common operators.</span></span>
  
<span data-ttu-id="9375a-106"><xref:System.IDisposable?displayProperty=nameWithType> 接口在本部分未进行介绍，但在[释放模式](../garbage-collection/implementing-dispose.md)部分中进行了讨论。</span><span class="sxs-lookup"><span data-stu-id="9375a-106">The <xref:System.IDisposable?displayProperty=nameWithType> interface is not covered in this section, but is discussed in the [Dispose Pattern](../garbage-collection/implementing-dispose.md) section.</span></span>

> [!NOTE]
> <span data-ttu-id="9375a-107">有关其他常见内置 .NET Framework 类型的指南和附加信息，请参阅以下各项的引用主题：<xref:System.DateTime?displayProperty=nameWithType>、<xref:System.DateTimeOffset?displayProperty=nameWithType>、<xref:System.ICloneable?displayProperty=nameWithType>、<xref:System.IComparable%601?displayProperty=nameWithType>、<xref:System.IEquatable%601?displayProperty=nameWithType>、<xref:System.Nullable%601?displayProperty=nameWithType>、<xref:System.Object?displayProperty=nameWithType>、<xref:System.Uri?displayProperty=nameWithType>。</span><span class="sxs-lookup"><span data-stu-id="9375a-107">For guidelines and additional information about other common, built-in .NET Framework types, see the reference topics for the following: <xref:System.DateTime?displayProperty=nameWithType>, <xref:System.DateTimeOffset?displayProperty=nameWithType>, <xref:System.ICloneable?displayProperty=nameWithType>, <xref:System.IComparable%601?displayProperty=nameWithType>, <xref:System.IEquatable%601?displayProperty=nameWithType>, <xref:System.Nullable%601?displayProperty=nameWithType>, <xref:System.Object?displayProperty=nameWithType>, <xref:System.Uri?displayProperty=nameWithType>.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9375a-108">本节内容</span><span class="sxs-lookup"><span data-stu-id="9375a-108">In this section</span></span>

[<span data-ttu-id="9375a-109">数组</span><span class="sxs-lookup"><span data-stu-id="9375a-109">Arrays</span></span>](arrays.md)  
[<span data-ttu-id="9375a-110">特性</span><span class="sxs-lookup"><span data-stu-id="9375a-110">Attributes</span></span>](attributes.md)  
[<span data-ttu-id="9375a-111">集合</span><span class="sxs-lookup"><span data-stu-id="9375a-111">Collections</span></span>](guidelines-for-collections.md)  
[<span data-ttu-id="9375a-112">序列化</span><span class="sxs-lookup"><span data-stu-id="9375a-112">Serialization</span></span>](serialization.md)  
[<span data-ttu-id="9375a-113">System.Xml 使用情况</span><span class="sxs-lookup"><span data-stu-id="9375a-113">System.Xml Usage</span></span>](system-xml-usage.md)  
[<span data-ttu-id="9375a-114">相等运算符</span><span class="sxs-lookup"><span data-stu-id="9375a-114">Equality Operators</span></span>](equality-operators.md)  

<span data-ttu-id="9375a-115">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="9375a-115">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

<span data-ttu-id="9375a-116">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="9375a-116">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9375a-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="9375a-117">See also</span></span>

- [<span data-ttu-id="9375a-118">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="9375a-118">Framework Design Guidelines</span></span>](index.md)
