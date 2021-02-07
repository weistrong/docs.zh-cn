---
description: '了解有关以下内容的详细信息： Visual Basic 的派生数学函数 () '
title: 派生的数学函数
ms.date: 07/20/2015
helpviewer_keywords:
- arithmetic operations, derived math functions
- cosecant function
- arcsecant function
- arccotangent function
- functions [Visual Basic], derived math functions
- inverse functions
- math functions, derived
- derived math functions
- cotangent function
- angles
- secant function
- trigonometric functions
- logarithms
- arccosecant function
- hyperbolic functions
- arcsine function
- degrees
- arccosine function
ms.assetid: 63e449d8-9444-44fb-8db1-6d9cf346e2aa
ms.openlocfilehash: daaed1312f08cecc0c68af0e36d574424fc526a1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99730767"
---
# <a name="derived-math-functions-visual-basic"></a><span data-ttu-id="d3d7d-103">派生的数学函数 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d3d7d-103">Derived Math Functions (Visual Basic)</span></span>

<span data-ttu-id="d3d7d-104">下表显示了可以从对象的内部数学函数派生的非内部数学函数 <xref:System.Math?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="d3d7d-104">The following table shows non-intrinsic math functions that can be derived from the intrinsic math functions of the <xref:System.Math?displayProperty=nameWithType> object.</span></span> <span data-ttu-id="d3d7d-105">您可以通过将添加 `Imports System.Math` 到您的文件或项目来访问内部数学函数。</span><span class="sxs-lookup"><span data-stu-id="d3d7d-105">You can access the intrinsic math functions by adding `Imports System.Math` to your file or project.</span></span>  
  
