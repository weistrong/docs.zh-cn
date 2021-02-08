---
description: 了解详细信息： ICorDebugType2 接口
title: ICorDebugType2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugType2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugType2
helpviewer_keywords:
- ICorDebugType2 interface
ms.assetid: 376fb03f-f1ef-4107-baa4-4d9d55884862
topic_type:
- apiref
ms.openlocfilehash: 8691cf294e835bef0f5a0ac694110f73577fb5d3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800864"
---
# <a name="icordebugtype2-interface"></a><span data-ttu-id="17dce-103">ICorDebugType2 接口</span><span class="sxs-lookup"><span data-stu-id="17dce-103">ICorDebugType2 Interface</span></span>

<span data-ttu-id="17dce-104">扩展 ICorDebugType 接口以检索基类型或复杂 (用户定义的) 类型的类型标识符。</span><span class="sxs-lookup"><span data-stu-id="17dce-104">Extends the ICorDebugType interface to retrieve the type identifier  of a base type or complex (user-defined) type.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="17dce-105">方法</span><span class="sxs-lookup"><span data-stu-id="17dce-105">Methods</span></span>  
  
|<span data-ttu-id="17dce-106">方法</span><span class="sxs-lookup"><span data-stu-id="17dce-106">Method</span></span>||  
|------------|-|  
|[<span data-ttu-id="17dce-107">GetTypeID 方法</span><span class="sxs-lookup"><span data-stu-id="17dce-107">GetTypeID Method</span></span>](icordebugtype2-gettypeid-method.md)|<span data-ttu-id="17dce-108">获取此类型的 [COR_TYPEID](cor-typeid-structure.md) 。</span><span class="sxs-lookup"><span data-stu-id="17dce-108">Gets a [COR_TYPEID](cor-typeid-structure.md) for this type.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="17dce-109">备注</span><span class="sxs-lookup"><span data-stu-id="17dce-109">Remarks</span></span>  

 <span data-ttu-id="17dce-110">此接口是 ICorDebugType 接口的逻辑扩展。</span><span class="sxs-lookup"><span data-stu-id="17dce-110">This interface is a logical extension of the ICorDebugType interface.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="17dce-111">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="17dce-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="example"></a><span data-ttu-id="17dce-112">示例</span><span class="sxs-lookup"><span data-stu-id="17dce-112">Example</span></span>  

 <span data-ttu-id="17dce-113">下面的代码段演示了如何使用 [ICorDebugType2：： GetTypeID](icordebugtype2-gettypeid-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="17dce-113">The following code fragment illustrates the use of the [ICorDebugType2::GetTypeID](icordebugtype2-gettypeid-method.md) method.</span></span>  
  
```cpp  
// (error checking omitted for brevity)  
// given an ICorDebugType *pType  
  
ICorDebugType2 *pType2 = NULL;  
pType->QueryInterface(IID_ICorDebugType2, &pType);  
  
COR_TYPEID id;  
pType2->GetTypeID(&id);  
  
// now we can use existing APIs to get information about this COR_TYPEID  
```  
  
## <a name="requirements"></a><span data-ttu-id="17dce-114">要求</span><span class="sxs-lookup"><span data-stu-id="17dce-114">Requirements</span></span>  

 <span data-ttu-id="17dce-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="17dce-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="17dce-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="17dce-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="17dce-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="17dce-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="17dce-118">**.NET Framework 版本：**[!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="17dce-118">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="17dce-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="17dce-119">See also</span></span>

- [<span data-ttu-id="17dce-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="17dce-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
