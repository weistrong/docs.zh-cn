---
description: '了解详细信息： (Visual Basic 的堆栈空间不足) '
title: 堆栈空间不足
ms.date: 07/20/2015
f1_keywords:
- vbrID28
ms.assetid: bfcd792b-ac29-4158-81fc-ea0c13f4ffa2
ms.openlocfilehash: a32ca0d2becade33177596501b7eabde4251e0a9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795478"
---
# <a name="out-of-stack-space-visual-basic"></a>堆栈空间不足 (Visual Basic)

堆栈是内存的工作区，它随执行程序的需求动态地增长和收缩。 已超过其限制。  
  
## <a name="to-correct-this-error"></a>更正此错误  
  
1. 检查过程的嵌套太深。  
  
2. 请确保递归过程正确终止。  
  
3. 如果本地变量需要的本地变量空间超过可用空间，请尝试在模块级别声明一些变量。 还可以通过在 `Property` 、或关键字前面加来声明过程中的所有变量 `Sub` `Function` `Static` 。 或者，可以使用 `Static` 语句在过程中声明单个静态变量。  
  
4. 将一些固定长度的字符串重新定义为可变长度字符串，因为固定长度字符串使用的堆栈空间多于可变长度字符串。 你还可以在模块级别定义不需要堆栈空间的字符串。  
  
5. `DoEvents`通过使用 `Calls` 对话框查看在堆栈上处于活动状态的过程，检查嵌套函数调用的数量。  
  
6. 请确保通过触发调用堆栈上已有的事件过程的事件，不会导致 "事件级联"。 事件级联类似于未终止的递归过程调用，但不太明显，因为调用是通过 Visual Basic 而不是在代码中显式调用来进行的。 使用 "" `Calls` 对话框可以查看在堆栈上处于活动状态的过程。  
  
## <a name="see-also"></a>请参阅

- [“内存”窗口](/visualstudio/debugger/memory-windows)
