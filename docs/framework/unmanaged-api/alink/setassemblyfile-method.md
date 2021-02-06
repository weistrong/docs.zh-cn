---
description: 了解详细信息： SetAssemblyFile 方法
title: SetAssemblyFile 方法
ms.date: 03/30/2017
api_name:
- IALink.SetAssemblyFile
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- SetAssemblyFile
helpviewer_keywords:
- SetAssemblyFile method
ms.assetid: 3a912787-f139-43ca-a841-8bbda3107ecf
topic_type:
- apiref
ms.openlocfilehash: 943e0600b9781aeaf45cc26e39bd8a8b33a783c2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662489"
---
# <a name="setassemblyfile-method"></a><span data-ttu-id="05a8d-103">SetAssemblyFile 方法</span><span class="sxs-lookup"><span data-stu-id="05a8d-103">SetAssemblyFile Method</span></span>

<span data-ttu-id="05a8d-104">指定要生成的程序集的名称。</span><span class="sxs-lookup"><span data-stu-id="05a8d-104">Assigns the name of the assembly to be built.</span></span> <span data-ttu-id="05a8d-105">不在生成未绑定的模块时使用。</span><span class="sxs-lookup"><span data-stu-id="05a8d-105">Not for use when producing unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="05a8d-106">语法</span><span class="sxs-lookup"><span data-stu-id="05a8d-106">Syntax</span></span>  
  
```cpp  
HRESULT SetAssemblyFile(  
    LPCWSTR pszFilename,  
    IMetaDataEmit* pEmitter,  
    AssemblyFlags afFlags,  
    mdAssembly* pAssemblyID  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="05a8d-107">参数</span><span class="sxs-lookup"><span data-stu-id="05a8d-107">Parameters</span></span>  

 `pszFilename`  
 <span data-ttu-id="05a8d-108">清单文件的完全限定名称。</span><span class="sxs-lookup"><span data-stu-id="05a8d-108">Fully qualified name of the manifest file.</span></span>  
  
 `pEmitter`  
 <span data-ttu-id="05a8d-109">指向 [IMetaDataEmit 接口](../metadata/imetadataemit-interface.md) 接口的指针。</span><span class="sxs-lookup"><span data-stu-id="05a8d-109">Pointer to [IMetaDataEmit Interface](../metadata/imetadataemit-interface.md) interface.</span></span>  
  
 `afFlags`  
 <span data-ttu-id="05a8d-110">[AssemblyFlags 枚举](../metadata/assemblyflags-enumeration.md)中定义的标志。</span><span class="sxs-lookup"><span data-stu-id="05a8d-110">Flags as defined in [AssemblyFlags Enumeration](../metadata/assemblyflags-enumeration.md).</span></span>  
  
 `pAssemblyID`  
 <span data-ttu-id="05a8d-111">指向生成的程序集的 ID 的指针。</span><span class="sxs-lookup"><span data-stu-id="05a8d-111">Pointer to ID of resulting assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="05a8d-112">返回值</span><span class="sxs-lookup"><span data-stu-id="05a8d-112">Return Value</span></span>  

 <span data-ttu-id="05a8d-113">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="05a8d-113">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="05a8d-114">要求</span><span class="sxs-lookup"><span data-stu-id="05a8d-114">Requirements</span></span>  

 <span data-ttu-id="05a8d-115">需要 alink。</span><span class="sxs-lookup"><span data-stu-id="05a8d-115">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="05a8d-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="05a8d-116">See also</span></span>

- [<span data-ttu-id="05a8d-117">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="05a8d-117">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="05a8d-118">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="05a8d-118">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="05a8d-119">ALink API</span><span class="sxs-lookup"><span data-stu-id="05a8d-119">ALink API</span></span>](index.md)
