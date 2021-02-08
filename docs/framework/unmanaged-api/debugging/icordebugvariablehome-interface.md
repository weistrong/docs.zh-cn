---
description: 了解详细信息： ICorDebugVariableHome 接口
title: ICorDebugVariableHome 接口
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorDebugVariableHome
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome
helpviewer_keywords:
- ICorDebugVariableHome interface [.NET Framework debugging]
ms.assetid: 76f2bf3b-759f-4eed-bce7-119415b25915
topic_type:
- apiref
ms.openlocfilehash: a1dcc959ba9aeffc0e511dcd2f5bb15f58445139
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790628"
---
# <a name="icordebugvariablehome-interface"></a><span data-ttu-id="542c5-103">ICorDebugVariableHome 接口</span><span class="sxs-lookup"><span data-stu-id="542c5-103">ICorDebugVariableHome Interface</span></span>

<span data-ttu-id="542c5-104">表示函数的局部变量或自变量。</span><span class="sxs-lookup"><span data-stu-id="542c5-104">Represents a local variable or argument of a function.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="542c5-105">方法</span><span class="sxs-lookup"><span data-stu-id="542c5-105">Methods</span></span>  
  
|<span data-ttu-id="542c5-106">方法</span><span class="sxs-lookup"><span data-stu-id="542c5-106">Method</span></span>|<span data-ttu-id="542c5-107">说明</span><span class="sxs-lookup"><span data-stu-id="542c5-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="542c5-108">GetArgumentIndex 方法</span><span class="sxs-lookup"><span data-stu-id="542c5-108">GetArgumentIndex Method</span></span>](icordebugvariablehome-getargumentindex-method.md)|<span data-ttu-id="542c5-109">获取函数参数的索引。</span><span class="sxs-lookup"><span data-stu-id="542c5-109">Gets the index of a function argument.</span></span>|  
|[<span data-ttu-id="542c5-110">GetCode 方法</span><span class="sxs-lookup"><span data-stu-id="542c5-110">GetCode Method</span></span>](icordebugvariablehome-getcode-method.md)|<span data-ttu-id="542c5-111">获取包含此对象的 "ICorDebugCode" 实例 `ICorDebugVariableHome` 。</span><span class="sxs-lookup"><span data-stu-id="542c5-111">Gets the "ICorDebugCode" instance that contains this `ICorDebugVariableHome` object.</span></span>|  
|[<span data-ttu-id="542c5-112">GetLiveRange 方法</span><span class="sxs-lookup"><span data-stu-id="542c5-112">GetLiveRange Method</span></span>](icordebugvariablehome-getliverange-method.md)|<span data-ttu-id="542c5-113">获取此变量的生存期的本机范围。</span><span class="sxs-lookup"><span data-stu-id="542c5-113">Gets the native range over which this variable is live.</span></span>|  
|[<span data-ttu-id="542c5-114">GetLocationType 方法</span><span class="sxs-lookup"><span data-stu-id="542c5-114">GetLocationType Method</span></span>](icordebugvariablehome-getlocationtype-method.md)|<span data-ttu-id="542c5-115">获取变量的本机位置的类型。</span><span class="sxs-lookup"><span data-stu-id="542c5-115">Gets the type of the variable's native location.</span></span>|  
|[<span data-ttu-id="542c5-116">GetOffset 方法</span><span class="sxs-lookup"><span data-stu-id="542c5-116">GetOffset Method</span></span>](icordebugvariablehome-getoffset-method.md)|<span data-ttu-id="542c5-117">获取与基寄存器相对应的偏移量。</span><span class="sxs-lookup"><span data-stu-id="542c5-117">Gets the offset from the base register for a variable.</span></span>|  
|[<span data-ttu-id="542c5-118">GetRegister 方法</span><span class="sxs-lookup"><span data-stu-id="542c5-118">GetRegister Method</span></span>](icordebugvariablehome-getregister-method.md)|<span data-ttu-id="542c5-119">获取一个寄存器，其中包含位置类型为的变量 `VLT_REGISTER` ，以及位置类型为的变量的基寄存器 `VLT_REGISTER_RELATIVE` 。</span><span class="sxs-lookup"><span data-stu-id="542c5-119">Gets the register that contains a variable with a location type of `VLT_REGISTER`, and the base register for a variable with a location type of `VLT_REGISTER_RELATIVE`.</span></span>|  
|[<span data-ttu-id="542c5-120">GetSlotIndex 方法</span><span class="sxs-lookup"><span data-stu-id="542c5-120">GetSlotIndex Method</span></span>](icordebugvariablehome-getslotindex-method.md)|<span data-ttu-id="542c5-121">获取本地变量的托管槽索引。</span><span class="sxs-lookup"><span data-stu-id="542c5-121">Gets the managed slot-index of a local variable.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="542c5-122">示例</span><span class="sxs-lookup"><span data-stu-id="542c5-122">Example</span></span>  

 <span data-ttu-id="542c5-123">下面的代码片段使用名为的 [ICorDebugCode4](icordebugcode4-interface.md) 对象 `pCode4` 。</span><span class="sxs-lookup"><span data-stu-id="542c5-123">The following code fragment uses the [ICorDebugCode4](icordebugcode4-interface.md) object named `pCode4`.</span></span>  
  
```cpp  
ICorDebugCode4 *pCode4 = NULL;  
pCode->QueryInterface(IID_ICorDebugCode4, &pCode4);  
  
ICorDebugVariableEnum *pVarLocEnum = NULL;  
pCode4->EnumerateVariableHomes(&pVarLocEnum);  
  
// retrieve local variables and arguments  
ULONG celt = 0;  
pVarLocEnum->GetCount(&celt);  
ICorDebugVariableHome **homes = new ICorDebugVariableHome *[celt];  
ULONG celtFetched = 0;  
pVarLocEnum->Next(celt, homes, &celtFetched);  
  
for (int i = 0; i < celtFetched; i++)  
{  
    VariableLocationType locType = VLT_INVALID;  
    homes[i].GetLocationType(&locType);  
    switch (locType)  
    {  
    case VLT_REGISTER:  
        CorDebugRegister register = 0;  
        locals[i].GetRegister(&register);  
        // now we know which register it is in  
        break;  
    case VLT_REGISTER_RELATIVE:  
        CorDebugRegister baseRegister = 0;  
        LONG offset = 0;  
        locals[i].GetRegister(&register);  
        locals[i].GetOffset(&offset);  
        // now we know the register-relative offset  
        break;  
    case VLT_INVALID:  
        // handle case where we can't access the location  
        break;  
    }  
}  
```  
  
## <a name="requirements"></a><span data-ttu-id="542c5-124">要求</span><span class="sxs-lookup"><span data-stu-id="542c5-124">Requirements</span></span>  

 <span data-ttu-id="542c5-125">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="542c5-125">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="542c5-126">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="542c5-126">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="542c5-127">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="542c5-127">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="542c5-128">**.NET Framework 版本：**[!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="542c5-128">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="542c5-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="542c5-129">See also</span></span>

- [<span data-ttu-id="542c5-130">调试接口</span><span class="sxs-lookup"><span data-stu-id="542c5-130">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="542c5-131">ICorDebugVariableHomeEnum 接口</span><span class="sxs-lookup"><span data-stu-id="542c5-131">ICorDebugVariableHomeEnum Interface</span></span>](icordebugvariablehomeenum-interface.md)
