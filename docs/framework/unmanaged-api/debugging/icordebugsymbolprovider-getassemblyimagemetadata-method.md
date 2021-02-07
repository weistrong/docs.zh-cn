---
description: 了解详细信息： ICorDebugSymbolProvider：： GetAssemblyImageMetadata 方法
title: ICorDebugSymbolProvider::GetAssemblyImageMetadata 方法
ms.date: 03/30/2017
ms.assetid: c3c9de67-b865-4ecf-b887-1f1d0719a0c0
ms.openlocfilehash: 4abe5cc2b2a31f89e6ca4f8fc643f26eac276515
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99717181"
---
# <a name="icordebugsymbolprovidergetassemblyimagemetadata-method"></a><span data-ttu-id="67d3b-103">ICorDebugSymbolProvider::GetAssemblyImageMetadata 方法</span><span class="sxs-lookup"><span data-stu-id="67d3b-103">ICorDebugSymbolProvider::GetAssemblyImageMetadata Method</span></span>

<span data-ttu-id="67d3b-104">返回合并程序集中的元数据。</span><span class="sxs-lookup"><span data-stu-id="67d3b-104">Returns the metadata from a merged assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="67d3b-105">语法</span><span class="sxs-lookup"><span data-stu-id="67d3b-105">Syntax</span></span>  
  
```cpp  
HRESULT GetAssemblyImageMetadata(  
   [out] ICorDebugMemoryBuffer** ppMemoryBuffer  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="67d3b-106">参数</span><span class="sxs-lookup"><span data-stu-id="67d3b-106">Parameters</span></span>  

 `ppMemoryBuffer`  
 <span data-ttu-id="67d3b-107">弄指向 [ICorDebugMemoryBuffer](icordebugmemorybuffer-interface.md) 对象地址的指针，该对象包含有关合并的程序集元数据的大小和地址的信息。</span><span class="sxs-lookup"><span data-stu-id="67d3b-107">[out] A pointer to the address of an [ICorDebugMemoryBuffer](icordebugmemorybuffer-interface.md) object that contains information about the size and address of the merged assembly's metadata.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="67d3b-108">备注</span><span class="sxs-lookup"><span data-stu-id="67d3b-108">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="67d3b-109">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="67d3b-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="67d3b-110">要求</span><span class="sxs-lookup"><span data-stu-id="67d3b-110">Requirements</span></span>  

 <span data-ttu-id="67d3b-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="67d3b-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="67d3b-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="67d3b-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="67d3b-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="67d3b-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="67d3b-114">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="67d3b-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="67d3b-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="67d3b-115">See also</span></span>

- [<span data-ttu-id="67d3b-116">ICorDebugSymbolProvider 接口</span><span class="sxs-lookup"><span data-stu-id="67d3b-116">ICorDebugSymbolProvider Interface</span></span>](icordebugsymbolprovider-interface.md)
- [<span data-ttu-id="67d3b-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="67d3b-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
