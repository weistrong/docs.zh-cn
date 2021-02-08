---
description: 了解有关：必须首先使用 "PathName" 参数调用 "Dir" 函数的详细信息
title: 必须首先用一个“PathName”自变量调用“Dir”函数
ms.date: 07/20/2015
f1_keywords:
- vbrDIR_IllegalCall
ms.assetid: 7b5d149f-be91-4ac3-8262-86a360894e7d
ms.openlocfilehash: ee492a269d41e8c9fe1fddbd59210b59fbe8618c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796582"
---
# <a name="dir-function-must-first-be-called-with-a-pathname-argument"></a><span data-ttu-id="21cdd-103">必须首先用一个“PathName”自变量调用“Dir”函数</span><span class="sxs-lookup"><span data-stu-id="21cdd-103">'Dir' function must first be called with a 'PathName' argument</span></span>

<span data-ttu-id="21cdd-104">对函数的初始调用 `Dir` 不包含 `PathName` 参数。</span><span class="sxs-lookup"><span data-stu-id="21cdd-104">An initial call to the `Dir` function does not include the `PathName` argument.</span></span> <span data-ttu-id="21cdd-105">对的第一次调用 `Dir` 必须包含 `PathName` ，但对的后续调用 `Dir` 不需要包含参数来检索下一项。</span><span class="sxs-lookup"><span data-stu-id="21cdd-105">The first call to `Dir` must include a `PathName`, but subsequent calls to `Dir` do not need to include parameters to retrieve the next item.</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="21cdd-106">更正此错误</span><span class="sxs-lookup"><span data-stu-id="21cdd-106">To correct this error</span></span>

- <span data-ttu-id="21cdd-107">`PathName`在函数调用中提供参数。</span><span class="sxs-lookup"><span data-stu-id="21cdd-107">Supply a `PathName` argument in the function call.</span></span>

## <a name="see-also"></a><span data-ttu-id="21cdd-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="21cdd-108">See also</span></span>

- <xref:Microsoft.VisualBasic.FileSystem.Dir%2A>
