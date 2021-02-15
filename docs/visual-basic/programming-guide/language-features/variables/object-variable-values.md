---
description: '了解详细信息： (Visual Basic 的对象变量值) '
title: 对象变量值
ms.date: 07/20/2015
helpviewer_keywords:
- object variables [Visual Basic], values
- values [Visual Basic], of object variables
- data types [Visual Basic], object variable
- variables [Visual Basic], object
ms.assetid: 31555704-58a3-49f1-9a0a-6421f605664f
ms.openlocfilehash: 3259a0b04ed629feea89c1a3e9dba69ed7d226f6
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100481670"
---
# <a name="object-variable-values-visual-basic"></a><span data-ttu-id="ad2bc-103">对象变量值 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ad2bc-103">Object Variable Values (Visual Basic)</span></span>

<span data-ttu-id="ad2bc-104">[对象数据类型](../../../language-reference/data-types/object-data-type.md)的变量可以引用任何类型的数据。</span><span class="sxs-lookup"><span data-stu-id="ad2bc-104">A variable of the [Object Data Type](../../../language-reference/data-types/object-data-type.md) can refer to data of any type.</span></span> <span data-ttu-id="ad2bc-105">在变量中存储的值 `Object` 将保留在内存中的其他位置，而变量本身保存指向数据的指针。</span><span class="sxs-lookup"><span data-stu-id="ad2bc-105">The value you store in an `Object` variable is kept elsewhere in memory, while the variable itself holds a pointer to the data.</span></span>  
  
## <a name="object-classifier-functions"></a><span data-ttu-id="ad2bc-106">对象分类器函数</span><span class="sxs-lookup"><span data-stu-id="ad2bc-106">Object Classifier Functions</span></span>  

 <span data-ttu-id="ad2bc-107">Visual Basic 提供返回变量引用信息的函数 `Object` ，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="ad2bc-107">Visual Basic supplies functions that return information about what an `Object` variable refers to, as shown in the following table.</span></span>  
  
|<span data-ttu-id="ad2bc-108">功能</span><span class="sxs-lookup"><span data-stu-id="ad2bc-108">Function</span></span>|<span data-ttu-id="ad2bc-109">如果对象变量引用，则返回 True</span><span class="sxs-lookup"><span data-stu-id="ad2bc-109">Returns True if the Object variable refers to</span></span>|  
|--------------|---------------------------------------------------|  
|<xref:Microsoft.VisualBasic.Information.IsArray%2A>|<span data-ttu-id="ad2bc-110">值的数组，而不是单个值</span><span class="sxs-lookup"><span data-stu-id="ad2bc-110">An array of values, rather than a single value</span></span>|  
|<xref:Microsoft.VisualBasic.Information.IsDate%2A>|<span data-ttu-id="ad2bc-111">[日期数据类型](../../../language-reference/data-types/date-data-type.md)值，或可解释为日期和时间值的字符串</span><span class="sxs-lookup"><span data-stu-id="ad2bc-111">A [Date Data Type](../../../language-reference/data-types/date-data-type.md) value, or a string that can be interpreted as a date and time value</span></span>|  
|<xref:Microsoft.VisualBasic.Information.IsDBNull%2A>|<span data-ttu-id="ad2bc-112">类型为的对象 <xref:System.DBNull> ，表示缺少或不存在的数据</span><span class="sxs-lookup"><span data-stu-id="ad2bc-112">An object of type <xref:System.DBNull>, which represents missing or nonexistent data</span></span>|  
|<xref:Microsoft.VisualBasic.Information.IsError%2A>|<span data-ttu-id="ad2bc-113">异常对象，派生自 <xref:System.Exception></span><span class="sxs-lookup"><span data-stu-id="ad2bc-113">An exception object, which derives from <xref:System.Exception></span></span>|  
|<xref:Microsoft.VisualBasic.Information.IsNothing%2A>|<span data-ttu-id="ad2bc-114">[没有，也就是说](../../../language-reference/nothing.md)，当前没有对象赋给变量</span><span class="sxs-lookup"><span data-stu-id="ad2bc-114">[Nothing](../../../language-reference/nothing.md), that is, no object is currently assigned to the variable</span></span>|  
|<xref:Microsoft.VisualBasic.Information.IsNumeric%2A>|<span data-ttu-id="ad2bc-115">一个数字，或者一个可解释为数字的字符串。</span><span class="sxs-lookup"><span data-stu-id="ad2bc-115">A number, or a string that can be interpreted as a number</span></span>|  
|<xref:Microsoft.VisualBasic.Information.IsReference%2A>|<span data-ttu-id="ad2bc-116">引用类型 (例如字符串、数组、委托或类类型) </span><span class="sxs-lookup"><span data-stu-id="ad2bc-116">A reference type (such as a string, array, delegate, or class type)</span></span>|  
  
 <span data-ttu-id="ad2bc-117">您可以使用这些函数来避免将无效值提交给操作或过程。</span><span class="sxs-lookup"><span data-stu-id="ad2bc-117">You can use these functions to avoid submitting an invalid value to an operation or a procedure.</span></span>  
  
