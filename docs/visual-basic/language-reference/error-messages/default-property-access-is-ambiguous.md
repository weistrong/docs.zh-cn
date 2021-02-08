---
description: 了解更多相关信息： BC30686：默认属性访问在 <defaultpropertyname> 接口 "" 的继承接口成员 "" <interfacename1> 和接口 "" <defaultpropertyname> 的 "" 之间不明确<interfacename2>
title: 默认属性访问在接口“<defaultpropertyname>”的继承接口成员“<interfacename1>”和接口“<defaultpropertyname>”的“<interfacename2>”之间不明确
ms.date: 07/20/2015
f1_keywords:
- vbc30686
- bc30686
helpviewer_keywords:
- BC30686
ms.assetid: 784fefec-ef57-48cf-b960-957df419b439
ms.openlocfilehash: 5ae5e5b2dc7a61540e26d125e960d4755141d975
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796647"
---
# <a name="bc30686-default-property-access-is-ambiguous-between-the-inherited-interface-members-defaultpropertyname-of-interface-interfacename1-and-defaultpropertyname-of-interface-interfacename2"></a><span data-ttu-id="2019d-103">BC30686：默认属性访问在接口 "" 的继承接口成员 "" \<defaultpropertyname> \<interfacename1> 和 \<defaultpropertyname> 接口 "" 的 " \<interfacename2> " 之间不明确</span><span class="sxs-lookup"><span data-stu-id="2019d-103">BC30686: Default property access is ambiguous between the inherited interface members '\<defaultpropertyname>' of interface '\<interfacename1>' and '\<defaultpropertyname>' of interface '\<interfacename2>'</span></span>

<span data-ttu-id="2019d-104">接口继承自两个接口，每个接口都声明一个具有相同名称的默认属性。</span><span class="sxs-lookup"><span data-stu-id="2019d-104">An interface inherits from two interfaces, each of which declares a default property with the same name.</span></span> <span data-ttu-id="2019d-105">编译器无法解析对此默认属性的访问，无需进行限定。</span><span class="sxs-lookup"><span data-stu-id="2019d-105">The compiler cannot resolve an access to this default property without qualification.</span></span> <span data-ttu-id="2019d-106">下面的示例阐释了这一点。</span><span class="sxs-lookup"><span data-stu-id="2019d-106">The following example illustrates this.</span></span>

```vb
Public Interface Iface1
    Default Property prop(ByVal arg As Integer) As Integer
End Interface
Public Interface Iface2
    Default Property prop(ByVal arg As Integer) As Integer
End Interface
Public Interface Iface3
    Inherits Iface1, Iface2
End Interface
Public Class testClass
    Public Sub accessDefaultProperty()
        Dim testObj As Iface3
        Dim testInt As Integer = testObj(1)
    End Sub
End Class
```

<span data-ttu-id="2019d-107">指定时 `testObj(1)` ，编译器会尝试将其解析为默认属性。</span><span class="sxs-lookup"><span data-stu-id="2019d-107">When you specify `testObj(1)`, the compiler tries to resolve it to the default property.</span></span> <span data-ttu-id="2019d-108">不过，由于继承了接口，有两个可能的默认属性，因此编译器会发出此错误信号。</span><span class="sxs-lookup"><span data-stu-id="2019d-108">However, there are two possible default properties because of the inherited interfaces, so the compiler signals this error.</span></span>

<span data-ttu-id="2019d-109">**错误 ID：** BC30686</span><span class="sxs-lookup"><span data-stu-id="2019d-109">**Error ID:** BC30686</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="2019d-110">更正此错误</span><span class="sxs-lookup"><span data-stu-id="2019d-110">To correct this error</span></span>

- <span data-ttu-id="2019d-111">避免继承任何具有相同名称的成员。</span><span class="sxs-lookup"><span data-stu-id="2019d-111">Avoid inheriting any members with the same name.</span></span> <span data-ttu-id="2019d-112">在前面的示例中，如果 `testObj` 不需要的任何成员（例如），请按 `Iface2` 如下所示声明：</span><span class="sxs-lookup"><span data-stu-id="2019d-112">In the preceding example, if `testObj` does not need any of the members of, say, `Iface2`, then declare it as follows:</span></span>

  ```vb
  Dim testObj As Iface1
  ```

  <span data-ttu-id="2019d-113">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="2019d-113">\-or-</span></span>

- <span data-ttu-id="2019d-114">在类中实现继承接口。</span><span class="sxs-lookup"><span data-stu-id="2019d-114">Implement the inheriting interface in a class.</span></span> <span data-ttu-id="2019d-115">然后，可以用不同的名称实现每个继承的属性。</span><span class="sxs-lookup"><span data-stu-id="2019d-115">Then you can implement each of the inherited properties with different names.</span></span> <span data-ttu-id="2019d-116">但是，其中只有一个可以是实现类的默认属性。</span><span class="sxs-lookup"><span data-stu-id="2019d-116">However, only one of them can be the default property of the implementing class.</span></span> <span data-ttu-id="2019d-117">下面的示例阐释了这一点。</span><span class="sxs-lookup"><span data-stu-id="2019d-117">The following example illustrates this.</span></span>

  ```vb
  Public Class useIface3
      Implements Iface3
      Default Public Property prop1(ByVal arg As Integer) As Integer Implements Iface1.prop
          ' Insert code to define Get and Set procedures for prop1.
      End Property
      Public Property prop2(ByVal arg As Integer) As Integer Implements Iface2.prop
          ' Insert code to define Get and Set procedures for prop2.
      End Property
  End Class
  ```

## <a name="see-also"></a><span data-ttu-id="2019d-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="2019d-118">See also</span></span>

- [<span data-ttu-id="2019d-119">接口</span><span class="sxs-lookup"><span data-stu-id="2019d-119">Interfaces</span></span>](../../programming-guide/language-features/interfaces/index.md)
