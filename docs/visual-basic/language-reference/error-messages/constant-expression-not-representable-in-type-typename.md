---
description: 了解有关以下内容的详细信息： BC30439：常量表达式无法在类型 "中表示<typename>
title: 常量表达式无法在类型“<typename>”中表示
ms.date: 07/20/2015
f1_keywords:
- bc30439
- vbc30439
helpviewer_keywords:
- BC30439
ms.assetid: 0a842906-3bc5-4946-8a37-3e3da883ef63
ms.openlocfilehash: 763ed8a414d8dda3e950ae85a4b1152a459518a5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796738"
---
# <a name="bc30439-constant-expression-not-representable-in-type-typename"></a><span data-ttu-id="4c6d9-103">BC30439：常量表达式无法在类型 "" 中表示 \<typename></span><span class="sxs-lookup"><span data-stu-id="4c6d9-103">BC30439: Constant expression not representable in type '\<typename>'</span></span>

<span data-ttu-id="4c6d9-104">你正在尝试评估将无法适应目标类型的常量，这通常是因为它溢出范围。</span><span class="sxs-lookup"><span data-stu-id="4c6d9-104">You are trying to evaluate a constant that will not fit into the target type, usually because it is overflowing the range.</span></span>

 <span data-ttu-id="4c6d9-105">**错误 ID：** BC30439</span><span class="sxs-lookup"><span data-stu-id="4c6d9-105">**Error ID:** BC30439</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="4c6d9-106">更正此错误</span><span class="sxs-lookup"><span data-stu-id="4c6d9-106">To correct this error</span></span>

1. <span data-ttu-id="4c6d9-107">将目标类型更改为可处理该常量的目标类型。</span><span class="sxs-lookup"><span data-stu-id="4c6d9-107">Change the target type to one that can handle the constant.</span></span>

## <a name="see-also"></a><span data-ttu-id="4c6d9-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="4c6d9-108">See also</span></span>

- [<span data-ttu-id="4c6d9-109">常量概述</span><span class="sxs-lookup"><span data-stu-id="4c6d9-109">Constants Overview</span></span>](../../programming-guide/language-features/constants-enums/constants-overview.md)
- [<span data-ttu-id="4c6d9-110">常量和枚举</span><span class="sxs-lookup"><span data-stu-id="4c6d9-110">Constants and Enumerations</span></span>](../constants-and-enumerations.md)
