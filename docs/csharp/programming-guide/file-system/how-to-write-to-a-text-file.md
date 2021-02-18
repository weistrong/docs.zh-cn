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
# <a name="how-to-write-to-a-text-file-c-programming-guide"></a><span data-ttu-id="53fe0-104">如何写入文本文件（C# 编程指南）</span><span class="sxs-lookup"><span data-stu-id="53fe0-104">How to write to a text file (C# Programming Guide)</span></span>

<span data-ttu-id="53fe0-105">本文提供了几个示例，演示了将文本写入文件的多种方法。</span><span class="sxs-lookup"><span data-stu-id="53fe0-105">In this article, there are several examples showing various ways to write text to a file.</span></span> <span data-ttu-id="53fe0-106">前两个示例使用 <xref:System.IO.File?displayProperty=nameWithType> 类上的静态便捷方法将任意 `IEnumerable<string>` 的每个元素和 `string` 写入文本文件。</span><span class="sxs-lookup"><span data-stu-id="53fe0-106">The first two examples use static convenience methods on the <xref:System.IO.File?displayProperty=nameWithType> class to write each element of any `IEnumerable<string>` and a `string` to a text file.</span></span> <span data-ttu-id="53fe0-107">第三个示例演示了在写入文件时必须分别处理文本的每一行的情况下，如何将文本添加到文件。</span><span class="sxs-lookup"><span data-stu-id="53fe0-107">The third example shows how to add text to a file when you have to process each line individually as you write to the file.</span></span> <span data-ttu-id="53fe0-108">在前三个示例中，会覆盖文件中的所有现有内容。</span><span class="sxs-lookup"><span data-stu-id="53fe0-108">In the first three examples, you overwrite all existing content in the file.</span></span> <span data-ttu-id="53fe0-109">最后一个示例演示如何将文本追加到现有文件。</span><span class="sxs-lookup"><span data-stu-id="53fe0-109">The final example shows how to append text to an existing file.</span></span>

 <span data-ttu-id="53fe0-110">这些示例都将字符串文本写入了文件。</span><span class="sxs-lookup"><span data-stu-id="53fe0-110">These examples all write string literals to files.</span></span> <span data-ttu-id="53fe0-111">如果想设置写入文件的文本的格式，请使用 <xref:System.String.Format%2A> 方法或 C# [字符串内插](../../language-reference/tokens/interpolated.md)功能。</span><span class="sxs-lookup"><span data-stu-id="53fe0-111">If you want to format text written to a file, use the <xref:System.String.Format%2A> method or C# [string interpolation](../../language-reference/tokens/interpolated.md) feature.</span></span>

## <a name="write-a-collection-of-strings-to-a-file"></a><span data-ttu-id="53fe0-112">将字符串的集合写入文件</span><span class="sxs-lookup"><span data-stu-id="53fe0-112">Write a collection of strings to a file</span></span>

:::code language="csharp" source="snippets/write-text/WriteAllLines.cs":::

<span data-ttu-id="53fe0-113">前面的源代码示例：</span><span class="sxs-lookup"><span data-stu-id="53fe0-113">The preceding source code example:</span></span>

- <span data-ttu-id="53fe0-114">使用三个值实例化字符串数组。</span><span class="sxs-lookup"><span data-stu-id="53fe0-114">Instantiates a string array with three values.</span></span>
- <span data-ttu-id="53fe0-115">等待对 <xref:System.IO.File.WriteAllLinesAsync%2A?displayProperty=nameWithType> 的调用完成，该调用会执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="53fe0-115">Awaits a call to <xref:System.IO.File.WriteAllLinesAsync%2A?displayProperty=nameWithType> which:</span></span>

  - <span data-ttu-id="53fe0-116">以异步方式创建一个名为“WriteLines.txt”的文件。</span><span class="sxs-lookup"><span data-stu-id="53fe0-116">Asynchronously creates a file name *WriteLines.txt*.</span></span> <span data-ttu-id="53fe0-117">如果该文件已存在，则会覆盖该文件。</span><span class="sxs-lookup"><span data-stu-id="53fe0-117">If the file already exists, it is overwritten.</span></span>
  - <span data-ttu-id="53fe0-118">将给定行写入该文件。</span><span class="sxs-lookup"><span data-stu-id="53fe0-118">Writes the given lines to the file.</span></span>
  - <span data-ttu-id="53fe0-119">关闭该文件，并根据需要自动刷新和释放。</span><span class="sxs-lookup"><span data-stu-id="53fe0-119">Closes the file, automatically flushing and disposing as needed.</span></span>

