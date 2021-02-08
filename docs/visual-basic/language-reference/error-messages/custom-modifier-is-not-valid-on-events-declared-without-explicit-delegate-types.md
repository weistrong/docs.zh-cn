---
description: 了解更多相关信息： BC31122： "Custom" 修饰符在没有显式委托类型的声明事件上无效
title: “Custom”修饰符在未用显式委托类型声明的事件上无效
ms.date: 07/20/2015
f1_keywords:
- vbc31122
- bc31122
helpviewer_keywords:
- BC31122
ms.assetid: 6911f0d1-641a-473b-906d-8ee5681194be
ms.openlocfilehash: 6cbddd31dfa9c923038f8ea706bfc49233574cfb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796673"
---
# <a name="bc31122-custom-modifier-is-not-valid-on-events-declared-without-explicit-delegate-types"></a><span data-ttu-id="e48ee-103">BC31122： "Custom" 修饰符在没有显式委托类型的声明事件上无效</span><span class="sxs-lookup"><span data-stu-id="e48ee-103">BC31122: 'Custom' modifier is not valid on events declared without explicit delegate types</span></span>

<span data-ttu-id="e48ee-104">与非自定义事件不同， `Custom Event` 声明在 `As` 事件名称后需要一个子句，该事件名称显式指定事件的委托类型。</span><span class="sxs-lookup"><span data-stu-id="e48ee-104">Unlike a non-custom event, a `Custom Event` declaration requires an `As` clause following the event name that explicitly specifies the delegate type for the event.</span></span>

 <span data-ttu-id="e48ee-105">可使用 `As` 子句和显式委托类型定义非自定义事件，或使用紧跟在事件名称后面的参数列表定义。</span><span class="sxs-lookup"><span data-stu-id="e48ee-105">Non-custom events can be defined either with an `As` clause and an explicit delegate type, or with a parameter list immediately following the event name.</span></span>

 <span data-ttu-id="e48ee-106">**错误 ID：** BC31122</span><span class="sxs-lookup"><span data-stu-id="e48ee-106">**Error ID:** BC31122</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="e48ee-107">更正此错误</span><span class="sxs-lookup"><span data-stu-id="e48ee-107">To correct this error</span></span>

1. <span data-ttu-id="e48ee-108">定义与自定义事件具有相同参数列表的委托。</span><span class="sxs-lookup"><span data-stu-id="e48ee-108">Define a delegate with the same parameter list as the custom event.</span></span>

     <span data-ttu-id="e48ee-109">例如，如果定义了 `Custom Event` `Custom Event Test(ByVal sender As Object, ByVal i As Integer)` ，则相应的委托将如下所示。</span><span class="sxs-lookup"><span data-stu-id="e48ee-109">For example, if the `Custom Event` was defined by `Custom Event Test(ByVal sender As Object, ByVal i As Integer)`, then the corresponding delegate would be the following.</span></span>

     [!code-vb[VbVbalrEventError#18](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrEventError/VB/VbVbalrEventError.vb#18)]

2. <span data-ttu-id="e48ee-110">将自定义事件的参数列表替换为 `As` 指定委托类型的子句。</span><span class="sxs-lookup"><span data-stu-id="e48ee-110">Replace the parameter list of the custom event with an `As` clause specifying the delegate type.</span></span>

     <span data-ttu-id="e48ee-111">继续此示例，将 `Custom Event` 按如下所示重写声明。</span><span class="sxs-lookup"><span data-stu-id="e48ee-111">Continuing with the example, `Custom Event` declaration would be rewritten as follows.</span></span>

     [!code-vb[VbVbalrEventError#19](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrEventError/VB/VbVbalrEventError.vb#19)]

## <a name="example"></a><span data-ttu-id="e48ee-112">示例</span><span class="sxs-lookup"><span data-stu-id="e48ee-112">Example</span></span>

 <span data-ttu-id="e48ee-113">此示例声明一个 `Custom Event` ，并指定 `As` 具有委托类型的必需子句。</span><span class="sxs-lookup"><span data-stu-id="e48ee-113">This example declares a `Custom Event` and specifies the required `As` clause with a delegate type.</span></span>

 [!code-vb[VbVbalrEventError#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrEventError/VB/VbVbalrEventError.vb#2)]

## <a name="see-also"></a><span data-ttu-id="e48ee-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="e48ee-114">See also</span></span>

- [<span data-ttu-id="e48ee-115">Event 语句</span><span class="sxs-lookup"><span data-stu-id="e48ee-115">Event Statement</span></span>](../statements/event-statement.md)
- [<span data-ttu-id="e48ee-116">Delegate 语句</span><span class="sxs-lookup"><span data-stu-id="e48ee-116">Delegate Statement</span></span>](../statements/delegate-statement.md)
- [<span data-ttu-id="e48ee-117">事件</span><span class="sxs-lookup"><span data-stu-id="e48ee-117">Events</span></span>](../../programming-guide/language-features/events/index.md)
