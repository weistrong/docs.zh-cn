---
description: 了解详细信息： GetResolutionScope 方法
title: GetResolutionScope 方法
ms.date: 03/30/2017
api_name:
- IALink.GetResolutionScope
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetResolutionScope
helpviewer_keywords:
- GetResolutionScope method
ms.assetid: 5b48ca60-dacd-44b2-9979-4a5122f00812
topic_type:
- apiref
ms.openlocfilehash: add8ccb1ef6eb0f4b688dcf80563e9280099120d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99718390"
---
# <a name="getresolutionscope-method"></a><span data-ttu-id="3271f-103">GetResolutionScope 方法</span><span class="sxs-lookup"><span data-stu-id="3271f-103">GetResolutionScope Method</span></span>

<span data-ttu-id="3271f-104">检索给定类型的作用域。</span><span class="sxs-lookup"><span data-stu-id="3271f-104">Retrieves the scope of a given type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3271f-105">语法</span><span class="sxs-lookup"><span data-stu-id="3271f-105">Syntax</span></span>  
  
```cpp  
HRESULT GetResolutionScope(  
    mdAssembly  AssemblyID,  
    mdToken     FileToken,  
    mdToken     TargetFile,  
    mdToken*    pScope  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="3271f-106">参数</span><span class="sxs-lookup"><span data-stu-id="3271f-106">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="3271f-107">程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="3271f-107">ID of the assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="3271f-108">需要引用的文件。</span><span class="sxs-lookup"><span data-stu-id="3271f-108">File that is in need of a reference.</span></span>  
  
 `TargetFile`  
 <span data-ttu-id="3271f-109">在中定义类型的文件的标记，通常用 [ImportFile 方法](importfile-method.md)进行检索。</span><span class="sxs-lookup"><span data-stu-id="3271f-109">Token of file that type is defined in, usually retrieved with [ImportFile Method](importfile-method.md).</span></span>  
  
 `pScope`  
 <span data-ttu-id="3271f-110">接收程序集或模块引用。</span><span class="sxs-lookup"><span data-stu-id="3271f-110">Receives the assembly or module reference.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3271f-111">返回值</span><span class="sxs-lookup"><span data-stu-id="3271f-111">Return Value</span></span>  

 <span data-ttu-id="3271f-112">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="3271f-112">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3271f-113">要求</span><span class="sxs-lookup"><span data-stu-id="3271f-113">Requirements</span></span>  

 <span data-ttu-id="3271f-114">需要 alink。</span><span class="sxs-lookup"><span data-stu-id="3271f-114">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3271f-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="3271f-115">See also</span></span>

- [<span data-ttu-id="3271f-116">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="3271f-116">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="3271f-117">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="3271f-117">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="3271f-118">ALink API</span><span class="sxs-lookup"><span data-stu-id="3271f-118">ALink API</span></span>](index.md)
