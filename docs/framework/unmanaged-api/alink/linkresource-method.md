---
description: 了解详细信息： LinkResource 方法
title: LinkResource 方法
ms.date: 03/30/2017
api_name:
- IALink.LinkResource
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- LinkResource
helpviewer_keywords:
- LinkResource method
ms.assetid: c404acb3-4c59-4100-9a4c-483cbdb1d736
topic_type:
- apiref
ms.openlocfilehash: ff12138433577eccbb313b8e64a329be1358ba70
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662541"
---
# <a name="linkresource-method"></a><span data-ttu-id="8092b-103">LinkResource 方法</span><span class="sxs-lookup"><span data-stu-id="8092b-103">LinkResource Method</span></span>

<span data-ttu-id="8092b-104">资源中的链接。</span><span class="sxs-lookup"><span data-stu-id="8092b-104">Links in a resource.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8092b-105">语法</span><span class="sxs-lookup"><span data-stu-id="8092b-105">Syntax</span></span>  
  
```cpp  
HRESULT LinkResource(  
    mdAssembly  AssemblyID,  
    LPCWSTR     pszFileName,  
    LPCWSTR     pszNewLocation,  
    LPCWSTR     pszResourceName,  
    DWORD       dwFlags  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="8092b-106">参数</span><span class="sxs-lookup"><span data-stu-id="8092b-106">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="8092b-107">程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="8092b-107">ID of the assembly.</span></span>  
  
 `pszFileName`  
 <span data-ttu-id="8092b-108">文件的名称。</span><span class="sxs-lookup"><span data-stu-id="8092b-108">Name of the file.</span></span>  
  
 `pszNewLocation`  
 <span data-ttu-id="8092b-109">可选的新文件名。</span><span class="sxs-lookup"><span data-stu-id="8092b-109">Optional new file name.</span></span> <span data-ttu-id="8092b-110">如果非 NULL， `pszFileName` 则将复制到 pszNewLocation。</span><span class="sxs-lookup"><span data-stu-id="8092b-110">If non-NULL, `pszFileName` will be copied to pszNewLocation.</span></span>  
  
 `pszResourceName`  
 <span data-ttu-id="8092b-111">资源的名称。</span><span class="sxs-lookup"><span data-stu-id="8092b-111">Name of the resource.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="8092b-112">辅助功能标志 `mrPublic` ，例如和 `mrPrivate` 。</span><span class="sxs-lookup"><span data-stu-id="8092b-112">Accessibility flags such as `mrPublic` and `mrPrivate`.</span></span> <span data-ttu-id="8092b-113">此参数可传递给 [DefineManifestResource 方法](../metadata/imetadataassemblyemit-definemanifestresource-method.md)。</span><span class="sxs-lookup"><span data-stu-id="8092b-113">This parameter may be passed to [DefineManifestResource Method](../metadata/imetadataassemblyemit-definemanifestresource-method.md).</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8092b-114">返回值</span><span class="sxs-lookup"><span data-stu-id="8092b-114">Return Value</span></span>  

 <span data-ttu-id="8092b-115">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="8092b-115">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8092b-116">要求</span><span class="sxs-lookup"><span data-stu-id="8092b-116">Requirements</span></span>  

 <span data-ttu-id="8092b-117">需要 alink。</span><span class="sxs-lookup"><span data-stu-id="8092b-117">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8092b-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="8092b-118">See also</span></span>

- [<span data-ttu-id="8092b-119">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="8092b-119">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="8092b-120">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="8092b-120">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="8092b-121">ALink API</span><span class="sxs-lookup"><span data-stu-id="8092b-121">ALink API</span></span>](index.md)
