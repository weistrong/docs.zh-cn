---
description: 了解详细信息： ICorDebugLoadedModule：： GetBaseAddress 方法
title: ICorDebugLoadedModule::GetBaseAddress 方法
ms.date: 03/30/2017
ms.assetid: 7c036772-d58a-47f1-a5fa-31779898ef0d
ms.openlocfilehash: 2852131d543cfb9593cf4ff607d1f752226c2880
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801262"
---
# <a name="icordebugloadedmodulegetbaseaddress-method"></a><span data-ttu-id="680e1-103">ICorDebugLoadedModule::GetBaseAddress 方法</span><span class="sxs-lookup"><span data-stu-id="680e1-103">ICorDebugLoadedModule::GetBaseAddress Method</span></span>

<span data-ttu-id="680e1-104">获取已加载模块的基址。</span><span class="sxs-lookup"><span data-stu-id="680e1-104">Gets the base address of the loaded module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="680e1-105">语法</span><span class="sxs-lookup"><span data-stu-id="680e1-105">Syntax</span></span>  
  
```cpp  
HRESULT GetBaseAddress(  
   [out] CORDB_ADDRESS *pAddress  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="680e1-106">参数</span><span class="sxs-lookup"><span data-stu-id="680e1-106">Parameters</span></span>  

 `pAddress`  
 <span data-ttu-id="680e1-107">[out] 指向已加载模块的基址的指针。</span><span class="sxs-lookup"><span data-stu-id="680e1-107">[out] A pointer to the base address of the loaded module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="680e1-108">备注</span><span class="sxs-lookup"><span data-stu-id="680e1-108">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="680e1-109">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="680e1-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="680e1-110">要求</span><span class="sxs-lookup"><span data-stu-id="680e1-110">Requirements</span></span>  

 <span data-ttu-id="680e1-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="680e1-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="680e1-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="680e1-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="680e1-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="680e1-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="680e1-114">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="680e1-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="680e1-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="680e1-115">See also</span></span>

- [<span data-ttu-id="680e1-116">ICorDebugLoadedModule 接口</span><span class="sxs-lookup"><span data-stu-id="680e1-116">ICorDebugLoadedModule Interface</span></span>](icordebugloadedmodule-interface.md)
- [<span data-ttu-id="680e1-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="680e1-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
