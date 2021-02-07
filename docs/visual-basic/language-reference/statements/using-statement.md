---
description: '了解详细信息：使用语句 (Visual Basic) '
title: Using 语句
ms.date: 07/20/2015
f1_keywords:
- vb.using
helpviewer_keywords:
- resource disposal
- Try...Catch...Finally statements, equivalent to Using statement
- resources [Visual Basic], disposing
- Using statement [Visual Basic]
ms.assetid: 665d1580-dd54-4e96-a9a9-6be2a68948f1
ms.openlocfilehash: fea77a441182b7c3ecac58d4fe7f1297a87f086c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99740881"
---
# <a name="using-statement-visual-basic"></a><span data-ttu-id="f4749-103">Using 语句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f4749-103">Using Statement (Visual Basic)</span></span>

<span data-ttu-id="f4749-104">声明块的开头 `Using` ，并根据需要获取块所控制的系统资源。</span><span class="sxs-lookup"><span data-stu-id="f4749-104">Declares the beginning of a `Using` block and optionally acquires the system resources that the block controls.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4749-105">语法</span><span class="sxs-lookup"><span data-stu-id="f4749-105">Syntax</span></span>

```vb
Using { resourcelist | resourceexpression }
    [ statements ]
End Using
```

## <a name="parts"></a><span data-ttu-id="f4749-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="f4749-106">Parts</span></span>

|<span data-ttu-id="f4749-107">术语</span><span class="sxs-lookup"><span data-stu-id="f4749-107">Term</span></span>|<span data-ttu-id="f4749-108">定义</span><span class="sxs-lookup"><span data-stu-id="f4749-108">Definition</span></span>|  
|---|---|  
|`resourcelist`|<span data-ttu-id="f4749-109">如果未提供，则为必需 `resourceexpression` 。</span><span class="sxs-lookup"><span data-stu-id="f4749-109">Required if you do not supply `resourceexpression`.</span></span> <span data-ttu-id="f4749-110">此块控制的一个或多个系统资源的列表 `Using` （用逗号分隔）。</span><span class="sxs-lookup"><span data-stu-id="f4749-110">List of one or more system resources that this `Using` block controls, separated by commas.</span></span>|  
|`resourceexpression`|<span data-ttu-id="f4749-111">如果未提供，则为必需 `resourcelist` 。</span><span class="sxs-lookup"><span data-stu-id="f4749-111">Required if you do not supply `resourcelist`.</span></span> <span data-ttu-id="f4749-112">引用由此块控制的系统资源的引用变量或表达式 `Using` 。</span><span class="sxs-lookup"><span data-stu-id="f4749-112">Reference variable or expression referring to a system resource to be controlled by this `Using` block.</span></span>|  
|`statements`|<span data-ttu-id="f4749-113">可选。</span><span class="sxs-lookup"><span data-stu-id="f4749-113">Optional.</span></span> <span data-ttu-id="f4749-114">块运行的语句块 `Using` 。</span><span class="sxs-lookup"><span data-stu-id="f4749-114">Block of statements that the `Using` block runs.</span></span>|  
|`End Using`|<span data-ttu-id="f4749-115">必需。</span><span class="sxs-lookup"><span data-stu-id="f4749-115">Required.</span></span> <span data-ttu-id="f4749-116">终止块的定义 `Using` ，并释放其控制的所有资源。</span><span class="sxs-lookup"><span data-stu-id="f4749-116">Terminates the definition of the `Using` block and disposes of all the resources that it controls.</span></span>|  

 <span data-ttu-id="f4749-117">此部分中的每个资源 `resourcelist` 都具有以下语法和部分：</span><span class="sxs-lookup"><span data-stu-id="f4749-117">Each resource in the `resourcelist` part has the following syntax and parts:</span></span>

 `resourcename As New resourcetype [ ( [ arglist ] ) ]`

 <span data-ttu-id="f4749-118">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="f4749-118">-or-</span></span>

 `resourcename As resourcetype = resourceexpression`

## <a name="resourcelist-parts"></a><span data-ttu-id="f4749-119">resourcelist 部件</span><span class="sxs-lookup"><span data-stu-id="f4749-119">resourcelist Parts</span></span>

