---
title: dotnet test 命令
description: dotnet test 命令可用于在给定项目中执行单元测试。
ms.date: 04/29/2020
ms.openlocfilehash: 4834da766bd052f44127a72635b65866eb7e3352
ms.sourcegitcommit: a4cecb7389f02c27e412b743f9189bd2a6dea4d6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/14/2021
ms.locfileid: "98189149"
---
# <a name="dotnet-test"></a><span data-ttu-id="ca2b7-103">dotnet test</span><span class="sxs-lookup"><span data-stu-id="ca2b7-103">dotnet test</span></span>

<span data-ttu-id="ca2b7-104">本文适用于： ✔️ .NET Core 2.1 SDK 及更高版本</span><span class="sxs-lookup"><span data-stu-id="ca2b7-104">**This article applies to:** ✔️ .NET Core 2.1 SDK and later versions</span></span>

## <a name="name"></a><span data-ttu-id="ca2b7-105">“属性”</span><span class="sxs-lookup"><span data-stu-id="ca2b7-105">Name</span></span>

<span data-ttu-id="ca2b7-106">`dotnet test` - 用于执行单元测试的 .NET 测试驱动程序。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-106">`dotnet test` - .NET test driver used to execute unit tests.</span></span>

## <a name="synopsis"></a><span data-ttu-id="ca2b7-107">摘要</span><span class="sxs-lookup"><span data-stu-id="ca2b7-107">Synopsis</span></span>

```dotnetcli
dotnet test [<PROJECT> | <SOLUTION> | <DIRECTORY> | <DLL>]
    [-a|--test-adapter-path <ADAPTER_PATH>] [--blame] [--blame-crash]
    [--blame-crash-dump-type <DUMP_TYPE>] [--blame-crash-collect-always]
    [--blame-hang] [--blame-hang-dump-type <DUMP_TYPE>]
    [--blame-hang-timeout <TIMESPAN>]
    [-c|--configuration <CONFIGURATION>]
    [--collect <DATA_COLLECTOR_NAME>]
    [-d|--diag <LOG_FILE>] [-f|--framework <FRAMEWORK>]
    [--filter <EXPRESSION>] [--interactive]
    [-l|--logger <LOGGER>] [--no-build]
    [--nologo] [--no-restore] [-o|--output <OUTPUT_DIRECTORY>]
    [-r|--results-directory <RESULTS_DIR>] [--runtime <RUNTIME_IDENTIFIER>]
    [-s|--settings <SETTINGS_FILE>] [-t|--list-tests]
    [-v|--verbosity <LEVEL>] [[--] <RunSettings arguments>]

dotnet test -h|--help
```

## <a name="description"></a><span data-ttu-id="ca2b7-108">描述</span><span class="sxs-lookup"><span data-stu-id="ca2b7-108">Description</span></span>

<span data-ttu-id="ca2b7-109">`dotnet test` 命令用于在给定的解决方案中执行单元测试。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-109">The `dotnet test` command is used to execute unit tests in a given solution.</span></span> <span data-ttu-id="ca2b7-110">`dotnet test` 命令生成解决方案，并为解决方案中的每个测试项目运行测试主机应用程序。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-110">The `dotnet test` command builds the solution and runs a test host application for each test project in the solution.</span></span> <span data-ttu-id="ca2b7-111">测试主机使用测试框架（例如，MSTest、NUnit 或 xUnit）在给定项目中执行测试，并报告每个测试成功与否。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-111">The test host executes tests in the given project using a test framework, for example: MSTest, NUnit, or xUnit, and reports the success or failure of each test.</span></span> <span data-ttu-id="ca2b7-112">如果所有测试均成功，测试运行程序将返回 0 作为退出代码；否则将返回 1。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-112">If all tests are successful, the test runner returns 0 as an exit code; otherwise if any test fails, it returns 1.</span></span>

<span data-ttu-id="ca2b7-113">对于多目标项目，将为每个目标框架运行测试。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-113">For multi-targeted projects, tests are run for each targeted framework.</span></span> <span data-ttu-id="ca2b7-114">测试主机和单元测试框架打包为 NuGet 包，并还原为项目的普通依赖项。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-114">The test host and the unit test framework are packaged as NuGet packages and are restored as ordinary dependencies for the project.</span></span>

<span data-ttu-id="ca2b7-115">测试项目使用普通 `<PackageReference>` 元素指定测试运行程序，如下方示例项目文件所示：</span><span class="sxs-lookup"><span data-stu-id="ca2b7-115">Test projects specify the test runner using an ordinary `<PackageReference>` element, as seen in the following sample project file:</span></span>

[!code-xml[XUnit Basic Template](../../../samples/snippets/csharp/xunit-test/xunit-test.csproj)]

<span data-ttu-id="ca2b7-116">如果 `Microsoft.NET.Test.Sdk` 是测试主机，则 `xunit` 是测试框架。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-116">Where `Microsoft.NET.Test.Sdk` is the test host, `xunit` is the test framework.</span></span> <span data-ttu-id="ca2b7-117">另外，`xunit.runner.visualstudio` 是测试适配器，可便于 xUnit 框架与测试主机一起运行。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-117">And `xunit.runner.visualstudio` is a test adapter, which allows the xUnit framework to work with the test host.</span></span>

