---
description: 了解详细信息：无法完成操作，因为目标目录位于源目录下
title: 未能完成操作，因为目标目录位于源目录下
ms.date: 07/20/2015
f1_keywords:
- vbrIO_CyclicOperation
ms.assetid: 850d3a24-5d51-4ac8-a912-630efcd75278
ms.openlocfilehash: 5fb0bf1d761faf9d3d0c64e8815e28e14841b1fd
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100463515"
---
# <a name="could-not-complete-operation-since-target-directory-is-under-source-directory"></a><span data-ttu-id="57d0f-103">未能完成操作，因为目标目录位于源目录下</span><span class="sxs-lookup"><span data-stu-id="57d0f-103">Could not complete operation since target directory is under source directory</span></span>

<span data-ttu-id="57d0f-104">循环操作已失败。</span><span class="sxs-lookup"><span data-stu-id="57d0f-104">A cyclic operation has failed.</span></span> <span data-ttu-id="57d0f-105">循环操作正在循环，因此无法完成。</span><span class="sxs-lookup"><span data-stu-id="57d0f-105">Cyclic operations cycle and therefore cannot complete.</span></span> <span data-ttu-id="57d0f-106">例如，对象 A 可能会尝试从对象 B 中继承，而后者反之从对象 A 中继承。</span><span class="sxs-lookup"><span data-stu-id="57d0f-106">For example, Object A may attempt to inherit from Object B, which in turn inherits from Object A.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="57d0f-107">更正此错误</span><span class="sxs-lookup"><span data-stu-id="57d0f-107">To correct this error</span></span>  
  
- <span data-ttu-id="57d0f-108">继承时，请确保没有任何循环引用。</span><span class="sxs-lookup"><span data-stu-id="57d0f-108">When inheriting, make sure that there are no cyclic references.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="57d0f-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="57d0f-109">See also</span></span>

- [<span data-ttu-id="57d0f-110">错误类型</span><span class="sxs-lookup"><span data-stu-id="57d0f-110">Error Types</span></span>](../programming-guide/language-features/error-types.md)
- [<span data-ttu-id="57d0f-111">在 Visual Studio 调试器中使用断点</span><span class="sxs-lookup"><span data-stu-id="57d0f-111">Use breakpoints in the Visual Studio debugger</span></span>](/visualstudio/debugger/using-breakpoints)
