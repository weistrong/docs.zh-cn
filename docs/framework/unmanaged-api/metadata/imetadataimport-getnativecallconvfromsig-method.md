---
description: 了解详细信息： IMetaDataImport：： GetNativeCallConvFromSig 方法
title: IMetaDataImport::GetNativeCallConvFromSig 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetNativeCallConvFromSig
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetNativeCallConvFromSig
helpviewer_keywords:
- GetNativeCallConvFromSig method [.NET Framework metadata]
- IMetaDataImport::GetNativeCallConvFromSig method [.NET Framework metadata]
ms.assetid: 50e04026-4d4a-47d9-96c1-f4677d6d938b
topic_type:
- apiref
ms.openlocfilehash: 2fb5c347098f860f9ad32eab20c8b5bd6278f838
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99677567"
---
# <a name="imetadataimportgetnativecallconvfromsig-method"></a><span data-ttu-id="39778-103">IMetaDataImport::GetNativeCallConvFromSig 方法</span><span class="sxs-lookup"><span data-stu-id="39778-103">IMetaDataImport::GetNativeCallConvFromSig Method</span></span>

<span data-ttu-id="39778-104">获取指定的签名指针所表示的方法的本机调用约定。</span><span class="sxs-lookup"><span data-stu-id="39778-104">Gets the native calling convention for the method that is represented by the specified signature pointer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="39778-105">语法</span><span class="sxs-lookup"><span data-stu-id="39778-105">Syntax</span></span>  
  
```cpp  
HRESULT GetNativeCallConvFromSig (  
   [in]  void const  *pvSig,  
   [in]  ULONG       cbSig,  
   [out] ULONG       *pCallConv  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="39778-106">参数</span><span class="sxs-lookup"><span data-stu-id="39778-106">Parameters</span></span>  

 `pvSig`  
 <span data-ttu-id="39778-107">中指向要为其返回调用约定的方法的元数据签名的指针。</span><span class="sxs-lookup"><span data-stu-id="39778-107">[in] A pointer to the metadata signature of the method to return the calling convention for.</span></span>  
  
 `cbSig`  
 <span data-ttu-id="39778-108">中的大小（以字节为单位） `pvSig` 。</span><span class="sxs-lookup"><span data-stu-id="39778-108">[in] The size in bytes of `pvSig`.</span></span>  
  
 `pCallConv`  
 <span data-ttu-id="39778-109">弄指向本机调用约定的指针。</span><span class="sxs-lookup"><span data-stu-id="39778-109">[out] A pointer to the native calling convention.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="39778-110">要求</span><span class="sxs-lookup"><span data-stu-id="39778-110">Requirements</span></span>  

 <span data-ttu-id="39778-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="39778-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="39778-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="39778-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="39778-113">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="39778-113">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="39778-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="39778-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="39778-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="39778-115">See also</span></span>

- <xref:System.Runtime.InteropServices.CallingConvention>
- [<span data-ttu-id="39778-116">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="39778-116">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="39778-117">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="39778-117">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
