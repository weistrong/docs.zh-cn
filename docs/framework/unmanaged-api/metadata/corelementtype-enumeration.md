---
description: 了解详细信息： CorElementType 枚举
title: CorElementType 枚举
ms.date: 03/30/2017
api_name:
- CorElementType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorElementType
helpviewer_keywords:
- CorElementType enumeration [.NET Framework metadata]
ms.assetid: c3809c8f-1737-4f0f-9442-0c01ee689871
topic_type:
- apiref
ms.openlocfilehash: 3eaf75a6d2094ec875ab1861aac49e4382e65801
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784526"
---
# <a name="corelementtype-enumeration"></a><span data-ttu-id="9460c-103">CorElementType 枚举</span><span class="sxs-lookup"><span data-stu-id="9460c-103">CorElementType Enumeration</span></span>

<span data-ttu-id="9460c-104">指定公共语言运行时 <xref:System.Type> 、类型修饰符或元数据类型签名中的类型的相关信息。</span><span class="sxs-lookup"><span data-stu-id="9460c-104">Specifies a common language runtime <xref:System.Type>, a type modifier, or information about a type in a metadata type signature.</span></span>

## <a name="syntax"></a><span data-ttu-id="9460c-105">语法</span><span class="sxs-lookup"><span data-stu-id="9460c-105">Syntax</span></span>

```cpp
typedef enum CorElementType {
    ELEMENT_TYPE_END            = 0x0,
    ELEMENT_TYPE_VOID           = 0x1,
    ELEMENT_TYPE_BOOLEAN        = 0x2,
    ELEMENT_TYPE_CHAR           = 0x3,
    ELEMENT_TYPE_I1             = 0x4,
    ELEMENT_TYPE_U1             = 0x5,
    ELEMENT_TYPE_I2             = 0x6,
    ELEMENT_TYPE_U2             = 0x7,
    ELEMENT_TYPE_I4             = 0x8,
    ELEMENT_TYPE_U4             = 0x9,
    ELEMENT_TYPE_I8             = 0xa,
    ELEMENT_TYPE_U8             = 0xb,
    ELEMENT_TYPE_R4             = 0xc,
    ELEMENT_TYPE_R8             = 0xd,
    ELEMENT_TYPE_STRING         = 0xe,

    ELEMENT_TYPE_PTR            = 0xf,
    ELEMENT_TYPE_BYREF          = 0x10,

    ELEMENT_TYPE_VALUETYPE      = 0x11,
    ELEMENT_TYPE_CLASS          = 0x12,
    ELEMENT_TYPE_VAR            = 0x13,
    ELEMENT_TYPE_ARRAY          = 0x14,
    ELEMENT_TYPE_GENERICINST    = 0x15,
    ELEMENT_TYPE_TYPEDBYREF     = 0x16,

    ELEMENT_TYPE_I              = 0x18,
    ELEMENT_TYPE_U              = 0x19,
    ELEMENT_TYPE_FNPTR          = 0x1B,
    ELEMENT_TYPE_OBJECT         = 0x1C,
    ELEMENT_TYPE_SZARRAY        = 0x1D,
    ELEMENT_TYPE_MVAR           = 0x1e,

    ELEMENT_TYPE_CMOD_REQD      = 0x1F,
    ELEMENT_TYPE_CMOD_OPT       = 0x20,

    ELEMENT_TYPE_INTERNAL       = 0x21,
    ELEMENT_TYPE_MAX            = 0x22,

    ELEMENT_TYPE_MODIFIER       = 0x40,
    ELEMENT_TYPE_SENTINEL       = 0x01 | ELEMENT_TYPE_MODIFIER,
    ELEMENT_TYPE_PINNED         = 0x05 | ELEMENT_TYPE_MODIFIER

} CorElementType;
```

## <a name="members"></a><span data-ttu-id="9460c-106">成员</span><span class="sxs-lookup"><span data-stu-id="9460c-106">Members</span></span>

