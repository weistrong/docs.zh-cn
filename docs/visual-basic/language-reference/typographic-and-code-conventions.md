---
description: '了解详细信息：版式和代码约定 (Visual Basic) '
title: 版式和代码约定
ms.date: 07/20/2015
helpviewer_keywords:
- coding conventions [Visual Basic], Visual Basic
- best practices [Visual Basic], coding conventions
- conventions [Visual Basic], Visual Basic coding
- typographic conventions [Visual Basic]
- document conventions [Visual Basic]
- conventions [Visual Basic], documentation
- Visual Basic code, conventions
ms.assetid: 1916cd81-ea9d-4faa-81f7-4a0d864b60f4
ms.openlocfilehash: 44e8445bb56f4f0c8b2f4eedddecda46ffcebb68
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99768800"
---
# <a name="typographic-and-code-conventions-visual-basic"></a><span data-ttu-id="92d63-103">版式和代码约定 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="92d63-103">Typographic and Code Conventions (Visual Basic)</span></span>

<span data-ttu-id="92d63-104">Visual Basic 文档使用以下排字和代码约定。</span><span class="sxs-lookup"><span data-stu-id="92d63-104">Visual Basic documentation uses the following typographic and code conventions.</span></span>  
  
## <a name="typographic-conventions"></a><span data-ttu-id="92d63-105">版式约定</span><span class="sxs-lookup"><span data-stu-id="92d63-105">Typographic Conventions</span></span>  
  
