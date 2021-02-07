---
description: '了解详细信息： (Visual Basic 的常量和枚举) '
title: 常量和枚举
ms.date: 07/20/2015
helpviewer_keywords:
- enumerations [Visual Basic]
- constants [Visual Basic]
- constants [Visual Basic], list of
ms.assetid: 309c0ad5-83e4-4f96-99ea-83cd95107417
ms.openlocfilehash: 4306b007fc5cc881cbe1342a5f4bdd7802c252f0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99675138"
---
# <a name="constants-and-enumerations-visual-basic"></a><span data-ttu-id="f4159-103">常量和枚举 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f4159-103">Constants and Enumerations (Visual Basic)</span></span>

<span data-ttu-id="f4159-104">Visual Basic 为开发人员提供了许多预定义的常量和枚举。</span><span class="sxs-lookup"><span data-stu-id="f4159-104">Visual Basic supplies a number of predefined constants and enumerations for developers.</span></span> <span data-ttu-id="f4159-105">常量存储在应用程序的整个执行过程中保持不变的值。</span><span class="sxs-lookup"><span data-stu-id="f4159-105">Constants store values that remain constant throughout the execution of an application.</span></span> <span data-ttu-id="f4159-106">枚举提供了使用相关常量集以及将常量值与名称相关联的一个便捷方法。</span><span class="sxs-lookup"><span data-stu-id="f4159-106">Enumerations provide a convenient way to work with sets of related constants, and to associate constant values with names.</span></span>  
  
## <a name="constants"></a><span data-ttu-id="f4159-107">常量</span><span class="sxs-lookup"><span data-stu-id="f4159-107">Constants</span></span>  
  
### <a name="conditional-compilation-constants"></a><span data-ttu-id="f4159-108">条件编译常量</span><span class="sxs-lookup"><span data-stu-id="f4159-108">Conditional Compilation Constants</span></span>  

 <span data-ttu-id="f4159-109">下表列出了可用于条件编译的预定义常量。</span><span class="sxs-lookup"><span data-stu-id="f4159-109">The following table lists the predefined constants available for conditional compilation.</span></span>  
  
