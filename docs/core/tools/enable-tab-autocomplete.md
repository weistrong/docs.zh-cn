---
title: 启用 tab 自动补全
description: 本文介绍了如何为 .NET CLI 的 PowerShell、Bash、zsh 和 fish 启用 Tab 自动补全。
author: adegeo
ms.author: adegeo
ms.topic: how-to
ms.date: 11/03/2019
ms.openlocfilehash: b5b63166faa1762d9fa82a93aa70aebb33167630
ms.sourcegitcommit: 65af0f0ad316858882845391d60ef7e303b756e8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "99585554"
---
# <a name="how-to-enable-tab-completion-for-the-net-cli"></a><span data-ttu-id="e25c7-103">如何为 .NET CLI 启用 Tab 自动补全</span><span class="sxs-lookup"><span data-stu-id="e25c7-103">How to enable TAB completion for the .NET CLI</span></span>

<span data-ttu-id="e25c7-104"> 本文适用于： ✔️ .NET Core 2.1 SDK 及更高版本</span><span class="sxs-lookup"><span data-stu-id="e25c7-104">**This article applies to:** ✔️ .NET Core 2.1 SDK and later versions</span></span>

<span data-ttu-id="e25c7-105">本文介绍了如何为四种 shell（PowerShell、Bash、zsh 和 fish）配置 Tab 自动补全。</span><span class="sxs-lookup"><span data-stu-id="e25c7-105">This article describes how to configure tab completion for four shells, PowerShell, Bash, zsh, and fish.</span></span> <span data-ttu-id="e25c7-106">对于其他 shell，请参阅相关文档，了解如何配置 tab 自动补全。</span><span class="sxs-lookup"><span data-stu-id="e25c7-106">For other shells, refer to their documentation on how to configure tab completion.</span></span>

<span data-ttu-id="e25c7-107">设置完成后，通过在 shell 中键入 `dotnet` 命令，然后按下 Tab 键即可触发 .NET CLI 的 Tab 自动补全。</span><span class="sxs-lookup"><span data-stu-id="e25c7-107">Once set up, tab completion for the .NET CLI is triggered by typing a `dotnet` command in the shell, and then pressing the TAB key.</span></span> <span data-ttu-id="e25c7-108">当前命令行将发送到 `dotnet complete` 命令，结果将由 shell 处理。</span><span class="sxs-lookup"><span data-stu-id="e25c7-108">The current command line is sent to the `dotnet complete` command, and the results are processed by your shell.</span></span> <span data-ttu-id="e25c7-109">可以通过直接向 `dotnet complete` 命令发送内容来测试结果而无需启用 tab 自动补全。</span><span class="sxs-lookup"><span data-stu-id="e25c7-109">You can test the results without enabling tab completion by sending something directly to the `dotnet complete` command.</span></span> <span data-ttu-id="e25c7-110">例如：</span><span class="sxs-lookup"><span data-stu-id="e25c7-110">For example:</span></span>

```console
> dotnet complete "dotnet a"
add
clean
--diagnostics
migrate
pack
```

<span data-ttu-id="e25c7-111">如果该命令不起作用，请确保已安装 .NET Core 2.0 SDK 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="e25c7-111">If that command doesn't work, make sure that .NET Core 2.0 SDK or above is installed.</span></span> <span data-ttu-id="e25c7-112">如果已安装，但该命令仍不起作用，请确保 `dotnet` 命令解析为 .NET Core 2.0 SDK 及更高版本。</span><span class="sxs-lookup"><span data-stu-id="e25c7-112">If it's installed, but that command still doesn't work, make sure that the `dotnet` command resolves to a version of .NET Core 2.0 SDK and above.</span></span> <span data-ttu-id="e25c7-113">使用 `dotnet --version` 命令查看当前路径解析为的 `dotnet` 的版本。</span><span class="sxs-lookup"><span data-stu-id="e25c7-113">Use the `dotnet --version` command to see what version of `dotnet` your current path is resolving to.</span></span> <span data-ttu-id="e25c7-114">有关详细信息，请参阅[选择要使用的 .NET 版本](../versions/selection.md)。</span><span class="sxs-lookup"><span data-stu-id="e25c7-114">For more information, see [Select the .NET version to use](../versions/selection.md).</span></span>

### <a name="examples"></a><span data-ttu-id="e25c7-115">示例</span><span class="sxs-lookup"><span data-stu-id="e25c7-115">Examples</span></span>

<span data-ttu-id="e25c7-116">下面是 tab 自动补全提供的一些示例：</span><span class="sxs-lookup"><span data-stu-id="e25c7-116">Here are some examples of what tab completion provides:</span></span>

