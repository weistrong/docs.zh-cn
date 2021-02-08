---
description: 了解详细信息： BC36550： "Extension" 特性只能应用于 "Module"、"Sub" 或 "Function" 声明
title: “Extension”特性只能应用于“Module”、“Sub”或“Function”声明。
ms.date: 07/20/2015
f1_keywords:
- bc36550
- vbc36550
helpviewer_keywords:
- BC36550
ms.assetid: 4387a51f-733c-45d7-abdb-eb64d4f51078
ms.openlocfilehash: f0c87de34238974229bc572a0f634a16e8cc78d9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796309"
---
# <a name="bc36550-extension-attribute-can-be-applied-only-to-module-sub-or-function-declarations"></a><span data-ttu-id="f87bc-103">BC36550： "Extension" 特性只能应用于 "Module"、"Sub" 或 "Function" 声明</span><span class="sxs-lookup"><span data-stu-id="f87bc-103">BC36550: 'Extension' attribute can be applied only to 'Module', 'Sub', or 'Function' declarations</span></span>

<span data-ttu-id="f87bc-104">在 Visual Basic 中扩展数据类型的唯一方法是在标准模块内定义扩展方法。</span><span class="sxs-lookup"><span data-stu-id="f87bc-104">The only way to extend a data type in Visual Basic is to define an extension method inside a standard module.</span></span> <span data-ttu-id="f87bc-105">扩展方法可以是 `Sub` 过程或 `Function` 过程。</span><span class="sxs-lookup"><span data-stu-id="f87bc-105">The extension method can be a `Sub` procedure or a `Function` procedure.</span></span> <span data-ttu-id="f87bc-106">必须用 `<Extension()>` 命名空间中的扩展属性标记所有扩展方法 <xref:System.Runtime.CompilerServices?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="f87bc-106">All extension methods must be marked with the extension attribute, `<Extension()>`, from the <xref:System.Runtime.CompilerServices?displayProperty=nameWithType> namespace.</span></span> <span data-ttu-id="f87bc-107">或者，包含扩展方法的模块可以用相同的方式进行标记。</span><span class="sxs-lookup"><span data-stu-id="f87bc-107">Optionally, a module that contains an extension method may be marked in the same way.</span></span> <span data-ttu-id="f87bc-108">扩展属性的其他使用无效。</span><span class="sxs-lookup"><span data-stu-id="f87bc-108">No other use of the extension attribute is valid.</span></span>

<span data-ttu-id="f87bc-109">**错误 ID：** BC36550</span><span class="sxs-lookup"><span data-stu-id="f87bc-109">**Error ID:** BC36550</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="f87bc-110">更正此错误</span><span class="sxs-lookup"><span data-stu-id="f87bc-110">To correct this error</span></span>

- <span data-ttu-id="f87bc-111">删除扩展属性。</span><span class="sxs-lookup"><span data-stu-id="f87bc-111">Remove the extension attribute.</span></span>

- <span data-ttu-id="f87bc-112">将扩展重新设计为封闭模块中定义的方法。</span><span class="sxs-lookup"><span data-stu-id="f87bc-112">Redesign your extension as a method, defined in an enclosing module.</span></span>

## <a name="example"></a><span data-ttu-id="f87bc-113">示例</span><span class="sxs-lookup"><span data-stu-id="f87bc-113">Example</span></span>

<span data-ttu-id="f87bc-114">下面的示例定义了 `Print` `String` 数据类型的方法。</span><span class="sxs-lookup"><span data-stu-id="f87bc-114">The following example defines a `Print` method for the `String` data type.</span></span>

```vb
Imports StringUtility
Imports System.Runtime.CompilerServices
Namespace StringUtility
    <Extension()>
    Module StringExtensions
        <Extension()>
        Public Sub Print (ByVal str As String)
            Console.WriteLine(str)
        End Sub
    End Module
End Namespace
```

## <a name="see-also"></a><span data-ttu-id="f87bc-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="f87bc-115">See also</span></span>

- [<span data-ttu-id="f87bc-116">属性概述</span><span class="sxs-lookup"><span data-stu-id="f87bc-116">Attributes overview</span></span>](../../programming-guide/concepts/attributes/index.md)
- [<span data-ttu-id="f87bc-117">扩展方法</span><span class="sxs-lookup"><span data-stu-id="f87bc-117">Extension Methods</span></span>](../../programming-guide/language-features/procedures/extension-methods.md)
- [<span data-ttu-id="f87bc-118">Module 语句</span><span class="sxs-lookup"><span data-stu-id="f87bc-118">Module Statement</span></span>](../statements/module-statement.md)
