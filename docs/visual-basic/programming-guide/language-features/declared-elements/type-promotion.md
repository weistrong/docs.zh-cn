---
description: '了解详细信息：类型升级 (Visual Basic) '
title: 类型提升
ms.date: 07/20/2015
helpviewer_keywords:
- declared elements [Visual Basic], scope
- visibility [Visual Basic], declared elements
- Partial keyword [Visual Basic], unexpected results with type promotion
- scope [Visual Basic], declared elements
- scope [Visual Basic], Visual Basic
- type promotion
- declared elements [Visual Basic], visibility
ms.assetid: 035eeb15-e4c5-4288-ab3c-6bd5d22f7051
ms.openlocfilehash: fd8a30fb7e442d82222ae55daabf70bd8e532138
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100434714"
---
# <a name="type-promotion-visual-basic"></a><span data-ttu-id="fee83-103">类型提升 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="fee83-103">Type Promotion (Visual Basic)</span></span>

<span data-ttu-id="fee83-104">在模块中声明编程元素时 Visual Basic 会将其范围提升到包含该模块的命名空间。</span><span class="sxs-lookup"><span data-stu-id="fee83-104">When you declare a programming element in a module, Visual Basic promotes its scope to the namespace containing the module.</span></span> <span data-ttu-id="fee83-105">这称为 *类型提升*。</span><span class="sxs-lookup"><span data-stu-id="fee83-105">This is known as *type promotion*.</span></span>  
  
 <span data-ttu-id="fee83-106">下面的示例演示模块的主干定义以及该模块的两个成员。</span><span class="sxs-lookup"><span data-stu-id="fee83-106">The following example shows a skeleton definition of a module and two members of that module.</span></span>  
  
 [!code-vb[VbVbalrDeclaredElements#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDeclaredElements/VB/Class1.vb#1)]  
  
 <span data-ttu-id="fee83-107">在中 `projModule` ，在模块级别声明的编程元素将升级到 `projNamespace` 。</span><span class="sxs-lookup"><span data-stu-id="fee83-107">Within `projModule`, programming elements declared at module level are promoted to `projNamespace`.</span></span> <span data-ttu-id="fee83-108">在前面的示例中， `basicEnum` 和已 `innerClass` 升级，但不是 `numberSub` ，因为它未在模块级别声明。</span><span class="sxs-lookup"><span data-stu-id="fee83-108">In the preceding example, `basicEnum` and `innerClass` are promoted, but `numberSub` is not, because it is not declared at module level.</span></span>  
  
## <a name="effect-of-type-promotion"></a><span data-ttu-id="fee83-109">类型提升的效果</span><span class="sxs-lookup"><span data-stu-id="fee83-109">Effect of Type Promotion</span></span>  

 <span data-ttu-id="fee83-110">类型提升的影响在于，限定字符串不需要包含模块名称。</span><span class="sxs-lookup"><span data-stu-id="fee83-110">The effect of type promotion is that a qualification string does not need to include the module name.</span></span> <span data-ttu-id="fee83-111">下面的示例对上述示例中的过程进行了两次调用。</span><span class="sxs-lookup"><span data-stu-id="fee83-111">The following example makes two calls to the procedure in the preceding example.</span></span>  
  
 [!code-vb[VbVbalrDeclaredElements#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDeclaredElements/VB/Class1.vb#2)]  
  
 <span data-ttu-id="fee83-112">在前面的示例中，第一次调用使用完全限定字符串。</span><span class="sxs-lookup"><span data-stu-id="fee83-112">In the preceding example, the first call uses complete qualification strings.</span></span> <span data-ttu-id="fee83-113">但是，这不是必需的，因为类型提升。</span><span class="sxs-lookup"><span data-stu-id="fee83-113">However, this is not necessary because of type promotion.</span></span> <span data-ttu-id="fee83-114">第二次调用还访问模块的成员，而不包括 `projModule` 在限定字符串中。</span><span class="sxs-lookup"><span data-stu-id="fee83-114">The second call also accesses the module's members without including `projModule` in the qualification strings.</span></span>  
  
## <a name="defeat-of-type-promotion"></a><span data-ttu-id="fee83-115">类型提升的失效</span><span class="sxs-lookup"><span data-stu-id="fee83-115">Defeat of Type Promotion</span></span>  

 <span data-ttu-id="fee83-116">如果命名空间已具有与模块成员同名的成员，则该模块成员的类型提升会失效。</span><span class="sxs-lookup"><span data-stu-id="fee83-116">If the namespace already has a member with the same name as a module member, type promotion is defeated for that module member.</span></span> <span data-ttu-id="fee83-117">下面的示例演示了枚举的主干定义和同一命名空间中的模块。</span><span class="sxs-lookup"><span data-stu-id="fee83-117">The following example shows a skeleton definition of an enumeration and a module within the same namespace.</span></span>  
  
 [!code-vb[VbVbalrDeclaredElements#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDeclaredElements/VB/Class1.vb#3)]  
  
 <span data-ttu-id="fee83-118">在前面的示例中，Visual Basic 无法将类升级 `abc` 到， `thisNameSpace` 因为在命名空间级别已存在具有相同名称的枚举。</span><span class="sxs-lookup"><span data-stu-id="fee83-118">In the preceding example, Visual Basic cannot promote class `abc` to `thisNameSpace` because there is already an enumeration with the same name at namespace level.</span></span> <span data-ttu-id="fee83-119">若要访问 `abcSub` ，必须使用完全限定字符串 `thisNamespace.thisModule.abc.abcSub` 。</span><span class="sxs-lookup"><span data-stu-id="fee83-119">To access `abcSub`, you must use the full qualification string `thisNamespace.thisModule.abc.abcSub`.</span></span> <span data-ttu-id="fee83-120">但是，类 `xyz` 仍会升级，你可以 `xyzSub` 使用较短的限定字符串访问 `thisNamespace.xyz.xyzSub` 。</span><span class="sxs-lookup"><span data-stu-id="fee83-120">However, class `xyz` is still promoted, and you can access `xyzSub` with the shorter qualification string `thisNamespace.xyz.xyzSub`.</span></span>  
  
### <a name="defeat-of-type-promotion-for-partial-types"></a><span data-ttu-id="fee83-121">分部类型升级类型的不足</span><span class="sxs-lookup"><span data-stu-id="fee83-121">Defeat of Type Promotion for Partial Types</span></span>  

 <span data-ttu-id="fee83-122">如果模块内的类或结构使用 [Partial](../../../language-reference/modifiers/partial.md) 关键字，则对于该类或结构，类型提升将自动失效，无论命名空间是否具有同名的成员。</span><span class="sxs-lookup"><span data-stu-id="fee83-122">If a class or structure inside a module uses the [Partial](../../../language-reference/modifiers/partial.md) keyword, type promotion is automatically defeated for that class or structure, whether or not the namespace has a member with the same name.</span></span> <span data-ttu-id="fee83-123">模块中的其他元素仍适用于类型提升。</span><span class="sxs-lookup"><span data-stu-id="fee83-123">Other elements in the module are still eligible for type promotion.</span></span>  
  
 <span data-ttu-id="fee83-124">**什么.**</span><span class="sxs-lookup"><span data-stu-id="fee83-124">**Consequences.**</span></span> <span data-ttu-id="fee83-125">部分定义的类型提升的不足会导致意外的结果，甚至编译器错误。</span><span class="sxs-lookup"><span data-stu-id="fee83-125">Defeat of type promotion of a partial definition can cause unexpected results and even compiler errors.</span></span> <span data-ttu-id="fee83-126">下面的示例显示了一个类的主干分部定义，其中一个类位于模块中。</span><span class="sxs-lookup"><span data-stu-id="fee83-126">The following example shows skeleton partial definitions of a class, one of which is inside a module.</span></span>  
  
 [!code-vb[VbVbalrDeclaredElements#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDeclaredElements/VB/Class1.vb#4)]  
  
 <span data-ttu-id="fee83-127">在前面的示例中，开发人员可能希望编译器合并的两个分部定义 `sampleClass` 。</span><span class="sxs-lookup"><span data-stu-id="fee83-127">In the preceding example, the developer might expect the compiler to merge the two partial definitions of `sampleClass`.</span></span> <span data-ttu-id="fee83-128">但是，编译器不会考虑升级内部定义 `sampleModule` 。</span><span class="sxs-lookup"><span data-stu-id="fee83-128">However, the compiler does not consider promotion for the partial definition inside `sampleModule`.</span></span> <span data-ttu-id="fee83-129">因此，它会尝试编译两个单独的不同类，两者都命名， `sampleClass` 但具有不同的限定路径。</span><span class="sxs-lookup"><span data-stu-id="fee83-129">As a result, it attempts to compile two separate and distinct classes, both named `sampleClass` but with different qualification paths.</span></span>  
  
 <span data-ttu-id="fee83-130">仅当其完全限定的路径相同时，编译器才将合并分部定义。</span><span class="sxs-lookup"><span data-stu-id="fee83-130">The compiler merges partial definitions only when their fully qualified paths are identical.</span></span>  
  
## <a name="recommendations"></a><span data-ttu-id="fee83-131">建议</span><span class="sxs-lookup"><span data-stu-id="fee83-131">Recommendations</span></span>  

 <span data-ttu-id="fee83-132">以下建议表示良好的编程做法。</span><span class="sxs-lookup"><span data-stu-id="fee83-132">The following recommendations represent good programming practice.</span></span>  
  
- <span data-ttu-id="fee83-133">**唯一名称。**</span><span class="sxs-lookup"><span data-stu-id="fee83-133">**Unique Names.**</span></span> <span data-ttu-id="fee83-134">当你完全控制编程元素的命名时，在任何地方使用唯一名称始终是一个好主意。</span><span class="sxs-lookup"><span data-stu-id="fee83-134">When you have full control over the naming of programming elements, it is always a good idea to use unique names everywhere.</span></span> <span data-ttu-id="fee83-135">相同的名称需要额外的限制，并且可能会使代码更难以阅读。</span><span class="sxs-lookup"><span data-stu-id="fee83-135">Identical names require extra qualification and can make your code harder to read.</span></span> <span data-ttu-id="fee83-136">它们还可能导致微妙的错误和意外的结果。</span><span class="sxs-lookup"><span data-stu-id="fee83-136">They can also lead to subtle errors and unexpected results.</span></span>  
  
- <span data-ttu-id="fee83-137">**完全限定。**</span><span class="sxs-lookup"><span data-stu-id="fee83-137">**Full Qualification.**</span></span> <span data-ttu-id="fee83-138">使用同一个命名空间中的模块和其他元素时，最安全的方法是始终对所有编程元素使用完全限定。</span><span class="sxs-lookup"><span data-stu-id="fee83-138">When you are working with modules and other elements in the same namespace, the safest approach is to always use full qualification for all programming elements.</span></span> <span data-ttu-id="fee83-139">如果类型提升对于某个模块成员失效，并且你未完全限定该成员，则可能会无意中访问其他编程元素。</span><span class="sxs-lookup"><span data-stu-id="fee83-139">If type promotion is defeated for a module member and you do not fully qualify that member, you could inadvertently access a different programming element.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fee83-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="fee83-140">See also</span></span>

- [<span data-ttu-id="fee83-141">Module 语句</span><span class="sxs-lookup"><span data-stu-id="fee83-141">Module Statement</span></span>](../../../language-reference/statements/module-statement.md)
- [<span data-ttu-id="fee83-142">Namespace 语句</span><span class="sxs-lookup"><span data-stu-id="fee83-142">Namespace Statement</span></span>](../../../language-reference/statements/namespace-statement.md)
- [<span data-ttu-id="fee83-143">Partial</span><span class="sxs-lookup"><span data-stu-id="fee83-143">Partial</span></span>](../../../language-reference/modifiers/partial.md)
- [<span data-ttu-id="fee83-144">Visual Basic 中的范围</span><span class="sxs-lookup"><span data-stu-id="fee83-144">Scope in Visual Basic</span></span>](scope.md)
- [<span data-ttu-id="fee83-145">如何：控制变量的范围</span><span class="sxs-lookup"><span data-stu-id="fee83-145">How to: Control the Scope of a Variable</span></span>](how-to-control-the-scope-of-a-variable.md)
- [<span data-ttu-id="fee83-146">References to Declared Elements</span><span class="sxs-lookup"><span data-stu-id="fee83-146">References to Declared Elements</span></span>](references-to-declared-elements.md)
