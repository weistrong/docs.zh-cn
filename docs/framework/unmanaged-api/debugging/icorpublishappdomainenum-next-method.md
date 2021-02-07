---
description: 了解详细信息： ICorPublishAppDomainEnum：： Next 方法
title: ICorPublishAppDomainEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorPublishAppDomainEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishAppDomainEnum::Next
helpviewer_keywords:
- Next method, ICorPublishAppDomainEnum interface [.NET Framework debugging]
- ICorPublishAppDomainEnum::Next method [.NET Framework debugging]
ms.assetid: ad37cd10-0339-4d08-9b0e-4b3428bb4dc3
topic_type:
- apiref
ms.openlocfilehash: 8e8255aa2326c6f0678132f5735d6cdf504dcbd0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721718"
---
# <a name="icorpublishappdomainenumnext-method"></a><span data-ttu-id="2d0af-103">ICorPublishAppDomainEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="2d0af-103">ICorPublishAppDomainEnum::Next Method</span></span>

<span data-ttu-id="2d0af-104">从当前位置开始，获取进程中当前存在的指定数量的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="2d0af-104">Gets the specified number of application domains that currently exist in the process, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2d0af-105">语法</span><span class="sxs-lookup"><span data-stu-id="2d0af-105">Syntax</span></span>  
  
```cpp  
HRESULT Next (  
    [in] ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]
        ICorPublishAppDomain **objects,  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2d0af-106">参数</span><span class="sxs-lookup"><span data-stu-id="2d0af-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="2d0af-107">中要检索的元素的数目。</span><span class="sxs-lookup"><span data-stu-id="2d0af-107">[in] The number of elements to be retrieved.</span></span>  
  
 `objects`  
 <span data-ttu-id="2d0af-108">弄一个指针，指向检索到的 [ICorPublishAppDomain](icorpublishappdomain-interface.md) 对象的数组，其中每个对象都表示一个应用程序域。</span><span class="sxs-lookup"><span data-stu-id="2d0af-108">[out] A pointer to the array of retrieved [ICorPublishAppDomain](icorpublishappdomain-interface.md) objects, each of which represents an application domain.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="2d0af-109">弄一个指针，指向实际返回的应用程序域的数量。</span><span class="sxs-lookup"><span data-stu-id="2d0af-109">[out] Pointer to the number of application domains actually returned.</span></span> <span data-ttu-id="2d0af-110">如果为1，则此值可以为 null `celt` 。</span><span class="sxs-lookup"><span data-stu-id="2d0af-110">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2d0af-111">要求</span><span class="sxs-lookup"><span data-stu-id="2d0af-111">Requirements</span></span>  

 <span data-ttu-id="2d0af-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2d0af-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2d0af-113">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="2d0af-113">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="2d0af-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2d0af-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2d0af-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2d0af-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2d0af-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="2d0af-116">See also</span></span>

- [<span data-ttu-id="2d0af-117">ICorPublishAppDomainEnum 接口</span><span class="sxs-lookup"><span data-stu-id="2d0af-117">ICorPublishAppDomainEnum Interface</span></span>](icorpublishappdomainenum-interface.md)
