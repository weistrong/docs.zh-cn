---
description: 了解详细信息： CreateAssemblyNameObject 函数
title: CreateAssemblyNameObject 函数
ms.date: 03/30/2017
api_name:
- CreateAssemblyNameObject
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- CreateAssemblyNameObject
helpviewer_keywords:
- CreateAssemblyNameObject function [.NET Framework fusion]
ms.assetid: 55c8b41e-fbe4-4ae0-aa29-68fbb2311691
topic_type:
- apiref
ms.openlocfilehash: 0eaa74bdb37a098ad58b81658229f8c04259b730
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761169"
---
# <a name="createassemblynameobject-function"></a><span data-ttu-id="d4312-103">CreateAssemblyNameObject 函数</span><span class="sxs-lookup"><span data-stu-id="d4312-103">CreateAssemblyNameObject Function</span></span>

<span data-ttu-id="d4312-104">获取一个接口指针，该指针指向表示具有指定名称的程序集的唯一标识的 [IAssemblyName](iassemblyname-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="d4312-104">Gets an interface pointer to an [IAssemblyName](iassemblyname-interface.md) instance that represents the unique identity of the assembly with the specified name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d4312-105">语法</span><span class="sxs-lookup"><span data-stu-id="d4312-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateAssemblyNameObject (  
    [out] LPASSEMBLYNAME  *ppAssemblyNameObj,  
    [in]  LPCWSTR         szAssemblyName,  
    [in]  DWORD           dwFlags,  
    [in]  LPVOID          pvReserved  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="d4312-106">参数</span><span class="sxs-lookup"><span data-stu-id="d4312-106">Parameters</span></span>  

 `ppAssemblyNameObj`  
 <span data-ttu-id="d4312-107">弄返回的 `IAssemblyName` 。</span><span class="sxs-lookup"><span data-stu-id="d4312-107">[out] The returned `IAssemblyName`.</span></span>  
  
 `szAssemblyName`  
 <span data-ttu-id="d4312-108">中要为其创建新实例的程序集的名称 `IAssemblyName` 。</span><span class="sxs-lookup"><span data-stu-id="d4312-108">[in] The name of the assembly for which to create the new `IAssemblyName` instance.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="d4312-109">中要传递给对象构造函数的标志。</span><span class="sxs-lookup"><span data-stu-id="d4312-109">[in] Flags to pass to the object constructor.</span></span>  
  
 `pvReserved`  
 <span data-ttu-id="d4312-110">中保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="d4312-110">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="d4312-111">`pvReserved` 必须为空引用。</span><span class="sxs-lookup"><span data-stu-id="d4312-111">`pvReserved` must be a null reference.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d4312-112">要求</span><span class="sxs-lookup"><span data-stu-id="d4312-112">Requirements</span></span>  

 <span data-ttu-id="d4312-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d4312-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d4312-114">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="d4312-114">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="d4312-115">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d4312-115">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d4312-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d4312-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d4312-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="d4312-117">See also</span></span>

- [<span data-ttu-id="d4312-118">IAssemblyName 接口</span><span class="sxs-lookup"><span data-stu-id="d4312-118">IAssemblyName Interface</span></span>](iassemblyname-interface.md)
- [<span data-ttu-id="d4312-119">合成全局静态函数</span><span class="sxs-lookup"><span data-stu-id="d4312-119">Fusion Global Static Functions</span></span>](fusion-global-static-functions.md)
