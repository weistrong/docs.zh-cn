---
description: '了解详细信息：此数组是固定的或临时锁定的 (Visual Basic) '
title: 此数组是固定数组或被临时锁定
ms.date: 07/20/2015
f1_keywords:
- vbrID10
ms.assetid: de6713a6-51d7-4edb-8515-d5fb544e2091
ms.openlocfilehash: 034bcc23055f7fb3f707e1105589a4526e6f9009
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99641208"
---
# <a name="this-array-is-fixed-or-temporarily-locked-visual-basic"></a><span data-ttu-id="a0030-103">此数组被固定或临时锁定 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a0030-103">This array is fixed or temporarily locked (Visual Basic)</span></span>

<span data-ttu-id="a0030-104">此错误具有以下可能的原因：</span><span class="sxs-lookup"><span data-stu-id="a0030-104">This error has the following possible causes:</span></span>  
  
- <span data-ttu-id="a0030-105">使用 `ReDim` 更改固定大小数组的元素数。</span><span class="sxs-lookup"><span data-stu-id="a0030-105">Using `ReDim` to change the number of elements of a fixed-size array.</span></span>  
  
- <span data-ttu-id="a0030-106">Redimensioning 模块级动态数组，其中一个元素已作为参数传递给过程。</span><span class="sxs-lookup"><span data-stu-id="a0030-106">Redimensioning a module-level dynamic array, in which one element has been passed as an argument to a procedure.</span></span> <span data-ttu-id="a0030-107">如果传递了某个元素，则会锁定数组，以防在过程中为引用参数释放内存。</span><span class="sxs-lookup"><span data-stu-id="a0030-107">If an element is passed, the array is locked to prevent deallocating memory for the reference parameter within the procedure.</span></span>  
  
- <span data-ttu-id="a0030-108">尝试向 `Variant` 包含数组的变量赋值，但 `Variant` 当前已锁定。</span><span class="sxs-lookup"><span data-stu-id="a0030-108">Attempting to assign a value to a `Variant` variable containing an array, but the `Variant` is currently locked.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="a0030-109">更正此错误</span><span class="sxs-lookup"><span data-stu-id="a0030-109">To correct this error</span></span>  
  
1. <span data-ttu-id="a0030-110">如果数组是在) 过程中声明的，则通过使用 (进行声明来使原始数组成为动态的（而不是固定的 `ReDim` ）; 或者，如果数组是在模块级别声明的，则通过在不指定元素数目的情况下声明，而不指定 (元素数</span><span class="sxs-lookup"><span data-stu-id="a0030-110">Make the original array dynamic rather than fixed by declaring it with `ReDim` (if the array is declared within a procedure), or by declaring it without specifying the number of elements (if the array is declared at the module level.</span></span>  
  
2. <span data-ttu-id="a0030-111">确定是否确实需要传递元素，因为它在模块中的所有过程中可见。</span><span class="sxs-lookup"><span data-stu-id="a0030-111">Determine whether you really need to pass the element, since it is visible within all procedures in the module.</span></span>  
  
3. <span data-ttu-id="a0030-112">确定锁定 `Variant` 和更正的内容。</span><span class="sxs-lookup"><span data-stu-id="a0030-112">Determine what is locking the `Variant` and remedy it.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a0030-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="a0030-113">See also</span></span>

- [<span data-ttu-id="a0030-114">数组</span><span class="sxs-lookup"><span data-stu-id="a0030-114">Arrays</span></span>](../../programming-guide/language-features/arrays/index.md)