|<span data-ttu-id="f4749-120">术语</span><span class="sxs-lookup"><span data-stu-id="f4749-120">Term</span></span>|<span data-ttu-id="f4749-121">定义</span><span class="sxs-lookup"><span data-stu-id="f4749-121">Definition</span></span>|  
|---|---|  
|`resourcename`|<span data-ttu-id="f4749-122">必需。</span><span class="sxs-lookup"><span data-stu-id="f4749-122">Required.</span></span> <span data-ttu-id="f4749-123">引用变量，该变量引用块所控制的系统资源 `Using` 。</span><span class="sxs-lookup"><span data-stu-id="f4749-123">Reference variable that refers to a system resource that the `Using` block controls.</span></span>|  
|`New`|<span data-ttu-id="f4749-124">如果语句获取资源，则为必需 `Using` 。</span><span class="sxs-lookup"><span data-stu-id="f4749-124">Required if the `Using` statement acquires the resource.</span></span> <span data-ttu-id="f4749-125">如果已获取资源，请使用第二种语法替代方法。</span><span class="sxs-lookup"><span data-stu-id="f4749-125">If you have already acquired the resource, use the second syntax alternative.</span></span>|  
|`resourcetype`|<span data-ttu-id="f4749-126">必需。</span><span class="sxs-lookup"><span data-stu-id="f4749-126">Required.</span></span> <span data-ttu-id="f4749-127">资源的类。</span><span class="sxs-lookup"><span data-stu-id="f4749-127">The class of the resource.</span></span> <span data-ttu-id="f4749-128">类必须实现 <xref:System.IDisposable> 接口。</span><span class="sxs-lookup"><span data-stu-id="f4749-128">The class must implement the <xref:System.IDisposable> interface.</span></span>|  
|`arglist`|<span data-ttu-id="f4749-129">可选。</span><span class="sxs-lookup"><span data-stu-id="f4749-129">Optional.</span></span> <span data-ttu-id="f4749-130">要传递给构造函数来创建实例的参数的列表 `resourcetype` 。</span><span class="sxs-lookup"><span data-stu-id="f4749-130">List of arguments you are passing to the constructor to create an instance of `resourcetype`.</span></span> <span data-ttu-id="f4749-131">请参阅 [参数列表](parameter-list.md)。</span><span class="sxs-lookup"><span data-stu-id="f4749-131">See [Parameter List](parameter-list.md).</span></span>|  
|`resourceexpression`|<span data-ttu-id="f4749-132">必需。</span><span class="sxs-lookup"><span data-stu-id="f4749-132">Required.</span></span> <span data-ttu-id="f4749-133">引用满足的要求的系统资源的变量或表达式 `resourcetype` 。</span><span class="sxs-lookup"><span data-stu-id="f4749-133">Variable or expression referring to a system resource satisfying the requirements of `resourcetype`.</span></span> <span data-ttu-id="f4749-134">如果使用第二种语法替代方法，则必须先获取资源，然后才能将控制传递给 `Using` 语句。</span><span class="sxs-lookup"><span data-stu-id="f4749-134">If you use the second syntax alternative, you must acquire the resource before passing control to the `Using` statement.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f4749-135">备注</span><span class="sxs-lookup"><span data-stu-id="f4749-135">Remarks</span></span>

 <span data-ttu-id="f4749-136">有时，您的代码需要非托管资源，如文件句柄、COM 包装或 SQL 连接。</span><span class="sxs-lookup"><span data-stu-id="f4749-136">Sometimes your code requires an unmanaged resource, such as a file handle, a COM wrapper, or a SQL connection.</span></span> <span data-ttu-id="f4749-137">`Using`当你的代码完成了一个或多个此类资源时，块可保证其释放。</span><span class="sxs-lookup"><span data-stu-id="f4749-137">A `Using` block guarantees the disposal of one or more such resources when your code is finished with them.</span></span> <span data-ttu-id="f4749-138">这使它们可供其他代码使用。</span><span class="sxs-lookup"><span data-stu-id="f4749-138">This makes them available for other code to use.</span></span>

 <span data-ttu-id="f4749-139">托管资源由 .NET Framework 垃圾回收器释放 (GC) ，而不会对你的部分进行任何额外编码。</span><span class="sxs-lookup"><span data-stu-id="f4749-139">Managed resources are disposed of by the .NET Framework garbage collector (GC) without any extra coding on your part.</span></span> <span data-ttu-id="f4749-140">对于托管资源，无需使用 `Using` 块。</span><span class="sxs-lookup"><span data-stu-id="f4749-140">You do not need a `Using` block for managed resources.</span></span> <span data-ttu-id="f4749-141">但是，您仍然可以使用 `Using` 块来强制处置托管资源，而不是等待垃圾回收器。</span><span class="sxs-lookup"><span data-stu-id="f4749-141">However, you can still use a `Using` block to force the disposal of a managed resource instead of waiting for the garbage collector.</span></span>

 <span data-ttu-id="f4749-142">`Using`块有三个部分：获取、使用和处理。</span><span class="sxs-lookup"><span data-stu-id="f4749-142">A `Using` block has three parts: acquisition, usage, and disposal.</span></span>

