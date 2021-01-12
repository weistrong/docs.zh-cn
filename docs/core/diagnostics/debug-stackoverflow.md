---
title: 调试 StackOverflow 错误
description: 了解如何诊断 StackOverflow 异常
ms.topic: tutorial
ms.date: 12/22/2020
ms.openlocfilehash: 92edf854ddcc2e778949d74eff1370cf27db25b4
ms.sourcegitcommit: c0b803bffaf101e12f071faf94ca21b46d04ff30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/24/2020
ms.locfileid: "97764924"
---
# <a name="debugging-stackoverflow-errors"></a><span data-ttu-id="7e8e1-103">调试 StackOverflow 错误</span><span class="sxs-lookup"><span data-stu-id="7e8e1-103">Debugging StackOverflow errors</span></span>

<span data-ttu-id="7e8e1-104">当执行堆栈溢出时，将引发 <xref:System.StackOverflowException>，因为它包含太多的嵌套方法调用。</span><span class="sxs-lookup"><span data-stu-id="7e8e1-104">A <xref:System.StackOverflowException> is thrown when when the execution stack overflows because it contains too many nested method calls.</span></span>  

<span data-ttu-id="7e8e1-105">例如，假设你有一款应用，如下所示：</span><span class="sxs-lookup"><span data-stu-id="7e8e1-105">For example, suppose you have an app as follows:</span></span>

````
using System;

namespace temp
{
    class Program
    {
        static void Main(string[] args)
        {
            Main(args); // oops this recursion won't stop
        }
    }
}
````

<span data-ttu-id="7e8e1-106">Main 方法将持续调用自身，直到没有更多堆栈空间为止。</span><span class="sxs-lookup"><span data-stu-id="7e8e1-106">The Main method will continuously call itself until there is no more stack space.</span></span>  <span data-ttu-id="7e8e1-107">没有更多堆栈空间后，执行将无法继续，于是将引发 <xref:System.StackOverflowException>。</span><span class="sxs-lookup"><span data-stu-id="7e8e1-107">Once there is no more stack space, execution cannot continue and so it will throw a <xref:System.StackOverflowException>.</span></span>  

````
> dotnet run
Stack overflow.
````

> [!NOTE]
> <span data-ttu-id="7e8e1-108">在 .NET 5 及更高版本上，调用栈将输出到控制台。</span><span class="sxs-lookup"><span data-stu-id="7e8e1-108">On .NET 5 and later, the callstack is output to the console.</span></span>

