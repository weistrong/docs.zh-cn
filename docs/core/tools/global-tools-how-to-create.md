---
title: 教程：创建 .NET 工具
description: 了解如何创建 .NET 工具。 工具是一个通过使用 .NET CLI 安装的控制台应用程序。
ms.topic: tutorial
ms.date: 12/14/2020
ms.openlocfilehash: dc5cf014336848ff1a3035647a386419653a083b
ms.sourcegitcommit: 635a0ff775d2447a81ef7233a599b8f88b162e5d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/17/2020
ms.locfileid: "97633892"
---
# <a name="tutorial-create-a-net-tool-using-the-net-cli"></a><span data-ttu-id="3b9d8-104">教程：使用 .NET CLI 创建 .NET 工具</span><span class="sxs-lookup"><span data-stu-id="3b9d8-104">Tutorial: Create a .NET tool using the .NET CLI</span></span>

<span data-ttu-id="3b9d8-105"> 本文适用于： ✔️ .NET Core 2.1 SDK 及更高版本</span><span class="sxs-lookup"><span data-stu-id="3b9d8-105">**This article applies to:** ✔️ .NET Core 2.1 SDK and later versions</span></span>

<span data-ttu-id="3b9d8-106">本教程介绍如何创建和打包 .NET 工具。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-106">This tutorial teaches you how to create and package a .NET tool.</span></span> <span data-ttu-id="3b9d8-107">使用 .NET CLI，你可以创建一个控制台应用程序作为工具，便于其他人安装并运行。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-107">The .NET CLI lets you create a console application as a tool, which others can install and run.</span></span> <span data-ttu-id="3b9d8-108">.NET 工具是从 .NET CLI 安装的 NuGet 包。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-108">.NET tools are NuGet packages that are installed from the .NET CLI.</span></span> <span data-ttu-id="3b9d8-109">有关工具的详细信息，请参阅 [.NET 工具概述](global-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-109">For more information about tools, see [.NET tools overview](global-tools.md).</span></span>

<span data-ttu-id="3b9d8-110">将创建的工具是一个控制台应用程序，它将消息作为输入，并显示消息以及用于创建机器人图像的文本行。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-110">The tool that you'll create is a console application that takes a message as input and displays the message along with lines of text that create the image of a robot.</span></span>

<span data-ttu-id="3b9d8-111">这是一系列教程（包含三个教程）中的第一个。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-111">This is the first in a series of three tutorials.</span></span> <span data-ttu-id="3b9d8-112">在本教程中，将创建并打包工具。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-112">In this tutorial, you create and package a tool.</span></span> <span data-ttu-id="3b9d8-113">在接下来的两个教程中，[使用该工具作为全局工具](global-tools-how-to-use.md)并[使用该工具作为本地工具](local-tools-how-to-use.md)。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-113">In the next two tutorials you [use the tool as a global tool](global-tools-how-to-use.md) and [use the tool as a local tool](local-tools-how-to-use.md).</span></span> <span data-ttu-id="3b9d8-114">无论你是将工具用作全局工具还是用作本地工具，创建工具的过程都是相同的。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-114">The procedures for creating a tool are the same whether you use it as a global tool or as a local tool.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3b9d8-115">必备知识</span><span class="sxs-lookup"><span data-stu-id="3b9d8-115">Prerequisites</span></span>

