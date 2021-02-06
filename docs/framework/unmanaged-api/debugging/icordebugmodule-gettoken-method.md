---
description: 了解详细信息： ICorDebugModule：： GetToken 方法
title: ICorDebugModule::GetToken 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetToken
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetToken
helpviewer_keywords:
- ICorDebugModule::GetToken method [.NET Framework debugging]
- GetToken method, ICorDebugModule interface [.NET Framework debugging]
ms.assetid: f759f87a-18ae-4c1a-8300-29b803432d0a
topic_type:
- apiref
ms.openlocfilehash: fd1bc4bc397e7f81c77f2fe784c68dbaaceb2695
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99660162"
---
# <a name="icordebugmodulegettoken-method"></a><span data-ttu-id="c9f85-103">ICorDebugModule::GetToken 方法</span><span class="sxs-lookup"><span data-stu-id="c9f85-103">ICorDebugModule::GetToken Method</span></span>

<span data-ttu-id="c9f85-104">获取此模块的表项的标记。</span><span class="sxs-lookup"><span data-stu-id="c9f85-104">Gets the token for the table entry for this module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c9f85-105">语法</span><span class="sxs-lookup"><span data-stu-id="c9f85-105">Syntax</span></span>  
  
```cpp  
HRESULT GetToken(  
    [out] mdModule *pToken  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c9f85-106">参数</span><span class="sxs-lookup"><span data-stu-id="c9f85-106">Parameters</span></span>  

 `pToken`  
 <span data-ttu-id="c9f85-107">弄指向 `mdModule` 引用模块元数据的标记的指针。</span><span class="sxs-lookup"><span data-stu-id="c9f85-107">[out] A pointer to the `mdModule` token that references the module's metadata.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c9f85-108">备注</span><span class="sxs-lookup"><span data-stu-id="c9f85-108">Remarks</span></span>  

 <span data-ttu-id="c9f85-109">该令牌可以传递到 [IMetaDataImport](../metadata/imetadataimport-interface.md)、 [IMetaDataImport2](../metadata/imetadataimport2-interface.md)和 [IMetaDataAssemblyImport](../metadata/imetadataassemblyimport-interface.md) 元数据导入接口。</span><span class="sxs-lookup"><span data-stu-id="c9f85-109">The token can be passed to the [IMetaDataImport](../metadata/imetadataimport-interface.md), [IMetaDataImport2](../metadata/imetadataimport2-interface.md), and [IMetaDataAssemblyImport](../metadata/imetadataassemblyimport-interface.md) metadata import interfaces.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c9f85-110">要求</span><span class="sxs-lookup"><span data-stu-id="c9f85-110">Requirements</span></span>  

 <span data-ttu-id="c9f85-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c9f85-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c9f85-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c9f85-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c9f85-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c9f85-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c9f85-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c9f85-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c9f85-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="c9f85-115">See also</span></span>

- <span data-ttu-id="c9f85-116">Metadata </span><span class="sxs-lookup"><span data-stu-id="c9f85-116">[Metadata](../metadata/index.md)</span></span>
