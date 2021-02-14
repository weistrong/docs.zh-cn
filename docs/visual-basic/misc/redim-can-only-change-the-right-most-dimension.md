---
description: 了解详细信息： "ReDim" 只能更改最右边的维度
title: “ReDim”只能更改最右边的维度
ms.date: 07/20/2015
f1_keywords:
- vbrArray_TypeMismatch
ms.assetid: d53cf41b-7a7a-466c-a29a-920d99698fa9
ms.openlocfilehash: 6816e5b2e9c7c079b78ce53e168f46b337831512
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100454685"
---
# <a name="redim-can-only-change-the-right-most-dimension"></a><span data-ttu-id="eda77-103">“ReDim”只能更改最右边的维度</span><span class="sxs-lookup"><span data-stu-id="eda77-103">'ReDim' can only change the right-most dimension</span></span>

<span data-ttu-id="eda77-104">`ReDim` 语句尝试使用 `Preserve` 关键字来更改一个数组的维度，它不是最后一个维度。</span><span class="sxs-lookup"><span data-stu-id="eda77-104">A `ReDim` statement attempted to use the `Preserve` keyword to change a dimension of an array that is not the last dimension.</span></span> <span data-ttu-id="eda77-105">使用 `Preserve`时，只能调整数组最后一个维度的大小。</span><span class="sxs-lookup"><span data-stu-id="eda77-105">When using `Preserve`, you can resize only the last dimension of an array.</span></span> <span data-ttu-id="eda77-106">对于其他所有维度，必须指定与现有数组相同的大小。</span><span class="sxs-lookup"><span data-stu-id="eda77-106">For all other dimensions, you must specify the same size as for the existing array.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="eda77-107">更正此错误</span><span class="sxs-lookup"><span data-stu-id="eda77-107">To correct this error</span></span>  
  
- <span data-ttu-id="eda77-108">删除 `Preserve` 关键字。</span><span class="sxs-lookup"><span data-stu-id="eda77-108">Remove the `Preserve` keyword.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eda77-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="eda77-109">See also</span></span>

- [<span data-ttu-id="eda77-110">Visual Basic 中的数组</span><span class="sxs-lookup"><span data-stu-id="eda77-110">Arrays in Visual Basic</span></span>](../programming-guide/language-features/arrays/index.md)
- [<span data-ttu-id="eda77-111">Visual Basic 中的数组维度</span><span class="sxs-lookup"><span data-stu-id="eda77-111">Array dimensions in Visual Basic</span></span>](../programming-guide/language-features/arrays/array-dimensions.md)
- [<span data-ttu-id="eda77-112">ReDim 语句</span><span class="sxs-lookup"><span data-stu-id="eda77-112">ReDim Statement</span></span>](../language-reference/statements/redim-statement.md)
- [<span data-ttu-id="eda77-113">Dim 语句</span><span class="sxs-lookup"><span data-stu-id="eda77-113">Dim Statement</span></span>](../language-reference/statements/dim-statement.md)
