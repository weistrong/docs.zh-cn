---
description: 了解详细信息： BC31168： XML 轴属性不支持后期绑定
title: XML 轴属性不支持后期绑定
ms.date: 07/20/2015
f1_keywords:
- bc31168
- vbc31168
helpviewer_keywords:
- BC31168
ms.assetid: 45707363-55e4-4151-892d-d8729106355b
ms.openlocfilehash: 19fe5bae200eaad9086626421d013bbbf8d143c3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99640831"
---
# <a name="bc31168-xml-axis-properties-do-not-support-late-binding"></a><span data-ttu-id="2eac1-103">BC31168： XML 轴属性不支持后期绑定</span><span class="sxs-lookup"><span data-stu-id="2eac1-103">BC31168: XML axis properties do not support late binding</span></span>

<span data-ttu-id="2eac1-104">为非类型化对象引用了 XML 轴属性。</span><span class="sxs-lookup"><span data-stu-id="2eac1-104">An XML axis property has been referenced for an untyped object.</span></span>

 <span data-ttu-id="2eac1-105">**错误 ID：** BC31168</span><span class="sxs-lookup"><span data-stu-id="2eac1-105">**Error ID:** BC31168</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="2eac1-106">更正此错误</span><span class="sxs-lookup"><span data-stu-id="2eac1-106">To correct this error</span></span>

- <span data-ttu-id="2eac1-107">在引用 XML 轴属性之前，请确保对象为强类型 <xref:System.Xml.Linq.XElement> 对象。</span><span class="sxs-lookup"><span data-stu-id="2eac1-107">Ensure that the object is a strong-typed <xref:System.Xml.Linq.XElement> object before referencing the XML axis property.</span></span>

## <a name="see-also"></a><span data-ttu-id="2eac1-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="2eac1-108">See also</span></span>

- [<span data-ttu-id="2eac1-109">XML 轴属性</span><span class="sxs-lookup"><span data-stu-id="2eac1-109">XML Axis Properties</span></span>](../xml-axis/index.md)
- [<span data-ttu-id="2eac1-110">XML</span><span class="sxs-lookup"><span data-stu-id="2eac1-110">XML</span></span>](../../programming-guide/language-features/xml/index.md)
