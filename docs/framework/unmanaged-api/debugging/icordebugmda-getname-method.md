---
description: 了解详细信息： ICorDebugMDA：： GetName 方法
title: ICorDebugMDA::GetName 方法
ms.date: 03/30/2017
api_name:
- ICorDebugMDA.GetName
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugMDA::GetName
helpviewer_keywords:
- ICorDebugMDA::GetName method [.NET Framework debugging]
- GetName method, ICorDebugMDA interface [.NET Framework debugging]
ms.assetid: 885bf5e8-00b7-4cd7-9d8d-e720d47918c4
topic_type:
- apiref
ms.openlocfilehash: 4ea39f062071073684a20d8f60875fbaaab43a2f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801158"
---
# <a name="icordebugmdagetname-method"></a><span data-ttu-id="c05e7-103">ICorDebugMDA::GetName 方法</span><span class="sxs-lookup"><span data-stu-id="c05e7-103">ICorDebugMDA::GetName Method</span></span>

<span data-ttu-id="c05e7-104">获取一个字符串，该字符串包含 [ICorDebugMDA](icordebugmda-interface.md)表示的托管调试助手 (MDA) 。</span><span class="sxs-lookup"><span data-stu-id="c05e7-104">Gets a string containing the name of the managed debugging assistant (MDA) represented by [ICorDebugMDA](icordebugmda-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c05e7-105">语法</span><span class="sxs-lookup"><span data-stu-id="c05e7-105">Syntax</span></span>  
  
```cpp  
HRESULT GetName (  
    [in] ULONG32   cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]  
        WCHAR      szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c05e7-106">参数</span><span class="sxs-lookup"><span data-stu-id="c05e7-106">Parameters</span></span>  

 `cchName`  
 <span data-ttu-id="c05e7-107">[in] `szName` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="c05e7-107">[in] The size of the `szName` array.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="c05e7-108">弄指向名称长度的指针。</span><span class="sxs-lookup"><span data-stu-id="c05e7-108">[out] A pointer to the length of the name.</span></span>  
  
 `szName`  
 <span data-ttu-id="c05e7-109">弄要在其中存储名称的数组。</span><span class="sxs-lookup"><span data-stu-id="c05e7-109">[out] An array in which to store the name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c05e7-110">备注</span><span class="sxs-lookup"><span data-stu-id="c05e7-110">Remarks</span></span>  

 <span data-ttu-id="c05e7-111">MDA 名称是唯一值。</span><span class="sxs-lookup"><span data-stu-id="c05e7-111">MDA names are unique values.</span></span> <span data-ttu-id="c05e7-112">`GetName`方法是获取 XML 流并基于该架构从流中提取名称的一种方便的性能方法。</span><span class="sxs-lookup"><span data-stu-id="c05e7-112">The `GetName` method is a convenient performance alternative to getting the XML stream and extracting the name from the stream based on the schema.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c05e7-113">要求</span><span class="sxs-lookup"><span data-stu-id="c05e7-113">Requirements</span></span>  

 <span data-ttu-id="c05e7-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c05e7-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c05e7-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c05e7-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c05e7-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c05e7-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c05e7-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c05e7-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c05e7-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="c05e7-118">See also</span></span>

- [<span data-ttu-id="c05e7-119">ICorDebugMDA 接口</span><span class="sxs-lookup"><span data-stu-id="c05e7-119">ICorDebugMDA Interface</span></span>](icordebugmda-interface.md)
- [<span data-ttu-id="c05e7-120">使用托管调试助手诊断错误</span><span class="sxs-lookup"><span data-stu-id="c05e7-120">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
