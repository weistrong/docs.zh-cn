---
description: '了解有关以下内容的详细信息：如何：访问 XML 子代元素 (Visual Basic) '
title: 如何：访问 XML 子代元素
ms.date: 07/20/2015
helpviewer_keywords:
- XML descendent axis property [Visual Basic]
- XML axis [Visual Basic], descendent
- descendent axis property [Visual Basic]
- XML [Visual Basic], accessing
ms.assetid: aabfa258-4112-4e7e-bab9-403f96072ef7
ms.openlocfilehash: d8f3176a91c2f637f49d2754513f3253399ee8ed
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100433169"
---
# <a name="how-to-access-xml-descendant-elements-visual-basic"></a><span data-ttu-id="83b97-103">如何：访问 XML 后代元素 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="83b97-103">How to: Access XML Descendant Elements (Visual Basic)</span></span>

<span data-ttu-id="83b97-104">此示例演示如何使用子代轴属性访问具有指定名称并包含在 XML 元素下的所有 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="83b97-104">This example shows how to use a descendant axis property to access all XML elements that have a specified name and that are contained under an XML element.</span></span> <span data-ttu-id="83b97-105">具体而言，它使用 `Value` 属性获取 `name` 子代轴属性返回的集合中第一个元素的值。</span><span class="sxs-lookup"><span data-stu-id="83b97-105">In particular, it uses the `Value` property to get the value of the first element in the collection that the `name` descendant axis property returns.</span></span> <span data-ttu-id="83b97-106">`name`子代轴属性获取 `name` 对象中包含的所有名为的元素 `contacts` 。</span><span class="sxs-lookup"><span data-stu-id="83b97-106">The `name` descendant axis property gets all elements named `name` that are contained in the `contacts` object.</span></span> <span data-ttu-id="83b97-107">此示例还使用 `phone` 子代轴属性来访问 `phone` 对象中包含的所有名为的后代 `contacts` 。</span><span class="sxs-lookup"><span data-stu-id="83b97-107">This example also uses the `phone` descendant axis property to access all descendants named `phone` that are contained in the `contacts` object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="83b97-108">示例</span><span class="sxs-lookup"><span data-stu-id="83b97-108">Example</span></span>  

 [!code-vb[VbXMLSamples#31](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples13.vb#31)]  
  
## <a name="compile-the-code"></a><span data-ttu-id="83b97-109">编译代码</span><span class="sxs-lookup"><span data-stu-id="83b97-109">Compile the code</span></span>  

 <span data-ttu-id="83b97-110">此示例需要：</span><span class="sxs-lookup"><span data-stu-id="83b97-110">This example requires:</span></span>  
  
- <span data-ttu-id="83b97-111">对 <xref:System.Xml.Linq> 命名空间的引用。</span><span class="sxs-lookup"><span data-stu-id="83b97-111">A reference to the <xref:System.Xml.Linq> namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="83b97-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="83b97-112">See also</span></span>

- <xref:System.Xml.Linq.XContainer.Descendants%2A?displayProperty=nameWithType>
- [<span data-ttu-id="83b97-113">XML Descendant Axis Property</span><span class="sxs-lookup"><span data-stu-id="83b97-113">XML Descendant Axis Property</span></span>](../../../language-reference/xml-axis/xml-descendant-axis-property.md)
- [<span data-ttu-id="83b97-114">XML 值属性</span><span class="sxs-lookup"><span data-stu-id="83b97-114">XML Value Property</span></span>](../../../language-reference/xml-axis/xml-value-property.md)
- [<span data-ttu-id="83b97-115">在 Visual Basic 中访问 XML</span><span class="sxs-lookup"><span data-stu-id="83b97-115">Accessing XML in Visual Basic</span></span>](accessing-xml.md)
- [<span data-ttu-id="83b97-116">XML</span><span class="sxs-lookup"><span data-stu-id="83b97-116">XML</span></span>](index.md)
