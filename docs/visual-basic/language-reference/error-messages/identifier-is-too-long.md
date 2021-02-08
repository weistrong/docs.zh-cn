---
description: 了解详细信息： BC30033：标识符太长
title: 标识符太长
ms.date: 07/20/2015
f1_keywords:
- bc30033
- vbc30033
helpviewer_keywords:
- BC30033
ms.assetid: 3d07f6d0-9a2f-49ca-94e8-1e354932e855
ms.openlocfilehash: f2439c4bfc53f906fdc277b0de1faac0941c8808
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796088"
---
# <a name="bc30033-identifier-is-too-long"></a><span data-ttu-id="af342-103">BC30033：标识符太长</span><span class="sxs-lookup"><span data-stu-id="af342-103">BC30033: Identifier is too long</span></span>

<span data-ttu-id="af342-104">每个编程元素的名称或标识符限制为1023个字符。</span><span class="sxs-lookup"><span data-stu-id="af342-104">The name, or identifier, of every programming element is limited to 1023 characters.</span></span> <span data-ttu-id="af342-105">此外，完全限定的名称不能超过1023个字符。</span><span class="sxs-lookup"><span data-stu-id="af342-105">In addition, a fully qualified name cannot exceed 1023 characters.</span></span> <span data-ttu-id="af342-106">这意味着 () 的整个标识符字符串的 `<namespace>.<...>.<namespace>.<class>.<element>` 长度不能超过1023个字符，包括成员访问运算符 (`.`) 字符。</span><span class="sxs-lookup"><span data-stu-id="af342-106">This means that the entire identifier string (`<namespace>.<...>.<namespace>.<class>.<element>`) cannot be more than 1023 characters long, including the member-access operator (`.`) characters.</span></span>

 <span data-ttu-id="af342-107">**错误 ID：** BC30033</span><span class="sxs-lookup"><span data-stu-id="af342-107">**Error ID:** BC30033</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="af342-108">更正此错误</span><span class="sxs-lookup"><span data-stu-id="af342-108">To correct this error</span></span>

- <span data-ttu-id="af342-109">减小标识符的长度。</span><span class="sxs-lookup"><span data-stu-id="af342-109">Reduce the length of the identifier.</span></span>

## <a name="see-also"></a><span data-ttu-id="af342-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="af342-110">See also</span></span>

- [<span data-ttu-id="af342-111">Declared Element Names</span><span class="sxs-lookup"><span data-stu-id="af342-111">Declared Element Names</span></span>](../../programming-guide/language-features/declared-elements/declared-element-names.md)
