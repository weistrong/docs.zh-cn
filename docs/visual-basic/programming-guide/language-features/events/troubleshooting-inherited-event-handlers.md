---
description: 了解更多相关信息： Visual Basic 中继承的事件处理程序疑难解答
title: 继承的事件处理程序疑难解答
ms.date: 07/20/2015
helpviewer_keywords:
- troubleshooting events [Visual Basic]
- inherited events [Visual Basic]
- troubleshooting Visual Basic, event handlers
- event handling, troubleshooting
- event handlers, troubleshooting
ms.assetid: e1c8759f-5370-4308-8476-8c48b73509bf
ms.openlocfilehash: b489b6c85510bb942b403a508b6bbe232c3e1853
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100424471"
---
# <a name="troubleshooting-inherited-event-handlers-in-visual-basic"></a><span data-ttu-id="96ba0-103">有关 Visual Basic 中继承的事件处理程序的疑难解答</span><span class="sxs-lookup"><span data-stu-id="96ba0-103">Troubleshooting Inherited Event Handlers in Visual Basic</span></span>

<span data-ttu-id="96ba0-104">本主题列出了继承的组件中的事件处理程序所发生的常见问题。</span><span class="sxs-lookup"><span data-stu-id="96ba0-104">This topic lists common issues that arise with event handlers in inherited components.</span></span>  
  
## <a name="procedures"></a><span data-ttu-id="96ba0-105">过程</span><span class="sxs-lookup"><span data-stu-id="96ba0-105">Procedures</span></span>  
  
#### <a name="code-in-event-handler-executes-twice-for-every-call"></a><span data-ttu-id="96ba0-106">事件处理程序中的代码对每个调用执行两次</span><span class="sxs-lookup"><span data-stu-id="96ba0-106">Code in Event Handler Executes Twice for Every Call</span></span>  
  
- <span data-ttu-id="96ba0-107">继承的事件处理程序不得包含 [Handles](../../../language-reference/statements/handles-clause.md) 子句。</span><span class="sxs-lookup"><span data-stu-id="96ba0-107">An inherited event handler must not include a [Handles](../../../language-reference/statements/handles-clause.md) clause.</span></span> <span data-ttu-id="96ba0-108">基类中的方法已与事件关联，并会相应地激发。</span><span class="sxs-lookup"><span data-stu-id="96ba0-108">The method in the base class is already associated with the event and will fire accordingly.</span></span> <span data-ttu-id="96ba0-109">`Handles`从继承的方法中删除子句。</span><span class="sxs-lookup"><span data-stu-id="96ba0-109">Remove the `Handles` clause from the inherited method.</span></span>  
  
     [!code-vb[VbVbalrEvents#32](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrEvents/VB/Class1.vb#32)]  
  
- <span data-ttu-id="96ba0-110">如果继承的方法不具有 `Handles` 关键字，请验证你的代码不包含额外的 [AddHandler 语句](../../../language-reference/statements/addhandler-statement.md) 或处理相同事件的任何其他方法。</span><span class="sxs-lookup"><span data-stu-id="96ba0-110">If the inherited method does not have a `Handles` keyword, verify that your code does not contain an extra [AddHandler Statement](../../../language-reference/statements/addhandler-statement.md) or any additional methods that handle the same event.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="96ba0-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="96ba0-111">See also</span></span>

- [<span data-ttu-id="96ba0-112">事件</span><span class="sxs-lookup"><span data-stu-id="96ba0-112">Events</span></span>](index.md)
