---
title: 使用 Visual Studio 创建 .NET 类库
description: 了解如何使用 Visual Studio 创建 .NET 类库。
ms.date: 08/07/2020
dev_langs:
- csharp
- vb
ms.custom: vs-dotnet,contperf-fy21q1
ms.openlocfilehash: 2d9b02a155c950b77565a66417948568f5fa039f
ms.sourcegitcommit: d0990c1c1ab2f81908360f47eafa8db9aa165137
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/15/2020
ms.locfileid: "97513115"
---
# <a name="tutorial-create-a-net-class-library-using-visual-studio"></a><span data-ttu-id="56c3f-103">教程：使用 Visual Studio 创建 .NET 类库</span><span class="sxs-lookup"><span data-stu-id="56c3f-103">Tutorial: Create a .NET class library using Visual Studio</span></span>

<span data-ttu-id="56c3f-104">在本教程中，将创建包含一个字符串处理方法的简单类库。</span><span class="sxs-lookup"><span data-stu-id="56c3f-104">In this tutorial, you create a simple class library that contains a single string-handling method.</span></span>

<span data-ttu-id="56c3f-105">类库定义的是可以由应用程序调用的类型和方法。</span><span class="sxs-lookup"><span data-stu-id="56c3f-105">A *class library* defines types and methods that are called by an application.</span></span> <span data-ttu-id="56c3f-106">如果库以 .NET Standard 2.0 为目标，则支持 .NET Standard 2.0 的任何 .NET 实现（包括 .NET Framework）均可调用该库。</span><span class="sxs-lookup"><span data-stu-id="56c3f-106">If the library targets .NET Standard 2.0, it can be called by any .NET implementation (including .NET Framework) that supports .NET Standard 2.0.</span></span> <span data-ttu-id="56c3f-107">如果库以 .NET 5 为目标，则以 .NET 5 为目标的任何应用程序均可调用该库。</span><span class="sxs-lookup"><span data-stu-id="56c3f-107">If the library targets .NET 5, it can be called by any application that targets .NET 5.</span></span> <span data-ttu-id="56c3f-108">本教程演示如何以 .NET 5 为目标。</span><span class="sxs-lookup"><span data-stu-id="56c3f-108">This tutorial shows how to target .NET 5.</span></span>

<span data-ttu-id="56c3f-109">创建类库后，可将其作为 NuGet 包或作为与使用该类库的应用程序捆绑在一起的组件进行分发。</span><span class="sxs-lookup"><span data-stu-id="56c3f-109">When you create a class library, you can distribute it as a NuGet package or as a component bundled with the application that uses it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="56c3f-110">必备条件</span><span class="sxs-lookup"><span data-stu-id="56c3f-110">Prerequisites</span></span>

- <span data-ttu-id="56c3f-111">安装了具有“.NET Core 跨平台开发”工作负载的 [Visual Studio 2019 版本 16.8 或更高版本](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019)。</span><span class="sxs-lookup"><span data-stu-id="56c3f-111">[Visual Studio 2019 version 16.8 or a later version](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019) with the **.NET Core cross-platform development** workload installed.</span></span> <span data-ttu-id="56c3f-112">选择此工作负载时，将自动安装 .NET 5.0 SDK。</span><span class="sxs-lookup"><span data-stu-id="56c3f-112">The .NET 5.0 SDK is automatically installed when you select this workload.</span></span> <span data-ttu-id="56c3f-113">本教程假设已启用“在‘新建项目’中显示所有 .NET Core 模板”，如[教程：使用 Visual Studio 创建 .NET 控制台应用程序](with-visual-studio.md)中所示。</span><span class="sxs-lookup"><span data-stu-id="56c3f-113">This tutorial assumes you have enabled **Show all .NET Core templates in the New project**, as shown in [Tutorial: Create a .NET console application using Visual Studio](with-visual-studio.md).</span></span>

## <a name="create-a-solution"></a><span data-ttu-id="56c3f-114">创建解决方案</span><span class="sxs-lookup"><span data-stu-id="56c3f-114">Create a solution</span></span>

