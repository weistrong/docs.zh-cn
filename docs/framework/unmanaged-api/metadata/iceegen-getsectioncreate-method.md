---
description: 了解详细信息： ICeeGen：： GetSectionCreate 方法
title: ICeeGen::GetSectionCreate 方法
ms.date: 03/30/2017
api_name:
- ICeeGen.GetSectionCreate
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GetSectionCreate
helpviewer_keywords:
- ICeeGen::GetSectionCreate method [.NET Framework metadata]
- GetSectionCreate method [.NET Framework metadata]
ms.assetid: 154b2460-59ce-4874-a9f2-1b3353486ac5
topic_type:
- apiref
ms.openlocfilehash: 2839d11c927dbf573f213d3ebaa9e6e6d8d5015d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99706859"
---
# <a name="iceegengetsectioncreate-method"></a><span data-ttu-id="cec63-103">ICeeGen::GetSectionCreate 方法</span><span class="sxs-lookup"><span data-stu-id="cec63-103">ICeeGen::GetSectionCreate Method</span></span>

<span data-ttu-id="cec63-104">使用指定的名称和标志值生成并获取代码部分。</span><span class="sxs-lookup"><span data-stu-id="cec63-104">Generates and gets a code section using the specified name and flag values.</span></span>  
  
 <span data-ttu-id="cec63-105">此方法已过时，不应使用。</span><span class="sxs-lookup"><span data-stu-id="cec63-105">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cec63-106">语法</span><span class="sxs-lookup"><span data-stu-id="cec63-106">Syntax</span></span>  
  
```cpp  
HRESULT GetSectionCreate (  
    [in]  const char     *name,  
    [in]  DWORD          flags,  
    [out] HCEESECTION    *section  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cec63-107">参数</span><span class="sxs-lookup"><span data-stu-id="cec63-107">Parameters</span></span>  

 `name`  
 <span data-ttu-id="cec63-108">中指向字符串的指针，该字符串指定要创建的节的名称。</span><span class="sxs-lookup"><span data-stu-id="cec63-108">[in] A pointer to a string that specifies the name of the section to be created.</span></span>  
  
 `flags`  
 <span data-ttu-id="cec63-109">中指定选项的标志。</span><span class="sxs-lookup"><span data-stu-id="cec63-109">[in] Flags that specify options.</span></span>  
  
 `section`  
 <span data-ttu-id="cec63-110">弄指向新创建的代码部分的指针。</span><span class="sxs-lookup"><span data-stu-id="cec63-110">[out] A pointer to the newly created code section.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cec63-111">备注</span><span class="sxs-lookup"><span data-stu-id="cec63-111">Remarks</span></span>  

 <span data-ttu-id="cec63-112">`GetSectionCreate`仅当有特殊部分的要求不是由其他方法处理时才调用。</span><span class="sxs-lookup"><span data-stu-id="cec63-112">Call `GetSectionCreate` only if you have special section requirements that are not handled by other methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cec63-113">要求</span><span class="sxs-lookup"><span data-stu-id="cec63-113">Requirements</span></span>  

 <span data-ttu-id="cec63-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cec63-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cec63-115">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="cec63-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="cec63-116">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="cec63-116">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="cec63-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cec63-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cec63-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="cec63-118">See also</span></span>

- [<span data-ttu-id="cec63-119">ICeeGen 接口</span><span class="sxs-lookup"><span data-stu-id="cec63-119">ICeeGen Interface</span></span>](iceegen-interface.md)
