---
description: 了解详细信息： ICLRDebuggingLibraryProvider 接口
title: ICLRDebuggingLibraryProvider 接口
ms.date: 03/30/2017
api_name:
- ICLRDebuggingLibraryProvider
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDebuggingLibraryProvider
helpviewer_keywords:
- ICLRDebuggingLibraryProvider interface [.NET Framework debugging]
ms.assetid: 67739617-6add-41a9-9de5-a3200c3109ce
topic_type:
- apiref
ms.openlocfilehash: 8aaec87e97d45c8b7b6f87aee64154ea3f48b133
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99723278"
---
# <a name="iclrdebugginglibraryprovider-interface"></a><span data-ttu-id="d3da5-103">ICLRDebuggingLibraryProvider 接口</span><span class="sxs-lookup"><span data-stu-id="d3da5-103">ICLRDebuggingLibraryProvider Interface</span></span>

<span data-ttu-id="d3da5-104">包括 [ProvideLibrary 方法](iclrdebugginglibraryprovider-providelibrary-method.md) 方法，该方法可获取一个库提供程序回调接口，该接口允许根据需要定位和加载特定于公共语言运行时版本的调试库。</span><span class="sxs-lookup"><span data-stu-id="d3da5-104">Includes the [ProvideLibrary Method](iclrdebugginglibraryprovider-providelibrary-method.md) method, which gets a library provider callback interface that allows common language runtime version-specific debugging libraries to be located and loaded on demand.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d3da5-105">方法</span><span class="sxs-lookup"><span data-stu-id="d3da5-105">Methods</span></span>  
  
|<span data-ttu-id="d3da5-106">方法</span><span class="sxs-lookup"><span data-stu-id="d3da5-106">Method</span></span>|<span data-ttu-id="d3da5-107">说明</span><span class="sxs-lookup"><span data-stu-id="d3da5-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d3da5-108">ProvideLibrary 方法</span><span class="sxs-lookup"><span data-stu-id="d3da5-108">ProvideLibrary Method</span></span>](iclrdebugginglibraryprovider-providelibrary-method.md)|<span data-ttu-id="d3da5-109">允许调试器提供可用于加载调试库的模块的句柄。</span><span class="sxs-lookup"><span data-stu-id="d3da5-109">Allows the debugger to provide a handle to a module which can be used to load a debug library.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d3da5-110">要求</span><span class="sxs-lookup"><span data-stu-id="d3da5-110">Requirements</span></span>  

 <span data-ttu-id="d3da5-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d3da5-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d3da5-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d3da5-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d3da5-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d3da5-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d3da5-114">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d3da5-114">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d3da5-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="d3da5-115">See also</span></span>

- [<span data-ttu-id="d3da5-116">调试接口</span><span class="sxs-lookup"><span data-stu-id="d3da5-116">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="d3da5-117">调试</span><span class="sxs-lookup"><span data-stu-id="d3da5-117">Debugging</span></span>](index.md)
