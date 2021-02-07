---
description: 了解详细信息： CreateInstallReferenceEnum 函数
title: CreateInstallReferenceEnum 函数
ms.date: 03/30/2017
api_name:
- CreateInstallReferenceEnum
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- CreateInstallReference
helpviewer_keywords:
- CreateInstallReference function [.NET Framework fusion]
ms.assetid: 80dbbbf8-54fc-4894-b74a-0179d3201083
topic_type:
- apiref
ms.openlocfilehash: cc7551707cb46bcf0c475a0095684dbc790836e3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761130"
---
# <a name="createinstallreferenceenum-function"></a><span data-ttu-id="e23ce-103">CreateInstallReferenceEnum 函数</span><span class="sxs-lookup"><span data-stu-id="e23ce-103">CreateInstallReferenceEnum Function</span></span>

<span data-ttu-id="e23ce-104">获取一个指针，该指针指向表示应用程序对指定程序集的引用列表的 [IInstallReferenceEnum](iinstallreferenceenum-interface.md) 实例。</span><span class="sxs-lookup"><span data-stu-id="e23ce-104">Gets a pointer to an [IInstallReferenceEnum](iinstallreferenceenum-interface.md) instance that represents a list of an application's references to the specified assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e23ce-105">语法</span><span class="sxs-lookup"><span data-stu-id="e23ce-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateInstallReferenceEnum (  
    [out] IInstallReferenceEnum **ppRefEnum,  
    [in]  IAssemblyName         *pName,  
    [in]  DWORD                 dwFlags,  
    [in]  LPVOID                pvReserved  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="e23ce-106">参数</span><span class="sxs-lookup"><span data-stu-id="e23ce-106">Parameters</span></span>  

 `ppRefEnum`  
 <span data-ttu-id="e23ce-107">弄返回的 `IInstallReferenceEnum` 指针。</span><span class="sxs-lookup"><span data-stu-id="e23ce-107">[out] The returned `IInstallReferenceEnum` pointer.</span></span>  
  
 `pName`  
 <span data-ttu-id="e23ce-108">中标识要枚举其引用的程序集的 [IAssemblyName](iassemblyname-interface.md) 。</span><span class="sxs-lookup"><span data-stu-id="e23ce-108">[in] The [IAssemblyName](iassemblyname-interface.md) that identifies the assembly for which to enumerate references.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="e23ce-109">中影响枚举器行为的标志。</span><span class="sxs-lookup"><span data-stu-id="e23ce-109">[in] Flags that influence the enumerator's behavior.</span></span>  
  
 `pvReserved`  
 <span data-ttu-id="e23ce-110">中保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="e23ce-110">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="e23ce-111">`pvReserved` 必须为空引用。</span><span class="sxs-lookup"><span data-stu-id="e23ce-111">`pvReserved` must be a null reference.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e23ce-112">要求</span><span class="sxs-lookup"><span data-stu-id="e23ce-112">Requirements</span></span>  

 <span data-ttu-id="e23ce-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e23ce-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e23ce-114">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="e23ce-114">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="e23ce-115">**库：** Fusion.dll 和 Mscorwks.dll。</span><span class="sxs-lookup"><span data-stu-id="e23ce-115">**Library:** Fusion.dll and Mscorwks.dll.</span></span> <span data-ttu-id="e23ce-116">使用 Fusion.dll 而不是 Mscorwks.dll 确保以正确的 .NET Framework 版本为目标。</span><span class="sxs-lookup"><span data-stu-id="e23ce-116">Use Fusion.dll instead of Mscorwks.dll to ensure that you target the correct version of the .NET Framework.</span></span>  
  
 <span data-ttu-id="e23ce-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e23ce-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e23ce-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="e23ce-118">See also</span></span>

- [<span data-ttu-id="e23ce-119">IInstallReferenceEnum 接口</span><span class="sxs-lookup"><span data-stu-id="e23ce-119">IInstallReferenceEnum Interface</span></span>](iinstallreferenceenum-interface.md)
- [<span data-ttu-id="e23ce-120">IAssemblyName 接口</span><span class="sxs-lookup"><span data-stu-id="e23ce-120">IAssemblyName Interface</span></span>](iassemblyname-interface.md)
- [<span data-ttu-id="e23ce-121">合成全局静态函数</span><span class="sxs-lookup"><span data-stu-id="e23ce-121">Fusion Global Static Functions</span></span>](fusion-global-static-functions.md)