### <a name="implicit-restore"></a><span data-ttu-id="ca2b7-118">隐式还原</span><span class="sxs-lookup"><span data-stu-id="ca2b7-118">Implicit restore</span></span>

[!INCLUDE[dotnet restore note](~/includes/dotnet-restore-note.md)]

## <a name="arguments"></a><span data-ttu-id="ca2b7-119">自变量</span><span class="sxs-lookup"><span data-stu-id="ca2b7-119">Arguments</span></span>

- **`PROJECT | SOLUTION | DIRECTORY | DLL`**

  - <span data-ttu-id="ca2b7-120">指向测试项目的路径。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-120">Path to the test project.</span></span>
  - <span data-ttu-id="ca2b7-121">解决方案的路径。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-121">Path to the solution.</span></span>
  - <span data-ttu-id="ca2b7-122">包含项目或解决方案的目录的路径。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-122">Path to a directory that contains a project or a solution.</span></span>
  - <span data-ttu-id="ca2b7-123">测试项目 .dll 文件的路径。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-123">Path to a test project *.dll* file.</span></span>

  <span data-ttu-id="ca2b7-124">如果未指定，则会在当前目录中搜索项目或解决方案。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-124">If not specified, it searches for a project or a solution in the current directory.</span></span>

## <a name="options"></a><span data-ttu-id="ca2b7-125">选项</span><span class="sxs-lookup"><span data-stu-id="ca2b7-125">Options</span></span>

- **`-a|--test-adapter-path <ADAPTER_PATH>`**

  <span data-ttu-id="ca2b7-126">要在其中搜索其他测试适配器的目录的路径。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-126">Path to a directory to be searched for additional test adapters.</span></span> <span data-ttu-id="ca2b7-127">只检查后缀为 `.TestAdapter.dll` 的 .dll 文件。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-127">Only *.dll* files with suffix `.TestAdapter.dll` are inspected.</span></span> <span data-ttu-id="ca2b7-128">如果未指定，则会搜索测试 .dll 的目录。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-128">If not specified, the directory of the test *.dll* is searched.</span></span>

- **`--blame`**

  <span data-ttu-id="ca2b7-129">在意见模式中运行测试。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-129">Runs the tests in blame mode.</span></span> <span data-ttu-id="ca2b7-130">此选项有助于隔离导致测试主机出现故障的有问题的测试。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-130">This option is helpful in isolating problematic tests that cause the test host to crash.</span></span> <span data-ttu-id="ca2b7-131">检测到故障时，它会在 `TestResults/<Guid>/<Guid>_Sequence.xml` 中创建一个序列文件，用于捕获在出现故障之前运行的测试的顺序。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-131">When a crash is detected, it creates a sequence file in `TestResults/<Guid>/<Guid>_Sequence.xml` that captures the order of tests that were run before the crash.</span></span>

- <span data-ttu-id="ca2b7-132">**`--blame-crash`** （自 .NET 5.0 预览版 SDK 起可用）</span><span class="sxs-lookup"><span data-stu-id="ca2b7-132">**`--blame-crash`** (Available since .NET 5.0 preview SDK)</span></span>

  <span data-ttu-id="ca2b7-133">在追责模式下运行测试，并在测试主机意外退出时收集故障转储。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-133">Runs the tests in blame mode and collects a crash dump when the test host exits unexpectedly.</span></span> <span data-ttu-id="ca2b7-134">此选项取决于所使用的 .NET 版本、错误的类型和操作系统。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-134">This option depends on the version of .NET used, the type of error, and the operating system.</span></span>
  
  <span data-ttu-id="ca2b7-135">对于托管代码中的异常，将在 .NET 5.0 及更高版本上自动收集转储。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-135">For exceptions in managed code, a dump will be automatically collected on .NET 5.0 and later versions.</span></span> <span data-ttu-id="ca2b7-136">对于 testhost 或也在 .NET 5.0 上运行并且出现故障的任何子进程，它将生成转储。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-136">It will generate a dump for testhost or any child process that also ran on .NET 5.0 and crashed.</span></span> <span data-ttu-id="ca2b7-137">本机代码中的故障将不会生成转储。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-137">Crashes in native code will not generate a dump.</span></span> <span data-ttu-id="ca2b7-138">此选项适用于 Windows、macOS 和 Linux。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-138">This option works on Windows, macOS, and Linux.</span></span>
  
  <span data-ttu-id="ca2b7-139">本机代码中的故障转储（或者当使用 .NET Core 3.1 或更早版本时）只能使用 Procdump 在 Windows 上进行收集。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-139">Crash dumps in native code, or when using .NET Core 3.1 or earlier versions, can only be collected on Windows, by using Procdump.</span></span> <span data-ttu-id="ca2b7-140">包含 procdump.exe 和 procdump64.exe 的目录必须位于 PATH 或 PROCDUMP_PATH 环境变量中。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-140">A directory that contains *procdump.exe* and *procdump64.exe* must be in the PATH or PROCDUMP_PATH environment variable.</span></span> <span data-ttu-id="ca2b7-141">[下载工具](/sysinternals/downloads/procdump)。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-141">[Download the tools](/sysinternals/downloads/procdump).</span></span> <span data-ttu-id="ca2b7-142">意味着 `--blame`。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-142">Implies `--blame`.</span></span>
  
  <span data-ttu-id="ca2b7-143">若要从 .NET 5.0 或更高版本上运行的本机应用程序收集故障转储，可以通过将 `VSTEST_DUMP_FORCEPROCDUMP` 环境变量设置为 `1` 来强制执行 Procdump 的使用。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-143">To collect a crash dump from a native application running on .NET 5.0 or later, the usage of Procdump can be forced by setting the `VSTEST_DUMP_FORCEPROCDUMP` environment variable to `1`.</span></span>