|<span data-ttu-id="f4159-110">**Constant**</span><span class="sxs-lookup"><span data-stu-id="f4159-110">**Constant**</span></span>|<span data-ttu-id="f4159-111">**说明**</span><span class="sxs-lookup"><span data-stu-id="f4159-111">**Description**</span></span>|  
|---|---|  
|`CONFIG`|<span data-ttu-id="f4159-112">与 **Configuration Manager** 中 "**活动解决方案配置**" 框的当前设置相对应的字符串。</span><span class="sxs-lookup"><span data-stu-id="f4159-112">A string that corresponds to the current setting of the **Active Solution Configuration** box in the **Configuration Manager**.</span></span>|  
|`DEBUG`|<span data-ttu-id="f4159-113">`Boolean`可在 "**项目属性**" 对话框中设置的值。</span><span class="sxs-lookup"><span data-stu-id="f4159-113">A `Boolean` value that can be set in the **Project Properties** dialog box.</span></span> <span data-ttu-id="f4159-114">默认情况下，项目的 "调试" 配置定义 `DEBUG` 。</span><span class="sxs-lookup"><span data-stu-id="f4159-114">By default, the Debug configuration for a project defines `DEBUG`.</span></span> <span data-ttu-id="f4159-115">`DEBUG`定义后， <xref:System.Diagnostics.Debug> 类方法会将输出生成到 **输出** 窗口。</span><span class="sxs-lookup"><span data-stu-id="f4159-115">When `DEBUG` is defined, <xref:System.Diagnostics.Debug> class methods generate output to the **Output** window.</span></span> <span data-ttu-id="f4159-116">如果未定义，则 <xref:System.Diagnostics.Debug> 不会编译类方法，也不会生成任何调试输出。</span><span class="sxs-lookup"><span data-stu-id="f4159-116">When it is not defined, <xref:System.Diagnostics.Debug> class methods are not compiled and no Debug output is generated.</span></span>|  
|`TARGET`|<span data-ttu-id="f4159-117">一个字符串，表示项目的输出类型或命令行 **目标** 选项的设置。</span><span class="sxs-lookup"><span data-stu-id="f4159-117">A string representing the output type for the project or the setting of the command-line **-target** option.</span></span> <span data-ttu-id="f4159-118">的可能值 `TARGET` 为：</span><span class="sxs-lookup"><span data-stu-id="f4159-118">The possible values of `TARGET` are:</span></span><br /><br /> <span data-ttu-id="f4159-119">-Windows 应用程序的 "winexe"。</span><span class="sxs-lookup"><span data-stu-id="f4159-119">-   "winexe" for a Windows application.</span></span><br /><span data-ttu-id="f4159-120">-适用于控制台应用程序的 "exe"。</span><span class="sxs-lookup"><span data-stu-id="f4159-120">-   "exe" for a console application.</span></span><br /><span data-ttu-id="f4159-121">-类库的 "库"。</span><span class="sxs-lookup"><span data-stu-id="f4159-121">-   "library" for a class library.</span></span><br /><span data-ttu-id="f4159-122">-模块的 "module"。</span><span class="sxs-lookup"><span data-stu-id="f4159-122">-   "module" for a module.</span></span><br /><span data-ttu-id="f4159-123">-可在 Visual Studio 集成开发环境中设置 **-target** 选项。</span><span class="sxs-lookup"><span data-stu-id="f4159-123">-   The **-target** option may be set in the Visual Studio integrated development environment.</span></span> <span data-ttu-id="f4159-124">有关详细信息，请参阅 [-target (Visual Basic)](../reference/command-line-compiler/target.md)。</span><span class="sxs-lookup"><span data-stu-id="f4159-124">For more information, see [-target (Visual Basic)](../reference/command-line-compiler/target.md).</span></span>|  
|`TRACE`|<span data-ttu-id="f4159-125">`Boolean`可在 "**项目属性**" 对话框中设置的值。</span><span class="sxs-lookup"><span data-stu-id="f4159-125">A `Boolean` value that can be set in the **Project Properties** dialog box.</span></span> <span data-ttu-id="f4159-126">默认情况下，项目的所有配置都定义 `TRACE` 。</span><span class="sxs-lookup"><span data-stu-id="f4159-126">By default, all configurations for a project define `TRACE`.</span></span> <span data-ttu-id="f4159-127">`TRACE`定义后， <xref:System.Diagnostics.Trace> 类方法会将输出生成到 **输出** 窗口。</span><span class="sxs-lookup"><span data-stu-id="f4159-127">When `TRACE` is defined, <xref:System.Diagnostics.Trace> class methods generate output to the **Output** window.</span></span> <span data-ttu-id="f4159-128">如果未定义，则 <xref:System.Diagnostics.Trace> 不会编译类方法，也不会 `Trace` 生成任何输出。</span><span class="sxs-lookup"><span data-stu-id="f4159-128">When it is not defined, <xref:System.Diagnostics.Trace> class methods are not compiled and no `Trace` output is generated.</span></span>|  
|`VBC_VER`|<span data-ttu-id="f4159-129">一个表示 Visual Basic 版本的数字，以 *主*。*小* 格式。</span><span class="sxs-lookup"><span data-stu-id="f4159-129">A number representing the Visual Basic version, in *major*.*minor* format.</span></span>|  
  
### <a name="print-and-display-constants"></a><span data-ttu-id="f4159-130">打印和显示常量</span><span class="sxs-lookup"><span data-stu-id="f4159-130">Print and Display Constants</span></span>  

 <span data-ttu-id="f4159-131">调用打印和显示功能时，可以在代码中使用以下常量来替换实际值。</span><span class="sxs-lookup"><span data-stu-id="f4159-131">When you call print and display functions, you can use the following constants in your code in place of the actual values.</span></span>  
  
