---
description: 了解详细信息：文件名错误或号码无效
title: 错误的文件名或文件号
ms.date: 07/20/2015
f1_keywords:
- vbrID52
ms.assetid: d0e96aea-7621-48f6-a78b-5d37d18aaa4e
ms.openlocfilehash: 6e568a721fb3606c5b4bc046041c9d6f24b6d126
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797063"
---
# <a name="bad-file-name-or-number"></a><span data-ttu-id="b9d2a-103">错误的文件名或文件号</span><span class="sxs-lookup"><span data-stu-id="b9d2a-103">Bad file name or number</span></span>

<span data-ttu-id="b9d2a-104">尝试访问指定的文件时出错。</span><span class="sxs-lookup"><span data-stu-id="b9d2a-104">An error occurred while trying to access the specified file.</span></span> <span data-ttu-id="b9d2a-105">此错误的可能原因包括：</span><span class="sxs-lookup"><span data-stu-id="b9d2a-105">Among the possible causes for this error are:</span></span>  
  
- <span data-ttu-id="b9d2a-106">语句引用的文件具有未在语句中指定 `FileOpen` 或在语句中指定的、 `FileOpen` 但随后已关闭的文件。</span><span class="sxs-lookup"><span data-stu-id="b9d2a-106">A statement refers to a file with a file name or number that was not specified in the `FileOpen` statement or that was specified in a `FileOpen` statement but was subsequently closed.</span></span>  
  
- <span data-ttu-id="b9d2a-107">语句引用的文件的数量超出了文件编号范围。</span><span class="sxs-lookup"><span data-stu-id="b9d2a-107">A statement refers to a file with a number that is out of the range of file numbers.</span></span>  
  
- <span data-ttu-id="b9d2a-108">语句引用的文件名或编号无效。</span><span class="sxs-lookup"><span data-stu-id="b9d2a-108">A statement refers to a file name or number that is not valid.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="b9d2a-109">更正此错误</span><span class="sxs-lookup"><span data-stu-id="b9d2a-109">To correct this error</span></span>  
  
1. <span data-ttu-id="b9d2a-110">请确保在语句中指定了文件名 `FileOpen` 。</span><span class="sxs-lookup"><span data-stu-id="b9d2a-110">Make sure the file name is specified in a `FileOpen` statement.</span></span> <span data-ttu-id="b9d2a-111">请注意，如果调用 `FileClose` 不带参数的语句，则可能会无意中关闭所有打开的文件。</span><span class="sxs-lookup"><span data-stu-id="b9d2a-111">Note that if you invoked the `FileClose` statement without arguments, you may have inadvertently closed all open files.</span></span>  
  
2. <span data-ttu-id="b9d2a-112">如果你的代码生成了文件号算法，请确保数字有效。</span><span class="sxs-lookup"><span data-stu-id="b9d2a-112">If your code is generating file numbers algorithmically, make sure the numbers are valid.</span></span>  
  
3. <span data-ttu-id="b9d2a-113">检查文件名，确保它们符合操作系统约定。</span><span class="sxs-lookup"><span data-stu-id="b9d2a-113">Check the file names to make sure they conform to operating system conventions.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b9d2a-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="b9d2a-114">See also</span></span>

- <xref:Microsoft.VisualBasic.FileSystem.FileOpen%2A>
- [<span data-ttu-id="b9d2a-115">Visual Basic 命名约定</span><span class="sxs-lookup"><span data-stu-id="b9d2a-115">Visual Basic Naming Conventions</span></span>](../../programming-guide/program-structure/naming-conventions.md)
