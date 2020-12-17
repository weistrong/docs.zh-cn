---
title: dotnet sln 命令
description: 使用 dotnet-sln 命令，可以便捷地在解决方案文件中添加、删除和列出项目。
ms.date: 12/07/2020
ms.openlocfilehash: 480634550f6fa1983bb46f51b439dc8a686ead3c
ms.sourcegitcommit: 45c7148f2483db2501c1aa696ab6ed2ed8cb71b2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/08/2020
ms.locfileid: "96851688"
---
# <a name="dotnet-sln"></a><span data-ttu-id="9bf71-103">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="9bf71-103">dotnet sln</span></span>

<span data-ttu-id="9bf71-104">**本文适用于：** ✔️ .NET Core 2.x SDK 及更高版本</span><span class="sxs-lookup"><span data-stu-id="9bf71-104">**This article applies to:** ✔️ .NET Core 2.x SDK and later versions</span></span>

## <a name="name"></a><span data-ttu-id="9bf71-105">“属性”</span><span class="sxs-lookup"><span data-stu-id="9bf71-105">Name</span></span>

<span data-ttu-id="9bf71-106">`dotnet sln` - 在 .NET 解决方案文件中列出或修改项目。</span><span class="sxs-lookup"><span data-stu-id="9bf71-106">`dotnet sln` - Lists or modifies the projects in a .NET solution file.</span></span>

## <a name="synopsis"></a><span data-ttu-id="9bf71-107">摘要</span><span class="sxs-lookup"><span data-stu-id="9bf71-107">Synopsis</span></span>

```dotnetcli
dotnet sln [<SOLUTION_FILE>] [command]

dotnet sln [command] -h|--help
```

## <a name="description"></a><span data-ttu-id="9bf71-108">描述</span><span class="sxs-lookup"><span data-stu-id="9bf71-108">Description</span></span>

<span data-ttu-id="9bf71-109">使用 `dotnet sln` 命令，可以便捷地在解决方案文件中列出和修改项目。</span><span class="sxs-lookup"><span data-stu-id="9bf71-109">The `dotnet sln` command provides a convenient way to list and modify projects in a solution file.</span></span>

<span data-ttu-id="9bf71-110">若要使用 `dotnet sln` 命令，必须存在解决方案文件。</span><span class="sxs-lookup"><span data-stu-id="9bf71-110">To use the `dotnet sln` command, the solution file must already exist.</span></span> <span data-ttu-id="9bf71-111">如果需要创建一个解决方案文件，请使用 [dotnet new](dotnet-new.md) 命令，如下例所示：</span><span class="sxs-lookup"><span data-stu-id="9bf71-111">If you need to create one, use the [dotnet new](dotnet-new.md) command, as in the following example:</span></span>

```dotnetcli
dotnet new sln
```

## <a name="arguments"></a><span data-ttu-id="9bf71-112">自变量</span><span class="sxs-lookup"><span data-stu-id="9bf71-112">Arguments</span></span>

- **`SOLUTION_FILE`**

  <span data-ttu-id="9bf71-113">要使用的解决方案文件。</span><span class="sxs-lookup"><span data-stu-id="9bf71-113">The solution file to use.</span></span> <span data-ttu-id="9bf71-114">如果省略此参数，此命令会搜索当前目录来获取一个解决方案文件。</span><span class="sxs-lookup"><span data-stu-id="9bf71-114">If this argument is omitted, the command searches the current directory for one.</span></span> <span data-ttu-id="9bf71-115">如果未找到解决方案文件或找到多个解决方案文件，则该命令将失败。</span><span class="sxs-lookup"><span data-stu-id="9bf71-115">If it finds no solution file or multiple solution files, the command fails.</span></span>

## <a name="options"></a><span data-ttu-id="9bf71-116">选项</span><span class="sxs-lookup"><span data-stu-id="9bf71-116">Options</span></span>

- **`-h|--help`**

  <span data-ttu-id="9bf71-117">打印出有关如何使用命令的说明。</span><span class="sxs-lookup"><span data-stu-id="9bf71-117">Prints out a description of how to use the command.</span></span>

## <a name="commands"></a><span data-ttu-id="9bf71-118">命令</span><span class="sxs-lookup"><span data-stu-id="9bf71-118">Commands</span></span>

### `list`

