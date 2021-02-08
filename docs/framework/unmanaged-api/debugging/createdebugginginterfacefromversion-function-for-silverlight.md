---
description: 了解有关以下内容的详细信息： Silverlight 的 CreateDebuggingInterfaceFromVersion 函数
title: Silverlight 的 CreateDebuggingInterfaceFromVersion 函数
ms.date: 03/30/2017
f1_keywords:
- CreateDebuggingInterfaceFromVersion
helpviewer_keywords:
- CreateDebuggingInterfaceFromVersion function
- debugging API [Silverlight]
- Silverlight, debugging
ms.assetid: 35c7a18f-133a-4584-bd25-bb338568b0c6
ms.openlocfilehash: 8c61593f2e912260ecca65efce9f905ce56e88dc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801444"
---
# <a name="createdebugginginterfacefromversion-function-for-silverlight"></a><span data-ttu-id="52dd7-103">Silverlight 的 CreateDebuggingInterfaceFromVersion 函数</span><span class="sxs-lookup"><span data-stu-id="52dd7-103">CreateDebuggingInterfaceFromVersion Function for Silverlight</span></span>

<span data-ttu-id="52dd7-104">接受公共语言运行时 (从 [CreateVersionStringFromModule 函数](createversionstringfrommodule-function.md)返回的 CLR) 版本字符串，并返回 (通常为 [ICorDebug](icordebug-interface.md)) 的相应调试器接口。</span><span class="sxs-lookup"><span data-stu-id="52dd7-104">Accepts a common language runtime (CLR) version string that is returned from the [CreateVersionStringFromModule function](createversionstringfrommodule-function.md), and returns a corresponding debugger interface (typically, [ICorDebug](icordebug-interface.md)).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="52dd7-105">语法</span><span class="sxs-lookup"><span data-stu-id="52dd7-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateDebuggingInterfaceFromVersion (  
    [in]  LPCWSTR      szDebuggeeVersion,  
    [out] IUnknown**   ppCordb,  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="52dd7-106">参数</span><span class="sxs-lookup"><span data-stu-id="52dd7-106">Parameters</span></span>  

 `szDebuggeeVersion`\
 <span data-ttu-id="52dd7-107">中目标调试对象（由 [CreateVersionStringFromModule 函数](createversionstringfrommodule-function.md)返回）中的 CLR 的版本字符串。</span><span class="sxs-lookup"><span data-stu-id="52dd7-107">[in] Version string of the CLR in the target debuggee, which is returned by the [CreateVersionStringFromModule function](createversionstringfrommodule-function.md).</span></span>  
  
 `ppCordb`\
 <span data-ttu-id="52dd7-108">[out] 指向“COM 对象的指针”的指针 (`IUnknown`)。</span><span class="sxs-lookup"><span data-stu-id="52dd7-108">[out] Pointer to a pointer to a COM object (`IUnknown`).</span></span> <span data-ttu-id="52dd7-109">此对象将在返回之前强制转换为 [ICorDebug](icordebug-interface.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="52dd7-109">This object will be cast to an [ICorDebug](icordebug-interface.md) object before it is returned.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="52dd7-110">返回值</span><span class="sxs-lookup"><span data-stu-id="52dd7-110">Return Value</span></span>

 `S_OK`\
 <span data-ttu-id="52dd7-111">`ppCordb` 引用实现 [ICorDebug 接口](icordebug-interface.md) 接口的有效对象。</span><span class="sxs-lookup"><span data-stu-id="52dd7-111">`ppCordb` references a valid object that implements the [ICorDebug interface](icordebug-interface.md) interface.</span></span>  
  
 `E_INVALIDARG`\
 <span data-ttu-id="52dd7-112">`szDebuggeeVersion` 或 `ppCordb` 为 null。</span><span class="sxs-lookup"><span data-stu-id="52dd7-112">Either `szDebuggeeVersion` or `ppCordb` is null.</span></span>  
  
 `CORDBG_E_DEBUG_COMPONENT_MISSING`\
 <span data-ttu-id="52dd7-113">找不到 CLR 调试所需的组件。</span><span class="sxs-lookup"><span data-stu-id="52dd7-113">A component that is necessary for CLR debugging cannot be located.</span></span> <span data-ttu-id="52dd7-114">在目标 CoreCLR.dll 所在的同一目录中找不到 _mscordbi.dll_ 或 _mscordaccore.dll_ 。</span><span class="sxs-lookup"><span data-stu-id="52dd7-114">Either _mscordbi.dll_ or _mscordaccore.dll_ was not found in the same directory as the target CoreCLR.dll.</span></span>  
  
 `CORDBG_E_INCOMPATIBLE_PROTOCOL`\
 <span data-ttu-id="52dd7-115">mscordbi.dll 或 mscordaccore.dll 与目标 CoreCLR.dll 版本不一致。</span><span class="sxs-lookup"><span data-stu-id="52dd7-115">Either mscordbi.dll or mscordaccore.dll is not the same version as the target CoreCLR.dll.</span></span>  
  
 <span data-ttu-id="52dd7-116">`E_FAIL` (或其他 `E_` 返回代码) </span><span class="sxs-lookup"><span data-stu-id="52dd7-116">`E_FAIL` (or other `E_` return codes)</span></span>\
 <span data-ttu-id="52dd7-117">无法返回 [ICorDebug 接口](icordebug-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="52dd7-117">Unable to return an [ICorDebug interface](icordebug-interface.md).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="52dd7-118">备注</span><span class="sxs-lookup"><span data-stu-id="52dd7-118">Remarks</span></span>

 <span data-ttu-id="52dd7-119">返回的接口提供用于附加到目标进程中的 CLR 和调试 CLR 正在运行的托管代码的功能。</span><span class="sxs-lookup"><span data-stu-id="52dd7-119">The interface that is returned provides the facilities for attaching to a CLR in a target process and debugging the managed code that the CLR is running.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="52dd7-120">要求</span><span class="sxs-lookup"><span data-stu-id="52dd7-120">Requirements</span></span>

 <span data-ttu-id="52dd7-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="52dd7-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="52dd7-122">**标头：** dbgshim.dll</span><span class="sxs-lookup"><span data-stu-id="52dd7-122">**Header:** dbgshim.h</span></span>  
  
 <span data-ttu-id="52dd7-123">**库：** dbgshim.dll</span><span class="sxs-lookup"><span data-stu-id="52dd7-123">**Library:** dbgshim.dll</span></span>  
  
 <span data-ttu-id="52dd7-124">**.NET Framework 版本：** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="52dd7-124">**.NET Framework Versions:** 3.5 SP1</span></span>
