---
description: '了解有关详细信息，请参阅如何：控制变量 (Visual Basic 的可用性) '
title: 如何：控制变量的可用性
ms.date: 07/20/2015
helpviewer_keywords:
- access levels, declared elements
- Private keyword [Visual Basic], accessing variables
- access levels, variables
- Public keyword [Visual Basic], accessing variables
- Friend keyword [Visual Basic], accessing variables
- variables [Visual Basic], access level
- declared elements [Visual Basic], access level
- Protected keyword [Visual Basic], accessing variables
ms.assetid: eaf4f073-7922-43ce-ae1e-90ff376ae947
ms.openlocfilehash: 3fa21a804008f31da9003aa847752f749154d602
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100429879"
---
# <a name="how-to-control-the-availability-of-a-variable-visual-basic"></a><span data-ttu-id="f9265-103">如何：控制变量的可用性 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f9265-103">How to: Control the Availability of a Variable (Visual Basic)</span></span>

<span data-ttu-id="f9265-104">可以通过指定变量的 *访问级别* 来控制变量的可用性。</span><span class="sxs-lookup"><span data-stu-id="f9265-104">You control the availability of a variable by specifying its *access level*.</span></span> <span data-ttu-id="f9265-105">访问级别确定哪些代码有权读取或写入变量。</span><span class="sxs-lookup"><span data-stu-id="f9265-105">The access level determines what code has permission to read or write to the variable.</span></span>  
  
- <span data-ttu-id="f9265-106">*成员变量* (在模块级和任何过程外部定义) 默认为公共访问权限，这意味着可查看它们的任何代码都可以访问这些变量。</span><span class="sxs-lookup"><span data-stu-id="f9265-106">*Member variables* (defined at module level and outside any procedure) default to public access, which means any code that can see them can access them.</span></span> <span data-ttu-id="f9265-107">可以通过指定访问修饰符来更改此。</span><span class="sxs-lookup"><span data-stu-id="f9265-107">You can change this by specifying an access modifier.</span></span>  
  
