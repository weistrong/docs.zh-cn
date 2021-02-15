---
description: 了解详细信息：在类构造函数中使用类的默认实例可能会导致无限递归调用
title: 在类构造函数中使用类的默认实例可能会导致无限递归调用
ms.date: 07/20/2015
ms.assetid: 9645b47f-7de5-46d0-bb45-d5fdaa8aaa2a
ms.openlocfilehash: f65956c92f7d391aa77734d7afd5adf3bea1f906
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100475677"
---
# <a name="use-of-default-instance-of-a-class-in-the-class-constructor-could-lead-to-infinite-recursive-call"></a><span data-ttu-id="b0d39-103">在类构造函数中使用类的默认实例可能会导致无限递归调用</span><span class="sxs-lookup"><span data-stu-id="b0d39-103">Use of Default Instance of a class in the class constructor could lead to infinite recursive call</span></span>

<span data-ttu-id="b0d39-104">已在类的构造函数中使用类的默认实例。</span><span class="sxs-lookup"><span data-stu-id="b0d39-104">A default instance of a class has been used in the constructor of the class.</span></span> <span data-ttu-id="b0d39-105">这可能会导致无限递归调用（也称为无限循环）。</span><span class="sxs-lookup"><span data-stu-id="b0d39-105">This can lead to an infinite recursive call, also known as an infinite loop.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="b0d39-106">更正此错误</span><span class="sxs-lookup"><span data-stu-id="b0d39-106">To correct this error</span></span>  
  
- <span data-ttu-id="b0d39-107">从类构造函数中删除默认实例。</span><span class="sxs-lookup"><span data-stu-id="b0d39-107">Remove the default instance from the class constructor.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b0d39-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="b0d39-108">See also</span></span>

- [<span data-ttu-id="b0d39-109">构造函数</span><span class="sxs-lookup"><span data-stu-id="b0d39-109">Constructors</span></span>](../programming-guide/concepts/object-oriented-programming.md#constructors)
