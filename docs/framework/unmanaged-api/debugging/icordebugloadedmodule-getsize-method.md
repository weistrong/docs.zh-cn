---
description: 了解详细信息： ICorDebugLoadedModule：： GetSize 方法
title: ICorDebugLoadedModule::GetSize 方法
ms.date: 03/30/2017
ms.assetid: aaa0e5c0-be9d-4fe1-8418-5295b9b184d6
ms.openlocfilehash: 6701d2578559a039f352df19bf9e859658c6687f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801236"
---
# <a name="icordebugloadedmodulegetsize-method"></a><span data-ttu-id="46ea8-103">ICorDebugLoadedModule::GetSize 方法</span><span class="sxs-lookup"><span data-stu-id="46ea8-103">ICorDebugLoadedModule::GetSize Method</span></span>

<span data-ttu-id="46ea8-104">获取加载模块的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="46ea8-104">Gets the size in bytes of the loaded module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="46ea8-105">语法</span><span class="sxs-lookup"><span data-stu-id="46ea8-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSize(  
   [out] ULONG32 *pcBytes  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="46ea8-106">参数</span><span class="sxs-lookup"><span data-stu-id="46ea8-106">Parameters</span></span>  

 `pcBytes`  
 <span data-ttu-id="46ea8-107">[out] 指向已加载模块中字节数的指针。</span><span class="sxs-lookup"><span data-stu-id="46ea8-107">[out] A pointer to the number of bytes in the loaded module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="46ea8-108">备注</span><span class="sxs-lookup"><span data-stu-id="46ea8-108">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="46ea8-109">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="46ea8-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="46ea8-110">要求</span><span class="sxs-lookup"><span data-stu-id="46ea8-110">Requirements</span></span>  

 <span data-ttu-id="46ea8-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="46ea8-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="46ea8-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="46ea8-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="46ea8-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="46ea8-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="46ea8-114">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="46ea8-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46ea8-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="46ea8-115">See also</span></span>

- [<span data-ttu-id="46ea8-116">ICorDebugLoadedModule 接口</span><span class="sxs-lookup"><span data-stu-id="46ea8-116">ICorDebugLoadedModule Interface</span></span>](icordebugloadedmodule-interface.md)
- [<span data-ttu-id="46ea8-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="46ea8-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