|<span data-ttu-id="92d63-106">示例</span><span class="sxs-lookup"><span data-stu-id="92d63-106">Example</span></span>|<span data-ttu-id="92d63-107">说明</span><span class="sxs-lookup"><span data-stu-id="92d63-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="92d63-108">`Sub`, `If`, `ChDir`, `Print`, `True`, `Debug`</span><span class="sxs-lookup"><span data-stu-id="92d63-108">`Sub`, `If`, `ChDir`, `Print`, `True`, `Debug`</span></span>|<span data-ttu-id="92d63-109">特定于语言的关键字和运行时成员具有词首大写字母，并设置格式，如本示例中所示。</span><span class="sxs-lookup"><span data-stu-id="92d63-109">Language-specific keywords and runtime members have initial uppercase letters and are formatted as shown in this example.</span></span>|  
|<span data-ttu-id="92d63-110">**SmallProject**、 **ButtonCollection**</span><span class="sxs-lookup"><span data-stu-id="92d63-110">**SmallProject**, **ButtonCollection**</span></span>|<span data-ttu-id="92d63-111">将为您指示键入的单词和短语设置格式，如本示例中所示。</span><span class="sxs-lookup"><span data-stu-id="92d63-111">Words and phrases you are instructed to type are formatted as shown in this example.</span></span>|  
|[<span data-ttu-id="92d63-112">Module 语句</span><span class="sxs-lookup"><span data-stu-id="92d63-112">Module Statement</span></span>](statements/module-statement.md)|<span data-ttu-id="92d63-113">可单击以切换到另一个帮助页的链接的格式如本示例中所示。</span><span class="sxs-lookup"><span data-stu-id="92d63-113">Links you can click to go to another Help page are formatted as shown in this example.</span></span>|  
|<span data-ttu-id="92d63-114">*object*、 *variableName*、 `argumentList`</span><span class="sxs-lookup"><span data-stu-id="92d63-114">*object*, *variableName*, `argumentList`</span></span>|<span data-ttu-id="92d63-115">您提供的信息的占位符格式如本示例中所示。</span><span class="sxs-lookup"><span data-stu-id="92d63-115">Placeholders for information that you supply are formatted as shown in this example.</span></span>|  
|<span data-ttu-id="92d63-116">[Shadows]，[ *expressionList* ]</span><span class="sxs-lookup"><span data-stu-id="92d63-116">[ Shadows ], [ *expressionList* ]</span></span>|<span data-ttu-id="92d63-117">在语法中，可选项括在括号中。</span><span class="sxs-lookup"><span data-stu-id="92d63-117">In syntax, optional items are enclosed in brackets.</span></span>|  
|<span data-ttu-id="92d63-118">{ `Public` &#124; `Friend` &#124; `Private` }</span><span class="sxs-lookup"><span data-stu-id="92d63-118">{ `Public` &#124; `Friend` &#124; `Private` }</span></span>|<span data-ttu-id="92d63-119">在语法中，当你必须在两个或多个项之间进行选择时，项括在大括号中，并用竖线分隔。</span><span class="sxs-lookup"><span data-stu-id="92d63-119">In syntax, when you must make a choice between two or more items, the items are enclosed in braces and separated by vertical bars.</span></span><br /><br /> <span data-ttu-id="92d63-120">您必须选择一个（且只有一个）项。</span><span class="sxs-lookup"><span data-stu-id="92d63-120">You must select one, and only one, of the items.</span></span>|  
|<span data-ttu-id="92d63-121">[ `Protected` &#124; `Friend` ]</span><span class="sxs-lookup"><span data-stu-id="92d63-121">[ `Protected` &#124; `Friend` ]</span></span>|<span data-ttu-id="92d63-122">在语法中，当您有选择两个或多个项之间的选项时，项将括在方括号中，并用竖线分隔。</span><span class="sxs-lookup"><span data-stu-id="92d63-122">In syntax, when you have the option of selecting between two or more items, the items are enclosed in square brackets and separated by vertical bars.</span></span><br /><br /> <span data-ttu-id="92d63-123">您可以选择项的任意组合，或不选择任何项。</span><span class="sxs-lookup"><span data-stu-id="92d63-123">You can select any combination of the items, or no item.</span></span>|  
|<span data-ttu-id="92d63-124">[{ `ByVal` &#124; `ByRef` }]</span><span class="sxs-lookup"><span data-stu-id="92d63-124">[{ `ByVal` &#124; `ByRef` }]</span></span>|<span data-ttu-id="92d63-125">在语法中，如果您可以选择不多个项，但您也可以完全省略项，则项括在括在大括号中的方括号内，并用竖线分隔。</span><span class="sxs-lookup"><span data-stu-id="92d63-125">In syntax, when you can select no more than one item, but you can also omit the items completely, the items are enclosed in square brackets surrounded by braces and separated by vertical bars.</span></span>|  
|<span data-ttu-id="92d63-126">*成员* 名称1， *成员名称* 2， *成员名称* 3</span><span class="sxs-lookup"><span data-stu-id="92d63-126">*memberName* 1, *memberName* 2, *memberName* 3</span></span>|<span data-ttu-id="92d63-127">同一个占位符的多个实例通过下标来区分，如示例中所示。</span><span class="sxs-lookup"><span data-stu-id="92d63-127">Multiple instances of the same placeholder are differentiated by subscripts, as shown in the example.</span></span>|  
|<span data-ttu-id="92d63-128">*1*</span><span class="sxs-lookup"><span data-stu-id="92d63-128">*memberName1*</span></span><br /><br /> <span data-ttu-id="92d63-129">...</span><span class="sxs-lookup"><span data-stu-id="92d63-129">...</span></span><br /><br /> <span data-ttu-id="92d63-130">*memberNameN*</span><span class="sxs-lookup"><span data-stu-id="92d63-130">*memberNameN*</span></span>|<span data-ttu-id="92d63-131">在语法中，省略号 ( ... ) 用于表示直接在省略号前面的类型的无限项。</span><span class="sxs-lookup"><span data-stu-id="92d63-131">In syntax, an ellipsis (...) is used to indicate an indefinite number of items of the kind immediately in front of the ellipsis.</span></span><br /><br /> <span data-ttu-id="92d63-132">在代码中，省略号表示为清楚起见省略了代码。</span><span class="sxs-lookup"><span data-stu-id="92d63-132">In code, ellipses signify code omitted for the sake of clarity.</span></span>|  
|<span data-ttu-id="92d63-133">ESC，ENTER</span><span class="sxs-lookup"><span data-stu-id="92d63-133">ESC, ENTER</span></span>|<span data-ttu-id="92d63-134">键盘上的键名和键序列均以大写字母显示。</span><span class="sxs-lookup"><span data-stu-id="92d63-134">Key names and key sequences on the keyboard appear in all uppercase letters.</span></span>|  
|<span data-ttu-id="92d63-135">Alt+F1</span><span class="sxs-lookup"><span data-stu-id="92d63-135">ALT+F1</span></span>|<span data-ttu-id="92d63-136">当键名称之间出现加号 (+) 时，必须按住一个键，同时按下一个键。</span><span class="sxs-lookup"><span data-stu-id="92d63-136">When plus signs (+) appear between key names, you must hold down one key while pressing the other.</span></span> <span data-ttu-id="92d63-137">例如，ALT + F1 表示按下 F1 键时按下 ALT 键。</span><span class="sxs-lookup"><span data-stu-id="92d63-137">For example, ALT+F1 means hold down the ALT key while pressing the F1 key.</span></span>|  
  
## <a name="code-conventions"></a><span data-ttu-id="92d63-138">代码约定</span><span class="sxs-lookup"><span data-stu-id="92d63-138">Code Conventions</span></span>  
  
|<span data-ttu-id="92d63-139">示例</span><span class="sxs-lookup"><span data-stu-id="92d63-139">Example</span></span>|<span data-ttu-id="92d63-140">说明</span><span class="sxs-lookup"><span data-stu-id="92d63-140">Description</span></span>|  
|-------------|-----------------|  
|`sampleString = "Hello, world!"`|<span data-ttu-id="92d63-141">代码示例以固定间距字体显示，并设置格式，如本示例中所示。</span><span class="sxs-lookup"><span data-stu-id="92d63-141">Code samples appear in a fixed-pitch font and are formatted as shown in this example.</span></span>|  
|<span data-ttu-id="92d63-142">上一语句将的值设置 `sampleString` 为 "Hello，world！"</span><span class="sxs-lookup"><span data-stu-id="92d63-142">The previous statement sets the value of `sampleString` to "Hello, world!"</span></span>|<span data-ttu-id="92d63-143">解释性文本中的代码元素显示为固定间距字体，如本示例中所示。</span><span class="sxs-lookup"><span data-stu-id="92d63-143">Code elements in explanatory text appear in a fixed-pitch font, as shown in this example.</span></span>|  
|`' This is a comment.`<br /><br /> `REM This is also a comment.`|<span data-ttu-id="92d63-144">代码注释由撇号 ( ") 或 REM 关键字引入。</span><span class="sxs-lookup"><span data-stu-id="92d63-144">Code comments are introduced by an apostrophe (') or the REM keyword.</span></span>|  
|`sampleVar = "This is an " _`<br /><br /> `& "example" _`<br /><br /> `& " of how to continue code."`|<span data-ttu-id="92d63-145">在行的末尾有一个空格 ( _) ，指示语句在下一行继续。</span><span class="sxs-lookup"><span data-stu-id="92d63-145">A space followed by an underscore ( _) at the end of a line indicates that the statement continues on the following line.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="92d63-146">请参阅</span><span class="sxs-lookup"><span data-stu-id="92d63-146">See also</span></span>

- [<span data-ttu-id="92d63-147">Visual Basic 语言参考</span><span class="sxs-lookup"><span data-stu-id="92d63-147">Visual Basic Language Reference</span></span>](index.md)
- [<span data-ttu-id="92d63-148">关键字</span><span class="sxs-lookup"><span data-stu-id="92d63-148">Keywords</span></span>](keywords/index.md)
- [<span data-ttu-id="92d63-149">Visual Basic 运行库成员</span><span class="sxs-lookup"><span data-stu-id="92d63-149">Visual Basic Runtime Library Members</span></span>](runtime-library-members.md)
- [<span data-ttu-id="92d63-150">Visual Basic 命名约定</span><span class="sxs-lookup"><span data-stu-id="92d63-150">Visual Basic Naming Conventions</span></span>](../programming-guide/program-structure/naming-conventions.md)
- [<span data-ttu-id="92d63-151">如何：在代码中拆分和合并语句</span><span class="sxs-lookup"><span data-stu-id="92d63-151">How to: Break and Combine Statements in Code</span></span>](../programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md)
- [<span data-ttu-id="92d63-152">代码中的注释</span><span class="sxs-lookup"><span data-stu-id="92d63-152">Comments in Code</span></span>](../programming-guide/program-structure/comments-in-code.md)
