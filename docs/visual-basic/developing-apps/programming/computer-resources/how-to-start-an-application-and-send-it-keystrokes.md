---
description: 详细了解：如何：启动应用程序并向其发送击键 (Visual Basic)
title: 如何：启动应用程序并向其发送击键 - Visual Basic
ms.date: 10/23/2019
helpviewer_keywords:
- keystrokes, sending
- Shell command example [Visual Basic]
- processes, starting and sending keystrokes
- SendKeys.SendWait examples
ms.assetid: f1303184-fce4-44fb-88b4-aac5f42d5d77
ms.openlocfilehash: ea54b940b528e0833d9c7a6cbef67f65a4cb4f6b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99666454"
---
# <a name="how-to-start-an-application-and-send-it-keystrokes-visual-basic"></a><span data-ttu-id="46e7a-103">如何：启动应用程序并向其发送击键 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="46e7a-103">How to: start an application and send it keystrokes (Visual Basic)</span></span>

<span data-ttu-id="46e7a-104">本示例使用 <xref:Microsoft.VisualBasic.Interaction.Shell%2A> 方法启动记事本应用程序，然后使用 [My.Computer.Keyboard.SendKeys](xref:Microsoft.VisualBasic.Devices.Keyboard.SendKeys%2A) 方法发送击键来打印句子。</span><span class="sxs-lookup"><span data-stu-id="46e7a-104">This example uses the <xref:Microsoft.VisualBasic.Interaction.Shell%2A> method to start the Notepad application and then prints a sentence by sending keystrokes using the [My.Computer.Keyboard.SendKeys](xref:Microsoft.VisualBasic.Devices.Keyboard.SendKeys%2A) method.</span></span>

## <a name="example"></a><span data-ttu-id="46e7a-105">示例</span><span class="sxs-lookup"><span data-stu-id="46e7a-105">Example</span></span>

[!code-vb[VbVbalrMyComputer#25](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyComputer/VB/Class2.vb#25)]

## <a name="robust-programming"></a><span data-ttu-id="46e7a-106">可靠编程</span><span class="sxs-lookup"><span data-stu-id="46e7a-106">Robust programming</span></span>

<span data-ttu-id="46e7a-107">如果找不到具有请求的进程标识符的应用程序，则会引发 <xref:System.ArgumentException> 异常。</span><span class="sxs-lookup"><span data-stu-id="46e7a-107">An <xref:System.ArgumentException> exception is raised if an application with the requested process identifier cannot be found.</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="46e7a-108">.NET Framework 安全性</span><span class="sxs-lookup"><span data-stu-id="46e7a-108">.NET Framework Security</span></span>

<span data-ttu-id="46e7a-109">对 `Shell` 函数的调用需要完全信任（<xref:System.Security.SecurityException> 类）。</span><span class="sxs-lookup"><span data-stu-id="46e7a-109">The call to the `Shell` function requires full trust (<xref:System.Security.SecurityException> class).</span></span>

## <a name="see-also"></a><span data-ttu-id="46e7a-110">另请参阅</span><span class="sxs-lookup"><span data-stu-id="46e7a-110">See also</span></span>

- <xref:Microsoft.VisualBasic.Devices.Keyboard.SendKeys%2A>
- <xref:Microsoft.VisualBasic.Interaction.Shell%2A>
- <xref:Microsoft.VisualBasic.Interaction.AppActivate%2A>
