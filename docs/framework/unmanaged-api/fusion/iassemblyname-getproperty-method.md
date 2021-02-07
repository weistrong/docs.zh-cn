---
description: 了解详细信息： IAssemblyName：： GetProperty 方法
title: IAssemblyName::GetProperty 方法
ms.date: 03/30/2017
api_name:
- IAssemblyName.GetProperty
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::GetProperty
helpviewer_keywords:
- IAssemblyName::GetProperty method [.NET Framework fusion]
- GetProperty method [.NET Framework fusion]
ms.assetid: e59fda62-77d5-4e37-89cb-ce7ae4627975
topic_type:
- apiref
ms.openlocfilehash: 66528bb54e1cb4adbba8fa87088065bc40c2ee15
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760727"
---
# <a name="iassemblynamegetproperty-method"></a><span data-ttu-id="83c87-103">IAssemblyName::GetProperty 方法</span><span class="sxs-lookup"><span data-stu-id="83c87-103">IAssemblyName::GetProperty Method</span></span>

<span data-ttu-id="83c87-104">获取一个指针，该指针指向由指定的属性标识符引用的属性。</span><span class="sxs-lookup"><span data-stu-id="83c87-104">Gets a pointer to the property referenced by the specified property identifier.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="83c87-105">语法</span><span class="sxs-lookup"><span data-stu-id="83c87-105">Syntax</span></span>  
  
```cpp  
HRESULT GetProperty (  
    [in]      DWORD    PropertyId,  
    [out]     LPVOID   pvProperty,  
    [in, out] LPDWORD  pcbProperty  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="83c87-106">参数</span><span class="sxs-lookup"><span data-stu-id="83c87-106">Parameters</span></span>  

 `PropertyId`  
 <span data-ttu-id="83c87-107">中请求的属性的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="83c87-107">[in] The unique identifier for the requested property.</span></span>  
  
 `pvProperty`  
 <span data-ttu-id="83c87-108">弄返回的属性数据。</span><span class="sxs-lookup"><span data-stu-id="83c87-108">[out] The returned property data.</span></span>  
  
 `pcbProperty`  
 <span data-ttu-id="83c87-109">[in，out]的大小（以字节为单位） `pvProperty` 。</span><span class="sxs-lookup"><span data-stu-id="83c87-109">[in, out] The size, in bytes, of `pvProperty`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="83c87-110">要求</span><span class="sxs-lookup"><span data-stu-id="83c87-110">Requirements</span></span>  

 <span data-ttu-id="83c87-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="83c87-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="83c87-112">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="83c87-112">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="83c87-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="83c87-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="83c87-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="83c87-114">See also</span></span>

- [<span data-ttu-id="83c87-115">IAssemblyName 接口</span><span class="sxs-lookup"><span data-stu-id="83c87-115">IAssemblyName Interface</span></span>](iassemblyname-interface.md)
