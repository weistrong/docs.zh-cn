---
description: 了解详细信息： Module 语句
title: Module 语句
ms.date: 07/20/2015
f1_keywords:
- Module
- vb.Module
helpviewer_keywords:
- modules, classes
- modules
- Module statement [Visual Basic]
- modules, declaring
- standard modules
- classes [Visual Basic], vs. modules
- declarations [Visual Basic], modules
ms.assetid: a1243afc-14a5-45df-95d5-51118aeac362
ms.openlocfilehash: 2a19bcfa4521d34b5a91fbc9de412a6d8f6f39c0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99768865"
---
# <a name="module-statement"></a><span data-ttu-id="8d9f9-103">Module 语句</span><span class="sxs-lookup"><span data-stu-id="8d9f9-103">Module Statement</span></span>

<span data-ttu-id="8d9f9-104">声明模块的名称，并引入模块包含的变量、属性、事件和过程的定义。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-104">Declares the name of a module and introduces the definition of the variables, properties, events, and procedures that the module comprises.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d9f9-105">语法</span><span class="sxs-lookup"><span data-stu-id="8d9f9-105">Syntax</span></span>

```vb
[ <attributelist> ] [ accessmodifier ]  Module name
    [ statements ]
End Module
```

## <a name="parts"></a><span data-ttu-id="8d9f9-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="8d9f9-106">Parts</span></span>

`attributelist`  
<span data-ttu-id="8d9f9-107">可选。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-107">Optional.</span></span> <span data-ttu-id="8d9f9-108">请参阅 [特性列表](attribute-list.md)。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-108">See [Attribute List](attribute-list.md).</span></span>

`accessmodifier`  
<span data-ttu-id="8d9f9-109">可选。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-109">Optional.</span></span> <span data-ttu-id="8d9f9-110">可以是以下其中一个值：</span><span class="sxs-lookup"><span data-stu-id="8d9f9-110">Can be one of the following:</span></span>

- [<span data-ttu-id="8d9f9-111">公共</span><span class="sxs-lookup"><span data-stu-id="8d9f9-111">Public</span></span>](../modifiers/public.md)

- [<span data-ttu-id="8d9f9-112">Friend</span><span class="sxs-lookup"><span data-stu-id="8d9f9-112">Friend</span></span>](../modifiers/friend.md)

