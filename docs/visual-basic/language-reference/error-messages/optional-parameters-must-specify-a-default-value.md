---
description: 了解详细信息： BC30812：可选参数必须指定默认值
title: 可选参数必须指定默认值
ms.date: 07/20/2015
f1_keywords:
- vbc30812
- bc30812
helpviewer_keywords:
- BC30812
ms.assetid: 5091a250-be66-413b-98a3-2a9974c4d600
ms.openlocfilehash: 1cbed1c0f1297ecacdae94d9234d18a3d268f487
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795529"
---
# <a name="bc30812-optional-parameters-must-specify-a-default-value"></a><span data-ttu-id="6ae13-103">BC30812：可选参数必须指定默认值</span><span class="sxs-lookup"><span data-stu-id="6ae13-103">BC30812: Optional parameters must specify a default value</span></span>

<span data-ttu-id="6ae13-104">可选参数必须提供默认值，如果调用过程未提供任何参数，则可以使用这些默认值。</span><span class="sxs-lookup"><span data-stu-id="6ae13-104">Optional parameters must provide default values that can be used if no parameter is supplied by a calling procedure.</span></span>

<span data-ttu-id="6ae13-105">**错误 ID：** BC30812</span><span class="sxs-lookup"><span data-stu-id="6ae13-105">**Error ID:** BC30812</span></span>

## <a name="example"></a><span data-ttu-id="6ae13-106">示例</span><span class="sxs-lookup"><span data-stu-id="6ae13-106">Example</span></span>

<span data-ttu-id="6ae13-107">下面的示例生成 BC30812：</span><span class="sxs-lookup"><span data-stu-id="6ae13-107">The following example generates BC30812:</span></span>

```vb
Sub Proc1(x As Integer, Optional y As String)
    Console.WriteLine("Default argument is: " & y)
End Sub
```

## <a name="to-correct-this-error"></a><span data-ttu-id="6ae13-108">更正此错误</span><span class="sxs-lookup"><span data-stu-id="6ae13-108">To correct this error</span></span>

<span data-ttu-id="6ae13-109">指定可选参数的默认值：</span><span class="sxs-lookup"><span data-stu-id="6ae13-109">Specify default values for optional parameters:</span></span>

```vb
Sub Proc1(x As Integer, Optional y As String = "Default Value")
    Console.WriteLine("Default argument is: " & y)
End Sub
```

## <a name="see-also"></a><span data-ttu-id="6ae13-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="6ae13-110">See also</span></span>

- [<span data-ttu-id="6ae13-111">可选</span><span class="sxs-lookup"><span data-stu-id="6ae13-111">Optional</span></span>](../modifiers/optional.md)
