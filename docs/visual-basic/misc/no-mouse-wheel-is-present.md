---
description: 了解详细信息：不存在鼠标轮
title: 没有鼠标滚轮
ms.date: 07/20/2015
f1_keywords:
- vbrMouse_NoWheelIsPresent
ms.assetid: e924ffba-4af1-4247-9a6f-d19a03738f62
ms.openlocfilehash: c712903f41aa9f7c37c0cf1e3ffdc76edfd85b7f
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100479096"
---
# <a name="no-mouse-wheel-is-present"></a><span data-ttu-id="bad13-103">没有鼠标滚轮</span><span class="sxs-lookup"><span data-stu-id="bad13-103">No mouse wheel is present</span></span>

<span data-ttu-id="bad13-104">调用了 `My.Computer.Mouse.WheelScrollLines` 属性，但鼠标没有滚轮。</span><span class="sxs-lookup"><span data-stu-id="bad13-104">The `My.Computer.Mouse.WheelScrollLines` property was called, but the mouse has no scroll wheel.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="bad13-105">更正此错误</span><span class="sxs-lookup"><span data-stu-id="bad13-105">To correct this error</span></span>  
  
- <span data-ttu-id="bad13-106">检查 `My.Computer.Mouse.WheelExists` 属性，以查看鼠标是否有滚轮，然后再调用 `My.Computer.Mouse.WheelScrollLines` 属性。</span><span class="sxs-lookup"><span data-stu-id="bad13-106">Check the `My.Computer.Mouse.WheelExists` property to see if the mouse has a scroll wheel before calling the `My.Computer.Mouse.WheelScrollLines` property.</span></span>  
  
     <span data-ttu-id="bad13-107">- 或 -</span><span class="sxs-lookup"><span data-stu-id="bad13-107">-or-</span></span>  
  
- <span data-ttu-id="bad13-108">在计算机上安装带滚轮的鼠标。</span><span class="sxs-lookup"><span data-stu-id="bad13-108">Install a mouse with a scroll wheel on the computer.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bad13-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="bad13-109">See also</span></span>

- [<span data-ttu-id="bad13-110">我的 My.computer.mouse.wheelscrolllines</span><span class="sxs-lookup"><span data-stu-id="bad13-110">My.Computer.Mouse.WheelScrollLines</span></span>](xref:Microsoft.VisualBasic.Devices.Mouse.WheelScrollLines)
- [<span data-ttu-id="bad13-111">我的 My.computer.mouse.wheelexists</span><span class="sxs-lookup"><span data-stu-id="bad13-111">My.Computer.Mouse.WheelExists</span></span>](xref:Microsoft.VisualBasic.Devices.Mouse.WheelExists)
- [<span data-ttu-id="bad13-112">在 .NET 中处理和引发异常</span><span class="sxs-lookup"><span data-stu-id="bad13-112">Handling and throwing exceptions in .NET</span></span>](../../standard/exceptions/index.md)
