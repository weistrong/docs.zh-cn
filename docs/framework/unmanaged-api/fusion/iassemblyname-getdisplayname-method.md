---
description: 了解详细信息： IAssemblyName：： GetDisplayName 方法
title: IAssemblyName::GetDisplayName 方法
ms.date: 03/30/2017
api_name:
- IAssemblyName.GetDisplayName
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::GetDisplayName
helpviewer_keywords:
- GetDisplayName method, IAssemblyName interface [.NET Framework fusion]
- IAssemblyName::GetDisplayName method [.NET Framework fusion]
ms.assetid: 9a26547a-9a34-4284-a463-78a7d4b496cf
topic_type:
- apiref
ms.openlocfilehash: 9b52a901385fa9b3ba7cb6bcd1678d0718f8f695
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760753"
---
# <a name="iassemblynamegetdisplayname-method"></a><span data-ttu-id="40f01-103">IAssemblyName::GetDisplayName 方法</span><span class="sxs-lookup"><span data-stu-id="40f01-103">IAssemblyName::GetDisplayName Method</span></span>

<span data-ttu-id="40f01-104">获取此 [IAssemblyName](iassemblyname-interface.md) 对象所引用的程序集的可读名称。</span><span class="sxs-lookup"><span data-stu-id="40f01-104">Gets the human-readable name of the assembly referenced by this [IAssemblyName](iassemblyname-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="40f01-105">语法</span><span class="sxs-lookup"><span data-stu-id="40f01-105">Syntax</span></span>  
  
```cpp  
HRESULT GetDisplayName (  
        [out]      LPOLESTR  szDisplayName,  
        [in, out]  LPDWORD   pccDisplayName,  
        [in]       DWORD     dwDisplayFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="40f01-106">参数</span><span class="sxs-lookup"><span data-stu-id="40f01-106">Parameters</span></span>  

 `szDisplayName`  
 <span data-ttu-id="40f01-107">弄包含所引用程序集的名称的字符串缓冲区。</span><span class="sxs-lookup"><span data-stu-id="40f01-107">[out] The string buffer that contains the name of the referenced assembly.</span></span>  
  
 `pccDisplayName`  
 <span data-ttu-id="40f01-108">[in，out] `szDisplayName` 宽字符的大小，包括 null 终止符。</span><span class="sxs-lookup"><span data-stu-id="40f01-108">[in, out] The size of `szDisplayName` in wide characters, including a null terminator character.</span></span>  
  
 `dwDisplayFlags`  
 <span data-ttu-id="40f01-109">中影响的功能 [ASM_DISPLAY_FLAGS](asm-display-flags-enumeration.md) 值的按位组合 `szDisplayName` 。</span><span class="sxs-lookup"><span data-stu-id="40f01-109">[in] A bitwise combination of [ASM_DISPLAY_FLAGS](asm-display-flags-enumeration.md) values that influence the features of `szDisplayName`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="40f01-110">要求</span><span class="sxs-lookup"><span data-stu-id="40f01-110">Requirements</span></span>  

 <span data-ttu-id="40f01-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="40f01-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="40f01-112">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="40f01-112">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="40f01-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="40f01-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="40f01-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="40f01-114">See also</span></span>

- [<span data-ttu-id="40f01-115">IAssemblyName 接口</span><span class="sxs-lookup"><span data-stu-id="40f01-115">IAssemblyName Interface</span></span>](iassemblyname-interface.md)
- [<span data-ttu-id="40f01-116">合成枚举</span><span class="sxs-lookup"><span data-stu-id="40f01-116">Fusion Enumerations</span></span>](fusion-enumerations.md)
