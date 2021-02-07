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
# <a name="bc31200-xml-literals-and-xml-properties-are-not-supported-in-embedded-code-within-aspnet"></a>BC31200： ASP.NET 中的嵌入式代码不支持 XML 文本和 XML 属性

ASP.NET 中的嵌入式代码不支持 XML 文本和 XML 属性。 若要使用 XML 功能，请将代码移到代码隐藏。

 在嵌入代码中定义 XML 文本或 XML 轴属性， (`<%= =>` 在 ASP.NET 文件中) 。

 **错误 ID：** BC31200

## <a name="to-correct-this-error"></a>更正此错误

- 将包括 XML 文本或 XML 轴属性的代码移到 ASP.NET 代码隐藏文件中。

## <a name="see-also"></a>请参阅

- [XML 文本](../xml-literals/index.md)
- [XML 轴属性](../xml-axis/index.md)
- [XML](../../programming-guide/language-features/xml/index.md)
