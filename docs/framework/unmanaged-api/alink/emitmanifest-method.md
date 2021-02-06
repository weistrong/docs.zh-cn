---
description: 了解详细信息： EmitManifest 方法
title: EmitManifest 方法
ms.date: 03/30/2017
api_name:
- EmitManifest
- IALink.EmitManifest
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EmitManifest
helpviewer_keywords:
- EmitManifest method
ms.assetid: fdebc1f3-b62e-4d9e-b775-8ccaa8ecb250
topic_type:
- apiref
ms.openlocfilehash: 770631864c030c067feb0b02d2f00c36076aa44c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638270"
---
# <a name="emitmanifest-method"></a><span data-ttu-id="84069-103">EmitManifest 方法</span><span class="sxs-lookup"><span data-stu-id="84069-103">EmitManifest Method</span></span>

<span data-ttu-id="84069-104">发出最终清单。</span><span class="sxs-lookup"><span data-stu-id="84069-104">Emits the final manifest.</span></span> <span data-ttu-id="84069-105">导入所有其他文件并设置所有选项后，调用此方法。</span><span class="sxs-lookup"><span data-stu-id="84069-105">Call this method after importing all other files and setting all options.</span></span> <span data-ttu-id="84069-106">不要对未绑定的模块调用此方法。</span><span class="sxs-lookup"><span data-stu-id="84069-106">Do not call this method for unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="84069-107">语法</span><span class="sxs-lookup"><span data-stu-id="84069-107">Syntax</span></span>  
  
```cpp  
HRESULT EmitManifest(  
    mdAssembly   AssemblyID,  
    DWORD*       pdwReserveSize,  
    mdAssembly*  ptkManifest  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="84069-108">参数</span><span class="sxs-lookup"><span data-stu-id="84069-108">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="84069-109">程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="84069-109">ID of the assembly.</span></span>  
  
 `pdwReserveSize`  
 <span data-ttu-id="84069-110">接收程序集文件中要保留的大小，从 [StrongNameSignatureSize 函数](../strong-naming/strongnamesignaturesize-function.md)检索。</span><span class="sxs-lookup"><span data-stu-id="84069-110">Receives the size to reserve in the assembly file, retrieved from [StrongNameSignatureSize Function](../strong-naming/strongnamesignaturesize-function.md).</span></span>  
  
 `ptkManifest`  
 <span data-ttu-id="84069-111">可以选择接收程序集清单标记。</span><span class="sxs-lookup"><span data-stu-id="84069-111">Optionally receives the assembly manifest token.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="84069-112">返回值</span><span class="sxs-lookup"><span data-stu-id="84069-112">Return Value</span></span>  

 <span data-ttu-id="84069-113">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="84069-113">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="84069-114">要求</span><span class="sxs-lookup"><span data-stu-id="84069-114">Requirements</span></span>  

 <span data-ttu-id="84069-115">需要 alink。</span><span class="sxs-lookup"><span data-stu-id="84069-115">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="84069-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="84069-116">See also</span></span>

- [<span data-ttu-id="84069-117">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="84069-117">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="84069-118">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="84069-118">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="84069-119">ALink API</span><span class="sxs-lookup"><span data-stu-id="84069-119">ALink API</span></span>](index.md)