|<span data-ttu-id="f4159-132">**Constant**</span><span class="sxs-lookup"><span data-stu-id="f4159-132">**Constant**</span></span>|<span data-ttu-id="f4159-133">**说明**</span><span class="sxs-lookup"><span data-stu-id="f4159-133">**Description**</span></span>|  
|---|---|  
|`vbCrLf`|<span data-ttu-id="f4159-134">回车符/换行符的组合。</span><span class="sxs-lookup"><span data-stu-id="f4159-134">Carriage return/linefeed character combination.</span></span>|  
|`vbCr`|<span data-ttu-id="f4159-135">回车符。</span><span class="sxs-lookup"><span data-stu-id="f4159-135">Carriage return character.</span></span>|  
|`vbLf`|<span data-ttu-id="f4159-136">换行符。</span><span class="sxs-lookup"><span data-stu-id="f4159-136">Linefeed character.</span></span>|  
|`vbNewLine`|<span data-ttu-id="f4159-137">换行符。</span><span class="sxs-lookup"><span data-stu-id="f4159-137">Newline character.</span></span>|  
|`vbNullChar`|<span data-ttu-id="f4159-138">空字符。</span><span class="sxs-lookup"><span data-stu-id="f4159-138">Null character.</span></span>|  
|`vbNullString`|<span data-ttu-id="f4159-139">与零长度字符串不同 ( "" ) ;用于调用外部过程。</span><span class="sxs-lookup"><span data-stu-id="f4159-139">Not the same as a zero-length string (""); used for calling external procedures.</span></span>|  
|`vbObjectError`|<span data-ttu-id="f4159-140">错误号。</span><span class="sxs-lookup"><span data-stu-id="f4159-140">Error number.</span></span> <span data-ttu-id="f4159-141">用户定义的错误号应当大于此值。</span><span class="sxs-lookup"><span data-stu-id="f4159-141">User-defined error numbers should be greater than this value.</span></span> <span data-ttu-id="f4159-142">例如：</span><span class="sxs-lookup"><span data-stu-id="f4159-142">For example:</span></span><br /><br /> `Err.Raise(Number) = vbObjectError + 1000`|  
|`vbTab`|<span data-ttu-id="f4159-143">制表符。</span><span class="sxs-lookup"><span data-stu-id="f4159-143">Tab character.</span></span>|  
|`vbBack`|<span data-ttu-id="f4159-144">Backspace 字符。</span><span class="sxs-lookup"><span data-stu-id="f4159-144">Backspace character.</span></span>|  
|`vbFormFeed`|<span data-ttu-id="f4159-145">不在 Microsoft Windows 中使用。</span><span class="sxs-lookup"><span data-stu-id="f4159-145">Not used in Microsoft Windows.</span></span>|  
|`vbVerticalTab`|<span data-ttu-id="f4159-146">在 Microsoft Windows 中不起作用。</span><span class="sxs-lookup"><span data-stu-id="f4159-146">Not useful in Microsoft Windows.</span></span>|  
  
## <a name="enumerations"></a><span data-ttu-id="f4159-147">枚举</span><span class="sxs-lookup"><span data-stu-id="f4159-147">Enumerations</span></span>  

 <span data-ttu-id="f4159-148">下表列出并描述了 Visual Basic 提供的枚举。</span><span class="sxs-lookup"><span data-stu-id="f4159-148">The following table lists and describes the enumerations provided by Visual Basic.</span></span>  
  
