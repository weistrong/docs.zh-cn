---
description: 了解详细信息：选项推断语句
title: Option Infer 语句
ms.date: 07/20/2015
f1_keywords:
- vb.OptionInfer
- vb.Infer
helpviewer_keywords:
- variables [Visual Basic], declaring
- Option Infer statement [Visual Basic]
- Infer keyword [Visual Basic]
- declaring variables [Visual Basic], inferred
- inferred variable declaration
ms.assetid: 4ad3e6e9-8f5b-4209-a248-de22ef6e4652
ms.openlocfilehash: d0c3de7bdafb7e9b361da7a8538046e3d76b5ce7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99741583"
---
# <a name="option-infer-statement"></a><span data-ttu-id="10978-103">Option Infer 语句</span><span class="sxs-lookup"><span data-stu-id="10978-103">Option Infer Statement</span></span>

<span data-ttu-id="10978-104">允许声明变量时使用局部类型推理。</span><span class="sxs-lookup"><span data-stu-id="10978-104">Enables the use of local type inference in declaring variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="10978-105">语法</span><span class="sxs-lookup"><span data-stu-id="10978-105">Syntax</span></span>

```vb
Option Infer { On | Off }
```

## <a name="parts"></a><span data-ttu-id="10978-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="10978-106">Parts</span></span>

|<span data-ttu-id="10978-107">术语</span><span class="sxs-lookup"><span data-stu-id="10978-107">Term</span></span>|<span data-ttu-id="10978-108">定义</span><span class="sxs-lookup"><span data-stu-id="10978-108">Definition</span></span>|
|---|---|
|`On`|<span data-ttu-id="10978-109">可选。</span><span class="sxs-lookup"><span data-stu-id="10978-109">Optional.</span></span> <span data-ttu-id="10978-110">启用局部类型推理。</span><span class="sxs-lookup"><span data-stu-id="10978-110">Enables local type inference.</span></span>|
|`Off`|<span data-ttu-id="10978-111">可选。</span><span class="sxs-lookup"><span data-stu-id="10978-111">Optional.</span></span> <span data-ttu-id="10978-112">禁用局部类型推理。</span><span class="sxs-lookup"><span data-stu-id="10978-112">Disables local type inference.</span></span>|

## <a name="remarks"></a><span data-ttu-id="10978-113">备注</span><span class="sxs-lookup"><span data-stu-id="10978-113">Remarks</span></span>

<span data-ttu-id="10978-114">若要在文件中设置 `Option Infer`，请在任何其他源代码之前、文件顶部键入 `Option Infer On` 或 `Option Infer Off`。</span><span class="sxs-lookup"><span data-stu-id="10978-114">To set `Option Infer` in a file, type `Option Infer On` or `Option Infer Off` at the top of the file, before any other source code.</span></span> <span data-ttu-id="10978-115">如果为文件中 `Option Infer` 设置的值与在 IDE 中或在命令行上设置的值冲突，则文件中的值优先。</span><span class="sxs-lookup"><span data-stu-id="10978-115">If the value set for `Option Infer` in a file conflicts with the value set in the IDE or on the command line, the value in the file has precedence.</span></span>

<span data-ttu-id="10978-116">将 `Option Infer` 设置为 `On`时，你可以无需显式声明数据类型就声明本地变量。</span><span class="sxs-lookup"><span data-stu-id="10978-116">When you set `Option Infer` to `On`, you can declare local variables without explicitly stating a data type.</span></span> <span data-ttu-id="10978-117">编译器会从其初始化表达式的类型推断出变量的数据类型。</span><span class="sxs-lookup"><span data-stu-id="10978-117">The compiler infers the data type of a variable from the type of its initialization expression.</span></span>

