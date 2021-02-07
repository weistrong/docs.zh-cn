---
description: '了解详细信息：属性列表 (Visual Basic) '
title: 特性列表
ms.date: 07/20/2015
helpviewer_keywords:
- attribute list
- attributes [Visual Basic], applying
ms.assetid: 5880073a-68a4-4b6b-8a07-ace32959a4e2
ms.openlocfilehash: bde9387a48001a2696a6f69454edc311e7597bb6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99674033"
---
# <a name="attribute-list-visual-basic"></a><span data-ttu-id="7079e-103">特性列表 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="7079e-103">Attribute List (Visual Basic)</span></span>

<span data-ttu-id="7079e-104">指定要应用于已声明的编程元素的特性。</span><span class="sxs-lookup"><span data-stu-id="7079e-104">Specifies the attributes to be applied to a declared programming element.</span></span> <span data-ttu-id="7079e-105">用逗号分隔多个属性。</span><span class="sxs-lookup"><span data-stu-id="7079e-105">Multiple attributes are separated by commas.</span></span> <span data-ttu-id="7079e-106">下面是一个属性的语法。</span><span class="sxs-lookup"><span data-stu-id="7079e-106">Following is the syntax for one attribute.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7079e-107">语法</span><span class="sxs-lookup"><span data-stu-id="7079e-107">Syntax</span></span>  
  
```vb  
[ attributemodifier ] attributename [ ( attributearguments | attributeinitializer ) ]  
```  
  
## <a name="parts"></a><span data-ttu-id="7079e-108">组成部分</span><span class="sxs-lookup"><span data-stu-id="7079e-108">Parts</span></span>  

|||
|---|---|
|`attributemodifier`|<span data-ttu-id="7079e-109">应用于源文件开头的属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="7079e-109">Required for attributes applied at the beginning of a source file.</span></span> <span data-ttu-id="7079e-110">可以是 [程序集](../modifiers/assembly.md) 或 [模块](../modifiers/module-keyword.md)。</span><span class="sxs-lookup"><span data-stu-id="7079e-110">Can be [Assembly](../modifiers/assembly.md) or [Module](../modifiers/module-keyword.md).</span></span>|
|`attributename`| <span data-ttu-id="7079e-111">必需。</span><span class="sxs-lookup"><span data-stu-id="7079e-111">Required.</span></span> <span data-ttu-id="7079e-112">属性的名称。</span><span class="sxs-lookup"><span data-stu-id="7079e-112">Name of the attribute.</span></span>|
|`attributearguments`|<span data-ttu-id="7079e-113">可选。</span><span class="sxs-lookup"><span data-stu-id="7079e-113">Optional.</span></span> <span data-ttu-id="7079e-114">此特性的位置自变量列表。</span><span class="sxs-lookup"><span data-stu-id="7079e-114">List of positional arguments for this attribute.</span></span> <span data-ttu-id="7079e-115">多个参数之间用逗号分隔。</span><span class="sxs-lookup"><span data-stu-id="7079e-115">Multiple arguments are separated by commas.</span></span>|
|`attributeinitializer`|<span data-ttu-id="7079e-116">可选。</span><span class="sxs-lookup"><span data-stu-id="7079e-116">Optional.</span></span> <span data-ttu-id="7079e-117">此特性的变量或属性初始值设定项的列表。</span><span class="sxs-lookup"><span data-stu-id="7079e-117">List of variable or property initializers for this attribute.</span></span> <span data-ttu-id="7079e-118">多个初始值设定项用逗号分隔。</span><span class="sxs-lookup"><span data-stu-id="7079e-118">Multiple initializers are separated by commas.</span></span>|
  
## <a name="remarks"></a><span data-ttu-id="7079e-119">备注</span><span class="sxs-lookup"><span data-stu-id="7079e-119">Remarks</span></span>  

 <span data-ttu-id="7079e-120">可以将一个或多个属性应用于几乎任何编程元素 (类型、过程、属性等) 。</span><span class="sxs-lookup"><span data-stu-id="7079e-120">You can apply one or more attributes to nearly any programming element (types, procedures, properties, and so forth).</span></span> <span data-ttu-id="7079e-121">特性显示在程序集的元数据中，它们可帮助你批注代码或指定如何使用特定编程元素。</span><span class="sxs-lookup"><span data-stu-id="7079e-121">Attributes appear in your assembly's metadata, and they can help you annotate your code or specify how to use a particular programming element.</span></span> <span data-ttu-id="7079e-122">您可以应用 Visual Basic 和 .NET Framework 定义的属性，并且可以定义自己的属性。</span><span class="sxs-lookup"><span data-stu-id="7079e-122">You can apply attributes defined by Visual Basic and the .NET Framework, and you can define your own attributes.</span></span>  

 <span data-ttu-id="7079e-123">有关何时使用属性的详细信息，请参阅 [属性概述](../../programming-guide/concepts/attributes/index.md)。</span><span class="sxs-lookup"><span data-stu-id="7079e-123">For more information on when to use attributes, see [Attributes overview](../../programming-guide/concepts/attributes/index.md).</span></span> <span data-ttu-id="7079e-124">有关属性名称的信息，请参阅已 [声明的元素名称](../../programming-guide/language-features/declared-elements/declared-element-names.md)。</span><span class="sxs-lookup"><span data-stu-id="7079e-124">For information on attribute names, see [Declared Element Names](../../programming-guide/language-features/declared-elements/declared-element-names.md).</span></span>  
  
## <a name="rules"></a><span data-ttu-id="7079e-125">规则</span><span class="sxs-lookup"><span data-stu-id="7079e-125">Rules</span></span>  
  
