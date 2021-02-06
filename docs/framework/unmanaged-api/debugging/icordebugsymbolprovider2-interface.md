---
description: 了解详细信息： ICorDebugSymbolProvider2 接口
title: ICorDebugSymbolProvider2 接口
ms.date: 03/30/2017
ms.assetid: 1c9c3d92-f0de-4d4d-87f1-0c702a4808af
ms.openlocfilehash: b4eaeb29c15da979a522fb20e33a56030889d0c4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99659499"
---
# <a name="icordebugsymbolprovider2-interface"></a><span data-ttu-id="0eae3-103">ICorDebugSymbolProvider2 接口</span><span class="sxs-lookup"><span data-stu-id="0eae3-103">ICorDebugSymbolProvider2 Interface</span></span>

<span data-ttu-id="0eae3-104">以逻辑方式扩展 [ICorDebugSymbolProvider](icordebugsymbolprovider-interface.md) 接口以检索其他调试符号信息。</span><span class="sxs-lookup"><span data-stu-id="0eae3-104">Logically extends the [ICorDebugSymbolProvider](icordebugsymbolprovider-interface.md) interface to retrieve additional debug symbol information.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="0eae3-105">方法</span><span class="sxs-lookup"><span data-stu-id="0eae3-105">Methods</span></span>  
  
|<span data-ttu-id="0eae3-106">方法</span><span class="sxs-lookup"><span data-stu-id="0eae3-106">Method</span></span>|<span data-ttu-id="0eae3-107">说明</span><span class="sxs-lookup"><span data-stu-id="0eae3-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="0eae3-108">GetFrameProps 方法</span><span class="sxs-lookup"><span data-stu-id="0eae3-108">GetFrameProps Method</span></span>](icordebugsymbolprovider2-getframeprops-method.md)|<span data-ttu-id="0eae3-109">返回启动方法相对虚拟地址的方法和具有代码相对虚拟地址的父框架。</span><span class="sxs-lookup"><span data-stu-id="0eae3-109">Returns the method starting relative virtual address of a method and the parent frame given a code relative virtual address.</span></span>|  
|[<span data-ttu-id="0eae3-110">GetGenericDictionaryInfo 方法</span><span class="sxs-lookup"><span data-stu-id="0eae3-110">GetGenericDictionaryInfo Method</span></span>](icordebugsymbolprovider2-getgenericdictionaryinfo-method.md)|<span data-ttu-id="0eae3-111">检索泛型字典映射。</span><span class="sxs-lookup"><span data-stu-id="0eae3-111">Retrieves a generic dictionary map.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0eae3-112">备注</span><span class="sxs-lookup"><span data-stu-id="0eae3-112">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="0eae3-113">此接口仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="0eae3-113">This interface is available with .NET Native only.</span></span> <span data-ttu-id="0eae3-114">如果在 .NET Native 外为 ICorDebug 方案实现此接口，则公共语言运行时将忽略此接口。</span><span class="sxs-lookup"><span data-stu-id="0eae3-114">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0eae3-115">要求</span><span class="sxs-lookup"><span data-stu-id="0eae3-115">Requirements</span></span>  

 <span data-ttu-id="0eae3-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0eae3-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0eae3-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0eae3-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0eae3-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0eae3-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0eae3-119">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0eae3-119">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0eae3-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="0eae3-120">See also</span></span>

- [<span data-ttu-id="0eae3-121">ICorDebugSymbolProvider 接口</span><span class="sxs-lookup"><span data-stu-id="0eae3-121">ICorDebugSymbolProvider Interface</span></span>](icordebugsymbolprovider-interface.md)
- [<span data-ttu-id="0eae3-122">调试接口</span><span class="sxs-lookup"><span data-stu-id="0eae3-122">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="0eae3-123">调试</span><span class="sxs-lookup"><span data-stu-id="0eae3-123">Debugging</span></span>](index.md)