- <span data-ttu-id="f4749-143">*获取* 是指创建一个变量并将其初始化，以引用系统资源。</span><span class="sxs-lookup"><span data-stu-id="f4749-143">*Acquisition* means creating a variable and initializing it to refer to the system resource.</span></span> <span data-ttu-id="f4749-144">`Using`语句可以获取一个或多个资源，也可以在输入块之前获取一个资源，并将其提供给 `Using` 语句。</span><span class="sxs-lookup"><span data-stu-id="f4749-144">The `Using` statement can acquire one or more resources, or you can acquire exactly one resource before entering the block and supply it to the `Using` statement.</span></span> <span data-ttu-id="f4749-145">如果提供 `resourceexpression` ，则必须先获取资源，然后才能将控制传递给 `Using` 语句。</span><span class="sxs-lookup"><span data-stu-id="f4749-145">If you supply `resourceexpression`, you must acquire the resource before passing control to the `Using` statement.</span></span>

- <span data-ttu-id="f4749-146">*用法* 是指访问资源并对其执行操作。</span><span class="sxs-lookup"><span data-stu-id="f4749-146">*Usage* means accessing the resources and performing actions with them.</span></span> <span data-ttu-id="f4749-147">和之间的 `Using` 语句 `End Using` 表示资源的使用情况。</span><span class="sxs-lookup"><span data-stu-id="f4749-147">The statements between `Using` and `End Using` represent the usage of the resources.</span></span>

- <span data-ttu-id="f4749-148">处理 <xref:System.IDisposable.Dispose%2A> 是指对中的对象调用方法 `resourcename` 。</span><span class="sxs-lookup"><span data-stu-id="f4749-148">*Disposal* means calling the <xref:System.IDisposable.Dispose%2A> method on the object in `resourcename`.</span></span> <span data-ttu-id="f4749-149">这使对象可以干净地终止其资源。</span><span class="sxs-lookup"><span data-stu-id="f4749-149">This allows the object to cleanly terminate its resources.</span></span> <span data-ttu-id="f4749-150">`End Using`语句释放块控件下的资源 `Using` 。</span><span class="sxs-lookup"><span data-stu-id="f4749-150">The `End Using` statement disposes of the resources under the `Using` block's control.</span></span>

## <a name="behavior"></a><span data-ttu-id="f4749-151">行为</span><span class="sxs-lookup"><span data-stu-id="f4749-151">Behavior</span></span>

 <span data-ttu-id="f4749-152">`Using`块的行为类似于 `Try` ... 构造， `Finally` 其中 `Try` 块使用资源，而 `Finally` 块处置它们。</span><span class="sxs-lookup"><span data-stu-id="f4749-152">A `Using` block behaves like a `Try`...`Finally` construction in which the `Try` block uses the resources and the `Finally` block disposes of them.</span></span> <span data-ttu-id="f4749-153">因此，无论 `Using` 退出块的方式如何，块都可保证资源的处置。</span><span class="sxs-lookup"><span data-stu-id="f4749-153">Because of this, the `Using` block guarantees disposal of the resources, no matter how you exit the block.</span></span> <span data-ttu-id="f4749-154">即使在发生未经处理的异常的情况下也是如此，但除外 <xref:System.StackOverflowException> 。</span><span class="sxs-lookup"><span data-stu-id="f4749-154">This is true even in the case of an unhandled exception, except for a <xref:System.StackOverflowException>.</span></span>

 <span data-ttu-id="f4749-155">语句获取的每个资源变量的作用域 `Using` 仅限于 `Using` 块。</span><span class="sxs-lookup"><span data-stu-id="f4749-155">The scope of every resource variable acquired by the `Using` statement is limited to the `Using` block.</span></span>

 <span data-ttu-id="f4749-156">如果在语句中指定多个系统资源 `Using` ，则效果与嵌套 `Using` 块在另一个中时相同。</span><span class="sxs-lookup"><span data-stu-id="f4749-156">If you specify more than one system resource in the `Using` statement, the effect is the same as if you nested `Using` blocks one within another.</span></span>

 <span data-ttu-id="f4749-157">如果 `resourcename` 为 `Nothing` ， <xref:System.IDisposable.Dispose%2A> 则不进行对的调用，且不引发异常。</span><span class="sxs-lookup"><span data-stu-id="f4749-157">If `resourcename` is `Nothing`, no call to <xref:System.IDisposable.Dispose%2A> is made, and no exception is thrown.</span></span>

