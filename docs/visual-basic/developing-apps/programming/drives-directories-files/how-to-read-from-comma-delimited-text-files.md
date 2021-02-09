---
description: 详细了解：如何：在 Visual Basic 中读取逗号分隔的文本文件
title: 如何：读取逗号分隔的文本文件
ms.date: 07/20/2015
helpviewer_keywords:
- files [Visual Basic], parsing
- text files [Visual Basic], tasks
- reading text files [Visual Basic], comma-delimited
- text files [Visual Basic], reading
ms.assetid: a8413fe4-0dba-49c8-8692-44fb67a9ec4f
ms.openlocfilehash: dc4d4d5a7639ab7b5aa342aa8646b02985e40797
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797479"
---
# <a name="how-to-read-from-comma-delimited-text-files-in-visual-basic"></a><span data-ttu-id="62e85-103">如何：在 Visual Basic 中读取逗号分隔的文本文件</span><span class="sxs-lookup"><span data-stu-id="62e85-103">How to: read from comma-delimited text files in Visual Basic</span></span>

<span data-ttu-id="62e85-104">`TextFieldParser` 对象提供一种可以轻松而高效地分析结构化文本文件（如日志）的方法。</span><span class="sxs-lookup"><span data-stu-id="62e85-104">The `TextFieldParser` object provides a way to easily and efficiently parse structured text files, such as logs.</span></span> <span data-ttu-id="62e85-105">`TextFieldType` 属性用于定义文件是带分隔符的文件还是具有固定宽度文本字段的文件。</span><span class="sxs-lookup"><span data-stu-id="62e85-105">The `TextFieldType` property defines whether it is a delimited file or one with fixed-width fields of text.</span></span>  
  
### <a name="to-parse-a-comma-delimited-text-file"></a><span data-ttu-id="62e85-106">分析逗号分隔的文本文件</span><span class="sxs-lookup"><span data-stu-id="62e85-106">To parse a comma delimited text file</span></span>  
  
