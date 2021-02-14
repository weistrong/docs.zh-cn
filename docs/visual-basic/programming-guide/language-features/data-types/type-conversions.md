---
description: 详细了解：中的类型转换 Visual Basic
title: 类型转换
ms.date: 07/20/2015
helpviewer_keywords:
- conversions [Visual Basic], type
- data types [Visual Basic], changing
- variables [Visual Basic], changing data type
- type conversion [Visual Basic]
- conversions [Visual Basic], data type
- changing data types [Visual Basic]
- data type conversion [Visual Basic]
ms.assetid: 1cdacd21-ba31-4b62-b5be-395e41eeaa17
ms.openlocfilehash: 1f40951856710eb6f2892a7f7a4e04173ee3ee44
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100454477"
---
# <a name="type-conversions-in-visual-basic"></a><span data-ttu-id="281d5-103">Visual Basic 中的类型转换</span><span class="sxs-lookup"><span data-stu-id="281d5-103">Type Conversions in Visual Basic</span></span>

<span data-ttu-id="281d5-104">将值从一种数据类型更改为另一种类型的过程称为 *转换*。</span><span class="sxs-lookup"><span data-stu-id="281d5-104">The process of changing a value from one data type to another type is called *conversion*.</span></span> <span data-ttu-id="281d5-105">转换可以是 *扩大* 或 *收缩* 转换，具体取决于所涉及的类型的数据容量。</span><span class="sxs-lookup"><span data-stu-id="281d5-105">Conversions are either *widening* or *narrowing*, depending on the data capacities of the types involved.</span></span> <span data-ttu-id="281d5-106">它们也是 *隐式* 或 *显式* 的，具体取决于源代码中的语法。</span><span class="sxs-lookup"><span data-stu-id="281d5-106">They are also *implicit* or *explicit*, depending on the syntax in the source code.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="281d5-107">本节内容</span><span class="sxs-lookup"><span data-stu-id="281d5-107">In This Section</span></span>  

 [<span data-ttu-id="281d5-108">Widening and Narrowing Conversions</span><span class="sxs-lookup"><span data-stu-id="281d5-108">Widening and Narrowing Conversions</span></span>](widening-and-narrowing-conversions.md)  
 <span data-ttu-id="281d5-109">说明按照目标类型是否可以保存数据进行分类的转换。</span><span class="sxs-lookup"><span data-stu-id="281d5-109">Explains conversions classified by whether the destination type can hold the data.</span></span>  
  
 [<span data-ttu-id="281d5-110">隐式转换和显式转换</span><span class="sxs-lookup"><span data-stu-id="281d5-110">Implicit and Explicit Conversions</span></span>](implicit-and-explicit-conversions.md)  
 <span data-ttu-id="281d5-111">讨论 Visual Basic 自动执行这些转换的分类转换。</span><span class="sxs-lookup"><span data-stu-id="281d5-111">Discusses conversions classified by whether Visual Basic performs them automatically.</span></span>  
  
 [<span data-ttu-id="281d5-112">字符串和其他类型之间的转换</span><span class="sxs-lookup"><span data-stu-id="281d5-112">Conversions Between Strings and Other Types</span></span>](conversions-between-strings-and-other-types.md)  
 <span data-ttu-id="281d5-113">说明如何在字符串与数字、 `Boolean` 或日期/时间值之间进行转换。</span><span class="sxs-lookup"><span data-stu-id="281d5-113">Illustrates converting between strings and numeric, `Boolean`, or date/time values.</span></span>  
  
 [<span data-ttu-id="281d5-114">如何：在 Visual Basic 中将一个对象转换为其他类型</span><span class="sxs-lookup"><span data-stu-id="281d5-114">How to: Convert an Object to Another Type in Visual Basic</span></span>](how-to-convert-an-object-to-another-type.md)  
 <span data-ttu-id="281d5-115">说明如何将变量转换 `Object` 为任何其他数据类型。</span><span class="sxs-lookup"><span data-stu-id="281d5-115">Shows how to convert an `Object` variable to any other data type.</span></span>  
  
 [<span data-ttu-id="281d5-116">数组转换</span><span class="sxs-lookup"><span data-stu-id="281d5-116">Array Conversions</span></span>](array-conversions.md)  
 <span data-ttu-id="281d5-117">逐步介绍在不同数据类型的数组之间进行转换的过程。</span><span class="sxs-lookup"><span data-stu-id="281d5-117">Steps you through the process of converting between arrays of different data types.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="281d5-118">相关章节</span><span class="sxs-lookup"><span data-stu-id="281d5-118">Related Sections</span></span>  

 [<span data-ttu-id="281d5-119">数据类型</span><span class="sxs-lookup"><span data-stu-id="281d5-119">Data Types</span></span>](index.md)  
 <span data-ttu-id="281d5-120">介绍 Visual Basic 数据类型，并说明如何使用它们。</span><span class="sxs-lookup"><span data-stu-id="281d5-120">Introduces the Visual Basic data types and describes how to use them.</span></span>  
  
 [<span data-ttu-id="281d5-121">数据类型</span><span class="sxs-lookup"><span data-stu-id="281d5-121">Data Types</span></span>](../../../language-reference/data-types/index.md)  
 <span data-ttu-id="281d5-122">列出 Visual Basic 提供的基本数据类型。</span><span class="sxs-lookup"><span data-stu-id="281d5-122">Lists the elementary data types supplied by Visual Basic.</span></span>  
  
 [<span data-ttu-id="281d5-123">数据类型疑难解答</span><span class="sxs-lookup"><span data-stu-id="281d5-123">Troubleshooting Data Types</span></span>](troubleshooting-data-types.md)  
 <span data-ttu-id="281d5-124">讨论在使用数据类型时可能出现的一些常见问题。</span><span class="sxs-lookup"><span data-stu-id="281d5-124">Discusses some common problems that can arise when working with data types.</span></span>
