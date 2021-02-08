---
description: '了解详细信息： Erase 语句 (Visual Basic) '
title: Erase 语句
ms.date: 07/20/2015
f1_keywords:
- vb.Erase
helpviewer_keywords:
- Erase keyword [Visual Basic]
- Erase statement [Visual Basic]
ms.assetid: 7a8133d7-b750-4d74-8b66-ba1dd9778d4b
ms.openlocfilehash: 295abec89f3d69f8f2641a5a3d574a2d10f98474
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99769151"
---
# <a name="erase-statement-visual-basic"></a><span data-ttu-id="40c38-103">Erase 语句 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="40c38-103">Erase Statement (Visual Basic)</span></span>

<span data-ttu-id="40c38-104">用于释放数组变量并解除分配用于其元素的内存。</span><span class="sxs-lookup"><span data-stu-id="40c38-104">Used to release array variables and deallocate the memory used for their elements.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="40c38-105">语法</span><span class="sxs-lookup"><span data-stu-id="40c38-105">Syntax</span></span>  
  
```vb  
Erase arraylist  
```  
  
## <a name="parts"></a><span data-ttu-id="40c38-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="40c38-106">Parts</span></span>  

 `arraylist`  
 <span data-ttu-id="40c38-107">必需。</span><span class="sxs-lookup"><span data-stu-id="40c38-107">Required.</span></span> <span data-ttu-id="40c38-108">要清除的数组变量的列表。</span><span class="sxs-lookup"><span data-stu-id="40c38-108">List of array variables to be erased.</span></span> <span data-ttu-id="40c38-109">以逗号分隔多个变量。</span><span class="sxs-lookup"><span data-stu-id="40c38-109">Multiple variables are separated by commas.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="40c38-110">备注</span><span class="sxs-lookup"><span data-stu-id="40c38-110">Remarks</span></span>  

 <span data-ttu-id="40c38-111">`Erase`语句只能出现在过程级别。</span><span class="sxs-lookup"><span data-stu-id="40c38-111">The `Erase` statement can appear only at procedure level.</span></span> <span data-ttu-id="40c38-112">这意味着，可以在过程中释放数组，但不能在类或模块级别进行。</span><span class="sxs-lookup"><span data-stu-id="40c38-112">This means you can release arrays inside a procedure but not at class or module level.</span></span>  
  
 <span data-ttu-id="40c38-113">`Erase`语句等效于分配 `Nothing` 给每个数组变量。</span><span class="sxs-lookup"><span data-stu-id="40c38-113">The `Erase` statement is equivalent to assigning `Nothing` to each array variable.</span></span>  
  
## <a name="example"></a><span data-ttu-id="40c38-114">示例</span><span class="sxs-lookup"><span data-stu-id="40c38-114">Example</span></span>  

 <span data-ttu-id="40c38-115">下面的示例使用 `Erase` 语句来清除两个数组，并分别)  (1000 和100存储元素的内存。</span><span class="sxs-lookup"><span data-stu-id="40c38-115">The following example uses the `Erase` statement to clear two arrays and free their memory (1000 and 100 storage elements, respectively).</span></span> <span data-ttu-id="40c38-116">`ReDim`然后，语句将新的数组实例赋给三维数组。</span><span class="sxs-lookup"><span data-stu-id="40c38-116">The `ReDim` statement then assigns a new array instance to the three-dimensional array.</span></span>  
  
 [!code-vb[VbVbalrStatements#19](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#19)]  
  
## <a name="see-also"></a><span data-ttu-id="40c38-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="40c38-117">See also</span></span>

- [<span data-ttu-id="40c38-118">Nothing</span><span class="sxs-lookup"><span data-stu-id="40c38-118">Nothing</span></span>](../nothing.md)
- [<span data-ttu-id="40c38-119">ReDim 语句</span><span class="sxs-lookup"><span data-stu-id="40c38-119">ReDim Statement</span></span>](redim-statement.md)
