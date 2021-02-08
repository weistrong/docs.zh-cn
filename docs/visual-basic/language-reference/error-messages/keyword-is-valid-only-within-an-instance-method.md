---
description: 了解更多相关信息： BC30043： " <keyword> " 仅在实例方法中有效
title: “<keyword>”只在实例方法中有效
ms.date: 07/20/2015
f1_keywords:
- bc30043
- vbc30043
helpviewer_keywords:
- BC30043
ms.assetid: 7973aa82-a681-440c-9bca-242627d7ba86
ms.openlocfilehash: 0bca2df44e096da016c9cb0c2031a8ef6faeb2b0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795971"
---
# <a name="bc30043-keyword-is-valid-only-within-an-instance-method"></a><span data-ttu-id="81b62-103">BC30043： " \<keyword> " 仅在实例方法中有效</span><span class="sxs-lookup"><span data-stu-id="81b62-103">BC30043: '\<keyword>' is valid only within an instance method</span></span>

<span data-ttu-id="81b62-104">`Me`、 `MyClass` 和 `MyBase` 关键字引用特定的类实例。</span><span class="sxs-lookup"><span data-stu-id="81b62-104">The `Me`, `MyClass`, and `MyBase` keywords refer to specific class instances.</span></span> <span data-ttu-id="81b62-105">不能在共享或过程中使用它们 `Function` `Sub` 。</span><span class="sxs-lookup"><span data-stu-id="81b62-105">You cannot use them inside a shared `Function` or `Sub` procedure.</span></span>

<span data-ttu-id="81b62-106">*错误 ID：*\* BC30043</span><span class="sxs-lookup"><span data-stu-id="81b62-106">*Error ID:*\* BC30043</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="81b62-107">更正此错误</span><span class="sxs-lookup"><span data-stu-id="81b62-107">To correct this error</span></span>

- <span data-ttu-id="81b62-108">从过程中删除关键字，或 `Shared` 从过程声明中删除关键字。</span><span class="sxs-lookup"><span data-stu-id="81b62-108">Remove the keyword from the procedure, or remove the `Shared` keyword from the procedure declaration.</span></span>

## <a name="see-also"></a><span data-ttu-id="81b62-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="81b62-109">See also</span></span>

- [<span data-ttu-id="81b62-110">对象变量赋值</span><span class="sxs-lookup"><span data-stu-id="81b62-110">Object Variable Assignment</span></span>](../../programming-guide/language-features/variables/object-variable-assignment.md)
- [<span data-ttu-id="81b62-111">Me、My、MyBase 和 MyClass</span><span class="sxs-lookup"><span data-stu-id="81b62-111">Me, My, MyBase, and MyClass</span></span>](../../programming-guide/program-structure/me-my-mybase-and-myclass.md)
- [<span data-ttu-id="81b62-112">继承基础知识</span><span class="sxs-lookup"><span data-stu-id="81b62-112">Inheritance Basics</span></span>](../../programming-guide/language-features/objects-and-classes/inheritance-basics.md)
