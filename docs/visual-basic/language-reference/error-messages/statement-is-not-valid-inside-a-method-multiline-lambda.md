---
description: 了解详细信息： BC30024：语句在方法/多行 lambda 内无效
title: 语句在方法/多行 lambda 内无效
ms.date: 07/20/2015
f1_keywords:
- vbc30024
- bc30024
helpviewer_keywords:
- BC30024
ms.assetid: 758e7a8f-429b-42c1-9a78-778e5b480e04
ms.openlocfilehash: c70e5563ab8c161966cd9790ae1f192fa5d50b17
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99731170"
---
# <a name="bc30024-statement-is-not-valid-inside-a-methodmultiline-lambda"></a><span data-ttu-id="903bd-103">BC30024：语句在方法/多行 lambda 内无效</span><span class="sxs-lookup"><span data-stu-id="903bd-103">BC30024: Statement is not valid inside a method/multiline lambda</span></span>

<span data-ttu-id="903bd-104">语句在 `Sub` 、 `Function` 、属性 `Get` 或属性过程中无效 `Set` 。</span><span class="sxs-lookup"><span data-stu-id="903bd-104">The statement is not valid within a `Sub`, `Function`, property `Get`, or property `Set` procedure.</span></span> <span data-ttu-id="903bd-105">某些语句可以放置在模块或类级别。</span><span class="sxs-lookup"><span data-stu-id="903bd-105">Some statements can be placed at the module or class level.</span></span> <span data-ttu-id="903bd-106">其他类（如 `Option Strict` ）必须位于命名空间级别，并位于所有其他声明之前。</span><span class="sxs-lookup"><span data-stu-id="903bd-106">Others, such as `Option Strict`, must be at namespace level and precede all other declarations.</span></span>

 <span data-ttu-id="903bd-107">**错误 ID：** BC30024</span><span class="sxs-lookup"><span data-stu-id="903bd-107">**Error ID:** BC30024</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="903bd-108">更正此错误</span><span class="sxs-lookup"><span data-stu-id="903bd-108">To correct this error</span></span>

- <span data-ttu-id="903bd-109">删除过程中的语句。</span><span class="sxs-lookup"><span data-stu-id="903bd-109">Remove the statement from the procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="903bd-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="903bd-110">See also</span></span>

- [<span data-ttu-id="903bd-111">Sub 语句</span><span class="sxs-lookup"><span data-stu-id="903bd-111">Sub Statement</span></span>](../statements/sub-statement.md)
- [<span data-ttu-id="903bd-112">Function 语句</span><span class="sxs-lookup"><span data-stu-id="903bd-112">Function Statement</span></span>](../statements/function-statement.md)
- [<span data-ttu-id="903bd-113">Get 语句</span><span class="sxs-lookup"><span data-stu-id="903bd-113">Get Statement</span></span>](../statements/get-statement.md)
- [<span data-ttu-id="903bd-114">Set 语句</span><span class="sxs-lookup"><span data-stu-id="903bd-114">Set Statement</span></span>](../statements/set-statement.md)