<span data-ttu-id="56c3f-115">首先，创建一个空白解决方案来放置类库项目。</span><span class="sxs-lookup"><span data-stu-id="56c3f-115">Start by creating a blank solution to put the class library project in.</span></span> <span data-ttu-id="56c3f-116">Visual Studio 解决方案用作一个或多个项目的容器。</span><span class="sxs-lookup"><span data-stu-id="56c3f-116">A Visual Studio solution serves as a container for one or more projects.</span></span> <span data-ttu-id="56c3f-117">将其他相关项目添加到同一个解决方案中。</span><span class="sxs-lookup"><span data-stu-id="56c3f-117">You'll add additional, related projects to the same solution.</span></span>

<span data-ttu-id="56c3f-118">创建空白解决方案：</span><span class="sxs-lookup"><span data-stu-id="56c3f-118">To create the blank solution:</span></span>

1. <span data-ttu-id="56c3f-119">启动 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="56c3f-119">Start Visual Studio.</span></span>

2. <span data-ttu-id="56c3f-120">在“开始”窗口上，选择“创建新项目”。</span><span class="sxs-lookup"><span data-stu-id="56c3f-120">On the start window, choose **Create a new project**.</span></span>

3. <span data-ttu-id="56c3f-121">在“创建新项目”页面上，在搜索框中输入“解决方案”。</span><span class="sxs-lookup"><span data-stu-id="56c3f-121">On the **Create a new project** page, enter **solution** in the search box.</span></span> <span data-ttu-id="56c3f-122">选择“空白解决方案”模板，然后选择“下一步”。</span><span class="sxs-lookup"><span data-stu-id="56c3f-122">Choose the **Blank Solution** template, and then choose **Next**.</span></span>

   :::image type="content" source="media/library-with-visual-studio/blank-solution.png" alt-text="Visual Studio 中的空白解决方案模板":::

4. <span data-ttu-id="56c3f-124">在“配置新项目”页面上，在“项目名称”框中输入“ClassLibraryProjects”。</span><span class="sxs-lookup"><span data-stu-id="56c3f-124">On the **Configure your new project** page, enter **ClassLibraryProjects** in the **Project name** box.</span></span> <span data-ttu-id="56c3f-125">然后选择“创建”。</span><span class="sxs-lookup"><span data-stu-id="56c3f-125">Then choose **Create**.</span></span>

## <a name="create-a-class-library-project"></a><span data-ttu-id="56c3f-126">创建类库项目</span><span class="sxs-lookup"><span data-stu-id="56c3f-126">Create a class library project</span></span>

1. <span data-ttu-id="56c3f-127">将名为“StringLibrary”的新 .NET 类库项目添加到解决方案。</span><span class="sxs-lookup"><span data-stu-id="56c3f-127">Add a new .NET class library project named "StringLibrary" to the solution.</span></span>

   1. <span data-ttu-id="56c3f-128">在“解决方案资源管理器”中，右键单击解决方案并选择“添加” > “新建项目”  。</span><span class="sxs-lookup"><span data-stu-id="56c3f-128">Right-click on the solution in **Solution Explorer** and select **Add** > **New Project**.</span></span>

   1. <span data-ttu-id="56c3f-129">在“创建新项目”页面上，在搜索框中输入“库”。</span><span class="sxs-lookup"><span data-stu-id="56c3f-129">On the **Add a new project** page, enter **library** in the search box.</span></span> <span data-ttu-id="56c3f-130">从“语言”列表中选择“C#”或“Visual Basic”，然后从“平台”列表中选择“所有平台”。</span><span class="sxs-lookup"><span data-stu-id="56c3f-130">Choose **C#** or **Visual Basic** from the Language list, and then choose **All platforms** from the Platform list.</span></span> <span data-ttu-id="56c3f-131">选择“类库”模板，然后选择“下一步” 。</span><span class="sxs-lookup"><span data-stu-id="56c3f-131">Choose the **Class Library** template, and then choose **Next**.</span></span>

   1. <span data-ttu-id="56c3f-132">在“配置新项目”页的“项目名称”框中，输入“StringLibrary”，然后选择“下一步”   。</span><span class="sxs-lookup"><span data-stu-id="56c3f-132">On the **Configure your new project** page, enter **StringLibrary** in the **Project name** box, and then choose **Next**.</span></span>

   1. <span data-ttu-id="56c3f-133">在“其他信息”页上，选择“.NET 5.0 (当前)”，然后选择“创建”  。</span><span class="sxs-lookup"><span data-stu-id="56c3f-133">On the **Additional information** page, select **.NET 5.0 (Current)**, and then choose **Create**.</span></span>