> [!NOTE]
> <span data-ttu-id="7e8e1-109">本文介绍如何使用 lldb 调试堆栈溢出。</span><span class="sxs-lookup"><span data-stu-id="7e8e1-109">This article describes how to debug a stack overflow with lldb.</span></span> <span data-ttu-id="7e8e1-110">如果在 Windows 上运行，建议使用 [Visual Studio](/visualstudio/debugger/what-is-debugging) 或 [Visual Studio Code](https://code.visualstudio.com/Docs/editor/debugging) 调试应用。</span><span class="sxs-lookup"><span data-stu-id="7e8e1-110">If you are running on Windows, we suggest debugging the app with [Visual Studio](/visualstudio/debugger/what-is-debugging) or [Visual Studio Code](https://code.visualstudio.com/Docs/editor/debugging).</span></span>  

## <a name="example"></a><span data-ttu-id="7e8e1-111">示例</span><span class="sxs-lookup"><span data-stu-id="7e8e1-111">Example</span></span>

1. <span data-ttu-id="7e8e1-112">运行配置为在发生故障时收集转储的应用</span><span class="sxs-lookup"><span data-stu-id="7e8e1-112">Run the app with it configured to collect a dump on crash</span></span>

    ````
    > export COMPlus_DbgEnableMiniDump=1
    > dotnet run
    Stack overflow.
    Writing minidump with heap to file /tmp/coredump.6412
    Written 58191872 bytes (14207 pages) to core file
    ````

2. <span data-ttu-id="7e8e1-113">使用 [dotnet-sos](dotnet-sos.md) 安装 SOS 扩展</span><span class="sxs-lookup"><span data-stu-id="7e8e1-113">Install the SOS extension using [dotnet-sos](dotnet-sos.md)</span></span>

    ````
    dotnet-sos install
    ````

3. <span data-ttu-id="7e8e1-114">在 lldb 中调试转储以查看失败的堆栈</span><span class="sxs-lookup"><span data-stu-id="7e8e1-114">Debug the dump in lldb to see the failing stack</span></span>

    ````
    lldb --core /temp/coredump.6412
    (lldb) bt
    ...
        frame #261930: 0x00007f59b40900cc
        frame #261931: 0x00007f59b40900cc
        frame #261932: 0x00007f59b40900cc
        frame #261933: 0x00007f59b40900cc
        frame #261934: 0x00007f59b40900cc
        frame #261935: 0x00007f5a2d4a080f libcoreclr.so`CallDescrWorkerInternal at unixasmmacrosamd64.inc:867
        frame #261936: 0x00007f5a2d3cc4c3 libcoreclr.so`MethodDescCallSite::CallTargetWorker(unsigned long const*, unsigned long*, int) at callhelpers.cpp:70
        frame #261937: 0x00007f5a2d3cc468 libcoreclr.so`MethodDescCallSite::CallTargetWorker(this=<unavailable>, pArguments=0x00007ffe8222e7b0, pReturnValue=0x0000000000000000, cbReturnValue=0) at callhelpers.cpp:604
        frame #261938: 0x00007f5a2d4b6182 libcoreclr.so`RunMain(MethodDesc*, short, int*, PtrArray**) [inlined] MethodDescCallSite::Call(this=<unavailable>, pArguments=<unavailable>) at callhelpers.h:468
    ...
    ````

4. <span data-ttu-id="7e8e1-115">顶部框架 `0x00007f59b40900cc` 重复了几次。</span><span class="sxs-lookup"><span data-stu-id="7e8e1-115">The top frame `0x00007f59b40900cc` is repeated several times.</span></span> <span data-ttu-id="7e8e1-116">使用 [SOS](sos-debugging-extension.md) `ip2md` 命令找出 `0x00007f59b40900cc` 地址处的方法</span><span class="sxs-lookup"><span data-stu-id="7e8e1-116">Use the [SOS](sos-debugging-extension.md) `ip2md` command to figure out what method is located at the `0x00007f59b40900cc` address</span></span>

    ````
    (lldb) ip2md 0x00007f59b40900cc
    MethodDesc:   00007f59b413ffa8
    Method Name:          temp.Program.Main(System.String[])
    Class:                00007f59b4181d40
    MethodTable:          00007f59b4190020
    mdToken:              0000000006000001
    Module:               00007f59b413dbf8
    IsJitted:             yes
    Current CodeAddr:     00007f59b40900a0
    Version History:
      ILCodeVersion:      0000000000000000
      ReJIT ID:           0
      IL Addr:            0000000000000000
         CodeAddr:           00007f59b40900a0  (MinOptJitted)
         NativeCodeVersion:  0000000000000000
    Source file:  /temp/Program.cs @ 9
    ````

5. <span data-ttu-id="7e8e1-117">查看指定方法 temp.Program.Main(System.String[]) 和源代码“/temp/Program.cs @ 9”，了解能否找出错误。</span><span class="sxs-lookup"><span data-stu-id="7e8e1-117">Go look at the indicated method temp.Program.Main(System.String[]) and source "/temp/Program.cs @ 9" to see if you can figure out what you did wrong.</span></span> <span data-ttu-id="7e8e1-118">如果仍不清楚，则可以在该代码区域中添加日志记录。</span><span class="sxs-lookup"><span data-stu-id="7e8e1-118">If it still wasn't clear you could add logging in that area of the code.</span></span>

## <a name="see-also"></a><span data-ttu-id="7e8e1-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7e8e1-119">See Also</span></span>

* [<span data-ttu-id="7e8e1-120">.NET 中的转储简介</span><span class="sxs-lookup"><span data-stu-id="7e8e1-120">An introduction to dumps in .NET</span></span>](dumps.md)
* [<span data-ttu-id="7e8e1-121">调试 Linux 转储</span><span class="sxs-lookup"><span data-stu-id="7e8e1-121">Debug Linux dumps</span></span>](debug-linux-dumps.md)
* [<span data-ttu-id="7e8e1-122">适用于 .NET 的 SOS 调试扩展</span><span class="sxs-lookup"><span data-stu-id="7e8e1-122">SOS Debugging Extension for .NET</span></span>](sos-debugging-extension.md)
