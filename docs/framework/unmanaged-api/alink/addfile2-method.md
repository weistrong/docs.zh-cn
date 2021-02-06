---
description: 了解详细信息： AddFile2 方法
title: AddFile2 方法
ms.date: 03/30/2017
api_name:
- AddFile2
- IALink2.AddFile2
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- AddFile2
helpviewer_keywords:
- AddFile2 method
ms.assetid: 03bc49bf-a89b-4fb6-a88d-97482e061195
topic_type:
- apiref
ms.openlocfilehash: d53527ecf7e8b3a99a11ea99512fbc812125de3e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638608"
---
# <a name="addfile2-method"></a><span data-ttu-id="1ca5b-103">AddFile2 方法</span><span class="sxs-lookup"><span data-stu-id="1ca5b-103">AddFile2 Method</span></span>

<span data-ttu-id="1ca5b-104">将文件添加到程序集。</span><span class="sxs-lookup"><span data-stu-id="1ca5b-104">Adds files to the assembly.</span></span> <span data-ttu-id="1ca5b-105">还可用于创建未绑定的模块。</span><span class="sxs-lookup"><span data-stu-id="1ca5b-105">Can also be used to create unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1ca5b-106">语法</span><span class="sxs-lookup"><span data-stu-id="1ca5b-106">Syntax</span></span>  
  
```cpp  
HRESULT AddFile2(  
    mdAssembly AssemblyID,  
    LPCWSTR pszFilename,  
    DWORD dwFlags,  
    IMetaDataEmit2* pEmitter,  
    mdFile* pFileToken  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="1ca5b-107">参数</span><span class="sxs-lookup"><span data-stu-id="1ca5b-107">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="1ca5b-108">向其中添加文件的程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="1ca5b-108">ID for the assembly to which the file is added.</span></span>  
  
 `pszFilename`  
 <span data-ttu-id="1ca5b-109">要添加的文件的名称。</span><span class="sxs-lookup"><span data-stu-id="1ca5b-109">Name of the file to be added.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="1ca5b-110">COM + `FileDef` 标志 `ffContainsNoMetaData` ，例如和 `ffWriteable` 。</span><span class="sxs-lookup"><span data-stu-id="1ca5b-110">COM+ `FileDef` flags such as `ffContainsNoMetaData` and `ffWriteable`.</span></span> <span data-ttu-id="1ca5b-111">`dwFlags` 传递给 [DefineFile 方法](../metadata/imetadataassemblyemit-definefile-method.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca5b-111">`dwFlags` is passed to [DefineFile Method](../metadata/imetadataassemblyemit-definefile-method.md).</span></span>  
  
 `pEmitter`  
 <span data-ttu-id="1ca5b-112">[IMetaDataEmit2 接口](../metadata/imetadataemit2-interface.md)接口的接口。</span><span class="sxs-lookup"><span data-stu-id="1ca5b-112">Interface to [IMetaDataEmit2 Interface](../metadata/imetadataemit2-interface.md) interface.</span></span>  
  
 `pFileToken`  
 <span data-ttu-id="1ca5b-113">接收要添加的文件的 ID。</span><span class="sxs-lookup"><span data-stu-id="1ca5b-113">Receives ID for the file being added.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1ca5b-114">返回值</span><span class="sxs-lookup"><span data-stu-id="1ca5b-114">Return Value</span></span>  

 <span data-ttu-id="1ca5b-115">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="1ca5b-115">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1ca5b-116">要求</span><span class="sxs-lookup"><span data-stu-id="1ca5b-116">Requirements</span></span>  

 <span data-ttu-id="1ca5b-117">需要 alink。</span><span class="sxs-lookup"><span data-stu-id="1ca5b-117">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1ca5b-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="1ca5b-118">See also</span></span>

- [<span data-ttu-id="1ca5b-119">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="1ca5b-119">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="1ca5b-120">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="1ca5b-120">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="1ca5b-121">ALink API</span><span class="sxs-lookup"><span data-stu-id="1ca5b-121">ALink API</span></span>](index.md)