1. <span data-ttu-id="56c3f-134">请检查以确保库以 .NET 的正确版本为目标。</span><span class="sxs-lookup"><span data-stu-id="56c3f-134">Check to make sure that the library targets the correct version of .NET.</span></span> <span data-ttu-id="56c3f-135">右键单击“解决方案资源管理器”中的库项目，然后选择“属性”。</span><span class="sxs-lookup"><span data-stu-id="56c3f-135">Right-click on the library project in **Solution Explorer**, and then select **Properties**.</span></span> <span data-ttu-id="56c3f-136">“目标框架”文本框显示项目以 .NET 5.0 为目标。</span><span class="sxs-lookup"><span data-stu-id="56c3f-136">The **Target Framework** text box shows that the project targets .NET 5.0.</span></span>

1. <span data-ttu-id="56c3f-137">如果使用 Visual Basic，请清除“根命名空间”文本框中的文本。</span><span class="sxs-lookup"><span data-stu-id="56c3f-137">If you're using Visual Basic, clear the text in the **Root namespace** text box.</span></span>

   :::image type="content" source="./media/library-with-visual-studio/vb/library-project-properties.png" alt-text="类库的项目属性":::

   <span data-ttu-id="56c3f-139">对于每个项目，Visual Basic 会自动创建一个与项目名称对应的命名空间。</span><span class="sxs-lookup"><span data-stu-id="56c3f-139">For each project, Visual Basic automatically creates a namespace that corresponds to the project name.</span></span> <span data-ttu-id="56c3f-140">在本教程中，通过使用代码文件中的 [`namespace`](../../visual-basic/language-reference/statements/namespace-statement.md) 关键字定义顶级命名空间。</span><span class="sxs-lookup"><span data-stu-id="56c3f-140">In this tutorial, you define a top-level namespace by using the [`namespace`](../../visual-basic/language-reference/statements/namespace-statement.md) keyword in the code file.</span></span>

1. <span data-ttu-id="56c3f-141">将 Class1.cs 或 Class1.vb 代码窗口中的代码替换为以下代码，并保存文件 。</span><span class="sxs-lookup"><span data-stu-id="56c3f-141">Replace the code in the code window for *Class1.cs*  or *Class1.vb* with the following code, and save the file.</span></span> <span data-ttu-id="56c3f-142">如果未显示想要使用的语言，请更改页面顶部的语言选择器。</span><span class="sxs-lookup"><span data-stu-id="56c3f-142">If the language you want to use is not shown, change the language selector at the top of the page.</span></span>

   :::code language="csharp" source="./snippets/library-with-visual-studio/csharp/StringLibrary/Class1.cs":::
   :::code language="vb" source="./snippets/library-with-visual-studio/vb/StringLibrary/Class1.vb":::

   <span data-ttu-id="56c3f-143">类库 `UtilityLibraries.StringLibrary`包含一个名为 `StartsWithUpper` 的方法。</span><span class="sxs-lookup"><span data-stu-id="56c3f-143">The class library, `UtilityLibraries.StringLibrary`, contains a method named `StartsWithUpper`.</span></span> <span data-ttu-id="56c3f-144">此方法会返回 <xref:System.Boolean> 值，以指明当前字符串实例是否以大写字符开头。</span><span class="sxs-lookup"><span data-stu-id="56c3f-144">This method returns a <xref:System.Boolean> value that indicates whether the current string instance begins with an uppercase character.</span></span> <span data-ttu-id="56c3f-145">Unicode 标准会区分大小写字符。</span><span class="sxs-lookup"><span data-stu-id="56c3f-145">The Unicode standard distinguishes uppercase characters from lowercase characters.</span></span> <span data-ttu-id="56c3f-146">如果为大写字符，<xref:System.Char.IsUpper(System.Char)?displayProperty=nameWithType> 方法返回 `true`。</span><span class="sxs-lookup"><span data-stu-id="56c3f-146">The <xref:System.Char.IsUpper(System.Char)?displayProperty=nameWithType> method returns `true` if a character is uppercase.</span></span>

   <span data-ttu-id="56c3f-147">`StartsWithUpper` 以[扩展方法](../../csharp/programming-guide/classes-and-structs/extension-methods.md)的形式进行实现，这样就可以将其作为 <xref:System.String> 类成员进行调用。</span><span class="sxs-lookup"><span data-stu-id="56c3f-147">`StartsWithUpper` is implemented as an [extension method](../../csharp/programming-guide/classes-and-structs/extension-methods.md) so that you can call it as if it were a member of the <xref:System.String> class.</span></span>

