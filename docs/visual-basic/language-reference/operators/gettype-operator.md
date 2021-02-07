---
description: '详细了解： GetType 运算符 (Visual Basic) '
title: GetType Operator
ms.date: 07/20/2015
f1_keywords:
- vb.GetType
helpviewer_keywords:
- GetType operator [Visual Basic]
- GetType keyword [Visual Basic]
ms.assetid: 4f733297-2503-4607-850c-15eba65fff90
ms.openlocfilehash: 15fe9c28997aa01527f23c0cc8fdbb0fe6cc53f7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99665986"
---
# <a name="gettype-operator-visual-basic"></a><span data-ttu-id="2acb6-103">GetType 运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="2acb6-103">GetType Operator (Visual Basic)</span></span>

<span data-ttu-id="2acb6-104">返回 <xref:System.Type> 指定类型的对象。</span><span class="sxs-lookup"><span data-stu-id="2acb6-104">Returns a <xref:System.Type> object for the specified type.</span></span> <span data-ttu-id="2acb6-105"><xref:System.Type>对象提供有关类型的信息，如属性、方法和事件。</span><span class="sxs-lookup"><span data-stu-id="2acb6-105">The <xref:System.Type> object provides information about the type such as its properties, methods, and events.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2acb6-106">语法</span><span class="sxs-lookup"><span data-stu-id="2acb6-106">Syntax</span></span>  
  
```vb  
GetType(typename)  
```  
  
## <a name="parameters"></a><span data-ttu-id="2acb6-107">参数</span><span class="sxs-lookup"><span data-stu-id="2acb6-107">Parameters</span></span>  
  
|<span data-ttu-id="2acb6-108">参数</span><span class="sxs-lookup"><span data-stu-id="2acb6-108">Parameter</span></span>|<span data-ttu-id="2acb6-109">说明</span><span class="sxs-lookup"><span data-stu-id="2acb6-109">Description</span></span>|  
|---|---|  
|`typename`|<span data-ttu-id="2acb6-110">要获取其信息的类型的名称。</span><span class="sxs-lookup"><span data-stu-id="2acb6-110">The name of the type for which you desire information.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2acb6-111">备注</span><span class="sxs-lookup"><span data-stu-id="2acb6-111">Remarks</span></span>  

 <span data-ttu-id="2acb6-112">`GetType`运算符返回 <xref:System.Type> 指定的对象 `typename` 。</span><span class="sxs-lookup"><span data-stu-id="2acb6-112">The `GetType` operator returns the <xref:System.Type> object for the specified `typename`.</span></span> <span data-ttu-id="2acb6-113">可以在中传递任何已定义类型的名称 `typename` 。</span><span class="sxs-lookup"><span data-stu-id="2acb6-113">You can pass the name of any defined type in `typename`.</span></span> <span data-ttu-id="2acb6-114">这包括：</span><span class="sxs-lookup"><span data-stu-id="2acb6-114">This includes the following:</span></span>  
  
- <span data-ttu-id="2acb6-115">任何 Visual Basic 数据类型，如 `Boolean` 或 `Date` 。</span><span class="sxs-lookup"><span data-stu-id="2acb6-115">Any Visual Basic data type, such as `Boolean` or `Date`.</span></span>  
  
- <span data-ttu-id="2acb6-116">任何 .NET Framework 类、结构、模块或接口，如 <xref:System.ArgumentException?displayProperty=nameWithType> 或 <xref:System.Double?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="2acb6-116">Any .NET Framework class, structure, module, or interface, such as <xref:System.ArgumentException?displayProperty=nameWithType> or <xref:System.Double?displayProperty=nameWithType>.</span></span>  
  
- <span data-ttu-id="2acb6-117">应用程序定义的任何类、结构、模块或接口。</span><span class="sxs-lookup"><span data-stu-id="2acb6-117">Any class, structure, module, or interface defined by your application.</span></span>  
  
