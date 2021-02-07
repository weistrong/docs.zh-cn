---
description: 了解详细信息：数值运算符和比较运算符
title: 数值和比较运算符
ms.date: 03/30/2017
ms.assetid: 25b4a26a-06f2-4f80-87a9-76705ed46197
ms.openlocfilehash: 5b17f19769436ac4e575ac974668eadc3b17b8f6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99695523"
---
# <a name="numeric-and-comparison-operators"></a><span data-ttu-id="ab897-103">数值和比较运算符</span><span class="sxs-lookup"><span data-stu-id="ab897-103">Numeric and Comparison Operators</span></span>

<span data-ttu-id="ab897-104">算术运算符和比较运算符在公共语言运行库 (CLR) 中按预期方式工作，但有以下几点例外：</span><span class="sxs-lookup"><span data-stu-id="ab897-104">Arithmetic and comparison operators work as expected in the common language runtime (CLR) except as follows:</span></span>

- <span data-ttu-id="ab897-105">SQL 不支持对浮点数字使用取模运算符。</span><span class="sxs-lookup"><span data-stu-id="ab897-105">SQL does not support the modulus operator on floating-point numbers.</span></span>

- <span data-ttu-id="ab897-106">SQL 不支持未校验的算法。</span><span class="sxs-lookup"><span data-stu-id="ab897-106">SQL does not support unchecked arithmetic.</span></span>

- <span data-ttu-id="ab897-107">在无法复制到 SQL 中的表达式中使用增量和减量运算符时会产生副作用，因而不支持此类运算符。</span><span class="sxs-lookup"><span data-stu-id="ab897-107">Increment and decrement operators cause side-effects when you use them in expressions that cannot be replicated in SQL and are, therefore, not supported.</span></span>

## <a name="supported-operators"></a><span data-ttu-id="ab897-108">支持的运算符</span><span class="sxs-lookup"><span data-stu-id="ab897-108">Supported Operators</span></span>

[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="ab897-109">支持以下运算符。</span><span class="sxs-lookup"><span data-stu-id="ab897-109">supports the following operators.</span></span>

- <span data-ttu-id="ab897-110">基本算术运算符：</span><span class="sxs-lookup"><span data-stu-id="ab897-110">Basic arithmetic operators:</span></span>

  - `+`

  - <span data-ttu-id="ab897-111">`-`（减号）</span><span class="sxs-lookup"><span data-stu-id="ab897-111">`-` (subtraction)</span></span>

  - `*`

  - `/`

  - <span data-ttu-id="ab897-112">Visual Basic 整除 (`\`)</span><span class="sxs-lookup"><span data-stu-id="ab897-112">Visual Basic integer division (`\`)</span></span>

  - <span data-ttu-id="ab897-113">`%` (Visual Basic `Mod`)</span><span class="sxs-lookup"><span data-stu-id="ab897-113">`%` (Visual Basic `Mod`)</span></span>

  - `<<`

  - `>>`

  - <span data-ttu-id="ab897-114">`-`（一元求反）</span><span class="sxs-lookup"><span data-stu-id="ab897-114">`-` (unary negation)</span></span>

- <span data-ttu-id="ab897-115">基本比较运算符：</span><span class="sxs-lookup"><span data-stu-id="ab897-115">Basic comparison operators:</span></span>

  - <span data-ttu-id="ab897-116">Visual Basic `=` 和 C# `==`</span><span class="sxs-lookup"><span data-stu-id="ab897-116">Visual Basic `=` and C# `==`</span></span>

  - <span data-ttu-id="ab897-117">Visual Basic `<>` 和 C# `!=`</span><span class="sxs-lookup"><span data-stu-id="ab897-117">Visual Basic `<>` and C# `!=`</span></span>

  - <span data-ttu-id="ab897-118">Visual Basic `Is/IsNot`</span><span class="sxs-lookup"><span data-stu-id="ab897-118">Visual Basic `Is/IsNot`</span></span>

  - `<`

  - `<=`

  - `>`

  - `>=`

## <a name="see-also"></a><span data-ttu-id="ab897-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="ab897-119">See also</span></span>

- [<span data-ttu-id="ab897-120">数据类型和函数</span><span class="sxs-lookup"><span data-stu-id="ab897-120">Data Types and Functions</span></span>](data-types-and-functions.md)
- [<span data-ttu-id="ab897-121">C# 运算符</span><span class="sxs-lookup"><span data-stu-id="ab897-121">C# Operators</span></span>](../../../../../csharp/language-reference/operators/index.md)
- [<span data-ttu-id="ab897-122">运算符</span><span class="sxs-lookup"><span data-stu-id="ab897-122">Operators</span></span>](../../../../../visual-basic/language-reference/operators/index.md)
