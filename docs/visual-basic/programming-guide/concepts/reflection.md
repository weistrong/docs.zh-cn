---
description: '了解详细信息：反射 (Visual Basic) '
title: 反射
ms.date: 07/20/2015
ms.assetid: d991bc0f-d16a-4ac5-9351-70e5c5b9891b
ms.openlocfilehash: 532087f2ac32242b473d4524a6026519951d96d2
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100486805"
---
# <a name="reflection-visual-basic"></a><span data-ttu-id="addaa-103">反射 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="addaa-103">Reflection (Visual Basic)</span></span>

<span data-ttu-id="addaa-104">反射提供描述程序集、模块和类型的对象（<xref:System.Type> 类型）。</span><span class="sxs-lookup"><span data-stu-id="addaa-104">Reflection provides objects (of type <xref:System.Type>) that describe assemblies, modules and types.</span></span> <span data-ttu-id="addaa-105">可以使用反射动态地创建类型的实例，将类型绑定到现有对象，或从现有对象中获取类型，然后调用其方法或访问器字段和属性。</span><span class="sxs-lookup"><span data-stu-id="addaa-105">You can use reflection to dynamically create an instance of a type, bind the type to an existing object, or get the type from an existing object and invoke its methods or access its fields and properties.</span></span> <span data-ttu-id="addaa-106">如果代码中使用了特性，可以利用反射来访问它们。</span><span class="sxs-lookup"><span data-stu-id="addaa-106">If you are using attributes in your code, reflection enables you to access them.</span></span> <span data-ttu-id="addaa-107">有关更多信息，请参阅[特性](../../../standard/attributes/index.md)。</span><span class="sxs-lookup"><span data-stu-id="addaa-107">For more information, see [Attributes](../../../standard/attributes/index.md).</span></span>  
  
 <span data-ttu-id="addaa-108">下面一个简单的反射示例，使用静态方法 `GetType`被 `Object` 基类的所有类型继承）以获取变量类型：</span><span class="sxs-lookup"><span data-stu-id="addaa-108">Here's a simple example of reflection using the static method `GetType` - inherited by all types from the `Object` base class - to obtain the type of a variable:</span></span>  
  
```vb  
' Using GetType to obtain type information:  
Dim i As Integer = 42  
Dim type As System.Type = i.GetType()  
System.Console.WriteLine(type)  
```  
  
 <span data-ttu-id="addaa-109">输出为：</span><span class="sxs-lookup"><span data-stu-id="addaa-109">The output is:</span></span>  
  
 `System.Int32`  
  
 <span data-ttu-id="addaa-110">下面的示例使用反射获取已加载的程序集的完整名称。</span><span class="sxs-lookup"><span data-stu-id="addaa-110">The following example uses reflection to obtain the full name of the loaded assembly.</span></span>  
  
```vb  
' Using Reflection to get information from an Assembly:  
Dim info As System.Reflection.Assembly = GetType(System.Int32).Assembly  
System.Console.WriteLine(info)  
```  
  
 <span data-ttu-id="addaa-111">输出为：</span><span class="sxs-lookup"><span data-stu-id="addaa-111">The output is:</span></span>  
  
 `mscorlib, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089`  
  
## <a name="reflection-overview"></a><span data-ttu-id="addaa-112">反射概述</span><span class="sxs-lookup"><span data-stu-id="addaa-112">Reflection Overview</span></span>  

 <span data-ttu-id="addaa-113">反射在以下情况下很有用：</span><span class="sxs-lookup"><span data-stu-id="addaa-113">Reflection is useful in the following situations:</span></span>  
  
- <span data-ttu-id="addaa-114">需要访问程序元数据中的特性时。</span><span class="sxs-lookup"><span data-stu-id="addaa-114">When you have to access attributes in your program's metadata.</span></span> <span data-ttu-id="addaa-115">有关详细信息，请参阅[检索存储在特性中的信息](../../../standard/attributes/retrieving-information-stored-in-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="addaa-115">For more information, see [Retrieving Information Stored in Attributes](../../../standard/attributes/retrieving-information-stored-in-attributes.md).</span></span>  
  
- <span data-ttu-id="addaa-116">检查和实例化程序集中的类型。</span><span class="sxs-lookup"><span data-stu-id="addaa-116">For examining and instantiating types in an assembly.</span></span>  
  
- <span data-ttu-id="addaa-117">在运行时构建新类型。</span><span class="sxs-lookup"><span data-stu-id="addaa-117">For building new types at runtime.</span></span> <span data-ttu-id="addaa-118">使用 <xref:System.Reflection.Emit> 中的类。</span><span class="sxs-lookup"><span data-stu-id="addaa-118">Use classes in <xref:System.Reflection.Emit>.</span></span>  
  
- <span data-ttu-id="addaa-119">执行后期绑定，访问在运行时创建的类型上的方法。</span><span class="sxs-lookup"><span data-stu-id="addaa-119">For performing late binding, accessing methods on types created at run time.</span></span> <span data-ttu-id="addaa-120">请参阅主题 “[动态加载和使用类型](../../../framework/reflection-and-codedom/dynamically-loading-and-using-types.md)”。</span><span class="sxs-lookup"><span data-stu-id="addaa-120">See the topic [Dynamically Loading and Using Types](../../../framework/reflection-and-codedom/dynamically-loading-and-using-types.md).</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="addaa-121">相关章节</span><span class="sxs-lookup"><span data-stu-id="addaa-121">Related Sections</span></span>  

 <span data-ttu-id="addaa-122">更多相关信息：</span><span class="sxs-lookup"><span data-stu-id="addaa-122">For more information:</span></span>  
  
- [<span data-ttu-id="addaa-123">反射</span><span class="sxs-lookup"><span data-stu-id="addaa-123">Reflection</span></span>](../../../framework/reflection-and-codedom/reflection.md)  
  
- [<span data-ttu-id="addaa-124">查看类型信息</span><span class="sxs-lookup"><span data-stu-id="addaa-124">Viewing Type Information</span></span>](../../../framework/reflection-and-codedom/viewing-type-information.md)  
  
- [<span data-ttu-id="addaa-125">反射类型和泛型类型</span><span class="sxs-lookup"><span data-stu-id="addaa-125">Reflection and Generic Types</span></span>](../../../framework/reflection-and-codedom/reflection-and-generic-types.md)  
  
- <xref:System.Reflection.Emit>  
  
- [<span data-ttu-id="addaa-126">检索存储在特性中的信息</span><span class="sxs-lookup"><span data-stu-id="addaa-126">Retrieving Information Stored in Attributes</span></span>](../../../standard/attributes/retrieving-information-stored-in-attributes.md)  
  
## <a name="see-also"></a><span data-ttu-id="addaa-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="addaa-127">See also</span></span>

- [<span data-ttu-id="addaa-128">Visual Basic 编程指南</span><span class="sxs-lookup"><span data-stu-id="addaa-128">Visual Basic Programming Guide</span></span>](../index.md)
- [<span data-ttu-id="addaa-129">.NET 中的程序集</span><span class="sxs-lookup"><span data-stu-id="addaa-129">Assemblies in .NET</span></span>](../../../standard/assembly/index.md)
