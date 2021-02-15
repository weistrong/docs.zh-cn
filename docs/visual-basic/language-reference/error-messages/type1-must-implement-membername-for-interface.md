---
description: 了解详细信息： BC30154： <type1> " <typename> " 必须 <membername> 为接口 "" 实现 " <interfacename> "
title: <type1>“<typename>”必须为接口“<interfacename>”实现“<membername>”
ms.date: 07/20/2015
f1_keywords:
- vbc30154
- bc30154
helpviewer_keywords:
- BC30154
ms.assetid: 259afdfa-3608-4760-adcb-88ec0da5020d
ms.openlocfilehash: fc0cf8544984ddf41f1f91cb0bca90b630d9614d
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100473558"
---
# <a name="bc30154-type1typename-must-implement-membername-for-interface-interfacename"></a><span data-ttu-id="3596a-103">BC30154： \<type1> " \<typename> " 必须 \<membername> 为接口 "" 实现 " \<interfacename> "</span><span class="sxs-lookup"><span data-stu-id="3596a-103">BC30154: \<type1>'\<typename>' must implement '\<membername>' for interface '\<interfacename>'</span></span>

<span data-ttu-id="3596a-104">" \<typename> " 必须为接口 "" 实现 "" \<membername> \<interfacename> 。</span><span class="sxs-lookup"><span data-stu-id="3596a-104">'\<typename>' must implement '\<membername>' for interface '\<interfacename>'.</span></span> <span data-ttu-id="3596a-105">实现属性必须具有匹配的 "ReadOnly"/"WriteOnly" 说明符。</span><span class="sxs-lookup"><span data-stu-id="3596a-105">Implementing property must have matching 'ReadOnly'/'WriteOnly' specifiers.</span></span>

 <span data-ttu-id="3596a-106">类或结构声明实现接口，但不实现由接口定义的过程、属性或事件。</span><span class="sxs-lookup"><span data-stu-id="3596a-106">A class or structure claims to implement an interface but does not implement a procedure, property, or event defined by the interface.</span></span> <span data-ttu-id="3596a-107">必须实现接口的每个成员。</span><span class="sxs-lookup"><span data-stu-id="3596a-107">Every member of the interface must be implemented.</span></span>

 <span data-ttu-id="3596a-108">**错误 ID：** BC30154</span><span class="sxs-lookup"><span data-stu-id="3596a-108">**Error ID:** BC30154</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="3596a-109">更正此错误</span><span class="sxs-lookup"><span data-stu-id="3596a-109">To correct this error</span></span>

1. <span data-ttu-id="3596a-110">使用在接口中定义的相同名称和签名声明成员。</span><span class="sxs-lookup"><span data-stu-id="3596a-110">Declare a member with the same name and signature as defined in the interface.</span></span> <span data-ttu-id="3596a-111">请确保至少包含 `End Function` 、 `End Sub` 或 `End Property` 语句。</span><span class="sxs-lookup"><span data-stu-id="3596a-111">Be sure to include at least the `End Function`, `End Sub`, or `End Property` statement.</span></span>

2. <span data-ttu-id="3596a-112">将 `Implements` 子句添加到 `Function` 、、 `Sub` `Property` 或 `Event` 语句的末尾。</span><span class="sxs-lookup"><span data-stu-id="3596a-112">Add an `Implements` clause to the end of the `Function`, `Sub`, `Property`, or `Event` statement.</span></span> <span data-ttu-id="3596a-113">例如：</span><span class="sxs-lookup"><span data-stu-id="3596a-113">For example:</span></span>

    ```vb
    Public Event ItHappened() Implements IBaseInterface.ItHappened
    ```

3. <span data-ttu-id="3596a-114">实现某个属性时，请确保 `ReadOnly` 或的 `WriteOnly` 使用方式与接口定义中的相同。</span><span class="sxs-lookup"><span data-stu-id="3596a-114">When implementing a property, make sure that `ReadOnly` or `WriteOnly` is used in the same way as in the interface definition.</span></span>

4. <span data-ttu-id="3596a-115">在实现属性时，请 `Get` `Set` 根据需要声明和过程。</span><span class="sxs-lookup"><span data-stu-id="3596a-115">When implementing a property, declare `Get` and `Set` procedures, as appropriate.</span></span>

## <a name="see-also"></a><span data-ttu-id="3596a-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="3596a-116">See also</span></span>

- [<span data-ttu-id="3596a-117">Implements 语句</span><span class="sxs-lookup"><span data-stu-id="3596a-117">Implements Statement</span></span>](../statements/implements-statement.md)
- [<span data-ttu-id="3596a-118">接口</span><span class="sxs-lookup"><span data-stu-id="3596a-118">Interfaces</span></span>](../../programming-guide/language-features/interfaces/index.md)
