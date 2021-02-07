---
description: 了解详细信息： BC31183： XML 命名空间 URI `http://www.w3.org/XML/1998/namespace` ; 只能绑定到 "xmlns"
title: XML 命名空间 URI“<uri>”可只绑定到“xmlns”
ms.date: 07/20/2015
f1_keywords:
- bc31183
- vbc31183
helpviewer_keywords:
- BC31183
ms.assetid: 0ab1dbce-8397-4959-b2cd-f58798b051a0
ms.openlocfilehash: e6a552f4754a12b8e80e5333232d0c48432f7a63
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99701386"
---
# <a name="bc31183-xml-namespace-uri-httpwwww3orgxml1998namespace-can-be-bound-only-to-xmlns"></a><span data-ttu-id="cea88-103">BC31183： XML 命名空间 URI `http://www.w3.org/XML/1998/namespace` ; 只能绑定到 "xmlns"</span><span class="sxs-lookup"><span data-stu-id="cea88-103">BC31183: XML namespace URI `http://www.w3.org/XML/1998/namespace`; can be bound only to 'xmlns'</span></span>

<span data-ttu-id="cea88-104">URI `http://www.w3.org/XML/1998/namespace` 用于 XML 命名空间声明。</span><span class="sxs-lookup"><span data-stu-id="cea88-104">The URI `http://www.w3.org/XML/1998/namespace` is used in an XML namespace declaration.</span></span> <span data-ttu-id="cea88-105">此 URI 是保留命名空间，不能包含在 XML 命名空间声明中。</span><span class="sxs-lookup"><span data-stu-id="cea88-105">This URI is a reserved namespace and cannot be included in an XML namespace declaration.</span></span>

 <span data-ttu-id="cea88-106">**错误 ID：** BC31183</span><span class="sxs-lookup"><span data-stu-id="cea88-106">**Error ID:** BC31183</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="cea88-107">更正此错误</span><span class="sxs-lookup"><span data-stu-id="cea88-107">To correct this error</span></span>

<span data-ttu-id="cea88-108">删除 XML 命名空间声明，或将 URI 替换 `http://www.w3.org/XML/1998/namespace` 为有效的命名空间 URI。</span><span class="sxs-lookup"><span data-stu-id="cea88-108">Remove the XML namespace declaration or replace the URI `http://www.w3.org/XML/1998/namespace` with a valid namespace URI.</span></span>

## <a name="see-also"></a><span data-ttu-id="cea88-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="cea88-109">See also</span></span>

- [<span data-ttu-id="cea88-110">Imports 语句（XML 命名空间）</span><span class="sxs-lookup"><span data-stu-id="cea88-110">Imports Statement (XML Namespace)</span></span>](../statements/imports-statement-xml-namespace.md)
- [<span data-ttu-id="cea88-111">XML 文本</span><span class="sxs-lookup"><span data-stu-id="cea88-111">XML Literals</span></span>](../xml-literals/index.md)
- [<span data-ttu-id="cea88-112">XML</span><span class="sxs-lookup"><span data-stu-id="cea88-112">XML</span></span>](../../programming-guide/language-features/xml/index.md)
