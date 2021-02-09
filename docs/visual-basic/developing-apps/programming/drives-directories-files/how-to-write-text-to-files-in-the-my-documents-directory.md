---
description: 详细了解：操作说明：在 Visual Basic 中将文本写入“我的文档”目录中的文件
title: 如何：将文本写入“我的文档”目录中的文件
ms.date: 07/20/2015
helpviewer_keywords:
- files [Visual Basic], writing to
- text, writing to files
- examples [Visual Basic], text files
- writing to files [Visual Basic], in My Documents
ms.assetid: 1c726124-781d-4976-9baa-ed46814ff3fe
ms.openlocfilehash: da7472e9d8d4c39509dda814a18e7c0149236eeb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797362"
---
# <a name="how-to-write-text-to-files-in-the-my-documents-directory-in-visual-basic"></a><span data-ttu-id="2f707-103">如何：在 Visual Basic 中将文本写入“我的文档”目录中的文件</span><span class="sxs-lookup"><span data-stu-id="2f707-103">How to: Write Text to Files in the My Documents Directory in Visual Basic</span></span>

<span data-ttu-id="2f707-104">`My.Computer.FileSystem.SpecialDirectories` 对象允许用户访问特殊目录，如 MyDocuments 目录。</span><span class="sxs-lookup"><span data-stu-id="2f707-104">The `My.Computer.FileSystem.SpecialDirectories` object allows you to access special directories, such as the **MyDocuments** directory.</span></span>  
  
## <a name="procedure"></a><span data-ttu-id="2f707-105">过程</span><span class="sxs-lookup"><span data-stu-id="2f707-105">Procedure</span></span>  
  
#### <a name="to-write-new-text-files-in-the-my-documents-directory"></a><span data-ttu-id="2f707-106">在“我的文档”目录中写入新的文本文件</span><span class="sxs-lookup"><span data-stu-id="2f707-106">To write new text files in the My Documents directory</span></span>  
  
