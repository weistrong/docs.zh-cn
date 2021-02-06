---
description: 了解详细信息： AddImport 方法
title: AddImport 方法
ms.date: 03/30/2017
api_name:
- AddImport
- IALink.AddImport
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- AddImport
helpviewer_keywords:
- AddImport method
ms.assetid: 4fedf8a0-08c8-43d0-aa00-20f2a521c991
topic_type:
- apiref
ms.openlocfilehash: 9dca26501e66313b0932caf1288db7c909154e1a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638595"
---
# <a name="addimport-method"></a><span data-ttu-id="ab406-103">AddImport 方法</span><span class="sxs-lookup"><span data-stu-id="ab406-103">AddImport Method</span></span>

<span data-ttu-id="ab406-104">将导入添加到程序集。</span><span class="sxs-lookup"><span data-stu-id="ab406-104">Adds imports to the assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ab406-105">语法</span><span class="sxs-lookup"><span data-stu-id="ab406-105">Syntax</span></span>  
  
```cpp  
HRESULT AddImport(  
    mdAssembly      AssemblyID,  
    mdToken         ImportToken,  
    DWORD           dwFlags,  
    mdFile*         pFileToken  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="ab406-106">参数</span><span class="sxs-lookup"><span data-stu-id="ab406-106">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="ab406-107">要扩充的程序集的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="ab406-107">Unique ID of assembly to be augmented.</span></span>  
  
 `ImportToken`  
 <span data-ttu-id="ab406-108">要导入的文件从 [ImportFile 方法](importfile-method.md)检索的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="ab406-108">Unique ID, retrieved from [ImportFile Method](importfile-method.md), of file to be imported.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="ab406-109">COM + FileDef 标志 `ffContainsNoMetaData` ，例如和 `ffWriteable` 。</span><span class="sxs-lookup"><span data-stu-id="ab406-109">COM+ FileDef flags such as `ffContainsNoMetaData` and `ffWriteable`.</span></span> <span data-ttu-id="ab406-110">`dwFlags` 传递给 [DefineFile 方法](../metadata/imetadataassemblyemit-definefile-method.md)。</span><span class="sxs-lookup"><span data-stu-id="ab406-110">`dwFlags` is passed to [DefineFile Method](../metadata/imetadataassemblyemit-definefile-method.md).</span></span>  
  
 `pFileToken`  
 <span data-ttu-id="ab406-111">指向接收结果文件的 ID 的标记的指针。</span><span class="sxs-lookup"><span data-stu-id="ab406-111">Pointer to token that receives the ID for the resulting file.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ab406-112">返回值</span><span class="sxs-lookup"><span data-stu-id="ab406-112">Return Value</span></span>  

 <span data-ttu-id="ab406-113">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="ab406-113">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ab406-114">要求</span><span class="sxs-lookup"><span data-stu-id="ab406-114">Requirements</span></span>  

 <span data-ttu-id="ab406-115">需要 alink</span><span class="sxs-lookup"><span data-stu-id="ab406-115">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab406-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="ab406-116">See also</span></span>

- [<span data-ttu-id="ab406-117">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="ab406-117">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="ab406-118">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="ab406-118">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="ab406-119">ALink API</span><span class="sxs-lookup"><span data-stu-id="ab406-119">ALink API</span></span>](index.md)