<span data-ttu-id="10978-118">在下图中，`Option Infer` 处于打开状态。</span><span class="sxs-lookup"><span data-stu-id="10978-118">In the following illustration, `Option Infer` is turned on.</span></span> <span data-ttu-id="10978-119">声明 `Dim someVar = 2` 中的变量由类型推理声明为整数。</span><span class="sxs-lookup"><span data-stu-id="10978-119">The variable in the declaration `Dim someVar = 2` is declared as an integer by type inference.</span></span>

<span data-ttu-id="10978-120">以下屏幕截图显示了选项推断为启用时的 IntelliSense：</span><span class="sxs-lookup"><span data-stu-id="10978-120">The following screenshot shows IntelliSense when Option Infer is on:</span></span>

![当选项推断为 on 时显示 IntelliSense 视图的屏幕截图。](./media/option-infer-statement/option-infer-as-integer-on.png)

<span data-ttu-id="10978-122">在下图中，`Option Infer` 处于关闭状态。</span><span class="sxs-lookup"><span data-stu-id="10978-122">In the following illustration, `Option Infer` is turned off.</span></span> <span data-ttu-id="10978-123">声明 `Dim someVar = 2` 中的变量由类型推理声明为 `Object`。</span><span class="sxs-lookup"><span data-stu-id="10978-123">The variable in the declaration `Dim someVar = 2` is declared as an `Object` by type inference.</span></span> <span data-ttu-id="10978-124">在此示例中，"编译" 页上的 " **Option Strict** " 设置设置为 " **关闭** " [，而 "项目设计器" (Visual Basic)](/visualstudio/ide/reference/compile-page-project-designer-visual-basic)。</span><span class="sxs-lookup"><span data-stu-id="10978-124">In this example, the **Option Strict** setting is set to **Off** on the [Compile Page, Project Designer (Visual Basic)](/visualstudio/ide/reference/compile-page-project-designer-visual-basic).</span></span>

<span data-ttu-id="10978-125">以下屏幕截图显示了选项推断为 off 时的 IntelliSense：</span><span class="sxs-lookup"><span data-stu-id="10978-125">The following screenshot shows IntelliSense when Option Infer is off:</span></span>

![当选项推理为 off 时显示 IntelliSense 视图的屏幕截图。](./media/option-infer-statement/option-infer-as-object-off.png)

> [!NOTE]
> <span data-ttu-id="10978-127">变量声明为 `Object` 时，可在程序运行时更改运行时类型。</span><span class="sxs-lookup"><span data-stu-id="10978-127">When a variable is declared as an `Object`, the run-time type can change while the program is running.</span></span> <span data-ttu-id="10978-128">Visual Basic 执行称为 *装箱* 和 *取消装箱* 的操作，以便在 `Object` 和值类型之间进行转换，这会使执行速度变慢。</span><span class="sxs-lookup"><span data-stu-id="10978-128">Visual Basic performs operations called *boxing* and *unboxing* to convert between an `Object` and a value type, which makes execution slower.</span></span> <span data-ttu-id="10978-129">有关装箱和取消装箱的信息，请参阅 [Visual Basic 语言规范](~/_vblang/spec/conversions.md#value-type-conversions)。</span><span class="sxs-lookup"><span data-stu-id="10978-129">For information about boxing and unboxing, see the [Visual Basic Language Specification](~/_vblang/spec/conversions.md#value-type-conversions).</span></span>

<span data-ttu-id="10978-130">类型推理适用于过程级，且在类、结构、模块或接口中的过程之外不适用。</span><span class="sxs-lookup"><span data-stu-id="10978-130">Type inference applies at the procedure level, and does not apply outside a procedure in a class, structure, module, or interface.</span></span>

<span data-ttu-id="10978-131">有关其他信息，请参阅 [局部类型推理](../../programming-guide/language-features/variables/local-type-inference.md)。</span><span class="sxs-lookup"><span data-stu-id="10978-131">For additional information, see [Local Type Inference](../../programming-guide/language-features/variables/local-type-inference.md).</span></span>

## <a name="when-an-option-infer-statement-is-not-present"></a><span data-ttu-id="10978-132">当 Option Infer 语句不存在时</span><span class="sxs-lookup"><span data-stu-id="10978-132">When an Option Infer Statement Is Not Present</span></span>

<span data-ttu-id="10978-133">如果源代码不包含 `Option Infer` 语句，则在 "编译" 页上 **选择 "推断** 设置"，将使用 " [项目设计器" (Visual Basic)](/visualstudio/ide/reference/compile-page-project-designer-visual-basic) 。</span><span class="sxs-lookup"><span data-stu-id="10978-133">If the source code does not contain an `Option Infer` statement, the **Option Infer** setting on the [Compile Page, Project Designer (Visual Basic)](/visualstudio/ide/reference/compile-page-project-designer-visual-basic) is used.</span></span> <span data-ttu-id="10978-134">如果使用命令行编译器，则使用 [-optioninfer](../../reference/command-line-compiler/optioninfer.md) 编译器选项。</span><span class="sxs-lookup"><span data-stu-id="10978-134">If the command-line compiler is used, the [-optioninfer](../../reference/command-line-compiler/optioninfer.md) compiler option is used.</span></span>