|<span data-ttu-id="9460c-107">成员</span><span class="sxs-lookup"><span data-stu-id="9460c-107">Member</span></span>|<span data-ttu-id="9460c-108">说明</span><span class="sxs-lookup"><span data-stu-id="9460c-108">Description</span></span>|
|------------|-----------------|
|`ELEMENT_TYPE_END`|<span data-ttu-id="9460c-109">内部使用。</span><span class="sxs-lookup"><span data-stu-id="9460c-109">Used internally.</span></span>|
|`ELEMENT_TYPE_VOID`|<span data-ttu-id="9460c-110">Void 类型。</span><span class="sxs-lookup"><span data-stu-id="9460c-110">A void type.</span></span>|
|`ELEMENT_TYPE_BOOLEAN`|<span data-ttu-id="9460c-111">布尔类型</span><span class="sxs-lookup"><span data-stu-id="9460c-111">A Boolean type</span></span>|
|`ELEMENT_TYPE_CHAR`|<span data-ttu-id="9460c-112">一个字符类型。</span><span class="sxs-lookup"><span data-stu-id="9460c-112">A character type.</span></span>|
|`ELEMENT_TYPE_I1`|<span data-ttu-id="9460c-113">有符号1字节整数。</span><span class="sxs-lookup"><span data-stu-id="9460c-113">A signed 1-byte integer.</span></span>|
|`ELEMENT_TYPE_U1`|<span data-ttu-id="9460c-114">1 字节无符号整数。</span><span class="sxs-lookup"><span data-stu-id="9460c-114">An unsigned 1-byte integer.</span></span>|
|`ELEMENT_TYPE_I2`|<span data-ttu-id="9460c-115">有符号的2字节整数。</span><span class="sxs-lookup"><span data-stu-id="9460c-115">A signed 2-byte integer.</span></span>|
|`ELEMENT_TYPE_U2`|<span data-ttu-id="9460c-116">无符号2字节整数。</span><span class="sxs-lookup"><span data-stu-id="9460c-116">An unsigned 2-byte integer.</span></span>|
|`ELEMENT_TYPE_I4`|<span data-ttu-id="9460c-117">有符号4字节整数。</span><span class="sxs-lookup"><span data-stu-id="9460c-117">A signed 4-byte integer.</span></span>|
|`ELEMENT_TYPE_U4`|<span data-ttu-id="9460c-118">4字节无符号整数。</span><span class="sxs-lookup"><span data-stu-id="9460c-118">An unsigned 4-byte integer.</span></span>|
|`ELEMENT_TYPE_I8`|<span data-ttu-id="9460c-119">8字节有符号整数。</span><span class="sxs-lookup"><span data-stu-id="9460c-119">A signed 8-byte integer.</span></span>|
|`ELEMENT_TYPE_U8`|<span data-ttu-id="9460c-120">8字节无符号整数。</span><span class="sxs-lookup"><span data-stu-id="9460c-120">An unsigned 8-byte integer.</span></span>|
|`ELEMENT_TYPE_R4`|<span data-ttu-id="9460c-121">4字节浮点数。</span><span class="sxs-lookup"><span data-stu-id="9460c-121">A 4-byte floating point.</span></span>|
|`ELEMENT_TYPE_R8`|<span data-ttu-id="9460c-122">8字节浮点数。</span><span class="sxs-lookup"><span data-stu-id="9460c-122">An 8-byte floating point.</span></span>|
|`ELEMENT_TYPE_STRING`|<span data-ttu-id="9460c-123">System.string 类型。</span><span class="sxs-lookup"><span data-stu-id="9460c-123">A System.String type.</span></span>|
|`ELEMENT_TYPE_PTR`|<span data-ttu-id="9460c-124">指针类型修饰符。</span><span class="sxs-lookup"><span data-stu-id="9460c-124">A pointer type modifier.</span></span>|
|`ELEMENT_TYPE_BYREF`|<span data-ttu-id="9460c-125">引用类型修饰符。</span><span class="sxs-lookup"><span data-stu-id="9460c-125">A reference type modifier.</span></span>|
|`ELEMENT_TYPE_VALUETYPE`|<span data-ttu-id="9460c-126">值类型修饰符。</span><span class="sxs-lookup"><span data-stu-id="9460c-126">A value type modifier.</span></span>|
|`ELEMENT_TYPE_CLASS`|<span data-ttu-id="9460c-127">类类型修饰符。</span><span class="sxs-lookup"><span data-stu-id="9460c-127">A class type modifier.</span></span>|
|`ELEMENT_TYPE_VAR`|<span data-ttu-id="9460c-128">类变量类型修饰符。</span><span class="sxs-lookup"><span data-stu-id="9460c-128">A class variable type modifier.</span></span>|
|`ELEMENT_TYPE_ARRAY`|<span data-ttu-id="9460c-129">多维数组类型修饰符。</span><span class="sxs-lookup"><span data-stu-id="9460c-129">A multi-dimensional array type modifier.</span></span>|
|`ELEMENT_TYPE_GENERICINST`|<span data-ttu-id="9460c-130">泛型类型的类型修饰符。</span><span class="sxs-lookup"><span data-stu-id="9460c-130">A type modifier for generic types.</span></span>|
|`ELEMENT_TYPE_TYPEDBYREF`|<span data-ttu-id="9460c-131">类型化的引用。</span><span class="sxs-lookup"><span data-stu-id="9460c-131">A typed reference.</span></span>|
|`ELEMENT_TYPE_I`|<span data-ttu-id="9460c-132">本机整数的大小。</span><span class="sxs-lookup"><span data-stu-id="9460c-132">Size of a native integer.</span></span>|
|`ELEMENT_TYPE_U`|<span data-ttu-id="9460c-133">无符号本机整数的大小。</span><span class="sxs-lookup"><span data-stu-id="9460c-133">Size of an unsigned native integer.</span></span>|
|`ELEMENT_TYPE_FNPTR`|<span data-ttu-id="9460c-134">指向函数的指针。</span><span class="sxs-lookup"><span data-stu-id="9460c-134">A pointer to a function.</span></span>|
|`ELEMENT_TYPE_OBJECT`|<span data-ttu-id="9460c-135">System.object 类型。</span><span class="sxs-lookup"><span data-stu-id="9460c-135">A System.Object type.</span></span>|
|`ELEMENT_TYPE_SZARRAY`|<span data-ttu-id="9460c-136">一维的、从零开始的下限数组类型修饰符。</span><span class="sxs-lookup"><span data-stu-id="9460c-136">A single-dimensional, zero lower-bound array type modifier.</span></span>|
|`ELEMENT_TYPE_MVAR`|<span data-ttu-id="9460c-137">方法变量类型修饰符。</span><span class="sxs-lookup"><span data-stu-id="9460c-137">A method variable type modifier.</span></span>|
|`ELEMENT_TYPE_CMOD_REQD`|<span data-ttu-id="9460c-138">C 语言必需的修饰符。</span><span class="sxs-lookup"><span data-stu-id="9460c-138">A C language required modifier.</span></span>|
|`ELEMENT_TYPE_CMOD_OPT`|<span data-ttu-id="9460c-139">C 语言可选修饰符。</span><span class="sxs-lookup"><span data-stu-id="9460c-139">A C language optional modifier.</span></span>|
|`ELEMENT_TYPE_INTERNAL`|<span data-ttu-id="9460c-140">内部使用。</span><span class="sxs-lookup"><span data-stu-id="9460c-140">Used internally.</span></span>|
|`ELEMENT_TYPE_MAX`|<span data-ttu-id="9460c-141">无效类型。</span><span class="sxs-lookup"><span data-stu-id="9460c-141">An invalid type.</span></span>|
|`ELEMENT_TYPE_MODIFIER`|<span data-ttu-id="9460c-142">内部使用。</span><span class="sxs-lookup"><span data-stu-id="9460c-142">Used internally.</span></span>|
|`ELEMENT_TYPE_SENTINEL`|<span data-ttu-id="9460c-143">作为参数数目可变的列表的 sentinel 的类型修饰符。</span><span class="sxs-lookup"><span data-stu-id="9460c-143">A type modifier that is a sentinel for a list of a variable number of parameters.</span></span>|
|`ELEMENT_TYPE_PINNED`|<span data-ttu-id="9460c-144">内部使用。</span><span class="sxs-lookup"><span data-stu-id="9460c-144">Used internally.</span></span>|

