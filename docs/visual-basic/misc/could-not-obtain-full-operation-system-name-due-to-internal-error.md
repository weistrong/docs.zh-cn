---
description: 了解详细信息：由于内部错误，无法获取完整的操作系统名
title: 由于内部错误，无法获取完整的操作系统名
ms.date: 07/20/2015
f1_keywords:
- vbrDiagnosticInfo_FullOSName
ms.assetid: f69da02b-eb9a-4284-bb9e-3025517ae6c1
ms.openlocfilehash: d274a08728b084b21309862de69e2fded5c164da
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100463488"
---
# <a name="could-not-obtain-full-operation-system-name-due-to-internal-error"></a><span data-ttu-id="d71e9-103">由于内部错误，无法获取完整的操作系统名</span><span class="sxs-lookup"><span data-stu-id="d71e9-103">Could not obtain full operation system name due to internal error</span></span>

<span data-ttu-id="d71e9-104">由于内部错误，无法获取完整的操作系统名。</span><span class="sxs-lookup"><span data-stu-id="d71e9-104">Could not obtain full operation system name due to internal error.</span></span> <span data-ttu-id="d71e9-105">这可能由当前计算机上不存在 WMI 导致。</span><span class="sxs-lookup"><span data-stu-id="d71e9-105">This might be caused by WMI not existing on the current machine.</span></span>  
  
 <span data-ttu-id="d71e9-106">对 `My.Computer.Info.OSFullName` 属性的调用失败。</span><span class="sxs-lookup"><span data-stu-id="d71e9-106">A call to the `My.Computer.Info.OSFullName` property failed.</span></span> <span data-ttu-id="d71e9-107">此失败的可能原因是当前计算机上是否未安装 Windows Management Instrumentation (WMI)。</span><span class="sxs-lookup"><span data-stu-id="d71e9-107">A possible cause for this failure is if Windows Management Instrumentation (WMI) is not installed on the current computer.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="d71e9-108">更正此错误</span><span class="sxs-lookup"><span data-stu-id="d71e9-108">To correct this error</span></span>  
  
1. <span data-ttu-id="d71e9-109">将调用周围的 `Try...Catch` 块添加到 `My.Computer.Info.OSFullName` 属性。</span><span class="sxs-lookup"><span data-stu-id="d71e9-109">Add a `Try...Catch` block around the call to the `My.Computer.Info.OSFullName` property.</span></span>  
  
2. <span data-ttu-id="d71e9-110">有关 WMI 及其安装方法的详细信息，请参阅和搜索 "Windows Management Instrumentation Core"。</span><span class="sxs-lookup"><span data-stu-id="d71e9-110">For more information about WMI and how to install it, go to  and search for "Windows Management Instrumentation Core".</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d71e9-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="d71e9-111">See also</span></span>

- [<span data-ttu-id="d71e9-112">OSFullName。</span><span class="sxs-lookup"><span data-stu-id="d71e9-112">My.Computer.Info.OSFullName</span></span>](xref:Microsoft.VisualBasic.Devices.ComputerInfo.OSFullName)
- [<span data-ttu-id="d71e9-113">在 .NET 中处理和引发异常</span><span class="sxs-lookup"><span data-stu-id="d71e9-113">Handling and throwing exceptions in .NET</span></span>](../../standard/exceptions/index.md)
- [<span data-ttu-id="d71e9-114">Try...Catch...Finally 语句</span><span class="sxs-lookup"><span data-stu-id="d71e9-114">Try...Catch...Finally Statement</span></span>](../language-reference/statements/try-catch-finally-statement.md)
