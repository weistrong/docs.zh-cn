---
description: 详细了解：静态类设计
title: 静态类设计
ms.date: 10/22/2008
helpviewer_keywords:
- type design guidelines, static classes
- class library design guidelines [.NET Framework], classes
- classes [.NET Framework], static
- static classes [.NET Framework]
- classes [.NET Framework], design guidelines
- type design guidelines, classes
ms.assetid: d67c14d8-c4dd-443f-affb-4ccae677c9b6
ms.openlocfilehash: 16db470ab0975a5545617c9c5471d6ac157e688b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99782463"
---
# <a name="static-class-design"></a><span data-ttu-id="79c5b-103">静态类设计</span><span class="sxs-lookup"><span data-stu-id="79c5b-103">Static Class Design</span></span>

<span data-ttu-id="79c5b-104">静态类定义为仅包含静态成员（除了从 <xref:System.Object?displayProperty=nameWithType> 继承的实例成员和可能的专用构造函数之外）的类。</span><span class="sxs-lookup"><span data-stu-id="79c5b-104">A static class is defined as a class that contains only static members (of course besides the instance members inherited from <xref:System.Object?displayProperty=nameWithType> and possibly a private constructor).</span></span> <span data-ttu-id="79c5b-105">某些语言为静态类提供内置支持。</span><span class="sxs-lookup"><span data-stu-id="79c5b-105">Some languages provide built-in support for static classes.</span></span> <span data-ttu-id="79c5b-106">在 C# 2.0 及更高版本中，将一个类声明为静态时，它是密封的、抽象的，并且不能替代或声明任何实例成员。</span><span class="sxs-lookup"><span data-stu-id="79c5b-106">In C# 2.0 and later, when a class is declared to be static, it is sealed, abstract, and no instance members can be overridden or declared.</span></span>

 <span data-ttu-id="79c5b-107">静态类是纯面向对象的设计与简单性之间的折衷。</span><span class="sxs-lookup"><span data-stu-id="79c5b-107">Static classes are a compromise between pure object-oriented design and simplicity.</span></span> <span data-ttu-id="79c5b-108">它们通常用于提供其他操作（如 <xref:System.IO.File?displayProperty=nameWithType>）的快捷方式、扩展方法的持有者或者无法为其确保完整的面向对象包装器的功能（如 <xref:System.Environment?displayProperty=nameWithType>）。</span><span class="sxs-lookup"><span data-stu-id="79c5b-108">They are commonly used to provide shortcuts to other operations (such as <xref:System.IO.File?displayProperty=nameWithType>), holders of extension methods, or functionality for which a full object-oriented wrapper is unwarranted (such as <xref:System.Environment?displayProperty=nameWithType>).</span></span>

 <span data-ttu-id="79c5b-109">✔️ 请务必要少使用静态类。</span><span class="sxs-lookup"><span data-stu-id="79c5b-109">✔️ DO use static classes sparingly.</span></span>

 <span data-ttu-id="79c5b-110">静态类应该只用作框架的面向对象核心的支持类。</span><span class="sxs-lookup"><span data-stu-id="79c5b-110">Static classes should be used only as supporting classes for the object-oriented core of the framework.</span></span>

 <span data-ttu-id="79c5b-111">❌ 请勿将静态类视为杂项桶。</span><span class="sxs-lookup"><span data-stu-id="79c5b-111">❌ DO NOT treat static classes as a miscellaneous bucket.</span></span>

 <span data-ttu-id="79c5b-112">❌ 请勿在静态类中声明或替代实例成员。</span><span class="sxs-lookup"><span data-stu-id="79c5b-112">❌ DO NOT declare or override instance members in static classes.</span></span>

 <span data-ttu-id="79c5b-113">✔️ 如果你的编程语言没有对静态类的内置支持，请务必将静态类声明为密封的且抽象的，并添加一个专用实例构造函数。</span><span class="sxs-lookup"><span data-stu-id="79c5b-113">✔️ DO declare static classes as sealed, abstract, and add a private instance constructor if your programming language does not have built-in support for static classes.</span></span>

 <span data-ttu-id="79c5b-114">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="79c5b-114">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="79c5b-115">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="79c5b-115">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="79c5b-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="79c5b-116">See also</span></span>

- [<span data-ttu-id="79c5b-117">类型设计准则</span><span class="sxs-lookup"><span data-stu-id="79c5b-117">Type Design Guidelines</span></span>](type.md)
- [<span data-ttu-id="79c5b-118">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="79c5b-118">Framework Design Guidelines</span></span>](index.md)
