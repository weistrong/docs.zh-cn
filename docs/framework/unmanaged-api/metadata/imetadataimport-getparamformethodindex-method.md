---
description: 了解详细信息： IMetaDataImport：： GetParamForMethodIndex 方法
title: IMetaDataImport::GetParamForMethodIndex 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetParamForMethodIndex
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetParamForMethodIndex
helpviewer_keywords:
- IMetaDataImport::GetParamForMethodIndex method [.NET Framework metadata]
- GetParamForMethodIndex method [.NET Framework metadata]
ms.assetid: ec3bfa95-1920-4511-932e-3ff23d76fcb8
topic_type:
- apiref
ms.openlocfilehash: d84b26f1239e548b6cf96d1e6b38791eb6ecddff
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99728140"
---
# <a name="imetadataimportgetparamformethodindex-method"></a><span data-ttu-id="f9e3e-103">IMetaDataImport::GetParamForMethodIndex 方法</span><span class="sxs-lookup"><span data-stu-id="f9e3e-103">IMetaDataImport::GetParamForMethodIndex Method</span></span>

<span data-ttu-id="f9e3e-104">获取表示指定的 MethodDef 标记所表示的方法的指定参数的令牌。</span><span class="sxs-lookup"><span data-stu-id="f9e3e-104">Gets the token that represents a specified parameter of the method represented by the specified MethodDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f9e3e-105">语法</span><span class="sxs-lookup"><span data-stu-id="f9e3e-105">Syntax</span></span>  
  
```cpp  
HRESULT GetParamForMethodIndex (  
   [in]  mdMethodDef      md,  
   [in]  ULONG            ulParamSeq,  
   [out] mdParamDef       *ppd  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f9e3e-106">参数</span><span class="sxs-lookup"><span data-stu-id="f9e3e-106">Parameters</span></span>  

 `md`  
 <span data-ttu-id="f9e3e-107">中一个标记，表示要为其返回参数标记的方法。</span><span class="sxs-lookup"><span data-stu-id="f9e3e-107">[in] A token that represents the method to return the parameter token for.</span></span>  
  
 `ulParamSeq`  
 <span data-ttu-id="f9e3e-108">中参数列表中出现请求的参数的序号位置。</span><span class="sxs-lookup"><span data-stu-id="f9e3e-108">[in] The ordinal position in the parameter list where the requested parameter occurs.</span></span> <span data-ttu-id="f9e3e-109">参数从1开始编号，方法的返回值位于位置零。</span><span class="sxs-lookup"><span data-stu-id="f9e3e-109">Parameters are numbered starting from one, with the method's return value in position zero.</span></span>  
  
 `ppd`  
 <span data-ttu-id="f9e3e-110">弄一个指针，指向表示请求的参数的 ParamDef 标记。</span><span class="sxs-lookup"><span data-stu-id="f9e3e-110">[out] A pointer to a ParamDef token that represents the requested parameter.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f9e3e-111">要求</span><span class="sxs-lookup"><span data-stu-id="f9e3e-111">Requirements</span></span>  

 <span data-ttu-id="f9e3e-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f9e3e-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f9e3e-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="f9e3e-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f9e3e-114">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f9e3e-114">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="f9e3e-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f9e3e-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f9e3e-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="f9e3e-116">See also</span></span>

- [<span data-ttu-id="f9e3e-117">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="f9e3e-117">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="f9e3e-118">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="f9e3e-118">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
