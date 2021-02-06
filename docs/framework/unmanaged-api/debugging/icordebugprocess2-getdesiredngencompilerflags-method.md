---
description: 了解详细信息： ICorDebugProcess2：： GetDesiredNGENCompilerFlags 方法
title: ICorDebugProcess2::GetDesiredNGENCompilerFlags 方法
ms.date: 03/30/2017
api_name:
- ICorDebugProcess2.GetDesiredNGENCompilerFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess2::GetDesiredNGENCompilerFlags
helpviewer_keywords:
- ICorDebugProcess2::GetDesiredNGENCompilerFlags method [.NET Framework debugging]
- GetDesiredNGENCompilerFlags method [.NET Framework debugging]
ms.assetid: fc834580-3a90-4315-95d2-349b6bb7d059
topic_type:
- apiref
ms.openlocfilehash: ddc1c3a958ef42ab51d0ae06fd7ff29b13829c3c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99650196"
---
# <a name="icordebugprocess2getdesiredngencompilerflags-method"></a><span data-ttu-id="0157a-103">ICorDebugProcess2::GetDesiredNGENCompilerFlags 方法</span><span class="sxs-lookup"><span data-stu-id="0157a-103">ICorDebugProcess2::GetDesiredNGENCompilerFlags Method</span></span>

<span data-ttu-id="0157a-104">获取公共语言运行时 (CLR) 使用的当前编译器标志设置来选择正确的预编译 (，即要加载到此进程中的本机) 映像。</span><span class="sxs-lookup"><span data-stu-id="0157a-104">Gets the current compiler flag settings that the common language runtime (CLR) uses to select the correct precompiled (that is, native) image to be loaded into this process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0157a-105">语法</span><span class="sxs-lookup"><span data-stu-id="0157a-105">Syntax</span></span>  
  
```cpp  
HRESULT GetDesiredNGENCompilerFlags (  
    [out] DWORD   *pdwFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0157a-106">参数</span><span class="sxs-lookup"><span data-stu-id="0157a-106">Parameters</span></span>  

 `pdwFlags`  
 <span data-ttu-id="0157a-107">弄指向 [CorDebugJITCompilerFlags](cordebugjitcompilerflags-enumeration.md) 枚举值的按位组合的指针，这些值用于选择要加载的正确预编译映像。</span><span class="sxs-lookup"><span data-stu-id="0157a-107">[out] A pointer to a bitwise combination of the [CorDebugJITCompilerFlags](cordebugjitcompilerflags-enumeration.md) enumeration values that are used to select the correct precompiled image to be loaded.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0157a-108">备注</span><span class="sxs-lookup"><span data-stu-id="0157a-108">Remarks</span></span>  

 <span data-ttu-id="0157a-109">使用 [ICorDebugProcess2：： SetDesiredNGENCompilerFlags](icordebugprocess2-setdesiredngencompilerflags-method.md) 方法设置 CLR 将用于选择要加载的正确预编译图像的标志。</span><span class="sxs-lookup"><span data-stu-id="0157a-109">Use the [ICorDebugProcess2::SetDesiredNGENCompilerFlags](icordebugprocess2-setdesiredngencompilerflags-method.md) method to set the flags that the CLR will use to select the correct pre-compiled image to load.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0157a-110">要求</span><span class="sxs-lookup"><span data-stu-id="0157a-110">Requirements</span></span>  

 <span data-ttu-id="0157a-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0157a-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0157a-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0157a-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0157a-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0157a-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0157a-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0157a-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
