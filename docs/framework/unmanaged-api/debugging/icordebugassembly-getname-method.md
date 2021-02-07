---
description: 了解详细信息： ICorDebugAssembly：： GetName 方法
title: ICorDebugAssembly::GetName 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAssembly.GetName
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssembly::GetName
helpviewer_keywords:
- ICorDebugAssembly::GetName method [.NET Framework debugging]
- GetName method, ICorDebugAssembly interface [.NET Framework debugging]
ms.assetid: cdeda721-b214-4503-a291-c70b68b5f36b
topic_type:
- apiref
ms.openlocfilehash: c2ffa910eaf97c5539a33dbcd3486b7dfb117b51
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711981"
---
# <a name="icordebugassemblygetname-method"></a><span data-ttu-id="5dc5d-103">ICorDebugAssembly::GetName 方法</span><span class="sxs-lookup"><span data-stu-id="5dc5d-103">ICorDebugAssembly::GetName Method</span></span>

<span data-ttu-id="5dc5d-104">获取此实例表示的程序集的名称 `ICorDebugAssembly` 。</span><span class="sxs-lookup"><span data-stu-id="5dc5d-104">Gets the name of the assembly that this `ICorDebugAssembly` instance represents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5dc5d-105">语法</span><span class="sxs-lookup"><span data-stu-id="5dc5d-105">Syntax</span></span>  
  
```cpp  
HRESULT GetName (  
    [in] ULONG32  cchName,  
    [out] ULONG32 *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5dc5d-106">参数</span><span class="sxs-lookup"><span data-stu-id="5dc5d-106">Parameters</span></span>  

 `cchName`  
 <span data-ttu-id="5dc5d-107">[in] `szName` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="5dc5d-107">[in] The size of the `szName` array.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="5dc5d-108">弄指向整数的指针，该整数指定名称的实际长度。</span><span class="sxs-lookup"><span data-stu-id="5dc5d-108">[out] A pointer to an integer that specifies the actual length of the name.</span></span>  
  
 `szName`  
 <span data-ttu-id="5dc5d-109">弄存储名称的数组。</span><span class="sxs-lookup"><span data-stu-id="5dc5d-109">[out] An array that stores the name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5dc5d-110">备注</span><span class="sxs-lookup"><span data-stu-id="5dc5d-110">Remarks</span></span>  

 <span data-ttu-id="5dc5d-111">`GetName`方法返回程序集的完整路径和文件名。</span><span class="sxs-lookup"><span data-stu-id="5dc5d-111">The `GetName` method returns the full path and file name of the assembly.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5dc5d-112">要求</span><span class="sxs-lookup"><span data-stu-id="5dc5d-112">Requirements</span></span>  

 <span data-ttu-id="5dc5d-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5dc5d-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5dc5d-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5dc5d-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5dc5d-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5dc5d-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5dc5d-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5dc5d-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
