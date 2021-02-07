---
description: 了解详细信息： IMetaDataEmit：:D efineMethod 方法
title: IMetaDataEmit::DefineMethod 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineMethod
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineMethod
helpviewer_keywords:
- DefineMethod method [.NET Framework metadata]
- IMetaDataEmit::DefineMethod method [.NET Framework metadata]
ms.assetid: 3e2102c5-48b7-4c0e-b805-7e2b5e156e3d
topic_type:
- apiref
ms.openlocfilehash: b0ba2bb68f1d4387229767f6f2550d64b9008898
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99677959"
---
# <a name="imetadataemitdefinemethod-method"></a><span data-ttu-id="078cd-103">IMetaDataEmit::DefineMethod 方法</span><span class="sxs-lookup"><span data-stu-id="078cd-103">IMetaDataEmit::DefineMethod Method</span></span>

<span data-ttu-id="078cd-104">使用指定的签名创建方法或全局函数的定义，并将标记返回到该方法定义。</span><span class="sxs-lookup"><span data-stu-id="078cd-104">Creates a definition for a method or global function with the specified signature, and returns a token to that method definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="078cd-105">语法</span><span class="sxs-lookup"><span data-stu-id="078cd-105">Syntax</span></span>  
  
```cpp  
HRESULT DefineMethod (
    [in]  mdTypeDef         td,
    [in]  LPCWSTR           szName,
    [in]  DWORD             dwMethodFlags,
    [in]  PCCOR_SIGNATURE   pvSigBlob,
    [in]  ULONG             cbSigBlob,
    [in]  ULONG             ulCodeRVA,
    [in]  DWORD             dwImplFlags,
    [out] mdMethodDef      *pmd  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="078cd-106">参数</span><span class="sxs-lookup"><span data-stu-id="078cd-106">Parameters</span></span>  

 `td`  
 <span data-ttu-id="078cd-107">中 `mdTypedef` 方法的父类或父接口的标记。</span><span class="sxs-lookup"><span data-stu-id="078cd-107">[in] The `mdTypedef` token of the parent class or parent interface of the method.</span></span> <span data-ttu-id="078cd-108">`td` `mdTokenNil` 如果正在定义全局函数，则设置为。</span><span class="sxs-lookup"><span data-stu-id="078cd-108">Set `td` to `mdTokenNil`, if you are defining a global function.</span></span>  
  
 `szName`  
 <span data-ttu-id="078cd-109">中Unicode 中的成员名称。</span><span class="sxs-lookup"><span data-stu-id="078cd-109">[in] The member name in Unicode.</span></span>  
  
 `dwMethodFlags`  
 <span data-ttu-id="078cd-110">中 [CorMethodAttr](cormethodattr-enumeration.md) 枚举的一个值，该值指定方法或全局函数的特性。</span><span class="sxs-lookup"><span data-stu-id="078cd-110">[in] A value of the [CorMethodAttr](cormethodattr-enumeration.md) enumeration that specifies the attributes of the method or global function.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="078cd-111">中方法签名。</span><span class="sxs-lookup"><span data-stu-id="078cd-111">[in] The method signature.</span></span> <span data-ttu-id="078cd-112">签名按提供的方式持久保存。</span><span class="sxs-lookup"><span data-stu-id="078cd-112">The signature is persisted as supplied.</span></span> <span data-ttu-id="078cd-113">如果需要指定任何参数的其他信息，请使用 [IMetaDataEmit：： SetParamProps](imetadataemit-setparamprops-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="078cd-113">If you need to specify additional information for any parameters, use the [IMetaDataEmit::SetParamProps](imetadataemit-setparamprops-method.md) method.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="078cd-114">中中的字节数 `pvSigBlob` 。</span><span class="sxs-lookup"><span data-stu-id="078cd-114">[in] The count of bytes in `pvSigBlob`.</span></span>  
  
 `ulCodeRVA`  
 <span data-ttu-id="078cd-115">中代码的地址。</span><span class="sxs-lookup"><span data-stu-id="078cd-115">[in] The address of the code.</span></span>  
  
 `dwImplFlags`  
 <span data-ttu-id="078cd-116">中 [CorMethodImpl](cormethodimpl-enumeration.md) 枚举的一个值，该值指定方法的实现功能。</span><span class="sxs-lookup"><span data-stu-id="078cd-116">[in] A value of the [CorMethodImpl](cormethodimpl-enumeration.md) enumeration that specifies the implementation features of the method.</span></span>  
  
 `pmd`  
 <span data-ttu-id="078cd-117">弄成员标记。</span><span class="sxs-lookup"><span data-stu-id="078cd-117">[out] The member token.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="078cd-118">备注</span><span class="sxs-lookup"><span data-stu-id="078cd-118">Remarks</span></span>  

 <span data-ttu-id="078cd-119">元数据 API 保证按调用方为给定的封闭类或接口发出方法（在参数中指定）来保持方法的顺序相同 `td` 。</span><span class="sxs-lookup"><span data-stu-id="078cd-119">The metadata API guarantees to persist methods in the same order as the caller emits them for a given enclosing class or interface, which is specified in the `td` parameter.</span></span>  
  
 <span data-ttu-id="078cd-120">下面给出了有关使用 `DefineMethod` 和特定参数设置的其他信息。</span><span class="sxs-lookup"><span data-stu-id="078cd-120">Additional information regarding the use of `DefineMethod` and particular parameter settings is given below.</span></span>  
  
## <a name="slots-in-the-v-table"></a><span data-ttu-id="078cd-121">V-表中的槽</span><span class="sxs-lookup"><span data-stu-id="078cd-121">Slots in the V-table</span></span>  

 <span data-ttu-id="078cd-122">运行时使用方法定义设置 v 表槽。</span><span class="sxs-lookup"><span data-stu-id="078cd-122">The runtime uses method definitions to set up v-table slots.</span></span> <span data-ttu-id="078cd-123">如果需要跳过一个或多个槽，如使用 COM 接口布局保留奇偶校验，则会定义一个虚方法，用于在下表中占据槽;将设置 `dwMethodFlags` 为 `mdRTSpecialName` [CorMethodAttr](cormethodattr-enumeration.md) 枚举的值，并将该名称指定为：</span><span class="sxs-lookup"><span data-stu-id="078cd-123">In the case where one or more slots need to be skipped, such as to preserve parity with a COM interface layout, a dummy method is defined to take up the slot or slots in the v-table; set the `dwMethodFlags` to the `mdRTSpecialName` value of the [CorMethodAttr](cormethodattr-enumeration.md) enumeration and specify the name as:</span></span>  
  
 <span data-ttu-id="078cd-124">_VtblGap\<*SequenceNumber*>\<\_*CountOfSlots*></span><span class="sxs-lookup"><span data-stu-id="078cd-124">_VtblGap\<*SequenceNumber*>\<\_*CountOfSlots*></span></span>
  
 <span data-ttu-id="078cd-125">其中， *SequenceNumber* 是方法的序列号， *CountOfSlots* 是要在 v 表中跳过的槽数。</span><span class="sxs-lookup"><span data-stu-id="078cd-125">where *SequenceNumber* is the sequence number of the method and *CountOfSlots* is the number of slots to skip in the v-table.</span></span> <span data-ttu-id="078cd-126">如果省略 *CountOfSlots* ，则假定为1。</span><span class="sxs-lookup"><span data-stu-id="078cd-126">If *CountOfSlots* is omitted, 1 is assumed.</span></span> <span data-ttu-id="078cd-127">不能从托管或非托管代码中调用这些虚方法，任何从托管或非托管代码调用它们的尝试都将生成异常。</span><span class="sxs-lookup"><span data-stu-id="078cd-127">These dummy methods are not callable from either managed or unmanaged code and any attempt to call them, from either managed or unmanaged code, generates an exception.</span></span> <span data-ttu-id="078cd-128">其唯一目的是在运行时为 COM 集成生成的 v 表中占用空间。</span><span class="sxs-lookup"><span data-stu-id="078cd-128">Their only purpose is to take up space in the v-table that the runtime generates for COM integration.</span></span>  
  
## <a name="duplicate-methods"></a><span data-ttu-id="078cd-129">重复方法</span><span class="sxs-lookup"><span data-stu-id="078cd-129">Duplicate Methods</span></span>  

 <span data-ttu-id="078cd-130">不应定义重复的方法。</span><span class="sxs-lookup"><span data-stu-id="078cd-130">You should not define duplicate methods.</span></span> <span data-ttu-id="078cd-131">也就是说，不应 `DefineMethod` 使用 `td` 、和参数中的重复值集调用 `wzName` `pvSig` 。</span><span class="sxs-lookup"><span data-stu-id="078cd-131">That is, you should not call `DefineMethod` with a duplicate set of values in the `td`, `wzName`, and `pvSig` parameters.</span></span> <span data-ttu-id="078cd-132"> (这三个参数一起唯一定义方法. ) 。</span><span class="sxs-lookup"><span data-stu-id="078cd-132">(These three parameters together uniquely define the method.).</span></span> <span data-ttu-id="078cd-133">不过，你可以使用一种重复的三重，为其中一个方法定义设置 `mdPrivateScope` 参数中的位 `dwMethodFlags` 。</span><span class="sxs-lookup"><span data-stu-id="078cd-133">However, you can use a duplicate triple provided that, for one of the method definitions, you set the `mdPrivateScope` bit in the `dwMethodFlags` parameter.</span></span> <span data-ttu-id="078cd-134"> (`mdPrivateScope` 位意味着编译器不会发出对此方法定义的引用。 ) </span><span class="sxs-lookup"><span data-stu-id="078cd-134">(The `mdPrivateScope` bit means that the compiler will not emit a reference to this method definition.)</span></span>  
  
## <a name="method-implementation-information"></a><span data-ttu-id="078cd-135">方法实现信息</span><span class="sxs-lookup"><span data-stu-id="078cd-135">Method Implementation Information</span></span>  

 <span data-ttu-id="078cd-136">在声明该方法时，有关方法实现的信息通常是未知的。</span><span class="sxs-lookup"><span data-stu-id="078cd-136">Information about the method implementation is often not known at the time the method is declared.</span></span> <span data-ttu-id="078cd-137">因此，在调用时，不需要在和参数中传递值 `ulCodeRVA` `dwImplFlags` `DefineMethod` 。</span><span class="sxs-lookup"><span data-stu-id="078cd-137">Therefore, you do not need to pass values in the `ulCodeRVA` and `dwImplFlags` parameters when calling `DefineMethod`.</span></span> <span data-ttu-id="078cd-138">可在以后根据需要通过 [IMetaDataEmit：： SetMethodImplFlags](imetadataemit-setmethodimplflags-method.md) 或 [IMetaDataEmit：： SetRVA](imetadataemit-setrva-method.md)来提供这些值。</span><span class="sxs-lookup"><span data-stu-id="078cd-138">The values can be supplied later through [IMetaDataEmit::SetMethodImplFlags](imetadataemit-setmethodimplflags-method.md) or [IMetaDataEmit::SetRVA](imetadataemit-setrva-method.md), as appropriate.</span></span>  
  
 <span data-ttu-id="078cd-139">在某些情况下（例如平台调用 (PInvoke) 或 COM 互操作方案），将不提供方法体，因此 `ulCodeRVA` 应将其设置为零。</span><span class="sxs-lookup"><span data-stu-id="078cd-139">In some situations, such as platform invocation (PInvoke) or COM interop scenarios, the method body will not be supplied, and `ulCodeRVA` should be set to zero.</span></span> <span data-ttu-id="078cd-140">在这些情况下，不应将方法标记为抽象方法，因为运行时将找到实现。</span><span class="sxs-lookup"><span data-stu-id="078cd-140">In these situations, the method should not be tagged as abstract, because the runtime will locate the implementation.</span></span>  
  
## <a name="defining-a-method-for-pinvoke"></a><span data-ttu-id="078cd-141">为 PInvoke 定义方法</span><span class="sxs-lookup"><span data-stu-id="078cd-141">Defining a Method for PInvoke</span></span>  

 <span data-ttu-id="078cd-142">对于要通过 PInvoke 调用的每个非托管函数，必须定义一个表示目标非托管函数的托管方法。</span><span class="sxs-lookup"><span data-stu-id="078cd-142">For each unmanaged function to be called through PInvoke, you must define a managed method that represents the target unmanaged function.</span></span> <span data-ttu-id="078cd-143">若要定义托管方法，请使用，将 `DefineMethod` 某些参数设置为特定值，具体取决于使用 PInvoke 的方式：</span><span class="sxs-lookup"><span data-stu-id="078cd-143">To define the managed method, use `DefineMethod` with some of the parameters set to certain values, depending on the way in which PInvoke is used:</span></span>  
  
- <span data-ttu-id="078cd-144">True PInvoke-涉及调用驻留在非托管 DLL 中的外部非托管方法。</span><span class="sxs-lookup"><span data-stu-id="078cd-144">True PInvoke - involves invocation of an external unmanaged method that resides in an unmanaged DLL.</span></span>  
  
- <span data-ttu-id="078cd-145">本地 PInvoke-涉及对嵌入当前托管模块的本机非托管方法的调用。</span><span class="sxs-lookup"><span data-stu-id="078cd-145">Local PInvoke - involves invocation of a native unmanaged method that is embedded in the current managed module.</span></span>  
  
 <span data-ttu-id="078cd-146">下表给出了参数设置。</span><span class="sxs-lookup"><span data-stu-id="078cd-146">The parameter settings are given in the following table.</span></span>  
  
|<span data-ttu-id="078cd-147">参数</span><span class="sxs-lookup"><span data-stu-id="078cd-147">Parameter</span></span>|<span data-ttu-id="078cd-148">True PInvoke 的值</span><span class="sxs-lookup"><span data-stu-id="078cd-148">Values for true PInvoke</span></span>|<span data-ttu-id="078cd-149">本地 PInvoke 的值</span><span class="sxs-lookup"><span data-stu-id="078cd-149">Values for local PInvoke</span></span>|  
|---------------|-----------------------------|------------------------------|  
|`dwMethodFlags`||<span data-ttu-id="078cd-150">Set `mdStatic` ; 清除 `mdSynchronized` 和 `mdAbstract` 。</span><span class="sxs-lookup"><span data-stu-id="078cd-150">Set `mdStatic`; clear `mdSynchronized` and `mdAbstract`.</span></span>|  
|`pvSigBlob`|<span data-ttu-id="078cd-151">有效的公共语言运行时 (CLR) 方法签名，其参数是有效的托管类型。</span><span class="sxs-lookup"><span data-stu-id="078cd-151">A valid common language runtime (CLR) method signature with parameters that are valid managed types.</span></span>|<span data-ttu-id="078cd-152">包含有效托管类型参数的有效 CLR 方法签名。</span><span class="sxs-lookup"><span data-stu-id="078cd-152">A valid CLR method signature with parameters that are valid managed types.</span></span>|  
|`ulCodeRVA`||<span data-ttu-id="078cd-153">0</span><span class="sxs-lookup"><span data-stu-id="078cd-153">0</span></span>|  
|`dwImplFlags`|<span data-ttu-id="078cd-154">设置 `miCil` 和 `miManaged`。</span><span class="sxs-lookup"><span data-stu-id="078cd-154">Set `miCil` and `miManaged`.</span></span>|<span data-ttu-id="078cd-155">设置 `miNative` 和 `miUnmanaged`。</span><span class="sxs-lookup"><span data-stu-id="078cd-155">Set `miNative` and `miUnmanaged`.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="078cd-156">要求</span><span class="sxs-lookup"><span data-stu-id="078cd-156">Requirements</span></span>  

 <span data-ttu-id="078cd-157">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="078cd-157">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="078cd-158">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="078cd-158">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="078cd-159">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="078cd-159">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="078cd-160">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="078cd-160">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="078cd-161">请参阅</span><span class="sxs-lookup"><span data-stu-id="078cd-161">See also</span></span>

- [<span data-ttu-id="078cd-162">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="078cd-162">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="078cd-163">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="078cd-163">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
