---
description: 了解详细信息： EmitAssembly 方法
title: EmitAssembly 方法
ms.date: 03/30/2017
api_name:
- IALink2.EmitAssembly
- EmitAssembly
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EmitAssembly
helpviewer_keywords:
- EmitAssembly method
ms.assetid: 605ff39e-e5cc-4bff-8196-e8d68a9715b9
topic_type:
- apiref
ms.openlocfilehash: aada17d8df6435c5edfe6beb5db5ee13f887f253
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638335"
---
# <a name="emitassembly-method"></a><span data-ttu-id="2dae7-103">EmitAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="2dae7-103">EmitAssembly Method</span></span>

<span data-ttu-id="2dae7-104">创建程序集。</span><span class="sxs-lookup"><span data-stu-id="2dae7-104">Creates the assembly.</span></span> <span data-ttu-id="2dae7-105">除程序集文件以外的所有其他文件关闭后，调用此方法。</span><span class="sxs-lookup"><span data-stu-id="2dae7-105">Call this method after all other files are closed except for the assembly file.</span></span> <span data-ttu-id="2dae7-106">在生成未绑定的模块时不要调用此方法。</span><span class="sxs-lookup"><span data-stu-id="2dae7-106">Do not call this method when producing unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2dae7-107">语法</span><span class="sxs-lookup"><span data-stu-id="2dae7-107">Syntax</span></span>  
  
```cpp  
HRESULT EmitAssembly(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="2dae7-108">参数</span><span class="sxs-lookup"><span data-stu-id="2dae7-108">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="2dae7-109">程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="2dae7-109">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2dae7-110">返回值</span><span class="sxs-lookup"><span data-stu-id="2dae7-110">Return Value</span></span>  

 <span data-ttu-id="2dae7-111">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="2dae7-111">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2dae7-112">要求</span><span class="sxs-lookup"><span data-stu-id="2dae7-112">Requirements</span></span>  

 <span data-ttu-id="2dae7-113">需要 alink</span><span class="sxs-lookup"><span data-stu-id="2dae7-113">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2dae7-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="2dae7-114">See also</span></span>

- [<span data-ttu-id="2dae7-115">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="2dae7-115">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="2dae7-116">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="2dae7-116">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="2dae7-117">ALink API</span><span class="sxs-lookup"><span data-stu-id="2dae7-117">ALink API</span></span>](index.md)