## <a name="write-one-string-to-a-file"></a><span data-ttu-id="53fe0-120">向文件写入一个字符串</span><span class="sxs-lookup"><span data-stu-id="53fe0-120">Write one string to a file</span></span>

:::code language="csharp" source="snippets/write-text/WriteAllText.cs":::

<span data-ttu-id="53fe0-121">前面的源代码示例：</span><span class="sxs-lookup"><span data-stu-id="53fe0-121">The preceding source code example:</span></span>

- <span data-ttu-id="53fe0-122">根据指定的字符串字面量实例化一个字符串。</span><span class="sxs-lookup"><span data-stu-id="53fe0-122">Instantiates a string given the assigned string literal.</span></span>
- <span data-ttu-id="53fe0-123">等待对 <xref:System.IO.File.WriteAllTextAsync%2A?displayProperty=nameWithType> 的调用完成，该调用会执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="53fe0-123">Awaits a call to <xref:System.IO.File.WriteAllTextAsync%2A?displayProperty=nameWithType> which:</span></span>

  - <span data-ttu-id="53fe0-124">以异步方式创建一个名为“WriteText.txt”的文件。</span><span class="sxs-lookup"><span data-stu-id="53fe0-124">Asynchronously creates a file name *WriteText.txt*.</span></span> <span data-ttu-id="53fe0-125">如果该文件已存在，则会覆盖该文件。</span><span class="sxs-lookup"><span data-stu-id="53fe0-125">If the file already exists, it is overwritten.</span></span>
  - <span data-ttu-id="53fe0-126">将给定文本写入该文件。</span><span class="sxs-lookup"><span data-stu-id="53fe0-126">Writes the given text to the file.</span></span>
  - <span data-ttu-id="53fe0-127">关闭该文件，并根据需要自动刷新和释放。</span><span class="sxs-lookup"><span data-stu-id="53fe0-127">Closes the file, automatically flushing and disposing as needed.</span></span>

## <a name="write-selected-strings-from-an-array-to-a-file"></a><span data-ttu-id="53fe0-128">将数组中的选定字符串写入文件</span><span class="sxs-lookup"><span data-stu-id="53fe0-128">Write selected strings from an array to a file</span></span>

:::code language="csharp" source="snippets/write-text/StreamWriterOne.cs":::

<span data-ttu-id="53fe0-129">前面的源代码示例：</span><span class="sxs-lookup"><span data-stu-id="53fe0-129">The preceding source code example:</span></span>

