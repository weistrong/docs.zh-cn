---
description: 了解详细信息： BC30149： <type1> " <typename> " 必须 <methodname> 为接口 "" 实现 ""<interfacename>
title: <type1>“<typename>”必须为接口“<interfacename>”实现“<methodname>”
ms.date: 07/20/2015
f1_keywords:
- vbc30149
- bc30149
helpviewer_keywords:
- BC30149
ms.assetid: 29d1b7f4-dca7-478c-bbe7-c657f342c183
ms.openlocfilehash: 34635cbe5b8736d273d5972a1bb83aa3d975490b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99675008"
---
# <a name="bc30149-type1typename-must-implement-methodname-for-interface-interfacename"></a><span data-ttu-id="84f1a-103">BC30149： \<type1> " \<typename> " 必须 \<methodname> 为接口 "" 实现 " \<interfacename> "</span><span class="sxs-lookup"><span data-stu-id="84f1a-103">BC30149: \<type1>'\<typename>' must implement '\<methodname>' for interface '\<interfacename>'</span></span>

<span data-ttu-id="84f1a-104">类或结构声明实现接口，但不实现由接口定义的过程。</span><span class="sxs-lookup"><span data-stu-id="84f1a-104">A class or structure claims to implement an interface but does not implement a procedure defined by the interface.</span></span> <span data-ttu-id="84f1a-105">必须实现接口的每个成员。</span><span class="sxs-lookup"><span data-stu-id="84f1a-105">Every member of the interface must be implemented.</span></span>

 <span data-ttu-id="84f1a-106">**错误 ID：** BC30149</span><span class="sxs-lookup"><span data-stu-id="84f1a-106">**Error ID:** BC30149</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="84f1a-107">更正此错误</span><span class="sxs-lookup"><span data-stu-id="84f1a-107">To correct this error</span></span>

1. <span data-ttu-id="84f1a-108">使用在接口中定义的相同名称和签名声明过程。</span><span class="sxs-lookup"><span data-stu-id="84f1a-108">Declare a procedure with the same name and signature as defined in the interface.</span></span> <span data-ttu-id="84f1a-109">请确保至少包含 `End Function` 或 `End Sub` 语句。</span><span class="sxs-lookup"><span data-stu-id="84f1a-109">Be sure to include at least the `End Function` or `End Sub` statement.</span></span>

2. <span data-ttu-id="84f1a-110">将 `Implements` 子句添加到或语句的末尾 `Function` `Sub` 。</span><span class="sxs-lookup"><span data-stu-id="84f1a-110">Add an `Implements` clause to the end of the `Function` or `Sub` statement.</span></span> <span data-ttu-id="84f1a-111">例如：</span><span class="sxs-lookup"><span data-stu-id="84f1a-111">For example:</span></span>

    ```vb
    Public Sub DoSomething() Implements IBaseInterface.DoSomething
    ```

## <a name="see-also"></a><span data-ttu-id="84f1a-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="84f1a-112">See also</span></span>

- [<span data-ttu-id="84f1a-113">Implements 语句</span><span class="sxs-lookup"><span data-stu-id="84f1a-113">Implements Statement</span></span>](../statements/implements-statement.md)
- [<span data-ttu-id="84f1a-114">接口</span><span class="sxs-lookup"><span data-stu-id="84f1a-114">Interfaces</span></span>](../../programming-guide/language-features/interfaces/index.md)
