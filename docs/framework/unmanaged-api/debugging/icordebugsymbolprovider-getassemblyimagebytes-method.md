---
description: 了解详细信息： ICorDebugSymbolProvider：： GetAssemblyImageBytes 方法
title: ICorDebugSymbolProvider::GetAssemblyImageBytes 方法
ms.date: 03/30/2017
ms.assetid: 3db215aa-e180-4f70-8d23-6d5a0ffbc8e5
ms.openlocfilehash: 2e08b23e35913e8767135d75d28ff66efc890565
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99717272"
---
# <a name="icordebugsymbolprovidergetassemblyimagebytes-method"></a><span data-ttu-id="db616-103">ICorDebugSymbolProvider::GetAssemblyImageBytes 方法</span><span class="sxs-lookup"><span data-stu-id="db616-103">ICorDebugSymbolProvider::GetAssemblyImageBytes Method</span></span>

<span data-ttu-id="db616-104">给定合并程序集的相对虚拟地址 (RVA)，读取合并程序集中的数据。</span><span class="sxs-lookup"><span data-stu-id="db616-104">Reads data from a merged assembly given a relative virtual address (RVA) in the merged assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="db616-105">语法</span><span class="sxs-lookup"><span data-stu-id="db616-105">Syntax</span></span>  
  
```cpp  
HRESULT GetAssemblyImageBytes(  
   [in] CORDB_ADDRESS rva,
   [in] ULONG32 length,
   [out] ICorDebugMemoryBuffer** ppMemoryBuffer  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="db616-106">参数</span><span class="sxs-lookup"><span data-stu-id="db616-106">Parameters</span></span>  

 `rva`  
 <span data-ttu-id="db616-107">[in] 合并程序集中的相对虚拟地址 (RVA)。</span><span class="sxs-lookup"><span data-stu-id="db616-107">[in] A relative virtual address (RVA) in a merged assembly.</span></span>  
  
 `length`  
 <span data-ttu-id="db616-108">要在合并程序集中读取的字节数。</span><span class="sxs-lookup"><span data-stu-id="db616-108">The number of bytes to read from the merged assembly.</span></span>  
  
 `ppMemoryBuffer`  
 <span data-ttu-id="db616-109">指向 [ICorDebugMemoryBuffer](icordebugmemorybuffer-interface.md) 对象地址的指针，该对象包含包含合并的程序集元数据的内存缓冲区的相关信息。</span><span class="sxs-lookup"><span data-stu-id="db616-109">A pointer to the address of an [ICorDebugMemoryBuffer](icordebugmemorybuffer-interface.md) object that contains information about the memory buffer with merged assembly metadata.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="db616-110">备注</span><span class="sxs-lookup"><span data-stu-id="db616-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="db616-111">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="db616-111">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="db616-112">要求</span><span class="sxs-lookup"><span data-stu-id="db616-112">Requirements</span></span>  

 <span data-ttu-id="db616-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="db616-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="db616-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="db616-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="db616-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="db616-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="db616-116">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="db616-116">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="db616-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="db616-117">See also</span></span>

- [<span data-ttu-id="db616-118">ICorDebugSymbolProvider 接口</span><span class="sxs-lookup"><span data-stu-id="db616-118">ICorDebugSymbolProvider Interface</span></span>](icordebugsymbolprovider-interface.md)
- [<span data-ttu-id="db616-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="db616-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
