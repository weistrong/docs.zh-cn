---
description: 了解详细信息： Property 语句
title: Property Statement
ms.date: 05/12/2018
f1_keywords:
- vb.PropertySet
- vb.Property
- vb.PropertyGet
helpviewer_keywords:
- Property statement [Visual Basic]
- default modifier
- property procedures [Visual Basic], Property statements
- Property keyword [Visual Basic]
ms.assetid: 3155edaf-8ebd-45c6-9cef-11d5d2dc8d38
ms.openlocfilehash: 95f2ac1f993fc8698d2033dfe50d925cd55a7dc4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99741388"
---
# <a name="property-statement"></a><span data-ttu-id="99ef3-103">Property Statement</span><span class="sxs-lookup"><span data-stu-id="99ef3-103">Property Statement</span></span>

<span data-ttu-id="99ef3-104">声明属性的名称，以及用于存储和检索属性值的属性过程。</span><span class="sxs-lookup"><span data-stu-id="99ef3-104">Declares the name of a property, and the property procedures used to store and retrieve the value of the property.</span></span>

## <a name="syntax"></a><span data-ttu-id="99ef3-105">语法</span><span class="sxs-lookup"><span data-stu-id="99ef3-105">Syntax</span></span>

```vb
[ <attributelist> ] [ Default ] [ accessmodifier ]
[ propertymodifiers ] [ Shared ] [ Shadows ] [ ReadOnly | WriteOnly ] [ Iterator ]
Property name ( [ parameterlist ] ) [ As returntype ] [ Implements implementslist ]
    [ <attributelist> ] [ accessmodifier ] Get
        [ statements ]
    End Get
    [ <attributelist> ] [ accessmodifier ] Set ( ByVal value As returntype [, parameterlist ] )
        [ statements ]
    End Set
End Property
- or -
[ <attributelist> ] [ Default ] [ accessmodifier ]
[ propertymodifiers ] [ Shared ] [ Shadows ] [ ReadOnly | WriteOnly ]
Property name ( [ parameterlist ] ) [ As returntype ] [ Implements implementslist ]
```

## <a name="parts"></a><span data-ttu-id="99ef3-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="99ef3-106">Parts</span></span>

- `attributelist`

  <span data-ttu-id="99ef3-107">可选。</span><span class="sxs-lookup"><span data-stu-id="99ef3-107">Optional.</span></span> <span data-ttu-id="99ef3-108">应用于此属性或或过程的特性的列表 `Get` `Set` 。</span><span class="sxs-lookup"><span data-stu-id="99ef3-108">List of attributes that apply to this property or `Get` or `Set` procedure.</span></span> <span data-ttu-id="99ef3-109">请参阅 [特性列表](attribute-list.md)。</span><span class="sxs-lookup"><span data-stu-id="99ef3-109">See [Attribute List](attribute-list.md).</span></span>

- `Default`

  <span data-ttu-id="99ef3-110">可选。</span><span class="sxs-lookup"><span data-stu-id="99ef3-110">Optional.</span></span> <span data-ttu-id="99ef3-111">指定此属性是在其上定义该属性的类或结构的默认属性。</span><span class="sxs-lookup"><span data-stu-id="99ef3-111">Specifies that this property is the default property for the class or structure on which it is defined.</span></span> <span data-ttu-id="99ef3-112">默认属性必须接受参数，并且可以在不指定属性名称的情况下进行设置和检索。</span><span class="sxs-lookup"><span data-stu-id="99ef3-112">Default properties must accept parameters and can be set and retrieved without specifying the property name.</span></span> <span data-ttu-id="99ef3-113">如果将属性声明为 `Default` ，则不能 `Private` 对属性或其任一属性过程使用。</span><span class="sxs-lookup"><span data-stu-id="99ef3-113">If you declare the property as `Default`, you cannot use `Private` on the property or on either of its property procedures.</span></span>