- <span data-ttu-id="53fe0-130">使用三个值实例化字符串数组。</span><span class="sxs-lookup"><span data-stu-id="53fe0-130">Instantiates a string array with three values.</span></span>
- <span data-ttu-id="53fe0-131">以 [using 声明](../../whats-new/csharp-8.md#using-declarations)的形式使用 WriteLines2.txt 的文件路径实例化 <xref:System.IO.StreamWriter>。</span><span class="sxs-lookup"><span data-stu-id="53fe0-131">Instantiates a <xref:System.IO.StreamWriter> with a file path of *WriteLines2.txt* as a [using declaration](../../whats-new/csharp-8.md#using-declarations).</span></span>
- <span data-ttu-id="53fe0-132">循环访问所有行。</span><span class="sxs-lookup"><span data-stu-id="53fe0-132">Iterates through all the lines.</span></span>
- <span data-ttu-id="53fe0-133">有条件地等待对 <xref:System.IO.StreamWriter.WriteLineAsync(System.String)?displayProperty=nameWithType> 的调用完成，该调用在行不包含 `"Second"` 时将该行写入文件。</span><span class="sxs-lookup"><span data-stu-id="53fe0-133">Conditionally awaits a call to <xref:System.IO.StreamWriter.WriteLineAsync(System.String)?displayProperty=nameWithType>, which writes the line to the file when the line doesn't contain `"Second"`.</span></span>

## <a name="append-text-to-an-existing-file"></a><span data-ttu-id="53fe0-134">将文本追加到现有文件</span><span class="sxs-lookup"><span data-stu-id="53fe0-134">Append text to an existing file</span></span>

:::code language="csharp" source="snippets/write-text/StreamWriterTwo.cs":::

<span data-ttu-id="53fe0-135">前面的源代码示例：</span><span class="sxs-lookup"><span data-stu-id="53fe0-135">The preceding source code example:</span></span>

- <span data-ttu-id="53fe0-136">使用三个值实例化字符串数组。</span><span class="sxs-lookup"><span data-stu-id="53fe0-136">Instantiates a string array with three values.</span></span>
- <span data-ttu-id="53fe0-137">以 [using 声明](../../whats-new/csharp-8.md#using-declarations)的形式使用 WriteLines2.txt 的文件路径实例化 <xref:System.IO.StreamWriter>，并传入要追加的 `true`。</span><span class="sxs-lookup"><span data-stu-id="53fe0-137">Instantiates a <xref:System.IO.StreamWriter> with a file path of *WriteLines2.txt* as a [using declaration](../../whats-new/csharp-8.md#using-declarations), passing in `true` to append.</span></span>
- <span data-ttu-id="53fe0-138">等待对 <xref:System.IO.StreamWriter.WriteLineAsync(System.String)?displayProperty=nameWithType> 的调用完成，该调用将字符串作为追加行写入文件。</span><span class="sxs-lookup"><span data-stu-id="53fe0-138">Awaits a call to <xref:System.IO.StreamWriter.WriteLineAsync(System.String)?displayProperty=nameWithType>, which writes the string to the file as an appended line.</span></span>

## <a name="exceptions"></a><span data-ttu-id="53fe0-139">异常</span><span class="sxs-lookup"><span data-stu-id="53fe0-139">Exceptions</span></span>

<span data-ttu-id="53fe0-140">以下情况可能会导致异常：</span><span class="sxs-lookup"><span data-stu-id="53fe0-140">The following conditions may cause an exception:</span></span>

- <span data-ttu-id="53fe0-141"><xref:System.InvalidOperationException>：文件已存在并且为只读。</span><span class="sxs-lookup"><span data-stu-id="53fe0-141"><xref:System.InvalidOperationException>: The file exists and is read-only.</span></span>
- <span data-ttu-id="53fe0-142"><xref:System.IO.PathTooLongException>：路径名可能太长。</span><span class="sxs-lookup"><span data-stu-id="53fe0-142"><xref:System.IO.PathTooLongException>: The path name may be too long.</span></span>
- <span data-ttu-id="53fe0-143"><xref:System.IO.IOException>：磁盘可能已满。</span><span class="sxs-lookup"><span data-stu-id="53fe0-143"><xref:System.IO.IOException>: The disk may be full.</span></span>

<span data-ttu-id="53fe0-144">使用文件系统时，还有其他可能会导致异常的情况，因此最好进行防御性编程。</span><span class="sxs-lookup"><span data-stu-id="53fe0-144">There are additional conditions that may cause exceptions when working with the file system, it is best to program defensively.</span></span>

## <a name="see-also"></a><span data-ttu-id="53fe0-145">请参阅</span><span class="sxs-lookup"><span data-stu-id="53fe0-145">See also</span></span>

- [<span data-ttu-id="53fe0-146">C# 编程指南</span><span class="sxs-lookup"><span data-stu-id="53fe0-146">C# Programming Guide</span></span>](../index.md)
- [<span data-ttu-id="53fe0-147">文件系统和注册表（C# 编程指南）</span><span class="sxs-lookup"><span data-stu-id="53fe0-147">File System and the Registry (C# Programming Guide)</span></span>](./index.md)
- [<span data-ttu-id="53fe0-148">示例：将集合保存到应用程序存储</span><span class="sxs-lookup"><span data-stu-id="53fe0-148">Sample: Save a collection to Application Storage</span></span>](https://code.msdn.microsoft.com/CSWinStoreAppSaveCollection-bed5d6e6)
