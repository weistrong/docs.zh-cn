---
description: 了解详细信息：如果将 EscapeQuote 设置为 True，则双引号不是分隔字段的有效注释标记
title: 如果将 EscapeQuote 设置为 True，则双引号不是分隔字段的有效注释标记
ms.date: 07/20/2015
f1_keywords:
- vbrTextFieldParser_InvalidComment
ms.assetid: 636d4b81-00ba-4cfd-98f7-4d57036f494d
ms.openlocfilehash: d0668c6ffb479e649d4d3900070dc125db6dec05
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797206"
---
# <a name="a-double-quote-is-not-a-valid-comment-token-for-delimited-fields-where-escapequote-is-set-to-true"></a><span data-ttu-id="3f35c-103">如果将 EscapeQuote 设置为 True，则双引号不是分隔字段的有效注释标记</span><span class="sxs-lookup"><span data-stu-id="3f35c-103">A double quote is not a valid comment token for delimited fields where EscapeQuote is set to True</span></span>

<span data-ttu-id="3f35c-104">已提供了一个引号作为 `TextFieldParser`的分隔符，但 `EscapeQuotes` 已设置为 `True`。</span><span class="sxs-lookup"><span data-stu-id="3f35c-104">A quotation mark has been supplied as the delimiter for the `TextFieldParser`, but `EscapeQuotes` is set to `True`.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="3f35c-105">更正此错误</span><span class="sxs-lookup"><span data-stu-id="3f35c-105">To correct this error</span></span>  
  
- <span data-ttu-id="3f35c-106">将 `EscapeQuotes` 设置为 `False`。</span><span class="sxs-lookup"><span data-stu-id="3f35c-106">Set `EscapeQuotes` to `False`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3f35c-107">请参阅</span><span class="sxs-lookup"><span data-stu-id="3f35c-107">See also</span></span>

- <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.SetDelimiters%2A>
- <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.Delimiters%2A>
- <xref:Microsoft.VisualBasic.FileIO.TextFieldParser>
- [<span data-ttu-id="3f35c-108">如何：读取逗号分隔的文本文件</span><span class="sxs-lookup"><span data-stu-id="3f35c-108">How to: Read From Comma-Delimited Text Files</span></span>](../../developing-apps/programming/drives-directories-files/how-to-read-from-comma-delimited-text-files.md)
