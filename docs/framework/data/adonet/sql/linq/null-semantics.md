---
description: 了解更多： Null 语义
title: Null 语义
ms.date: 03/30/2017
ms.assetid: a97017ae-d634-4cf3-bbaf-054a528fd683
ms.openlocfilehash: 2326cd20a225f31693260aa038477f1f6090d02f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99695550"
---
# <a name="null-semantics"></a><span data-ttu-id="07073-103">Null 语义</span><span class="sxs-lookup"><span data-stu-id="07073-103">Null Semantics</span></span>

<span data-ttu-id="07073-104">下表提供了文档的各个部分的链接， [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 其中 `null` `Nothing` 讨论了 Visual Basic) 问题 (。</span><span class="sxs-lookup"><span data-stu-id="07073-104">The following table provides links to various parts of the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] documentation where `null` (`Nothing` in Visual Basic) issues are discussed.</span></span>  
  
|<span data-ttu-id="07073-105">主题</span><span class="sxs-lookup"><span data-stu-id="07073-105">Topic</span></span>|<span data-ttu-id="07073-106">说明</span><span class="sxs-lookup"><span data-stu-id="07073-106">Description</span></span>|  
|-----------|-----------------|  
|[<span data-ttu-id="07073-107">SQL-CLR 类型不匹配</span><span class="sxs-lookup"><span data-stu-id="07073-107">SQL-CLR Type Mismatches</span></span>](sql-clr-type-mismatches.md)|<span data-ttu-id="07073-108">本主题的 "Null 语义" 部分包括以下内容的讨论：三态 SQL Boolean 与两态公共语言运行时 (CLR) <xref:System.Boolean> 、文本 `Nothing` (Visual Basic) 和 `null` (c # ) ，以及其他类似问题。</span><span class="sxs-lookup"><span data-stu-id="07073-108">The "Null Semantics" section of this topic includes discussion of the three-state SQL Boolean versus the two-state common language runtime (CLR) <xref:System.Boolean>, the literal `Nothing` (Visual Basic) and `null` (C#), and other similar issues.</span></span>|  
|[<span data-ttu-id="07073-109">标准查询运算符转换</span><span class="sxs-lookup"><span data-stu-id="07073-109">Standard Query Operator Translation</span></span>](standard-query-operator-translation.md)|<span data-ttu-id="07073-110">本主题的“Null 语义”部分介绍 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]中的 null 比较语义。</span><span class="sxs-lookup"><span data-stu-id="07073-110">The "Null Semantics" section of this topic describes null comparison semantics in [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].</span></span>|  
|[<span data-ttu-id="07073-111">System.String 方法</span><span class="sxs-lookup"><span data-stu-id="07073-111">System.String Methods</span></span>](system-string-methods.md)|<span data-ttu-id="07073-112">本主题的“与 .NET 的差异”部分说明从 <xref:System.String.LastIndexOf%2A> 返回 0 为何意味着字符串为 null 或找到的位置为 0。</span><span class="sxs-lookup"><span data-stu-id="07073-112">The "Differences from .NET" section of this topic describes how a return of 0 from <xref:System.String.LastIndexOf%2A> might mean either that the string is null or that the found position is 0.</span></span>|  
|[<span data-ttu-id="07073-113">计算数值序列中值的和</span><span class="sxs-lookup"><span data-stu-id="07073-113">Compute the Sum of Values in a Numeric Sequence</span></span>](compute-the-sum-of-values-in-a-numeric-sequence.md)|<span data-ttu-id="07073-114">描述运算符如何 <xref:System.Linq.Enumerable.Sum%2A> 计算 `null` (`Nothing` 在 Visual Basic) 而不是0（对于仅包含 null 值或空序列的序列）。</span><span class="sxs-lookup"><span data-stu-id="07073-114">Describes how the <xref:System.Linq.Enumerable.Sum%2A> operator evaluates to `null` (`Nothing` in Visual Basic) instead of 0 for a sequence that contains only nulls or for an empty sequence.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="07073-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="07073-115">See also</span></span>

- [<span data-ttu-id="07073-116">数据类型和函数</span><span class="sxs-lookup"><span data-stu-id="07073-116">Data Types and Functions</span></span>](data-types-and-functions.md)
