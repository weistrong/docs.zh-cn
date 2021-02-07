---
description: 了解更多相关信息： BC42104：变量 " <variablename> " 在赋值前已被使用
title: 变量“<variablename>”在赋值前被使用
ms.date: 07/20/2015
f1_keywords:
- vbc42104
- BC42104
helpviewer_keywords:
- BC42104
ms.assetid: 6909aa0b-b4a1-46f5-a18c-ba3e565c1dd8
ms.openlocfilehash: 501c3e3971c5ca0ebdba6981134f5029b77d0075
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99701490"
---
# <a name="bc42104-variable-variablename-is-used-before-it-has-been-assigned-a-value"></a><span data-ttu-id="aa29e-103">BC42104：变量 " \<variablename> " 在赋值前被使用</span><span class="sxs-lookup"><span data-stu-id="aa29e-103">BC42104: Variable '\<variablename>' is used before it has been assigned a value</span></span>

<span data-ttu-id="aa29e-104">变量 " \<variablename> " 在赋值前被使用。</span><span class="sxs-lookup"><span data-stu-id="aa29e-104">Variable '\<variablename>' is used before it has been assigned a value.</span></span> <span data-ttu-id="aa29e-105">可能在运行时导致 null 引用异常。</span><span class="sxs-lookup"><span data-stu-id="aa29e-105">A null reference exception could result at run time.</span></span>

 <span data-ttu-id="aa29e-106">应用程序在其代码上至少有一个可能的路径，该路径将在分配任何值之前读取该变量。</span><span class="sxs-lookup"><span data-stu-id="aa29e-106">An application has at least one possible path through its code that reads a variable before any value is assigned to it.</span></span>

 <span data-ttu-id="aa29e-107">如果从未为变量赋值，则它保持其数据类型的默认值。</span><span class="sxs-lookup"><span data-stu-id="aa29e-107">If a variable has never been assigned a value, it holds the default value for its data type.</span></span> <span data-ttu-id="aa29e-108">对于引用数据类型，默认值是 [Nothing](../nothing.md)。</span><span class="sxs-lookup"><span data-stu-id="aa29e-108">For a reference data type, that default value is [Nothing](../nothing.md).</span></span> <span data-ttu-id="aa29e-109">在某些情况下，读取具有 `Nothing` 值的引用变量可能导致 <xref:System.NullReferenceException> 。</span><span class="sxs-lookup"><span data-stu-id="aa29e-109">Reading a reference variable that has a value of `Nothing` can cause a <xref:System.NullReferenceException> in some circumstances.</span></span>

 <span data-ttu-id="aa29e-110">默认情况下，此消息是一个警告。</span><span class="sxs-lookup"><span data-stu-id="aa29e-110">By default, this message is a warning.</span></span> <span data-ttu-id="aa29e-111">有关隐藏警告或将警告视为错误的详细信息，请参见 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)。</span><span class="sxs-lookup"><span data-stu-id="aa29e-111">For more information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>

 <span data-ttu-id="aa29e-112">**错误 ID：** BC42104</span><span class="sxs-lookup"><span data-stu-id="aa29e-112">**Error ID:** BC42104</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="aa29e-113">更正此错误</span><span class="sxs-lookup"><span data-stu-id="aa29e-113">To correct this error</span></span>

- <span data-ttu-id="aa29e-114">检查控制流逻辑，并确保在控制传递到读取它的任何语句之前，该变量具有一个有效的值。</span><span class="sxs-lookup"><span data-stu-id="aa29e-114">Check your control flow logic and make sure the variable has a valid value before control passes to any statement that reads it.</span></span>

- <span data-ttu-id="aa29e-115">保证变量始终具有有效值的一种方法是将其初始化为其声明的一部分。</span><span class="sxs-lookup"><span data-stu-id="aa29e-115">One way to guarantee that the variable always has a valid value is to initialize it as part of its declaration.</span></span> <span data-ttu-id="aa29e-116">请参阅 [Dim 语句](../statements/dim-statement.md)中的 "初始化"。</span><span class="sxs-lookup"><span data-stu-id="aa29e-116">See "Initialization" in [Dim Statement](../statements/dim-statement.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="aa29e-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="aa29e-117">See also</span></span>

- [<span data-ttu-id="aa29e-118">Dim 语句</span><span class="sxs-lookup"><span data-stu-id="aa29e-118">Dim Statement</span></span>](../statements/dim-statement.md)
- [<span data-ttu-id="aa29e-119">变量声明</span><span class="sxs-lookup"><span data-stu-id="aa29e-119">Variable Declaration</span></span>](../../programming-guide/language-features/variables/variable-declaration.md)
- [<span data-ttu-id="aa29e-120">变量疑难解答</span><span class="sxs-lookup"><span data-stu-id="aa29e-120">Troubleshooting Variables</span></span>](../../programming-guide/language-features/variables/troubleshooting-variables.md)
