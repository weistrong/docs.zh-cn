---
description: '了解有关详细信息，请参阅如何：引用对象的当前实例 (Visual Basic) '
title: 如何：引用对象的当前实例
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], object
- objects [Visual Basic], referring to current instance
- instances [Visual Basic], referring to current
- current instance
- object variables [Visual Basic]
ms.assetid: 7f9b2c77-03cd-428f-adc2-b18070226e7c
ms.openlocfilehash: 84a52c9d0a8b1f588630b31d022490f37595850d
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100481735"
---
# <a name="how-to-refer-to-the-current-instance-of-an-object-visual-basic"></a><span data-ttu-id="8ba07-103">如何：引用对象的当前实例 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8ba07-103">How to: Refer to the Current Instance of an Object (Visual Basic)</span></span>

<span data-ttu-id="8ba07-104">对象的 *当前实例* 是当前在其中执行代码的实例。</span><span class="sxs-lookup"><span data-stu-id="8ba07-104">The *current instance* of an object is the instance in which the code is currently executing.</span></span>  
  
 <span data-ttu-id="8ba07-105">使用 `Me` 关键字引用当前实例。</span><span class="sxs-lookup"><span data-stu-id="8ba07-105">You use the `Me` keyword to refer to the current instance.</span></span>  
  
### <a name="to-refer-to-the-current-instance"></a><span data-ttu-id="8ba07-106">引用当前实例</span><span class="sxs-lookup"><span data-stu-id="8ba07-106">To refer to the current instance</span></span>  
  
- <span data-ttu-id="8ba07-107">使用 `Me` 关键字，通常使用对象变量的名称。</span><span class="sxs-lookup"><span data-stu-id="8ba07-107">Use the `Me` keyword where you would normally use the name of an object variable.</span></span>  
  
    ```vb  
    Me.ForeColor = System.Drawing.Color.Crimson  
    Me.Close()  
    ```  
  
     <span data-ttu-id="8ba07-108">尽管 `Me` 的行为与对象变量类似，但不能对其进行声明或向其分配任何内容。</span><span class="sxs-lookup"><span data-stu-id="8ba07-108">Although `Me` behaves like an object variable, you cannot declare it or assign anything to it.</span></span> <span data-ttu-id="8ba07-109">`Me` 始终引用当前实例。</span><span class="sxs-lookup"><span data-stu-id="8ba07-109">`Me` always refers to the current instance.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8ba07-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="8ba07-110">See also</span></span>

- [<span data-ttu-id="8ba07-111">对象变量</span><span class="sxs-lookup"><span data-stu-id="8ba07-111">Object Variables</span></span>](object-variables.md)
- [<span data-ttu-id="8ba07-112">对象变量赋值</span><span class="sxs-lookup"><span data-stu-id="8ba07-112">Object Variable Assignment</span></span>](object-variable-assignment.md)
- [<span data-ttu-id="8ba07-113">Me、My、MyBase 和 MyClass</span><span class="sxs-lookup"><span data-stu-id="8ba07-113">Me, My, MyBase, and MyClass</span></span>](../../program-structure/me-my-mybase-and-myclass.md)
