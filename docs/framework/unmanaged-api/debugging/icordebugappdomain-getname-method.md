---
description: 了解详细信息： ICorDebugAppDomain：： GetName 方法
title: ICorDebugAppDomain::GetName 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.GetName
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::GetName
helpviewer_keywords:
- ICorDebugAppDomain::GetName method [.NET Framework debugging]
- GetName method, ICorDebugAppDomain interface [.NET Framework debugging]
ms.assetid: 02c596d7-00b0-4e2c-856b-5425158fcefd
topic_type:
- apiref
ms.openlocfilehash: 56995f544e1576534e35b899a659ed409972305f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772414"
---
# <a name="icordebugappdomaingetname-method"></a><span data-ttu-id="756bf-103">ICorDebugAppDomain::GetName 方法</span><span class="sxs-lookup"><span data-stu-id="756bf-103">ICorDebugAppDomain::GetName Method</span></span>

<span data-ttu-id="756bf-104">获取应用程序域的名称。</span><span class="sxs-lookup"><span data-stu-id="756bf-104">Gets the name of the application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="756bf-105">语法</span><span class="sxs-lookup"><span data-stu-id="756bf-105">Syntax</span></span>  
  
```cpp  
HRESULT GetName (  
    [in]  ULONG32           cchName,  
    [out] ULONG32           *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]
         WCHAR              szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="756bf-106">参数</span><span class="sxs-lookup"><span data-stu-id="756bf-106">Parameters</span></span>  

 `cchName`  
 <span data-ttu-id="756bf-107">[in] `szName` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="756bf-107">[in] The size of the `szName` array.</span></span> <span data-ttu-id="756bf-108">将此值设置为零可以在查询模式下放置此方法。</span><span class="sxs-lookup"><span data-stu-id="756bf-108">Set this value to zero to put this method in query mode.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="756bf-109">弄一个指针，指向在中实际返回的名称的大小或字符数 `szName` 。</span><span class="sxs-lookup"><span data-stu-id="756bf-109">[out] A pointer to the size of the name or the number of characters actually returned in `szName`.</span></span> <span data-ttu-id="756bf-110">在查询模式下，此值允许调用方了解要为名称分配的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="756bf-110">In query mode, this value lets the caller know how large a buffer to allocate for the name.</span></span>  
  
 `szName`  
 <span data-ttu-id="756bf-111">弄一个数组，该数组存储应用程序域的名称。</span><span class="sxs-lookup"><span data-stu-id="756bf-111">[out] An array that stores the name of the application domain.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="756bf-112">备注</span><span class="sxs-lookup"><span data-stu-id="756bf-112">Remarks</span></span>  

 <span data-ttu-id="756bf-113">调试器调用 `GetName` 方法一次，以获取该名称所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="756bf-113">A debugger calls the `GetName` method once to get the size of a buffer needed for the name.</span></span> <span data-ttu-id="756bf-114">调试器将分配缓冲区，然后再次调用方法来填充缓冲区。</span><span class="sxs-lookup"><span data-stu-id="756bf-114">The debugger allocates the buffer, and then calls the method a second time to fill the buffer.</span></span> <span data-ttu-id="756bf-115">要获取名称大小的第一次调用称为 *查询模式*。</span><span class="sxs-lookup"><span data-stu-id="756bf-115">The first call, to get the size of the name, is referred to as *query mode*.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="756bf-116">要求</span><span class="sxs-lookup"><span data-stu-id="756bf-116">Requirements</span></span>  

 <span data-ttu-id="756bf-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="756bf-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="756bf-118">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="756bf-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="756bf-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="756bf-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="756bf-120">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="756bf-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
