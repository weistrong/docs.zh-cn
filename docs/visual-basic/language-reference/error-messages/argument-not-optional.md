---
description: '了解详细信息：参数 not optional (Visual Basic) '
title: 自变量不可选
ms.date: 07/20/2015
f1_keywords:
- vbrID449
ms.assetid: 76e7bcf3-24ed-4cd5-945b-b98f1c76944b
ms.openlocfilehash: 3683f07174b980f6ceebf42151658a5be4615310
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797154"
---
# <a name="argument-not-optional-visual-basic"></a><span data-ttu-id="f788f-103">非可选自变量 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f788f-103">Argument not optional (Visual Basic)</span></span>

<span data-ttu-id="f788f-104">参数的数量和类型必须与需要的参数匹配。</span><span class="sxs-lookup"><span data-stu-id="f788f-104">The number and types of arguments must match those expected.</span></span> <span data-ttu-id="f788f-105">参数的数目不正确，或者省略的参数不是可选的。</span><span class="sxs-lookup"><span data-stu-id="f788f-105">Either there is an incorrect number of arguments, or an omitted argument is not optional.</span></span> <span data-ttu-id="f788f-106">如果在过程定义中声明了某个参数，则只能通过对用户定义的过程的调用来省略此参数 `Optional` 。</span><span class="sxs-lookup"><span data-stu-id="f788f-106">An argument can only be omitted from a call to a user-defined procedure if it was declared `Optional` in the procedure definition.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="f788f-107">更正此错误</span><span class="sxs-lookup"><span data-stu-id="f788f-107">To correct this error</span></span>  
  
1. <span data-ttu-id="f788f-108">提供所有必需的参数。</span><span class="sxs-lookup"><span data-stu-id="f788f-108">Supply all necessary arguments.</span></span>  
  
2. <span data-ttu-id="f788f-109">请确保省略的参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="f788f-109">Make sure omitted arguments are optional.</span></span> <span data-ttu-id="f788f-110">如果不是，则在调用中提供参数，或在定义中声明参数 `Optional` 。</span><span class="sxs-lookup"><span data-stu-id="f788f-110">If they are not, either supply the argument in the call, or declare the parameter `Optional` in the definition.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f788f-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="f788f-111">See also</span></span>

- [<span data-ttu-id="f788f-112">错误类型</span><span class="sxs-lookup"><span data-stu-id="f788f-112">Error Types</span></span>](../../programming-guide/language-features/error-types.md)
