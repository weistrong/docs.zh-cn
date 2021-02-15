---
description: 详细了解：异常设计准则
title: 异常设计准则
ms.date: 10/22/2008
helpviewer_keywords:
- exceptions [.NET Framework], design guidelines
- class library design guidelines [.NET Framework], exceptions
- errors [.NET Framework], exceptions
- reporting errors
ms.assetid: bc177b2f-7528-4ae4-83db-aacfb04b86d0
ms.openlocfilehash: 0845f06dca0ee83d7315c3b0b4b6ae090b24a875
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642105"
---
# <a name="design-guidelines-for-exceptions"></a><span data-ttu-id="d5010-103">异常设计准则</span><span class="sxs-lookup"><span data-stu-id="d5010-103">Design Guidelines for Exceptions</span></span>

<span data-ttu-id="d5010-104">与基于返回值的错误报告相比，异常处理具有很多优点。</span><span class="sxs-lookup"><span data-stu-id="d5010-104">Exception handling has many advantages over return-value-based error reporting.</span></span> <span data-ttu-id="d5010-105">良好的框架设计可帮助应用程序开发人员实现异常的优点。</span><span class="sxs-lookup"><span data-stu-id="d5010-105">Good framework design helps the application developer realize the benefits of exceptions.</span></span> <span data-ttu-id="d5010-106">本部分讨论异常的优点，并提供有效使用它们的准则。</span><span class="sxs-lookup"><span data-stu-id="d5010-106">This section discusses the benefits of exceptions and presents guidelines for using them effectively.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="d5010-107">本节内容</span><span class="sxs-lookup"><span data-stu-id="d5010-107">In This Section</span></span>  

 [<span data-ttu-id="d5010-108">异常引发</span><span class="sxs-lookup"><span data-stu-id="d5010-108">Exception Throwing</span></span>](exception-throwing.md)  
 [<span data-ttu-id="d5010-109">使用标准异常类型</span><span class="sxs-lookup"><span data-stu-id="d5010-109">Using Standard Exception Types</span></span>](using-standard-exception-types.md)  
 [<span data-ttu-id="d5010-110">异常和性能</span><span class="sxs-lookup"><span data-stu-id="d5010-110">Exceptions and Performance</span></span>](exceptions-and-performance.md)  
 <span data-ttu-id="d5010-111">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="d5010-111">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="d5010-112">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="d5010-112">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d5010-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="d5010-113">See also</span></span>

- [<span data-ttu-id="d5010-114">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="d5010-114">Framework Design Guidelines</span></span>](index.md)
