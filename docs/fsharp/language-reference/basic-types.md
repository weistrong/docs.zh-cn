---
title: 基本类型
description: '了解 F # 语言中使用的基本基本类型。'
ms.date: 08/15/2020
ms.openlocfilehash: 2bfc9ba9370cb8ba1fcc1d42369c2551cbb57623
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100456908"
---
# <a name="basic-types"></a><span data-ttu-id="79daf-103">基本类型</span><span class="sxs-lookup"><span data-stu-id="79daf-103">Basic types</span></span>

<span data-ttu-id="79daf-104">本主题列出了在 F # 语言中定义的基本类型。</span><span class="sxs-lookup"><span data-stu-id="79daf-104">This topic lists the basic types that are defined in the F# language.</span></span> <span data-ttu-id="79daf-105">这些类型在 F # 中是最基本的，构成了几乎每个 F # 程序的基础。</span><span class="sxs-lookup"><span data-stu-id="79daf-105">These types are the most fundamental in F#, forming the basis of nearly every F# program.</span></span> <span data-ttu-id="79daf-106">它们是 .NET 基元类型的超集。</span><span class="sxs-lookup"><span data-stu-id="79daf-106">They are a superset of .NET primitive types.</span></span>

|<span data-ttu-id="79daf-107">类型</span><span class="sxs-lookup"><span data-stu-id="79daf-107">Type</span></span>|<span data-ttu-id="79daf-108">.NET 类型</span><span class="sxs-lookup"><span data-stu-id="79daf-108">.NET type</span></span>|<span data-ttu-id="79daf-109">说明</span><span class="sxs-lookup"><span data-stu-id="79daf-109">Description</span></span>|<span data-ttu-id="79daf-110">示例</span><span class="sxs-lookup"><span data-stu-id="79daf-110">Example</span></span>|
|----|---------|-----------|-------|
|`bool`|<xref:System.Boolean>|<span data-ttu-id="79daf-111">可能值为 `true` 和 `false`。</span><span class="sxs-lookup"><span data-stu-id="79daf-111">Possible values are `true` and `false`.</span></span>|`true`/`false`|
|`byte`|<xref:System.Byte>|<span data-ttu-id="79daf-112">介于0到255之间的值。</span><span class="sxs-lookup"><span data-stu-id="79daf-112">Values from 0 to 255.</span></span>|`1uy`|
|`sbyte`|<xref:System.SByte>|<span data-ttu-id="79daf-113">值从-128 到127。</span><span class="sxs-lookup"><span data-stu-id="79daf-113">Values from -128 to 127.</span></span>|`1y`|
|`int16`|<xref:System.Int16>|<span data-ttu-id="79daf-114">值从-32768 到32767。</span><span class="sxs-lookup"><span data-stu-id="79daf-114">Values from -32768 to 32767.</span></span>|`1s`|
|`uint16`|<xref:System.UInt16>|<span data-ttu-id="79daf-115">介于0到65535之间的值。</span><span class="sxs-lookup"><span data-stu-id="79daf-115">Values from 0 to 65535.</span></span>|`1us`|
|`int`|<xref:System.Int32>|<span data-ttu-id="79daf-116">值从-2147483648 到2147483647。</span><span class="sxs-lookup"><span data-stu-id="79daf-116">Values from -2,147,483,648 to 2,147,483,647.</span></span>|`1`|
|`uint`|<xref:System.UInt32>|<span data-ttu-id="79daf-117">介于0到4294967295之间的值。</span><span class="sxs-lookup"><span data-stu-id="79daf-117">Values from 0 to 4,294,967,295.</span></span>|`1u`|
|`int64`|<xref:System.Int64>|<span data-ttu-id="79daf-118">值介于-9223372036854775808 到9223372036854775807之间。</span><span class="sxs-lookup"><span data-stu-id="79daf-118">Values from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807.</span></span>|`1L`|
|`uint64`|<xref:System.UInt64>|<span data-ttu-id="79daf-119">介于0到18446744073709551615之间的值。</span><span class="sxs-lookup"><span data-stu-id="79daf-119">Values from 0 to 18,446,744,073,709,551,615.</span></span>|`1UL`|
|`nativeint`|<xref:System.IntPtr>|<span data-ttu-id="79daf-120">作为带符号整数的本机指针。</span><span class="sxs-lookup"><span data-stu-id="79daf-120">A native pointer as a signed integer.</span></span>|`nativeint 1`|
|`unativeint`|<xref:System.UIntPtr>|<span data-ttu-id="79daf-121">作为无符号整数的本机指针。</span><span class="sxs-lookup"><span data-stu-id="79daf-121">A native pointer as an unsigned integer.</span></span>|`unativeint 1`|
|`decimal`|<xref:System.Decimal>|<span data-ttu-id="79daf-122">至少具有28个有效数字的浮点数据类型。</span><span class="sxs-lookup"><span data-stu-id="79daf-122">A floating point data type that has at least 28 significant digits.</span></span>|`1.0`|
|<span data-ttu-id="79daf-123">`float`, `double`</span><span class="sxs-lookup"><span data-stu-id="79daf-123">`float`, `double`</span></span>|<xref:System.Double>|<span data-ttu-id="79daf-124">64位浮点类型。</span><span class="sxs-lookup"><span data-stu-id="79daf-124">A 64-bit floating point type.</span></span>|`1.0`|
|<span data-ttu-id="79daf-125">`float32`, `single`</span><span class="sxs-lookup"><span data-stu-id="79daf-125">`float32`, `single`</span></span>|<xref:System.Single>|<span data-ttu-id="79daf-126">32位浮点类型。</span><span class="sxs-lookup"><span data-stu-id="79daf-126">A 32-bit floating point type.</span></span>|`1.0f`|
|`char`|<xref:System.Char>|<span data-ttu-id="79daf-127">Unicode 字符值。</span><span class="sxs-lookup"><span data-stu-id="79daf-127">Unicode character values.</span></span>|`'c'`|
|`string`|<xref:System.String>|<span data-ttu-id="79daf-128">Unicode 文本。</span><span class="sxs-lookup"><span data-stu-id="79daf-128">Unicode text.</span></span>|`"str"`|
|`unit`|<span data-ttu-id="79daf-129">不适用</span><span class="sxs-lookup"><span data-stu-id="79daf-129">not applicable</span></span>|<span data-ttu-id="79daf-130">指示缺少实际值。</span><span class="sxs-lookup"><span data-stu-id="79daf-130">Indicates the absence of an actual value.</span></span> <span data-ttu-id="79daf-131">该类型仅有一个表示的形式值 `()` 。</span><span class="sxs-lookup"><span data-stu-id="79daf-131">The type has only one formal value, which is denoted `()`.</span></span> <span data-ttu-id="79daf-132">Unit 值通常用作 `()` 占位符，其中需要值，但没有实际值可用或有意义。</span><span class="sxs-lookup"><span data-stu-id="79daf-132">The unit value, `()`, is often used as a placeholder where a value is needed but no real value is available or makes sense.</span></span>|`()`|

> [!NOTE]
> <span data-ttu-id="79daf-133">您可以使用类型对64位整数类型的整数进行太大的计算 `bigint` 。</span><span class="sxs-lookup"><span data-stu-id="79daf-133">You can perform computations with integers too big for the 64-bit integer type by using the `bigint` type.</span></span> <span data-ttu-id="79daf-134">`bigint` 不被视为基本类型;它是的缩写 `System.Numerics.BigInteger` 。</span><span class="sxs-lookup"><span data-stu-id="79daf-134">`bigint` is not considered a basic type; it is an abbreviation for `System.Numerics.BigInteger`.</span></span>

## <a name="see-also"></a><span data-ttu-id="79daf-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="79daf-135">See also</span></span>

- [<span data-ttu-id="79daf-136">F# 语言参考</span><span class="sxs-lookup"><span data-stu-id="79daf-136">F# Language Reference</span></span>](index.md)
