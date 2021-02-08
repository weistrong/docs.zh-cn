---
description: 了解详细信息： ICorDebugInstanceFieldSymbol：： GetSize 方法
title: ICorDebugInstanceFieldSymbol::GetSize 方法
ms.date: 03/30/2017
ms.assetid: a4af1e3b-6a9f-4855-95ba-5317565c8e2b
ms.openlocfilehash: fa143620b57ec053ab26ff79b7ea2b2f386431e7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791148"
---
# <a name="icordebuginstancefieldsymbolgetsize-method"></a><span data-ttu-id="ed020-103">ICorDebugInstanceFieldSymbol::GetSize 方法</span><span class="sxs-lookup"><span data-stu-id="ed020-103">ICorDebugInstanceFieldSymbol::GetSize Method</span></span>

<span data-ttu-id="ed020-104">获取实例字段的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="ed020-104">Gets the size in bytes of the instance field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ed020-105">语法</span><span class="sxs-lookup"><span data-stu-id="ed020-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSize(  
   [out] ULONG32 *pcbSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ed020-106">参数</span><span class="sxs-lookup"><span data-stu-id="ed020-106">Parameters</span></span>  

 `pcbSize`  
 <span data-ttu-id="ed020-107">[out] 指向字段长度的指针。</span><span class="sxs-lookup"><span data-stu-id="ed020-107">[out] A pointer to length of the field.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ed020-108">备注</span><span class="sxs-lookup"><span data-stu-id="ed020-108">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="ed020-109">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="ed020-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ed020-110">要求</span><span class="sxs-lookup"><span data-stu-id="ed020-110">Requirements</span></span>  

 <span data-ttu-id="ed020-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ed020-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ed020-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ed020-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ed020-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ed020-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ed020-114">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ed020-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ed020-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="ed020-115">See also</span></span>

- [<span data-ttu-id="ed020-116">ICorDebugInstanceFieldSymbol 接口</span><span class="sxs-lookup"><span data-stu-id="ed020-116">ICorDebugInstanceFieldSymbol Interface</span></span>](icordebuginstancefieldsymbol-interface.md)
- [<span data-ttu-id="ed020-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="ed020-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