|<span data-ttu-id="f4159-149">枚举</span><span class="sxs-lookup"><span data-stu-id="f4159-149">Enumeration</span></span>|<span data-ttu-id="f4159-150">描述</span><span class="sxs-lookup"><span data-stu-id="f4159-150">Description</span></span>|  
|---|---|  
|<xref:Microsoft.VisualBasic.AppWinStyle>|<span data-ttu-id="f4159-151">指示在调用 <xref:Microsoft.VisualBasic.Interaction.Shell%2A> 函数时用于被调用程序的窗口样式。</span><span class="sxs-lookup"><span data-stu-id="f4159-151">Indicates the window style to use for the invoked program when calling the <xref:Microsoft.VisualBasic.Interaction.Shell%2A> function.</span></span>|  
|<xref:Microsoft.VisualBasic.AudioPlayMode>|<span data-ttu-id="f4159-152">指示在调用音频方法时如何播放声音。</span><span class="sxs-lookup"><span data-stu-id="f4159-152">Indicates how to play sounds when calling audio methods.</span></span>|  
|<xref:Microsoft.VisualBasic.ApplicationServices.BuiltInRole>|<span data-ttu-id="f4159-153">指示在调用 <xref:Microsoft.VisualBasic.ApplicationServices.User.IsInRole%2A> 方法时检查的角色类型。</span><span class="sxs-lookup"><span data-stu-id="f4159-153">Indicates the type of role to check when calling the <xref:Microsoft.VisualBasic.ApplicationServices.User.IsInRole%2A> method.</span></span>|  
|<xref:Microsoft.VisualBasic.CallType>|<span data-ttu-id="f4159-154">指示在调用 <xref:Microsoft.VisualBasic.Interaction.CallByName%2A> 函数时调用的过程类型。</span><span class="sxs-lookup"><span data-stu-id="f4159-154">Indicates the type of procedure being invoked when calling the <xref:Microsoft.VisualBasic.Interaction.CallByName%2A> function.</span></span>|  
|<xref:Microsoft.VisualBasic.CompareMethod>|<span data-ttu-id="f4159-155">指示当调用比较函数时如何比较字符串。</span><span class="sxs-lookup"><span data-stu-id="f4159-155">Indicates how to compare strings when calling comparison functions.</span></span>|  
|<xref:Microsoft.VisualBasic.DateFormat>|<span data-ttu-id="f4159-156">指示在调用 <xref:Microsoft.VisualBasic.Strings.FormatDateTime%2A> 函数时如何显示日期。</span><span class="sxs-lookup"><span data-stu-id="f4159-156">Indicates how to display dates when calling the <xref:Microsoft.VisualBasic.Strings.FormatDateTime%2A> function.</span></span>|  
|<xref:Microsoft.VisualBasic.DateInterval>|<span data-ttu-id="f4159-157">指示当调用与日期相关的函数时如何确定日期间隔并设置其格式。</span><span class="sxs-lookup"><span data-stu-id="f4159-157">Indicates how to determine and format date intervals when calling date-related functions.</span></span>|  
|<xref:Microsoft.VisualBasic.FileIO.DeleteDirectoryOption>|<span data-ttu-id="f4159-158">指定当要删除的目录中含有文件或目录时应采取的操作。</span><span class="sxs-lookup"><span data-stu-id="f4159-158">Specifies what should be done when a directory that is to be deleted contains files or directories.</span></span>|  
|<xref:Microsoft.VisualBasic.DueDate>|<span data-ttu-id="f4159-159">指示在调用财务方法时付款何时到期。</span><span class="sxs-lookup"><span data-stu-id="f4159-159">Indicates when payments are due when calling financial methods.</span></span>|  
|<xref:Microsoft.VisualBasic.FileIO.FieldType>|<span data-ttu-id="f4159-160">指示文本字段是分隔的还是固定宽度的。</span><span class="sxs-lookup"><span data-stu-id="f4159-160">Indicates whether text fields are delimited or fixed-width.</span></span>|  
|<xref:Microsoft.VisualBasic.FileAttribute>|<span data-ttu-id="f4159-161">指示当调用文件访问函数时要使用的文件特性。</span><span class="sxs-lookup"><span data-stu-id="f4159-161">Indicates the file attributes to use when calling file-access functions.</span></span>|  
|<xref:Microsoft.VisualBasic.FirstDayOfWeek>|<span data-ttu-id="f4159-162">指示在调用与日期相关的函数时使用的每周的第一天。</span><span class="sxs-lookup"><span data-stu-id="f4159-162">Indicates the first day of the week to use when calling date-related functions.</span></span>|  
|<xref:Microsoft.VisualBasic.FirstWeekOfYear>|<span data-ttu-id="f4159-163">指示在调用与日期相关的函数时使用的每年的第一周。</span><span class="sxs-lookup"><span data-stu-id="f4159-163">Indicates the first week of the year to use when calling date-related functions.</span></span>|  
|<xref:Microsoft.VisualBasic.MsgBoxResult>|<span data-ttu-id="f4159-164">指示在消息框上按下了哪个按钮，由 <xref:Microsoft.VisualBasic.Interaction.MsgBox%2A> 函数返回。</span><span class="sxs-lookup"><span data-stu-id="f4159-164">Indicates which button was pressed on a message box, returned by the <xref:Microsoft.VisualBasic.Interaction.MsgBox%2A> function.</span></span>|  
|<xref:Microsoft.VisualBasic.MsgBoxStyle>|<span data-ttu-id="f4159-165">指示调用 <xref:Microsoft.VisualBasic.Interaction.MsgBox%2A> 函数时显示的按钮。</span><span class="sxs-lookup"><span data-stu-id="f4159-165">Indicates which buttons to display when calling the <xref:Microsoft.VisualBasic.Interaction.MsgBox%2A> function.</span></span>|  
|<xref:Microsoft.VisualBasic.OpenAccess>|<span data-ttu-id="f4159-166">指示调用文件访问函数时如何打开文件。</span><span class="sxs-lookup"><span data-stu-id="f4159-166">Indicates how to open a file when calling file-access functions.</span></span>|  
|<xref:Microsoft.VisualBasic.OpenMode>|<span data-ttu-id="f4159-167">指示调用文件访问函数时如何打开文件。</span><span class="sxs-lookup"><span data-stu-id="f4159-167">Indicates how to open a file when calling file-access functions.</span></span>|  
|<xref:Microsoft.VisualBasic.OpenShare>|<span data-ttu-id="f4159-168">指示调用文件访问函数时如何打开文件。</span><span class="sxs-lookup"><span data-stu-id="f4159-168">Indicates how to open a file when calling file-access functions.</span></span>|  
|<xref:Microsoft.VisualBasic.FileIO.RecycleOption>|<span data-ttu-id="f4159-169">指定文件是应永久删除还是放入“回收站”中。</span><span class="sxs-lookup"><span data-stu-id="f4159-169">Specifies whether a file should be deleted permanently or placed in the Recycle Bin.</span></span>|  
|<xref:Microsoft.VisualBasic.FileIO.SearchOption>|<span data-ttu-id="f4159-170">指定是搜索所有目录还是仅搜索顶级目录。</span><span class="sxs-lookup"><span data-stu-id="f4159-170">Specifies whether to search all or only top-level directories.</span></span>|  
|<xref:Microsoft.VisualBasic.TriState>|<span data-ttu-id="f4159-171">指示 `Boolean` 值，或者在调用数字格式设置函数时是否应使用默认值。</span><span class="sxs-lookup"><span data-stu-id="f4159-171">Indicates a `Boolean` value or whether the default should be used when calling number-formatting functions.</span></span>|  
|<xref:Microsoft.VisualBasic.FileIO.UICancelOption>|<span data-ttu-id="f4159-172">指定当用户在操作过程中单击 " **取消** " 时应执行的操作。</span><span class="sxs-lookup"><span data-stu-id="f4159-172">Specifies what should be done if the user clicks **Cancel** during an operation.</span></span>|  
|<xref:Microsoft.VisualBasic.FileIO.UIOption>|<span data-ttu-id="f4159-173">指定在复制、删除或移动文件或目录时是否显示进度对话框。</span><span class="sxs-lookup"><span data-stu-id="f4159-173">Specifies whether or not to show a progress dialog when copying, deleting, or moving files or directories.</span></span>|  
|<xref:Microsoft.VisualBasic.VariantType>|<span data-ttu-id="f4159-174">指示由 <xref:Microsoft.VisualBasic.Information.VarType%2A> 函数返回的变量对象的类型。</span><span class="sxs-lookup"><span data-stu-id="f4159-174">Indicates the type of a variant object, returned by the <xref:Microsoft.VisualBasic.Information.VarType%2A> function.</span></span>|  
|<xref:Microsoft.VisualBasic.VbStrConv>|<span data-ttu-id="f4159-175">指示调用 <xref:Microsoft.VisualBasic.Strings.StrConv%2A> 函数时要执行的转换类型。</span><span class="sxs-lookup"><span data-stu-id="f4159-175">Indicates which type of conversion to perform when calling the <xref:Microsoft.VisualBasic.Strings.StrConv%2A> function.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f4159-176">请参阅</span><span class="sxs-lookup"><span data-stu-id="f4159-176">See also</span></span>

- [<span data-ttu-id="f4159-177">Visual Basic 语言参考</span><span class="sxs-lookup"><span data-stu-id="f4159-177">Visual Basic Language Reference</span></span>](index.md)
- [<span data-ttu-id="f4159-178">常量概述</span><span class="sxs-lookup"><span data-stu-id="f4159-178">Constants Overview</span></span>](../programming-guide/language-features/constants-enums/constants-overview.md)
- [<span data-ttu-id="f4159-179">枚举概述</span><span class="sxs-lookup"><span data-stu-id="f4159-179">Enumerations Overview</span></span>](../programming-guide/language-features/constants-enums/enumerations-overview.md)
