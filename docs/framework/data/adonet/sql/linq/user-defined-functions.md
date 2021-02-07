---
description: 了解详细信息： User-Defined 函数
title: 用户定义函数
ms.date: 03/30/2017
ms.assetid: 3304c9b2-5c7a-4a95-9d45-4f260dcb606e
ms.openlocfilehash: d27abd78e15ad6cb5ce4e9440ac425159a0b5bdc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99680936"
---
# <a name="user-defined-functions"></a><span data-ttu-id="69f37-103">用户定义函数</span><span class="sxs-lookup"><span data-stu-id="69f37-103">User-Defined Functions</span></span>

[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="69f37-104">在您的对象模型中使用方法来表示用户定义的函数。</span><span class="sxs-lookup"><span data-stu-id="69f37-104">uses methods in your object model to represent user-defined functions.</span></span> <span data-ttu-id="69f37-105">您可以通过应用 <xref:System.Data.Linq.Mapping.FunctionAttribute> 属性和 <xref:System.Data.Linq.Mapping.ParameterAttribute> 属性（如果需要）将方法指定为函数。</span><span class="sxs-lookup"><span data-stu-id="69f37-105">You designate methods as functions by applying the <xref:System.Data.Linq.Mapping.FunctionAttribute> attribute and, where required, the <xref:System.Data.Linq.Mapping.ParameterAttribute> attribute.</span></span> <span data-ttu-id="69f37-106">有关详细信息，请参阅 [LINQ to SQL 对象模型](the-linq-to-sql-object-model.md)。</span><span class="sxs-lookup"><span data-stu-id="69f37-106">For more information, see [The LINQ to SQL Object Model](the-linq-to-sql-object-model.md).</span></span>  
  
 <span data-ttu-id="69f37-107">为避免出现 <xref:System.InvalidOperationException>，[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 中用户定义的函数必须采用以下形式之一：</span><span class="sxs-lookup"><span data-stu-id="69f37-107">To avoid an <xref:System.InvalidOperationException>, user-defined functions in [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] must be in one of the following forms:</span></span>  
  
- <span data-ttu-id="69f37-108">包装为具有正确映射属性的方法调用的函数。</span><span class="sxs-lookup"><span data-stu-id="69f37-108">A function wrapped as a method call having the correct mapping attributes.</span></span> <span data-ttu-id="69f37-109">有关详细信息，请参阅 [基于属性的映射](attribute-based-mapping.md)。</span><span class="sxs-lookup"><span data-stu-id="69f37-109">For more information, see [Attribute-Based Mapping](attribute-based-mapping.md).</span></span>  
  
- <span data-ttu-id="69f37-110">特定于 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 的静态 SQL 方法。</span><span class="sxs-lookup"><span data-stu-id="69f37-110">A static SQL method specific to [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].</span></span>  
  
- <span data-ttu-id="69f37-111">.NET Framework 方法支持的函数。</span><span class="sxs-lookup"><span data-stu-id="69f37-111">A function supported by a .NET Framework method.</span></span>  
  
 <span data-ttu-id="69f37-112">本节中的主题说明了在您自行编写代码的情况下，如何在您的应用程序中构建和调用这些方法。</span><span class="sxs-lookup"><span data-stu-id="69f37-112">The topics in this section show how to form and call these methods in your application if you write the code yourself.</span></span> <span data-ttu-id="69f37-113">使用 Visual Studio 的开发人员通常会使用对象关系设计器来映射用户定义的函数。</span><span class="sxs-lookup"><span data-stu-id="69f37-113">Developers using Visual Studio would typically use the Object Relational Designer to map user-defined functions.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="69f37-114">本节内容</span><span class="sxs-lookup"><span data-stu-id="69f37-114">In This Section</span></span>  

 [<span data-ttu-id="69f37-115">如何：使用标量值用户定义的函数</span><span class="sxs-lookup"><span data-stu-id="69f37-115">How to: Use Scalar-Valued User-Defined Functions</span></span>](how-to-use-scalar-valued-user-defined-functions.md)  
 <span data-ttu-id="69f37-116">介绍如何实现返回标量值的函数。</span><span class="sxs-lookup"><span data-stu-id="69f37-116">Describes how to implement a function that returns scalar values.</span></span>  
  
 [<span data-ttu-id="69f37-117">如何：使用表值用户定义的函数</span><span class="sxs-lookup"><span data-stu-id="69f37-117">How to: Use Table-Valued User-Defined Functions</span></span>](how-to-use-table-valued-user-defined-functions.md)  
 <span data-ttu-id="69f37-118">介绍如何实现返回表值的函数。</span><span class="sxs-lookup"><span data-stu-id="69f37-118">Describes how to implement a function that returns table values.</span></span>  
  
 [<span data-ttu-id="69f37-119">如何：以内联方式调用用户定义的函数</span><span class="sxs-lookup"><span data-stu-id="69f37-119">How to: Call User-Defined Functions Inline</span></span>](how-to-call-user-defined-functions-inline.md)  
 <span data-ttu-id="69f37-120">介绍如何对函数进行内联调用，以及进行内联调用时在执行方面的差异。</span><span class="sxs-lookup"><span data-stu-id="69f37-120">Describes how to make inline calls to functions and the differences in execution when the call is made inline.</span></span>
