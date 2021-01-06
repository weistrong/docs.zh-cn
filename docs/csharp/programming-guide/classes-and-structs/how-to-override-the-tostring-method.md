---
title: 如何替代 ToString 方法（C# 编程指南）
description: 了解如何替代 C# 中的 ToString 方法。 每个类或结构都继承对象并获取 ToString，后者返回该对象的字符串表示形式。
ms.date: 07/20/2015
helpviewer_keywords:
- ToString method, overriding in C#
- inheritance [C#], overriding OnPaint and ToString
ms.topic: how-to
ms.custom: contperf-fy21q2
ms.assetid: 8016db69-1f19-420c-8e17-98e8bebb7749
ms.openlocfilehash: 9573e6b97383d6f422c6a2802040fb9d6db709dd
ms.sourcegitcommit: d0990c1c1ab2f81908360f47eafa8db9aa165137
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/15/2020
ms.locfileid: "97512738"
---
# <a name="how-to-override-the-tostring-method-c-programming-guide"></a><span data-ttu-id="9f5d7-104">如何替代 ToString 方法（C# 编程指南）</span><span class="sxs-lookup"><span data-stu-id="9f5d7-104">How to override the ToString method (C# Programming Guide)</span></span>

<span data-ttu-id="9f5d7-105">C# 中的每个类或结构都可隐式继承 <xref:System.Object> 类。</span><span class="sxs-lookup"><span data-stu-id="9f5d7-105">Every class or struct in C# implicitly inherits the <xref:System.Object> class.</span></span> <span data-ttu-id="9f5d7-106">因此，C# 中的每个对象都会获取 <xref:System.Object.ToString%2A> 方法，该方法返回该对象的字符串表示形式。</span><span class="sxs-lookup"><span data-stu-id="9f5d7-106">Therefore, every object in C# gets the <xref:System.Object.ToString%2A> method, which returns a string representation of that object.</span></span> <span data-ttu-id="9f5d7-107">例如，类型为 `int` 的所有变量都有一个 `ToString` 方法，使它们可以将其内容作为字符串返回：</span><span class="sxs-lookup"><span data-stu-id="9f5d7-107">For example, all variables of type `int` have a `ToString` method, which enables them to return their contents as a string:</span></span>  
  
 [!code-csharp[csProgGuideInheritance#37](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideInheritance/CS/Inheritance.cs#37)]  
  
 <span data-ttu-id="9f5d7-108">创建自定义类或结构时，应替代 <xref:System.Object.ToString%2A> 方法，以向客户端代码提供有关你的类型的信息。</span><span class="sxs-lookup"><span data-stu-id="9f5d7-108">When you create a custom class or struct, you should override the <xref:System.Object.ToString%2A> method in order to provide information about your type to client code.</span></span>  
  
 <span data-ttu-id="9f5d7-109">若要深入了解如何通过 `ToString` 方法使用格式字符串和其他类型的自定义格式设置，请参阅[格式化类型](../../../standard/base-types/formatting-types.md)。</span><span class="sxs-lookup"><span data-stu-id="9f5d7-109">For information about how to use format strings and other types of custom formatting with the `ToString` method, see [Formatting Types](../../../standard/base-types/formatting-types.md).</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="9f5d7-110">决定通过此方法提供信息内容时，请考虑你的类或结构是否会被不受信任的代码使用。</span><span class="sxs-lookup"><span data-stu-id="9f5d7-110">When you decide what information to provide through this method, consider whether your class or struct will ever be used by untrusted code.</span></span> <span data-ttu-id="9f5d7-111">请务必确保不提供可能被恶意代码利用的任何信息。</span><span class="sxs-lookup"><span data-stu-id="9f5d7-111">Be careful to ensure that you do not provide any information that could be exploited by malicious code.</span></span>  
  
<span data-ttu-id="9f5d7-112">替代类或结构中的 `ToString` 方法：</span><span class="sxs-lookup"><span data-stu-id="9f5d7-112">To override the `ToString` method in your class or struct:</span></span>
  
1. <span data-ttu-id="9f5d7-113">声明具有下列修饰符和返回类型的 `ToString` 方法：</span><span class="sxs-lookup"><span data-stu-id="9f5d7-113">Declare a `ToString` method with the following modifiers and return type:</span></span>  
  
    ```csharp  
    public override string ToString(){}  
    ```  
  
2. <span data-ttu-id="9f5d7-114">实现该方法，使其返回一个字符串。</span><span class="sxs-lookup"><span data-stu-id="9f5d7-114">Implement the method so that it returns a string.</span></span>  
  
     <span data-ttu-id="9f5d7-115">下面的示例返回类的名称，但特定于该类的特定实例的数据除外。</span><span class="sxs-lookup"><span data-stu-id="9f5d7-115">The following example returns the name of the class in addition to the data specific to a particular instance of the class.</span></span>  
  
     [!code-csharp[csProgGuideInheritance#36](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideInheritance/CS/Inheritance.cs#36)]  
  
     <span data-ttu-id="9f5d7-116">可以测试 `ToString` 方法，如以下代码示例所示：</span><span class="sxs-lookup"><span data-stu-id="9f5d7-116">You can test the `ToString` method as shown in the following code example:</span></span>  
  
     [!code-csharp[csProgGuideInheritance#38](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideInheritance/CS/Inheritance.cs#38)]  
  
## <a name="see-also"></a><span data-ttu-id="9f5d7-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="9f5d7-117">See also</span></span>

- <xref:System.IFormattable>
- [<span data-ttu-id="9f5d7-118">C# 编程指南</span><span class="sxs-lookup"><span data-stu-id="9f5d7-118">C# Programming Guide</span></span>](../index.md)
- [<span data-ttu-id="9f5d7-119">类和结构</span><span class="sxs-lookup"><span data-stu-id="9f5d7-119">Classes and Structs</span></span>](./index.md)
- [<span data-ttu-id="9f5d7-120">字符串</span><span class="sxs-lookup"><span data-stu-id="9f5d7-120">Strings</span></span>](../strings/index.md)
- [<span data-ttu-id="9f5d7-121">string</span><span class="sxs-lookup"><span data-stu-id="9f5d7-121">string</span></span>](../../language-reference/builtin-types/reference-types.md)
- [<span data-ttu-id="9f5d7-122">override</span><span class="sxs-lookup"><span data-stu-id="9f5d7-122">override</span></span>](../../language-reference/keywords/override.md)
- [<span data-ttu-id="9f5d7-123">virtual</span><span class="sxs-lookup"><span data-stu-id="9f5d7-123">virtual</span></span>](../../language-reference/keywords/virtual.md)
- [<span data-ttu-id="9f5d7-124">格式设置类型</span><span class="sxs-lookup"><span data-stu-id="9f5d7-124">Formatting Types</span></span>](../../../standard/base-types/formatting-types.md)