#### <a name="to-set-option-infer-in-the-ide"></a><span data-ttu-id="10978-135">若要在 IDE 中设置 Option Infer</span><span class="sxs-lookup"><span data-stu-id="10978-135">To set Option Infer in the IDE</span></span>

1. <span data-ttu-id="10978-136">在“解决方案资源管理器”中，选择一个项目。</span><span class="sxs-lookup"><span data-stu-id="10978-136">In **Solution Explorer**, select a project.</span></span> <span data-ttu-id="10978-137">在“项目”菜单上，单击“属性” 。</span><span class="sxs-lookup"><span data-stu-id="10978-137">On the **Project** menu, click **Properties**.</span></span>

2. <span data-ttu-id="10978-138">单击“编译”选项卡。</span><span class="sxs-lookup"><span data-stu-id="10978-138">Click the **Compile** tab.</span></span>

3. <span data-ttu-id="10978-139">设置 " **选项推断** 框" 中的值。</span><span class="sxs-lookup"><span data-stu-id="10978-139">Set the value in the **Option infer** box.</span></span>

<span data-ttu-id="10978-140">创建新项目时，"**编译**" 选项卡上的 "**选择推断** 设置" 设置为 " **VB 默认值**" 对话框中的 "推断设置"**选项**。</span><span class="sxs-lookup"><span data-stu-id="10978-140">When you create a new project, the **Option Infer** setting on the **Compile** tab is set to the **Option Infer** setting in the **VB Defaults** dialog box.</span></span> <span data-ttu-id="10978-141">若要访问 " **VB 默认值** " 对话框，请在 " **工具** " 菜单上单击 " **选项**"。</span><span class="sxs-lookup"><span data-stu-id="10978-141">To access the **VB Defaults** dialog box, on the **Tools** menu, click **Options**.</span></span> <span data-ttu-id="10978-142">在“选项”对话框中，展开“项目和解决方案”，然后单击“VB 默认值”。</span><span class="sxs-lookup"><span data-stu-id="10978-142">In the **Options** dialog box, expand **Projects and Solutions**, and then click **VB Defaults**.</span></span> <span data-ttu-id="10978-143">**VB 默认** 设置中的初始默认设置为 `On` 。</span><span class="sxs-lookup"><span data-stu-id="10978-143">The initial default setting in **VB Defaults** is `On`.</span></span>

#### <a name="to-set-option-infer-on-the-command-line"></a><span data-ttu-id="10978-144">若要设置命令行上的 Option Infer</span><span class="sxs-lookup"><span data-stu-id="10978-144">To set Option Infer on the command line</span></span>

<span data-ttu-id="10978-145">在 **vbc** 命令中包含 [-optioninfer](../../reference/command-line-compiler/optioninfer.md)编译器选项。</span><span class="sxs-lookup"><span data-stu-id="10978-145">Include the [-optioninfer](../../reference/command-line-compiler/optioninfer.md) compiler option in the **vbc** command.</span></span>

