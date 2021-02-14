---
description: 了解详细信息： SimplifiedChinese 和 Vbstrconv.wide。 Vbstrconv.traditionalchinese 无法组合
title: 不能组合 SimplifiedChinese 和 VbStrConv.TraditionalChinese
ms.date: 07/20/2015
f1_keywords:
- vbrArgument_StrConvSCandTC
ms.assetid: d8e6a11b-f549-43b5-8337-0594340e1325
ms.openlocfilehash: c1389976c6b4e33a418531c62b59bf1eb6460218
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100438224"
---
# <a name="simplifiedchinese-and-vbstrconvtraditionalchinese-cannot-be-combined"></a><span data-ttu-id="28f4c-103">不能组合 SimplifiedChinese 和 VbStrConv.TraditionalChinese</span><span class="sxs-lookup"><span data-stu-id="28f4c-103">SimplifiedChinese and VbStrConv.TraditionalChinese cannot be combined</span></span>

<span data-ttu-id="28f4c-104">应用程序尝试组合 `VbStrConv` 枚举成员 `SimplifiedChinese` 和 `TraditionalChinese`，而它们是互斥的。</span><span class="sxs-lookup"><span data-stu-id="28f4c-104">Your application is attempting to combine the `VbStrConv` enumeration members `SimplifiedChinese` and `TraditionalChinese`, which are mutually exclusive.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="28f4c-105">更正此错误</span><span class="sxs-lookup"><span data-stu-id="28f4c-105">To correct this error</span></span>  
  
- <span data-ttu-id="28f4c-106">删除 `VbStrConv.SimplifiedChinese` 或 `VbStrConv.TraditionalChinese`。</span><span class="sxs-lookup"><span data-stu-id="28f4c-106">Remove either `VbStrConv.SimplifiedChinese` or `VbStrConv.TraditionalChinese`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="28f4c-107">请参阅</span><span class="sxs-lookup"><span data-stu-id="28f4c-107">See also</span></span>

- <xref:System.Globalization>

- [<span data-ttu-id="28f4c-108">开发全球化和本地化应用</span><span class="sxs-lookup"><span data-stu-id="28f4c-108">Develop globalized and localized apps</span></span>](/visualstudio/ide/globalizing-and-localizing-applications)
