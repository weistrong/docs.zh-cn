---
description: 了解详细信息： BC42319： XML 注释异常必须具有 "cref" 特性
title: XML 注释异常必须具有“cref”特性
ms.date: 07/20/2015
f1_keywords:
- bc42319
- vbc42319
helpviewer_keywords:
- BC42319
ms.assetid: 62eeeba3-6811-48be-b1ef-c2e4feda3177
ms.openlocfilehash: e602a2973d95f70d5ab532e6be319a9575d239a7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99701451"
---
# <a name="bc42319-xml-comment-exception-must-have-a-cref-attribute"></a><span data-ttu-id="73b39-103">BC42319： XML 注释异常必须具有 "cref" 特性</span><span class="sxs-lookup"><span data-stu-id="73b39-103">BC42319: XML comment exception must have a 'cref' attribute</span></span>

<span data-ttu-id="73b39-104">\<exception>标记提供了一种方法来记录可由方法引发的异常。</span><span class="sxs-lookup"><span data-stu-id="73b39-104">The \<exception> tag provides a way to document the exceptions that may be thrown by a method.</span></span> <span data-ttu-id="73b39-105">必需的 `cref` 属性指定由文档生成器检查的成员的名称。</span><span class="sxs-lookup"><span data-stu-id="73b39-105">The required `cref` attribute designates the name of a member, which is checked by the documentation generator.</span></span> <span data-ttu-id="73b39-106">如果该成员存在，则将其转换为文档文件中的规范元素名称。</span><span class="sxs-lookup"><span data-stu-id="73b39-106">If the member exists, it is translated to the canonical element name in the documentation file.</span></span>

<span data-ttu-id="73b39-107">**错误 ID：** BC42319</span><span class="sxs-lookup"><span data-stu-id="73b39-107">**Error ID:** BC42319</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="73b39-108">更正此错误</span><span class="sxs-lookup"><span data-stu-id="73b39-108">To correct this error</span></span>

<span data-ttu-id="73b39-109">将 `cref` 属性添加到异常，如下所示：</span><span class="sxs-lookup"><span data-stu-id="73b39-109">Add the `cref` attribute to the exception as follows:</span></span>

```xml
<exception cref="member">description</exception>
```

## <a name="see-also"></a><span data-ttu-id="73b39-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="73b39-110">See also</span></span>

- [\<exception>](../xmldoc/exception.md)
- [<span data-ttu-id="73b39-111">如何：创建 XML 文档</span><span class="sxs-lookup"><span data-stu-id="73b39-111">How to: Create XML Documentation</span></span>](../../programming-guide/program-structure/how-to-create-xml-documentation.md)
- [<span data-ttu-id="73b39-112">XML 注释标记</span><span class="sxs-lookup"><span data-stu-id="73b39-112">XML Comment Tags</span></span>](../xmldoc/index.md)