<span data-ttu-id="e25c7-117">输入</span><span class="sxs-lookup"><span data-stu-id="e25c7-117">Input</span></span>                                | <span data-ttu-id="e25c7-118">将变为</span><span class="sxs-lookup"><span data-stu-id="e25c7-118">becomes</span></span>                                                                     | <span data-ttu-id="e25c7-119">因为</span><span class="sxs-lookup"><span data-stu-id="e25c7-119">because</span></span>
:------------------------------------|:----------------------------------------------------------------------------|:--------------------------------
`dotnet a⇥`                          | `dotnet add`                                                                 | <span data-ttu-id="e25c7-120">`add` 是第一项子命令，按字母排序。</span><span class="sxs-lookup"><span data-stu-id="e25c7-120">`add` is the first subcommand, alphabetically.</span></span>
`dotnet add p⇥`                      | `dotnet add --help`                                                          | <span data-ttu-id="e25c7-121">Tab 自动补全匹配子字符串，`--help` 首先按字母顺序排列。</span><span class="sxs-lookup"><span data-stu-id="e25c7-121">Tab completion matches substrings and `--help` comes first alphabetically.</span></span>
`dotnet add p⇥⇥`                    | `dotnet add package`                                                          | <span data-ttu-id="e25c7-122">第二次按 Tab 将显示下一条建议。</span><span class="sxs-lookup"><span data-stu-id="e25c7-122">Pressing tab a second time brings up the next suggestion.</span></span>
`dotnet add package Microsoft⇥`      | `dotnet add package Microsoft.ApplicationInsights.Web`                      | <span data-ttu-id="e25c7-123">结果按字母顺序返回。</span><span class="sxs-lookup"><span data-stu-id="e25c7-123">Results are returned alphabetically.</span></span>
`dotnet remove reference ⇥`          | `dotnet remove reference ..\..\src\OmniSharp.DotNet\OmniSharp.DotNet.csproj` | <span data-ttu-id="e25c7-124">Tab 自动补全是可识别的项目文件。</span><span class="sxs-lookup"><span data-stu-id="e25c7-124">Tab completion is project file aware.</span></span>

## <a name="powershell"></a><span data-ttu-id="e25c7-125">PowerShell</span><span class="sxs-lookup"><span data-stu-id="e25c7-125">PowerShell</span></span>

<span data-ttu-id="e25c7-126">若要将 Tab 自动补全添加到适用于 .NET CLI 的 PowerShell，请创建或编辑存储在变量 `$PROFILE` 中的配置文件。</span><span class="sxs-lookup"><span data-stu-id="e25c7-126">To add tab completion to **PowerShell** for the .NET CLI, create or edit the profile stored in the variable `$PROFILE`.</span></span> <span data-ttu-id="e25c7-127">有关详细信息，请参阅[如何创建配置文件](/powershell/module/microsoft.powershell.core/about/about_profiles#how-to-create-a-profile)和[配置文件和执行策略](/powershell/module/microsoft.powershell.core/about/about_profiles#profiles-and-execution-policy)。</span><span class="sxs-lookup"><span data-stu-id="e25c7-127">For more information, see [How to create your profile](/powershell/module/microsoft.powershell.core/about/about_profiles#how-to-create-a-profile) and [Profiles and execution policy](/powershell/module/microsoft.powershell.core/about/about_profiles#profiles-and-execution-policy).</span></span>

<span data-ttu-id="e25c7-128">将以下代码添加到配置文件中：</span><span class="sxs-lookup"><span data-stu-id="e25c7-128">Add the following code to your profile:</span></span>

```powershell
# PowerShell parameter completion shim for the dotnet CLI
Register-ArgumentCompleter -Native -CommandName dotnet -ScriptBlock {
     param($commandName, $wordToComplete, $cursorPosition)
         dotnet complete --position $cursorPosition "$wordToComplete" | ForEach-Object {
            [System.Management.Automation.CompletionResult]::new($_, $_, 'ParameterValue', $_)
         }
 }
```

## <a name="bash"></a><span data-ttu-id="e25c7-129">bash</span><span class="sxs-lookup"><span data-stu-id="e25c7-129">bash</span></span>

<span data-ttu-id="e25c7-130">若要将 Tab 自动补全添加到适用于 .NET CLI 的 bash shell，请将以下代码添加到 `.bashrc` 文件：</span><span class="sxs-lookup"><span data-stu-id="e25c7-130">To add tab completion to your **bash** shell for the .NET CLI, add the following code to your `.bashrc` file:</span></span>

```bash
# bash parameter completion for the dotnet CLI

_dotnet_bash_complete()
{
  local word=${COMP_WORDS[COMP_CWORD]}

  local completions
  completions="$(dotnet complete --position "${COMP_POINT}" "${COMP_LINE}" 2>/dev/null)"
  if [ $? -ne 0 ]; then
    completions=""
  fi

  COMPREPLY=( $(compgen -W "$completions" -- "$word") )
}

complete -f -F _dotnet_bash_complete dotnet
```

## <a name="zsh"></a><span data-ttu-id="e25c7-131">zsh</span><span class="sxs-lookup"><span data-stu-id="e25c7-131">zsh</span></span>

<span data-ttu-id="e25c7-132">若要将 Tab 自动补全添加到适用于 .NET CLI 的 zsh shell，请将以下代码添加到 `.zshrc` 文件：</span><span class="sxs-lookup"><span data-stu-id="e25c7-132">To add tab completion to your **zsh** shell for the .NET CLI, add the following code to your `.zshrc` file:</span></span>

```zsh
# zsh parameter completion for the dotnet CLI

_dotnet_zsh_complete()
{
  local completions=("$(dotnet complete "$words")")

  reply=( "${(ps:\n:)completions}" )
}

compctl -K _dotnet_zsh_complete dotnet
```

## <a name="fish"></a><span data-ttu-id="e25c7-133">fish</span><span class="sxs-lookup"><span data-stu-id="e25c7-133">fish</span></span>

<span data-ttu-id="e25c7-134">若要向 .NET CLI 的 fish shell 添加 Tab 自动补全，请将以下代码添加到 `config.fish` 文件中：</span><span class="sxs-lookup"><span data-stu-id="e25c7-134">To add tab completion to your **fish** shell for the .NET CLI, add the following code to your `config.fish` file:</span></span>

```fish
complete -f -c dotnet -a "(dotnet complete)"
```
