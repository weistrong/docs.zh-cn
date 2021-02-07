---
description: 了解详细信息： IAssemblyCache：： QueryAssemblyInfo 方法
title: IAssemblyCache::QueryAssemblyInfo 方法
ms.date: 03/30/2017
api_name:
- IAssemblyCache.QueryAssemblyInfo
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCache::QueryAssemblyInfo
helpviewer_keywords:
- IAssemblyCache::QueryAssemblyInfo method [.NET Framework fusion]
- QueryAssemblyInfo method [.NET Framework fusion]
ms.assetid: 09313cb5-06f6-43bd-94f4-1055c6b0c99a
topic_type:
- apiref
ms.openlocfilehash: b3aa0064e24b22cf0af8b4e8d23a8b92d2f1ac34
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760909"
---
# <a name="iassemblycachequeryassemblyinfo-method"></a><span data-ttu-id="d47ea-103">IAssemblyCache::QueryAssemblyInfo 方法</span><span class="sxs-lookup"><span data-stu-id="d47ea-103">IAssemblyCache::QueryAssemblyInfo Method</span></span>

<span data-ttu-id="d47ea-104">获取有关指定程序集的请求的数据。</span><span class="sxs-lookup"><span data-stu-id="d47ea-104">Gets the requested data about the specified assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d47ea-105">语法</span><span class="sxs-lookup"><span data-stu-id="d47ea-105">Syntax</span></span>  
  
```cpp  
HRESULT QueryAssemblyInfo (  
    [in] DWORD dwFlags,  
    [in] LPCWSTR pszAssemblyName,  
    [in, out] ASSEMBLY_INFO *pAsmInfo  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d47ea-106">参数</span><span class="sxs-lookup"><span data-stu-id="d47ea-106">Parameters</span></span>  

 `dwFlags`  
 <span data-ttu-id="d47ea-107">中在合成 .idl 中定义的标志。</span><span class="sxs-lookup"><span data-stu-id="d47ea-107">[in] Flags defined in Fusion.idl.</span></span> <span data-ttu-id="d47ea-108">支持以下值：</span><span class="sxs-lookup"><span data-stu-id="d47ea-108">The following values are supported:</span></span>  
  
- <span data-ttu-id="d47ea-109"> (0x00000001) QUERYASMINFO_FLAG_VALIDATE</span><span class="sxs-lookup"><span data-stu-id="d47ea-109">QUERYASMINFO_FLAG_VALIDATE (0x00000001)</span></span>  
  
- <span data-ttu-id="d47ea-110">QUERYASMINFO_FLAG_GETSIZE (0x00000002) </span><span class="sxs-lookup"><span data-stu-id="d47ea-110">QUERYASMINFO_FLAG_GETSIZE (0x00000002)</span></span>  
  
 `pszAssemblyName`  
 <span data-ttu-id="d47ea-111">中将为其检索数据的程序集的名称。</span><span class="sxs-lookup"><span data-stu-id="d47ea-111">[in] The name of the assembly for which data will be retrieved.</span></span>  
  
 `pAsmInfo`  
 <span data-ttu-id="d47ea-112">[in，out]一个 [ASSEMBLY_INFO](assembly-info-structure.md) 结构，它包含有关程序集的数据。</span><span class="sxs-lookup"><span data-stu-id="d47ea-112">[in, out] An [ASSEMBLY_INFO](assembly-info-structure.md) structure that contains data about the assembly.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d47ea-113">要求</span><span class="sxs-lookup"><span data-stu-id="d47ea-113">Requirements</span></span>  

 <span data-ttu-id="d47ea-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d47ea-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d47ea-115">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="d47ea-115">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="d47ea-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d47ea-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d47ea-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="d47ea-117">See also</span></span>

- [<span data-ttu-id="d47ea-118">IAssemblyCache 接口</span><span class="sxs-lookup"><span data-stu-id="d47ea-118">IAssemblyCache Interface</span></span>](iassemblycache-interface.md)