<span data-ttu-id="8d9f9-113">请参阅 [Visual Basic 中的访问级别](../../programming-guide/language-features/declared-elements/access-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-113">See [Access levels in Visual Basic](../../programming-guide/language-features/declared-elements/access-levels.md).</span></span>

`name`  
<span data-ttu-id="8d9f9-114">必需。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-114">Required.</span></span> <span data-ttu-id="8d9f9-115">此模块的名称。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-115">Name of this module.</span></span> <span data-ttu-id="8d9f9-116">请参阅 [Declared Element Names](../../programming-guide/language-features/declared-elements/declared-element-names.md)。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-116">See [Declared Element Names](../../programming-guide/language-features/declared-elements/declared-element-names.md).</span></span>

`statements`  
<span data-ttu-id="8d9f9-117">可选。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-117">Optional.</span></span> <span data-ttu-id="8d9f9-118">定义此模块的变量、属性、事件、过程和嵌套类型的语句。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-118">Statements which define the variables, properties, events, procedures, and nested types of this module.</span></span>

`End Module`  
<span data-ttu-id="8d9f9-119">终止 `Module` 定义。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-119">Terminates the `Module` definition.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d9f9-120">备注</span><span class="sxs-lookup"><span data-stu-id="8d9f9-120">Remarks</span></span>

<span data-ttu-id="8d9f9-121">`Module`语句定义在其命名空间中可用的引用类型。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-121">A `Module` statement defines a reference type available throughout its namespace.</span></span> <span data-ttu-id="8d9f9-122">*模块* (有时称为 *标准模块*) 与类相似，但有一些重要的区别。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-122">A *module* (sometimes called a *standard module*) is similar to a class but with some important distinctions.</span></span> <span data-ttu-id="8d9f9-123">每个模块都有一个实例，无需创建或分配给变量。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-123">Every module has exactly one instance and does not need to be created or assigned to a variable.</span></span> <span data-ttu-id="8d9f9-124">模块不支持继承或实现接口。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-124">Modules do not support inheritance or implement interfaces.</span></span> <span data-ttu-id="8d9f9-125">请注意，如果某个模块不是类或结构的 *类型* ，则不能将编程元素声明为具有模块的数据类型。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-125">Notice that a module is not a *type* in the sense that a class or structure is — you cannot declare a programming element to have the data type of a module.</span></span>

<span data-ttu-id="8d9f9-126">只能 `Module` 在命名空间级别使用。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-126">You can use `Module` only at namespace level.</span></span> <span data-ttu-id="8d9f9-127">这意味着模块的 *声明上下文* 必须是源文件或命名空间，不能是类、结构、模块、接口、过程或块。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-127">This means the *declaration context* for a module must be a source file or namespace, and cannot be a class, structure, module, interface, procedure, or block.</span></span> <span data-ttu-id="8d9f9-128">不能将模块嵌套在其他模块或任何类型中。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-128">You cannot nest a module within another module, or within any type.</span></span> <span data-ttu-id="8d9f9-129">有关详细信息，请参阅[声明上下文和默认访问级别](declaration-contexts-and-default-access-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-129">For more information, see [Declaration Contexts and Default Access Levels](declaration-contexts-and-default-access-levels.md).</span></span>

<span data-ttu-id="8d9f9-130">模块与程序具有相同的生存期。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-130">A module has the same lifetime as your program.</span></span> <span data-ttu-id="8d9f9-131">因为其成员都是 `Shared` ，所以它们的生存期也等于程序的生存期。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-131">Because its members are all `Shared`, they also have lifetimes equal to that of the program.</span></span>

<span data-ttu-id="8d9f9-132">模块默认为 [Friend](../modifiers/friend.md) 访问。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-132">Modules default to [Friend](../modifiers/friend.md) access.</span></span> <span data-ttu-id="8d9f9-133">您可以使用访问修饰符调整其访问级别。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-133">You can adjust their access levels with the access modifiers.</span></span> <span data-ttu-id="8d9f9-134">有关详细信息，请参阅 [Visual Basic 中的访问级别](../../programming-guide/language-features/declared-elements/access-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-134">For more information, see [Access levels in Visual Basic](../../programming-guide/language-features/declared-elements/access-levels.md).</span></span>

<span data-ttu-id="8d9f9-135">模块的所有成员都是隐式的 `Shared` 。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-135">All members of a module are implicitly `Shared`.</span></span>

## <a name="classes-and-modules"></a><span data-ttu-id="8d9f9-136">类和模块</span><span class="sxs-lookup"><span data-stu-id="8d9f9-136">Classes and Modules</span></span>

<span data-ttu-id="8d9f9-137">这些元素具有许多相似之处，但也存在一些重要的差异。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-137">These elements have many similarities, but there are some important differences as well.</span></span>

- <span data-ttu-id="8d9f9-138">**术语。**</span><span class="sxs-lookup"><span data-stu-id="8d9f9-138">**Terminology.**</span></span> <span data-ttu-id="8d9f9-139">Visual Basic 的早期版本可识别两种类型的模块： *类模块* ( cls 文件) 和 *标准模块* ( bas 文件) 。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-139">Previous versions of Visual Basic recognize two types of modules: *class modules* (.cls files) and *standard modules* (.bas files).</span></span> <span data-ttu-id="8d9f9-140">当前版本分别调用这些 *类* 和 *模块*。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-140">The current version calls these *classes* and *modules*, respectively.</span></span>

- <span data-ttu-id="8d9f9-141">**共享成员。**</span><span class="sxs-lookup"><span data-stu-id="8d9f9-141">**Shared Members.**</span></span> <span data-ttu-id="8d9f9-142">您可以控制某个类的成员是共享成员还是实例成员。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-142">You can control whether a member of a class is a shared or instance member.</span></span>

- <span data-ttu-id="8d9f9-143">**对象方向。**</span><span class="sxs-lookup"><span data-stu-id="8d9f9-143">**Object Orientation.**</span></span> <span data-ttu-id="8d9f9-144">类是面向对象的，但模块不是。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-144">Classes are object-oriented, but modules are not.</span></span> <span data-ttu-id="8d9f9-145">因此，只有类可以实例化为对象。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-145">So only classes can be instantiated as objects.</span></span> <span data-ttu-id="8d9f9-146">有关详细信息，请参阅 [对象和类](../../programming-guide/language-features/objects-and-classes/index.md)。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-146">For more information, see [Objects and Classes](../../programming-guide/language-features/objects-and-classes/index.md).</span></span>

## <a name="rules"></a><span data-ttu-id="8d9f9-147">规则</span><span class="sxs-lookup"><span data-stu-id="8d9f9-147">Rules</span></span>

- <span data-ttu-id="8d9f9-148">**组成.**</span><span class="sxs-lookup"><span data-stu-id="8d9f9-148">**Modifiers.**</span></span> <span data-ttu-id="8d9f9-149">所有模块成员都是隐式 [共享](../modifiers/shared.md)的。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-149">All module members are implicitly [Shared](../modifiers/shared.md).</span></span> <span data-ttu-id="8d9f9-150">不能在 `Shared` 声明成员时使用关键字，也不能更改任何成员的共享状态。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-150">You cannot use the `Shared` keyword when declaring a member, and you cannot alter the shared status of any member.</span></span>

- <span data-ttu-id="8d9f9-151">**继承.**</span><span class="sxs-lookup"><span data-stu-id="8d9f9-151">**Inheritance.**</span></span> <span data-ttu-id="8d9f9-152">模块不能从 <xref:System.Object> 所有模块继承的类型继承。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-152">A module cannot inherit from any type other than <xref:System.Object>, from which all modules inherit.</span></span> <span data-ttu-id="8d9f9-153">特别是，一个模块不能从另一个模块继承。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-153">In particular, one module cannot inherit from another.</span></span>

  <span data-ttu-id="8d9f9-154">不能在模块定义中使用 [Inherits 语句](inherits-statement.md) ，甚至可以指定 <xref:System.Object> 。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-154">You cannot use the [Inherits Statement](inherits-statement.md) in a module definition, even to specify <xref:System.Object>.</span></span>

- <span data-ttu-id="8d9f9-155">**默认属性。**</span><span class="sxs-lookup"><span data-stu-id="8d9f9-155">**Default Property.**</span></span> <span data-ttu-id="8d9f9-156">不能在模块中定义任何默认属性。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-156">You cannot define any default properties in a module.</span></span> <span data-ttu-id="8d9f9-157">有关详细信息，请参阅 [默认值](../modifiers/default.md)。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-157">For more information, see [Default](../modifiers/default.md).</span></span>

## <a name="behavior"></a><span data-ttu-id="8d9f9-158">行为</span><span class="sxs-lookup"><span data-stu-id="8d9f9-158">Behavior</span></span>

- <span data-ttu-id="8d9f9-159">**访问级别。**</span><span class="sxs-lookup"><span data-stu-id="8d9f9-159">**Access Level.**</span></span> <span data-ttu-id="8d9f9-160">在模块中，你可以使用其自己的访问级别声明每个成员。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-160">Within a module, you can declare each member with its own access level.</span></span> <span data-ttu-id="8d9f9-161">模块成员默认为 [公共](../modifiers/public.md) 访问权限，变量和常量除外，默认为 [私有](../modifiers/private.md) 访问。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-161">Module members default to [Public](../modifiers/public.md) access, except variables and constants, which default to [Private](../modifiers/private.md) access.</span></span> <span data-ttu-id="8d9f9-162">当某个模块的访问权限超过其成员之一时，将优先使用指定的模块访问级别。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-162">When a module has more restricted access than one of its members, the specified module access level takes precedence.</span></span>

- <span data-ttu-id="8d9f9-163">**划分范围。**</span><span class="sxs-lookup"><span data-stu-id="8d9f9-163">**Scope.**</span></span> <span data-ttu-id="8d9f9-164">模块在其命名空间中的作用域。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-164">A module is in scope throughout its namespace.</span></span>

  <span data-ttu-id="8d9f9-165">每个模块成员的作用域都是整个模块。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-165">The scope of every module member is the entire module.</span></span> <span data-ttu-id="8d9f9-166">请注意，所有成员都接受 *类型提升*，这会导致其作用域升级到包含该模块的命名空间。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-166">Notice that all members undergo *type promotion*, which causes their scope to be promoted to the namespace containing the module.</span></span> <span data-ttu-id="8d9f9-167">有关详细信息，请参阅 [类型提升](../../programming-guide/language-features/declared-elements/type-promotion.md)。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-167">For more information, see [Type Promotion](../../programming-guide/language-features/declared-elements/type-promotion.md).</span></span>

- <span data-ttu-id="8d9f9-168">**限定.**</span><span class="sxs-lookup"><span data-stu-id="8d9f9-168">**Qualification.**</span></span> <span data-ttu-id="8d9f9-169">项目中可以有多个模块，可以在两个或多个模块中声明同名的成员。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-169">You can have multiple modules in a project, and you can declare members with the same name in two or more modules.</span></span> <span data-ttu-id="8d9f9-170">但是，如果引用来自模块外部，则必须使用适当的模块名称来限定对此类成员的任何引用。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-170">However, you must qualify any reference to such a member with the appropriate module name if the reference is from outside that module.</span></span> <span data-ttu-id="8d9f9-171">有关详细信息，请参阅 [References to Declared Elements](../../programming-guide/language-features/declared-elements/references-to-declared-elements.md)。</span><span class="sxs-lookup"><span data-stu-id="8d9f9-171">For more information, see [References to Declared Elements](../../programming-guide/language-features/declared-elements/references-to-declared-elements.md).</span></span>

## <a name="example"></a><span data-ttu-id="8d9f9-172">示例</span><span class="sxs-lookup"><span data-stu-id="8d9f9-172">Example</span></span>

[!code-vb[VbVbalrStatements#69](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#69)]

## <a name="see-also"></a><span data-ttu-id="8d9f9-173">请参阅</span><span class="sxs-lookup"><span data-stu-id="8d9f9-173">See also</span></span>

- [<span data-ttu-id="8d9f9-174">Class 语句</span><span class="sxs-lookup"><span data-stu-id="8d9f9-174">Class Statement</span></span>](class-statement.md)
- [<span data-ttu-id="8d9f9-175">Namespace 语句</span><span class="sxs-lookup"><span data-stu-id="8d9f9-175">Namespace Statement</span></span>](namespace-statement.md)
- [<span data-ttu-id="8d9f9-176">Structure 语句</span><span class="sxs-lookup"><span data-stu-id="8d9f9-176">Structure Statement</span></span>](structure-statement.md)
- [<span data-ttu-id="8d9f9-177">Interface 语句</span><span class="sxs-lookup"><span data-stu-id="8d9f9-177">Interface Statement</span></span>](interface-statement.md)
- [<span data-ttu-id="8d9f9-178">Property Statement</span><span class="sxs-lookup"><span data-stu-id="8d9f9-178">Property Statement</span></span>](property-statement.md)
- [<span data-ttu-id="8d9f9-179">类型提升</span><span class="sxs-lookup"><span data-stu-id="8d9f9-179">Type Promotion</span></span>](../../programming-guide/language-features/declared-elements/type-promotion.md)
