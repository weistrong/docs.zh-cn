---
description: 了解详细信息： Visual Basic 限制
title: 限制
ms.date: 07/20/2015
helpviewer_keywords:
- limits
- limitations [Visual Basic]
- limitations
- limits, Visual Basic code
- Visual Basic code, limitations
ms.assetid: cf1646b7-5d24-48c6-9616-bda8a4849d91
ms.openlocfilehash: 9182c5fe475e4350cb17ed3e4b734e3924bb9f7b
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100432840"
---
# <a name="visual-basic-limitations"></a><span data-ttu-id="c346a-103">Visual Basic 限制</span><span class="sxs-lookup"><span data-stu-id="c346a-103">Visual Basic Limitations</span></span>

<span data-ttu-id="c346a-104">的早期版本 Visual Basic 在代码中强制实施边界，如变量名称长度、模块中允许的变量数和模块大小。</span><span class="sxs-lookup"><span data-stu-id="c346a-104">Earlier versions of Visual Basic enforced boundaries in code, such as the length of variable names, the number of variables allowed in modules, and module size.</span></span> <span data-ttu-id="c346a-105">在 Visual Basic .NET 中，这些限制已被宽松，使你可以更自由地编写和排列代码。</span><span class="sxs-lookup"><span data-stu-id="c346a-105">In Visual Basic .NET, these restrictions have been relaxed, giving you greater freedom in writing and arranging your code.</span></span>  
  
 <span data-ttu-id="c346a-106">物理限制在运行时内存上依赖于编译时注意事项。</span><span class="sxs-lookup"><span data-stu-id="c346a-106">Physical limits are dependent more on run-time memory than on compile-time considerations.</span></span> <span data-ttu-id="c346a-107">如果使用明智的编程做法，并将大型应用程序划分为多个类和模块，则可能会遇到内部 Visual Basic 限制。</span><span class="sxs-lookup"><span data-stu-id="c346a-107">If you use prudent programming practices, and divide large applications into multiple classes and modules, then there is very little chance of encountering an internal Visual Basic limitation.</span></span>  
  
 <span data-ttu-id="c346a-108">下面是在极端情况下可能遇到的一些限制：</span><span class="sxs-lookup"><span data-stu-id="c346a-108">The following are some limitations that you might encounter in extreme cases:</span></span>  
  
- <span data-ttu-id="c346a-109">**名称长度。**</span><span class="sxs-lookup"><span data-stu-id="c346a-109">**Name Length.**</span></span> <span data-ttu-id="c346a-110">每个声明的编程元素的名称中的字符数最多为个。</span><span class="sxs-lookup"><span data-stu-id="c346a-110">There is a maximum number of characters for the name of every declared programming element.</span></span> <span data-ttu-id="c346a-111">如果元素名称是限定的，则此最大值适用于整个限定字符串。</span><span class="sxs-lookup"><span data-stu-id="c346a-111">This maximum applies to an entire qualification string if the element name is qualified.</span></span> <span data-ttu-id="c346a-112">请参阅 [Declared Element Names](../language-features/declared-elements/declared-element-names.md)。</span><span class="sxs-lookup"><span data-stu-id="c346a-112">See [Declared Element Names](../language-features/declared-elements/declared-element-names.md).</span></span>  
  
- <span data-ttu-id="c346a-113">**行长度。**</span><span class="sxs-lookup"><span data-stu-id="c346a-113">**Line Length.**</span></span> <span data-ttu-id="c346a-114">源代码的物理行中最多包含65535个字符。</span><span class="sxs-lookup"><span data-stu-id="c346a-114">There is a maximum of 65535 characters in a physical line of source code.</span></span> <span data-ttu-id="c346a-115">如果使用行继续符，则逻辑源代码行可能会更长。</span><span class="sxs-lookup"><span data-stu-id="c346a-115">The logical source code line can be longer if you use line continuation characters.</span></span> <span data-ttu-id="c346a-116">请参阅 [如何：在代码中中断和组合语句](how-to-break-and-combine-statements-in-code.md)。</span><span class="sxs-lookup"><span data-stu-id="c346a-116">See [How to: Break and Combine Statements in Code](how-to-break-and-combine-statements-in-code.md).</span></span>  
  
- <span data-ttu-id="c346a-117">**数组维度。**</span><span class="sxs-lookup"><span data-stu-id="c346a-117">**Array Dimensions.**</span></span> <span data-ttu-id="c346a-118">可以为数组声明的维数有最大值。</span><span class="sxs-lookup"><span data-stu-id="c346a-118">There is a maximum number of dimensions you can declare for an array.</span></span> <span data-ttu-id="c346a-119">这限制了可用于指定数组元素的索引数。</span><span class="sxs-lookup"><span data-stu-id="c346a-119">This limits how many indexes you can use to specify an array element.</span></span> <span data-ttu-id="c346a-120">请参阅 [Visual Basic 中的数组维度](../language-features/arrays/array-dimensions.md)。</span><span class="sxs-lookup"><span data-stu-id="c346a-120">See [Array Dimensions in Visual Basic](../language-features/arrays/array-dimensions.md).</span></span>  
  
- <span data-ttu-id="c346a-121">**字符串长度。**</span><span class="sxs-lookup"><span data-stu-id="c346a-121">**String Length.**</span></span> <span data-ttu-id="c346a-122">在单个字符串中，可以存储的 Unicode 字符数最多为个。</span><span class="sxs-lookup"><span data-stu-id="c346a-122">There is a maximum number of Unicode characters you can store in a single string.</span></span> <span data-ttu-id="c346a-123">请参阅 [String 数据类型](../../language-reference/data-types/string-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="c346a-123">See [String Data Type](../../language-reference/data-types/string-data-type.md).</span></span>  
  
- <span data-ttu-id="c346a-124">**环境字符串长度。**</span><span class="sxs-lookup"><span data-stu-id="c346a-124">**Environment String Length.**</span></span> <span data-ttu-id="c346a-125">对于用作命令行参数的任何环境字符串，最多可包含32768个字符。</span><span class="sxs-lookup"><span data-stu-id="c346a-125">There is a maximum of 32768 characters for any environment string used as a command-line argument.</span></span> <span data-ttu-id="c346a-126">这是对所有平台的限制。</span><span class="sxs-lookup"><span data-stu-id="c346a-126">This is a limitation on all platforms.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c346a-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="c346a-127">See also</span></span>

- [<span data-ttu-id="c346a-128">程序结构和代码约定</span><span class="sxs-lookup"><span data-stu-id="c346a-128">Program Structure and Code Conventions</span></span>](program-structure-and-code-conventions.md)
- [<span data-ttu-id="c346a-129">Visual Basic 命名约定</span><span class="sxs-lookup"><span data-stu-id="c346a-129">Visual Basic Naming Conventions</span></span>](naming-conventions.md)