1. <span data-ttu-id="56c3f-148">在菜单栏上，选择“生成” > “生成解决方案”或按 <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>B</kbd>，验证项目是否编译正确 。</span><span class="sxs-lookup"><span data-stu-id="56c3f-148">On the menu bar, select **Build** > **Build Solution** or press <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>B</kbd> to verify that the project compiles without error.</span></span>

## <a name="add-a-console-app-to-the-solution"></a><span data-ttu-id="56c3f-149">向解决方案添加控制台应用</span><span class="sxs-lookup"><span data-stu-id="56c3f-149">Add a console app to the solution</span></span>

<span data-ttu-id="56c3f-150">添加使用类库的控制台应用程序。</span><span class="sxs-lookup"><span data-stu-id="56c3f-150">Add a console application that uses the class library.</span></span> <span data-ttu-id="56c3f-151">应用将提示用户输入字符串，并报告字符串是否以大写字符开头。</span><span class="sxs-lookup"><span data-stu-id="56c3f-151">The app will prompt the user to enter a string and report whether the string begins with an uppercase character.</span></span>

1. <span data-ttu-id="56c3f-152">将名为“ShowCase”的新 .NET 控制台应用程序添加到解决方案。</span><span class="sxs-lookup"><span data-stu-id="56c3f-152">Add a new .NET console application named "ShowCase" to the solution.</span></span>

   1. <span data-ttu-id="56c3f-153">在“解决方案资源管理器”中右键单击解决方案并选择“添加” > “新建项目”。</span><span class="sxs-lookup"><span data-stu-id="56c3f-153">Right-click on the solution in **Solution Explorer** and select **Add** > **New project**.</span></span>

   1. <span data-ttu-id="56c3f-154">在“创建新项目”页面，在搜索框中输入“控制台”。</span><span class="sxs-lookup"><span data-stu-id="56c3f-154">On the **Add a new project** page, enter **console** in the search box.</span></span> <span data-ttu-id="56c3f-155">从“语言”列表中选择“C#”或“Visual Basic”，然后从“平台”列表中选择“所有平台”。</span><span class="sxs-lookup"><span data-stu-id="56c3f-155">Choose **C#** or **Visual Basic** from the Language list, and then choose **All platforms** from the Platform list.</span></span>

   1. <span data-ttu-id="56c3f-156">选择“控制台应用程序”模板，然后选择“下一步” 。</span><span class="sxs-lookup"><span data-stu-id="56c3f-156">Choose the **Console Application** template, and then choose **Next**.</span></span>

   1. <span data-ttu-id="56c3f-157">在“配置新项目”页面，在“项目名称”框中输入“ShowCase”。</span><span class="sxs-lookup"><span data-stu-id="56c3f-157">On the **Configure your new project** page, enter **ShowCase** in the **Project name** box.</span></span> <span data-ttu-id="56c3f-158">然后选择“下一步”  。</span><span class="sxs-lookup"><span data-stu-id="56c3f-158">Then choose **Next**.</span></span>

   1. <span data-ttu-id="56c3f-159">在“其他信息”页上，选择“目标框架”框中的“.NET 5.0 (当前)”  。</span><span class="sxs-lookup"><span data-stu-id="56c3f-159">On the **Additional information** page, select **.NET 5.0 (Current)** in the **Target Framework** box.</span></span> <span data-ttu-id="56c3f-160">然后选择“创建”。</span><span class="sxs-lookup"><span data-stu-id="56c3f-160">Then choose **Create**.</span></span>

