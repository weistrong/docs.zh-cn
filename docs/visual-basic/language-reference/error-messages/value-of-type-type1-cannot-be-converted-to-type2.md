---
description: 了解详细信息： BC31194：类型 "type1" 的值无法转换为 "type2"
title: 类型“type1”的值无法转换为“type2”
ms.date: 07/20/2015
f1_keywords:
- vbc31194
- bc31194
helpviewer_keywords:
- BC31194
ms.assetid: 03d50c31-addd-4c90-9c53-725b84f9782e
ms.openlocfilehash: 8cdb5206f0bc09a447ce241921b0efda63792c28
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99674774"
---
# <a name="bc31194-value-of-type-type1-cannot-be-converted-to-type2"></a><span data-ttu-id="bb79c-103">BC31194：类型 "type1" 的值无法转换为 "type2"</span><span class="sxs-lookup"><span data-stu-id="bb79c-103">BC31194: Value of type 'type1' cannot be converted to 'type2'</span></span>

<span data-ttu-id="bb79c-104">类型 "type1" 的值无法转换为 "type2"。</span><span class="sxs-lookup"><span data-stu-id="bb79c-104">Value of type 'type1' cannot be converted to 'type2'.</span></span> <span data-ttu-id="bb79c-105">您可以使用 "Value" 属性来获取 "" 的第一个元素的字符串值 \<parentElement> 。</span><span class="sxs-lookup"><span data-stu-id="bb79c-105">You can use the 'Value' property to get the string value of the first element of '\<parentElement>'.</span></span>

 <span data-ttu-id="bb79c-106">已尝试将 XML 文本隐式强制转换为特定类型。</span><span class="sxs-lookup"><span data-stu-id="bb79c-106">An attempt has been made to implicitly cast an XML literal to a specific type.</span></span> <span data-ttu-id="bb79c-107">XML 文本不能隐式强制转换为指定类型。</span><span class="sxs-lookup"><span data-stu-id="bb79c-107">The XML literal cannot be implicitly cast to the specified type.</span></span>

 <span data-ttu-id="bb79c-108">**错误 ID：** BC31194</span><span class="sxs-lookup"><span data-stu-id="bb79c-108">**Error ID:** BC31194</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="bb79c-109">更正此错误</span><span class="sxs-lookup"><span data-stu-id="bb79c-109">To correct this error</span></span>

- <span data-ttu-id="bb79c-110">使用 XML 文本的 `Value` 属性来将其值作为 `String`引用。</span><span class="sxs-lookup"><span data-stu-id="bb79c-110">Use the `Value` property of the XML literal to reference its value as a `String`.</span></span> <span data-ttu-id="bb79c-111">使用 `CType` 函数、另一个类型转换函数，或 <xref:System.Convert> 类将值强制转换为指定类型。</span><span class="sxs-lookup"><span data-stu-id="bb79c-111">Use the `CType` function, another type conversion function, or the <xref:System.Convert> class to cast the value as the specified type.</span></span>

## <a name="see-also"></a><span data-ttu-id="bb79c-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="bb79c-112">See also</span></span>

- <xref:System.Convert>
- [<span data-ttu-id="bb79c-113">Type Conversion Functions</span><span class="sxs-lookup"><span data-stu-id="bb79c-113">Type Conversion Functions</span></span>](../functions/type-conversion-functions.md)
- [<span data-ttu-id="bb79c-114">XML 文本</span><span class="sxs-lookup"><span data-stu-id="bb79c-114">XML Literals</span></span>](../xml-literals/index.md)
- [<span data-ttu-id="bb79c-115">XML</span><span class="sxs-lookup"><span data-stu-id="bb79c-115">XML</span></span>](../../programming-guide/language-features/xml/index.md)