## <a name="structured-exception-handling-within-a-using-block"></a><span data-ttu-id="f4749-158">Using 块中的结构化异常处理</span><span class="sxs-lookup"><span data-stu-id="f4749-158">Structured Exception Handling Within a Using Block</span></span>

 <span data-ttu-id="f4749-159">如果需要处理可能在块中发生的异常 `Using` ，可以向其添加完整的 `Try` ... `Finally` 构造。</span><span class="sxs-lookup"><span data-stu-id="f4749-159">If you need to handle an exception that might occur within the `Using` block, you can add a complete `Try`...`Finally` construction to it.</span></span> <span data-ttu-id="f4749-160">如果需要处理 `Using` 语句未能成功获取资源的情况，则可以进行测试以查看 `resourcename` 是否为 `Nothing` 。</span><span class="sxs-lookup"><span data-stu-id="f4749-160">If you need to handle the case where the `Using` statement is not successful in acquiring a resource, you can test to see if `resourcename` is `Nothing`.</span></span>

## <a name="structured-exception-handling-instead-of-a-using-block"></a><span data-ttu-id="f4749-161">结构化异常处理而不是 Using 块</span><span class="sxs-lookup"><span data-stu-id="f4749-161">Structured Exception Handling Instead of a Using Block</span></span>

 <span data-ttu-id="f4749-162">如果需要更好地控制资源的获取，或在块中需要其他代码， `Finally` 则可以将块重写 `Using` 为 `Try` ... `Finally` 构造。</span><span class="sxs-lookup"><span data-stu-id="f4749-162">If you need finer control over the acquisition of the resources, or you need additional code in the `Finally` block, you can rewrite the `Using` block as a `Try`...`Finally` construction.</span></span> <span data-ttu-id="f4749-163">下面的示例显示了 `Try` 的 `Using` 采集和处置中等效的主干和构造 `resource` 。</span><span class="sxs-lookup"><span data-stu-id="f4749-163">The following example shows skeleton `Try` and `Using` constructions that are equivalent in the acquisition and disposal of `resource`.</span></span>

```vb
Using resource As New resourceType
    ' Insert code to work with resource.
End Using

' For the acquisition and disposal of resource, the following  
' Try construction is equivalent to the Using block.
Dim resource As New resourceType
Try
    ' Insert code to work with resource.
Finally
    If resource IsNot Nothing Then
        resource.Dispose()
    End If
End Try
```

> [!NOTE]
> <span data-ttu-id="f4749-164">块内的代码 `Using` 不应将对象分配 `resourcename` 给另一个变量。</span><span class="sxs-lookup"><span data-stu-id="f4749-164">The code inside the `Using` block should not assign the object in `resourcename` to another variable.</span></span> <span data-ttu-id="f4749-165">退出 `Using` 块后，资源会被释放，另一个变量将无法访问它所指向的资源。</span><span class="sxs-lookup"><span data-stu-id="f4749-165">When you exit the `Using` block, the resource is disposed, and the other variable cannot access the resource to which it points.</span></span>

## <a name="example"></a><span data-ttu-id="f4749-166">示例</span><span class="sxs-lookup"><span data-stu-id="f4749-166">Example</span></span>

 <span data-ttu-id="f4749-167">下面的示例创建一个名为 log.txt 的文件，并向该文件写入两行文本。</span><span class="sxs-lookup"><span data-stu-id="f4749-167">The following example creates a file that is named log.txt and writes two lines of text to the file.</span></span> <span data-ttu-id="f4749-168">该示例还读取同一文件并显示文本行：</span><span class="sxs-lookup"><span data-stu-id="f4749-168">The example also reads that same file and displays the lines of text:</span></span>

 <span data-ttu-id="f4749-169">由于 <xref:System.IO.TextWriter> 和 <xref:System.IO.TextReader> 类实现 <xref:System.IDisposable> 接口，因此代码可以使用 `Using` 语句来确保文件在执行写入和读取操作后正确关闭。</span><span class="sxs-lookup"><span data-stu-id="f4749-169">Because the <xref:System.IO.TextWriter> and <xref:System.IO.TextReader> classes implement the <xref:System.IDisposable> interface, the code can use `Using` statements to ensure that the file is correctly closed after the write and read operations.</span></span>

 [!code-vb[VbVbalrStatements#50](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#50)]

## <a name="see-also"></a><span data-ttu-id="f4749-170">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f4749-170">See also</span></span>

- <xref:System.IDisposable>
- [<span data-ttu-id="f4749-171">Try...Catch...Finally 语句</span><span class="sxs-lookup"><span data-stu-id="f4749-171">Try...Catch...Finally Statement</span></span>](try-catch-finally-statement.md)
- [<span data-ttu-id="f4749-172">如何：释放系统资源</span><span class="sxs-lookup"><span data-stu-id="f4749-172">How to: Dispose of a System Resource</span></span>](../../programming-guide/language-features/control-flow/how-to-dispose-of-a-system-resource.md)