- <span data-ttu-id="7079e-126">**虚拟.**</span><span class="sxs-lookup"><span data-stu-id="7079e-126">**Placement.**</span></span> <span data-ttu-id="7079e-127">您可以将特性应用于大多数已声明的编程元素。</span><span class="sxs-lookup"><span data-stu-id="7079e-127">You can apply attributes to most declared programming elements.</span></span> <span data-ttu-id="7079e-128">若要应用一个或多个特性，请将 *特性块* 置于元素声明的开头。</span><span class="sxs-lookup"><span data-stu-id="7079e-128">To apply one or more attributes, you place an *attribute block* at the beginning of the element declaration.</span></span> <span data-ttu-id="7079e-129">"属性" 列表中的每个条目指定要应用的属性，以及用于此属性调用的修饰符和参数。</span><span class="sxs-lookup"><span data-stu-id="7079e-129">Each entry in the attribute list specifies an attribute you wish to apply, and the modifier and arguments you are using for this invocation of the attribute.</span></span>  
  
- <span data-ttu-id="7079e-130">**尖括号。**</span><span class="sxs-lookup"><span data-stu-id="7079e-130">**Angle Brackets.**</span></span> <span data-ttu-id="7079e-131">如果提供了属性列表，则必须将其括在尖括号中 ( " `<` " 和 " `>` " ) 。</span><span class="sxs-lookup"><span data-stu-id="7079e-131">If you supply an attribute list, you must enclose it in angle brackets ("`<`" and "`>`").</span></span>  
  
- <span data-ttu-id="7079e-132">**声明的一部分。**</span><span class="sxs-lookup"><span data-stu-id="7079e-132">**Part of the Declaration.**</span></span> <span data-ttu-id="7079e-133">特性必须是元素声明的一部分，而不是单独的语句。</span><span class="sxs-lookup"><span data-stu-id="7079e-133">The attribute must be part of the element declaration, not a separate statement.</span></span> <span data-ttu-id="7079e-134">您可以使用行继续符序列 ( " `_` " ) 将声明语句扩展到多个源代码行上。</span><span class="sxs-lookup"><span data-stu-id="7079e-134">You can use the line-continuation sequence (" `_`") to extend the declaration statement onto multiple source-code lines.</span></span>  
  
- <span data-ttu-id="7079e-135">**组成.**</span><span class="sxs-lookup"><span data-stu-id="7079e-135">**Modifiers.**</span></span> <span data-ttu-id="7079e-136">`Assembly` `Module` 在源文件开头应用于编程元素的每个特性都需要 (或) 属性修饰符。</span><span class="sxs-lookup"><span data-stu-id="7079e-136">An attribute modifier (`Assembly` or `Module`) is required on every attribute applied to a programming element at the beginning of a source file.</span></span> <span data-ttu-id="7079e-137">应用于不在源文件开头的元素的特性上不允许使用特性修饰符。</span><span class="sxs-lookup"><span data-stu-id="7079e-137">Attribute modifiers are not allowed on attributes applied to elements that are not at the beginning of a source file.</span></span>  
  
- <span data-ttu-id="7079e-138">**形参.**</span><span class="sxs-lookup"><span data-stu-id="7079e-138">**Arguments.**</span></span> <span data-ttu-id="7079e-139">特性的所有位置参数都必须在任何变量或属性初始值设定项之前。</span><span class="sxs-lookup"><span data-stu-id="7079e-139">All positional arguments for an attribute must precede any variable or property initializers.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7079e-140">示例</span><span class="sxs-lookup"><span data-stu-id="7079e-140">Example</span></span>  

 <span data-ttu-id="7079e-141">下面的示例将属性应用于 <xref:System.Runtime.InteropServices.DllImportAttribute> 过程的主干定义 `Function` 。</span><span class="sxs-lookup"><span data-stu-id="7079e-141">The following example applies the <xref:System.Runtime.InteropServices.DllImportAttribute> attribute to a skeleton definition of a `Function` procedure.</span></span>  
  
 [!code-vb[VbVbalrStatements#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#1)]  
  
 <span data-ttu-id="7079e-142"><xref:System.Runtime.InteropServices.DllImportAttribute> 指示特性化过程表示非托管动态链接库中的入口点 (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="7079e-142"><xref:System.Runtime.InteropServices.DllImportAttribute> indicates that the attributed procedure represents an entry point in an unmanaged dynamic-link library (DLL).</span></span> <span data-ttu-id="7079e-143">特性提供 DLL 名称作为位置参数，将其他信息作为变量初始值设定项提供。</span><span class="sxs-lookup"><span data-stu-id="7079e-143">The attribute supplies the DLL name as a positional argument and the other information as variable initializers.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7079e-144">请参阅</span><span class="sxs-lookup"><span data-stu-id="7079e-144">See also</span></span>

- [<span data-ttu-id="7079e-145">程序集</span><span class="sxs-lookup"><span data-stu-id="7079e-145">Assembly</span></span>](../modifiers/assembly.md)
- [<span data-ttu-id="7079e-146">模块 \<keyword></span><span class="sxs-lookup"><span data-stu-id="7079e-146">Module \<keyword></span></span>](../modifiers/module-keyword.md)
- [<span data-ttu-id="7079e-147">属性概述</span><span class="sxs-lookup"><span data-stu-id="7079e-147">Attributes overview</span></span>](../../programming-guide/concepts/attributes/index.md)
- [<span data-ttu-id="7079e-148">如何：在代码中拆分和合并语句</span><span class="sxs-lookup"><span data-stu-id="7079e-148">How to: Break and Combine Statements in Code</span></span>](../../programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md)