- `accessmodifier`

  <span data-ttu-id="99ef3-114">语句上的可选 `Property` ，最多一个 `Get` 和 `Set` 语句。</span><span class="sxs-lookup"><span data-stu-id="99ef3-114">Optional on the `Property` statement and on at most one of the `Get` and `Set` statements.</span></span> <span data-ttu-id="99ef3-115">可以是以下其中一个值：</span><span class="sxs-lookup"><span data-stu-id="99ef3-115">Can be one of the following:</span></span>

  - [<span data-ttu-id="99ef3-116">公共</span><span class="sxs-lookup"><span data-stu-id="99ef3-116">Public</span></span>](../modifiers/public.md)

  - [<span data-ttu-id="99ef3-117">Protected</span><span class="sxs-lookup"><span data-stu-id="99ef3-117">Protected</span></span>](../modifiers/protected.md)

  - [<span data-ttu-id="99ef3-118">Friend</span><span class="sxs-lookup"><span data-stu-id="99ef3-118">Friend</span></span>](../modifiers/friend.md)

  - [<span data-ttu-id="99ef3-119">专用</span><span class="sxs-lookup"><span data-stu-id="99ef3-119">Private</span></span>](../modifiers/private.md)

  - [<span data-ttu-id="99ef3-120">Protected Friend</span><span class="sxs-lookup"><span data-stu-id="99ef3-120">Protected Friend</span></span>](../modifiers/protected-friend.md)

  - [<span data-ttu-id="99ef3-121">Private Protected</span><span class="sxs-lookup"><span data-stu-id="99ef3-121">Private Protected</span></span>](../modifiers/private-protected.md)

  <span data-ttu-id="99ef3-122">请参阅 [Visual Basic 中的访问级别](../../programming-guide/language-features/declared-elements/access-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="99ef3-122">See [Access levels in Visual Basic](../../programming-guide/language-features/declared-elements/access-levels.md).</span></span>

- `propertymodifiers`

  <span data-ttu-id="99ef3-123">可选。</span><span class="sxs-lookup"><span data-stu-id="99ef3-123">Optional.</span></span> <span data-ttu-id="99ef3-124">可以是以下其中一个值：</span><span class="sxs-lookup"><span data-stu-id="99ef3-124">Can be one of the following:</span></span>

  - [<span data-ttu-id="99ef3-125">重载</span><span class="sxs-lookup"><span data-stu-id="99ef3-125">Overloads</span></span>](../modifiers/overloads.md)

  - [<span data-ttu-id="99ef3-126">替代</span><span class="sxs-lookup"><span data-stu-id="99ef3-126">Overrides</span></span>](../modifiers/overrides.md)

  - [<span data-ttu-id="99ef3-127">Overrides</span><span class="sxs-lookup"><span data-stu-id="99ef3-127">Overridable</span></span>](../modifiers/overridable.md)

  - [<span data-ttu-id="99ef3-128">NotOverridable</span><span class="sxs-lookup"><span data-stu-id="99ef3-128">NotOverridable</span></span>](../modifiers/notoverridable.md)

  - [<span data-ttu-id="99ef3-129">New</span><span class="sxs-lookup"><span data-stu-id="99ef3-129">MustOverride</span></span>](../modifiers/mustoverride.md)

  - `MustOverride Overrides`

  - `NotOverridable Overrides`

- `Shared`

  <span data-ttu-id="99ef3-130">可选。</span><span class="sxs-lookup"><span data-stu-id="99ef3-130">Optional.</span></span> <span data-ttu-id="99ef3-131">请参阅 [共享](../modifiers/shared.md)。</span><span class="sxs-lookup"><span data-stu-id="99ef3-131">See [Shared](../modifiers/shared.md).</span></span>

- `Shadows`

  <span data-ttu-id="99ef3-132">可选。</span><span class="sxs-lookup"><span data-stu-id="99ef3-132">Optional.</span></span> <span data-ttu-id="99ef3-133">请参阅 [阴影](../modifiers/shadows.md)。</span><span class="sxs-lookup"><span data-stu-id="99ef3-133">See [Shadows](../modifiers/shadows.md).</span></span>

- `ReadOnly`

  <span data-ttu-id="99ef3-134">可选。</span><span class="sxs-lookup"><span data-stu-id="99ef3-134">Optional.</span></span> <span data-ttu-id="99ef3-135">请参阅 [ReadOnly](../modifiers/readonly.md)。</span><span class="sxs-lookup"><span data-stu-id="99ef3-135">See [ReadOnly](../modifiers/readonly.md).</span></span>

- `WriteOnly`

  <span data-ttu-id="99ef3-136">可选。</span><span class="sxs-lookup"><span data-stu-id="99ef3-136">Optional.</span></span> <span data-ttu-id="99ef3-137">请参阅 [WriteOnly](../modifiers/writeonly.md)。</span><span class="sxs-lookup"><span data-stu-id="99ef3-137">See [WriteOnly](../modifiers/writeonly.md).</span></span>

- `Iterator`

  <span data-ttu-id="99ef3-138">可选。</span><span class="sxs-lookup"><span data-stu-id="99ef3-138">Optional.</span></span> <span data-ttu-id="99ef3-139">请参阅 [迭代器](../modifiers/iterator.md)。</span><span class="sxs-lookup"><span data-stu-id="99ef3-139">See [Iterator](../modifiers/iterator.md).</span></span>

- `name`

  <span data-ttu-id="99ef3-140">必需。</span><span class="sxs-lookup"><span data-stu-id="99ef3-140">Required.</span></span> <span data-ttu-id="99ef3-141">属性的名称。</span><span class="sxs-lookup"><span data-stu-id="99ef3-141">Name of the property.</span></span> <span data-ttu-id="99ef3-142">请参阅 [Declared Element Names](../../programming-guide/language-features/declared-elements/declared-element-names.md)。</span><span class="sxs-lookup"><span data-stu-id="99ef3-142">See [Declared Element Names](../../programming-guide/language-features/declared-elements/declared-element-names.md).</span></span>

- `parameterlist`

  <span data-ttu-id="99ef3-143">可选。</span><span class="sxs-lookup"><span data-stu-id="99ef3-143">Optional.</span></span> <span data-ttu-id="99ef3-144">表示此属性的参数的局部变量名称的列表，以及此过程的可能的其他参数 `Set` 。</span><span class="sxs-lookup"><span data-stu-id="99ef3-144">List of local variable names representing the parameters of this property, and possible additional parameters of the `Set` procedure.</span></span> <span data-ttu-id="99ef3-145">请参阅 [参数列表](parameter-list.md)。</span><span class="sxs-lookup"><span data-stu-id="99ef3-145">See [Parameter List](parameter-list.md).</span></span>

- `returntype`

  <span data-ttu-id="99ef3-146">如果 `Option Strict` 为，则为必需 `On` 。</span><span class="sxs-lookup"><span data-stu-id="99ef3-146">Required if `Option Strict` is `On`.</span></span> <span data-ttu-id="99ef3-147">此属性返回的值的数据类型。</span><span class="sxs-lookup"><span data-stu-id="99ef3-147">Data type of the value returned by this property.</span></span>

- `Implements`

  <span data-ttu-id="99ef3-148">可选。</span><span class="sxs-lookup"><span data-stu-id="99ef3-148">Optional.</span></span> <span data-ttu-id="99ef3-149">指示此属性实现一个或多个属性，每个属性都是由该属性的包含类或结构实现的接口中定义的。</span><span class="sxs-lookup"><span data-stu-id="99ef3-149">Indicates that this property implements one or more properties, each one defined in an interface implemented by this property's containing class or structure.</span></span> <span data-ttu-id="99ef3-150">请参阅 [Implements 语句](implements-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="99ef3-150">See [Implements Statement](implements-statement.md).</span></span>

- `implementslist`

  <span data-ttu-id="99ef3-151">如果提供 `Implements`，则是必需的。</span><span class="sxs-lookup"><span data-stu-id="99ef3-151">Required if `Implements` is supplied.</span></span> <span data-ttu-id="99ef3-152">要实现的属性列表。</span><span class="sxs-lookup"><span data-stu-id="99ef3-152">List of properties being implemented.</span></span>

  `implementedproperty [ , implementedproperty ... ]`

  <span data-ttu-id="99ef3-153">每个 `implementedproperty` 都具有以下语法和部件：</span><span class="sxs-lookup"><span data-stu-id="99ef3-153">Each `implementedproperty` has the following syntax and parts:</span></span>

  `interface.definedname`

  |<span data-ttu-id="99ef3-154">组成部分</span><span class="sxs-lookup"><span data-stu-id="99ef3-154">Part</span></span>|<span data-ttu-id="99ef3-155">说明</span><span class="sxs-lookup"><span data-stu-id="99ef3-155">Description</span></span>|
  |---|---|
  |`interface`|<span data-ttu-id="99ef3-156">必需。</span><span class="sxs-lookup"><span data-stu-id="99ef3-156">Required.</span></span> <span data-ttu-id="99ef3-157">此属性的包含类或结构实现的接口的名称。</span><span class="sxs-lookup"><span data-stu-id="99ef3-157">Name of an interface implemented by this property's containing class or structure.</span></span>|
  |`definedname`|<span data-ttu-id="99ef3-158">必需。</span><span class="sxs-lookup"><span data-stu-id="99ef3-158">Required.</span></span> <span data-ttu-id="99ef3-159">在其中定义属性的名称 `interface` 。</span><span class="sxs-lookup"><span data-stu-id="99ef3-159">Name by which the property is defined in `interface`.</span></span>|

- `Get`

  <span data-ttu-id="99ef3-160">可选。</span><span class="sxs-lookup"><span data-stu-id="99ef3-160">Optional.</span></span> <span data-ttu-id="99ef3-161">如果已标记属性，则为必需 `ReadOnly` 。</span><span class="sxs-lookup"><span data-stu-id="99ef3-161">Required if the property is marked `ReadOnly`.</span></span> <span data-ttu-id="99ef3-162">启动 `Get` 用于返回属性值的属性过程。</span><span class="sxs-lookup"><span data-stu-id="99ef3-162">Starts a `Get` property procedure that is used to return the value of the property.</span></span>  <span data-ttu-id="99ef3-163">`Get`语句不与[自动实现的属性](../../programming-guide/language-features/procedures/auto-implemented-properties.md)一起使用。</span><span class="sxs-lookup"><span data-stu-id="99ef3-163">The `Get` statement is not used with [auto-implemented properties](../../programming-guide/language-features/procedures/auto-implemented-properties.md).</span></span>

- `statements`

  <span data-ttu-id="99ef3-164">可选。</span><span class="sxs-lookup"><span data-stu-id="99ef3-164">Optional.</span></span> <span data-ttu-id="99ef3-165">要在或过程中运行的语句块 `Get` `Set` 。</span><span class="sxs-lookup"><span data-stu-id="99ef3-165">Block of statements to run within the `Get` or `Set` procedure.</span></span>

- `End Get`

  <span data-ttu-id="99ef3-166">终止 `Get` 属性过程。</span><span class="sxs-lookup"><span data-stu-id="99ef3-166">Terminates the `Get` property procedure.</span></span>

- `Set`

  <span data-ttu-id="99ef3-167">可选。</span><span class="sxs-lookup"><span data-stu-id="99ef3-167">Optional.</span></span> <span data-ttu-id="99ef3-168">如果已标记属性，则为必需 `WriteOnly` 。</span><span class="sxs-lookup"><span data-stu-id="99ef3-168">Required if the property is marked `WriteOnly`.</span></span> <span data-ttu-id="99ef3-169">启动 `Set` 用于存储属性值的属性过程。</span><span class="sxs-lookup"><span data-stu-id="99ef3-169">Starts a `Set` property procedure that is used to store the value of the property.</span></span>  <span data-ttu-id="99ef3-170">`Set`语句不与[自动实现的属性](../../programming-guide/language-features/procedures/auto-implemented-properties.md)一起使用。</span><span class="sxs-lookup"><span data-stu-id="99ef3-170">The `Set` statement is not used with [auto-implemented properties](../../programming-guide/language-features/procedures/auto-implemented-properties.md).</span></span>

- `End Set`

  <span data-ttu-id="99ef3-171">终止 `Set` 属性过程。</span><span class="sxs-lookup"><span data-stu-id="99ef3-171">Terminates the `Set` property procedure.</span></span>

- `End Property`

  <span data-ttu-id="99ef3-172">终止此属性的定义。</span><span class="sxs-lookup"><span data-stu-id="99ef3-172">Terminates the definition of this property.</span></span>

## <a name="remarks"></a><span data-ttu-id="99ef3-173">备注</span><span class="sxs-lookup"><span data-stu-id="99ef3-173">Remarks</span></span>

<span data-ttu-id="99ef3-174">`Property`语句引入属性的声明。</span><span class="sxs-lookup"><span data-stu-id="99ef3-174">The `Property` statement introduces the declaration of a property.</span></span> <span data-ttu-id="99ef3-175">属性可以有一个 `Get` 过程 (只读) 、 `Set` 过程 (只写) ，或是同时 (读写) 。</span><span class="sxs-lookup"><span data-stu-id="99ef3-175">A property can have a `Get` procedure (read only), a `Set` procedure (write only), or both (read-write).</span></span> <span data-ttu-id="99ef3-176">`Get` `Set` 使用自动实现的属性时，可以忽略和过程。</span><span class="sxs-lookup"><span data-stu-id="99ef3-176">You can omit the `Get` and `Set` procedure when using an auto-implemented property.</span></span> <span data-ttu-id="99ef3-177">有关详细信息，请参阅[自动实现的属性](../../programming-guide/language-features/procedures/auto-implemented-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="99ef3-177">For more information, see [Auto-Implemented Properties](../../programming-guide/language-features/procedures/auto-implemented-properties.md).</span></span>

<span data-ttu-id="99ef3-178">只能 `Property` 在类级别使用。</span><span class="sxs-lookup"><span data-stu-id="99ef3-178">You can use `Property` only at class level.</span></span> <span data-ttu-id="99ef3-179">这意味着属性的 *声明上下文* 必须是类、结构、模块或接口，不能是源文件、命名空间、过程或块。</span><span class="sxs-lookup"><span data-stu-id="99ef3-179">This means the *declaration context* for a property must be a class, structure, module, or interface, and cannot be a source file, namespace, procedure, or block.</span></span> <span data-ttu-id="99ef3-180">有关详细信息，请参阅[声明上下文和默认访问级别](declaration-contexts-and-default-access-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="99ef3-180">For more information, see [Declaration Contexts and Default Access Levels](declaration-contexts-and-default-access-levels.md).</span></span>

<span data-ttu-id="99ef3-181">默认情况下，属性使用公共访问。</span><span class="sxs-lookup"><span data-stu-id="99ef3-181">By default, properties use public access.</span></span> <span data-ttu-id="99ef3-182">您可以在语句中使用访问修饰符调整属性的访问级别 `Property` ，还可以根据需要将其一个属性过程调整到限制性更强的访问级别。</span><span class="sxs-lookup"><span data-stu-id="99ef3-182">You can adjust a property's access level with an access modifier on the `Property` statement, and you can optionally adjust one of its property procedures to a more restrictive access level.</span></span>

<span data-ttu-id="99ef3-183">Visual Basic `Set` 在属性分配过程中将参数传递给过程。</span><span class="sxs-lookup"><span data-stu-id="99ef3-183">Visual Basic passes a parameter to the `Set` procedure during property assignments.</span></span> <span data-ttu-id="99ef3-184">如果未提供参数 `Set` ，则集成开发环境 (IDE) 使用名为的隐式参数 `value` 。</span><span class="sxs-lookup"><span data-stu-id="99ef3-184">If you do not supply a parameter for `Set`, the integrated development environment (IDE) uses an implicit parameter named `value`.</span></span> <span data-ttu-id="99ef3-185">此参数保存要赋给属性的值。</span><span class="sxs-lookup"><span data-stu-id="99ef3-185">This parameter holds the value to be assigned to the property.</span></span> <span data-ttu-id="99ef3-186">通常将此值存储在私有本地变量中，并在 `Get` 调用过程时返回。</span><span class="sxs-lookup"><span data-stu-id="99ef3-186">You typically store this value in a private local variable and return it whenever the `Get` procedure is called.</span></span>

## <a name="rules"></a><span data-ttu-id="99ef3-187">规则</span><span class="sxs-lookup"><span data-stu-id="99ef3-187">Rules</span></span>

- <span data-ttu-id="99ef3-188">**混合访问级别。**</span><span class="sxs-lookup"><span data-stu-id="99ef3-188">**Mixed Access Levels.**</span></span> <span data-ttu-id="99ef3-189">如果要定义读写属性，则可以选择为或过程指定不同的访问级别 `Get` `Set` ，但不能同时指定两者。</span><span class="sxs-lookup"><span data-stu-id="99ef3-189">If you are defining a read-write property, you can optionally specify a different access level for either the `Get` or the `Set` procedure, but not both.</span></span> <span data-ttu-id="99ef3-190">如果执行此操作，则过程访问级别必须比属性的访问级别更严格。</span><span class="sxs-lookup"><span data-stu-id="99ef3-190">If you do this, the procedure access level must be more restrictive than the property's access level.</span></span> <span data-ttu-id="99ef3-191">例如，如果声明了属性 `Friend` ，则可以声明该 `Set` 过程 `Private` ，而不是 `Public` 。</span><span class="sxs-lookup"><span data-stu-id="99ef3-191">For example, if the property is declared `Friend`, you can declare the `Set` procedure `Private`, but not `Public`.</span></span>

  <span data-ttu-id="99ef3-192">如果要定义 `ReadOnly` 或 `WriteOnly` 属性，则单个属性过程 (`Get` 或 `Set` 分别) 表示所有属性。</span><span class="sxs-lookup"><span data-stu-id="99ef3-192">If you are defining a `ReadOnly` or `WriteOnly` property, the single property procedure (`Get` or `Set`, respectively) represents all of the property.</span></span> <span data-ttu-id="99ef3-193">不能为此类过程声明不同的访问级别，因为这会为属性设置两个访问级别。</span><span class="sxs-lookup"><span data-stu-id="99ef3-193">You cannot declare a different access level for such a procedure, because that would set two access levels for the property.</span></span>

- <span data-ttu-id="99ef3-194">**返回类型。**</span><span class="sxs-lookup"><span data-stu-id="99ef3-194">**Return Type.**</span></span> <span data-ttu-id="99ef3-195">`Property`语句可以声明其返回的值的数据类型。</span><span class="sxs-lookup"><span data-stu-id="99ef3-195">The `Property` statement can declare the data type of the value it returns.</span></span> <span data-ttu-id="99ef3-196">您可以指定任何数据类型或枚举、结构、类或接口的名称。</span><span class="sxs-lookup"><span data-stu-id="99ef3-196">You can specify any data type or the name of an enumeration, structure, class, or interface.</span></span>

  <span data-ttu-id="99ef3-197">如果不指定 `returntype` ，则属性将返回 `Object` 。</span><span class="sxs-lookup"><span data-stu-id="99ef3-197">If you do not specify `returntype`, the property returns `Object`.</span></span>

- <span data-ttu-id="99ef3-198">**部署.**</span><span class="sxs-lookup"><span data-stu-id="99ef3-198">**Implementation.**</span></span> <span data-ttu-id="99ef3-199">如果此属性使用 `Implements` 关键字，则包含类或结构必须 `Implements` 紧跟在其或语句后面的 `Class` 语句 `Structure` 。</span><span class="sxs-lookup"><span data-stu-id="99ef3-199">If this property uses the `Implements` keyword, the containing class or structure must have an `Implements` statement immediately following its `Class` or `Structure` statement.</span></span> <span data-ttu-id="99ef3-200">`Implements`语句必须包括中指定的每个接口 `implementslist` 。</span><span class="sxs-lookup"><span data-stu-id="99ef3-200">The `Implements` statement must include each interface specified in `implementslist`.</span></span> <span data-ttu-id="99ef3-201">但是，接口用于定义) 中的 (的名称不必与 `Property` `definedname`) 中 (的此属性的名称相同 `name` 。</span><span class="sxs-lookup"><span data-stu-id="99ef3-201">However, the name by which an interface defines the `Property` (in `definedname`) does not have to be the same as the name of this property (in `name`).</span></span>

## <a name="behavior"></a><span data-ttu-id="99ef3-202">行为</span><span class="sxs-lookup"><span data-stu-id="99ef3-202">Behavior</span></span>

- <span data-ttu-id="99ef3-203">**从属性过程返回。**</span><span class="sxs-lookup"><span data-stu-id="99ef3-203">**Returning from a Property Procedure.**</span></span> <span data-ttu-id="99ef3-204">当 `Get` 或 `Set` 过程返回到调用代码时，执行将继续执行调用它的语句后面的语句。</span><span class="sxs-lookup"><span data-stu-id="99ef3-204">When the `Get` or `Set` procedure returns to the calling code, execution continues with the statement following the statement that invoked it.</span></span>

  <span data-ttu-id="99ef3-205">`Exit Property`和 `Return` 语句导致直接从属性过程退出。</span><span class="sxs-lookup"><span data-stu-id="99ef3-205">The `Exit Property` and `Return` statements cause an immediate exit from a property procedure.</span></span> <span data-ttu-id="99ef3-206">任意数量的 `Exit Property` 和 `Return` 语句可以出现在过程中的任何位置，并且可以混合使用 `Exit Property` 和 `Return` 语句。</span><span class="sxs-lookup"><span data-stu-id="99ef3-206">Any number of `Exit Property` and `Return` statements can appear anywhere in the procedure, and you can mix `Exit Property` and `Return` statements.</span></span>

- <span data-ttu-id="99ef3-207">**返回值。**</span><span class="sxs-lookup"><span data-stu-id="99ef3-207">**Return Value.**</span></span> <span data-ttu-id="99ef3-208">若要从过程返回值 `Get` ，可以将值分配给属性名称，或者将其包含在 `Return` 语句中。</span><span class="sxs-lookup"><span data-stu-id="99ef3-208">To return a value from a `Get` procedure, you can either assign the value to the property name or include it in a `Return` statement.</span></span> <span data-ttu-id="99ef3-209">下面的示例将返回值分配给属性名称 `quoteForTheDay` ，然后使用 `Exit Property` 语句返回。</span><span class="sxs-lookup"><span data-stu-id="99ef3-209">The following example assigns the return value to the property name `quoteForTheDay` and then uses the `Exit Property` statement to return.</span></span>

  [!code-vb[VbVbalrStatements#27](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#27)]

  [!code-vb[VbVbalrStatements#28](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#28)]

  <span data-ttu-id="99ef3-210">如果在 `Exit Property` 不向赋值的情况下使用 `name` ，则该 `Get` 过程将返回属性数据类型的默认值。</span><span class="sxs-lookup"><span data-stu-id="99ef3-210">If you use `Exit Property` without assigning a value to `name`, the `Get` procedure returns the default value for the property's data type.</span></span>

  <span data-ttu-id="99ef3-211">`Return`语句同时分配 `Get` 过程返回值并退出该过程。</span><span class="sxs-lookup"><span data-stu-id="99ef3-211">The `Return` statement at the same time assigns the `Get` procedure return value and exits the procedure.</span></span> <span data-ttu-id="99ef3-212">下面的示例显示了这种情况。</span><span class="sxs-lookup"><span data-stu-id="99ef3-212">The following example shows this.</span></span>

  [!code-vb[VbVbalrStatements#27](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#27)]

  [!code-vb[VbVbalrStatements#29](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#29)]

## <a name="example"></a><span data-ttu-id="99ef3-213">示例</span><span class="sxs-lookup"><span data-stu-id="99ef3-213">Example</span></span>

<span data-ttu-id="99ef3-214">下面的示例声明类中的一个属性。</span><span class="sxs-lookup"><span data-stu-id="99ef3-214">The following example declares a property in a class.</span></span>

[!code-vb[VbVbalrStatements#51](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#51)]

## <a name="see-also"></a><span data-ttu-id="99ef3-215">请参阅</span><span class="sxs-lookup"><span data-stu-id="99ef3-215">See also</span></span>

- [<span data-ttu-id="99ef3-216">自动实现的属性</span><span class="sxs-lookup"><span data-stu-id="99ef3-216">Auto-Implemented Properties</span></span>](../../programming-guide/language-features/procedures/auto-implemented-properties.md)
- [<span data-ttu-id="99ef3-217">对象和类</span><span class="sxs-lookup"><span data-stu-id="99ef3-217">Objects and Classes</span></span>](../../programming-guide/language-features/objects-and-classes/index.md)
- [<span data-ttu-id="99ef3-218">Get 语句</span><span class="sxs-lookup"><span data-stu-id="99ef3-218">Get Statement</span></span>](get-statement.md)
- [<span data-ttu-id="99ef3-219">Set 语句</span><span class="sxs-lookup"><span data-stu-id="99ef3-219">Set Statement</span></span>](set-statement.md)
- [<span data-ttu-id="99ef3-220">参数列表</span><span class="sxs-lookup"><span data-stu-id="99ef3-220">Parameter List</span></span>](parameter-list.md)
- [<span data-ttu-id="99ef3-221">默认</span><span class="sxs-lookup"><span data-stu-id="99ef3-221">Default</span></span>](../modifiers/default.md)