<span data-ttu-id="9bf71-119">列出解决方案文件中的所有项目。</span><span class="sxs-lookup"><span data-stu-id="9bf71-119">Lists all projects in a solution file.</span></span>

#### <a name="synopsis"></a><span data-ttu-id="9bf71-120">摘要</span><span class="sxs-lookup"><span data-stu-id="9bf71-120">Synopsis</span></span>

```dotnetcli
dotnet sln list [-h|--help]
```

#### <a name="arguments"></a><span data-ttu-id="9bf71-121">自变量</span><span class="sxs-lookup"><span data-stu-id="9bf71-121">Arguments</span></span>

- **`SOLUTION_FILE`**

  <span data-ttu-id="9bf71-122">要使用的解决方案文件。</span><span class="sxs-lookup"><span data-stu-id="9bf71-122">The solution file to use.</span></span> <span data-ttu-id="9bf71-123">如果省略此参数，此命令会搜索当前目录来获取一个解决方案文件。</span><span class="sxs-lookup"><span data-stu-id="9bf71-123">If this argument is omitted, the command searches the current directory for one.</span></span> <span data-ttu-id="9bf71-124">如果未找到解决方案文件或找到多个解决方案文件，则该命令将失败。</span><span class="sxs-lookup"><span data-stu-id="9bf71-124">If it finds no solution file or multiple solution files, the command fails.</span></span>

#### <a name="options"></a><span data-ttu-id="9bf71-125">选项</span><span class="sxs-lookup"><span data-stu-id="9bf71-125">Options</span></span>

- **`-h|--help`**

  <span data-ttu-id="9bf71-126">打印出有关如何使用命令的说明。</span><span class="sxs-lookup"><span data-stu-id="9bf71-126">Prints out a description of how to use the command.</span></span>
  
### `add`

<span data-ttu-id="9bf71-127">将一个或多个项目添加到解决方案文件。</span><span class="sxs-lookup"><span data-stu-id="9bf71-127">Adds one or more projects to the solution file.</span></span>

#### <a name="synopsis"></a><span data-ttu-id="9bf71-128">摘要</span><span class="sxs-lookup"><span data-stu-id="9bf71-128">Synopsis</span></span>

```dotnetcli
dotnet sln [<SOLUTION_FILE>] add [--in-root] [-s|--solution-folder <PATH>] <PROJECT_PATH> [<PROJECT_PATH>...]
dotnet sln add [-h|--help]
```

#### <a name="arguments"></a><span data-ttu-id="9bf71-129">自变量</span><span class="sxs-lookup"><span data-stu-id="9bf71-129">Arguments</span></span>

- **`SOLUTION_FILE`**

  <span data-ttu-id="9bf71-130">要使用的解决方案文件。</span><span class="sxs-lookup"><span data-stu-id="9bf71-130">The solution file to use.</span></span> <span data-ttu-id="9bf71-131">如果未指定，此命令会搜索当前目录以获取一个解决方案文件，如果找到多个解决方案文件，则该命令将失败。</span><span class="sxs-lookup"><span data-stu-id="9bf71-131">If it is unspecified, the command searches the current directory for one and fails if there are multiple solution files.</span></span>

