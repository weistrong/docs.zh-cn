---
description: 了解详细信息： ICorDebugModule：： GetMetaDataInterface 方法
title: ICorDebugModule::GetMetaDataInterface 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetMetaDataInterface
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetMetaDataInterface
helpviewer_keywords:
- ICorDebugModule::GetMetaDatainterface method [.NET Framework debugging]
- GetMetaDatainterface method [.NET Framework debugging]
ms.assetid: 30d906f2-cf35-4fa9-9d4c-0c31b58c9f3a
topic_type:
- apiref
ms.openlocfilehash: 39af2560b4c10f6dc490bfba5425e2339a7c1823
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99691635"
---
# <a name="icordebugmodulegetmetadatainterface-method"></a><span data-ttu-id="90b59-103">ICorDebugModule::GetMetaDataInterface 方法</span><span class="sxs-lookup"><span data-stu-id="90b59-103">ICorDebugModule::GetMetaDataInterface Method</span></span>

<span data-ttu-id="90b59-104">获取可用于检查模块的元数据的元数据接口对象。</span><span class="sxs-lookup"><span data-stu-id="90b59-104">Gets a metadata interface object that can be used to examine the metadata for the module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="90b59-105">语法</span><span class="sxs-lookup"><span data-stu-id="90b59-105">Syntax</span></span>  
  
```cpp  
HRESULT GetMetaDataInterface (  
    [in] REFIID      riid,  
    [out] IUnknown **ppObj  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="90b59-106">参数</span><span class="sxs-lookup"><span data-stu-id="90b59-106">Parameters</span></span>  

 `riid`  
 <span data-ttu-id="90b59-107">中用于指定元数据接口的引用 ID。</span><span class="sxs-lookup"><span data-stu-id="90b59-107">[in] The reference ID that specifies the metadata interface.</span></span>  
  
 `ppObj`  
 <span data-ttu-id="90b59-108">弄指向对象地址的指针，该 `T:IUnknown` 对象是一个 [元数据接口](../metadata/metadata-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="90b59-108">[out] A pointer to the address of an `T:IUnknown` object that is one of the [metadata interfaces](../metadata/metadata-interfaces.md).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="90b59-109">备注</span><span class="sxs-lookup"><span data-stu-id="90b59-109">Remarks</span></span>  

 <span data-ttu-id="90b59-110">调试器可以使用 `GetMetaDataInterface` 方法创建模块的原始元数据的副本，必须执行此操作才能编辑该模块。</span><span class="sxs-lookup"><span data-stu-id="90b59-110">The debugger can use the `GetMetaDataInterface` method to make a copy of the original metadata for a module, which it must do in order to edit that module.</span></span> <span data-ttu-id="90b59-111">调试器调用 `GetMetaDataInterface` 以获取该模块的 [IMetaDataEmit](../metadata/imetadataemit-interface.md) 接口对象，然后调用 [IMetaDataEmit：： SaveToMemory](../metadata/imetadataemit-savetomemory-method.md) 将模块的元数据副本保存到内存。</span><span class="sxs-lookup"><span data-stu-id="90b59-111">The debugger calls `GetMetaDataInterface` to get an [IMetaDataEmit](../metadata/imetadataemit-interface.md) interface object for the module, then calls [IMetaDataEmit::SaveToMemory](../metadata/imetadataemit-savetomemory-method.md) to save a copy of the module's metadata to memory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="90b59-112">要求</span><span class="sxs-lookup"><span data-stu-id="90b59-112">Requirements</span></span>  

 <span data-ttu-id="90b59-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="90b59-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="90b59-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="90b59-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="90b59-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="90b59-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="90b59-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="90b59-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="90b59-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="90b59-117">See also</span></span>

- <span data-ttu-id="90b59-118">Metadata </span><span class="sxs-lookup"><span data-stu-id="90b59-118">[Metadata](../metadata/index.md)</span></span>