1. <span data-ttu-id="2f707-107">使用 `My.Computer.FileSystem.SpecialDirectories.MyDocuments` 属性提供路径。</span><span class="sxs-lookup"><span data-stu-id="2f707-107">Use the `My.Computer.FileSystem.SpecialDirectories.MyDocuments` property to supply the path.</span></span>  
  
     [!code-vb[VbFileIOWrite#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbFileIOWrite/VB/Class1.vb#1)]  
  
2. <span data-ttu-id="2f707-108">使用 `WriteAllText` 方法将文本写入指定文件。</span><span class="sxs-lookup"><span data-stu-id="2f707-108">Use the `WriteAllText` method to write text to the specified file.</span></span>  
  
     [!code-vb[VbVbcnMyFileSystem#14](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/Class1.vb#14)]  
  
## <a name="example"></a><span data-ttu-id="2f707-109">示例</span><span class="sxs-lookup"><span data-stu-id="2f707-109">Example</span></span>  

 [!code-vb[VbFileIOWrite#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbFileIOWrite/VB/Class1.vb#2)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="2f707-110">编译代码</span><span class="sxs-lookup"><span data-stu-id="2f707-110">Compiling the Code</span></span>  

 <span data-ttu-id="2f707-111">将 `test.txt` 替换为要写入的文件的名称。</span><span class="sxs-lookup"><span data-stu-id="2f707-111">Replace `test.txt` with the name of the file you want to write to.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="2f707-112">可靠编程</span><span class="sxs-lookup"><span data-stu-id="2f707-112">Robust Programming</span></span>  

 <span data-ttu-id="2f707-113">此代码会重新引发向文件写入文本时可能发生的所有异常。</span><span class="sxs-lookup"><span data-stu-id="2f707-113">This code rethrows all the exceptions that may occur when writing text to the file.</span></span> <span data-ttu-id="2f707-114">可以通过使用 Windows 窗体控件（如限制用户选择有效文件名的 [OpenFileDialog](/dotnet/desktop/winforms/controls/openfiledialog-component-windows-forms) 和 [SaveFileDialog](/dotnet/desktop/winforms/controls/savefiledialog-component-windows-forms) 组件）减少引发异常的可能性。</span><span class="sxs-lookup"><span data-stu-id="2f707-114">You can reduce the likelihood of exceptions by using Windows Forms controls such as the [OpenFileDialog](/dotnet/desktop/winforms/controls/openfiledialog-component-windows-forms) and the [SaveFileDialog](/dotnet/desktop/winforms/controls/savefiledialog-component-windows-forms) components that limit the user choices to valid file names.</span></span> <span data-ttu-id="2f707-115">但是，使用这些控件并不能做到万无一失。</span><span class="sxs-lookup"><span data-stu-id="2f707-115">Using these controls is not foolproof, however.</span></span> <span data-ttu-id="2f707-116">文件系统可以在用户选择文件和代码执行的间隙时间内更改。</span><span class="sxs-lookup"><span data-stu-id="2f707-116">The file system can change between the time the user selects a file and the time that the code executes.</span></span> <span data-ttu-id="2f707-117">因此，处理文件时，几乎总是需要处理异常。</span><span class="sxs-lookup"><span data-stu-id="2f707-117">Exception handling is therefore nearly always necessary when with working with files.</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="2f707-118">.NET Framework 安全性</span><span class="sxs-lookup"><span data-stu-id="2f707-118">.NET Framework Security</span></span>  

 <span data-ttu-id="2f707-119">如果在部分信任上下文中运行，该代码可能会因特权不足而引发异常。</span><span class="sxs-lookup"><span data-stu-id="2f707-119">If you are running in a partial-trust context, the code might throw an exception due to insufficient privileges.</span></span> <span data-ttu-id="2f707-120">有关详细信息，请参阅 [Code Access Security Basics](../../../../framework/misc/code-access-security-basics.md)。</span><span class="sxs-lookup"><span data-stu-id="2f707-120">For more information, see [Code Access Security Basics](../../../../framework/misc/code-access-security-basics.md).</span></span>  
  
 <span data-ttu-id="2f707-121">此示例创建一个新文件。</span><span class="sxs-lookup"><span data-stu-id="2f707-121">This example creates a new file.</span></span> <span data-ttu-id="2f707-122">如果某个应用程序需要创建文件，则该应用程序需要文件夹的“创建”权限。</span><span class="sxs-lookup"><span data-stu-id="2f707-122">If an application needs to create a file, that application needs Create permission for the folder.</span></span> <span data-ttu-id="2f707-123">可使用访问控制列表设置权限。</span><span class="sxs-lookup"><span data-stu-id="2f707-123">Permissions are set using access control lists.</span></span> <span data-ttu-id="2f707-124">如果文件已存在，则该应用程序只需要“写入”权限（这是较弱的权限）。</span><span class="sxs-lookup"><span data-stu-id="2f707-124">If the file already exists, the application needs only Write permission, a lesser privilege.</span></span> <span data-ttu-id="2f707-125">如有可能，在部署过程中创建文件，并且仅授予针对单个文件的“读取”权限（而不是针对文件夹授予“创建”权限）会更加安全。</span><span class="sxs-lookup"><span data-stu-id="2f707-125">Where possible, it is more secure to create the file during deployment, and only grant Read privileges to a single file, rather than to grant Create privileges for a folder.</span></span> <span data-ttu-id="2f707-126">此外，较安全的做法是将数据写入用户文件夹，而不是根文件夹或“Program Files”文件夹。</span><span class="sxs-lookup"><span data-stu-id="2f707-126">Also, it is more secure to write data to user folders than to the root folder or the **Program Files** folder.</span></span> <span data-ttu-id="2f707-127">有关详细信息，请参阅 [ACL 技术概述](/previous-versions/dotnet/netframework-4.0/ms229742(v=vs.100))。</span><span class="sxs-lookup"><span data-stu-id="2f707-127">For more information, see [ACL Technology Overview](/previous-versions/dotnet/netframework-4.0/ms229742(v=vs.100)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2f707-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2f707-128">See also</span></span>

- <xref:System.IO.Path.Combine%2A?displayProperty=nameWithType>
- <xref:Microsoft.VisualBasic.Devices.Computer>
- <xref:Microsoft.VisualBasic.FileIO.FileSystem>
- <xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllText%2A>
- <xref:Microsoft.VisualBasic.FileIO.SpecialDirectories>
