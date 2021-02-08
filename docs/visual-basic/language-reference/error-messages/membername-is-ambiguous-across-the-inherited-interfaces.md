---
description: 了解更多相关信息： BC30685： " <membername> " 在继承接口 " <interfacename1> " 和 "之间不明确<interfacename2>
title: “<membername>”在继承接口“<interfacename1>”和“<interfacename2>”之间不明确
ms.date: 07/20/2015
f1_keywords:
- vbc30685
- bc30685
helpviewer_keywords:
- BC30685
ms.assetid: 756add7a-23d5-4b4f-a48d-8297d6459c73
ms.openlocfilehash: 8d114755c4456c7e846c2e9570481abfd5d13bbf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795828"
---
# <a name="bc30685-membername-is-ambiguous-across-the-inherited-interfaces-interfacename1-and-interfacename2"></a><span data-ttu-id="4939f-103">BC30685： " \<membername> " 在继承接口 " \<interfacename1> " 和 "" 之间不 \<interfacename2> 明确</span><span class="sxs-lookup"><span data-stu-id="4939f-103">BC30685: '\<membername>' is ambiguous across the inherited interfaces '\<interfacename1>' and '\<interfacename2>'</span></span>

<span data-ttu-id="4939f-104">接口从多个接口继承具有相同名称的两个或多个成员。</span><span class="sxs-lookup"><span data-stu-id="4939f-104">The interface inherits two or more members with the same name from multiple interfaces.</span></span>

 <span data-ttu-id="4939f-105">**错误 ID：** BC30685</span><span class="sxs-lookup"><span data-stu-id="4939f-105">**Error ID:** BC30685</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="4939f-106">更正此错误</span><span class="sxs-lookup"><span data-stu-id="4939f-106">To correct this error</span></span>

- <span data-ttu-id="4939f-107">将值强制转换为要使用的基接口;例如：</span><span class="sxs-lookup"><span data-stu-id="4939f-107">Cast the value to the base interface that you want to use; for example:</span></span>

    ```vb
    Interface Left
        Sub MySub()
    End Interface

    Interface Right
        Sub MySub()
    End Interface

    Interface LeftRight
        Inherits Left, Right
    End Interface

    Module test
        Sub Main()
            Dim x As LeftRight
            ' x.MySub()  'x is ambiguous.
            CType(x, Left).MySub() ' Cast to base type.
            CType(x, Right).MySub() ' Call the other base type.
        End Sub
    End Module
    ```

## <a name="see-also"></a><span data-ttu-id="4939f-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="4939f-108">See also</span></span>

- [<span data-ttu-id="4939f-109">接口</span><span class="sxs-lookup"><span data-stu-id="4939f-109">Interfaces</span></span>](../../programming-guide/language-features/interfaces/index.md)
