---
description: 了解更多：错误的 DLL 调用约定
title: 错误的 DLL 调用约定
ms.date: 07/20/2015
f1_keywords:
- vbrID49
ms.assetid: 7c7def45-b0ab-450f-ad3f-4383dfd9aed7
ms.openlocfilehash: 7e98ce5131d440a12bff4a4630da087102bdc4da
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797089"
---
# <a name="bad-dll-calling-convention"></a><span data-ttu-id="1cde3-103">错误的 DLL 调用约定</span><span class="sxs-lookup"><span data-stu-id="1cde3-103">Bad DLL calling convention</span></span>

<span data-ttu-id="1cde3-104">传递给动态链接库 (DLL) 的参数必须与例程所需的参数完全匹配。</span><span class="sxs-lookup"><span data-stu-id="1cde3-104">Arguments passed to a dynamic-link library (DLL) must exactly match those expected by the routine.</span></span> <span data-ttu-id="1cde3-105">调用约定涉及参数的数字、类型和顺序。</span><span class="sxs-lookup"><span data-stu-id="1cde3-105">Calling conventions deal with number, type, and order of arguments.</span></span> <span data-ttu-id="1cde3-106">程序可能正在传递错误类型或参数数目的 DLL 中的例程。</span><span class="sxs-lookup"><span data-stu-id="1cde3-106">Your program may be calling a routine in a DLL that is being passed the wrong type or number of arguments.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="1cde3-107">更正此错误</span><span class="sxs-lookup"><span data-stu-id="1cde3-107">To correct this error</span></span>  
  
1. <span data-ttu-id="1cde3-108">请确保所有参数类型都与你要调用的例程声明中指定的类型一致。</span><span class="sxs-lookup"><span data-stu-id="1cde3-108">Make sure all argument types agree with those specified in the declaration of the routine that you are calling.</span></span>  
  
2. <span data-ttu-id="1cde3-109">请确保传递的参数数目与要调用的例程声明中指定的参数数目相同。</span><span class="sxs-lookup"><span data-stu-id="1cde3-109">Make sure you are passing the same number of arguments indicated in the declaration of the routine that you are calling.</span></span>  
  
3. <span data-ttu-id="1cde3-110">如果 DLL 例程需要参数的值，请确保 `ByVal` 在例程的声明中为这些参数指定。</span><span class="sxs-lookup"><span data-stu-id="1cde3-110">If the DLL routine expects arguments by value, make sure `ByVal` is specified for those arguments in the declaration for the routine.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1cde3-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="1cde3-111">See also</span></span>

- [<span data-ttu-id="1cde3-112">错误类型</span><span class="sxs-lookup"><span data-stu-id="1cde3-112">Error Types</span></span>](../../programming-guide/language-features/error-types.md)
- [<span data-ttu-id="1cde3-113">Call 语句</span><span class="sxs-lookup"><span data-stu-id="1cde3-113">Call Statement</span></span>](../statements/call-statement.md)
- [<span data-ttu-id="1cde3-114">Declare Statement</span><span class="sxs-lookup"><span data-stu-id="1cde3-114">Declare Statement</span></span>](../statements/declare-statement.md)
