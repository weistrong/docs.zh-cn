---
description: 了解详细信息： VariableLocationType 枚举
title: VariableLocationType 枚举
ms.date: 03/30/2017
api_name:
- VariableLocationType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- VariableLocationType
helpviewer_keywords:
- VariableLocationType enumeration [.NET Framework debugging]
ms.assetid: 8635ee3a-c84b-4626-876c-416bee54f787
topic_type:
- apiref
ms.openlocfilehash: 8561077b9f3f4d318eeb743d51538b2a9a22a217
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800521"
---
# <a name="variablelocationtype-enumeration"></a><span data-ttu-id="f18e7-103">VariableLocationType 枚举</span><span class="sxs-lookup"><span data-stu-id="f18e7-103">VariableLocationType Enumeration</span></span>

<span data-ttu-id="f18e7-104">指示变量的本机位置类型。</span><span class="sxs-lookup"><span data-stu-id="f18e7-104">Indicates the native location type of a variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f18e7-105">语法</span><span class="sxs-lookup"><span data-stu-id="f18e7-105">Syntax</span></span>  
  
```cpp  
typedef enum VariableLocationType  
{  
    VLT_REGISTER,
    VLT_REGISTER_RELATIVE,
    VLT_INVALID  
} VariableLocationType;  
```  
  
## <a name="members"></a><span data-ttu-id="f18e7-106">成员</span><span class="sxs-lookup"><span data-stu-id="f18e7-106">Members</span></span>  
  
|<span data-ttu-id="f18e7-107">成员</span><span class="sxs-lookup"><span data-stu-id="f18e7-107">Member</span></span>|<span data-ttu-id="f18e7-108">说明</span><span class="sxs-lookup"><span data-stu-id="f18e7-108">Description</span></span>|  
|------------|-----------------|  
|`VLT_REGISTER`|<span data-ttu-id="f18e7-109">变量在寄存器中。</span><span class="sxs-lookup"><span data-stu-id="f18e7-109">The variable is in a register.</span></span>|  
|`VLT_REGISTER_RELATIVE`|<span data-ttu-id="f18e7-110">变量在寄存器相对内存位置。</span><span class="sxs-lookup"><span data-stu-id="f18e7-110">The variable is in a register-relative memory location.</span></span>|  
|`VLT_INVALID`|<span data-ttu-id="f18e7-111">变量不存储在寄存器或寄存器相对内存位置中。</span><span class="sxs-lookup"><span data-stu-id="f18e7-111">The variable is not stored in a register or a register-relative memory location.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f18e7-112">备注</span><span class="sxs-lookup"><span data-stu-id="f18e7-112">Remarks</span></span>  

 <span data-ttu-id="f18e7-113">枚举的成员 `VariableLocationType` 由 [ICorDebugVariableHome：： GetLocationType](icordebugvariablehome-getlocationtype-method.md) 方法返回。</span><span class="sxs-lookup"><span data-stu-id="f18e7-113">A member of the `VariableLocationType` enumeration is returned by the [ICorDebugVariableHome::GetLocationType](icordebugvariablehome-getlocationtype-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f18e7-114">要求</span><span class="sxs-lookup"><span data-stu-id="f18e7-114">Requirements</span></span>  

 <span data-ttu-id="f18e7-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f18e7-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f18e7-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f18e7-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f18e7-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f18e7-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f18e7-118">**.NET Framework 版本：**[!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f18e7-118">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f18e7-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="f18e7-119">See also</span></span>

- [<span data-ttu-id="f18e7-120">调试枚举</span><span class="sxs-lookup"><span data-stu-id="f18e7-120">Debugging Enumerations</span></span>](debugging-enumerations.md)
