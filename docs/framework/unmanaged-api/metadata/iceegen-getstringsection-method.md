---
description: 了解详细信息： ICeeGen：： GetStringSection 方法
title: ICeeGen::GetStringSection 方法
ms.date: 03/30/2017
api_name:
- ICeeGen.GetStringSection
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GetStringSection
helpviewer_keywords:
- ICeeGen::GetStringSection method [.NET Framework metadata]
- GetStringSection method [.NET Framework metadata]
ms.assetid: a2267d39-69d1-4de1-bf37-f752cafacc71
topic_type:
- apiref
ms.openlocfilehash: ef4b4bb502e1099b9b3bcdbd494d03df0858aa6b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721027"
---
# <a name="iceegengetstringsection-method"></a><span data-ttu-id="21765-103">ICeeGen::GetStringSection 方法</span><span class="sxs-lookup"><span data-stu-id="21765-103">ICeeGen::GetStringSection Method</span></span>

<span data-ttu-id="21765-104">获取由指定句柄引用的代码段的字符串表示形式。</span><span class="sxs-lookup"><span data-stu-id="21765-104">Gets a string representation of the code section referenced by the specified handle.</span></span>  
  
 <span data-ttu-id="21765-105">此方法已过时，不应使用。</span><span class="sxs-lookup"><span data-stu-id="21765-105">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="21765-106">语法</span><span class="sxs-lookup"><span data-stu-id="21765-106">Syntax</span></span>  
  
```cpp  
HRESULT GetStringSection (  
    [in, out] HCEESECTION     *section  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="21765-107">参数</span><span class="sxs-lookup"><span data-stu-id="21765-107">Parameters</span></span>  

 `section`  
 <span data-ttu-id="21765-108">[in，out]代码部分的句柄。</span><span class="sxs-lookup"><span data-stu-id="21765-108">[in, out] The handle to the code section.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="21765-109">要求</span><span class="sxs-lookup"><span data-stu-id="21765-109">Requirements</span></span>  

 <span data-ttu-id="21765-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="21765-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="21765-111">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="21765-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="21765-112">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="21765-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="21765-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="21765-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="21765-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="21765-114">See also</span></span>

- [<span data-ttu-id="21765-115">ICeeGen 接口</span><span class="sxs-lookup"><span data-stu-id="21765-115">ICeeGen Interface</span></span>](iceegen-interface.md)
