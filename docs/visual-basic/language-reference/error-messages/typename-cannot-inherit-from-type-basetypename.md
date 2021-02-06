---
description: 了解有关以下内容的详细信息： BC30910： " <typename> " 不能从 <type> "" 继承， <basetypename> 因为它将对基的访问扩展到 <type> 程序集的外部
title: “<typename>”将对基 <type> 的访问扩展到程序集的外部，因此无法从 <basetypename>“<type>”继承
ms.date: 07/20/2015
f1_keywords:
- vbc30910
- bc30910
helpviewer_keywords:
- BC30910
ms.assetid: 68fc05c5-5d55-4742-9a3b-ea04312594f4
ms.openlocfilehash: 332bfcbe9345f03605d6e1d6ded4a3e931ed491f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99641091"
---
# <a name="bc30910-typename-cannot-inherit-from-type-basetypename-because-it-expands-the-access-of-the-base-type-outside-the-assembly"></a><span data-ttu-id="ae1c3-103">BC30910： " \<typename> " 不能从 \<type> " \<basetypename> " 继承，因为它将对基的访问扩展到 \<type> 程序集的外部</span><span class="sxs-lookup"><span data-stu-id="ae1c3-103">BC30910: '\<typename>' cannot inherit from \<type> '\<basetypename>' because it expands the access of the base \<type> outside the assembly</span></span>

<span data-ttu-id="ae1c3-104">类或接口继承自基类或接口，但具有限制性较低的访问级别。</span><span class="sxs-lookup"><span data-stu-id="ae1c3-104">A class or interface inherits from a base class or interface but has a less restrictive access level.</span></span>

 <span data-ttu-id="ae1c3-105">例如， `Public` 接口从 `Friend` 接口继承，或 `Protected` 从 `Private` 类继承。</span><span class="sxs-lookup"><span data-stu-id="ae1c3-105">For example, a `Public` interface inherits from a `Friend` interface, or a `Protected` class inherits from a `Private` class.</span></span> <span data-ttu-id="ae1c3-106">这会公开要访问的基类或接口超出目标级别。</span><span class="sxs-lookup"><span data-stu-id="ae1c3-106">This exposes the base class or interface to access beyond the intended level.</span></span>

 <span data-ttu-id="ae1c3-107">**错误 ID：** BC30910</span><span class="sxs-lookup"><span data-stu-id="ae1c3-107">**Error ID:** BC30910</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="ae1c3-108">更正此错误</span><span class="sxs-lookup"><span data-stu-id="ae1c3-108">To correct this error</span></span>

- <span data-ttu-id="ae1c3-109">更改派生类或接口的访问级别，使其至少与基类或接口的访问级别具有相同的限制。</span><span class="sxs-lookup"><span data-stu-id="ae1c3-109">Change the access level of the derived class or interface to be at least as restrictive as that of the base class or interface.</span></span>

     <span data-ttu-id="ae1c3-110">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="ae1c3-110">-or-</span></span>

- <span data-ttu-id="ae1c3-111">如果需要限制性较低的访问级别，请删除 `Inherits` 语句。</span><span class="sxs-lookup"><span data-stu-id="ae1c3-111">If you require the less restrictive access level, remove the `Inherits` statement.</span></span> <span data-ttu-id="ae1c3-112">不能从更受限制的基类或接口继承。</span><span class="sxs-lookup"><span data-stu-id="ae1c3-112">You cannot inherit from a more restricted base class or interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae1c3-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="ae1c3-113">See also</span></span>

- [<span data-ttu-id="ae1c3-114">Class 语句</span><span class="sxs-lookup"><span data-stu-id="ae1c3-114">Class Statement</span></span>](../statements/class-statement.md)
- [<span data-ttu-id="ae1c3-115">Interface 语句</span><span class="sxs-lookup"><span data-stu-id="ae1c3-115">Interface Statement</span></span>](../statements/interface-statement.md)
- [<span data-ttu-id="ae1c3-116">Inherits Statement</span><span class="sxs-lookup"><span data-stu-id="ae1c3-116">Inherits Statement</span></span>](../statements/inherits-statement.md)
- [<span data-ttu-id="ae1c3-117">Visual Basic 中的访问级别</span><span class="sxs-lookup"><span data-stu-id="ae1c3-117">Access levels in Visual Basic</span></span>](../../programming-guide/language-features/declared-elements/access-levels.md)