## <a name="typeof-operator"></a><span data-ttu-id="ad2bc-118">TypeOf 运算符</span><span class="sxs-lookup"><span data-stu-id="ad2bc-118">TypeOf Operator</span></span>  

 <span data-ttu-id="ad2bc-119">你还可以使用 [TypeOf 运算符](../../../language-reference/operators/typeof-operator.md) 来确定对象变量当前是否引用了特定数据类型。</span><span class="sxs-lookup"><span data-stu-id="ad2bc-119">You can also use the [TypeOf Operator](../../../language-reference/operators/typeof-operator.md) to determine whether an object variable currently refers to a specific data type.</span></span> <span data-ttu-id="ad2bc-120">`TypeOf` `Is` `True` 如果操作数的运行时类型派生自或实现指定的类型，则 ... 表达式的计算结果为。</span><span class="sxs-lookup"><span data-stu-id="ad2bc-120">The `TypeOf`...`Is` expression evaluates to `True` if the run-time type of the operand is derived from or implements the specified type.</span></span>  
  
 <span data-ttu-id="ad2bc-121">下面的示例 `TypeOf` 在引用值和引用类型的对象变量上使用。</span><span class="sxs-lookup"><span data-stu-id="ad2bc-121">The following example uses `TypeOf` on object variables referring to value and reference types.</span></span>  
  
```vb  
' The following statement puts a value type (Integer) in an Object variable.  
Dim num As Object = 10  
' The following statement puts a reference type (Form) in an Object variable.  
Dim frm As Object = New Form()  
If TypeOf num Is Long Then Debug.WriteLine("num is Long")  
If TypeOf num Is Integer Then Debug.WriteLine("num is Integer")  
If TypeOf num Is Short Then Debug.WriteLine("num is Short")  
If TypeOf num Is Object Then Debug.WriteLine("num is Object")  
If TypeOf frm Is Form Then Debug.WriteLine("frm is Form")  
If TypeOf frm Is Label Then Debug.WriteLine("frm is Label")  
If TypeOf frm Is Object Then Debug.WriteLine("frm is Object")  
```  
  
 <span data-ttu-id="ad2bc-122">前面的示例将以下行写入 " **调试** " 窗口：</span><span class="sxs-lookup"><span data-stu-id="ad2bc-122">The preceding example writes the following lines to the **Debug** window:</span></span>  
  
 `num is Integer`  
  
 `num is Object`  
  
 `frm is Form`  
  
 `frm is Object`  
  
 <span data-ttu-id="ad2bc-123">对象变量 `num` 引用类型的数据 `Integer` ，并 `frm` 引用类的对象 <xref:System.Windows.Forms.Form> 。</span><span class="sxs-lookup"><span data-stu-id="ad2bc-123">The object variable `num` refers to data of type `Integer`, and `frm` refers to an object of class <xref:System.Windows.Forms.Form>.</span></span>  
  
## <a name="object-arrays"></a><span data-ttu-id="ad2bc-124">对象数组</span><span class="sxs-lookup"><span data-stu-id="ad2bc-124">Object Arrays</span></span>  

 <span data-ttu-id="ad2bc-125">您可以声明和使用变量的数组 `Object` 。</span><span class="sxs-lookup"><span data-stu-id="ad2bc-125">You can declare and use an array of `Object` variables.</span></span> <span data-ttu-id="ad2bc-126">如果需要处理各种数据类型和对象类，这会很有用。</span><span class="sxs-lookup"><span data-stu-id="ad2bc-126">This is useful when you need to handle a variety of data types and object classes.</span></span> <span data-ttu-id="ad2bc-127">数组中的所有元素必须具有相同的声明数据类型。</span><span class="sxs-lookup"><span data-stu-id="ad2bc-127">All the elements in an array must have the same declared data type.</span></span> <span data-ttu-id="ad2bc-128">如果将此数据类型声明为，则可以在 `Object` 数组中将对象和类实例与其他数据类型一起存储。</span><span class="sxs-lookup"><span data-stu-id="ad2bc-128">Declaring this data type as `Object` allows you to store objects and class instances alongside other data types in the array.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ad2bc-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="ad2bc-129">See also</span></span>

- [<span data-ttu-id="ad2bc-130">对象变量</span><span class="sxs-lookup"><span data-stu-id="ad2bc-130">Object Variables</span></span>](object-variables.md)
- [<span data-ttu-id="ad2bc-131">对象变量声明</span><span class="sxs-lookup"><span data-stu-id="ad2bc-131">Object Variable Declaration</span></span>](object-variable-declaration.md)
- [<span data-ttu-id="ad2bc-132">对象变量赋值</span><span class="sxs-lookup"><span data-stu-id="ad2bc-132">Object Variable Assignment</span></span>](object-variable-assignment.md)
- [<span data-ttu-id="ad2bc-133">如何：引用对象的当前实例</span><span class="sxs-lookup"><span data-stu-id="ad2bc-133">How to: Refer to the Current Instance of an Object</span></span>](how-to-refer-to-the-current-instance-of-an-object.md)
- [<span data-ttu-id="ad2bc-134">如何：确定对象变量引用的类型</span><span class="sxs-lookup"><span data-stu-id="ad2bc-134">How to: Determine What Type an Object Variable Refers To</span></span>](how-to-determine-what-type-an-object-variable-refers-to.md)
- [<span data-ttu-id="ad2bc-135">如何：确定两个对象是否相关</span><span class="sxs-lookup"><span data-stu-id="ad2bc-135">How to: Determine Whether Two Objects Are Related</span></span>](how-to-determine-whether-two-objects-are-related.md)
- [<span data-ttu-id="ad2bc-136">如何：确定两个对象是否相同</span><span class="sxs-lookup"><span data-stu-id="ad2bc-136">How to: Determine Whether Two Objects Are Identical</span></span>](how-to-determine-whether-two-objects-are-identical.md)
- [<span data-ttu-id="ad2bc-137">数据类型</span><span class="sxs-lookup"><span data-stu-id="ad2bc-137">Data Types</span></span>](../data-types/index.md)