- <span data-ttu-id="3b9d8-116">[.NET SDK 5.0.100](https://dotnet.microsoft.com/download) 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-116">[.NET SDK 5.0.100](https://dotnet.microsoft.com/download) or a later version.</span></span>

  <span data-ttu-id="3b9d8-117">本教程使用 .NET SDK 5.0，但从 .NET Core SDK 2.1 开始，提供全局工具。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-117">This tutorial uses .NET SDK 5.0, but global tools are available starting in .NET Core SDK 2.1.</span></span> <span data-ttu-id="3b9d8-118">本地工具从 .NET Core SDK 3.0 开始可用。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-118">Local tools are available starting in .NET Core SDK 3.0.</span></span>

- <span data-ttu-id="3b9d8-119">按需选择的文本编辑器或代码编辑器。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-119">A text editor or code editor of your choice.</span></span>

## <a name="create-a-project"></a><span data-ttu-id="3b9d8-120">创建项目</span><span class="sxs-lookup"><span data-stu-id="3b9d8-120">Create a project</span></span>

1. <span data-ttu-id="3b9d8-121">打开命令提示符，创建一个名为“repository”  的文件夹。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-121">Open a command prompt and create a folder named *repository*.</span></span>

1. <span data-ttu-id="3b9d8-122">导航到“repository”文件夹并输入以下命令  ：</span><span class="sxs-lookup"><span data-stu-id="3b9d8-122">Navigate to the *repository* folder and enter the following command:</span></span>

   ```dotnetcli
   dotnet new console -n microsoft.botsay -f net5.0
   ```

   <span data-ttu-id="3b9d8-123">此命令将在“repository”文件夹下创建一个名为“microsoft.botsay”的新文件夹   。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-123">The command creates a new folder named *microsoft.botsay* under the *repository* folder.</span></span>

   > [!NOTE]
   > <span data-ttu-id="3b9d8-124">在本教程中，你将创建一个面向 .NET 5.0 的工具。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-124">For this tutorial you create a tool that targets .NET 5.0.</span></span> <span data-ttu-id="3b9d8-125">若要以其他框架为目标，请更改 `-f|--framework` 选项。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-125">To target a different framework, change the `-f|--framework` option.</span></span> <span data-ttu-id="3b9d8-126">若要以多个框架为目标，请将 `TargetFramework` 元素更改为项目文件中的 `TargetFrameworks` 元素，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="3b9d8-126">To target multiple frameworks, change the `TargetFramework` element to a `TargetFrameworks` element in the project file, as shown in the following example:</span></span>
   >
   > ```xml
   > <Project Sdk="Microsoft.NET.Sdk">
   >   <PropertyGroup>
   >     <OutputType>Exe</OutputType>
   >     <TargetFrameworks>netcoreapp3.1;net5.0</TargetFrameworks>
   >   </PropertyGroup>
   > </Project>
   > ```

1. <span data-ttu-id="3b9d8-127">导航到“microsoft.botsay”文件夹  。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-127">Navigate to the *microsoft.botsay* folder.</span></span>

   ```console
   cd microsoft.botsay
   ```

## <a name="add-the-code"></a><span data-ttu-id="3b9d8-128">添加代码</span><span class="sxs-lookup"><span data-stu-id="3b9d8-128">Add the code</span></span>

1. <span data-ttu-id="3b9d8-129">使用代码编辑器打开 `Program.cs` 文件。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-129">Open the `Program.cs` file with your code editor.</span></span>

1. <span data-ttu-id="3b9d8-130">将下面的 `using` 指令添加到文件的顶部：</span><span class="sxs-lookup"><span data-stu-id="3b9d8-130">Add the following `using` directive to the top of the file:</span></span>

   ```csharp
   using System.Reflection;
   ```

1. <span data-ttu-id="3b9d8-131">将 `Main` 方法替换为以下代码，以便处理应用程序的命令行参数。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-131">Replace the `Main` method with the following code to process the command-line arguments for the application.</span></span>

   ```csharp
   static void Main(string[] args)
   {
       if (args.Length == 0)
       {
           var versionString = Assembly.GetEntryAssembly()
                                   .GetCustomAttribute<AssemblyInformationalVersionAttribute>()
                                   .InformationalVersion
                                   .ToString();

           Console.WriteLine($"botsay v{versionString}");
           Console.WriteLine("-------------");
           Console.WriteLine("\nUsage:");
           Console.WriteLine("  botsay <message>");
           return;
       }

       ShowBot(string.Join(' ', args));
   }
   ```

   <span data-ttu-id="3b9d8-132">如果未传递任何参数，将显示简短的帮助消息。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-132">If no arguments are passed, a short help message is displayed.</span></span> <span data-ttu-id="3b9d8-133">否则，所有参数都将连接到单个字符串中，并通过调用在下一步中创建的 `ShowBot` 方法进行打印。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-133">Otherwise, all of the arguments are concatenated into a single string and printed by calling the `ShowBot` method that you create in the next step.</span></span>

1. <span data-ttu-id="3b9d8-134">添加一个名为 `ShowBot` 的新方法，该方法采用一个字符串参数。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-134">Add a new method named `ShowBot` that takes a string parameter.</span></span> <span data-ttu-id="3b9d8-135">该方法使用文本行打印出消息和机器人图像。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-135">The method prints out the message and an image of a robot using lines of text.</span></span>

   ```csharp
   static void ShowBot(string message)
   {
       string bot = $"\n        {message}";
       bot += @"
       __________________
                         \
                          \
                             ....
                             ....'
                              ....
                           ..........
                       .............'..'..
                    ................'..'.....
                  .......'..........'..'..'....
                 ........'..........'..'..'.....
                .'....'..'..........'..'.......'.
                .'..................'...   ......
                .  ......'.........         .....
                .    _            __        ......
               ..    #            ##        ......
              ....       .                 .......
              ......  .......          ............
               ................  ......................
               ........................'................
              ......................'..'......    .......
           .........................'..'.....       .......
        ........    ..'.............'..'....      ..........
      ..'..'...      ...............'.......      ..........
     ...'......     ...... ..........  ......         .......
    ...........   .......              ........        ......
   .......        '...'.'.              '.'.'.'         ....
   .......       .....'..               ..'.....
      ..       ..........               ..'........
             ............               ..............
            .............               '..............
           ...........'..              .'.'............
          ...............              .'.'.............
         .............'..               ..'..'...........
         ...............                 .'..............
          .........                        ..............
           .....
   ";
       Console.WriteLine(bot);
   }
   ```

1. <span data-ttu-id="3b9d8-136">保存更改。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-136">Save your changes.</span></span>

## <a name="test-the-application"></a><span data-ttu-id="3b9d8-137">测试应用程序</span><span class="sxs-lookup"><span data-stu-id="3b9d8-137">Test the application</span></span>

<span data-ttu-id="3b9d8-138">运行项目并观察输出。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-138">Run the project and see the output.</span></span> <span data-ttu-id="3b9d8-139">尝试使用命令行处的这些变体来查看不同的结果：</span><span class="sxs-lookup"><span data-stu-id="3b9d8-139">Try these variations at the command line to see different results:</span></span>

```dotnetcli
dotnet run
dotnet run -- "Hello from the bot"
dotnet run -- Hello from the bot
```

<span data-ttu-id="3b9d8-140">位于 `--` 分隔符后的所有参数均会传递给应用程序。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-140">All arguments after the `--` delimiter are passed to your application.</span></span>

## <a name="package-the-tool"></a><span data-ttu-id="3b9d8-141">打包工具</span><span class="sxs-lookup"><span data-stu-id="3b9d8-141">Package the tool</span></span>

<span data-ttu-id="3b9d8-142">在将应用程序作为工具打包并分发之前，你需要修改项目文件。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-142">Before you can pack and distribute the application as a tool, you need to modify the project file.</span></span>

1. <span data-ttu-id="3b9d8-143">打开“microsoft.botsay.csproj”文件，然后将三个新的 XML 节点添加到 `<PropertyGroup>` 节点的末尾  ：</span><span class="sxs-lookup"><span data-stu-id="3b9d8-143">Open the *microsoft.botsay.csproj* file and add three new XML nodes to the end of the `<PropertyGroup>` node:</span></span>

   ```xml
   <PackAsTool>true</PackAsTool>
   <ToolCommandName>botsay</ToolCommandName>
   <PackageOutputPath>./nupkg</PackageOutputPath>
   ```

   <span data-ttu-id="3b9d8-144">`<ToolCommandName>` 是一个可选元素，用于指定在安装工具后将调用该工具的命令。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-144">`<ToolCommandName>` is an optional element that specifies the command that will invoke the tool after it's installed.</span></span> <span data-ttu-id="3b9d8-145">如果未提供此元素，则该工具的命令名称为没有“.csproj”  扩展名的项目文件名。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-145">If this element isn't provided, the command name for the tool is the project file name without the *.csproj* extension.</span></span>

   <span data-ttu-id="3b9d8-146">`<PackageOutputPath>` 是一个可选元素，用于确定将在何处生成 NuGet 包。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-146">`<PackageOutputPath>` is an optional element that determines where the NuGet package will be produced.</span></span> <span data-ttu-id="3b9d8-147">NuGet 包是 .NET CLI 用于安装你的工具的包。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-147">The NuGet package is what the .NET CLI uses to install your tool.</span></span>

   <span data-ttu-id="3b9d8-148">项目文件现在类似于以下示例：</span><span class="sxs-lookup"><span data-stu-id="3b9d8-148">The project file now looks like the following example:</span></span>

   ```xml
   <Project Sdk="Microsoft.NET.Sdk">

     <PropertyGroup>

       <OutputType>Exe</OutputType>
       <TargetFramework>net5.0</TargetFramework>

       <PackAsTool>true</PackAsTool>
       <ToolCommandName>botsay</ToolCommandName>
       <PackageOutputPath>./nupkg</PackageOutputPath>

     </PropertyGroup>

   </Project>
   ```

1. <span data-ttu-id="3b9d8-149">通过运行 [dotnet pack](dotnet-pack.md) 命令创建 NuGet 包：</span><span class="sxs-lookup"><span data-stu-id="3b9d8-149">Create a NuGet package by running the [dotnet pack](dotnet-pack.md) command:</span></span>

   ```dotnetcli
   dotnet pack
   ```

   <span data-ttu-id="3b9d8-150">“microsoft.botsay.1.0.0.nupkg”文件在由 microsoft.botsay.csproj 文件的 `<PackageOutputPath>` 值标识的文件夹中创建，在本示例中为“./nupkg”文件夹    。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-150">The *microsoft.botsay.1.0.0.nupkg* file is created in the folder identified by the `<PackageOutputPath>` value from the *microsoft.botsay.csproj* file, which in this example is the *./nupkg* folder.</span></span>

   <span data-ttu-id="3b9d8-151">如果想要公开发布一个工具，你可以将其上传到 `https://www.nuget.org`。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-151">When you want to release a tool publicly, you can upload it to `https://www.nuget.org`.</span></span> <span data-ttu-id="3b9d8-152">该工具在 NuGet 上可用后，开发人员就可以使用 [dotnet tool install](dotnet-tool-install.md) 命令安装该工具。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-152">Once the tool is available on NuGet, developers can install the tool by using the [dotnet tool install](dotnet-tool-install.md) command.</span></span> <span data-ttu-id="3b9d8-153">在本教程中，你将直接从本地“nupkg”  文件夹安装包，因此无需将包上传到 NuGet。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-153">For this tutorial you install the package directly from the local *nupkg* folder, so there's no need to upload the package to NuGet.</span></span>

## <a name="troubleshoot"></a><span data-ttu-id="3b9d8-154">疑难解答</span><span class="sxs-lookup"><span data-stu-id="3b9d8-154">Troubleshoot</span></span>

<span data-ttu-id="3b9d8-155">如果在学习本教程时收到错误消息，请参阅[排查 .NET 工具使用问题](troubleshoot-usage-issues.md)。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-155">If you get an error message while following the tutorial, see [Troubleshoot .NET tool usage issues](troubleshoot-usage-issues.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="3b9d8-156">后续步骤</span><span class="sxs-lookup"><span data-stu-id="3b9d8-156">Next steps</span></span>

<span data-ttu-id="3b9d8-157">在本教程中，你创建了一个控制台应用程序并将其打包为工具。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-157">In this tutorial, you created a console application and packaged it as a tool.</span></span> <span data-ttu-id="3b9d8-158">若要了解如何使用该工具作为全局工具，请转到下一教程。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-158">To learn how to use the tool as a global tool, advance to the next tutorial.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="3b9d8-159">安装和使用全局工具</span><span class="sxs-lookup"><span data-stu-id="3b9d8-159">Install and use a global tool</span></span>](global-tools-how-to-use.md)

<span data-ttu-id="3b9d8-160">如果需要，可以跳过全局工具教程，直接转到本地工具教程。</span><span class="sxs-lookup"><span data-stu-id="3b9d8-160">If you prefer, you can skip the global tools tutorial and go directly to the local tools tutorial.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="3b9d8-161">安装和使用本地工具</span><span class="sxs-lookup"><span data-stu-id="3b9d8-161">Install and use a local tool</span></span>](local-tools-how-to-use.md)
