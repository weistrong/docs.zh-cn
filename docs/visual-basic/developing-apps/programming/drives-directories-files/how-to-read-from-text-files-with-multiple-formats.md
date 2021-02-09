---
description: 详细了解：操作说明：在 Visual Basic 中读取具有多种格式的文本文件
title: 操作说明：读取具有多种格式的文本文件
ms.date: 07/20/2015
helpviewer_keywords:
- TextFieldParser object, reading from a file
- TextFieldType enumeration
- My.Computer.FileSystem.WriteAllText method, parsing structured text files
- WriteAllText method [Visual Basic], parsing structured text files
- PeekChars method [Visual Basic], determining format of text
- reading text files [Visual Basic], multiple formats
- I/O [Visual Basic], reading text files
- text files [Visual Basic], reading
ms.assetid: 8d185eb2-79ca-42cd-95a7-d3ff44a5a0f8
ms.openlocfilehash: 90d981ad051fb395d57604434cf9ba6b74603e7d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797440"
---
# <a name="how-to-read-from-fext-files-with-multiple-formats-in-visual-basic"></a><span data-ttu-id="2c47a-103">操作说明：在 Visual Basic 中读取具有多种格式的文本文件</span><span class="sxs-lookup"><span data-stu-id="2c47a-103">How to: Read from fext files with multiple formats in Visual Basic</span></span>

<span data-ttu-id="2c47a-104"><xref:Microsoft.VisualBasic.FileIO.TextFieldParser> 对象提供一种可以轻松而高效地分析结构化文本文件（如日志）的方法。</span><span class="sxs-lookup"><span data-stu-id="2c47a-104">The <xref:Microsoft.VisualBasic.FileIO.TextFieldParser> object provides a way to easily and efficiently parse structured text files, such as logs.</span></span> <span data-ttu-id="2c47a-105">可以使用 `PeekChars` 方法处理具有多种格式的文件，以便在分析整个文件时确定每行的格式。</span><span class="sxs-lookup"><span data-stu-id="2c47a-105">You can process a file with multiple formats by using the `PeekChars` method to determine the format of each line as you parse through the file.</span></span>
  
### <a name="to-parse-a-text-file-with-multiple-formats"></a><span data-ttu-id="2c47a-106">分析具有多种格式的文本文件</span><span class="sxs-lookup"><span data-stu-id="2c47a-106">To parse a text file with multiple formats</span></span>

1. <span data-ttu-id="2c47a-107">将名为 testfile.txt 的文本文件添加到你的项目中。</span><span class="sxs-lookup"><span data-stu-id="2c47a-107">Add a text file named *testfile.txt* to your project.</span></span> <span data-ttu-id="2c47a-108">向文本文件添加以下内容：</span><span class="sxs-lookup"><span data-stu-id="2c47a-108">Add the following content to the text file:</span></span>

    ```text
    Err  1001 Cannot access resource.
    Err  2014 Resource not found.
    Acc  10/03/2009User1      Administrator.
    Err  0323 Warning: Invalid access attempt.
    Acc  10/03/2009User2      Standard user.
    Acc  10/04/2009User2      Standard user.
    ```

