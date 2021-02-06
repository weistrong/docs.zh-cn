---
description: 了解详细信息： ImportTypes 方法
title: ImportTypes 方法
ms.date: 03/30/2017
api_name:
- IALink.ImportTypes
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ImportTypes
helpviewer_keywords:
- ImportTypes method
ms.assetid: 351d4b4c-c939-486d-9471-51914a55f471
topic_type:
- apiref
ms.openlocfilehash: 9a30c735ca2c9ad0f945628c3de1eb1bb56efe2c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662619"
---
# <a name="importtypes-method"></a><span data-ttu-id="cc843-103">ImportTypes 方法</span><span class="sxs-lookup"><span data-stu-id="cc843-103">ImportTypes Method</span></span>

<span data-ttu-id="cc843-104">开始从通过 [ImportFile 方法](importfile-method.md)导入的每个范围导入类型。</span><span class="sxs-lookup"><span data-stu-id="cc843-104">Initiates the importing of types from each scope imported via [ImportFile Method](importfile-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cc843-105">语法</span><span class="sxs-lookup"><span data-stu-id="cc843-105">Syntax</span></span>  
  
```cpp  
HRESULT ImportTypes(  
    mdAssembly AssemblyID,  
    mdToken FileToken,  
    DWORD dwScope,  
    HALINKENUM* phEnum,  
    IMetaDataImport** ppImportScope,  
    DWORD* pdwCountOfTypes  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="cc843-106">参数</span><span class="sxs-lookup"><span data-stu-id="cc843-106">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="cc843-107">要导入到的程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="cc843-107">ID of the assembly to import to.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="cc843-108">要从中导入的文件的 ID。</span><span class="sxs-lookup"><span data-stu-id="cc843-108">ID of the file to import from.</span></span>  
  
 `dwScope`  
 <span data-ttu-id="cc843-109">要导入的从零开始的范围。</span><span class="sxs-lookup"><span data-stu-id="cc843-109">Zero-based scope to import.</span></span>  
  
 `phEnum`  
 <span data-ttu-id="cc843-110">接收此范围内的类型的枚举器句柄。</span><span class="sxs-lookup"><span data-stu-id="cc843-110">Receives enumerator handle for the types in this scope.</span></span>  
  
 `ppImportScope`  
 <span data-ttu-id="cc843-111">可以选择接收 [IMetaDataImport 接口](../metadata/imetadataimport-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="cc843-111">Optionally receives [IMetaDataImport Interface](../metadata/imetadataimport-interface.md) interface.</span></span>  
  
 `pdwCountOfTypes`  
 <span data-ttu-id="cc843-112">可以选择接收指定范围内的类型的计数。</span><span class="sxs-lookup"><span data-stu-id="cc843-112">Optionally receives count of types in the indicated scope.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cc843-113">返回值</span><span class="sxs-lookup"><span data-stu-id="cc843-113">Return Value</span></span>  

 <span data-ttu-id="cc843-114">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="cc843-114">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cc843-115">要求</span><span class="sxs-lookup"><span data-stu-id="cc843-115">Requirements</span></span>  

 <span data-ttu-id="cc843-116">需要 alink</span><span class="sxs-lookup"><span data-stu-id="cc843-116">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cc843-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="cc843-117">See also</span></span>

- [<span data-ttu-id="cc843-118">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="cc843-118">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="cc843-119">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="cc843-119">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="cc843-120">ALink API</span><span class="sxs-lookup"><span data-stu-id="cc843-120">ALink API</span></span>](index.md)
