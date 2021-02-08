---
description: 了解详细信息： ICeeGen：： TruncateSection 方法
title: ICeeGen::TruncateSection 方法
ms.date: 03/30/2017
api_name:
- ICeeGen.TruncateSection
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::TruncateSection
helpviewer_keywords:
- TruncateSection method [.NET Framework metadata]
- ICeeGen::TruncateSection method [.NET Framework metadata]
ms.assetid: 0451d752-1e5c-4c9a-8bad-6cd35b7ba3df
topic_type:
- apiref
ms.openlocfilehash: 074c7d7b4222b5b22f1d9b79169d531cd5544b1e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784205"
---
# <a name="iceegentruncatesection-method"></a><span data-ttu-id="61ba8-103">ICeeGen::TruncateSection 方法</span><span class="sxs-lookup"><span data-stu-id="61ba8-103">ICeeGen::TruncateSection Method</span></span>

<span data-ttu-id="61ba8-104">按指定长度截断指定的代码段。</span><span class="sxs-lookup"><span data-stu-id="61ba8-104">Truncates the specified code section by the specified length.</span></span>  
  
 <span data-ttu-id="61ba8-105">此方法已过时，不应使用。</span><span class="sxs-lookup"><span data-stu-id="61ba8-105">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="61ba8-106">语法</span><span class="sxs-lookup"><span data-stu-id="61ba8-106">Syntax</span></span>  
  
```cpp  
HRESULT TruncateSection (  
    [in]  HCEESECTION     section,  
    [in]  ULONG           len  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="61ba8-107">参数</span><span class="sxs-lookup"><span data-stu-id="61ba8-107">Parameters</span></span>  

 `section`  
 <span data-ttu-id="61ba8-108">中要截断的部分。</span><span class="sxs-lookup"><span data-stu-id="61ba8-108">[in] The section to truncate.</span></span>  
  
 `len`  
 <span data-ttu-id="61ba8-109">中用于截断部分的长度（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="61ba8-109">[in] The length, in bytes, by which to truncate the section.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="61ba8-110">备注</span><span class="sxs-lookup"><span data-stu-id="61ba8-110">Remarks</span></span>  

 <span data-ttu-id="61ba8-111">`TruncateSection`仅当有特殊部分的要求不是由其他方法处理时才调用。</span><span class="sxs-lookup"><span data-stu-id="61ba8-111">Call `TruncateSection` only if you have special section requirements that are not handled by other methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="61ba8-112">要求</span><span class="sxs-lookup"><span data-stu-id="61ba8-112">Requirements</span></span>  

 <span data-ttu-id="61ba8-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="61ba8-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="61ba8-114">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="61ba8-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="61ba8-115">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="61ba8-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="61ba8-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="61ba8-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="61ba8-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="61ba8-117">See also</span></span>

- [<span data-ttu-id="61ba8-118">ICeeGen 接口</span><span class="sxs-lookup"><span data-stu-id="61ba8-118">ICeeGen Interface</span></span>](iceegen-interface.md)