## <a name="default-data-types-and-values"></a><span data-ttu-id="10978-146">默认数据类型和值</span><span class="sxs-lookup"><span data-stu-id="10978-146">Default Data Types and Values</span></span>

<span data-ttu-id="10978-147">下表描述了指定 `Dim` 语句中数据类型和初始值设定项的各种组合的结果。</span><span class="sxs-lookup"><span data-stu-id="10978-147">The following table describes the results of various combinations of specifying the data type and initializer in a `Dim` statement.</span></span>

|<span data-ttu-id="10978-148">是否指定数据类型？</span><span class="sxs-lookup"><span data-stu-id="10978-148">Data type specified?</span></span>|<span data-ttu-id="10978-149">是否指定初始值设定项？</span><span class="sxs-lookup"><span data-stu-id="10978-149">Initializer specified?</span></span>|<span data-ttu-id="10978-150">示例</span><span class="sxs-lookup"><span data-stu-id="10978-150">Example</span></span>|<span data-ttu-id="10978-151">结果</span><span class="sxs-lookup"><span data-stu-id="10978-151">Result</span></span>|
|---|---|---|---|
|<span data-ttu-id="10978-152">否</span><span class="sxs-lookup"><span data-stu-id="10978-152">No</span></span>|<span data-ttu-id="10978-153">否</span><span class="sxs-lookup"><span data-stu-id="10978-153">No</span></span>|`Dim qty`|<span data-ttu-id="10978-154">如果 `Option Strict` 处于关闭状态（默认），则将变量设置为 `Nothing`。</span><span class="sxs-lookup"><span data-stu-id="10978-154">If `Option Strict` is off (the default), the variable is set to `Nothing`.</span></span><br /><br /> <span data-ttu-id="10978-155">如果 `Option Strict` 处于打开状态，则发生编译时错误。</span><span class="sxs-lookup"><span data-stu-id="10978-155">If `Option Strict` is on, a compile-time error occurs.</span></span>|
|<span data-ttu-id="10978-156">否</span><span class="sxs-lookup"><span data-stu-id="10978-156">No</span></span>|<span data-ttu-id="10978-157">是</span><span class="sxs-lookup"><span data-stu-id="10978-157">Yes</span></span>|`Dim qty = 5`|<span data-ttu-id="10978-158">如果 `Option Infer` 处于打开状态（默认），则变量采用初始值设定项的数据类型。</span><span class="sxs-lookup"><span data-stu-id="10978-158">If `Option Infer` is on (the default), the variable takes the data type of the initializer.</span></span> <span data-ttu-id="10978-159">请参阅 [局部类型推理](../../programming-guide/language-features/variables/local-type-inference.md)。</span><span class="sxs-lookup"><span data-stu-id="10978-159">See [Local Type Inference](../../programming-guide/language-features/variables/local-type-inference.md).</span></span><br /><br /> <span data-ttu-id="10978-160">如果 `Option Infer` 和 `Option Strict` 均处于关闭状态，则变量采用 `Object` 的数据类型。</span><span class="sxs-lookup"><span data-stu-id="10978-160">If `Option Infer` is off and `Option Strict` is off, the variable takes the data type of `Object`.</span></span><br /><br /> <span data-ttu-id="10978-161">如果 `Option Infer` 处于关闭状态但 `Option Strict` 处于打开状态，则发生编译时错误。</span><span class="sxs-lookup"><span data-stu-id="10978-161">If `Option Infer` is off and `Option Strict` is on, a compile-time error occurs.</span></span>|
|<span data-ttu-id="10978-162">是</span><span class="sxs-lookup"><span data-stu-id="10978-162">Yes</span></span>|<span data-ttu-id="10978-163">否</span><span class="sxs-lookup"><span data-stu-id="10978-163">No</span></span>|`Dim qty As Integer`|<span data-ttu-id="10978-164">将变量初始化为数据类型的默认值。</span><span class="sxs-lookup"><span data-stu-id="10978-164">The variable is initialized to the default value for the data type.</span></span> <span data-ttu-id="10978-165">有关详细信息，请参阅 [Dim 语句](dim-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="10978-165">For more information, see [Dim Statement](dim-statement.md).</span></span>|
|<span data-ttu-id="10978-166">是</span><span class="sxs-lookup"><span data-stu-id="10978-166">Yes</span></span>|<span data-ttu-id="10978-167">是</span><span class="sxs-lookup"><span data-stu-id="10978-167">Yes</span></span>|`Dim qty  As Integer = 5`|<span data-ttu-id="10978-168">如果初始值设定项的数据类型不可转换为指定数据类型，则会发生编译时错误。</span><span class="sxs-lookup"><span data-stu-id="10978-168">If the data type of the initializer is not convertible to the specified data type, a compile-time error occurs.</span></span>|

## <a name="example"></a><span data-ttu-id="10978-169">示例</span><span class="sxs-lookup"><span data-stu-id="10978-169">Example</span></span>

<span data-ttu-id="10978-170">下例演示了 `Option Infer` 语句启用局部类型推理的方式。</span><span class="sxs-lookup"><span data-stu-id="10978-170">The following examples demonstrate how the `Option Infer` statement enables local type inference.</span></span>

[!code-vb[VbVbalrTypeInference#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrTypeInference/VB/Class1.vb#6)]

## <a name="example"></a><span data-ttu-id="10978-171">示例</span><span class="sxs-lookup"><span data-stu-id="10978-171">Example</span></span>

<span data-ttu-id="10978-172">下例演示了变量被标识为 `Object` 时运行时类型可以改变的情况。</span><span class="sxs-lookup"><span data-stu-id="10978-172">The following example demonstrates that the run-time type can differ when a variable is identified as an `Object`.</span></span>

[!code-vb[VbVbalrTypeInference#11](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrTypeInference/VB/Class1.vb#11)]

## <a name="see-also"></a><span data-ttu-id="10978-173">请参阅</span><span class="sxs-lookup"><span data-stu-id="10978-173">See also</span></span>

- [<span data-ttu-id="10978-174">Dim 语句</span><span class="sxs-lookup"><span data-stu-id="10978-174">Dim Statement</span></span>](dim-statement.md)
- [<span data-ttu-id="10978-175">局部类型推理</span><span class="sxs-lookup"><span data-stu-id="10978-175">Local Type Inference</span></span>](../../programming-guide/language-features/variables/local-type-inference.md)
- [<span data-ttu-id="10978-176">Option Compare 语句</span><span class="sxs-lookup"><span data-stu-id="10978-176">Option Compare Statement</span></span>](option-compare-statement.md)
- [<span data-ttu-id="10978-177">Option Explicit 语句</span><span class="sxs-lookup"><span data-stu-id="10978-177">Option Explicit Statement</span></span>](option-explicit-statement.md)
- [<span data-ttu-id="10978-178">Option Strict 语句</span><span class="sxs-lookup"><span data-stu-id="10978-178">Option Strict Statement</span></span>](option-strict-statement.md)
- [<span data-ttu-id="10978-179">“选项”对话框 ->“项目”->“Visual Basic 默认值”</span><span class="sxs-lookup"><span data-stu-id="10978-179">Visual Basic Defaults, Projects, Options Dialog Box</span></span>](/visualstudio/ide/reference/visual-basic-defaults-projects-options-dialog-box)
- [<span data-ttu-id="10978-180">-optioninfer</span><span class="sxs-lookup"><span data-stu-id="10978-180">-optioninfer</span></span>](../../reference/command-line-compiler/optioninfer.md)
- [<span data-ttu-id="10978-181">装箱和取消装箱</span><span class="sxs-lookup"><span data-stu-id="10978-181">Boxing and Unboxing</span></span>](../../../csharp/programming-guide/types/boxing-and-unboxing.md)
