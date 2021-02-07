---
description: 了解详细信息： ICorDebugNativeFrame：： GetLocalRegisterMemoryValue 方法
title: ICorDebugNativeFrame::GetLocalRegisterMemoryValue 方法
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame.GetLocalRegisterMemoryValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame::GetLocalRegisterMemoryValue
helpviewer_keywords:
- ICorDebugNativeFrame::GetLocalRegisterMemoryValue method [.NET Framework debugging]
- GetLocalRegisterMemoryValue method [.NET Framework debugging]
ms.assetid: d350f69d-9aff-4f5a-8301-daea22dee2da
topic_type:
- apiref
ms.openlocfilehash: 36cf4d38c65e233a8be91a1e2aeca01ea009f340
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99729180"
---
# <a name="icordebugnativeframegetlocalregistermemoryvalue-method"></a><span data-ttu-id="0901f-103">ICorDebugNativeFrame::GetLocalRegisterMemoryValue 方法</span><span class="sxs-lookup"><span data-stu-id="0901f-103">ICorDebugNativeFrame::GetLocalRegisterMemoryValue Method</span></span>

<span data-ttu-id="0901f-104">获取参数或局部变量的值，该参数或局部变量的下限字和高位字分别存储在内存位置和指定的寄存器中（对于此本机帧）。</span><span class="sxs-lookup"><span data-stu-id="0901f-104">Gets the value of an argument or local variable, of which the low word and high word are stored in the memory location and specified register, respectively, for this native frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0901f-105">语法</span><span class="sxs-lookup"><span data-stu-id="0901f-105">Syntax</span></span>  
  
```cpp  
HRESULT GetLocalRegisterMemoryValue (  
    [in] CorDebugRegister   highWordReg,  
    [in] CORDB_ADDRESS      lowWordAddress,  
    [in] ULONG              cbSigBlob,  
    [in] PCCOR_SIGNATURE    pvSigBlob,  
    [out] ICorDebugValue    **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0901f-106">参数</span><span class="sxs-lookup"><span data-stu-id="0901f-106">Parameters</span></span>  

 `highWordReg`  
 <span data-ttu-id="0901f-107">中"CorDebugRegister" 枚举的一个值，它指定包含值高位字的寄存器。</span><span class="sxs-lookup"><span data-stu-id="0901f-107">[in] A value of the "CorDebugRegister" enumeration that specifies the register containing the high word of the value.</span></span>  
  
 `lowWordAddress`  
 <span data-ttu-id="0901f-108">中一个 `CORDB_ADDRESS` 值，该值指定包含值的低位字的内存位置。</span><span class="sxs-lookup"><span data-stu-id="0901f-108">[in] A `CORDB_ADDRESS` value that specifies the memory location containing the low word of the value.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="0901f-109">中一个整数，指定参数引用的二进制元数据签名的大小 `pvSigBlob` 。</span><span class="sxs-lookup"><span data-stu-id="0901f-109">[in] An integer that specifies the size of the binary metadata signature which is referenced by the `pvSigBlob` parameter.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="0901f-110">中一个 `PCCOR_SIGNATURE` 值，该值指向值类型的二进制元数据签名。</span><span class="sxs-lookup"><span data-stu-id="0901f-110">[in] A `PCCOR_SIGNATURE` value that points to the binary metadata signature of the value's type.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="0901f-111">弄一个指向 "ICorDebugValue" 对象地址的指针，该对象表示存储在指定寄存器和内存位置的检索到的值。</span><span class="sxs-lookup"><span data-stu-id="0901f-111">[out] A pointer to the address of an "ICorDebugValue" object representing the retrieved value that is stored in the specified register and memory location.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0901f-112">要求</span><span class="sxs-lookup"><span data-stu-id="0901f-112">Requirements</span></span>  

 <span data-ttu-id="0901f-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0901f-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0901f-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0901f-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0901f-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0901f-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0901f-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0901f-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0901f-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="0901f-117">See also</span></span>
