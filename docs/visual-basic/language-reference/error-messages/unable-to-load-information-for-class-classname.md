---
description: 了解详细信息： BC30712：无法加载类的信息<classname>
title: 无法加载类“<classname>”的信息
ms.date: 07/20/2015
f1_keywords:
- vbc30712
- bc30712
helpviewer_keywords:
- BC30712
ms.assetid: c7ffbd6d-05c6-4261-b44b-1bcd521bb350
ms.openlocfilehash: 5e96df57b83b32b70a2d0d6eca1578b5d15ec065
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99674826"
---
# <a name="bc30712-unable-to-load-information-for-class-classname"></a><span data-ttu-id="dca6b-103">BC30712：无法加载类 "" 的信息 \<classname></span><span class="sxs-lookup"><span data-stu-id="dca6b-103">BC30712: Unable to load information for class '\<classname>'</span></span>

<span data-ttu-id="dca6b-104">对不提供的类进行了引用。</span><span class="sxs-lookup"><span data-stu-id="dca6b-104">A reference was made to a class that is not available.</span></span>

 <span data-ttu-id="dca6b-105">**错误 ID：** BC30712</span><span class="sxs-lookup"><span data-stu-id="dca6b-105">**Error ID:** BC30712</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="dca6b-106">更正此错误</span><span class="sxs-lookup"><span data-stu-id="dca6b-106">To correct this error</span></span>

1. <span data-ttu-id="dca6b-107">验证是否定义了类，并且是否正确拼写了名称。</span><span class="sxs-lookup"><span data-stu-id="dca6b-107">Verify that the class is defined and that you spelled the name correctly.</span></span>

2. <span data-ttu-id="dca6b-108">尝试访问该模块中声明的其中一个成员。</span><span class="sxs-lookup"><span data-stu-id="dca6b-108">Try accessing one of the members declared in the module.</span></span> <span data-ttu-id="dca6b-109">在某些情况下，调试环境找不到成员，因为尚未加载在其中声明成员的模块。</span><span class="sxs-lookup"><span data-stu-id="dca6b-109">In some cases, the debugging environment cannot locate members because the modules where they are declared have not been loaded yet.</span></span>

## <a name="see-also"></a><span data-ttu-id="dca6b-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="dca6b-110">See also</span></span>

- [<span data-ttu-id="dca6b-111">在 Visual Studio 中进行调试</span><span class="sxs-lookup"><span data-stu-id="dca6b-111">Debugging in Visual Studio</span></span>](/visualstudio/debugger/debugger-feature-tour)