## <a name="remarks"></a><span data-ttu-id="9460c-145">备注</span><span class="sxs-lookup"><span data-stu-id="9460c-145">Remarks</span></span>

<span data-ttu-id="9460c-146">类型修饰符构成了用于表示更复杂类型的基础。</span><span class="sxs-lookup"><span data-stu-id="9460c-146">The type modifiers form the basis for representing more complex types.</span></span> <span data-ttu-id="9460c-147">`CorElementType`类型修饰符值应用于在类型签名中紧跟在其后面的值。</span><span class="sxs-lookup"><span data-stu-id="9460c-147">A `CorElementType` type modifier value is applied to the value that immediately follows it in the type signature.</span></span> <span data-ttu-id="9460c-148">在 `CorElementType` 类型修饰符值之后的值可以是 `CorElementType` 简单类型值、元数据标记或其他值，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="9460c-148">The value that follows the `CorElementType` type modifier value can be a `CorElementType` simple type value, a metadata token, or other value, as specified in the following table.</span></span>

> [!NOTE]
> <span data-ttu-id="9460c-149">所有数字 (*数字*、 *参数计数*、 *元数据令牌*、 *排名*、 *计数* 和 *绑定*) 均存储为压缩整数。</span><span class="sxs-lookup"><span data-stu-id="9460c-149">All numbers (*number*, *argument Count*, *metadata token*, *rank*, *count*, and *bound*) are stored as compressed integers.</span></span> <span data-ttu-id="9460c-150">有关详细信息，请参阅 ECMA 网站上的 [标准 ECMA-335-公共语言基础结构 (CLI) ](http://www.ecma-international.org/publications/standards/Ecma-335.htm) 。</span><span class="sxs-lookup"><span data-stu-id="9460c-150">See [Standard ECMA-335 - Common Language Infrastructure (CLI)](http://www.ecma-international.org/publications/standards/Ecma-335.htm) on the ECMA Web site for details.</span></span>

|<span data-ttu-id="9460c-151">类型修饰符</span><span class="sxs-lookup"><span data-stu-id="9460c-151">Type modifier</span></span>|<span data-ttu-id="9460c-152">格式</span><span class="sxs-lookup"><span data-stu-id="9460c-152">Format</span></span>|
|-------------------|------------|
|`ELEMENT_TYPE_PTR`|<span data-ttu-id="9460c-153">ELEMENT_TYPE_PTR \<a `CorElementType` value></span><span class="sxs-lookup"><span data-stu-id="9460c-153">ELEMENT_TYPE_PTR \<a `CorElementType` value></span></span>|
|`ELEMENT_TYPE_BYREF`|<span data-ttu-id="9460c-154">ELEMENT_TYPE_BYREF \<a `CorElementType` value></span><span class="sxs-lookup"><span data-stu-id="9460c-154">ELEMENT_TYPE_BYREF \<a `CorElementType` value></span></span>|
|`ELEMENT_TYPE_VALUETYPE`|<span data-ttu-id="9460c-155">ELEMENT_TYPE_VALUETYPE \<an `mdTypeDef` metadata token></span><span class="sxs-lookup"><span data-stu-id="9460c-155">ELEMENT_TYPE_VALUETYPE \<an `mdTypeDef` metadata token></span></span>|
|`ELEMENT_TYPE_CLASS`|<span data-ttu-id="9460c-156">ELEMENT_TYPE_CLASS \<an `mdTypeDef` metadata token></span><span class="sxs-lookup"><span data-stu-id="9460c-156">ELEMENT_TYPE_CLASS \<an `mdTypeDef` metadata token></span></span>|
|`ELEMENT_TYPE_VAR`|<span data-ttu-id="9460c-157">ELEMENT_TYPE_VAR \<number></span><span class="sxs-lookup"><span data-stu-id="9460c-157">ELEMENT_TYPE_VAR \<number></span></span>|
|`ELEMENT_TYPE_ARRAY`|<span data-ttu-id="9460c-158">ELEMENT_TYPE_ARRAY \<a `CorElementType` value> \<rank> \<count1> \<bound1> ... \<countN>\<boundN></span><span class="sxs-lookup"><span data-stu-id="9460c-158">ELEMENT_TYPE_ARRAY \<a `CorElementType` value> \<rank> \<count1> \<bound1> ... \<countN> \<boundN></span></span>|
|`ELEMENT_TYPE_GENERICINST`|<span data-ttu-id="9460c-159">ELEMENT_TYPE_GENERICINST \<an `mdTypeDef` metadata token> \<argument Count> \<arg1> .。。 \<argN></span><span class="sxs-lookup"><span data-stu-id="9460c-159">ELEMENT_TYPE_GENERICINST \<an `mdTypeDef` metadata token> \<argument Count> \<arg1> ... \<argN></span></span>|
|`ELEMENT_TYPE_FNPTR`|<span data-ttu-id="9460c-160">ELEMENT_TYPE_FNPTR \<complete signature for the function, including calling convention></span><span class="sxs-lookup"><span data-stu-id="9460c-160">ELEMENT_TYPE_FNPTR \<complete signature for the function, including calling convention></span></span>|
|`ELEMENT_TYPE_SZARRAY`|<span data-ttu-id="9460c-161">ELEMENT_TYPE_SZARRAY \<a `CorElementType` value></span><span class="sxs-lookup"><span data-stu-id="9460c-161">ELEMENT_TYPE_SZARRAY \<a `CorElementType` value></span></span>|
|`ELEMENT_TYPE_MVAR`|<span data-ttu-id="9460c-162">ELEMENT_TYPE_MVAR \<number></span><span class="sxs-lookup"><span data-stu-id="9460c-162">ELEMENT_TYPE_MVAR \<number></span></span>|
|`ELEMENT_TYPE_CMOD_REQD`|<span data-ttu-id="9460c-163">ELEMENT_TYPE_\<a `mdTypeRef` or `mdTypeDef` metadata token></span><span class="sxs-lookup"><span data-stu-id="9460c-163">ELEMENT_TYPE_\<a `mdTypeRef` or `mdTypeDef` metadata token></span></span>|
|`ELEMENT_TYPE_CMOD_OPT`|<span data-ttu-id="9460c-164">E_T_CMOD_OPT \<a `mdTypeRef` or `mdTypeDef` metadata token></span><span class="sxs-lookup"><span data-stu-id="9460c-164">E_T_CMOD_OPT \<a `mdTypeRef` or `mdTypeDef` metadata token></span></span>|

## <a name="requirements"></a><span data-ttu-id="9460c-165">要求</span><span class="sxs-lookup"><span data-stu-id="9460c-165">Requirements</span></span>

<span data-ttu-id="9460c-166">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9460c-166">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="9460c-167">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="9460c-167">**Header:** CorHdr.h</span></span>

<span data-ttu-id="9460c-168">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9460c-168">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="9460c-169">请参阅</span><span class="sxs-lookup"><span data-stu-id="9460c-169">See also</span></span>

- [<span data-ttu-id="9460c-170">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="9460c-170">Metadata Enumerations</span></span>](metadata-enumerations.md)
