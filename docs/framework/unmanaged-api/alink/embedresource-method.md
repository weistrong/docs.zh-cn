---
description: 了解详细信息： EmbedResource 方法
title: EmbedResource 方法
ms.date: 03/30/2017
api_name:
- IALink.EmbedResource
- EmbedResource
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EmbedResource
helpviewer_keywords:
- EmbedResource method
ms.assetid: 667bd954-6dc6-4020-a3cb-0e8224179993
topic_type:
- apiref
ms.openlocfilehash: f7896172e7416048352788caf7e092096924b7af
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638348"
---
# <a name="embedresource-method"></a><span data-ttu-id="96609-103">EmbedResource 方法</span><span class="sxs-lookup"><span data-stu-id="96609-103">EmbedResource Method</span></span>

<span data-ttu-id="96609-104">声明嵌入的资源。</span><span class="sxs-lookup"><span data-stu-id="96609-104">Declares an embedded resource.</span></span> <span data-ttu-id="96609-105">此方法并不实际嵌入资源。</span><span class="sxs-lookup"><span data-stu-id="96609-105">This method does not actually embed the resource.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="96609-106">语法</span><span class="sxs-lookup"><span data-stu-id="96609-106">Syntax</span></span>  
  
```cpp  
HRESULT EmbedResource(  
    mdAssembly  AssemblyID,  
    mdToken     FileToken,  
    LPCWSTR     pszResourceName,  
    DWORD       dwOffset,  
    DWORD       dwFlags  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="96609-107">参数</span><span class="sxs-lookup"><span data-stu-id="96609-107">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="96609-108">程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="96609-108">ID of the assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="96609-109">包含资源的文件的文件标记或程序集 ID。</span><span class="sxs-lookup"><span data-stu-id="96609-109">File token or assembly ID of file that contains the resource.</span></span>  
  
 `pszResourceName`  
 <span data-ttu-id="96609-110">资源的名称。</span><span class="sxs-lookup"><span data-stu-id="96609-110">Name of the resource.</span></span>  
  
 `dwOffset`  
 <span data-ttu-id="96609-111">RVA 中资源的偏移量。</span><span class="sxs-lookup"><span data-stu-id="96609-111">Offset of resource from RVA.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="96609-112">辅助功能标志 `mrPublic` ，例如和 `mrPrivate` 。</span><span class="sxs-lookup"><span data-stu-id="96609-112">Accessibility flags such as `mrPublic` and `mrPrivate`.</span></span> <span data-ttu-id="96609-113">这些标志可能会传递给 [DefineExportedType 方法](../metadata/imetadataassemblyemit-defineexportedtype-method.md)。</span><span class="sxs-lookup"><span data-stu-id="96609-113">These flags may be passed to [DefineExportedType Method](../metadata/imetadataassemblyemit-defineexportedtype-method.md).</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="96609-114">返回值</span><span class="sxs-lookup"><span data-stu-id="96609-114">Return Value</span></span>  

 <span data-ttu-id="96609-115">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="96609-115">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="96609-116">要求</span><span class="sxs-lookup"><span data-stu-id="96609-116">Requirements</span></span>  

 <span data-ttu-id="96609-117">需要 alink。</span><span class="sxs-lookup"><span data-stu-id="96609-117">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="96609-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="96609-118">See also</span></span>

- [<span data-ttu-id="96609-119">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="96609-119">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="96609-120">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="96609-120">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="96609-121">ALink API</span><span class="sxs-lookup"><span data-stu-id="96609-121">ALink API</span></span>](index.md)
