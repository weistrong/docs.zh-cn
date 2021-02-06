---
description: 了解详细信息： SetAssemblyFile2 方法
title: SetAssemblyFile2 方法
ms.date: 03/30/2017
api_name:
- IALink2.SetAssemblyFile2
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- SetAssemblyFile2
helpviewer_keywords:
- SetAssemblyFile2 method
ms.assetid: eedb9125-1ef1-4000-abfc-7de86e5a1f17
topic_type:
- apiref
ms.openlocfilehash: 890646b718c211b476d013daf021f8889198c1ba
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662398"
---
# <a name="setassemblyfile2-method"></a><span data-ttu-id="57b77-103">SetAssemblyFile2 方法</span><span class="sxs-lookup"><span data-stu-id="57b77-103">SetAssemblyFile2 Method</span></span>

<span data-ttu-id="57b77-104">为新的程序集设置和选项的名称。</span><span class="sxs-lookup"><span data-stu-id="57b77-104">Sets the name of and options for a new assembly.</span></span> <span data-ttu-id="57b77-105">生成未绑定的模块时，请勿调用此方法。</span><span class="sxs-lookup"><span data-stu-id="57b77-105">Do not call this method when you produce unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="57b77-106">语法</span><span class="sxs-lookup"><span data-stu-id="57b77-106">Syntax</span></span>  
  
```cpp  
HRESULT SetAssemblyFile2(  
    LPCWSTR pszFilename,  
    IMetaDataEmit2* pEmitter,  
    AssemblyFlags   afFlags,  
    mdAssembly* pAssemblyID  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="57b77-107">参数</span><span class="sxs-lookup"><span data-stu-id="57b77-107">Parameters</span></span>  

 `pszFilename`  
 <span data-ttu-id="57b77-108">清单文件的名称。</span><span class="sxs-lookup"><span data-stu-id="57b77-108">Name of manifest file.</span></span>  
  
 `pEmitter`  
 <span data-ttu-id="57b77-109">此文件的[IMetaDataEmit2 接口](../metadata/imetadataemit2-interface.md)接口。</span><span class="sxs-lookup"><span data-stu-id="57b77-109">[IMetaDataEmit2 Interface](../metadata/imetadataemit2-interface.md) interface for this file.</span></span>  
  
 `afFlags`  
 <span data-ttu-id="57b77-110">[AssemblyFlags 枚举](../metadata/assemblyflags-enumeration.md)表示的选项。</span><span class="sxs-lookup"><span data-stu-id="57b77-110">Options represented by [AssemblyFlags Enumeration](../metadata/assemblyflags-enumeration.md).</span></span>  
  
 `pAssemblyID`  
 <span data-ttu-id="57b77-111">接收正在构造的程序集的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="57b77-111">Receives unique ID for the assembly being constructed.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="57b77-112">返回值</span><span class="sxs-lookup"><span data-stu-id="57b77-112">Return Value</span></span>  

 <span data-ttu-id="57b77-113">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="57b77-113">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="57b77-114">要求</span><span class="sxs-lookup"><span data-stu-id="57b77-114">Requirements</span></span>  

 <span data-ttu-id="57b77-115">需要 alink。</span><span class="sxs-lookup"><span data-stu-id="57b77-115">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="57b77-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="57b77-116">See also</span></span>

- [<span data-ttu-id="57b77-117">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="57b77-117">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="57b77-118">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="57b77-118">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="57b77-119">ALink API</span><span class="sxs-lookup"><span data-stu-id="57b77-119">ALink API</span></span>](index.md)
