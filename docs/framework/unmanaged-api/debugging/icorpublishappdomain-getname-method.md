---
description: 了解详细信息： ICorPublishAppDomain：： GetName 方法
title: ICorPublishAppDomain::GetName 方法
ms.date: 03/30/2017
api_name:
- ICorPublishAppDomain.GetName
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishAppDomain::GetName
helpviewer_keywords:
- GetName method, ICorPublishAppDomain interface [.NET Framework debugging]
- ICorPublishAppDomain::GetName method [.NET Framework debugging]
ms.assetid: 6ef8ac9b-9803-4b65-8b13-25f3e0b1bc6b
topic_type:
- apiref
ms.openlocfilehash: 05b1b14f7e0db371b29059ec3d44333ac40428e9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721796"
---
# <a name="icorpublishappdomaingetname-method"></a><span data-ttu-id="dfaaa-103">ICorPublishAppDomain::GetName 方法</span><span class="sxs-lookup"><span data-stu-id="dfaaa-103">ICorPublishAppDomain::GetName Method</span></span>

<span data-ttu-id="dfaaa-104">获取此 [ICorPublishAppDomain](icorpublishappdomain-interface.md)所表示的应用程序域的名称。</span><span class="sxs-lookup"><span data-stu-id="dfaaa-104">Gets the name of the application domain that is represented by this [ICorPublishAppDomain](icorpublishappdomain-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dfaaa-105">语法</span><span class="sxs-lookup"><span data-stu-id="dfaaa-105">Syntax</span></span>  
  
```cpp  
HRESULT GetName (  
    [in]  ULONG32   cchName,
    [out] ULONG32   *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]
        WCHAR       *szName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dfaaa-106">参数</span><span class="sxs-lookup"><span data-stu-id="dfaaa-106">Parameters</span></span>  

 `cchName`  
 <span data-ttu-id="dfaaa-107">[in] `szName` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="dfaaa-107">[in] The size of the `szName` array.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="dfaaa-108">弄一个指针，它指向数组中返回的宽字符数，包括 null 字符 `szName` 。</span><span class="sxs-lookup"><span data-stu-id="dfaaa-108">[out] A pointer to the number of wide characters, including the null character, returned in the `szName` array.</span></span>  
  
 `szName`  
 <span data-ttu-id="dfaaa-109">弄要在其中存储名称的数组。</span><span class="sxs-lookup"><span data-stu-id="dfaaa-109">[out] An array in which to store the name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dfaaa-110">备注</span><span class="sxs-lookup"><span data-stu-id="dfaaa-110">Remarks</span></span>  

 <span data-ttu-id="dfaaa-111">如果 `szName` 为非 null，则该 `GetName` 方法将最多复制 `cchName` (个字符，包括 null 结束符) 入 `szName` 。</span><span class="sxs-lookup"><span data-stu-id="dfaaa-111">If `szName` is non-null, the `GetName` method copies up to `cchName` characters (including the null terminator) into `szName`.</span></span> <span data-ttu-id="dfaaa-112">如果在中返回非 null，则 `pcchName` 名称中的实际字符数 (包括 null 结束符) 存储在 `szName` 数组中。</span><span class="sxs-lookup"><span data-stu-id="dfaaa-112">If a non-null is returned in `pcchName`, the actual number of characters in the name (including the null terminator) is stored in the `szName` array.</span></span>  
  
 <span data-ttu-id="dfaaa-113">`GetName`无论复制了多少个字符，该方法都将返回 S_OK HRESULT。</span><span class="sxs-lookup"><span data-stu-id="dfaaa-113">The `GetName` method returns an S_OK HRESULT regardless of how many characters were copied.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dfaaa-114">要求</span><span class="sxs-lookup"><span data-stu-id="dfaaa-114">Requirements</span></span>  

 <span data-ttu-id="dfaaa-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="dfaaa-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dfaaa-116">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="dfaaa-116">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="dfaaa-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dfaaa-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="dfaaa-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dfaaa-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dfaaa-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="dfaaa-119">See also</span></span>

- [<span data-ttu-id="dfaaa-120">ICorPublishAppDomain 接口</span><span class="sxs-lookup"><span data-stu-id="dfaaa-120">ICorPublishAppDomain Interface</span></span>](icorpublishappdomain-interface.md)
