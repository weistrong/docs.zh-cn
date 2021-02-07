---
description: 了解详细信息： IMetaDataDispenserEx：： GetCORSystemDirectory 方法
title: IMetaDataDispenserEx::GetCORSystemDirectory 方法
ms.date: 03/30/2017
api_name:
- IMetaDataDispenserEx.GetCORSystemDirectory
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenserEx::GetCORSystemDirectory
helpviewer_keywords:
- IMetaDataDispenserEx::GetCORSystemDirectory method [.NET Framework metadata]
- GetCORSystemDirectory method [.NET Framework metadata]
ms.assetid: d9e0f3b6-e106-4820-bada-5bfba34ce360
topic_type:
- apiref
ms.openlocfilehash: 3ceda653e50ba5ad7de5548b78781f48cda41624
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753557"
---
# <a name="imetadatadispenserexgetcorsystemdirectory-method"></a><span data-ttu-id="1dc85-103">IMetaDataDispenserEx::GetCORSystemDirectory 方法</span><span class="sxs-lookup"><span data-stu-id="1dc85-103">IMetaDataDispenserEx::GetCORSystemDirectory Method</span></span>

<span data-ttu-id="1dc85-104">获取 (CLR) 保存当前公共语言运行时的目录。</span><span class="sxs-lookup"><span data-stu-id="1dc85-104">Gets the directory that holds the current common language runtime (CLR).</span></span> <span data-ttu-id="1dc85-105">此方法仅支持在进程外调试器中使用。</span><span class="sxs-lookup"><span data-stu-id="1dc85-105">This method is supported only for use by out-of-process debuggers.</span></span> <span data-ttu-id="1dc85-106">如果从另一个组件调用，它将返回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="1dc85-106">If called from another component, it will return E_NOTIMPL.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1dc85-107">语法</span><span class="sxs-lookup"><span data-stu-id="1dc85-107">Syntax</span></span>  
  
```cpp  
HRESULT GetCORSystemDirectory (  
    [out] LPWSTR      szBuffer,
    [in]  DWORD       cchBuffer,
    [out] DWORD*      pchBuffer  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1dc85-108">参数</span><span class="sxs-lookup"><span data-stu-id="1dc85-108">Parameters</span></span>  

 `szBuffer`  
 <span data-ttu-id="1dc85-109">弄要接收目录名称的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="1dc85-109">[out] The buffer to receive the directory name.</span></span>  
  
 `cchBuffer`  
 <span data-ttu-id="1dc85-110">中的大小（以字节为单位） `szBuffer` 。</span><span class="sxs-lookup"><span data-stu-id="1dc85-110">[in] The size, in bytes, of `szBuffer`.</span></span>  
  
 `pchBuffer`  
 <span data-ttu-id="1dc85-111">弄中实际返回的字节数 `szBuffer` 。</span><span class="sxs-lookup"><span data-stu-id="1dc85-111">[out] The number of bytes actually returned in `szBuffer`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1dc85-112">要求</span><span class="sxs-lookup"><span data-stu-id="1dc85-112">Requirements</span></span>  

 <span data-ttu-id="1dc85-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1dc85-113">**Platform:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1dc85-114">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="1dc85-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="1dc85-115">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="1dc85-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="1dc85-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1dc85-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1dc85-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="1dc85-117">See also</span></span>

- [<span data-ttu-id="1dc85-118">IMetaDataDispenserEx 接口</span><span class="sxs-lookup"><span data-stu-id="1dc85-118">IMetaDataDispenserEx Interface</span></span>](imetadatadispenserex-interface.md)
- [<span data-ttu-id="1dc85-119">IMetaDataDispenser 接口</span><span class="sxs-lookup"><span data-stu-id="1dc85-119">IMetaDataDispenser Interface</span></span>](imetadatadispenser-interface.md)
