---
description: 了解详细信息： ICorDebugNativeFrame：： GetLocalRegisterValue 方法
title: ICorDebugNativeFrame::GetLocalRegisterValue 方法
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame.GetLocalRegisterValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame::GetLocalRegisterValue
helpviewer_keywords:
- GetLocalRegisterValue method [.NET Framework debugging]
- ICorDebugNativeFrame::GetLocalRegisterValue method [.NET Framework debugging]
ms.assetid: 5ccb74f3-f891-430c-b70a-e370624edde2
topic_type:
- apiref
ms.openlocfilehash: ae21134db11c4d0449ed5f6d583f435a259b83fe
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99729141"
---
# <a name="icordebugnativeframegetlocalregistervalue-method"></a><span data-ttu-id="7a9e6-103">ICorDebugNativeFrame::GetLocalRegisterValue 方法</span><span class="sxs-lookup"><span data-stu-id="7a9e6-103">ICorDebugNativeFrame::GetLocalRegisterValue Method</span></span>

<span data-ttu-id="7a9e6-104">获取为此本机帧存储在指定寄存器中的参数或局部变量的值。</span><span class="sxs-lookup"><span data-stu-id="7a9e6-104">Gets the value of an argument or local variable that is stored in the specified register for this native frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7a9e6-105">语法</span><span class="sxs-lookup"><span data-stu-id="7a9e6-105">Syntax</span></span>  
  
```cpp  
HRESULT GetLocalRegisterValue (  
    [in]  CorDebugRegister   reg,  
    [in]  ULONG              cbSigBlob,  
    [in]  PCCOR_SIGNATURE    pvSigBlob,  
    [out] ICorDebugValue     **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7a9e6-106">参数</span><span class="sxs-lookup"><span data-stu-id="7a9e6-106">Parameters</span></span>  

 `reg`  
 <span data-ttu-id="7a9e6-107">中"CorDebugRegister" 枚举的一个值，它指定包含该值的寄存器。</span><span class="sxs-lookup"><span data-stu-id="7a9e6-107">[in] A value of the "CorDebugRegister" enumeration that specifies the register containing the value.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="7a9e6-108">中一个整数，指定参数引用的二进制元数据签名的大小 `pvSigBlob` 。</span><span class="sxs-lookup"><span data-stu-id="7a9e6-108">[in] An integer that specifies the size of the binary metadata signature which is referenced by the `pvSigBlob` parameter.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="7a9e6-109">中一个 `PCCOR_SIGNATURE` 值，该值指向值类型的二进制元数据签名。</span><span class="sxs-lookup"><span data-stu-id="7a9e6-109">[in] A `PCCOR_SIGNATURE` value that points to the binary metadata signature of the value's type.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="7a9e6-110">弄一个指向 "ICorDebugValue" 对象地址的指针，该对象表示存储在指定寄存器中的检索到的值。</span><span class="sxs-lookup"><span data-stu-id="7a9e6-110">[out] A pointer to the address of an "ICorDebugValue" object representing the retrieved value that is stored in the specified register.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7a9e6-111">备注</span><span class="sxs-lookup"><span data-stu-id="7a9e6-111">Remarks</span></span>  

 <span data-ttu-id="7a9e6-112">`GetLocalRegisterValue`方法既可以在本机框架中使用，也可以在实时 (JIT) 编译的框架中使用。</span><span class="sxs-lookup"><span data-stu-id="7a9e6-112">The `GetLocalRegisterValue` method can be used either in a native frame or a just-in-time (JIT)-compiled frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7a9e6-113">要求</span><span class="sxs-lookup"><span data-stu-id="7a9e6-113">Requirements</span></span>  

 <span data-ttu-id="7a9e6-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7a9e6-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7a9e6-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7a9e6-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7a9e6-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7a9e6-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7a9e6-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7a9e6-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7a9e6-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="7a9e6-118">See also</span></span>
