---
description: 了解详细信息： ImportFile2 方法
title: ImportFile2 方法
ms.date: 03/30/2017
api_name:
- IALink.ImportFile2
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ImportFile2
helpviewer_keywords:
- ImportFile2 method
ms.assetid: 9a6be861-c260-4a35-acea-3372ea515a0f
topic_type:
- apiref
ms.openlocfilehash: 98da8ecf4bfc19e52c5a92e6509f6af49afbdd5f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99718052"
---
# <a name="importfile2-method"></a><span data-ttu-id="55ecd-103">ImportFile2 方法</span><span class="sxs-lookup"><span data-stu-id="55ecd-103">ImportFile2 Method</span></span>

<span data-ttu-id="55ecd-104">导入程序集和未绑定模块。</span><span class="sxs-lookup"><span data-stu-id="55ecd-104">Imports assemblies and unbound modules.</span></span> <span data-ttu-id="55ecd-105">此方法类似于 [ImportFile 方法](importfile-method.md)，但即使磁盘上没有要导入的文件也能正常工作。</span><span class="sxs-lookup"><span data-stu-id="55ecd-105">This method is like [ImportFile Method](importfile-method.md), but works even if the file being imported does not exist on disk.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="55ecd-106">语法</span><span class="sxs-lookup"><span data-stu-id="55ecd-106">Syntax</span></span>  
  
```cpp  
HRESULT ImportFile2(  
    LPCWSTR         pszFilename,  
    LPCWSTR         pszTargetName,  
    IMetaDataAssemblyImport* pAssemblyScopeIn,  
    BOOL            fSmartImport,  
    mdToken*        pImportToken,  
    IMetaDataAssemblyImport** ppAssemblyScope,  
    DWORD*          pdwCountOfScopes  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="55ecd-107">参数</span><span class="sxs-lookup"><span data-stu-id="55ecd-107">Parameters</span></span>  

 `pszFilename`  
 <span data-ttu-id="55ecd-108">要导入的文件的名称。</span><span class="sxs-lookup"><span data-stu-id="55ecd-108">Name of file to be imported.</span></span>  
  
 `pszTargetName`  
 <span data-ttu-id="55ecd-109">可选输出文件名，可用于在文件链接到程序集时对其进行重命名。</span><span class="sxs-lookup"><span data-stu-id="55ecd-109">Optional output file name that can be used to rename the file as it is linked into the assembly.</span></span>  
  
 `pAssemblyScopeIn`  
 <span data-ttu-id="55ecd-110">可选范围 [IMetaDataAssemblyImport 接口](../metadata/imetadataassemblyimport-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="55ecd-110">Optional scope [IMetaDataAssemblyImport Interface](../metadata/imetadataassemblyimport-interface.md) interface.</span></span>  
  
 `fSmartImport`  
 <span data-ttu-id="55ecd-111">如果为 TRUE，则使用 ImportTypes，否则必须手动执行导入。</span><span class="sxs-lookup"><span data-stu-id="55ecd-111">If TRUE, ImportTypes is used, otherwise importing must be performed manually.</span></span>  
  
 `pImportToken`  
 <span data-ttu-id="55ecd-112">接收文件或程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="55ecd-112">Receives the ID for the file or assembly.</span></span>  
  
 `ppAssemblyScope`  
 <span data-ttu-id="55ecd-113">接收 [IMetaDataAssemblyImport 接口](../metadata/imetadataassemblyimport-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="55ecd-113">Receives the [IMetaDataAssemblyImport Interface](../metadata/imetadataassemblyimport-interface.md) interface.</span></span> <span data-ttu-id="55ecd-114">如果文件不是程序集，则为 NULL。</span><span class="sxs-lookup"><span data-stu-id="55ecd-114">NULL if the file is not an assembly.</span></span>  
  
 `pdwCountOfScopes`  
 <span data-ttu-id="55ecd-115">接收导入的文件和/或范围的发现。</span><span class="sxs-lookup"><span data-stu-id="55ecd-115">Receives the found of files and/or scopes imported.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="55ecd-116">返回值</span><span class="sxs-lookup"><span data-stu-id="55ecd-116">Return Value</span></span>  

 <span data-ttu-id="55ecd-117">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="55ecd-117">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="55ecd-118">要求</span><span class="sxs-lookup"><span data-stu-id="55ecd-118">Requirements</span></span>  

 <span data-ttu-id="55ecd-119">需要 alink。</span><span class="sxs-lookup"><span data-stu-id="55ecd-119">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="55ecd-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="55ecd-120">See also</span></span>

- [<span data-ttu-id="55ecd-121">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="55ecd-121">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="55ecd-122">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="55ecd-122">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="55ecd-123">ALink API</span><span class="sxs-lookup"><span data-stu-id="55ecd-123">ALink API</span></span>](index.md)
