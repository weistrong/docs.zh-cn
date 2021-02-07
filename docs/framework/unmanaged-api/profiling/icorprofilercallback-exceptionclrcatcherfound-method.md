---
description: 了解详细信息： ICorProfilerCallback：： ExceptionCLRCatcherFound 方法
title: ICorProfilerCallback::ExceptionCLRCatcherFound 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionCLRCatcherFound
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionCLRCatcherFound
helpviewer_keywords:
- ICorProfilerCallback::ExceptionCLRCatcherFound method [.NET Framework profiling]
- ExceptionCLRCatcherFound method [.NET Framework profiling]
ms.assetid: 73fe8b4b-8f9a-4ba5-a10c-b26521396a66
topic_type:
- apiref
ms.openlocfilehash: 37027a00e488eed5681b1d99ada6332d59e6a632
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99706300"
---
# <a name="icorprofilercallbackexceptionclrcatcherfound-method"></a><span data-ttu-id="0a4be-103">ICorProfilerCallback::ExceptionCLRCatcherFound 方法</span><span class="sxs-lookup"><span data-stu-id="0a4be-103">ICorProfilerCallback::ExceptionCLRCatcherFound Method</span></span>

<span data-ttu-id="0a4be-104">当在 `catch` 公共语言运行时中找到异常的块时调用 (CLR) 本身。</span><span class="sxs-lookup"><span data-stu-id="0a4be-104">Called when a `catch` block for an exception is found inside the common language runtime (CLR) itself.</span></span> <span data-ttu-id="0a4be-105">此方法在 .NET Framework 版本2.0 中已过时。</span><span class="sxs-lookup"><span data-stu-id="0a4be-105">This method is obsolete in the .NET Framework version 2.0.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0a4be-106">语法</span><span class="sxs-lookup"><span data-stu-id="0a4be-106">Syntax</span></span>  
  
```cpp  
HRESULT ExceptionCLRCatcherFound();  
```  
  
## <a name="requirements"></a><span data-ttu-id="0a4be-107">要求</span><span class="sxs-lookup"><span data-stu-id="0a4be-107">Requirements</span></span>  

 <span data-ttu-id="0a4be-108">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0a4be-108">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0a4be-109">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="0a4be-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="0a4be-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0a4be-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0a4be-111">**.NET Framework 版本：** 1。0</span><span class="sxs-lookup"><span data-stu-id="0a4be-111">**.NET Framework Version:** 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0a4be-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="0a4be-112">See also</span></span>

- [<span data-ttu-id="0a4be-113">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="0a4be-113">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="0a4be-114">ExceptionCLRCatcherExecute 方法</span><span class="sxs-lookup"><span data-stu-id="0a4be-114">ExceptionCLRCatcherExecute Method</span></span>](icorprofilercallback-exceptionclrcatcherexecute-method.md)
