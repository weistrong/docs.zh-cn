---
description: 了解详细信息： BC30188：需要声明
title: 需要声明
ms.date: 07/20/2015
f1_keywords:
- vbc30188
- bc30188
helpviewer_keywords:
- BC30188
ms.assetid: da6b1df3-fe6b-4415-88e6-0977e5189e0b
ms.openlocfilehash: b86c182fb9dc8ab7d624833136f0e87b072aed92
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796660"
---
# <a name="bc30188-declaration-expected"></a><span data-ttu-id="8561a-103">BC30188：应为声明</span><span class="sxs-lookup"><span data-stu-id="8561a-103">BC30188: Declaration expected</span></span>

<span data-ttu-id="8561a-104">Nondeclarative 语句，如赋值语句或循环语句，在任何过程外发生。</span><span class="sxs-lookup"><span data-stu-id="8561a-104">A nondeclarative statement, such as an assignment or loop statement, occurs outside any procedure.</span></span> <span data-ttu-id="8561a-105">仅允许在过程外使用声明。</span><span class="sxs-lookup"><span data-stu-id="8561a-105">Only declarations are allowed outside procedures.</span></span>

 <span data-ttu-id="8561a-106">或者，在没有声明关键字（如或）的情况下声明编程元素 `Dim` `Const` 。</span><span class="sxs-lookup"><span data-stu-id="8561a-106">Alternatively, a programming element is declared without a declaration keyword such as `Dim` or `Const`.</span></span>

 <span data-ttu-id="8561a-107">**错误 ID：** BC30188</span><span class="sxs-lookup"><span data-stu-id="8561a-107">**Error ID:** BC30188</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="8561a-108">更正此错误</span><span class="sxs-lookup"><span data-stu-id="8561a-108">To correct this error</span></span>

- <span data-ttu-id="8561a-109">将 nondeclarative 语句移到过程的主体。</span><span class="sxs-lookup"><span data-stu-id="8561a-109">Move the nondeclarative statement to the body of a procedure.</span></span>

- <span data-ttu-id="8561a-110">使用适当的声明关键字开始声明。</span><span class="sxs-lookup"><span data-stu-id="8561a-110">Begin the declaration with an appropriate declaration keyword.</span></span>

- <span data-ttu-id="8561a-111">确保声明关键字没有拼写错误。</span><span class="sxs-lookup"><span data-stu-id="8561a-111">Ensure that a declaration keyword is not misspelled.</span></span>

## <a name="see-also"></a><span data-ttu-id="8561a-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="8561a-112">See also</span></span>

- [<span data-ttu-id="8561a-113">过程</span><span class="sxs-lookup"><span data-stu-id="8561a-113">Procedures</span></span>](../../programming-guide/language-features/procedures/index.md)
- [<span data-ttu-id="8561a-114">Dim 语句</span><span class="sxs-lookup"><span data-stu-id="8561a-114">Dim Statement</span></span>](../statements/dim-statement.md)
