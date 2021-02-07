---
description: 了解更多相关信息： BC31200： ASP.NET 中的嵌入式代码不支持 XML 文本和 XML 属性
title: ASP.NET 中的嵌入式代码不支持 XML 文本和 XML 属性
ms.date: 07/20/2015
f1_keywords:
- vbc31200
- bc31200
helpviewer_keywords:
- BC31200
ms.assetid: 053e8cba-8584-45cc-9fa0-43d122779772
ms.openlocfilehash: 0a5328676ee38a56334b77f665a464daa586ce3a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99701399"
---
# <a name="bc31200-xml-literals-and-xml-properties-are-not-supported-in-embedded-code-within-aspnet"></a><span data-ttu-id="62832-103">BC31200： ASP.NET 中的嵌入式代码不支持 XML 文本和 XML 属性</span><span class="sxs-lookup"><span data-stu-id="62832-103">BC31200: XML literals and XML properties are not supported in embedded code within ASP.NET</span></span>

<span data-ttu-id="62832-104">ASP.NET 中的嵌入式代码不支持 XML 文本和 XML 属性。</span><span class="sxs-lookup"><span data-stu-id="62832-104">XML literals and XML properties are not supported in embedded code within ASP.NET.</span></span> <span data-ttu-id="62832-105">若要使用 XML 功能，请将代码移到代码隐藏。</span><span class="sxs-lookup"><span data-stu-id="62832-105">To use XML features, move the code to code-behind.</span></span>

 <span data-ttu-id="62832-106">在嵌入代码中定义 XML 文本或 XML 轴属性， (`<%= =>` 在 ASP.NET 文件中) 。</span><span class="sxs-lookup"><span data-stu-id="62832-106">An XML literal or XML axis property is defined within embedded code (`<%= =>`) in an ASP.NET file.</span></span>

 <span data-ttu-id="62832-107">**错误 ID：** BC31200</span><span class="sxs-lookup"><span data-stu-id="62832-107">**Error ID:** BC31200</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="62832-108">更正此错误</span><span class="sxs-lookup"><span data-stu-id="62832-108">To correct this error</span></span>

- <span data-ttu-id="62832-109">将包括 XML 文本或 XML 轴属性的代码移到 ASP.NET 代码隐藏文件中。</span><span class="sxs-lookup"><span data-stu-id="62832-109">Move the code that includes the XML literal or XML axis property to an ASP.NET code-behind file.</span></span>

## <a name="see-also"></a><span data-ttu-id="62832-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="62832-110">See also</span></span>

- [<span data-ttu-id="62832-111">XML 文本</span><span class="sxs-lookup"><span data-stu-id="62832-111">XML Literals</span></span>](../xml-literals/index.md)
- [<span data-ttu-id="62832-112">XML 轴属性</span><span class="sxs-lookup"><span data-stu-id="62832-112">XML Axis Properties</span></span>](../xml-axis/index.md)
- [<span data-ttu-id="62832-113">XML</span><span class="sxs-lookup"><span data-stu-id="62832-113">XML</span></span>](../../programming-guide/language-features/xml/index.md)
