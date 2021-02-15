---
description: 了解详细信息： BC30712：无法加载类 "" 的信息 <classname>
title: 无法加载类“<classname>”的信息
ms.date: 07/20/2015
f1_keywords:
- vbc30712
- bc30712
helpviewer_keywords:
- BC30712
ms.assetid: c7ffbd6d-05c6-4261-b44b-1bcd521bb350
ms.openlocfilehash: 5325afabfd267f15f0d0497be6ef03c8f5c828c0
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100480526"
---
# <a name="bc30712-unable-to-load-information-for-class-classname"></a><span data-ttu-id="2e481-103">BC30712：无法加载类 "" 的信息 \<classname></span><span class="sxs-lookup"><span data-stu-id="2e481-103">BC30712: Unable to load information for class '\<classname>'</span></span>

<span data-ttu-id="2e481-104">对不提供的类进行了引用。</span><span class="sxs-lookup"><span data-stu-id="2e481-104">A reference was made to a class that is not available.</span></span>

 <span data-ttu-id="2e481-105">**错误 ID：** BC30712</span><span class="sxs-lookup"><span data-stu-id="2e481-105">**Error ID:** BC30712</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="2e481-106">更正此错误</span><span class="sxs-lookup"><span data-stu-id="2e481-106">To correct this error</span></span>

1. <span data-ttu-id="2e481-107">验证是否定义了类，并且是否正确拼写了名称。</span><span class="sxs-lookup"><span data-stu-id="2e481-107">Verify that the class is defined and that you spelled the name correctly.</span></span>

2. <span data-ttu-id="2e481-108">尝试访问该模块中声明的其中一个成员。</span><span class="sxs-lookup"><span data-stu-id="2e481-108">Try accessing one of the members declared in the module.</span></span> <span data-ttu-id="2e481-109">在某些情况下，调试环境找不到成员，因为尚未加载在其中声明成员的模块。</span><span class="sxs-lookup"><span data-stu-id="2e481-109">In some cases, the debugging environment cannot locate members because the modules where they are declared have not been loaded yet.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e481-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="2e481-110">See also</span></span>

- [<span data-ttu-id="2e481-111">在 Visual Studio 中进行调试</span><span class="sxs-lookup"><span data-stu-id="2e481-111">Debugging in Visual Studio</span></span>](/visualstudio/debugger/debugger-feature-tour)