1. <span data-ttu-id="62e85-107">创建新的 `TextFieldParser`。</span><span class="sxs-lookup"><span data-stu-id="62e85-107">Create a new `TextFieldParser`.</span></span> <span data-ttu-id="62e85-108">下面的代码创建名为 `MyReader` 的 `TextFieldParser`，并打开 `test.txt` 文件。</span><span class="sxs-lookup"><span data-stu-id="62e85-108">The following code creates the `TextFieldParser` named `MyReader` and opens the file `test.txt`.</span></span>  
  
     [!code-vb[VbFileIORead#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbFileIORead/VB/Class1.vb#15)]  
  
2. <span data-ttu-id="62e85-109">定义 `TextField` 类型和分隔符。</span><span class="sxs-lookup"><span data-stu-id="62e85-109">Define the `TextField` type and delimiter.</span></span> <span data-ttu-id="62e85-110">下面的代码将 `TextFieldType` 属性定义为 `Delimited`，并将分隔符定义为“,”。</span><span class="sxs-lookup"><span data-stu-id="62e85-110">The following code defines the `TextFieldType` property as `Delimited` and the delimiter as ",".</span></span>  
  
     [!code-vb[VbFileIORead#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbFileIORead/VB/Class1.vb#16)]  
  
3. <span data-ttu-id="62e85-111">循环访问文件中的各个字段。</span><span class="sxs-lookup"><span data-stu-id="62e85-111">Loop through the fields in the file.</span></span> <span data-ttu-id="62e85-112">如果遇到任何损坏的行，则报告错误，然后继续分析。</span><span class="sxs-lookup"><span data-stu-id="62e85-112">If any lines are corrupt, report an error and continue parsing.</span></span> <span data-ttu-id="62e85-113">下面的代码循环访问该文件，依次显示各字段并报告所有格式不正确的字段。</span><span class="sxs-lookup"><span data-stu-id="62e85-113">The following code loops through the file, displaying each field in turn and reporting any fields that are formatted incorrectly.</span></span>  
  
     [!code-vb[VbFileIORead#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbFileIORead/VB/Class1.vb#17)]  
  
4. <span data-ttu-id="62e85-114">用 `End While` 和 `End Using` 结束 `While` 和 `Using` 块。</span><span class="sxs-lookup"><span data-stu-id="62e85-114">Close the `While` and `Using` blocks with `End While` and `End Using`.</span></span>  
  
     [!code-vb[VbFileIORead#18](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbFileIORead/VB/Class1.vb#18)]  
  
## <a name="example"></a><span data-ttu-id="62e85-115">示例</span><span class="sxs-lookup"><span data-stu-id="62e85-115">Example</span></span>  

 <span data-ttu-id="62e85-116">此示例读取文件 `test.txt`。</span><span class="sxs-lookup"><span data-stu-id="62e85-116">This example reads from the file `test.txt`.</span></span>  
  
 [!code-vb[VbFileIORead#19](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbFileIORead/VB/Class1.vb#19)]  
  
## <a name="robust-programming"></a><span data-ttu-id="62e85-117">可靠编程</span><span class="sxs-lookup"><span data-stu-id="62e85-117">Robust programming</span></span>  

 <span data-ttu-id="62e85-118">以下情况可能会导致异常：</span><span class="sxs-lookup"><span data-stu-id="62e85-118">The following conditions may cause an exception:</span></span>  
  
- <span data-ttu-id="62e85-119">无法使用指定的格式分析行 (<xref:Microsoft.VisualBasic.FileIO.MalformedLineException>)。</span><span class="sxs-lookup"><span data-stu-id="62e85-119">A row cannot be parsed using the specified format (<xref:Microsoft.VisualBasic.FileIO.MalformedLineException>).</span></span> <span data-ttu-id="62e85-120">此异常消息指定导致发生异常的行，同时将 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.ErrorLine%2A> 属性分配给该行中包含的文本。</span><span class="sxs-lookup"><span data-stu-id="62e85-120">The exception message specifies the line causing the exception, while the <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.ErrorLine%2A> property is assigned the text contained in the line.</span></span>  
  
- <span data-ttu-id="62e85-121">指定的文件不存在 (<xref:System.IO.FileNotFoundException>)。</span><span class="sxs-lookup"><span data-stu-id="62e85-121">The specified file does not exist (<xref:System.IO.FileNotFoundException>).</span></span>  
  
- <span data-ttu-id="62e85-122">在部分信任的情况下，用户没有足够的权限访问文件。</span><span class="sxs-lookup"><span data-stu-id="62e85-122">A partial-trust situation in which the user does not have sufficient permissions to access the file.</span></span> <span data-ttu-id="62e85-123">(<xref:System.Security.SecurityException>).</span><span class="sxs-lookup"><span data-stu-id="62e85-123">(<xref:System.Security.SecurityException>).</span></span>  
  
- <span data-ttu-id="62e85-124">路径过长 (<xref:System.IO.PathTooLongException>)。</span><span class="sxs-lookup"><span data-stu-id="62e85-124">The path is too long (<xref:System.IO.PathTooLongException>).</span></span>  
  
- <span data-ttu-id="62e85-125">用户没有足够的权限访问文件 (<xref:System.UnauthorizedAccessException>)。</span><span class="sxs-lookup"><span data-stu-id="62e85-125">The user does not have sufficient permissions to access the file (<xref:System.UnauthorizedAccessException>).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="62e85-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="62e85-126">See also</span></span>

- <xref:Microsoft.VisualBasic.FileIO.TextFieldParser?displayProperty=nameWithType>
- [<span data-ttu-id="62e85-127">如何：读取固定宽度的文本文件</span><span class="sxs-lookup"><span data-stu-id="62e85-127">How to: Read From Fixed-width Text Files</span></span>](how-to-read-from-fixed-width-text-files.md)
- [<span data-ttu-id="62e85-128">如何：读取具有多种格式的文本文件</span><span class="sxs-lookup"><span data-stu-id="62e85-128">How to: Read From Text Files with Multiple Formats</span></span>](how-to-read-from-text-files-with-multiple-formats.md)
- [<span data-ttu-id="62e85-129">使用 TextFieldParser 对象分析文本文件</span><span class="sxs-lookup"><span data-stu-id="62e85-129">Parsing Text Files with the TextFieldParser Object</span></span>](parsing-text-files-with-the-textfieldparser-object.md)
- [<span data-ttu-id="62e85-130">演练：在 Visual Basic 中操作文件和目录</span><span class="sxs-lookup"><span data-stu-id="62e85-130">Walkthrough: Manipulating Files and Directories in Visual Basic</span></span>](walkthrough-manipulating-files-and-directories.md)
- [<span data-ttu-id="62e85-131">疑难解答：读取和写入文本文件</span><span class="sxs-lookup"><span data-stu-id="62e85-131">Troubleshooting: Reading from and Writing to Text Files</span></span>](troubleshooting-reading-from-and-writing-to-text-files.md)
