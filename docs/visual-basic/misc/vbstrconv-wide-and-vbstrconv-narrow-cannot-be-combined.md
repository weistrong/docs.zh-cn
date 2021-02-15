---
description: 了解详细信息： Vbstrconv.wide 和 Vbstrconv.wide 不能组合
title: 不能组合 VbStrConv.Wide 和 VbStrConv.Narrow
ms.date: 07/20/2015
f1_keywords:
- vbrArgument_IllegalWideNarrow
ms.assetid: a53b4e6a-36b1-4e36-b2c5-8196313ec599
ms.openlocfilehash: 422c699bd06709368ea4f8948c4b2824a643e342
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100475664"
---
# <a name="vbstrconvwide-and-vbstrconvnarrow-cannot-be-combined"></a><span data-ttu-id="61e19-103">不能组合 VbStrConv.Wide 和 VbStrConv.Narrow</span><span class="sxs-lookup"><span data-stu-id="61e19-103">VbStrConv.Wide and VbStrConv.Narrow cannot be combined</span></span>

<span data-ttu-id="61e19-104">你的应用程序尝试组合 `VbStrConv` 枚举成员 `Wide` 和 `Narrow`，而它们是互斥的。</span><span class="sxs-lookup"><span data-stu-id="61e19-104">Your application is trying to combine the `VbStrConv` enumeration members `Wide` and `Narrow`, which are mutually exclusive.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="61e19-105">更正此错误</span><span class="sxs-lookup"><span data-stu-id="61e19-105">To correct this error</span></span>  
  
1. <span data-ttu-id="61e19-106">删除 `VbStrConv.Wide` 或 `VbStrConv.Narrow`。</span><span class="sxs-lookup"><span data-stu-id="61e19-106">Remove either `VbStrConv.Wide` or `VbStrConv.Narrow`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="61e19-107">请参阅</span><span class="sxs-lookup"><span data-stu-id="61e19-107">See also</span></span>

- <xref:System.Globalization>

- [<span data-ttu-id="61e19-108">开发全球化和本地化应用</span><span class="sxs-lookup"><span data-stu-id="61e19-108">Develop globalized and localized apps</span></span>](/visualstudio/ide/globalizing-and-localizing-applications)