1. <span data-ttu-id="56c3f-161">在“Program.cs”或“Program.vb”文件的代码窗口中，将所有代码替换为以下代码 。</span><span class="sxs-lookup"><span data-stu-id="56c3f-161">In the code window for the *Program.cs* or *Program.vb* file, replace all of the code with the following code.</span></span>

   :::code language="csharp" source="./snippets/library-with-visual-studio/csharp/ShowCase/Program.cs":::
   :::code language="vb" source="./snippets/library-with-visual-studio/vb/ShowCase/Program.vb":::

   <span data-ttu-id="56c3f-162">该代码使用 `row` 变量来维护写入到控制台窗口的数据行数计数。</span><span class="sxs-lookup"><span data-stu-id="56c3f-162">The code uses the `row` variable to maintain a count of the number of rows of data written to the console window.</span></span> <span data-ttu-id="56c3f-163">如果大于或等于 25，该代码将清除控制台窗口，并向用户显示一条消息。</span><span class="sxs-lookup"><span data-stu-id="56c3f-163">Whenever it's greater than or equal to 25, the code clears the console window and displays a message to the user.</span></span>

   <span data-ttu-id="56c3f-164">该程序会提示用户输入字符串。</span><span class="sxs-lookup"><span data-stu-id="56c3f-164">The program prompts the user to enter a string.</span></span> <span data-ttu-id="56c3f-165">它会指明字符串是否以大写字符开头。</span><span class="sxs-lookup"><span data-stu-id="56c3f-165">It indicates whether the string starts with an uppercase character.</span></span> <span data-ttu-id="56c3f-166">如果用户没有输入字符串就按 <kbd>Enter</kbd> 键，那么应用程序会终止，控制台窗口会关闭。</span><span class="sxs-lookup"><span data-stu-id="56c3f-166">If the user presses the <kbd>Enter</kbd> key without entering a string, the application ends, and the console window closes.</span></span>

## <a name="add-a-project-reference"></a><span data-ttu-id="56c3f-167">添加项目引用</span><span class="sxs-lookup"><span data-stu-id="56c3f-167">Add a project reference</span></span>

<span data-ttu-id="56c3f-168">最初，新的控制台应用项目无权访问类库。</span><span class="sxs-lookup"><span data-stu-id="56c3f-168">Initially, the new console app project doesn't have access to the class library.</span></span> <span data-ttu-id="56c3f-169">若要允许该项目调用类库中的方法，可以创建对类库项目的项目引用。</span><span class="sxs-lookup"><span data-stu-id="56c3f-169">To allow it to call methods in the class library, create a project reference to the class library project.</span></span>

1. <span data-ttu-id="56c3f-170">在“解决方案资源管理器”中，右键单击 `ShowCase` 项目的“依赖项”节点，并选择“添加项目引用”  。</span><span class="sxs-lookup"><span data-stu-id="56c3f-170">In **Solution Explorer**, right-click the `ShowCase` project's **Dependencies** node, and select **Add Project Reference**.</span></span>

   :::image type="content" source="media/library-with-visual-studio/add-reference-context-menu.png" alt-text="在 Visual Studio 中添加引用上下文菜单":::

1. <span data-ttu-id="56c3f-172">在“引用管理器”对话框中，选择“StringLibrary”项目，然后选择“确定”按钮  。</span><span class="sxs-lookup"><span data-stu-id="56c3f-172">In the **Reference Manager** dialog, select the **StringLibrary** project, and select **OK**.</span></span>

   :::image type="content" source="media/library-with-visual-studio/manage-project-references.png" alt-text="选择了“StringLibrary”的“引用管理器”对话框":::

## <a name="run-the-app"></a><span data-ttu-id="56c3f-174">运行应用</span><span class="sxs-lookup"><span data-stu-id="56c3f-174">Run the app</span></span>

