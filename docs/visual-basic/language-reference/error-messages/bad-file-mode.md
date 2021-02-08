---
description: 了解更多：文件模式错误
title: 错误的文件模式
ms.date: 07/20/2015
f1_keywords:
- vbrID54
ms.assetid: 74891e96-884b-4c8d-872d-cd11ae272372
ms.openlocfilehash: da792407fb37f5c206be7ff39da14d314ef1e2d2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797076"
---
# <a name="bad-file-mode"></a><span data-ttu-id="7c87a-103">错误的文件模式</span><span class="sxs-lookup"><span data-stu-id="7c87a-103">Bad file mode</span></span>

<span data-ttu-id="7c87a-104">用于操作文件内容的语句必须适合于打开该文件的模式。</span><span class="sxs-lookup"><span data-stu-id="7c87a-104">Statements used in manipulating file contents must be appropriate to the mode in which the file was opened.</span></span> <span data-ttu-id="7c87a-105">可能的原因包括：</span><span class="sxs-lookup"><span data-stu-id="7c87a-105">Possible causes include:</span></span>  
  
- <span data-ttu-id="7c87a-106">`FilePutObject`或 `FileGetObject` 语句指定顺序文件。</span><span class="sxs-lookup"><span data-stu-id="7c87a-106">A `FilePutObject` or `FileGetObject` statement specifies a sequential file.</span></span>  
  
- <span data-ttu-id="7c87a-107">`Print`语句指定了一个打开的文件，该文件用于访问模式，而不是 `Output` 或 `Append` 。</span><span class="sxs-lookup"><span data-stu-id="7c87a-107">A `Print` statement specifies a file opened for an access mode other than `Output` or `Append`.</span></span>  
  
- <span data-ttu-id="7c87a-108">`Input`语句指定为访问模式打开的文件，而不是`Input`</span><span class="sxs-lookup"><span data-stu-id="7c87a-108">An `Input` statement specifies a file opened for an access mode other than `Input`</span></span>  
  
- <span data-ttu-id="7c87a-109">尝试写入只读文件。</span><span class="sxs-lookup"><span data-stu-id="7c87a-109">An attempt to write to a read-only file.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="7c87a-110">更正此错误</span><span class="sxs-lookup"><span data-stu-id="7c87a-110">To correct this error</span></span>  
  
- <span data-ttu-id="7c87a-111">请确保 `FilePutObject` 和 `FileGetObject` 仅引用打开的 `Random` 或访问的文件 `Binary` 。</span><span class="sxs-lookup"><span data-stu-id="7c87a-111">Make sure `FilePutObject` and `FileGetObject` are only referring to files open for `Random` or `Binary` access.</span></span>  
  
- <span data-ttu-id="7c87a-112">请确保 `Print` 为 `Output` 或访问模式指定打开的文件 `Append` 。</span><span class="sxs-lookup"><span data-stu-id="7c87a-112">Make sure `Print` specifies a file opened for either `Output` or `Append` access mode.</span></span> <span data-ttu-id="7c87a-113">否则，请使用不同的语句将数据放置在文件中，或在适当的模式下重新打开文件。</span><span class="sxs-lookup"><span data-stu-id="7c87a-113">If not, use a different statement to place data in the file, or reopen the file in an appropriate mode.</span></span>  
  
- <span data-ttu-id="7c87a-114">请确保 `Input` 指定一个打开的文件 `Input` 。</span><span class="sxs-lookup"><span data-stu-id="7c87a-114">Make sure `Input` specifies a file opened for `Input`.</span></span> <span data-ttu-id="7c87a-115">否则，请使用不同的语句将数据放置在文件中，或在适当的模式下重新打开文件。</span><span class="sxs-lookup"><span data-stu-id="7c87a-115">If not, use a different statement to place data in the file or reopen the file in an appropriate mode.</span></span>  
  
- <span data-ttu-id="7c87a-116">如果要写入只读文件，请更改该文件的读/写状态，或不要尝试写入该文件。</span><span class="sxs-lookup"><span data-stu-id="7c87a-116">If you are writing to a read-only file, change the read/write status of the file or do not try to write to it.</span></span>  
  
- <span data-ttu-id="7c87a-117">使用 `My.Computer.FileSystem` 对象中的可用功能。</span><span class="sxs-lookup"><span data-stu-id="7c87a-117">Use the functionality available in the `My.Computer.FileSystem` object.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7c87a-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="7c87a-118">See also</span></span>

- <xref:Microsoft.VisualBasic.FileSystem>
- [<span data-ttu-id="7c87a-119">疑难解答：读取和写入文本文件</span><span class="sxs-lookup"><span data-stu-id="7c87a-119">Troubleshooting: Reading from and Writing to Text Files</span></span>](../../developing-apps/programming/drives-directories-files/troubleshooting-reading-from-and-writing-to-text-files.md)
