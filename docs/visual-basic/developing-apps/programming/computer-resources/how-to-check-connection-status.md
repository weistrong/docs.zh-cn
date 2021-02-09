---
description: 详细了解：操作说明：在 Visual Basic 中检查连接状态
title: 如何：检查连接状态
ms.date: 07/20/2015
helpviewer_keywords:
- Web connections [Visual Basic]
- IsAvailable property [Visual Basic], about IsAvailable
- connections [Visual Basic], checking status
- connection status [Visual Basic]
ms.assetid: 4d9ee8ab-9a6f-4279-ace4-b75afc976a74
ms.openlocfilehash: c568e3be5d8fedb1ae12c748110b23218deaf069
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797739"
---
# <a name="how-to-check-connection-status-in-visual-basic"></a><span data-ttu-id="1223f-103">如何：在 Visual Basic 中检查连接状态</span><span class="sxs-lookup"><span data-stu-id="1223f-103">How to: Check Connection Status in Visual Basic</span></span>

<span data-ttu-id="1223f-104"><xref:Microsoft.VisualBasic.Devices.Network.IsAvailable> 属性可用于确定计算机是否具有有效的网络连接或 Internet 连接。</span><span class="sxs-lookup"><span data-stu-id="1223f-104">The <xref:Microsoft.VisualBasic.Devices.Network.IsAvailable> property can be used to determine whether the computer has a working network or Internet connection.</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-check-whether-a-computer-has-a-working-connection"></a><span data-ttu-id="1223f-105">检查计算机是否具有有效的网络连接</span><span class="sxs-lookup"><span data-stu-id="1223f-105">To check whether a computer has a working connection</span></span>  
  
- <span data-ttu-id="1223f-106">确定 `IsAvailable` 属性是 `True` 还是 `False`。</span><span class="sxs-lookup"><span data-stu-id="1223f-106">Determine whether the `IsAvailable` property is `True` or `False`.</span></span> <span data-ttu-id="1223f-107">以下代码检查属性的状态并进行报告：</span><span class="sxs-lookup"><span data-stu-id="1223f-107">The following code checks the property's status and reports it:</span></span>  
  
     [!code-vb[VbResourceTasks#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbResourceTasks/VB/Class1.vb#3)]  
  
     <span data-ttu-id="1223f-108">此代码示例也可作为 IntelliSense 代码片段。</span><span class="sxs-lookup"><span data-stu-id="1223f-108">This code example is also available as an IntelliSense code snippet.</span></span> <span data-ttu-id="1223f-109">它位于代码片段选取器的“连接和网络”中。</span><span class="sxs-lookup"><span data-stu-id="1223f-109">In the code snippet picker, it is located in **Connectivity and Networking**.</span></span> <span data-ttu-id="1223f-110">有关详细信息，请参阅[代码片段](/visualstudio/ide/code-snippets)。</span><span class="sxs-lookup"><span data-stu-id="1223f-110">For more information, see [Code Snippets](/visualstudio/ide/code-snippets).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1223f-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1223f-111">See also</span></span>

- <xref:Microsoft.VisualBasic.Devices.Network?displayProperty=nameWithType>
- <xref:Microsoft.VisualBasic.Devices.Network.IsAvailable>
