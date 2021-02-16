---
description: 详细了解：System.Xml 使用情况
title: System.Xml 使用情况
ms.date: 10/22/2008
ms.assetid: 82302f0d-a621-4c6f-b57d-999bd61f21a6
ms.openlocfilehash: 51886c07f0b68bb329c258daa93e809d94839341
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99641845"
---
# <a name="systemxml-usage"></a><span data-ttu-id="f69c2-103">System.Xml 使用情况</span><span class="sxs-lookup"><span data-stu-id="f69c2-103">System.Xml Usage</span></span>

<span data-ttu-id="f69c2-104">本部分讨论 <xref:System.Xml?displayProperty=nameWithType> 命名空间中可用于表示 XML 数据的几种类型的用法。</span><span class="sxs-lookup"><span data-stu-id="f69c2-104">This section talks about usage of several types residing in <xref:System.Xml?displayProperty=nameWithType> namespaces that can be used to represent XML data.</span></span>

 <span data-ttu-id="f69c2-105">❌ 请勿使用 <xref:System.Xml.XmlNode> 或 <xref:System.Xml.XmlDocument> 来表示 XML 数据。</span><span class="sxs-lookup"><span data-stu-id="f69c2-105">❌ DO NOT use <xref:System.Xml.XmlNode> or <xref:System.Xml.XmlDocument> to represent XML data.</span></span> <span data-ttu-id="f69c2-106">优选改用 <xref:System.Xml.XPath.IXPathNavigable>、<xref:System.Xml.XmlReader>、<xref:System.Xml.XmlWriter> 的实例或 <xref:System.Xml.Linq.XNode> 的子类型。</span><span class="sxs-lookup"><span data-stu-id="f69c2-106">Favor using instances of <xref:System.Xml.XPath.IXPathNavigable>, <xref:System.Xml.XmlReader>, <xref:System.Xml.XmlWriter>, or subtypes of <xref:System.Xml.Linq.XNode> instead.</span></span> <span data-ttu-id="f69c2-107">`XmlNode` 和 `XmlDocument` 不是为在公共 API 中公开而设计的。</span><span class="sxs-lookup"><span data-stu-id="f69c2-107">`XmlNode` and `XmlDocument` are not designed for exposing in public APIs.</span></span>

 <span data-ttu-id="f69c2-108">✔️ 请确保使用 `XmlReader`、`IXPathNavigable` 或 `XNode` 的子类型作为接受或返回 XML 的成员的输入或输出。</span><span class="sxs-lookup"><span data-stu-id="f69c2-108">✔️ DO use `XmlReader`, `IXPathNavigable`, or subtypes of `XNode` as input or output of members that accept or return XML.</span></span>

 <span data-ttu-id="f69c2-109">使用这些抽象，而不是 `XmlDocument`、`XmlNode` 或 <xref:System.Xml.XPath.XPathDocument>，因为这会将方法与内存中 XML 文档的特定实现分离，并允许它们与公开 `XNode`、`XmlReader` 或 <xref:System.Xml.XPath.XPathNavigator> 的虚拟 XML 数据源一起工作。</span><span class="sxs-lookup"><span data-stu-id="f69c2-109">Use these abstractions instead of `XmlDocument`, `XmlNode`, or <xref:System.Xml.XPath.XPathDocument>, because this decouples the methods from specific implementations of an in-memory XML document and allows them to work with virtual XML data sources that expose `XNode`, `XmlReader`, or <xref:System.Xml.XPath.XPathNavigator>.</span></span>

 <span data-ttu-id="f69c2-110">❌ 如果要创建一个表示基础对象模型或数据源的 XML 视图的类型，请勿将 `XmlDocument` 子类化。</span><span class="sxs-lookup"><span data-stu-id="f69c2-110">❌ DO NOT subclass `XmlDocument` if you want to create a type representing an XML view of an underlying object model or data source.</span></span>

 <span data-ttu-id="f69c2-111">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="f69c2-111">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="f69c2-112">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="f69c2-112">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="f69c2-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="f69c2-113">See also</span></span>

- [<span data-ttu-id="f69c2-114">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="f69c2-114">Framework Design Guidelines</span></span>](index.md)
- [<span data-ttu-id="f69c2-115">使用准则</span><span class="sxs-lookup"><span data-stu-id="f69c2-115">Usage Guidelines</span></span>](usage-guidelines.md)
