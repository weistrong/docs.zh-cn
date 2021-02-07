---
description: 了解详细信息： ICeeGen：： EmitString 方法
title: ICeeGen::EmitString 方法
ms.date: 03/30/2017
api_name:
- ICeeGen.EmitString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::EmitString
helpviewer_keywords:
- EmitString method [.NET Framework metadata]
- ICeeGen::EmitString method [.NET Framework metadata]
ms.assetid: ad2710a7-edb8-4493-8619-3fce235e3334
topic_type:
- apiref
ms.openlocfilehash: fca388d044603f932bf90a176cada6e830284702
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707106"
---
# <a name="iceegenemitstring-method"></a><span data-ttu-id="108a4-103">ICeeGen::EmitString 方法</span><span class="sxs-lookup"><span data-stu-id="108a4-103">ICeeGen::EmitString Method</span></span>

<span data-ttu-id="108a4-104">向基本代码发出指定的字符串。</span><span class="sxs-lookup"><span data-stu-id="108a4-104">Emits the specified string into the code base.</span></span>  
  
 <span data-ttu-id="108a4-105">此方法已过时，不应使用。</span><span class="sxs-lookup"><span data-stu-id="108a4-105">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="108a4-106">语法</span><span class="sxs-lookup"><span data-stu-id="108a4-106">Syntax</span></span>  
  
```cpp  
HRESULT EmitString (  
    [in]  LPWSTR    lpString,  
    [out] ULONG     *RVA  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="108a4-107">参数</span><span class="sxs-lookup"><span data-stu-id="108a4-107">Parameters</span></span>  

 `lpString`  
 <span data-ttu-id="108a4-108">中要发出的字符串。</span><span class="sxs-lookup"><span data-stu-id="108a4-108">[in] The string to emit.</span></span>  
  
 `RVA`  
 <span data-ttu-id="108a4-109">弄发出的字符串的相对虚拟地址。</span><span class="sxs-lookup"><span data-stu-id="108a4-109">[out] The relative virtual address of the emitted string.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="108a4-110">要求</span><span class="sxs-lookup"><span data-stu-id="108a4-110">Requirements</span></span>  

 <span data-ttu-id="108a4-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="108a4-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="108a4-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="108a4-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="108a4-113">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="108a4-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="108a4-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="108a4-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="108a4-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="108a4-115">See also</span></span>

- [<span data-ttu-id="108a4-116">ICeeGen 接口</span><span class="sxs-lookup"><span data-stu-id="108a4-116">ICeeGen Interface</span></span>](iceegen-interface.md)