- <span data-ttu-id="ca2b7-144">**`--blame-crash-dump-type <DUMP_TYPE>`** （自 .NET 5.0 预览版 SDK 起可用）</span><span class="sxs-lookup"><span data-stu-id="ca2b7-144">**`--blame-crash-dump-type <DUMP_TYPE>`** (Available since .NET 5.0 preview SDK)</span></span>

  <span data-ttu-id="ca2b7-145">要收集的故障转储的类型。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-145">The type of crash dump to be collected.</span></span> <span data-ttu-id="ca2b7-146">意味着 `--blame-crash`。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-146">Implies `--blame-crash`.</span></span>

- <span data-ttu-id="ca2b7-147">**`--blame-crash-collect-always`** （自 .NET 5.0 预览版 SDK 起可用）</span><span class="sxs-lookup"><span data-stu-id="ca2b7-147">**`--blame-crash-collect-always`** (Available since .NET 5.0 preview SDK)</span></span>

  <span data-ttu-id="ca2b7-148">在预期和意外的测试主机退出时收集故障转储。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-148">Collects a crash dump on expected as well as unexpected test host exit.</span></span>

- <span data-ttu-id="ca2b7-149">**`--blame-hang`** （自 .NET 5.0 预览版 SDK 起可用）</span><span class="sxs-lookup"><span data-stu-id="ca2b7-149">**`--blame-hang`** (Available since .NET 5.0 preview SDK)</span></span>

  <span data-ttu-id="ca2b7-150">在追责模式下运行测试，并在测试超过给定超时时长时收集挂起转储。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-150">Run the tests in blame mode and collects a hang dump when a test exceeds the given timeout.</span></span>

- <span data-ttu-id="ca2b7-151">**`--blame-hang-dump-type <DUMP_TYPE>`** （自 .NET 5.0 预览版 SDK 起可用）</span><span class="sxs-lookup"><span data-stu-id="ca2b7-151">**`--blame-hang-dump-type <DUMP_TYPE>`** (Available since .NET 5.0 preview SDK)</span></span>

  <span data-ttu-id="ca2b7-152">要收集的故障转储的类型。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-152">The type of crash dump to be collected.</span></span> <span data-ttu-id="ca2b7-153">它应为 `full`、`mini` 或 `none`。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-153">It should be `full`, `mini`, or `none`.</span></span> <span data-ttu-id="ca2b7-154">指定 `none` 时，测试主机将在超时时终止，但不会收集任何转储。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-154">When `none` is specified, test host is terminated on timeout, but no dump is collected.</span></span> <span data-ttu-id="ca2b7-155">意味着 `--blame-hang`。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-155">Implies `--blame-hang`.</span></span>

- <span data-ttu-id="ca2b7-156">**`--blame-hang-timeout <TIMESPAN>`** （自 .NET 5.0 预览版 SDK 起可用）</span><span class="sxs-lookup"><span data-stu-id="ca2b7-156">**`--blame-hang-timeout <TIMESPAN>`** (Available since .NET 5.0 preview SDK)</span></span>

  <span data-ttu-id="ca2b7-157">每个测试超时时间，在此时间后，将触发挂起转储，并转储和终止测试主机进程及其所有子进程。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-157">Per-test timeout, after which a hang dump is triggered and the test host process and all of its child processes are dumped and terminated.</span></span> <span data-ttu-id="ca2b7-158">超时值是采用以下格式之一指定的：</span><span class="sxs-lookup"><span data-stu-id="ca2b7-158">The timeout value is specified in one of the following formats:</span></span>
  
  - <span data-ttu-id="ca2b7-159">1.5h、1.5hour、1.5hours</span><span class="sxs-lookup"><span data-stu-id="ca2b7-159">1.5h, 1.5hour, 1.5hours</span></span>
  - <span data-ttu-id="ca2b7-160">90m、90min、90minute、90minutes</span><span class="sxs-lookup"><span data-stu-id="ca2b7-160">90m, 90min, 90minute, 90minutes</span></span>
  - <span data-ttu-id="ca2b7-161">5400s、5400sec、5400second、5400seconds</span><span class="sxs-lookup"><span data-stu-id="ca2b7-161">5400s, 5400sec, 5400second, 5400seconds</span></span>
  - <span data-ttu-id="ca2b7-162">5400000ms、5400000mil、5400000millisecond、5400000milliseconds</span><span class="sxs-lookup"><span data-stu-id="ca2b7-162">5400000ms, 5400000mil, 5400000millisecond, 5400000milliseconds</span></span>

  <span data-ttu-id="ca2b7-163">如果未使用单位（例如，5400000），则假定该值以毫秒为单位。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-163">When no unit is used (for example, 5400000), the value is assumed to be in milliseconds.</span></span> <span data-ttu-id="ca2b7-164">与数据驱动的测试一起使用时，超时行为取决于所使用的测试适配器。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-164">When used together with data driven tests, the timeout behavior depends on the test adapter used.</span></span> <span data-ttu-id="ca2b7-165">对于 xUnit 和 NUnit，会在每个测试用例后更新超时。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-165">For xUnit and NUnit the timeout is renewed after every test case.</span></span> <span data-ttu-id="ca2b7-166">对于 MSTest，超时用于所有测试用例。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-166">For MSTest, the timeout is used for all test cases.</span></span> <span data-ttu-id="ca2b7-167">此选项在使用 netcoreapp 2.1 和更高版本的 Windows 上，在使用 netcoreapp 3.1 和更高版本的 Linux 上以及在使用 net5.0 或更高版本的 macOS 上受支持。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-167">This option is supported on Windows with netcoreapp2.1 and later, on Linux with netcoreapp3.1 and later, and on macOS with net5.0 or later.</span></span> <span data-ttu-id="ca2b7-168">意味着 `--blame` 和 `--blame-hang`。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-168">Implies `--blame` and `--blame-hang`.</span></span>

