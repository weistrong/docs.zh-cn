---
description: 了解详细信息： ICorDebugProcess6：： GetCode 方法
title: ICorDebugProcess6::GetCode 方法
ms.date: 03/30/2017
ms.assetid: faa538c2-60c9-4064-b996-1b4c24ebd751
ms.openlocfilehash: a7cb71ddb1e65cda37d762a0fba958d413145138
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99649658"
---
# <a name="icordebugprocess6getcode-method"></a><span data-ttu-id="d8329-103">ICorDebugProcess6::GetCode 方法</span><span class="sxs-lookup"><span data-stu-id="d8329-103">ICorDebugProcess6::GetCode Method</span></span>

<span data-ttu-id="d8329-104">获取特定代码地址上的托管代码的相关信息。</span><span class="sxs-lookup"><span data-stu-id="d8329-104">Gets information about the managed code at a particular code address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d8329-105">语法</span><span class="sxs-lookup"><span data-stu-id="d8329-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCode(  
    [in] CORDB_ADDRESS codeAddress,
    [out] ICorDebugCode **ppCode);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d8329-106">参数</span><span class="sxs-lookup"><span data-stu-id="d8329-106">Parameters</span></span>  

 `codeAddress`  
 <span data-ttu-id="d8329-107">中一个 [CORDB_ADDRESS](../common-data-types-unmanaged-api-reference.md) 值，该值指定托管代码段的起始地址。</span><span class="sxs-lookup"><span data-stu-id="d8329-107">[in] A [CORDB_ADDRESS](../common-data-types-unmanaged-api-reference.md) value that specifies the starting address of the managed code segment.</span></span>  
  
 `ppCode`  
 <span data-ttu-id="d8329-108">弄指向表示托管代码段的 "ICorDebugCode" 对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="d8329-108">[out] A pointer to the address of an "ICorDebugCode" object that represents a segment of managed code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d8329-109">备注</span><span class="sxs-lookup"><span data-stu-id="d8329-109">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="d8329-110">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="d8329-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d8329-111">要求</span><span class="sxs-lookup"><span data-stu-id="d8329-111">Requirements</span></span>  

 <span data-ttu-id="d8329-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d8329-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d8329-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d8329-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d8329-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d8329-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d8329-115">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d8329-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d8329-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="d8329-116">See also</span></span>

- [<span data-ttu-id="d8329-117">“ICor调试进程6”接口</span><span class="sxs-lookup"><span data-stu-id="d8329-117">ICorDebugProcess6 Interface</span></span>](icordebugprocess6-interface.md)
- [<span data-ttu-id="d8329-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="d8329-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
