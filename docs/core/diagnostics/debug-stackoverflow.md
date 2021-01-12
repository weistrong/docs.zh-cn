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
# <a name="debugging-stackoverflow-errors"></a>调试 StackOverflow 错误

当执行堆栈溢出时，将引发 <xref:System.StackOverflowException>，因为它包含太多的嵌套方法调用。  

例如，假设你有一款应用，如下所示：

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

Main 方法将持续调用自身，直到没有更多堆栈空间为止。  没有更多堆栈空间后，执行将无法继续，于是将引发 <xref:System.StackOverflowException>。  

````
> dotnet run
Stack overflow.
````

> [!NOTE]
> 在 .NET 5 及更高版本上，调用栈将输出到控制台。

> [!NOTE]
> 本文介绍如何使用 lldb 调试堆栈溢出。 如果在 Windows 上运行，建议使用 [Visual Studio](/visualstudio/debugger/what-is-debugging) 或 [Visual Studio Code](https://code.visualstudio.com/Docs/editor/debugging) 调试应用。  

## <a name="example"></a>示例

1. 运行配置为在发生故障时收集转储的应用

    ````
    > export COMPlus_DbgEnableMiniDump=1
    > dotnet run
    Stack overflow.
    Writing minidump with heap to file /tmp/coredump.6412
    Written 58191872 bytes (14207 pages) to core file
    ````

2. 使用 [dotnet-sos](dotnet-sos.md) 安装 SOS 扩展

    ````
    dotnet-sos install
    ````

3. 在 lldb 中调试转储以查看失败的堆栈

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

4. 顶部框架 `0x00007f59b40900cc` 重复了几次。 使用 [SOS](sos-debugging-extension.md) `ip2md` 命令找出 `0x00007f59b40900cc` 地址处的方法

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

5. 查看指定方法 temp.Program.Main(System.String[]) 和源代码“/temp/Program.cs @ 9”，了解能否找出错误。 如果仍不清楚，则可以在该代码区域中添加日志记录。

## <a name="see-also"></a>另请参阅

* [.NET 中的转储简介](dumps.md)
* [调试 Linux 转储](debug-linux-dumps.md)
* [适用于 .NET 的 SOS 调试扩展](sos-debugging-extension.md)
