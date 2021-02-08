---
description: 了解详细信息： BC36563：方法没有与委托兼容的签名
title: 方法没有与委托兼容的签名
ms.date: 07/20/2015
f1_keywords:
- bc36563
- vbc36563
helpviewer_keywords:
- BC36563
ms.assetid: 3ca8b873-e98d-419b-95f2-d75bd2a9eb6c
ms.openlocfilehash: d6756ea664a97e282497bf45ecd57efb7d7b59f6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795815"
---
# <a name="bc36563-method-does-not-have-a-signature-compatible-with-the-delegate"></a><span data-ttu-id="5fdfa-103">BC36563：方法没有与委托兼容的签名</span><span class="sxs-lookup"><span data-stu-id="5fdfa-103">BC36563: Method does not have a signature compatible with the delegate</span></span>

<span data-ttu-id="5fdfa-104">方法的签名与你尝试使用的委托的签名不兼容。</span><span class="sxs-lookup"><span data-stu-id="5fdfa-104">There is an incompatibility between the signatures of the method and the delegate you are trying to use.</span></span> <span data-ttu-id="5fdfa-105">`Delegate` 语句定义参数类型和委托类的返回类型。</span><span class="sxs-lookup"><span data-stu-id="5fdfa-105">The `Delegate` statement defines the parameter types and return types of a delegate class.</span></span> <span data-ttu-id="5fdfa-106">任何具有匹配的兼容类型参数和返回类型的过程都可以用于创建此委托类型的实例。</span><span class="sxs-lookup"><span data-stu-id="5fdfa-106">Any procedure that has matching parameters of compatible types and return types can be used to create an instance of this delegate type.</span></span>

 <span data-ttu-id="5fdfa-107">**错误 ID：** BC36563</span><span class="sxs-lookup"><span data-stu-id="5fdfa-107">**Error ID:** BC36563</span></span>

## <a name="see-also"></a><span data-ttu-id="5fdfa-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="5fdfa-108">See also</span></span>

- [<span data-ttu-id="5fdfa-109">AddressOf 运算符</span><span class="sxs-lookup"><span data-stu-id="5fdfa-109">AddressOf Operator</span></span>](../operators/addressof-operator.md)
- [<span data-ttu-id="5fdfa-110">Delegate 语句</span><span class="sxs-lookup"><span data-stu-id="5fdfa-110">Delegate Statement</span></span>](../statements/delegate-statement.md)
- [<span data-ttu-id="5fdfa-111">重载决策</span><span class="sxs-lookup"><span data-stu-id="5fdfa-111">Overload Resolution</span></span>](../../programming-guide/language-features/procedures/overload-resolution.md)
- [<span data-ttu-id="5fdfa-112">Generic Types in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5fdfa-112">Generic Types in Visual Basic</span></span>](../../programming-guide/language-features/data-types/generic-types.md)
