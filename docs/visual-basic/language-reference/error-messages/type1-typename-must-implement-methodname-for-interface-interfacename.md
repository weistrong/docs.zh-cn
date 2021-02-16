---
description: 了解详细信息： BC30149： <type1> " <typename> " 必须 <methodname> 为接口 "" 实现 " <interfacename> "
title: <type1>“<typename>”必须为接口“<interfacename>”实现“<methodname>”
ms.date: 07/20/2015
f1_keywords:
- vbc30149
- bc30149
helpviewer_keywords:
- BC30149
ms.assetid: 29d1b7f4-dca7-478c-bbe7-c657f342c183
ms.openlocfilehash: b2fb7f5ea019a86b18ea89456e353778e5246d2d
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100473432"
---
# <a name="bc30149-type1typename-must-implement-methodname-for-interface-interfacename"></a><span data-ttu-id="c5b74-103">BC30149： \<type1> " \<typename> " 必须 \<methodname> 为接口 "" 实现 " \<interfacename> "</span><span class="sxs-lookup"><span data-stu-id="c5b74-103">BC30149: \<type1>'\<typename>' must implement '\<methodname>' for interface '\<interfacename>'</span></span>

<span data-ttu-id="c5b74-104">类或结构声明实现接口，但不实现由接口定义的过程。</span><span class="sxs-lookup"><span data-stu-id="c5b74-104">A class or structure claims to implement an interface but does not implement a procedure defined by the interface.</span></span> <span data-ttu-id="c5b74-105">必须实现接口的每个成员。</span><span class="sxs-lookup"><span data-stu-id="c5b74-105">Every member of the interface must be implemented.</span></span>

 <span data-ttu-id="c5b74-106">**错误 ID：** BC30149</span><span class="sxs-lookup"><span data-stu-id="c5b74-106">**Error ID:** BC30149</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="c5b74-107">更正此错误</span><span class="sxs-lookup"><span data-stu-id="c5b74-107">To correct this error</span></span>

1. <span data-ttu-id="c5b74-108">使用在接口中定义的相同名称和签名声明过程。</span><span class="sxs-lookup"><span data-stu-id="c5b74-108">Declare a procedure with the same name and signature as defined in the interface.</span></span> <span data-ttu-id="c5b74-109">请确保至少包含 `End Function` 或 `End Sub` 语句。</span><span class="sxs-lookup"><span data-stu-id="c5b74-109">Be sure to include at least the `End Function` or `End Sub` statement.</span></span>

2. <span data-ttu-id="c5b74-110">将 `Implements` 子句添加到或语句的末尾 `Function` `Sub` 。</span><span class="sxs-lookup"><span data-stu-id="c5b74-110">Add an `Implements` clause to the end of the `Function` or `Sub` statement.</span></span> <span data-ttu-id="c5b74-111">例如：</span><span class="sxs-lookup"><span data-stu-id="c5b74-111">For example:</span></span>

    ```vb
    Public Sub DoSomething() Implements IBaseInterface.DoSomething
    ```

## <a name="see-also"></a><span data-ttu-id="c5b74-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="c5b74-112">See also</span></span>

- [<span data-ttu-id="c5b74-113">Implements 语句</span><span class="sxs-lookup"><span data-stu-id="c5b74-113">Implements Statement</span></span>](../statements/implements-statement.md)
- [<span data-ttu-id="c5b74-114">接口</span><span class="sxs-lookup"><span data-stu-id="c5b74-114">Interfaces</span></span>](../../programming-guide/language-features/interfaces/index.md)
