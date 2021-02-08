---
description: 了解详细信息： ICorDebugVariableHome：： GetRegister 方法
title: ICorDebugVariableHome：： GetRegister 方法
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHome.GetRegister
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome::GetRegister
helpviewer_keywords:
- ICorDebugVariableHome::GetRegister method [.NET Framework debugging]
- GetRegister method, ICorDebugVariableHome interface [.NET Framework debugging]
ms.assetid: a5eecd7b-b04c-4266-bff2-7c8771d519a8
topic_type:
- apiref
ms.openlocfilehash: c394d455048cf7451b8320ed72a6aa7adfb3518e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790654"
---
# <a name="icordebugvariablehomegetregister-method"></a><span data-ttu-id="1fd8d-103">ICorDebugVariableHome：： GetRegister 方法</span><span class="sxs-lookup"><span data-stu-id="1fd8d-103">ICorDebugVariableHome::GetRegister Method</span></span>

<span data-ttu-id="1fd8d-104">获取一个寄存器，其中包含位置类型为的变量 `VLT_REGISTER` ，以及位置类型为的变量的基寄存器 `VLT_REGISTER_RELATIVE` 。</span><span class="sxs-lookup"><span data-stu-id="1fd8d-104">Gets the register that contains a variable with a location type of `VLT_REGISTER`, and the base register for a variable with a location type of `VLT_REGISTER_RELATIVE`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1fd8d-105">语法</span><span class="sxs-lookup"><span data-stu-id="1fd8d-105">Syntax</span></span>  
  
```cpp  
HRESULT GetRegister(  
    [out] CorDebugRegister *pRegister  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1fd8d-106">参数</span><span class="sxs-lookup"><span data-stu-id="1fd8d-106">Parameters</span></span>  

 `pRegister`  
 <span data-ttu-id="1fd8d-107">弄一个 CorDebugRegister 枚举值，该值指示注册位置类型为的变量 `VLT_REGISTER` ，并为位置类型为的变量指定基寄存器 `VLT_REGISTER_RELATIVE` 。</span><span class="sxs-lookup"><span data-stu-id="1fd8d-107">[out] A CorDebugRegister enumeration value  that indicates the register for a variable with a location type of `VLT_REGISTER`, and the base register for a variable with a location type of `VLT_REGISTER_RELATIVE`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1fd8d-108">返回值</span><span class="sxs-lookup"><span data-stu-id="1fd8d-108">Return Value</span></span>  

 <span data-ttu-id="1fd8d-109">方法返回以下值：</span><span class="sxs-lookup"><span data-stu-id="1fd8d-109">The method returns the following values:</span></span>  
  
|<span data-ttu-id="1fd8d-110">值</span><span class="sxs-lookup"><span data-stu-id="1fd8d-110">Value</span></span>|<span data-ttu-id="1fd8d-111">说明</span><span class="sxs-lookup"><span data-stu-id="1fd8d-111">Description</span></span>|  
|-----------|-----------------|  
|`S_OK`|<span data-ttu-id="1fd8d-112">变量在由参数指示的寄存器中 `pRegister` 。</span><span class="sxs-lookup"><span data-stu-id="1fd8d-112">The variable is in the register indicated by the `pRegister` argument.</span></span>|  
|`E_FAIL`|<span data-ttu-id="1fd8d-113">变量不在寄存器或寄存器相对位置中。</span><span class="sxs-lookup"><span data-stu-id="1fd8d-113">The variable is not in a register or a register-relative location.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1fd8d-114">要求</span><span class="sxs-lookup"><span data-stu-id="1fd8d-114">Requirements</span></span>  

 <span data-ttu-id="1fd8d-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1fd8d-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1fd8d-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1fd8d-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1fd8d-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1fd8d-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1fd8d-118">**.NET Framework 版本：**[!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1fd8d-118">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1fd8d-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="1fd8d-119">See also</span></span>

- [<span data-ttu-id="1fd8d-120">VariableLocationType 枚举</span><span class="sxs-lookup"><span data-stu-id="1fd8d-120">VariableLocationType Enumeration</span></span>](variablelocationtype-enumeration.md)
- [<span data-ttu-id="1fd8d-121">ICorDebugVariableHome 接口</span><span class="sxs-lookup"><span data-stu-id="1fd8d-121">ICorDebugVariableHome Interface</span></span>](icordebugvariablehome-interface.md)
