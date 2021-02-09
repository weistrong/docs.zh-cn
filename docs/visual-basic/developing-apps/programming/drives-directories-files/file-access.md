---
description: 详细了解：使用 Visual Basic 访问文件
title: 文件访问
ms.date: 07/20/2015
helpviewer_keywords:
- file access
- files [Visual Basic], input and output
- file access, Visual Basic
- files [Visual Basic], I/O
- file I/O classes
- data [Visual Basic], accessing from files
- files [Visual Basic], accessing
- file access, using components
- My.Computer.FileSystem object, accessing files
- I/O [Visual Basic]
- sequential access
ms.assetid: 231533bf-d049-4345-befa-3fb78fe6517d
ms.openlocfilehash: b3ea742185e7219ce7fdfb8eee987fd9c17e3a88
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99666310"
---
# <a name="file-access-with-visual-basic"></a><span data-ttu-id="e61d0-103">使用 Visual Basic 访问文件</span><span class="sxs-lookup"><span data-stu-id="e61d0-103">File Access with Visual Basic</span></span>

<span data-ttu-id="e61d0-104">`My.Computer.FileSystem` 对象提供用于处理文件和文件夹的工具。</span><span class="sxs-lookup"><span data-stu-id="e61d0-104">The `My.Computer.FileSystem` object provides tools for working with files and folders.</span></span> <span data-ttu-id="e61d0-105">它的属性、方法和事件使你可以创建、复制、移动、调查以及删除文件和文件夹。</span><span class="sxs-lookup"><span data-stu-id="e61d0-105">Its properties, methods, and events allow you to create, copy, move, investigate, and delete files and folders.</span></span> <span data-ttu-id="e61d0-106">`My.Computer.FileSystem` 提供的性能比 Visual Basic 为后向兼容性提供的旧版功能（`FileOpen`、`FileClose`、`Input`、`InputString`、`LineInput` 等）的性能更好。</span><span class="sxs-lookup"><span data-stu-id="e61d0-106">`My.Computer.FileSystem` provides better performance than the legacy functions (`FileOpen`, `FileClose`, `Input`, `InputString`, `LineInput`, etc.) that are provided by Visual Basic for backward compatibility.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="e61d0-107">本节内容</span><span class="sxs-lookup"><span data-stu-id="e61d0-107">In This Section</span></span>  

 [<span data-ttu-id="e61d0-108">从文件读取</span><span class="sxs-lookup"><span data-stu-id="e61d0-108">Reading from Files</span></span>](reading-from-files.md)  
 <span data-ttu-id="e61d0-109">列出有关使用 `My.Computer.FileSystem` 对象读取文件的主题</span><span class="sxs-lookup"><span data-stu-id="e61d0-109">Lists topics dealing with using the `My.Computer.FileSystem` object to read from files</span></span>  
  
 [<span data-ttu-id="e61d0-110">写入文件</span><span class="sxs-lookup"><span data-stu-id="e61d0-110">Writing to Files</span></span>](writing-to-files.md)  
 <span data-ttu-id="e61d0-111">列出有关使用 `My.Computer.FileSystem` 对象写入文件的主题</span><span class="sxs-lookup"><span data-stu-id="e61d0-111">Lists topics dealing with using the `My.Computer.FileSystem` object to write to files</span></span>  
  
 [<span data-ttu-id="e61d0-112">创建、删除和移动文件和目录</span><span class="sxs-lookup"><span data-stu-id="e61d0-112">Creating, Deleting, and Moving Files and Directories</span></span>](creating-deleting-and-moving-files-and-directories.md)  
 <span data-ttu-id="e61d0-113">列出有关使用 `My.Computer.FileSystem` 对象创建、复制、删除以及移动文件和文件夹的主题。</span><span class="sxs-lookup"><span data-stu-id="e61d0-113">Lists topics dealing with using the `My.Computer.FileSystem` object to creating, copying, deleting and moving files and folders.</span></span>  
  
 [<span data-ttu-id="e61d0-114">使用 TextFieldParser 对象分析文本文件</span><span class="sxs-lookup"><span data-stu-id="e61d0-114">Parsing Text Files with the TextFieldParser Object</span></span>](parsing-text-files-with-the-textfieldparser-object.md)  
 <span data-ttu-id="e61d0-115">讨论如何使用 `TextFieldReader` 来解析文本文件（如日志）。</span><span class="sxs-lookup"><span data-stu-id="e61d0-115">Discusses how to use the `TextFieldReader` to parse text files such as logs.</span></span>  
  
 [<span data-ttu-id="e61d0-116">文件编码</span><span class="sxs-lookup"><span data-stu-id="e61d0-116">File Encodings</span></span>](file-encodings.md)  
 <span data-ttu-id="e61d0-117">描述文件编码及其用法。</span><span class="sxs-lookup"><span data-stu-id="e61d0-117">Describes file encodings and their use.</span></span>  
  
 [<span data-ttu-id="e61d0-118">演练：在 Visual Basic 中操作文件和目录</span><span class="sxs-lookup"><span data-stu-id="e61d0-118">Walkthrough: Manipulating Files and Directories in Visual Basic</span></span>](walkthrough-manipulating-files-and-directories.md)  
 <span data-ttu-id="e61d0-119">演示如何创建报告文件和文件夹相关信息的实用工具。</span><span class="sxs-lookup"><span data-stu-id="e61d0-119">Demonstrates how to create a utility that reports information about files and folders.</span></span>  
  
 [<span data-ttu-id="e61d0-120">疑难解答：读取和写入文本文件</span><span class="sxs-lookup"><span data-stu-id="e61d0-120">Troubleshooting: Reading from and Writing to Text Files</span></span>](troubleshooting-reading-from-and-writing-to-text-files.md)  
 <span data-ttu-id="e61d0-121">列出读取和写入文本文件时遇到的常见问题，并为每个问题提供补救措施。</span><span class="sxs-lookup"><span data-stu-id="e61d0-121">Lists common problems encountered when reading and writing to text files, and suggests remedies for each.</span></span>
