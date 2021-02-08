---
description: 了解详细信息：序数无效
title: 序号无效
ms.date: 07/20/2015
f1_keywords:
- vbrID452
ms.assetid: 7459562b-cd4f-4590-95e0-6126ae3589a5
ms.openlocfilehash: 7c58675a08d3821cd05ba0109e5ce0107c68e497
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795516"
---
# <a name="ordinal-is-not-valid"></a><span data-ttu-id="13f6f-103">序号无效</span><span class="sxs-lookup"><span data-stu-id="13f6f-103">Ordinal is not valid</span></span>

<span data-ttu-id="13f6f-104">对动态链接库的调用 (DLL) 指示使用语法，而不是过程名称 `#num` 。</span><span class="sxs-lookup"><span data-stu-id="13f6f-104">Your call to a dynamic-link library (DLL) indicated to use a number instead of a procedure name, using the `#num` syntax.</span></span> <span data-ttu-id="13f6f-105">此错误具有以下可能的原因：</span><span class="sxs-lookup"><span data-stu-id="13f6f-105">This error has the following possible causes:</span></span>  
  
- <span data-ttu-id="13f6f-106">尝试将 `#num` 表达式转换为序号失败。</span><span class="sxs-lookup"><span data-stu-id="13f6f-106">An attempt to convert the `#num` expression to an ordinal failed.</span></span>  
  
- <span data-ttu-id="13f6f-107">指定的不 `#num` 指定 DLL 中的任何函数。</span><span class="sxs-lookup"><span data-stu-id="13f6f-107">The `#num` specified does not specify any function in the DLL.</span></span>  
  
- <span data-ttu-id="13f6f-108">类型库具有无效的声明，导致内部使用的序号无效。</span><span class="sxs-lookup"><span data-stu-id="13f6f-108">A type library has an invalid declaration resulting in internal use of an invalid ordinal number.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="13f6f-109">更正此错误</span><span class="sxs-lookup"><span data-stu-id="13f6f-109">To correct this error</span></span>  
  
1. <span data-ttu-id="13f6f-110">请确保表达式表示有效数字，或按名称调用该过程。</span><span class="sxs-lookup"><span data-stu-id="13f6f-110">Make sure the expression represents a valid number, or call the procedure by name.</span></span>  
  
2. <span data-ttu-id="13f6f-111">请确保 `#num` 在 DLL 中标识有效函数。</span><span class="sxs-lookup"><span data-stu-id="13f6f-111">Make sure `#num` identifies a valid function in the DLL.</span></span>  
  
3. <span data-ttu-id="13f6f-112">通过注释掉代码，隔离导致问题的过程调用。</span><span class="sxs-lookup"><span data-stu-id="13f6f-112">Isolate the procedure call causing the problem by commenting out the code.</span></span> <span data-ttu-id="13f6f-113">`Declare`为过程编写语句，并将问题报告给类型库供应商。</span><span class="sxs-lookup"><span data-stu-id="13f6f-113">Write a `Declare` statement for the procedure, and report the problem to the type library vendor.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="13f6f-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="13f6f-114">See also</span></span>

- [<span data-ttu-id="13f6f-115">Declare Statement</span><span class="sxs-lookup"><span data-stu-id="13f6f-115">Declare Statement</span></span>](../statements/declare-statement.md)
