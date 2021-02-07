---
description: 了解详细信息： BC31180：不支持 XML 实体引用
title: 不支持 XML 实体引用
ms.date: 07/20/2015
f1_keywords:
- vbc31180
- bc31180
helpviewer_keywords:
- BC31180
ms.assetid: 2a393327-d8e2-4187-85b1-642b4f53b4ae
ms.openlocfilehash: c45202fbd97d2343caf6bf4cdccf9368d0a7a295
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99701412"
---
# <a name="bc31180-xml-entity-references-are-not-supported"></a><span data-ttu-id="cc568-103">BC31180：不支持 XML 实体引用</span><span class="sxs-lookup"><span data-stu-id="cc568-103">BC31180: XML entity references are not supported</span></span>

<span data-ttu-id="cc568-104">例如，在 `©` xml 1.0 规范中未定义的)  (实体引用包含为 xml 文本值。</span><span class="sxs-lookup"><span data-stu-id="cc568-104">An entity reference (for example, `©`) that is not defined in the XML 1.0 specification is included as a value for an XML literal.</span></span> <span data-ttu-id="cc568-105">`&` `"` `<` `>` Xml 文本中仅支持、、、和 `'` xml 实体引用。</span><span class="sxs-lookup"><span data-stu-id="cc568-105">Only `&`, `"`, `<`, `>`, and `'` XML entity references are supported in XML literals.</span></span>

 <span data-ttu-id="cc568-106">**错误 ID：** BC31180</span><span class="sxs-lookup"><span data-stu-id="cc568-106">**Error ID:** BC31180</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="cc568-107">更正此错误</span><span class="sxs-lookup"><span data-stu-id="cc568-107">To correct this error</span></span>

- <span data-ttu-id="cc568-108">删除不受支持的实体引用。</span><span class="sxs-lookup"><span data-stu-id="cc568-108">Remove the unsupported entity reference.</span></span>

## <a name="see-also"></a><span data-ttu-id="cc568-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="cc568-109">See also</span></span>

- [<span data-ttu-id="cc568-110">XML 文本和 XML 1.0 规范</span><span class="sxs-lookup"><span data-stu-id="cc568-110">XML Literals and the XML 1.0 Specification</span></span>](../../programming-guide/language-features/xml/xml-literals-and-the-xml-1-0-specification.md)
- [<span data-ttu-id="cc568-111">XML 文本</span><span class="sxs-lookup"><span data-stu-id="cc568-111">XML Literals</span></span>](../xml-literals/index.md)
- [<span data-ttu-id="cc568-112">XML</span><span class="sxs-lookup"><span data-stu-id="cc568-112">XML</span></span>](../../programming-guide/language-features/xml/index.md)