|<span data-ttu-id="d3d7d-106">函数</span><span class="sxs-lookup"><span data-stu-id="d3d7d-106">Function</span></span>|<span data-ttu-id="d3d7d-107">派生等效项</span><span class="sxs-lookup"><span data-stu-id="d3d7d-107">Derived equivalents</span></span>|  
|--------------|-------------------------|  
|<span data-ttu-id="d3d7d-108">正割 (秒 (x) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-108">Secant (Sec(x))</span></span>|<span data-ttu-id="d3d7d-109">1/Cos (x) </span><span class="sxs-lookup"><span data-stu-id="d3d7d-109">1 / Cos(x)</span></span>|  
|<span data-ttu-id="d3d7d-110">余割 (Csc (x) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-110">Cosecant (Csc(x))</span></span>|<span data-ttu-id="d3d7d-111">1/Sin (x) </span><span class="sxs-lookup"><span data-stu-id="d3d7d-111">1 / Sin(x)</span></span>|  
|<span data-ttu-id="d3d7d-112">余切 (Ctan (x) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-112">Cotangent (Ctan(x))</span></span>|<span data-ttu-id="d3d7d-113">1/Tan (x) </span><span class="sxs-lookup"><span data-stu-id="d3d7d-113">1 / Tan(x)</span></span>|  
|<span data-ttu-id="d3d7d-114">反正弦 (Asin (x) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-114">Inverse sine (Asin(x))</span></span>|<span data-ttu-id="d3d7d-115">Atan (x/Sqrt (-x \* x + 1) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-115">Atan(x / Sqrt(-x \* x + 1))</span></span>|  
|<span data-ttu-id="d3d7d-116">反余弦 (Acos (x) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-116">Inverse cosine (Acos(x))</span></span>|<span data-ttu-id="d3d7d-117">Atan (-x/Sqrt (-x \* x + 1) # A3 + 2 \* Atan (1) </span><span class="sxs-lookup"><span data-stu-id="d3d7d-117">Atan(-x / Sqrt(-x \* x + 1)) + 2 \* Atan(1)</span></span>|  
|<span data-ttu-id="d3d7d-118">反割 (Asec (x) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-118">Inverse secant (Asec(x))</span></span>|<span data-ttu-id="d3d7d-119">2 \* Atan (1) – Atan (号 (x) /Sqrt (x \* x – 1) # A7</span><span class="sxs-lookup"><span data-stu-id="d3d7d-119">2 \* Atan(1) – Atan(Sign(x) / Sqrt(x \* x – 1))</span></span>|  
|<span data-ttu-id="d3d7d-120">反向余割 (Acsc (x) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-120">Inverse cosecant (Acsc(x))</span></span>|<span data-ttu-id="d3d7d-121">Atan (Sign (x) /Sqrt (x \* x – 1) # A5</span><span class="sxs-lookup"><span data-stu-id="d3d7d-121">Atan(Sign(x) / Sqrt(x \* x – 1))</span></span>|  
|<span data-ttu-id="d3d7d-122">反余切 (Acot (x) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-122">Inverse cotangent (Acot(x))</span></span>|<span data-ttu-id="d3d7d-123">2 \* Atan (1) -Atan (x) </span><span class="sxs-lookup"><span data-stu-id="d3d7d-123">2 \* Atan(1) - Atan(x)</span></span>|  
|<span data-ttu-id="d3d7d-124">双曲正弦 (Sinh (x) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-124">Hyperbolic sine (Sinh(x))</span></span>|<span data-ttu-id="d3d7d-125"> (Exp (x) – Exp (-x) # A5/2</span><span class="sxs-lookup"><span data-stu-id="d3d7d-125">(Exp(x) – Exp(-x)) / 2</span></span>|  
|<span data-ttu-id="d3d7d-126">双曲余弦 (Cosh (x) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-126">Hyperbolic cosine (Cosh(x))</span></span>|<span data-ttu-id="d3d7d-127"> (Exp (x) + Exp (-x) # A5/2</span><span class="sxs-lookup"><span data-stu-id="d3d7d-127">(Exp(x) + Exp(-x)) / 2</span></span>|  
|<span data-ttu-id="d3d7d-128"> (Tanh (x 的双曲正切值) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-128">Hyperbolic tangent (Tanh(x))</span></span>|<span data-ttu-id="d3d7d-129"> (Exp (x) – Exp (-x) # A5/ (Exp (x) + Exp (-x) # A11</span><span class="sxs-lookup"><span data-stu-id="d3d7d-129">(Exp(x) – Exp(-x)) / (Exp(x) + Exp(-x))</span></span>|  
|<span data-ttu-id="d3d7d-130">双曲正则 (Sech (x) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-130">Hyperbolic secant (Sech(x))</span></span>|<span data-ttu-id="d3d7d-131">2/ (Exp (x) + Exp (-x) # A5</span><span class="sxs-lookup"><span data-stu-id="d3d7d-131">2 / (Exp(x) + Exp(-x))</span></span>|  
|<span data-ttu-id="d3d7d-132">双曲余割 (Csch (x) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-132">Hyperbolic cosecant (Csch(x))</span></span>|<span data-ttu-id="d3d7d-133">2/ (Exp (x) – Exp (-x) # A5</span><span class="sxs-lookup"><span data-stu-id="d3d7d-133">2 / (Exp(x) – Exp(-x))</span></span>|  
|<span data-ttu-id="d3d7d-134">双曲余切 (Coth (x) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-134">Hyperbolic cotangent (Coth(x))</span></span>|<span data-ttu-id="d3d7d-135"> (Exp (x) + Exp (-x) # A5/ (Exp (x) – Exp (-x) # A11</span><span class="sxs-lookup"><span data-stu-id="d3d7d-135">(Exp(x) + Exp(-x)) / (Exp(x) – Exp(-x))</span></span>|  
|<span data-ttu-id="d3d7d-136">反双曲正弦 (Asinh (x) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-136">Inverse hyperbolic sine (Asinh(x))</span></span>|<span data-ttu-id="d3d7d-137">记录 (x + Sqrt (x \* x + 1) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-137">Log(x + Sqrt(x \* x + 1))</span></span>|  
|<span data-ttu-id="d3d7d-138">反双曲余弦 (Acosh (x) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-138">Inverse hyperbolic cosine (Acosh(x))</span></span>|<span data-ttu-id="d3d7d-139">记录 (x + Sqrt (x \* x – 1) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-139">Log(x + Sqrt(x \* x – 1))</span></span>|  
|<span data-ttu-id="d3d7d-140">反双曲正切值 (Atanh (x) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-140">Inverse hyperbolic tangent (Atanh(x))</span></span>|<span data-ttu-id="d3d7d-141">日志 ( # B1 1 + x) / (1 – x) # A5/2</span><span class="sxs-lookup"><span data-stu-id="d3d7d-141">Log((1 + x) / (1 – x)) / 2</span></span>|  
|<span data-ttu-id="d3d7d-142">反双曲正割 (AsecH (x) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-142">Inverse hyperbolic secant (AsecH(x))</span></span>|<span data-ttu-id="d3d7d-143">日志 ( # B1 Sqrt (-x \* x + 1) + 1) /x) </span><span class="sxs-lookup"><span data-stu-id="d3d7d-143">Log((Sqrt(-x \* x + 1) + 1) / x)</span></span>|  
|<span data-ttu-id="d3d7d-144">反双曲余割 (Acsch (x) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-144">Inverse hyperbolic cosecant (Acsch(x))</span></span>|<span data-ttu-id="d3d7d-145">日志 ( # B1 Sign (x) \* Sqrt (x \* x + 1) + 1) /x) </span><span class="sxs-lookup"><span data-stu-id="d3d7d-145">Log((Sign(x) \* Sqrt(x \* x + 1) + 1) / x)</span></span>|  
|<span data-ttu-id="d3d7d-146">反双曲余切 (Acoth (x) # A3</span><span class="sxs-lookup"><span data-stu-id="d3d7d-146">Inverse hyperbolic cotangent (Acoth(x))</span></span>|<span data-ttu-id="d3d7d-147">日志 ( # B1 x + 1) / (x – 1) # A5/2</span><span class="sxs-lookup"><span data-stu-id="d3d7d-147">Log((x + 1) / (x – 1)) / 2</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d3d7d-148">请参阅</span><span class="sxs-lookup"><span data-stu-id="d3d7d-148">See also</span></span>

- [<span data-ttu-id="d3d7d-149">数学函数</span><span class="sxs-lookup"><span data-stu-id="d3d7d-149">Math Functions</span></span>](../functions/math-functions.md)