- <span data-ttu-id="2acb6-118">应用程序定义的任何数组。</span><span class="sxs-lookup"><span data-stu-id="2acb6-118">Any array defined by your application.</span></span>  
  
- <span data-ttu-id="2acb6-119">应用程序定义的任何委托。</span><span class="sxs-lookup"><span data-stu-id="2acb6-119">Any delegate defined by your application.</span></span>  
  
- <span data-ttu-id="2acb6-120">Visual Basic、.NET Framework 或应用程序定义的任何枚举。</span><span class="sxs-lookup"><span data-stu-id="2acb6-120">Any enumeration defined by Visual Basic, the .NET Framework, or your application.</span></span>  
  
 <span data-ttu-id="2acb6-121">如果要获取对象变量的类型对象，请使用 <xref:System.Type.GetType%2A?displayProperty=nameWithType> 方法。</span><span class="sxs-lookup"><span data-stu-id="2acb6-121">If you want to get the type object of an object variable, use the <xref:System.Type.GetType%2A?displayProperty=nameWithType> method.</span></span>  
  
 <span data-ttu-id="2acb6-122">`GetType`在以下情况下，该运算符可能很有用：</span><span class="sxs-lookup"><span data-stu-id="2acb6-122">The `GetType` operator can be useful in the following circumstances:</span></span>  
  
- <span data-ttu-id="2acb6-123">您必须在运行时访问类型的元数据。</span><span class="sxs-lookup"><span data-stu-id="2acb6-123">You must access the metadata for a type at run time.</span></span> <span data-ttu-id="2acb6-124"><xref:System.Type>对象提供类型成员和部署信息等元数据。</span><span class="sxs-lookup"><span data-stu-id="2acb6-124">The <xref:System.Type> object supplies metadata such as type members and deployment information.</span></span> <span data-ttu-id="2acb6-125">例如，您需要这样做来反映程序集。</span><span class="sxs-lookup"><span data-stu-id="2acb6-125">You need this, for example, to reflect over an assembly.</span></span> <span data-ttu-id="2acb6-126">有关详细信息，请参阅 <xref:System.Reflection?displayProperty=nameWithType>。</span><span class="sxs-lookup"><span data-stu-id="2acb6-126">For more information, see <xref:System.Reflection?displayProperty=nameWithType>.</span></span>  
  
- <span data-ttu-id="2acb6-127">要比较两个对象引用，以确定它们是否引用相同类型的实例。</span><span class="sxs-lookup"><span data-stu-id="2acb6-127">You want to compare two object references to see if they refer to instances of the same type.</span></span> <span data-ttu-id="2acb6-128">如果是，则 `GetType` 返回对同一对象的引用 <xref:System.Type> 。</span><span class="sxs-lookup"><span data-stu-id="2acb6-128">If they do, `GetType` returns references to the same <xref:System.Type> object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2acb6-129">示例</span><span class="sxs-lookup"><span data-stu-id="2acb6-129">Example</span></span>  

 <span data-ttu-id="2acb6-130">以下示例显示 `GetType` 使用中的运算符。</span><span class="sxs-lookup"><span data-stu-id="2acb6-130">The following examples show the `GetType` operator in use.</span></span>  
  
 [!code-vb[VbVbalrOperators#26](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#26)]  
  
## <a name="see-also"></a><span data-ttu-id="2acb6-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="2acb6-131">See also</span></span>

- [<span data-ttu-id="2acb6-132">Visual Basic 中的运算符优先级</span><span class="sxs-lookup"><span data-stu-id="2acb6-132">Operator Precedence in Visual Basic</span></span>](operator-precedence.md)
- [<span data-ttu-id="2acb6-133">按功能列出的运算符</span><span class="sxs-lookup"><span data-stu-id="2acb6-133">Operators Listed by Functionality</span></span>](operators-listed-by-functionality.md)
- [<span data-ttu-id="2acb6-134">运算符和表达式</span><span class="sxs-lookup"><span data-stu-id="2acb6-134">Operators and Expressions</span></span>](../../programming-guide/language-features/operators-and-expressions/index.md)
