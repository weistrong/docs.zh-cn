---
description: 详细了解：疑难解答：读取和写入文本文件 (Visual Basic)
title: 疑难解答：读取和写入文本文件
ms.date: 07/20/2015
helpviewer_keywords:
- troubleshooting file I/O
- writing text to files [Visual Basic], troubleshooting
- troubleshooting Visual Basic, text files
- I/O [Visual Basic], troubleshooting text files
- writing to files [Visual Basic], troubleshooting
- reading text files [Visual Basic], troubleshooting
ms.assetid: a8e9b44d-facb-4718-8c0f-466537171182
ms.openlocfilehash: 1c01f7673ef021759a9c1892f685aa90ef1acdf6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99675333"
---
# <a name="troubleshooting-reading-from-and-writing-to-text-files-visual-basic"></a><span data-ttu-id="9cbb1-103">疑难解答：读取和写入文本文件 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="9cbb1-103">Troubleshooting: reading from and writing to text files (Visual Basic)</span></span>

<span data-ttu-id="9cbb1-104">本主题讨论处理文本文件时遇到的常见问题，并针对每个问题提供建议解决方法。</span><span class="sxs-lookup"><span data-stu-id="9cbb1-104">This topic discusses common problems encountered when working with text files and suggests an approach to each.</span></span>  
  
## <a name="common-problems"></a><span data-ttu-id="9cbb1-105">常见问题</span><span class="sxs-lookup"><span data-stu-id="9cbb1-105">Common problems</span></span>  

 <span data-ttu-id="9cbb1-106">处理文本文件时遇到的最常见问题包括安全异常、文件编码和无效路径。</span><span class="sxs-lookup"><span data-stu-id="9cbb1-106">The most common issues encountered when working with text files include security exceptions, file encodings, or invalid paths.</span></span>  
  
### <a name="security-exceptions"></a><span data-ttu-id="9cbb1-107">安全异常</span><span class="sxs-lookup"><span data-stu-id="9cbb1-107">Security exceptions</span></span>  

 <span data-ttu-id="9cbb1-108">安全错误发生时引发 <xref:System.Security.SecurityException>。</span><span class="sxs-lookup"><span data-stu-id="9cbb1-108">A <xref:System.Security.SecurityException> is thrown when a security error occurs.</span></span> <span data-ttu-id="9cbb1-109">这通常是由用户缺少必要权限导致的，通过添加权限或者在独立存储中处理文件可以解决该问题。</span><span class="sxs-lookup"><span data-stu-id="9cbb1-109">This is often a result of the user lacking necessary permissions, which may be solved by adding permissions or working with files in isolated storage.</span></span>  
  
### <a name="file-encodings"></a><span data-ttu-id="9cbb1-110">文件编码</span><span class="sxs-lookup"><span data-stu-id="9cbb1-110">File encodings</span></span>  

 <span data-ttu-id="9cbb1-111">文件编码也称为字符编码，用于指定在处理文本时如何表示字符。</span><span class="sxs-lookup"><span data-stu-id="9cbb1-111">File encodings, also known as character encodings, specify how to represent characters when text processing.</span></span> <span data-ttu-id="9cbb1-112">文本文件中的意外字符可能是由于不正确的编码导致的。</span><span class="sxs-lookup"><span data-stu-id="9cbb1-112">Unexpected characters in a text file may result from incorrect encoding.</span></span> <span data-ttu-id="9cbb1-113">对于大多数文件，一种编码可能优于另一种编码主要取决于它能处理或不能处理哪些语言字符，不过通常首选的是 Unicode。</span><span class="sxs-lookup"><span data-stu-id="9cbb1-113">For most files, one encoding may be preferable over another in terms of which language characters it can or cannot handle, although Unicode is usually preferred.</span></span> <span data-ttu-id="9cbb1-114">有关详细信息，请参阅[文件编码](file-encodings.md)和 <xref:System.Text.Encoding>。</span><span class="sxs-lookup"><span data-stu-id="9cbb1-114">For more information, see [File Encodings](file-encodings.md) and <xref:System.Text.Encoding>.</span></span>  
  
### <a name="incorrect-paths"></a><span data-ttu-id="9cbb1-115">错误路径</span><span class="sxs-lookup"><span data-stu-id="9cbb1-115">Incorrect paths</span></span>  

 <span data-ttu-id="9cbb1-116">分析文件路径尤其是相对路径时，很容易提供错误的数据。</span><span class="sxs-lookup"><span data-stu-id="9cbb1-116">When parsing file paths, particularly relative paths, it is easy to supply the wrong data.</span></span> <span data-ttu-id="9cbb1-117">请确保提供正确的路径，这样可以纠正许多问题。</span><span class="sxs-lookup"><span data-stu-id="9cbb1-117">Many problems can be corrected by making sure you are supplying the correct path.</span></span> <span data-ttu-id="9cbb1-118">有关详细信息，请参阅[如何：分析文件路径](how-to-parse-file-paths.md)。</span><span class="sxs-lookup"><span data-stu-id="9cbb1-118">For more information, see [How to: Parse File Paths](how-to-parse-file-paths.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9cbb1-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9cbb1-119">See also</span></span>

- <xref:Microsoft.VisualBasic.FileIO.FileSystem>
- [<span data-ttu-id="9cbb1-120">从文件读取</span><span class="sxs-lookup"><span data-stu-id="9cbb1-120">Reading from Files</span></span>](reading-from-files.md)
- [<span data-ttu-id="9cbb1-121">写入文件</span><span class="sxs-lookup"><span data-stu-id="9cbb1-121">Writing to Files</span></span>](writing-to-files.md)
- [<span data-ttu-id="9cbb1-122">使用 TextFieldParser 对象分析文本文件</span><span class="sxs-lookup"><span data-stu-id="9cbb1-122">Parsing Text Files with the TextFieldParser Object</span></span>](parsing-text-files-with-the-textfieldparser-object.md)
