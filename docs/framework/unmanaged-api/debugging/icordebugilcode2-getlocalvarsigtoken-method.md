---
description: 了解详细信息： ICorDebugILCode2：： GetLocalVarSigToken 方法
title: ICorDebugILCode2::GetLocalVarSigToken 方法
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorDebugILCode2.GetLocalVarSigToken
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 17665b77-1342-4115-94fd-9f45b0ecfb0f
topic_type:
- apiref
ms.openlocfilehash: cdf2725274a132528123534ddd36ae95e265af44
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791421"
---
# <a name="icordebugilcode2getlocalvarsigtoken-method"></a><span data-ttu-id="484bb-103">ICorDebugILCode2::GetLocalVarSigToken 方法</span><span class="sxs-lookup"><span data-stu-id="484bb-103">ICorDebugILCode2::GetLocalVarSigToken Method</span></span>

<span data-ttu-id="484bb-104">[仅在 .NET Framework 4.5.2 及更高版本中受支持]</span><span class="sxs-lookup"><span data-stu-id="484bb-104">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="484bb-105">获取元数据标记，用于由此实例表示的函数的局部变量签名。</span><span class="sxs-lookup"><span data-stu-id="484bb-105">Gets the metadata token for the local variable signature for the function that is represented by this instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="484bb-106">语法</span><span class="sxs-lookup"><span data-stu-id="484bb-106">Syntax</span></span>  
  
```cpp
HRESULT GetLocalVarSigToken(  
   [out] mdSignature *pmdSig  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="484bb-107">参数</span><span class="sxs-lookup"><span data-stu-id="484bb-107">Parameters</span></span>  

 `pmdSig`  
 <span data-ttu-id="484bb-108">[out] 指向此函数的局部变量签名的 `mdSignature` 标记，或者指向 `mdSignatureNil`（如果不存在签名，即该函数没有任何局部变量）的指针。</span><span class="sxs-lookup"><span data-stu-id="484bb-108">[out] A pointer to the `mdSignature` token for the local variable signature for this function, or `mdSignatureNil` if there is no signature (that is, if the function doesn't have any local variables).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="484bb-109">备注</span><span class="sxs-lookup"><span data-stu-id="484bb-109">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="484bb-110">要求</span><span class="sxs-lookup"><span data-stu-id="484bb-110">Requirements</span></span>  

 <span data-ttu-id="484bb-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="484bb-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="484bb-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="484bb-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="484bb-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="484bb-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="484bb-114">**.NET Framework 版本：**[!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="484bb-114">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="484bb-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="484bb-115">See also</span></span>

- [<span data-ttu-id="484bb-116">ICorDebugILCode2 接口</span><span class="sxs-lookup"><span data-stu-id="484bb-116">ICorDebugILCode2 Interface</span></span>](icordebugilcode2-interface.md)
- [<span data-ttu-id="484bb-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="484bb-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
