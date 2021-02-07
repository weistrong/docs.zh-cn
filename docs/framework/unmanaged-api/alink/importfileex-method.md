---
description: 了解详细信息： ImportFileEx 方法
title: ImportFileEx 方法
ms.date: 03/30/2017
api_name:
- IALink2.ImportFileEx
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ImportFileEx
helpviewer_keywords:
- ImportFileEx method
ms.assetid: ad276f3f-b303-46ac-97e0-66a377adaa4f
topic_type:
- apiref
ms.openlocfilehash: a8a7e5a142091bf7cc93f50a4ae20c59d800f3ff
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99718013"
---
# <a name="importfileex-method"></a><span data-ttu-id="85dd8-103">ImportFileEx 方法</span><span class="sxs-lookup"><span data-stu-id="85dd8-103">ImportFileEx Method</span></span>

<span data-ttu-id="85dd8-104">导入指定的程序集或未绑定模块。</span><span class="sxs-lookup"><span data-stu-id="85dd8-104">Imports indicated assembly or unbound module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="85dd8-105">语法</span><span class="sxs-lookup"><span data-stu-id="85dd8-105">Syntax</span></span>  
  
```cpp  
HRESULT ImportFileEx(  
    LPCWSTR pszFilename,  
    LPCWSTR pszTargetName,  
    BOOL fSmartImport,  
    DWORD dwOpenFlags,  
    mdToken* pImportToken,  
    IMetaDataAssemblyImport** ppAssemblyScope,  
    DWORD* pdwCountOfScopes  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="85dd8-106">参数</span><span class="sxs-lookup"><span data-stu-id="85dd8-106">Parameters</span></span>  

 `pszFilename`  
 <span data-ttu-id="85dd8-107">要导入的文件的完全限定名称。</span><span class="sxs-lookup"><span data-stu-id="85dd8-107">Fully qualified name of file from which to import.</span></span>  
  
 `pszTargetName`  
 <span data-ttu-id="85dd8-108">目标文件的可选名称。</span><span class="sxs-lookup"><span data-stu-id="85dd8-108">Optional name of target file.</span></span>  
  
 `fSmartImport`  
 <span data-ttu-id="85dd8-109">如果为 TRUE，则使用 ImportTypes，否则必须手动执行导入。</span><span class="sxs-lookup"><span data-stu-id="85dd8-109">If TRUE, ImportTypes is used, otherwise importing must be performed manually.</span></span>  
  
 `dwOpenFlags`  
 <span data-ttu-id="85dd8-110">要传递给 [OpenScope 方法](../metadata/imetadatadispenser-openscope-method.md)的标志。</span><span class="sxs-lookup"><span data-stu-id="85dd8-110">Flags to be passed along to [OpenScope Method](../metadata/imetadatadispenser-openscope-method.md).</span></span>  
  
 `pImportToken`  
 <span data-ttu-id="85dd8-111">接收正在导入的文件的 ID。</span><span class="sxs-lookup"><span data-stu-id="85dd8-111">Receives ID of the file being imported.</span></span>  
  
 `ppAssemblyScope`  
 <span data-ttu-id="85dd8-112">接收程序集导入范围 [IMetaDataAssemblyImport 接口](../metadata/imetadataassemblyimport-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="85dd8-112">Receives assembly import scope [IMetaDataAssemblyImport Interface](../metadata/imetadataassemblyimport-interface.md) interface.</span></span> <span data-ttu-id="85dd8-113">如果文件不是程序集，则设置为 NULL。</span><span class="sxs-lookup"><span data-stu-id="85dd8-113">Is set to NULL if file is not an assembly.</span></span>  
  
 `pdwCountOfScopes`  
 <span data-ttu-id="85dd8-114">接收导入文件和/或范围的计数。</span><span class="sxs-lookup"><span data-stu-id="85dd8-114">Receives count of imported files and/or scopes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="85dd8-115">返回值</span><span class="sxs-lookup"><span data-stu-id="85dd8-115">Return Value</span></span>  

 <span data-ttu-id="85dd8-116">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="85dd8-116">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="85dd8-117">要求</span><span class="sxs-lookup"><span data-stu-id="85dd8-117">Requirements</span></span>  

 <span data-ttu-id="85dd8-118">需要 alink。</span><span class="sxs-lookup"><span data-stu-id="85dd8-118">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="85dd8-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="85dd8-119">See also</span></span>

- [<span data-ttu-id="85dd8-120">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="85dd8-120">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="85dd8-121">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="85dd8-121">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="85dd8-122">ALink API</span><span class="sxs-lookup"><span data-stu-id="85dd8-122">ALink API</span></span>](index.md)
