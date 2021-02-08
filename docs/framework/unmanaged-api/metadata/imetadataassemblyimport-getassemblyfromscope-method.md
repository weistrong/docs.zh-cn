---
description: 了解详细信息： IMetaDataAssemblyImport：： GetAssemblyFromScope 方法
title: IMetaDataAssemblyImport::GetAssemblyFromScope 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.GetAssemblyFromScope
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::GetAssemblyFromScope
helpviewer_keywords:
- IMetaDataAssemblyImport::GetAssemblyFromScope method [.NET Framework metadata]
- GetAssemblyFromScope method [.NET Framework metadata]
ms.assetid: 0b437f70-561d-48c7-abe0-0cb9ace10c08
topic_type:
- apiref
ms.openlocfilehash: 78e2862fca80dc06c37436f3d81db4b19c4ec332
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784153"
---
# <a name="imetadataassemblyimportgetassemblyfromscope-method"></a><span data-ttu-id="59118-103">IMetaDataAssemblyImport::GetAssemblyFromScope 方法</span><span class="sxs-lookup"><span data-stu-id="59118-103">IMetaDataAssemblyImport::GetAssemblyFromScope Method</span></span>

<span data-ttu-id="59118-104">获取指向当前范围内的程序集的指针。</span><span class="sxs-lookup"><span data-stu-id="59118-104">Gets a pointer to the assembly in the current scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="59118-105">语法</span><span class="sxs-lookup"><span data-stu-id="59118-105">Syntax</span></span>  
  
```cpp  
HRESULT GetAssemblyFromScope (  
    [out] mdAssembly  *ptkAssembly  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="59118-106">参数</span><span class="sxs-lookup"><span data-stu-id="59118-106">Parameters</span></span>  

 `ptkAssembly`  
 <span data-ttu-id="59118-107">弄指向用于标识程序集的检索到的标记的指针 `mdAssembly` 。</span><span class="sxs-lookup"><span data-stu-id="59118-107">[out] A pointer to the retrieved `mdAssembly` token that identifies the assembly.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="59118-108">要求</span><span class="sxs-lookup"><span data-stu-id="59118-108">Requirements</span></span>  

 <span data-ttu-id="59118-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="59118-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="59118-110">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="59118-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="59118-111">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="59118-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="59118-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="59118-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="59118-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="59118-113">See also</span></span>

- [<span data-ttu-id="59118-114">IMetaDataAssemblyImport 接口</span><span class="sxs-lookup"><span data-stu-id="59118-114">IMetaDataAssemblyImport Interface</span></span>](imetadataassemblyimport-interface.md)
