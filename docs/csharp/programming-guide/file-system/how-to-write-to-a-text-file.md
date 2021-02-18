---
title: 如何写入文本文件 - C# 编程指南
description: 了解如何使用 C# 编写文本文件。 查看一些代码示例和其他可用资源。
ms.date: 02/11/2021
f1_keywords:
- TextWriter.WriteLine
- StreamWriter.Close
helpviewer_keywords:
- files [C#], text files
- text, writing to files [C#]
ms.assetid: 2e99f184-d88b-4719-a7f1-d9ec482aa809
ms.topic: how-to
ms.custom: contperf-fy21q3
ms.openlocfilehash: ecc3ba73161d4f4571bbc6ae0c9aaa3337586ef7
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100475612"
---
# <a name="how-to-write-to-a-text-file-c-programming-guide"></a>如何写入文本文件（C# 编程指南）

本文提供了几个示例，演示了将文本写入文件的多种方法。 前两个示例使用 <xref:System.IO.File?displayProperty=nameWithType> 类上的静态便捷方法将任意 `IEnumerable<string>` 的每个元素和 `string` 写入文本文件。 第三个示例演示了在写入文件时必须分别处理文本的每一行的情况下，如何将文本添加到文件。 在前三个示例中，会覆盖文件中的所有现有内容。 最后一个示例演示如何将文本追加到现有文件。

 这些示例都将字符串文本写入了文件。 如果想设置写入文件的文本的格式，请使用 <xref:System.String.Format%2A> 方法或 C# [字符串内插](../../language-reference/tokens/interpolated.md)功能。

## <a name="write-a-collection-of-strings-to-a-file"></a>将字符串的集合写入文件

:::code language="csharp" source="snippets/write-text/WriteAllLines.cs":::

前面的源代码示例：

- 使用三个值实例化字符串数组。
- 等待对 <xref:System.IO.File.WriteAllLinesAsync%2A?displayProperty=nameWithType> 的调用完成，该调用会执行以下操作：

  - 以异步方式创建一个名为“WriteLines.txt”的文件。 如果该文件已存在，则会覆盖该文件。
  - 将给定行写入该文件。
  - 关闭该文件，并根据需要自动刷新和释放。

## <a name="write-one-string-to-a-file"></a>向文件写入一个字符串

:::code language="csharp" source="snippets/write-text/WriteAllText.cs":::

前面的源代码示例：

- 根据指定的字符串字面量实例化一个字符串。
- 等待对 <xref:System.IO.File.WriteAllTextAsync%2A?displayProperty=nameWithType> 的调用完成，该调用会执行以下操作：

  - 以异步方式创建一个名为“WriteText.txt”的文件。 如果该文件已存在，则会覆盖该文件。
  - 将给定文本写入该文件。
  - 关闭该文件，并根据需要自动刷新和释放。

## <a name="write-selected-strings-from-an-array-to-a-file"></a>将数组中的选定字符串写入文件

:::code language="csharp" source="snippets/write-text/StreamWriterOne.cs":::

前面的源代码示例：

- 使用三个值实例化字符串数组。
- 以 [using 声明](../../whats-new/csharp-8.md#using-declarations)的形式使用 WriteLines2.txt 的文件路径实例化 <xref:System.IO.StreamWriter>。
- 循环访问所有行。
- 有条件地等待对 <xref:System.IO.StreamWriter.WriteLineAsync(System.String)?displayProperty=nameWithType> 的调用完成，该调用在行不包含 `"Second"` 时将该行写入文件。

## <a name="append-text-to-an-existing-file"></a>将文本追加到现有文件

:::code language="csharp" source="snippets/write-text/StreamWriterTwo.cs":::

前面的源代码示例：

- 使用三个值实例化字符串数组。
- 以 [using 声明](../../whats-new/csharp-8.md#using-declarations)的形式使用 WriteLines2.txt 的文件路径实例化 <xref:System.IO.StreamWriter>，并传入要追加的 `true`。
- 等待对 <xref:System.IO.StreamWriter.WriteLineAsync(System.String)?displayProperty=nameWithType> 的调用完成，该调用将字符串作为追加行写入文件。

## <a name="exceptions"></a>异常

以下情况可能会导致异常：

- <xref:System.InvalidOperationException>：文件已存在并且为只读。
- <xref:System.IO.PathTooLongException>：路径名可能太长。
- <xref:System.IO.IOException>：磁盘可能已满。

使用文件系统时，还有其他可能会导致异常的情况，因此最好进行防御性编程。

## <a name="see-also"></a>请参阅

- [C# 编程指南](../index.md)
- [文件系统和注册表（C# 编程指南）](./index.md)
- [示例：将集合保存到应用程序存储](https://code.msdn.microsoft.com/CSWinStoreAppSaveCollection-bed5d6e6)
