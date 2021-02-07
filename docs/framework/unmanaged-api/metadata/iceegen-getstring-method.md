---
description: 了解详细信息： ICeeGen：： GetString 方法
title: ICeeGen::GetString 方法
ms.date: 03/30/2017
api_name:
- ICeeGen.GetString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GetString
helpviewer_keywords:
- ICeeGen::GetString method [.NET Framework metadata]
- GetString method, ICeeGen interface [.NET Framework metadata]
ms.assetid: 7cc22562-128c-440a-9147-55ff20f173d7
topic_type:
- apiref
ms.openlocfilehash: 227b4badff3265fc22f1c76301ba03e58fea34c6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99706885"
---
# <a name="iceegengetstring-method"></a><span data-ttu-id="1bfeb-103">ICeeGen::GetString 方法</span><span class="sxs-lookup"><span data-stu-id="1bfeb-103">ICeeGen::GetString Method</span></span>

<span data-ttu-id="1bfeb-104">获取存储在指定的相对虚拟地址的字符串。</span><span class="sxs-lookup"><span data-stu-id="1bfeb-104">Gets the string stored at the specified relative virtual address.</span></span>  
  
 <span data-ttu-id="1bfeb-105">此方法已过时，不应使用。</span><span class="sxs-lookup"><span data-stu-id="1bfeb-105">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1bfeb-106">语法</span><span class="sxs-lookup"><span data-stu-id="1bfeb-106">Syntax</span></span>  
  
```cpp  
HRESULT GetString (  
    [in]  ULONG      RVA,
    [out] LPWSTR     *lpString  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1bfeb-107">参数</span><span class="sxs-lookup"><span data-stu-id="1bfeb-107">Parameters</span></span>  

 `RVA`  
 <span data-ttu-id="1bfeb-108">中要返回的字符串的相对虚拟地址。</span><span class="sxs-lookup"><span data-stu-id="1bfeb-108">[in] The relative virtual address of the string to return.</span></span>  
  
 `lpString`  
 <span data-ttu-id="1bfeb-109">弄返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="1bfeb-109">[out] The returned string.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1bfeb-110">要求</span><span class="sxs-lookup"><span data-stu-id="1bfeb-110">Requirements</span></span>  

 <span data-ttu-id="1bfeb-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1bfeb-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1bfeb-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="1bfeb-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="1bfeb-113">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="1bfeb-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="1bfeb-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1bfeb-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1bfeb-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="1bfeb-115">See also</span></span>

- [<span data-ttu-id="1bfeb-116">ICeeGen 接口</span><span class="sxs-lookup"><span data-stu-id="1bfeb-116">ICeeGen Interface</span></span>](iceegen-interface.md)