- **`-c|--configuration <CONFIGURATION>`**

  <span data-ttu-id="ca2b7-169">定义生成配置。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-169">Defines the build configuration.</span></span> <span data-ttu-id="ca2b7-170">默认值为 `Debug`，但项目配置可以替代此默认 SDK 设置。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-170">The default value is `Debug`, but your project's configuration could override this default SDK setting.</span></span>

- **`--collect <DATA_COLLECTOR_NAME>`**

  <span data-ttu-id="ca2b7-171">为测试运行启用数据收集器。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-171">Enables data collector for the test run.</span></span> <span data-ttu-id="ca2b7-172">有关详细信息，请参阅[监视和分析测试运行](https://aka.ms/vstest-collect)。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-172">For more information, see [Monitor and analyze test run](https://aka.ms/vstest-collect).</span></span>
  
  <span data-ttu-id="ca2b7-173">若要在 .NET Core 支持的任何平台上收集代码覆盖率，请安装 [Coverlet](https://github.com/coverlet-coverage/coverlet/blob/master/README.md) 并使用 `--collect:"XPlat Code Coverage"` 选项。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-173">To collect code coverage on any platform that is supported by .NET Core, install [Coverlet](https://github.com/coverlet-coverage/coverlet/blob/master/README.md) and use the `--collect:"XPlat Code Coverage"` option.</span></span>

  <span data-ttu-id="ca2b7-174">在 Windows 上，可以使用 `--collect "Code Coverage"` 选项收集代码覆盖率。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-174">On Windows, you can collect code coverage by using the `--collect "Code Coverage"` option.</span></span> <span data-ttu-id="ca2b7-175">此选项将生成“.coverage”文件，该文件可在 Visual Studio 2019 Enterprise 中打开。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-175">This option generates a *.coverage* file, which can be opened in Visual Studio 2019 Enterprise.</span></span> <span data-ttu-id="ca2b7-176">有关详细信息，请参阅[使用代码覆盖率](/visualstudio/test/using-code-coverage-to-determine-how-much-code-is-being-tested)和[自定义代码覆盖率分析](/visualstudio/test/customizing-code-coverage-analysis)。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-176">For more information, see [Use code coverage](/visualstudio/test/using-code-coverage-to-determine-how-much-code-is-being-tested) and [Customize code coverage analysis](/visualstudio/test/customizing-code-coverage-analysis).</span></span>

- **`-d|--diag <LOG_FILE>`**

  <span data-ttu-id="ca2b7-177">启用测试平台的诊断模式，并将诊断消息写入到指定文件及其旁边的文件。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-177">Enables diagnostic mode for the test platform and writes diagnostic messages to the specified file and to files next to it.</span></span> <span data-ttu-id="ca2b7-178">正在记录消息的进程可确定创建了哪些文件，如测试主机日志的 `*.host_<date>.txt`，以及数据收集器日志的 `*.datacollector_<date>.txt`。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-178">The process that is logging the messages determines which files are created, such as `*.host_<date>.txt` for test host log, and `*.datacollector_<date>.txt` for data collector log.</span></span>

- **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="ca2b7-179">强制将 `dotnet` 或 .NET Framework 测试主机用于测试二进制文件。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-179">Forces the use of `dotnet` or .NET Framework test host for the test binaries.</span></span> <span data-ttu-id="ca2b7-180">此选项只确定要使用哪种类型的主机。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-180">This option only determines which type of host to use.</span></span> <span data-ttu-id="ca2b7-181">要使用的实际框架版本由测试项目的 runtimeconfig.json 决定。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-181">The actual framework version to be used is determined by the *runtimeconfig.json* of the test project.</span></span> <span data-ttu-id="ca2b7-182">如果未指定，则 [TargetFramework 程序集特性](/dotnet/api/system.runtime.versioning.targetframeworkattribute)用于确定主机的类型。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-182">When not specified, the [TargetFramework assembly attribute](/dotnet/api/system.runtime.versioning.targetframeworkattribute) is used to determine the type of host.</span></span> <span data-ttu-id="ca2b7-183">如果已从 .dll 中去除此特性，则使用的是 .NET Framework 主机。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-183">When that attribute is stripped from the *.dll*, the .NET Framework host is used.</span></span>

- **`--filter <EXPRESSION>`**

  <span data-ttu-id="ca2b7-184">使用给定表达式筛选掉当前项目中的测试。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-184">Filters out tests in the current project using the given expression.</span></span> <span data-ttu-id="ca2b7-185">有关详细信息，请参阅[筛选选项详细信息](#filter-option-details)部分。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-185">For more information, see the [Filter option details](#filter-option-details) section.</span></span> <span data-ttu-id="ca2b7-186">若要获取使用选择性单元测试筛选的其他信息和示例，请参阅[运行选择性单元测试](../testing/selective-unit-tests.md)。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-186">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

- **`-h|--help`**

  <span data-ttu-id="ca2b7-187">打印出有关命令的简短帮助。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-187">Prints out a short help for the command.</span></span>

- **`--interactive`**

  <span data-ttu-id="ca2b7-188">允许命令停止并等待用户输入或操作。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-188">Allows the command to stop and wait for user input or action.</span></span> <span data-ttu-id="ca2b7-189">例如，完成身份验证。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-189">For example, to complete authentication.</span></span> <span data-ttu-id="ca2b7-190">自 .NET Core 3.0 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-190">Available since .NET Core 3.0 SDK.</span></span>

- **`-l|--logger <LOGGER>`**

  <span data-ttu-id="ca2b7-191">指定测试结果记录器。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-191">Specifies a logger for test results.</span></span> <span data-ttu-id="ca2b7-192">与 MSBuild 不同，dotnet 测试不接受缩写，应使用 `-l "console;verbosity=detailed"`，而不使用 `-l "console;v=d"`。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-192">Unlike MSBuild, dotnet test doesn't accept abbreviations: instead of `-l "console;v=d"` use `-l "console;verbosity=detailed"`.</span></span> <span data-ttu-id="ca2b7-193">多次指定参数，以启用多个记录器。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-193">Specify the parameter multiple times to enable multiple loggers.</span></span>

- **`--no-build`**

  <span data-ttu-id="ca2b7-194">不在运行测试项目之前生成它。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-194">Doesn't build the test project before running it.</span></span> <span data-ttu-id="ca2b7-195">还将隐式设置 - `--no-restore` 标记。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-195">It also implicitly sets the - `--no-restore` flag.</span></span>

- **`--nologo`**

  <span data-ttu-id="ca2b7-196">运行测试，而不显示 Microsoft TestPlatform 横幅。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-196">Run tests without displaying the Microsoft TestPlatform banner.</span></span> <span data-ttu-id="ca2b7-197">自 .NET Core 3.0 SDK 起可用。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-197">Available since .NET Core 3.0 SDK.</span></span>

- **`--no-restore`**

  <span data-ttu-id="ca2b7-198">运行此命令时不执行隐式还原。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-198">Doesn't execute an implicit restore when running the command.</span></span>

- **`-o|--output <OUTPUT_DIRECTORY>`**

  <span data-ttu-id="ca2b7-199">查找要运行的二进制文件的目录。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-199">Directory in which to find the binaries to run.</span></span> <span data-ttu-id="ca2b7-200">如果未指定，则默认路径为 `./bin/<configuration>/<framework>/`。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-200">If not specified, the default path is `./bin/<configuration>/<framework>/`.</span></span>  <span data-ttu-id="ca2b7-201">对于具有多个目标框架的项目（通过 `TargetFrameworks` 属性），在指定此选项时还需要定义 `--framework`。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-201">For projects with multiple target frameworks (via the `TargetFrameworks` property), you also need to define `--framework` when you specify this option.</span></span> <span data-ttu-id="ca2b7-202">`dotnet test` 始终从输出目录运行测试。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-202">`dotnet test` always runs tests from the output directory.</span></span> <span data-ttu-id="ca2b7-203">可以使用 <xref:System.AppDomain.BaseDirectory%2A?displayProperty=nameWithType> 以使用输出目录中的测试资产。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-203">You can use <xref:System.AppDomain.BaseDirectory%2A?displayProperty=nameWithType> to consume test assets in the output directory.</span></span>

- **`-r|--results-directory <RESULTS_DIR>`**

  <span data-ttu-id="ca2b7-204">用于放置测试结果的目录。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-204">The directory where the test results are going to be placed.</span></span> <span data-ttu-id="ca2b7-205">如果指定的目录不存在，则会创建该目录。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-205">If the specified directory doesn't exist, it's created.</span></span> <span data-ttu-id="ca2b7-206">默认值为包含项目文件的目录中的 `TestResults`。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-206">The default is `TestResults` in the directory that contains the project file.</span></span>

- **`--runtime <RUNTIME_IDENTIFIER>`**

  <span data-ttu-id="ca2b7-207">要针对其测试的目标运行时。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-207">The target runtime to test for.</span></span>

- **`-s|--settings <SETTINGS_FILE>`**

  <span data-ttu-id="ca2b7-208">`.runsettings` 文件用于运行测试。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-208">The `.runsettings` file to use for running the tests.</span></span> <span data-ttu-id="ca2b7-209">`TargetPlatform` 元素 (x86|x64) 对 `dotnet test` 不起作用。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-209">The `TargetPlatform` element (x86|x64) has no effect for `dotnet test`.</span></span> <span data-ttu-id="ca2b7-210">若要运行面向 x86 的测试，请安装 .NET Core 的 x86 版本。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-210">To run tests that target x86, install the x86 version of .NET Core.</span></span> <span data-ttu-id="ca2b7-211">路径上 dotnet.exe 的位数是用于运行测试的内容。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-211">The bitness of the *dotnet.exe* that is on the path is what will be used for running tests.</span></span> <span data-ttu-id="ca2b7-212">有关更多信息，请参见以下资源：</span><span class="sxs-lookup"><span data-stu-id="ca2b7-212">For more information, see the following resources:</span></span>

  - [<span data-ttu-id="ca2b7-213">使用 `.runsettings` 文件配置单元测试。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-213">Configure unit tests by using a `.runsettings` file.</span></span>](/visualstudio/test/configure-unit-tests-by-using-a-dot-runsettings-file)
  - [<span data-ttu-id="ca2b7-214">配置测试运行</span><span class="sxs-lookup"><span data-stu-id="ca2b7-214">Configure a test run</span></span>](https://github.com/Microsoft/vstest-docs/blob/master/docs/configure.md)

- **`-t|--list-tests`**

  <span data-ttu-id="ca2b7-215">列出已发现的测试，而不是运行测试。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-215">List the discovered tests instead of running the tests.</span></span>

- **`-v|--verbosity <LEVEL>`**

  <span data-ttu-id="ca2b7-216">设置命令的详细级别。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-216">Sets the verbosity level of the command.</span></span> <span data-ttu-id="ca2b7-217">允许使用的值为 `q[uiet]`、`m[inimal]`、`n[ormal]`、`d[etailed]` 和 `diag[nostic]`。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-217">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="ca2b7-218">默认值为 `minimal`。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-218">The default is `minimal`.</span></span> <span data-ttu-id="ca2b7-219">有关详细信息，请参阅 <xref:Microsoft.Build.Framework.LoggerVerbosity>。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-219">For more information, see <xref:Microsoft.Build.Framework.LoggerVerbosity>.</span></span>

- <span data-ttu-id="ca2b7-220">`RunSettings` 参数</span><span class="sxs-lookup"><span data-stu-id="ca2b7-220">**`RunSettings`** arguments</span></span>

 <span data-ttu-id="ca2b7-221">内联的 `RunSettings` 作为“-- ”（请注意 -- 后面有空格）后的最后一个命令行参数传递。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-221">Inline `RunSettings` are passed as the last arguments on the command line after "-- " (note the space after --).</span></span> <span data-ttu-id="ca2b7-222">内联的 `RunSettings` 被指定为 `[name]=[value]` 对。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-222">Inline `RunSettings` are specified as `[name]=[value]` pairs.</span></span> <span data-ttu-id="ca2b7-223">空格用于分隔多个 `[name]=[value]` 对。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-223">A space is used to separate multiple `[name]=[value]` pairs.</span></span>

  <span data-ttu-id="ca2b7-224">示例：`dotnet test -- MSTest.DeploymentEnabled=false MSTest.MapInconclusiveToFailed=True`</span><span class="sxs-lookup"><span data-stu-id="ca2b7-224">Example: `dotnet test -- MSTest.DeploymentEnabled=false MSTest.MapInconclusiveToFailed=True`</span></span>

  <span data-ttu-id="ca2b7-225">有关详细信息，请参阅[通过命令行传递 RunSettings 参数](https://github.com/Microsoft/vstest-docs/blob/master/docs/RunSettingsArguments.md)。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-225">For more information, see [Passing RunSettings arguments through command line](https://github.com/Microsoft/vstest-docs/blob/master/docs/RunSettingsArguments.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ca2b7-226">示例</span><span class="sxs-lookup"><span data-stu-id="ca2b7-226">Examples</span></span>

- <span data-ttu-id="ca2b7-227">运行当前目录所含项目中的测试：</span><span class="sxs-lookup"><span data-stu-id="ca2b7-227">Run the tests in the project in the current directory:</span></span>

  ```dotnetcli
  dotnet test
  ```

- <span data-ttu-id="ca2b7-228">运行 `test1` 项目中的测试：</span><span class="sxs-lookup"><span data-stu-id="ca2b7-228">Run the tests in the `test1` project:</span></span>

  ```dotnetcli
  dotnet test ~/projects/test1/test1.csproj
  ```

- <span data-ttu-id="ca2b7-229">在当前目录运行项目中的测试，并以 trx 格式生成测试结果文件：</span><span class="sxs-lookup"><span data-stu-id="ca2b7-229">Run the tests in the project in the current directory, and generate a test results file in the trx format:</span></span>

  ```dotnetcli
  dotnet test --logger trx
  ```

- <span data-ttu-id="ca2b7-230">在当前目录运行项目中的测试，并生成代码覆盖率文件（安装 [Coverlet](https://github.com/coverlet-coverage/coverlet/blob/master/Documentation/VSTestIntegration.md) 收集器集成后）：</span><span class="sxs-lookup"><span data-stu-id="ca2b7-230">Run the tests in the project in the current directory, and generate a code coverage file (after installing [Coverlet](https://github.com/coverlet-coverage/coverlet/blob/master/Documentation/VSTestIntegration.md) collectors integration):</span></span>

  ```dotnetcli
  dotnet test --collect:"XPlat Code Coverage"
  ```

- <span data-ttu-id="ca2b7-231">在当前目录运行项目中的测试，并生成代码覆盖率文件（仅限 Windows）：</span><span class="sxs-lookup"><span data-stu-id="ca2b7-231">Run the tests in the project in the current directory, and generate a code coverage file (Windows only):</span></span>

  ```dotnetcli
  dotnet test --collect "Code Coverage"
  ```

- <span data-ttu-id="ca2b7-232">在当前目录中运行项目中的测试，并将详细的测试结果记录到控制台：</span><span class="sxs-lookup"><span data-stu-id="ca2b7-232">Run the tests in the project in the current directory, and log with detailed verbosity to the console:</span></span>

  ```dotnetcli
  dotnet test --logger "console;verbosity=detailed"
  ```

- <span data-ttu-id="ca2b7-233">在当前目录下的项目中运行测试，并报告在测试主机发生故障时正在进行的测试：</span><span class="sxs-lookup"><span data-stu-id="ca2b7-233">Run the tests in the project in the current directory, and report tests that were in progress when the test host crashed:</span></span>

  ```dotnetcli
  dotnet test --blame
  ```

## <a name="filter-option-details"></a><span data-ttu-id="ca2b7-234">筛选选项详细信息</span><span class="sxs-lookup"><span data-stu-id="ca2b7-234">Filter option details</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="ca2b7-235">`<Expression>` 格式为 `<property><operator><value>[|&<Expression>]`。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-235">`<Expression>` has the format `<property><operator><value>[|&<Expression>]`.</span></span>

<span data-ttu-id="ca2b7-236">`<property>` 是 `Test Case` 的特性。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-236">`<property>` is an attribute of the `Test Case`.</span></span> <span data-ttu-id="ca2b7-237">下面介绍了常用单元测试框架支持的属性：</span><span class="sxs-lookup"><span data-stu-id="ca2b7-237">The following are the properties supported by popular unit test frameworks:</span></span>

| <span data-ttu-id="ca2b7-238">测试框架</span><span class="sxs-lookup"><span data-stu-id="ca2b7-238">Test Framework</span></span> | <span data-ttu-id="ca2b7-239">支持的属性</span><span class="sxs-lookup"><span data-stu-id="ca2b7-239">Supported properties</span></span>                                                                                      |
| -------------- | --------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="ca2b7-240">MSTest</span><span class="sxs-lookup"><span data-stu-id="ca2b7-240">MSTest</span></span>         | <ul><li><span data-ttu-id="ca2b7-241">FullyQualifiedName</span><span class="sxs-lookup"><span data-stu-id="ca2b7-241">FullyQualifiedName</span></span></li><li><span data-ttu-id="ca2b7-242">“属性”</span><span class="sxs-lookup"><span data-stu-id="ca2b7-242">Name</span></span></li><li><span data-ttu-id="ca2b7-243">ClassName</span><span class="sxs-lookup"><span data-stu-id="ca2b7-243">ClassName</span></span></li><li><span data-ttu-id="ca2b7-244">Priority</span><span class="sxs-lookup"><span data-stu-id="ca2b7-244">Priority</span></span></li><li><span data-ttu-id="ca2b7-245">TestCategory</span><span class="sxs-lookup"><span data-stu-id="ca2b7-245">TestCategory</span></span></li></ul> |
| <span data-ttu-id="ca2b7-246">xUnit</span><span class="sxs-lookup"><span data-stu-id="ca2b7-246">xUnit</span></span>          | <ul><li><span data-ttu-id="ca2b7-247">FullyQualifiedName</span><span class="sxs-lookup"><span data-stu-id="ca2b7-247">FullyQualifiedName</span></span></li><li><span data-ttu-id="ca2b7-248">DisplayName</span><span class="sxs-lookup"><span data-stu-id="ca2b7-248">DisplayName</span></span></li><li><span data-ttu-id="ca2b7-249">Traits</span><span class="sxs-lookup"><span data-stu-id="ca2b7-249">Traits</span></span></li></ul>                                   |
| <span data-ttu-id="ca2b7-250">NUnit</span><span class="sxs-lookup"><span data-stu-id="ca2b7-250">NUnit</span></span>          | <ul><li><span data-ttu-id="ca2b7-251">FullyQualifiedName</span><span class="sxs-lookup"><span data-stu-id="ca2b7-251">FullyQualifiedName</span></span></li><li><span data-ttu-id="ca2b7-252">“属性”</span><span class="sxs-lookup"><span data-stu-id="ca2b7-252">Name</span></span></li><li><span data-ttu-id="ca2b7-253">TestCategory</span><span class="sxs-lookup"><span data-stu-id="ca2b7-253">TestCategory</span></span></li><li><span data-ttu-id="ca2b7-254">Priority</span><span class="sxs-lookup"><span data-stu-id="ca2b7-254">Priority</span></span></li></ul>                                   |

<span data-ttu-id="ca2b7-255">`<operator>` 说明了属性和值之间的关系：</span><span class="sxs-lookup"><span data-stu-id="ca2b7-255">The `<operator>` describes the relationship between the property and the value:</span></span>

| <span data-ttu-id="ca2b7-256">运算符</span><span class="sxs-lookup"><span data-stu-id="ca2b7-256">Operator</span></span> | <span data-ttu-id="ca2b7-257">函数</span><span class="sxs-lookup"><span data-stu-id="ca2b7-257">Function</span></span>        |
| :------: | --------------- |
| `=`      | <span data-ttu-id="ca2b7-258">完全匹配</span><span class="sxs-lookup"><span data-stu-id="ca2b7-258">Exact match</span></span>     |
| `!=`     | <span data-ttu-id="ca2b7-259">非完全匹配</span><span class="sxs-lookup"><span data-stu-id="ca2b7-259">Not exact match</span></span> |
| `~`      | <span data-ttu-id="ca2b7-260">包含</span><span class="sxs-lookup"><span data-stu-id="ca2b7-260">Contains</span></span>        |
| `!~`     | <span data-ttu-id="ca2b7-261">不包含</span><span class="sxs-lookup"><span data-stu-id="ca2b7-261">Not contains</span></span>    |

<span data-ttu-id="ca2b7-262">`<value>` 是字符串。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-262">`<value>` is a string.</span></span> <span data-ttu-id="ca2b7-263">所有查找都不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-263">All the lookups are case insensitive.</span></span>

<span data-ttu-id="ca2b7-264">不含 `<operator>` 的表达式自动被视为 `FullyQualifiedName` 属性上的 `contains`（例如，`dotnet test --filter xyz` 与 `dotnet test --filter FullyQualifiedName~xyz` 相同）。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-264">An expression without an `<operator>` is automatically considered as a `contains` on `FullyQualifiedName` property (for example, `dotnet test --filter xyz` is same as `dotnet test --filter FullyQualifiedName~xyz`).</span></span>

<span data-ttu-id="ca2b7-265">表达式可与条件运算符结合使用：</span><span class="sxs-lookup"><span data-stu-id="ca2b7-265">Expressions can be joined with conditional operators:</span></span>

| <span data-ttu-id="ca2b7-266">运算符</span><span class="sxs-lookup"><span data-stu-id="ca2b7-266">Operator</span></span>            | <span data-ttu-id="ca2b7-267">函数</span><span class="sxs-lookup"><span data-stu-id="ca2b7-267">Function</span></span> |
| ------------------- | -------- |
| <code>&#124;</code> | <span data-ttu-id="ca2b7-268">或</span><span class="sxs-lookup"><span data-stu-id="ca2b7-268">OR</span></span>       |
| `&`                 | <span data-ttu-id="ca2b7-269">AND</span><span class="sxs-lookup"><span data-stu-id="ca2b7-269">AND</span></span>      |

<span data-ttu-id="ca2b7-270">使用条件运算符时，可以用括号将表达式括起来（例如，`(Name~TestMethod1) | (Name~TestMethod2)`）。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-270">You can enclose expressions in parenthesis when using conditional operators (for example, `(Name~TestMethod1) | (Name~TestMethod2)`).</span></span>

<span data-ttu-id="ca2b7-271">若要获取使用选择性单元测试筛选的其他信息和示例，请参阅[运行选择性单元测试](../testing/selective-unit-tests.md)。</span><span class="sxs-lookup"><span data-stu-id="ca2b7-271">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ca2b7-272">请参阅</span><span class="sxs-lookup"><span data-stu-id="ca2b7-272">See also</span></span>

- [<span data-ttu-id="ca2b7-273">框架和目标</span><span class="sxs-lookup"><span data-stu-id="ca2b7-273">Frameworks and Targets</span></span>](../../standard/frameworks.md)
- [<span data-ttu-id="ca2b7-274">.NET 运行时标识符 (RID) 目录</span><span class="sxs-lookup"><span data-stu-id="ca2b7-274">.NET Runtime Identifier (RID) catalog</span></span>](../rid-catalog.md)
- [<span data-ttu-id="ca2b7-275">通过命令行传递 runsettings 参数</span><span class="sxs-lookup"><span data-stu-id="ca2b7-275">Passing runsettings arguments through commandline</span></span>](https://github.com/Microsoft/vstest-docs/blob/master/docs/RunSettingsArguments.md)