- <span data-ttu-id="f9265-108"> (在过程中定义的 *本地变量*) 通常具有公共访问权限，但只有其过程中的代码可以访问它们。</span><span class="sxs-lookup"><span data-stu-id="f9265-108">*Local variables* (defined inside a procedure) nominally have public access, although only code within their procedure can access them.</span></span> <span data-ttu-id="f9265-109">不能更改本地变量的访问级别，但可以更改包含它的过程的访问级别。</span><span class="sxs-lookup"><span data-stu-id="f9265-109">You cannot change the access level of a local variable, but you can change the access level of the procedure that contains it.</span></span>  
  
 <span data-ttu-id="f9265-110">有关详细信息，请参阅 [Visual Basic 中的访问级别](access-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="f9265-110">For more information, see [Access levels in Visual Basic](access-levels.md).</span></span>  
  
## <a name="private-and-public-access"></a><span data-ttu-id="f9265-111">私有和公共访问</span><span class="sxs-lookup"><span data-stu-id="f9265-111">Private and Public Access</span></span>  
  
#### <a name="to-make-a-variable-accessible-only-from-within-its-module-class-or-structure"></a><span data-ttu-id="f9265-112">仅允许从其模块、类或结构内部访问变量</span><span class="sxs-lookup"><span data-stu-id="f9265-112">To make a variable accessible only from within its module, class, or structure</span></span>  
  
1. <span data-ttu-id="f9265-113">将变量的 [Dim 语句](../../../language-reference/statements/dim-statement.md) 放入模块、类或结构中，但放在任何过程之外。</span><span class="sxs-lookup"><span data-stu-id="f9265-113">Place the [Dim Statement](../../../language-reference/statements/dim-statement.md) for the variable inside the module, class, or structure, but outside any procedure.</span></span>  
  
2. <span data-ttu-id="f9265-114">在语句中包含 [Private](../../../language-reference/modifiers/private.md) 关键字 `Dim` 。</span><span class="sxs-lookup"><span data-stu-id="f9265-114">Include the [Private](../../../language-reference/modifiers/private.md) keyword in the `Dim` statement.</span></span>  
  
     <span data-ttu-id="f9265-115">可以从模块、类或结构中的任何位置读取或写入变量，但不能从外部读取或写入。</span><span class="sxs-lookup"><span data-stu-id="f9265-115">You can read or write to the variable from anywhere within the module, class, or structure, but not from outside it.</span></span>  
  
#### <a name="to-make-a-variable-accessible-from-any-code-that-can-see-it"></a><span data-ttu-id="f9265-116">使变量可从可查看它的任何代码进行访问</span><span class="sxs-lookup"><span data-stu-id="f9265-116">To make a variable accessible from any code that can see it</span></span>  
  
1. <span data-ttu-id="f9265-117">对于成员变量，请将 `Dim` 变量的语句放置在模块、类或结构中，但放在任何过程之外。</span><span class="sxs-lookup"><span data-stu-id="f9265-117">For a member variable, place the `Dim` statement for the variable inside a module, class, or structure, but outside any procedure.</span></span>  
  
2. <span data-ttu-id="f9265-118">在语句中包含 [Public](../../../language-reference/modifiers/public.md) 关键字 `Dim` 。</span><span class="sxs-lookup"><span data-stu-id="f9265-118">Include the [Public](../../../language-reference/modifiers/public.md) keyword in the `Dim` statement.</span></span>  
  
     <span data-ttu-id="f9265-119">可以从与程序集互操作的任何代码读取或写入变量。</span><span class="sxs-lookup"><span data-stu-id="f9265-119">You can read or write to the variable from any code that interoperates with your assembly.</span></span>  
  
 <span data-ttu-id="f9265-120">- 或 -</span><span class="sxs-lookup"><span data-stu-id="f9265-120">-or-</span></span>  
  
1. <span data-ttu-id="f9265-121">对于局部变量，请将变量的 `Dim` 语句放置到过程内。</span><span class="sxs-lookup"><span data-stu-id="f9265-121">For a local variable, place the `Dim` statement for the variable inside a procedure.</span></span>  
  
2. <span data-ttu-id="f9265-122">不要 `Public` 在语句中包含关键字 `Dim` 。</span><span class="sxs-lookup"><span data-stu-id="f9265-122">Do not include the `Public` keyword in the `Dim` statement.</span></span>  
  
     <span data-ttu-id="f9265-123">可以从过程中的任何位置读取或写入变量，但不能从外部读取或写入。</span><span class="sxs-lookup"><span data-stu-id="f9265-123">You can read or write to the variable from anywhere within the procedure, but not from outside it.</span></span>  
  
## <a name="protected-and-friend-access"></a><span data-ttu-id="f9265-124">受保护和友元访问</span><span class="sxs-lookup"><span data-stu-id="f9265-124">Protected and Friend Access</span></span>  

 <span data-ttu-id="f9265-125">可以将变量的访问级别限制为其类和派生类，或限制为其程序集。</span><span class="sxs-lookup"><span data-stu-id="f9265-125">You can limit the access level of a variable to its class and any derived classes, or to its assembly.</span></span> <span data-ttu-id="f9265-126">您还可以指定这些限制的联合，这允许从任何派生类中的代码或同一程序集中的任何其他位置进行访问。</span><span class="sxs-lookup"><span data-stu-id="f9265-126">You can also specify the union of these limitations, which allows access from code in any derived class or in any other place in the same assembly.</span></span> <span data-ttu-id="f9265-127">通过组合 `Protected` 同一声明中的和关键字来指定此联合 `Friend` 。</span><span class="sxs-lookup"><span data-stu-id="f9265-127">You specify this union by combining the `Protected` and `Friend` keywords in the same declaration.</span></span>  
  
#### <a name="to-make-a-variable-accessible-only-from-within-its-class-and-any-derived-classes"></a><span data-ttu-id="f9265-128">使变量只能从其类和任何派生类中访问</span><span class="sxs-lookup"><span data-stu-id="f9265-128">To make a variable accessible only from within its class and any derived classes</span></span>  
  
1. <span data-ttu-id="f9265-129">将 `Dim` 变量的语句放置在类中，但将其放置在任何过程之外。</span><span class="sxs-lookup"><span data-stu-id="f9265-129">Place the `Dim` statement for the variable inside a class, but outside any procedure.</span></span>  
  
2. <span data-ttu-id="f9265-130">在语句中包含 [Protected](../../../language-reference/modifiers/protected.md) 关键字 `Dim` 。</span><span class="sxs-lookup"><span data-stu-id="f9265-130">Include the [Protected](../../../language-reference/modifiers/protected.md) keyword in the `Dim` statement.</span></span>  
  
     <span data-ttu-id="f9265-131">可以从类中的任何位置以及从派生的任何类（而不是从派生链中的任何类）读取或写入变量。</span><span class="sxs-lookup"><span data-stu-id="f9265-131">You can read or write to the variable from anywhere within the class, as well as from within any class derived from it, but not from outside any class in the derivation chain.</span></span>  
  
#### <a name="to-make-a-variable-accessible-only-from-within-the-same-assembly"></a><span data-ttu-id="f9265-132">使变量只能从同一程序集内访问</span><span class="sxs-lookup"><span data-stu-id="f9265-132">To make a variable accessible only from within the same assembly</span></span>  
  
1. <span data-ttu-id="f9265-133">将变量的语句放入 `Dim` 模块、类或结构中，但放在任何过程之外。</span><span class="sxs-lookup"><span data-stu-id="f9265-133">Place the `Dim` statement for the variable inside a module, class, or structure, but outside any procedure.</span></span>  
  
2. <span data-ttu-id="f9265-134">在语句中包含 [Friend](../../../language-reference/modifiers/friend.md) 关键字 `Dim` 。</span><span class="sxs-lookup"><span data-stu-id="f9265-134">Include the [Friend](../../../language-reference/modifiers/friend.md) keyword in the `Dim` statement.</span></span>  
  
     <span data-ttu-id="f9265-135">你可以从模块、类或结构中的任何位置读取或写入变量，也可以从同一程序集中的任何代码读取或写入到程序集之外的任何代码。</span><span class="sxs-lookup"><span data-stu-id="f9265-135">You can read or write to the variable from anywhere within the module, class, or structure, as well as from any code in the same assembly, but not from outside the assembly.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f9265-136">示例</span><span class="sxs-lookup"><span data-stu-id="f9265-136">Example</span></span>  

 <span data-ttu-id="f9265-137">下面的示例演示具有 `Public` 、 `Protected` 、、 `Friend` `Protected Friend` 和 `Private` 访问级别的变量的声明。</span><span class="sxs-lookup"><span data-stu-id="f9265-137">The following example shows declarations of variables with `Public`, `Protected`, `Friend`, `Protected Friend`, and `Private` access levels.</span></span> <span data-ttu-id="f9265-138">请注意，如果 `Dim` 语句指定了访问级别，则不需要包括 `Dim` 关键字。</span><span class="sxs-lookup"><span data-stu-id="f9265-138">Note that when the `Dim` statement specifies an access level, you do not need to include the `Dim` keyword.</span></span>  
  
```vb  
Public Class classForEverybody  
Protected Class classForMyHeirs  
Friend stringForThisProject As String  
Protected Friend stringForProjectAndHeirs As String  
Private numberForMeOnly As Integer  
```  
  
## <a name="net-framework-security"></a><span data-ttu-id="f9265-139">.NET Framework 安全性</span><span class="sxs-lookup"><span data-stu-id="f9265-139">.NET Framework Security</span></span>  

 <span data-ttu-id="f9265-140">变量访问级别的限制性越多，恶意代码使用它的可能性就越小。</span><span class="sxs-lookup"><span data-stu-id="f9265-140">The more restrictive the access level of a variable, the smaller the chances that malicious code can make improper use of it.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f9265-141">请参阅</span><span class="sxs-lookup"><span data-stu-id="f9265-141">See also</span></span>

- [<span data-ttu-id="f9265-142">Visual Basic 中的访问级别</span><span class="sxs-lookup"><span data-stu-id="f9265-142">Access levels in Visual Basic</span></span>](access-levels.md)
- [<span data-ttu-id="f9265-143">Dim 语句</span><span class="sxs-lookup"><span data-stu-id="f9265-143">Dim Statement</span></span>](../../../language-reference/statements/dim-statement.md)
- [<span data-ttu-id="f9265-144">公共</span><span class="sxs-lookup"><span data-stu-id="f9265-144">Public</span></span>](../../../language-reference/modifiers/public.md)
- [<span data-ttu-id="f9265-145">Protected</span><span class="sxs-lookup"><span data-stu-id="f9265-145">Protected</span></span>](../../../language-reference/modifiers/protected.md)
- [<span data-ttu-id="f9265-146">Friend</span><span class="sxs-lookup"><span data-stu-id="f9265-146">Friend</span></span>](../../../language-reference/modifiers/friend.md)
- [<span data-ttu-id="f9265-147">专用</span><span class="sxs-lookup"><span data-stu-id="f9265-147">Private</span></span>](../../../language-reference/modifiers/private.md)
