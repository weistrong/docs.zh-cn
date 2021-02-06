---
description: 了解详细信息： BC30251：类型 " <typename> " 没有构造函数
title: 类型“<typename>”没有构造函数
ms.date: 07/20/2015
f1_keywords:
- bc30251
- vbc30251
helpviewer_keywords:
- BC30251
ms.assetid: aff3e1df-abe6-4bc0-9abc-a1e70514c561
ms.openlocfilehash: 32ae854e9f1b037a17d9c378ce7ee4a3f9b43ad2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99641169"
---
# <a name="bc30251-type-typename-has-no-constructors"></a><span data-ttu-id="045c8-103">BC30251：类型 " \<typename> " 没有构造函数</span><span class="sxs-lookup"><span data-stu-id="045c8-103">BC30251: Type '\<typename>' has no constructors</span></span>

<span data-ttu-id="045c8-104">某个类型不支持对 `Sub New()` 的调用。</span><span class="sxs-lookup"><span data-stu-id="045c8-104">A type does not support a call to `Sub New()`.</span></span> <span data-ttu-id="045c8-105">一个可能的原因是编译器或二进制文件被损坏。</span><span class="sxs-lookup"><span data-stu-id="045c8-105">One possible cause is a corrupted compiler or binary file.</span></span>

 <span data-ttu-id="045c8-106">**错误 ID：** BC30251</span><span class="sxs-lookup"><span data-stu-id="045c8-106">**Error ID:** BC30251</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="045c8-107">更正此错误</span><span class="sxs-lookup"><span data-stu-id="045c8-107">To correct this error</span></span>

1. <span data-ttu-id="045c8-108">如果该类型位于其他项目或一个引用的文件中，则重新安装此项目或文件。</span><span class="sxs-lookup"><span data-stu-id="045c8-108">If the type is in a different project or in a referenced file, reinstall the project or file.</span></span>

2. <span data-ttu-id="045c8-109">如果该类型位于同一个项目中，则重新编译包含该类型的程序集。</span><span class="sxs-lookup"><span data-stu-id="045c8-109">If the type is in the same project, recompile the assembly containing the type.</span></span>

3. <span data-ttu-id="045c8-110">如果错误重复出现，请重新安装 Visual Basic 编译器。</span><span class="sxs-lookup"><span data-stu-id="045c8-110">If the error recurs, reinstall the Visual Basic compiler.</span></span>

4. <span data-ttu-id="045c8-111">如果仍然出现错误，则收集有关该情况的信息并通知 Microsoft 产品支持服务。</span><span class="sxs-lookup"><span data-stu-id="045c8-111">If the error persists, gather information about the circumstances and notify Microsoft Product Support Services.</span></span>

## <a name="see-also"></a><span data-ttu-id="045c8-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="045c8-112">See also</span></span>

- [<span data-ttu-id="045c8-113">对象和类</span><span class="sxs-lookup"><span data-stu-id="045c8-113">Objects and Classes</span></span>](../../programming-guide/language-features/objects-and-classes/index.md)
- [<span data-ttu-id="045c8-114">与我们交流</span><span class="sxs-lookup"><span data-stu-id="045c8-114">Talk to Us</span></span>](/visualstudio/ide/feedback-options)
