---
description: 了解详细信息： ICorDebugMDA：： GetXML 方法
title: ICorDebugMDA::GetXML 方法
ms.date: 03/30/2017
api_name:
- ICorDebugMDA.GetXML
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugMDA::GetXML
helpviewer_keywords:
- ICorDebugMDA::GetXML method [.NET Framework debugging]
- GetXML method [.NET Framework debugging]
ms.assetid: 29746b24-3766-4255-8813-0426c45e73e5
topic_type:
- apiref
ms.openlocfilehash: fa506e6e8f306271f10a7a715af9b8bc6a80c1d6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801130"
---
# <a name="icordebugmdagetxml-method"></a><span data-ttu-id="3a99a-103">ICorDebugMDA::GetXML 方法</span><span class="sxs-lookup"><span data-stu-id="3a99a-103">ICorDebugMDA::GetXML Method</span></span>

<span data-ttu-id="3a99a-104">获取与托管调试助手关联的完整 XML 流 (MDA) 表示的 [ICorDebugMDA](icordebugmda-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="3a99a-104">Gets the full XML stream associated with the managed debugging assistant (MDA) represented by [ICorDebugMDA](icordebugmda-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3a99a-105">语法</span><span class="sxs-lookup"><span data-stu-id="3a99a-105">Syntax</span></span>  
  
```cpp  
HRESULT GetXML (  
    [in] ULONG32   cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]  
        WCHAR      szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3a99a-106">参数</span><span class="sxs-lookup"><span data-stu-id="3a99a-106">Parameters</span></span>  

 `cchName`  
 <span data-ttu-id="3a99a-107">[in] `szName` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="3a99a-107">[in] The size of the `szName` array.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="3a99a-108">弄指向 XML 流长度的指针。</span><span class="sxs-lookup"><span data-stu-id="3a99a-108">[out] A pointer to the length of the XML stream.</span></span>  
  
 `szName`  
 <span data-ttu-id="3a99a-109">弄要在其中存储 XML 流的数组。</span><span class="sxs-lookup"><span data-stu-id="3a99a-109">[out] An array in which to store the XML stream.</span></span> <span data-ttu-id="3a99a-110">该数组可能为空。</span><span class="sxs-lookup"><span data-stu-id="3a99a-110">The array may be empty.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3a99a-111">备注</span><span class="sxs-lookup"><span data-stu-id="3a99a-111">Remarks</span></span>  

 <span data-ttu-id="3a99a-112">此 `GetXML` 方法可能会影响性能，具体取决于关联的 XML 流的大小。</span><span class="sxs-lookup"><span data-stu-id="3a99a-112">The `GetXML` method can potentially affect performance, depending on the size of the associated XML stream.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3a99a-113">要求</span><span class="sxs-lookup"><span data-stu-id="3a99a-113">Requirements</span></span>  

 <span data-ttu-id="3a99a-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3a99a-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3a99a-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3a99a-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3a99a-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3a99a-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3a99a-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3a99a-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3a99a-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="3a99a-118">See also</span></span>

- [<span data-ttu-id="3a99a-119">ICorDebugMDA 接口</span><span class="sxs-lookup"><span data-stu-id="3a99a-119">ICorDebugMDA Interface</span></span>](icordebugmda-interface.md)
- [<span data-ttu-id="3a99a-120">使用托管调试助手诊断错误</span><span class="sxs-lookup"><span data-stu-id="3a99a-120">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
