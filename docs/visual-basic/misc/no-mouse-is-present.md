---
description: 了解详细信息：不存在鼠标
title: 没有鼠标
ms.date: 07/20/2015
f1_keywords:
- vbrMouse_NoMouseIsPresent
ms.assetid: 4472fd57-4217-4463-9d3c-dc4a8fe88f1b
ms.openlocfilehash: 1964f1def655a1e38ce2b8919a69ab2e6ac929a7
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100479122"
---
# <a name="no-mouse-is-present"></a><span data-ttu-id="4d0e2-103">没有鼠标</span><span class="sxs-lookup"><span data-stu-id="4d0e2-103">No mouse is present</span></span>

<span data-ttu-id="4d0e2-104">调用了 `My.Computer.Mouse` 对象的一个属性，但是计算机未安装鼠标或鼠标端口。</span><span class="sxs-lookup"><span data-stu-id="4d0e2-104">One of the properties of the `My.Computer.Mouse` object was called, but the computer has no mouse or mouse port installed.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="4d0e2-105">更正此错误</span><span class="sxs-lookup"><span data-stu-id="4d0e2-105">To correct this error</span></span>  
  
- <span data-ttu-id="4d0e2-106">在调用周围将 `Try...Catch` 块添加到 `My.Computer.Mouse` 对象的属性。</span><span class="sxs-lookup"><span data-stu-id="4d0e2-106">Add a `Try...Catch` block around the call to the property of the `My.Computer.Mouse` object.</span></span>  
  
     <span data-ttu-id="4d0e2-107">— 或 —</span><span class="sxs-lookup"><span data-stu-id="4d0e2-107">— or —</span></span>  
  
- <span data-ttu-id="4d0e2-108">在计算机上安装鼠标。</span><span class="sxs-lookup"><span data-stu-id="4d0e2-108">Install a mouse on the computer.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4d0e2-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="4d0e2-109">See also</span></span>

- [<span data-ttu-id="4d0e2-110">My.Computer.Mouse</span><span class="sxs-lookup"><span data-stu-id="4d0e2-110">My.Computer.Mouse</span></span>](xref:Microsoft.VisualBasic.Devices.Mouse)
- [<span data-ttu-id="4d0e2-111">在 .NET 中处理和引发异常</span><span class="sxs-lookup"><span data-stu-id="4d0e2-111">Handling and throwing exceptions in .NET</span></span>](../../standard/exceptions/index.md)
- [<span data-ttu-id="4d0e2-112">Try...Catch...Finally 语句</span><span class="sxs-lookup"><span data-stu-id="4d0e2-112">Try...Catch...Finally Statement</span></span>](../language-reference/statements/try-catch-finally-statement.md)
