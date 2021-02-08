---
description: 了解详细信息： BC30202：应为 "Optional"
title: 需要“Optional”
ms.date: 07/20/2015
f1_keywords:
- bc30202
- vbc30202
helpviewer_keywords:
- BC30202
ms.assetid: 6f75060c-2db4-4a79-b5d1-5780c09a74cd
ms.openlocfilehash: 543dbf6226d4d298d46764ee506b55e770c91604
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795542"
---
# <a name="bc30202-optional-expected"></a><span data-ttu-id="31c33-103">BC30202：应为 "Optional"</span><span class="sxs-lookup"><span data-stu-id="31c33-103">BC30202: 'Optional' expected</span></span>

<span data-ttu-id="31c33-104">过程声明中的可选参数后跟必需的参数。</span><span class="sxs-lookup"><span data-stu-id="31c33-104">An optional argument in a procedure declaration is followed by a required argument.</span></span> <span data-ttu-id="31c33-105">可选参数后面的每个参数都必须是可选的。</span><span class="sxs-lookup"><span data-stu-id="31c33-105">Every argument following an optional argument must also be optional.</span></span>

 <span data-ttu-id="31c33-106">**错误 ID：** BC30202</span><span class="sxs-lookup"><span data-stu-id="31c33-106">**Error ID:** BC30202</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="31c33-107">更正此错误</span><span class="sxs-lookup"><span data-stu-id="31c33-107">To correct this error</span></span>

- <span data-ttu-id="31c33-108">如果需要参数，请将其移动到自变量列表中的第一个可选参数之前。</span><span class="sxs-lookup"><span data-stu-id="31c33-108">If the argument is intended to be required, move it to precede the first optional argument in the argument list.</span></span>

- <span data-ttu-id="31c33-109">如果参数旨在作为可选参数，请使用 `Optional` 关键字。</span><span class="sxs-lookup"><span data-stu-id="31c33-109">If the argument is intended to be optional, use the `Optional` keyword.</span></span>

## <a name="see-also"></a><span data-ttu-id="31c33-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="31c33-110">See also</span></span>

- [<span data-ttu-id="31c33-111">可选参数</span><span class="sxs-lookup"><span data-stu-id="31c33-111">Optional Parameters</span></span>](../../programming-guide/language-features/procedures/optional-parameters.md)
