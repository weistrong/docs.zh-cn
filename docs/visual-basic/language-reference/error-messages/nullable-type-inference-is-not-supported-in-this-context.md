---
description: 了解详细信息： BC36629：在此上下文中不支持可以为 Null 的类型推理
title: 该上下文中不支持可以为 null 的类型推理
ms.date: 07/20/2015
f1_keywords:
- vbc36629
- bc36629
helpviewer_keywords:
- BC36629
ms.assetid: 0a1e2dbc-d9a4-433d-9306-c5540782b81d
ms.openlocfilehash: 915f964d55068f39b0468e2c47cc6e5538be1a6f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795620"
---
# <a name="bc36629-nullable-type-inference-is-not-supported-in-this-context"></a><span data-ttu-id="66a5f-103">BC36629：在此上下文中不支持可以为 Null 的类型推理</span><span class="sxs-lookup"><span data-stu-id="66a5f-103">BC36629: Nullable type inference is not supported in this context</span></span>

<span data-ttu-id="66a5f-104">值类型和结构可以声明为 null。</span><span class="sxs-lookup"><span data-stu-id="66a5f-104">Value types and structures can be declared nullable.</span></span>

```vb
Dim a? As Integer
Dim b As Integer?
```

 <span data-ttu-id="66a5f-105">但是，不能将可为 null 的声明与类型推理结合使用。</span><span class="sxs-lookup"><span data-stu-id="66a5f-105">However, you cannot use the nullable declaration in combination with type inference.</span></span> <span data-ttu-id="66a5f-106">下面的示例将导致此错误。</span><span class="sxs-lookup"><span data-stu-id="66a5f-106">The following examples cause this error.</span></span>

```vb
' Not valid.
' Dim c? = 10
' Dim d? = a
```

 <span data-ttu-id="66a5f-107">**错误 ID：** BC36629</span><span class="sxs-lookup"><span data-stu-id="66a5f-107">**Error ID:** BC36629</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="66a5f-108">更正此错误</span><span class="sxs-lookup"><span data-stu-id="66a5f-108">To correct this error</span></span>

- <span data-ttu-id="66a5f-109">使用 `As` 子句将变量声明为可以为 null 的值类型。</span><span class="sxs-lookup"><span data-stu-id="66a5f-109">Use an `As` clause to declare the variable as a nullable value type.</span></span>

## <a name="see-also"></a><span data-ttu-id="66a5f-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="66a5f-110">See also</span></span>

- [<span data-ttu-id="66a5f-111">可以为 null 的值类型</span><span class="sxs-lookup"><span data-stu-id="66a5f-111">Nullable Value Types</span></span>](../../programming-guide/language-features/data-types/nullable-value-types.md)
- [<span data-ttu-id="66a5f-112">局部类型推理</span><span class="sxs-lookup"><span data-stu-id="66a5f-112">Local Type Inference</span></span>](../../programming-guide/language-features/variables/local-type-inference.md)
