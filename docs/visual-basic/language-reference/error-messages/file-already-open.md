---
description: 了解有关以下内容的详细信息：已打开文件
title: 文件已打开
ms.date: 07/20/2015
f1_keywords:
- vbrID55
ms.assetid: d674a0fb-ef16-4cc2-9da7-709a8a07dbea
ms.openlocfilehash: 2f3345c15f4a3095a8e733c2c8424edb25b4dee6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796296"
---
# <a name="file-already-open"></a><span data-ttu-id="7dd37-103">文件已打开</span><span class="sxs-lookup"><span data-stu-id="7dd37-103">File already open</span></span>

<span data-ttu-id="7dd37-104">有时，必须先关闭文件，然后才能 `FileOpen` 进行其他或其他操作。</span><span class="sxs-lookup"><span data-stu-id="7dd37-104">Sometimes a file must be closed before another `FileOpen` or other operation can occur.</span></span> <span data-ttu-id="7dd37-105">此错误的可能原因包括：</span><span class="sxs-lookup"><span data-stu-id="7dd37-105">Among the possible causes of this error are:</span></span>

- <span data-ttu-id="7dd37-106">`FileOpen`为已打开的文件执行了顺序输出模式操作</span><span class="sxs-lookup"><span data-stu-id="7dd37-106">A sequential output mode `FileOpen` operation was executed for a file that is already open</span></span>

- <span data-ttu-id="7dd37-107">语句引用打开的文件。</span><span class="sxs-lookup"><span data-stu-id="7dd37-107">A statement refers to an open file.</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="7dd37-108">更正此错误</span><span class="sxs-lookup"><span data-stu-id="7dd37-108">To correct this error</span></span>

- <span data-ttu-id="7dd37-109">在执行语句前关闭文件。</span><span class="sxs-lookup"><span data-stu-id="7dd37-109">Close the file before executing the statement.</span></span>

## <a name="see-also"></a><span data-ttu-id="7dd37-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="7dd37-110">See also</span></span>

- <xref:Microsoft.VisualBasic.FileSystem.FileOpen%2A>
