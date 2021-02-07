---
description: 了解详细信息： ICorDebugDataTarget2：： GetSymbolProviderForImage 方法
title: ICorDebugDataTarget2::GetSymbolProviderForImage 方法
ms.date: 03/30/2017
ms.assetid: b7c0a2f0-e904-43b3-98e1-d669e8a589e8
ms.openlocfilehash: 7b4493b6c0959dc39d955d7691a22ac6905034b1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99764380"
---
# <a name="icordebugdatatarget2getsymbolproviderforimage-method"></a><span data-ttu-id="b3da7-103">ICorDebugDataTarget2::GetSymbolProviderForImage 方法</span><span class="sxs-lookup"><span data-stu-id="b3da7-103">ICorDebugDataTarget2::GetSymbolProviderForImage Method</span></span>

<span data-ttu-id="b3da7-104">返回该模块基址中的模块符号提供程序。</span><span class="sxs-lookup"><span data-stu-id="b3da7-104">Returns the symbol-provider for a module from the base address of that module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b3da7-105">语法</span><span class="sxs-lookup"><span data-stu-id="b3da7-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSymbolProviderForImage(  
    [in] CORDB_ADDRESS imageBaseAddress,
    [out] ICorDebugSymbolProvider **ppSymProvider  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b3da7-106">参数</span><span class="sxs-lookup"><span data-stu-id="b3da7-106">Parameters</span></span>  

 `imageBaseAddress`  
 <span data-ttu-id="b3da7-107">中一个 [CORDB_ADDRESS](../common-data-types-unmanaged-api-reference.md) 值，该值表示模块的基址。</span><span class="sxs-lookup"><span data-stu-id="b3da7-107">[in] A [CORDB_ADDRESS](../common-data-types-unmanaged-api-reference.md) value that represents the base address of a module.</span></span>  
  
 `ppSymProvider`  
 <span data-ttu-id="b3da7-108">弄指向 [ICorDebugSymbolProvider](icordebugsymbolprovider-interface.md) 对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="b3da7-108">[out] A pointer to the address of an [ICorDebugSymbolProvider](icordebugsymbolprovider-interface.md) object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b3da7-109">备注</span><span class="sxs-lookup"><span data-stu-id="b3da7-109">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="b3da7-110">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="b3da7-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b3da7-111">要求</span><span class="sxs-lookup"><span data-stu-id="b3da7-111">Requirements</span></span>  

 <span data-ttu-id="b3da7-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b3da7-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b3da7-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b3da7-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b3da7-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b3da7-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b3da7-115">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b3da7-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b3da7-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="b3da7-116">See also</span></span>

- [<span data-ttu-id="b3da7-117">“ICor调试数据目标2”接口</span><span class="sxs-lookup"><span data-stu-id="b3da7-117">ICorDebugDataTarget2 Interface</span></span>](icordebugdatatarget2-interface.md)
- [<span data-ttu-id="b3da7-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="b3da7-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
