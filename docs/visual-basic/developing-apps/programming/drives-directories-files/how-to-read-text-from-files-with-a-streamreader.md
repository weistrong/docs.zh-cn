---
description: 详细了解：操作说明：使用 StreamReader 读取文件中的文本 (Visual Basic)
title: 如何：使用 StreamReader 读取文件中的文本
ms.date: 07/20/2015
helpviewer_keywords:
- reading files [Visual Basic], text
- text, reading from files
- reading text from files [Visual Basic]
- files [Visual Basic], reading
ms.assetid: 384033c6-18f9-4d59-9610-36371226558f
ms.openlocfilehash: 9a2eb08209a2a65f7be846c8cb5357978a48ed73
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797414"
---
# <a name="how-to-read-text-from-files-with-a-streamreader-visual-basic"></a><span data-ttu-id="2ffd7-103">如何：使用 StreamReader 读取文件中的文本 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="2ffd7-103">How to: Read Text from Files with a StreamReader (Visual Basic)</span></span>

<span data-ttu-id="2ffd7-104">`My.Computer.FileSystem` 对象提供打开 <xref:System.IO.TextReader> 和 <xref:System.IO.TextWriter> 的方法。</span><span class="sxs-lookup"><span data-stu-id="2ffd7-104">The `My.Computer.FileSystem` object provides methods to open a <xref:System.IO.TextReader> and a <xref:System.IO.TextWriter>.</span></span> <span data-ttu-id="2ffd7-105">这些方法（`OpenTextFileWriter` 和 `OpenTextFileReader`）是高级方法，除非选择“全部”选项卡，否则它们不会出现在 IntelliSense 中。</span><span class="sxs-lookup"><span data-stu-id="2ffd7-105">These methods, `OpenTextFileWriter` and `OpenTextFileReader`, are advanced methods that do not appear in IntelliSense unless you select the **All** tab.</span></span>  
  
### <a name="to-read-a-line-from-a-file-with-a-text-reader"></a><span data-ttu-id="2ffd7-106">使用文本读取器从文件读取一行</span><span class="sxs-lookup"><span data-stu-id="2ffd7-106">To read a line from a file with a text reader</span></span>  
  
- <span data-ttu-id="2ffd7-107">使用 `OpenTextFileReader` 方法打开 <xref:System.IO.TextReader> 并指定文件。</span><span class="sxs-lookup"><span data-stu-id="2ffd7-107">Use the `OpenTextFileReader` method to open the <xref:System.IO.TextReader>, specifying the file.</span></span> <span data-ttu-id="2ffd7-108">此示例打开名为 `testfile.txt` 的文件、从中读取一行，然后在消息框中显示该行。</span><span class="sxs-lookup"><span data-stu-id="2ffd7-108">This example opens the file named `testfile.txt`, reads a line from it, and displays the line in a message box.</span></span>  
  
     [!code-vb[VbFileIORead#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbFileIORead/VB/Class1.vb#1)]  
  
## <a name="robust-programming"></a><span data-ttu-id="2ffd7-109">可靠编程</span><span class="sxs-lookup"><span data-stu-id="2ffd7-109">Robust Programming</span></span>  

 <span data-ttu-id="2ffd7-110">读取的文件必须是文本文件。</span><span class="sxs-lookup"><span data-stu-id="2ffd7-110">The file that is read must be a text file.</span></span>  
  
 <span data-ttu-id="2ffd7-111">不要根据文件的名称来判断文件的内容。</span><span class="sxs-lookup"><span data-stu-id="2ffd7-111">Do not make decisions about the contents of the file based on the name of the file.</span></span> <span data-ttu-id="2ffd7-112">例如，文件 Form1.vb 可能不是 Visual Basic 源文件。</span><span class="sxs-lookup"><span data-stu-id="2ffd7-112">For example, the file Form1.vb may not be a Visual Basic source file.</span></span>  
  
 <span data-ttu-id="2ffd7-113">在应用程序中使用输入的数据之前，需验证所有的输入内容。</span><span class="sxs-lookup"><span data-stu-id="2ffd7-113">Verify all inputs before using the data in your application.</span></span> <span data-ttu-id="2ffd7-114">文件的内容可能不是预期内容，并且用来读取该文件的方法可能失败。</span><span class="sxs-lookup"><span data-stu-id="2ffd7-114">The contents of the file may not be what is expected, and methods to read from the file may fail.</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="2ffd7-115">.NET Framework 安全性</span><span class="sxs-lookup"><span data-stu-id="2ffd7-115">.NET Framework Security</span></span>  

 <span data-ttu-id="2ffd7-116">若要从文件中读取，程序集需要 <xref:System.Security.Permissions.FileIOPermission> 类授予的特权等级。</span><span class="sxs-lookup"><span data-stu-id="2ffd7-116">To read from a file, your assembly requires a privilege level granted by the <xref:System.Security.Permissions.FileIOPermission> class.</span></span> <span data-ttu-id="2ffd7-117">如果在部分信任上下文中运行，该代码可能会因特权不足而引发异常。</span><span class="sxs-lookup"><span data-stu-id="2ffd7-117">If you are running in a partial-trust context, the code might throw an exception due to insufficient privileges.</span></span> <span data-ttu-id="2ffd7-118">有关详细信息，请参阅 [Code Access Security Basics](../../../../framework/misc/code-access-security-basics.md)。</span><span class="sxs-lookup"><span data-stu-id="2ffd7-118">For more information, see [Code Access Security Basics](../../../../framework/misc/code-access-security-basics.md).</span></span> <span data-ttu-id="2ffd7-119">用户还需要具有对文件的访问权限。</span><span class="sxs-lookup"><span data-stu-id="2ffd7-119">The user also needs access to the file.</span></span> <span data-ttu-id="2ffd7-120">有关详细信息，请参阅 [ACL 技术概述](/previous-versions/dotnet/netframework-4.0/ms229742(v=vs.100))。</span><span class="sxs-lookup"><span data-stu-id="2ffd7-120">For more information, see [ACL Technology Overview](/previous-versions/dotnet/netframework-4.0/ms229742(v=vs.100)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2ffd7-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2ffd7-121">See also</span></span>

- <xref:Microsoft.VisualBasic.FileIO.FileSystem>
- <xref:System.Windows.Forms.OpenFileDialog>
- <xref:Microsoft.VisualBasic.FileIO.FileSystem.OpenTextFileWriter%2A>
- <xref:Microsoft.VisualBasic.FileIO.FileSystem.OpenTextFileReader%2A>
- [<span data-ttu-id="2ffd7-122">SaveFileDialog 组件</span><span class="sxs-lookup"><span data-stu-id="2ffd7-122">SaveFileDialog Component</span></span>](/dotnet/desktop/winforms/controls/savefiledialog-component-windows-forms)
- [<span data-ttu-id="2ffd7-123">从文件读取</span><span class="sxs-lookup"><span data-stu-id="2ffd7-123">Reading from Files</span></span>](reading-from-files.md)
