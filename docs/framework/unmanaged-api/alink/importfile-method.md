---
description: 了解详细信息： ImportFile 方法
title: ImportFile 方法
ms.date: 03/30/2017
api_name:
- IALink.ImportFile
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ImportFile
helpviewer_keywords:
- ImportFile method
ms.assetid: bcbe321f-b83a-4e9a-9f10-8d913e244dc9
topic_type:
- apiref
ms.openlocfilehash: 82c9c7de7cd739ee205dc3695ea651643d01ea3a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99718156"
---
# <a name="importfile-method"></a><span data-ttu-id="378dc-103">ImportFile 方法</span><span class="sxs-lookup"><span data-stu-id="378dc-103">ImportFile Method</span></span>

<span data-ttu-id="378dc-104">导入程序集和未绑定模块。</span><span class="sxs-lookup"><span data-stu-id="378dc-104">Imports assemblies and unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="378dc-105">语法</span><span class="sxs-lookup"><span data-stu-id="378dc-105">Syntax</span></span>  
  
```cpp  
HRESULT ImportFile(  
    LPCWSTR pszFilename,  
    LPCWSTR pszTargetName,  
    BOOL fSmartImport,  
    mdToken* pImportToken,  
    IMetaDataAssemblyImport** ppAssemblyScope,  
    DWORD* pdwCountOfScopes  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="378dc-106">参数</span><span class="sxs-lookup"><span data-stu-id="378dc-106">Parameters</span></span>  

 `pszFilename`  
 <span data-ttu-id="378dc-107">要导入的文件的完全限定名称。</span><span class="sxs-lookup"><span data-stu-id="378dc-107">Fully qualified name of file to be imported.</span></span>  
  
 `pszTargetName`  
 <span data-ttu-id="378dc-108">可选输出文件名，可用于在文件链接到程序集时对其进行重命名。</span><span class="sxs-lookup"><span data-stu-id="378dc-108">Optional output file name that can be used to rename the file as it is linked into the assembly.</span></span>  
  
 `fSmartImport`  
 <span data-ttu-id="378dc-109">如果为 TRUE，则使用 ImportTypes，否则必须手动执行导入。</span><span class="sxs-lookup"><span data-stu-id="378dc-109">If TRUE, ImportTypes is used, otherwise importing must be performed manually.</span></span>  
  
 `pImportToken`  
 <span data-ttu-id="378dc-110">指向将存储唯一文件 ID 的标记的指针。</span><span class="sxs-lookup"><span data-stu-id="378dc-110">Pointer to token where a unique file ID will be stored.</span></span> <span data-ttu-id="378dc-111">该文件可以是程序集或文件。</span><span class="sxs-lookup"><span data-stu-id="378dc-111">The file can be an assembly or a file.</span></span>  
  
 `ppAssemblyScope`  
 <span data-ttu-id="378dc-112">接收指向 [IMetaDataAssemblyImport 接口](../metadata/imetadataassemblyimport-interface.md)的指针。</span><span class="sxs-lookup"><span data-stu-id="378dc-112">Receives pointer to [IMetaDataAssemblyImport Interface](../metadata/imetadataassemblyimport-interface.md).</span></span> <span data-ttu-id="378dc-113">如果文件不是程序集，则可以为 NULL。</span><span class="sxs-lookup"><span data-stu-id="378dc-113">Can be NULL if the file is not an assembly.</span></span>  
  
 `pdwCountOfScopes`  
 <span data-ttu-id="378dc-114">一个指针，指向已导入的文件和/或范围的计数。</span><span class="sxs-lookup"><span data-stu-id="378dc-114">Pointer to the count of files and/or scopes that have been imported.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="378dc-115">返回值</span><span class="sxs-lookup"><span data-stu-id="378dc-115">Return Value</span></span>  

 <span data-ttu-id="378dc-116">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="378dc-116">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="378dc-117">要求</span><span class="sxs-lookup"><span data-stu-id="378dc-117">Requirements</span></span>  

 <span data-ttu-id="378dc-118">需要 alink</span><span class="sxs-lookup"><span data-stu-id="378dc-118">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="378dc-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="378dc-119">See also</span></span>

- [<span data-ttu-id="378dc-120">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="378dc-120">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="378dc-121">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="378dc-121">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="378dc-122">ALink API</span><span class="sxs-lookup"><span data-stu-id="378dc-122">ALink API</span></span>](index.md)