- **`PROJECT_PATH`**

  <span data-ttu-id="9bf71-132">要添加到解决方案的一个或多个项目的路径。</span><span class="sxs-lookup"><span data-stu-id="9bf71-132">The path to the project or projects to add to the solution.</span></span> <span data-ttu-id="9bf71-133">Unix/Linux shell [glob 模式](https://en.wikipedia.org/wiki/Glob_(programming))扩展由 `dotnet sln` 命令正确处理。</span><span class="sxs-lookup"><span data-stu-id="9bf71-133">Unix/Linux shell [globbing pattern](https://en.wikipedia.org/wiki/Glob_(programming)) expansions are processed correctly by the `dotnet sln` command.</span></span>

#### <a name="options"></a><span data-ttu-id="9bf71-134">选项</span><span class="sxs-lookup"><span data-stu-id="9bf71-134">Options</span></span>

- **`-h|--help`**

  <span data-ttu-id="9bf71-135">打印出有关如何使用命令的说明。</span><span class="sxs-lookup"><span data-stu-id="9bf71-135">Prints out a description of how to use the command.</span></span>

- **`--in-root`**

  <span data-ttu-id="9bf71-136">将项目放在解决方案的根目录下，而不是创建解决方案文件夹。</span><span class="sxs-lookup"><span data-stu-id="9bf71-136">Places the projects in the root of the solution, rather than creating a solution folder.</span></span> <span data-ttu-id="9bf71-137">自 .NET Core 3.0 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="9bf71-137">Available since .NET Core 3.0 SDK.</span></span>

- **`-s|--solution-folder <PATH>`**

  <span data-ttu-id="9bf71-138">要将项目添加到的目标解决方案文件夹路径。</span><span class="sxs-lookup"><span data-stu-id="9bf71-138">The destination solution folder path to add the projects to.</span></span> <span data-ttu-id="9bf71-139">自 .NET Core 3.0 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="9bf71-139">Available since .NET Core 3.0 SDK.</span></span>

### `remove`

<span data-ttu-id="9bf71-140">从解决方案文件中删除一个或多个项目。</span><span class="sxs-lookup"><span data-stu-id="9bf71-140">Removes a project or multiple projects from the solution file.</span></span>

#### <a name="synopsis"></a><span data-ttu-id="9bf71-141">摘要</span><span class="sxs-lookup"><span data-stu-id="9bf71-141">Synopsis</span></span>

```dotnetcli
dotnet sln [<SOLUTION_FILE>] remove <PROJECT_PATH> [<PROJECT_PATH>...]
dotnet sln [<SOLUTION_FILE>] remove [-h|--help]
```

#### <a name="arguments"></a><span data-ttu-id="9bf71-142">自变量</span><span class="sxs-lookup"><span data-stu-id="9bf71-142">Arguments</span></span>

- **`SOLUTION_FILE`**

  <span data-ttu-id="9bf71-143">要使用的解决方案文件。</span><span class="sxs-lookup"><span data-stu-id="9bf71-143">The solution file to use.</span></span> <span data-ttu-id="9bf71-144">如果保留未指定，此命令会搜索当前目录以获取一个解决方案文件，如果找到多个解决方案文件，则该命令将失败。</span><span class="sxs-lookup"><span data-stu-id="9bf71-144">If is left unspecified, the command searches the current directory for one and fails if there are multiple solution files.</span></span>

- **`PROJECT_PATH`**

  <span data-ttu-id="9bf71-145">要添加到解决方案的一个或多个项目的路径。</span><span class="sxs-lookup"><span data-stu-id="9bf71-145">The path to the project or projects to add to the solution.</span></span> <span data-ttu-id="9bf71-146">Unix/Linux shell [glob 模式](https://en.wikipedia.org/wiki/Glob_(programming))扩展由 `dotnet sln` 命令正确处理。</span><span class="sxs-lookup"><span data-stu-id="9bf71-146">Unix/Linux shell [globbing pattern](https://en.wikipedia.org/wiki/Glob_(programming)) expansions are processed correctly by the `dotnet sln` command.</span></span>

#### <a name="options"></a><span data-ttu-id="9bf71-147">选项</span><span class="sxs-lookup"><span data-stu-id="9bf71-147">Options</span></span>

- **`-h|--help`**

  <span data-ttu-id="9bf71-148">打印出有关如何使用命令的说明。</span><span class="sxs-lookup"><span data-stu-id="9bf71-148">Prints out a description of how to use the command.</span></span>

## <a name="examples"></a><span data-ttu-id="9bf71-149">示例</span><span class="sxs-lookup"><span data-stu-id="9bf71-149">Examples</span></span>

- <span data-ttu-id="9bf71-150">在解决方案中列出项目：</span><span class="sxs-lookup"><span data-stu-id="9bf71-150">List the projects in a solution:</span></span>

  ```dotnetcli
  dotnet sln todo.sln list
  ```

- <span data-ttu-id="9bf71-151">将一个 C# 项目添加到解决方案中：</span><span class="sxs-lookup"><span data-stu-id="9bf71-151">Add a C# project to a solution:</span></span>

  ```dotnetcli
  dotnet sln add todo-app/todo-app.csproj
  ```

- <span data-ttu-id="9bf71-152">从解决方案中删除一个 C# 项目：</span><span class="sxs-lookup"><span data-stu-id="9bf71-152">Remove a C# project from a solution:</span></span>

  ```dotnetcli
  dotnet sln remove todo-app/todo-app.csproj
  ```

- <span data-ttu-id="9bf71-153">将多个 C# 项目添加到解决方案的根目录中：</span><span class="sxs-lookup"><span data-stu-id="9bf71-153">Add multiple C# projects to the root of a solution:</span></span>

  ```dotnetcli
  dotnet sln todo.sln add todo-app/todo-app.csproj back-end/back-end.csproj --in-root
  ```

- <span data-ttu-id="9bf71-154">将多个 C# 项目添加到解决方案中：</span><span class="sxs-lookup"><span data-stu-id="9bf71-154">Add multiple C# projects to a solution:</span></span>

  ```dotnetcli
  dotnet sln todo.sln add todo-app/todo-app.csproj back-end/back-end.csproj
  ```

- <span data-ttu-id="9bf71-155">从解决方案中删除多个 C# 项目：</span><span class="sxs-lookup"><span data-stu-id="9bf71-155">Remove multiple C# projects from a solution:</span></span>

  ```dotnetcli
  dotnet sln todo.sln remove todo-app/todo-app.csproj back-end/back-end.csproj
  ```

- <span data-ttu-id="9bf71-156">使用 glob 模式（仅限 Unix/Linux）将多个 C# 项目添加到解决方案中：</span><span class="sxs-lookup"><span data-stu-id="9bf71-156">Add multiple C# projects to a solution using a globbing pattern (Unix/Linux only):</span></span>

  ```dotnetcli
  dotnet sln todo.sln add **/*.csproj
  ```

- <span data-ttu-id="9bf71-157">使用 globbing 模式（仅限 Windows PowerShell）将多个 C# 项目添加到解决方案中：</span><span class="sxs-lookup"><span data-stu-id="9bf71-157">Add multiple C# projects to a solution using a globbing pattern (Windows PowerShell only):</span></span>

  ```dotnetcli
  dotnet sln todo.sln add (ls -r **/*.csproj)
  ```

- <span data-ttu-id="9bf71-158">使用 glob 模式（仅限 Unix/Linux）将多个 C# 项目从解决方案中删除：</span><span class="sxs-lookup"><span data-stu-id="9bf71-158">Remove multiple C# projects from a solution using a globbing pattern (Unix/Linux only):</span></span>

  ```dotnetcli
  dotnet sln todo.sln remove **/*.csproj
  ```

- <span data-ttu-id="9bf71-159">使用 globbing 模式（仅限 Windows PowerShell）将多个 C# 项目从解决方案中删除：</span><span class="sxs-lookup"><span data-stu-id="9bf71-159">Remove multiple C# projects from a solution using a globbing pattern (Windows PowerShell only):</span></span>

  ```dotnetcli
  dotnet sln todo.sln remove (ls -r **/*.csproj)
  ```

- <span data-ttu-id="9bf71-160">创建解决方案、控制台应用和两个类库。</span><span class="sxs-lookup"><span data-stu-id="9bf71-160">Create a solution, a console app, and two class libraries.</span></span> <span data-ttu-id="9bf71-161">将项目添加到解决方案，并使用 `dotnet sln` 的 `--solution-folder` 选项将类库组织到一个解决方案文件夹中。</span><span class="sxs-lookup"><span data-stu-id="9bf71-161">Add the projects to the solution, and use the `--solution-folder` option of `dotnet sln` to organize the class libraries into a solution folder.</span></span>

  ```dotnetcli
  dotnet new sln -n mysolution
  dotnet new console -o myapp
  dotnet new classlib -o mylib1
  dotnet new classlib -o mylib2
  dotnet sln mysolution.sln add myapp\myapp.csproj
  dotnet sln mysolution.sln add mylib1\mylib1.csproj --solution-folder mylibs
  dotnet sln mysolution.sln add mylib2\mylib2.csproj --solution-folder mylibs
  ```

  <span data-ttu-id="9bf71-162">以下屏幕截图显示了 Visual Studio 2019“解决方案资源管理器”中的结果：</span><span class="sxs-lookup"><span data-stu-id="9bf71-162">The following screenshot shows the result in Visual Studio 2019 **Solution Explorer**:</span></span>

  :::image type="content" source="media/dotnet-sln/dotnet-sln-solution-folder.png" alt-text="解决方案资源管理器显示了组合到解决方案文件夹中的类库项目。":::
