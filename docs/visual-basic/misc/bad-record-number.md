---
description: 了解详细信息：错误记录号
title: 错误的记录号
ms.date: 07/20/2015
f1_keywords:
- vbrID63
ms.assetid: 1fcc33f8-822a-4de9-a6e3-228ddb5824a6
ms.openlocfilehash: a250419c131f75381426705d52563732322631cb
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100460990"
---
# <a name="bad-record-number"></a><span data-ttu-id="c1c14-103">错误的记录号</span><span class="sxs-lookup"><span data-stu-id="c1c14-103">Bad record number</span></span>

<span data-ttu-id="c1c14-104">`a FileGet`、`FilePut``FileGetObject` 或 `FilePutObject` 语句中的记录号小于或等于零。</span><span class="sxs-lookup"><span data-stu-id="c1c14-104">The record number in `a FileGet`, `FilePut`, `FileGetObject`, or `FilePutObject` statement is less than or equal to zero.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="c1c14-105">更正此错误</span><span class="sxs-lookup"><span data-stu-id="c1c14-105">To correct this error</span></span>  
  
1. <span data-ttu-id="c1c14-106">检查用于生成记录号的计算。</span><span class="sxs-lookup"><span data-stu-id="c1c14-106">Check the calculations used in generating the record number.</span></span> <span data-ttu-id="c1c14-107">验证包含记录号或用于计算记录号的变量的拼写。</span><span class="sxs-lookup"><span data-stu-id="c1c14-107">Verify spelling of the variables containing the record number or used in calculating record numbers.</span></span> <span data-ttu-id="c1c14-108">拼写错误的变量名称将被隐式声明并初始化为零，除非在此模块中使用 `Option Explicit On` 。</span><span class="sxs-lookup"><span data-stu-id="c1c14-108">A misspelled variable name is implicitly declared and initialized to zero, unless you used `Option Explicit On` in the module.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c1c14-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="c1c14-109">See also</span></span>

- [<span data-ttu-id="c1c14-110">Option Explicit 语句</span><span class="sxs-lookup"><span data-stu-id="c1c14-110">Option Explicit Statement</span></span>](../language-reference/statements/option-explicit-statement.md)