1. <span data-ttu-id="56c3f-175">在“**解决方案资源管理器**”中，右键单击“**ShowCase**”项目，在上下文菜单中选择“**设为启动项目**”。</span><span class="sxs-lookup"><span data-stu-id="56c3f-175">In **Solution Explorer**, right-click the **ShowCase** project and select **Set as StartUp Project** in the context menu.</span></span>

   :::image type="content" source="media/library-with-visual-studio/set-startup-project-context-menu.png" alt-text="Visual Studio 中用于设置启动项目的项目上下文菜单":::

1. <span data-ttu-id="56c3f-177">按 Ctrl+F5 编译并运行程序，而不进行调试<kbd></kbd><kbd></kbd>。</span><span class="sxs-lookup"><span data-stu-id="56c3f-177">Press <kbd>Ctrl</kbd>+<kbd>F5</kbd> to compile and run the program without debugging.</span></span>

   :::image type="content" source="media/library-with-visual-studio/visual-studio-project-toolbar.png" alt-text="Visual Studio 中显示“调试”按钮的项目工具栏":::

1. <span data-ttu-id="56c3f-179">输入字符串并按 Enter 以试用程序，然后按 Enter 退出<kbd></kbd><kbd></kbd>。</span><span class="sxs-lookup"><span data-stu-id="56c3f-179">Try out the program by entering strings and pressing <kbd>Enter</kbd>, then press <kbd>Enter</kbd> to exit.</span></span>

   :::image type="content" source="media/library-with-visual-studio/run-showcase.png" alt-text="运行展示的控制台窗口":::

## <a name="additional-resources"></a><span data-ttu-id="56c3f-181">其他资源</span><span class="sxs-lookup"><span data-stu-id="56c3f-181">Additional resources</span></span>

* [<span data-ttu-id="56c3f-182">使用 .NET CLI 开发库</span><span class="sxs-lookup"><span data-stu-id="56c3f-182">Develop libraries with the .NET CLI</span></span>](libraries.md)
* <span data-ttu-id="56c3f-183">[.NET Standard 版本及其支持的平台](../../standard/net-standard.md)。</span><span class="sxs-lookup"><span data-stu-id="56c3f-183">[.NET Standard versions and the platforms they support](../../standard/net-standard.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="56c3f-184">后续步骤</span><span class="sxs-lookup"><span data-stu-id="56c3f-184">Next steps</span></span>

<span data-ttu-id="56c3f-185">在本教程中，你创建了一个类库。</span><span class="sxs-lookup"><span data-stu-id="56c3f-185">In this tutorial, you created a class library.</span></span> <span data-ttu-id="56c3f-186">在下一教程中，你将了解如何对类库进行单元测试。</span><span class="sxs-lookup"><span data-stu-id="56c3f-186">In the next tutorial, you learn how to unit test the class library.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="56c3f-187">使用 Visual Studio 对 .NET 类库进行单元测试</span><span class="sxs-lookup"><span data-stu-id="56c3f-187">Unit test a .NET class library using Visual Studio</span></span>](testing-library-with-visual-studio.md)

<span data-ttu-id="56c3f-188">或者，你可以跳过自动单元测试，并了解如何通过创建 NuGet 包来共享库：</span><span class="sxs-lookup"><span data-stu-id="56c3f-188">Or you can skip automated unit testing and learn how to share the library by creating a NuGet package:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="56c3f-189">使用 Visual Studio 创建和发布包</span><span class="sxs-lookup"><span data-stu-id="56c3f-189">Create and publish a package using Visual Studio</span></span>](/nuget/quickstart/create-and-publish-a-package-using-visual-studio)

<span data-ttu-id="56c3f-190">同时，还可以了解如何发布控制台应用。</span><span class="sxs-lookup"><span data-stu-id="56c3f-190">Or learn how to publish a console app.</span></span> <span data-ttu-id="56c3f-191">如果从本教程中创建的解决方案发布控制台应用，类库将以 .dll 文件的形式随附。</span><span class="sxs-lookup"><span data-stu-id="56c3f-191">If you publish the console app from the solution you created in this tutorial, the class library goes with it as a *.dll* file.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="56c3f-192">使用 Visual Studio 发布 .NET 控制台应用程序</span><span class="sxs-lookup"><span data-stu-id="56c3f-192">Publish a .NET console application using Visual Studio</span></span>](publishing-with-visual-studio.md)
