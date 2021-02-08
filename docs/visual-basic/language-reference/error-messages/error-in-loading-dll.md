---
description: '了解详细信息：加载 DLL 时出错 (Visual Basic) '
title: 加载 DLL 时出错
ms.date: 07/20/2015
f1_keywords:
- vbrID48
ms.assetid: 4226cd1f-028c-477d-88a5-cb57f7e0cdc8
ms.openlocfilehash: 098d05e93d328f3667000bd81290f4b77cf7949e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796504"
---
# <a name="error-in-loading-dll-visual-basic"></a><span data-ttu-id="6132f-103">加载 DLL 时出错 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6132f-103">Error in loading DLL (Visual Basic)</span></span>

<span data-ttu-id="6132f-104">动态链接库 (DLL) 是语句的子句中指定的库 `Lib` `Declare` 。</span><span class="sxs-lookup"><span data-stu-id="6132f-104">A dynamic-link library (DLL) is a library specified in the `Lib` clause of a `Declare` statement.</span></span> <span data-ttu-id="6132f-105">此错误的可能原因包括：</span><span class="sxs-lookup"><span data-stu-id="6132f-105">Possible causes for this error include:</span></span>  
  
- <span data-ttu-id="6132f-106">该文件不是 DLL 可执行文件。</span><span class="sxs-lookup"><span data-stu-id="6132f-106">The file is not DLL executable.</span></span>  
  
- <span data-ttu-id="6132f-107">该文件不是 Microsoft Windows DLL。</span><span class="sxs-lookup"><span data-stu-id="6132f-107">The file is not a Microsoft Windows DLL.</span></span>  
  
- <span data-ttu-id="6132f-108">DLL 引用了不存在的另一个 DLL。</span><span class="sxs-lookup"><span data-stu-id="6132f-108">The DLL references another DLL that is not present.</span></span>  
  
- <span data-ttu-id="6132f-109">DLL 或被引用的 DLL 不在路径中指定的目录中。</span><span class="sxs-lookup"><span data-stu-id="6132f-109">The DLL or referenced DLL is not in a directory specified in the path.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="6132f-110">更正此错误</span><span class="sxs-lookup"><span data-stu-id="6132f-110">To correct this error</span></span>  
  
- <span data-ttu-id="6132f-111">如果该文件是源文本文件而不是 DLL 可执行文件，则必须对其进行编译并将其链接到 DLL 可执行文件形式。</span><span class="sxs-lookup"><span data-stu-id="6132f-111">If the file is a source-text file and therefore not DLL executable, it must be compiled and linked to a DLL-executable form.</span></span>  
  
- <span data-ttu-id="6132f-112">如果文件不是 Microsoft Windows DLL，请获取 Microsoft Windows 等效项。</span><span class="sxs-lookup"><span data-stu-id="6132f-112">If the file is not a Microsoft Windows DLL, obtain the Microsoft Windows equivalent.</span></span>  
  
- <span data-ttu-id="6132f-113">如果 DLL 引用了不存在的另一个 DLL，则获取被引用的 DLL 并使其可用。</span><span class="sxs-lookup"><span data-stu-id="6132f-113">If the DLL references another DLL that is not present, obtain the referenced DLL and make it available.</span></span>  
  
- <span data-ttu-id="6132f-114">如果 DLL 或被引用的 DLL 不在路径所指定的目录中，则将 DLL 移到引用的目录。</span><span class="sxs-lookup"><span data-stu-id="6132f-114">If the DLL or referenced DLL is not in a directory specified by the path, move the DLL to a referenced directory.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6132f-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="6132f-115">See also</span></span>

- [<span data-ttu-id="6132f-116">Declare Statement</span><span class="sxs-lookup"><span data-stu-id="6132f-116">Declare Statement</span></span>](../statements/declare-statement.md)
