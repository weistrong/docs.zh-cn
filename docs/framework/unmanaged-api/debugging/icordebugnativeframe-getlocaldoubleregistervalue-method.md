---
description: 了解详细信息： ICorDebugNativeFrame：： GetLocalDoubleRegisterValue 方法
title: ICorDebugNativeFrame::GetLocalDoubleRegisterValue 方法
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame.GetLocalDoubleRegisterValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame::GetLocalDoubleRegisterValue
helpviewer_keywords:
- ICorDebugNativeFrame::GetLocalDoubleRegisterValue method [.NET Framework debugging]
- GetLocalDoubleRegisterValue method [.NET Framework debugging]
ms.assetid: 1f838215-ac8a-434f-8ce6-03021d3098d9
topic_type:
- apiref
ms.openlocfilehash: a478c51ea7bf04b3fc3faf49fef39f9b29a30599
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722420"
---
# <a name="icordebugnativeframegetlocaldoubleregistervalue-method"></a><span data-ttu-id="706b3-103">ICorDebugNativeFrame::GetLocalDoubleRegisterValue 方法</span><span class="sxs-lookup"><span data-stu-id="706b3-103">ICorDebugNativeFrame::GetLocalDoubleRegisterValue Method</span></span>

<span data-ttu-id="706b3-104">获取此本机帧存储在两个指定寄存器中的参数或局部变量的值。</span><span class="sxs-lookup"><span data-stu-id="706b3-104">Gets the value of an argument or local variable that is stored in the two specified registers for this native frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="706b3-105">语法</span><span class="sxs-lookup"><span data-stu-id="706b3-105">Syntax</span></span>  
  
```cpp  
HRESULT GetLocalDoubleRegisterValue (  
    [in] CorDebugRegister   highWordReg,  
    [in] CorDebugRegister   lowWordReg,  
    [in] ULONG              cbSigBlob,  
    [in] PCCOR_SIGNATURE    pvSigBlob,  
    [out] ICorDebugValue    **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="706b3-106">参数</span><span class="sxs-lookup"><span data-stu-id="706b3-106">Parameters</span></span>  

 `highWordReg`  
 <span data-ttu-id="706b3-107">中"CorDebugRegister" 枚举的一个值，它指定包含值高位字的寄存器。</span><span class="sxs-lookup"><span data-stu-id="706b3-107">[in] A value of the "CorDebugRegister" enumeration that specifies the register containing the high word of the value.</span></span>  
  
 `lowWordReg`  
 <span data-ttu-id="706b3-108">中枚举的一个值 `CorDebugRegister` ，该值指定包含值的低位字的寄存器。</span><span class="sxs-lookup"><span data-stu-id="706b3-108">[in] A value of the `CorDebugRegister` enumeration that specifies the register containing the low word of the value.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="706b3-109">中一个整数，指定参数引用的二进制元数据签名的大小 `pvSigBlob` 。</span><span class="sxs-lookup"><span data-stu-id="706b3-109">[in] An integer that specifies the size of the binary metadata signature which is referenced by the `pvSigBlob` parameter.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="706b3-110">中一个 `PCCOR_SIGNATURE` 值，该值指向值类型的二进制元数据签名。</span><span class="sxs-lookup"><span data-stu-id="706b3-110">[in] A `PCCOR_SIGNATURE` value that points to the binary metadata signature of the value's type.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="706b3-111">弄一个指向 "ICorDebugValue" 对象地址的指针，该对象表示存储在指定寄存器中的检索到的值。</span><span class="sxs-lookup"><span data-stu-id="706b3-111">[out] A pointer to the address of an "ICorDebugValue" object representing the retrieved value that is stored in the specified registers.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="706b3-112">备注</span><span class="sxs-lookup"><span data-stu-id="706b3-112">Remarks</span></span>  

 <span data-ttu-id="706b3-113">`GetLocalDoubleRegisterValue`方法既可以在本机框架中使用，也可以在实时 (JIT) 编译的框架中使用。</span><span class="sxs-lookup"><span data-stu-id="706b3-113">The `GetLocalDoubleRegisterValue` method can be used either in a native frame or a just-in-time (JIT)-compiled frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="706b3-114">要求</span><span class="sxs-lookup"><span data-stu-id="706b3-114">Requirements</span></span>  

 <span data-ttu-id="706b3-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="706b3-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="706b3-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="706b3-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="706b3-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="706b3-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="706b3-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="706b3-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="706b3-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="706b3-119">See also</span></span>
