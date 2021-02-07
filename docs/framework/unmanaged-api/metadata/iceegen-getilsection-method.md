---
description: 了解详细信息： ICeeGen：： GetIlSection 方法
title: ICeeGen::GetIlSection 方法
ms.date: 03/30/2017
api_name:
- ICeeGen.GetIlSection
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GetIlSection
helpviewer_keywords:
- GetIlSection method [.NET Framework metadata]
- ICeeGen::GetIlSection method [.NET Framework metadata]
ms.assetid: 6f2db2ca-203f-4ac3-9530-208642ca385e
topic_type:
- apiref
ms.openlocfilehash: 44195ec55480279494620aed6db566f1c2308a6c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707002"
---
# <a name="iceegengetilsection-method"></a><span data-ttu-id="9c7f5-103">ICeeGen::GetIlSection 方法</span><span class="sxs-lookup"><span data-stu-id="9c7f5-103">ICeeGen::GetIlSection Method</span></span>

<span data-ttu-id="9c7f5-104">获取由指定句柄引用的中间语言代码库的部分。</span><span class="sxs-lookup"><span data-stu-id="9c7f5-104">Gets the section of the intermediate language code base referenced by the specified handle.</span></span>  
  
 <span data-ttu-id="9c7f5-105">此方法已过时，不应使用。</span><span class="sxs-lookup"><span data-stu-id="9c7f5-105">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9c7f5-106">语法</span><span class="sxs-lookup"><span data-stu-id="9c7f5-106">Syntax</span></span>  
  
```cpp  
HRESULT GetIlSection (  
    [in] HCEESECTION  *section  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9c7f5-107">参数</span><span class="sxs-lookup"><span data-stu-id="9c7f5-107">Parameters</span></span>  

 `section`  
 <span data-ttu-id="9c7f5-108">中要获取的节的句柄。</span><span class="sxs-lookup"><span data-stu-id="9c7f5-108">[in] The handle to the section to get.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9c7f5-109">要求</span><span class="sxs-lookup"><span data-stu-id="9c7f5-109">Requirements</span></span>  

 <span data-ttu-id="9c7f5-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9c7f5-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9c7f5-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="9c7f5-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="9c7f5-112">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="9c7f5-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="9c7f5-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9c7f5-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9c7f5-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="9c7f5-114">See also</span></span>

- [<span data-ttu-id="9c7f5-115">ICeeGen 接口</span><span class="sxs-lookup"><span data-stu-id="9c7f5-115">ICeeGen Interface</span></span>](iceegen-interface.md)
