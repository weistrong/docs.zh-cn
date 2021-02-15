---
description: '了解详细信息：结构 (Visual Basic) '
title: 結構
ms.date: 07/20/2015
helpviewer_keywords:
- structures [Visual Basic]
- user-defined data types [Visual Basic], structures
- user-defined types [Visual Basic], about user-defined types
- data types [Visual Basic], user-defined
- user-defined data types [Visual Basic], about user-defined data types
- types [Visual Basic], user-defined
ms.assetid: 55e86462-5e99-4d33-8018-6d097ca491b2
ms.openlocfilehash: c79ba7b4ea8e80aced6c2a280c4896ed9f8c9916
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100427616"
---
# <a name="structures-visual-basic"></a><span data-ttu-id="fec5b-103">结构 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="fec5b-103">Structures (Visual Basic)</span></span>

<span data-ttu-id="fec5b-104">*结构* 是 Visual Basic 早期版本支持的用户定义类型 (UDT) 的一般化。</span><span class="sxs-lookup"><span data-stu-id="fec5b-104">A *structure* is a generalization of the user-defined type (UDT) supported by previous versions of Visual Basic.</span></span> <span data-ttu-id="fec5b-105">除了字段外，结构还可以公开属性、方法和事件。</span><span class="sxs-lookup"><span data-stu-id="fec5b-105">In addition to fields, structures can expose properties, methods, and events.</span></span> <span data-ttu-id="fec5b-106">结构可以实现一个或多个接口，并且可以为每个字段声明单独的访问级别。</span><span class="sxs-lookup"><span data-stu-id="fec5b-106">A structure can implement one or more interfaces, and you can declare individual access levels for each field.</span></span>  
  
 <span data-ttu-id="fec5b-107">您可以组合不同类型的数据项来创建结构。</span><span class="sxs-lookup"><span data-stu-id="fec5b-107">You can combine data items of different types to create a structure.</span></span> <span data-ttu-id="fec5b-108">结构将一个或多个 *元素* 与另一个或多个元素彼此关联。</span><span class="sxs-lookup"><span data-stu-id="fec5b-108">A structure associates one or more *elements* with each other and with the structure itself.</span></span> <span data-ttu-id="fec5b-109">在声明结构时，它将成为 *复合数据类型*，并且可以声明该类型的变量。</span><span class="sxs-lookup"><span data-stu-id="fec5b-109">When you declare a structure, it becomes a *composite data type*, and you can declare variables of that type.</span></span>  
  
 <span data-ttu-id="fec5b-110">如果希望单个变量保存多个相关的信息片段，则结构非常有用。</span><span class="sxs-lookup"><span data-stu-id="fec5b-110">Structures are useful when you want a single variable to hold several related pieces of information.</span></span> <span data-ttu-id="fec5b-111">例如，你可能想要将雇员姓名、电话分机号码和薪金一起保留在一起。</span><span class="sxs-lookup"><span data-stu-id="fec5b-111">For example, you might want to keep an employee's name, telephone extension, and salary together.</span></span> <span data-ttu-id="fec5b-112">您可以为此信息使用几个变量，或者可以定义一个结构并将其用于单个员工变量。</span><span class="sxs-lookup"><span data-stu-id="fec5b-112">You could use several variables for this information, or you could define a structure and use it for a single employee variable.</span></span> <span data-ttu-id="fec5b-113">当你有许多员工，而此变量的多个实例时，结构的优势就变得很明显。</span><span class="sxs-lookup"><span data-stu-id="fec5b-113">The advantage of the structure becomes apparent when you have many employees and therefore many instances of the variable.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="fec5b-114">本节内容</span><span class="sxs-lookup"><span data-stu-id="fec5b-114">In This Section</span></span>  

 [<span data-ttu-id="fec5b-115">如何：声明结构</span><span class="sxs-lookup"><span data-stu-id="fec5b-115">How to: Declare a Structure</span></span>](how-to-declare-a-structure.md)  
 <span data-ttu-id="fec5b-116">演示如何声明结构及其元素。</span><span class="sxs-lookup"><span data-stu-id="fec5b-116">Shows how to declare a structure and its elements.</span></span>  
  
 [<span data-ttu-id="fec5b-117">结构变量</span><span class="sxs-lookup"><span data-stu-id="fec5b-117">Structure Variables</span></span>](structure-variables.md)  
 <span data-ttu-id="fec5b-118">介绍如何将结构分配给变量并访问其元素。</span><span class="sxs-lookup"><span data-stu-id="fec5b-118">Covers assigning a structure to a variable and accessing its elements.</span></span>  
  
 [<span data-ttu-id="fec5b-119">结构和其他编程元素</span><span class="sxs-lookup"><span data-stu-id="fec5b-119">Structures and Other Programming Elements</span></span>](structures-and-other-programming-elements.md)  
 <span data-ttu-id="fec5b-120">概述结构如何与数组、对象、过程相互交互。</span><span class="sxs-lookup"><span data-stu-id="fec5b-120">Summarizes how structures interact with arrays, objects, procedures, and each other.</span></span>  
  
 [<span data-ttu-id="fec5b-121">结构和类</span><span class="sxs-lookup"><span data-stu-id="fec5b-121">Structures and Classes</span></span>](structures-and-classes.md)  
 <span data-ttu-id="fec5b-122">描述结构和类之间的相似性和差异。</span><span class="sxs-lookup"><span data-stu-id="fec5b-122">Describes the similarities and differences between structures and classes.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="fec5b-123">相关章节</span><span class="sxs-lookup"><span data-stu-id="fec5b-123">Related Sections</span></span>  

 [<span data-ttu-id="fec5b-124">数据类型</span><span class="sxs-lookup"><span data-stu-id="fec5b-124">Data Types</span></span>](index.md)  
 <span data-ttu-id="fec5b-125">介绍 Visual Basic 数据类型，并说明如何使用它们。</span><span class="sxs-lookup"><span data-stu-id="fec5b-125">Introduces the Visual Basic data types and describes how to use them.</span></span>  
  
 [<span data-ttu-id="fec5b-126">数据类型</span><span class="sxs-lookup"><span data-stu-id="fec5b-126">Data Types</span></span>](../../../language-reference/data-types/index.md)  
 <span data-ttu-id="fec5b-127">列出 Visual Basic 提供的基本数据类型。</span><span class="sxs-lookup"><span data-stu-id="fec5b-127">Lists the elementary data types supplied by Visual Basic.</span></span>