2. <span data-ttu-id="2c47a-109">定义所需格式和报告错误时使用的格式。</span><span class="sxs-lookup"><span data-stu-id="2c47a-109">Define the expected format and the format used when an error is reported.</span></span> <span data-ttu-id="2c47a-110">每个数组中的最后一项为 -1，因此假定最后一个字段为可变宽度。</span><span class="sxs-lookup"><span data-stu-id="2c47a-110">The last entry in each array is -1, therefore the last field is assumed to be of variable width.</span></span> <span data-ttu-id="2c47a-111">数组中的最后一项小于或等于 0 时，会出现这种情况。</span><span class="sxs-lookup"><span data-stu-id="2c47a-111">This occurs when the last entry in the array is less than or equal to 0.</span></span>

     [!code-vb[VbFileIORead#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbFileIORead/VB/Class1.vb#4)]

3. <span data-ttu-id="2c47a-112">创建新的 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser> 对象，定义宽度和格式。</span><span class="sxs-lookup"><span data-stu-id="2c47a-112">Create a new <xref:Microsoft.VisualBasic.FileIO.TextFieldParser> object, defining the width and format.</span></span>

     [!code-vb[VbFileIORead#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbFileIORead/VB/Class1.vb#5)]

4. <span data-ttu-id="2c47a-113">依次通过各行，并在读取之前测试格式。</span><span class="sxs-lookup"><span data-stu-id="2c47a-113">Loop through the rows, testing for format before reading.</span></span>

     [!code-vb[VbFileIORead#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbFileIORead/VB/Class1.vb#6)]

5. <span data-ttu-id="2c47a-114">将错误写入控制台。</span><span class="sxs-lookup"><span data-stu-id="2c47a-114">Write errors to the console.</span></span>

     [!code-vb[VbFileIORead#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbFileIORead/VB/Class1.vb#7)]

## <a name="example"></a><span data-ttu-id="2c47a-115">示例</span><span class="sxs-lookup"><span data-stu-id="2c47a-115">Example</span></span>

<span data-ttu-id="2c47a-116">以下是从文件 `testfile.txt` 中读取的完整示例：</span><span class="sxs-lookup"><span data-stu-id="2c47a-116">The following is the complete example that reads from the file `testfile.txt`:</span></span>

 [!code-vb[VbFileIORead#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbFileIORead/VB/Class1.vb#8)]

## <a name="robust-programming"></a><span data-ttu-id="2c47a-117">可靠编程</span><span class="sxs-lookup"><span data-stu-id="2c47a-117">Robust programming</span></span>

<span data-ttu-id="2c47a-118">以下情况可能会导致异常：</span><span class="sxs-lookup"><span data-stu-id="2c47a-118">The following conditions may cause an exception:</span></span>  
  
- <span data-ttu-id="2c47a-119">无法使用指定的格式分析行 (<xref:Microsoft.VisualBasic.FileIO.MalformedLineException>)。</span><span class="sxs-lookup"><span data-stu-id="2c47a-119">A row cannot be parsed using the specified format (<xref:Microsoft.VisualBasic.FileIO.MalformedLineException>).</span></span> <span data-ttu-id="2c47a-120">此异常消息指定导致发生异常的行，同时将 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.ErrorLine%2A> 属性分配给该行中包含的文本。</span><span class="sxs-lookup"><span data-stu-id="2c47a-120">The exception message specifies the line causing the exception, while the <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.ErrorLine%2A> property is assigned to the text contained in the line.</span></span>
- <span data-ttu-id="2c47a-121">指定的文件不存在 (<xref:System.IO.FileNotFoundException>)。</span><span class="sxs-lookup"><span data-stu-id="2c47a-121">The specified file does not exist (<xref:System.IO.FileNotFoundException>).</span></span>
- <span data-ttu-id="2c47a-122">在部分信任的情况下，用户没有足够的权限访问文件。</span><span class="sxs-lookup"><span data-stu-id="2c47a-122">A partial-trust situation in which the user does not have sufficient permissions to access the file.</span></span> <span data-ttu-id="2c47a-123">(<xref:System.Security.SecurityException>).</span><span class="sxs-lookup"><span data-stu-id="2c47a-123">(<xref:System.Security.SecurityException>).</span></span>
- <span data-ttu-id="2c47a-124">路径过长 (<xref:System.IO.PathTooLongException>)。</span><span class="sxs-lookup"><span data-stu-id="2c47a-124">The path is too long (<xref:System.IO.PathTooLongException>).</span></span>
- <span data-ttu-id="2c47a-125">用户没有足够的权限访问文件 (<xref:System.UnauthorizedAccessException>)。</span><span class="sxs-lookup"><span data-stu-id="2c47a-125">The user does not have sufficient permissions to access the file (<xref:System.UnauthorizedAccessException>).</span></span>

## <a name="see-also"></a><span data-ttu-id="2c47a-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2c47a-126">See also</span></span>

- <xref:Microsoft.VisualBasic.FileIO.TextFieldParser?displayProperty=nameWithType>
- <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.PeekChars%2A>
- <xref:Microsoft.VisualBasic.FileIO.MalformedLineException>
- <xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllText%2A>
- <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.EndOfData%2A>
- <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.TextFieldType%2A>
- [<span data-ttu-id="2c47a-127">如何：读取逗号分隔的文本文件</span><span class="sxs-lookup"><span data-stu-id="2c47a-127">How to: Read From Comma-Delimited Text Files</span></span>](how-to-read-from-comma-delimited-text-files.md)
- [<span data-ttu-id="2c47a-128">如何：读取固定宽度的文本文件</span><span class="sxs-lookup"><span data-stu-id="2c47a-128">How to: Read From Fixed-width Text Files</span></span>](how-to-read-from-fixed-width-text-files.md)
- [<span data-ttu-id="2c47a-129">使用 TextFieldParser 对象分析文本文件</span><span class="sxs-lookup"><span data-stu-id="2c47a-129">Parsing Text Files with the TextFieldParser Object</span></span>](parsing-text-files-with-the-textfieldparser-object.md)
