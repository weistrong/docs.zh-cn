---
description: 了解详细信息： AddFile 方法
title: AddFile 方法
ms.date: 03/30/2017
api_name:
- IALink.AddFile
- AddFile
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- AddFile
helpviewer_keywords:
- AddFile method
ms.assetid: 9e707abb-f905-4568-9356-12aa21d1b11c
topic_type:
- apiref
ms.openlocfilehash: 5e1253587298b2c1559c72dced43ec70dc169090
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638621"
---
# <a name="addfile-method"></a><span data-ttu-id="955e0-103">AddFile 方法</span><span class="sxs-lookup"><span data-stu-id="955e0-103">AddFile Method</span></span>

<span data-ttu-id="955e0-104">将文件添加到程序集。</span><span class="sxs-lookup"><span data-stu-id="955e0-104">Adds files to the assembly.</span></span> <span data-ttu-id="955e0-105">还可用于创建未绑定的模块。</span><span class="sxs-lookup"><span data-stu-id="955e0-105">Can also be used to create unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="955e0-106">语法</span><span class="sxs-lookup"><span data-stu-id="955e0-106">Syntax</span></span>  
  
```cpp  
HRESULT AddFile(  
    mdAssembly      AssemblyID,  
    LPCWSTR         pszFilename,  
    DWORD           dwFlags,  
    IMetaDataEmit*  pEmitter,  
    mdFile*         pFileToken  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="955e0-107">参数</span><span class="sxs-lookup"><span data-stu-id="955e0-107">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="955e0-108">要扩充的程序集的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="955e0-108">Unique ID of the assembly to be augmented.</span></span>  
  
 `pszFilename`  
 <span data-ttu-id="955e0-109">要添加的文件的完全限定名称。</span><span class="sxs-lookup"><span data-stu-id="955e0-109">Fully qualified name of file to be added.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="955e0-110">COM + FileDef 标志 `ffContainsNoMetaData` ，例如和 `ffWriteable` 。</span><span class="sxs-lookup"><span data-stu-id="955e0-110">COM+ FileDef flags such as `ffContainsNoMetaData` and `ffWriteable`.</span></span> <span data-ttu-id="955e0-111">`dwFlags` 传递给 [DefineFile 方法](../metadata/imetadataassemblyemit-definefile-method.md)。</span><span class="sxs-lookup"><span data-stu-id="955e0-111">`dwFlags` is passed to [DefineFile Method](../metadata/imetadataassemblyemit-definefile-method.md).</span></span>  
  
 `pEmitter`  
 <span data-ttu-id="955e0-112">要用于发出元数据的[IMetaDataEmit 接口](../metadata/imetadataemit-interface.md)接口（如有必要）。</span><span class="sxs-lookup"><span data-stu-id="955e0-112">[IMetaDataEmit Interface](../metadata/imetadataemit-interface.md) interface to be used to emit metadata, if necessary.</span></span>  
  
 `pFileToken`  
 <span data-ttu-id="955e0-113">一个指针，指向将存储所添加文件的唯一 ID 的位置。</span><span class="sxs-lookup"><span data-stu-id="955e0-113">Pointer to where the unique ID of the added file will be stored.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="955e0-114">返回值</span><span class="sxs-lookup"><span data-stu-id="955e0-114">Return Value</span></span>  

 <span data-ttu-id="955e0-115">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="955e0-115">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="955e0-116">要求</span><span class="sxs-lookup"><span data-stu-id="955e0-116">Requirements</span></span>  

 <span data-ttu-id="955e0-117">需要 alink。</span><span class="sxs-lookup"><span data-stu-id="955e0-117">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="955e0-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="955e0-118">See also</span></span>

- [<span data-ttu-id="955e0-119">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="955e0-119">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="955e0-120">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="955e0-120">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="955e0-121">ALink API</span><span class="sxs-lookup"><span data-stu-id="955e0-121">ALink API</span></span>](index.md)
