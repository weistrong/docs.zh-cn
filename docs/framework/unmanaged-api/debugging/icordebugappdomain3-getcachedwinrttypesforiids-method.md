---
description: 了解详细信息： ICorDebugAppDomain3：： GetCachedWinRTTypesForIIDs 方法
title: ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain3.GetCachedWinRTTypesForIIDs
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs
helpviewer_keywords:
- ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs method, [.NET Framework debugging]
- GetCachedWinRTTypesForIIDs method, ICorDebugAppDomain3 interface [.NET Framework debugging]
ms.assetid: 23682ca0-1bcf-48e6-996e-69f7ba337682
topic_type:
- apiref
ms.openlocfilehash: 76b93cdb8c465935a4aaf36090ee44f2b6253a3b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754168"
---
# <a name="icordebugappdomain3getcachedwinrttypesforiids-method"></a><span data-ttu-id="7f929-103">ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs 方法</span><span class="sxs-lookup"><span data-stu-id="7f929-103">ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs Method</span></span>

<span data-ttu-id="7f929-104">基于其接口标识符获取应用程序域中缓存的 Windows 运行时类型的枚举器。</span><span class="sxs-lookup"><span data-stu-id="7f929-104">Gets an enumerator for cached Windows Runtime types in an application domain based on their interface identifiers.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7f929-105">语法</span><span class="sxs-lookup"><span data-stu-id="7f929-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCachedWinRTTypesForIIDs (
    [in]  ULONG32            cReqTypes,  
    [in]  GUID                *iidsToResolve,  
    [out] ICorDebugTypeEnum   **ppTypesEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7f929-106">参数</span><span class="sxs-lookup"><span data-stu-id="7f929-106">Parameters</span></span>  

 `cReqTypes`  
 <span data-ttu-id="7f929-107">中所需类型的数目。</span><span class="sxs-lookup"><span data-stu-id="7f929-107">[in] The number of required types.</span></span>  
  
 `iidsToResolve`  
 <span data-ttu-id="7f929-108">中指向数组的指针，该数组包含与要检索的 Windows 运行时类型的托管表示形式对应的接口标识符。</span><span class="sxs-lookup"><span data-stu-id="7f929-108">[in] A pointer to an array that contains the interface identifiers corresponding to the managed representations of the Windows Runtime types to be retrieved.</span></span>  
  
 `ppTypesEnum`  
 <span data-ttu-id="7f929-109">弄一个指向 "ICorDebugTypeEnum" 接口对象地址的指针，该对象可基于中的接口标识符枚举检索到的 Windows 运行时类型的缓存托管表示形式 `iidsToResolve` 。</span><span class="sxs-lookup"><span data-stu-id="7f929-109">[out] A pointer to the address of an "ICorDebugTypeEnum" interface object that allows enumeration of the cached managed representations of the Windows Runtime types retrieved, based on the interface identifiers in `iidsToResolve`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7f929-110">备注</span><span class="sxs-lookup"><span data-stu-id="7f929-110">Remarks</span></span>  

 <span data-ttu-id="7f929-111">如果该方法无法检索特定接口标识符的信息，则 "ICorDebugTypeEnum" 集合中的对应条目将有一种类型的 `ELEMENT_TYPE_END` 用于错误，这是由于数据检索问题或 `ELEMENT_TYPE_VOID` 未知接口标识符导致的。</span><span class="sxs-lookup"><span data-stu-id="7f929-111">If the method fails to retrieve information for a specific interface identifier, the corresponding entry in the "ICorDebugTypeEnum" collection will have a type of `ELEMENT_TYPE_END` for errors due to data retrieval issues, or `ELEMENT_TYPE_VOID` for unknown interface identifiers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7f929-112">要求</span><span class="sxs-lookup"><span data-stu-id="7f929-112">Requirements</span></span>  

 <span data-ttu-id="7f929-113">**平台：** Windows 运行时</span><span class="sxs-lookup"><span data-stu-id="7f929-113">**Platforms:** Windows Runtime</span></span>  
  
 <span data-ttu-id="7f929-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7f929-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7f929-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7f929-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7f929-116">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7f929-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7f929-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="7f929-117">See also</span></span>

- [<span data-ttu-id="7f929-118">ICorDebugAppDomain3 接口</span><span class="sxs-lookup"><span data-stu-id="7f929-118">ICorDebugAppDomain3 Interface</span></span>](icordebugappdomain3-interface.md)
