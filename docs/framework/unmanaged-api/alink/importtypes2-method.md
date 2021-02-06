---
description: 了解详细信息： ImportTypes2 方法
title: ImportTypes2 方法
ms.date: 03/30/2017
api_name:
- IALink2.ImportTypes2
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ImportTypes2
helpviewer_keywords:
- ImportTypes2 method
ms.assetid: 32f3ba58-9695-41e9-ba58-fd19e45ed396
topic_type:
- apiref
ms.openlocfilehash: ca0d174061608f9b4abf524c43023e867e9a9646
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662606"
---
# <a name="importtypes2-method"></a><span data-ttu-id="883e4-103">ImportTypes2 方法</span><span class="sxs-lookup"><span data-stu-id="883e4-103">ImportTypes2 Method</span></span>

<span data-ttu-id="883e4-104">启动类型的导入。</span><span class="sxs-lookup"><span data-stu-id="883e4-104">Initiates the import of types.</span></span> <span data-ttu-id="883e4-105">调用此方法以开始从通过 [ImportFile 方法](importfile-method.md)导入的每个范围导入类型。</span><span class="sxs-lookup"><span data-stu-id="883e4-105">Call this method to begin importing types from each scope imported via [ImportFile Method](importfile-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="883e4-106">语法</span><span class="sxs-lookup"><span data-stu-id="883e4-106">Syntax</span></span>  
  
```cpp  
HRESULT ImportTypes2(  
    mdAssembly AssemblyID,  
    mdToken FileToken,  
    DWORD dwScope,  
    HALINKENUM* phEnum,  
    IMetaDataImport2** ppImportScope,  
    DWORD* pdwCountOfTypes  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="883e4-107">参数</span><span class="sxs-lookup"><span data-stu-id="883e4-107">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="883e4-108">要导入的程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="883e4-108">ID of assembly into which to import.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="883e4-109">要从其导入的文件的 ID。</span><span class="sxs-lookup"><span data-stu-id="883e4-109">ID of file to from which to import.</span></span>  
  
 `dwScope`  
 <span data-ttu-id="883e4-110">要从中导入的从零开始的作用域。</span><span class="sxs-lookup"><span data-stu-id="883e4-110">Zero-based scope from which to import.</span></span>  
  
 `phEnum`  
 <span data-ttu-id="883e4-111">接收给定范围内的类型的枚举器句柄。</span><span class="sxs-lookup"><span data-stu-id="883e4-111">Receives enumerator handle for the types in the given scope.</span></span>  
  
 `ppImportScope`  
 <span data-ttu-id="883e4-112">可以选择接收 [IMetaDataImport2 接口](../metadata/imetadataimport2-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="883e4-112">Optionally receives [IMetaDataImport2 Interface](../metadata/imetadataimport2-interface.md) interface.</span></span>  
  
 `pdwCountOfTypes`  
 <span data-ttu-id="883e4-113">可以选择接收指定范围内的类型的计数。</span><span class="sxs-lookup"><span data-stu-id="883e4-113">Optionally receives count of types in the specified scope.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="883e4-114">返回值</span><span class="sxs-lookup"><span data-stu-id="883e4-114">Return Value</span></span>  

 <span data-ttu-id="883e4-115">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="883e4-115">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="883e4-116">要求</span><span class="sxs-lookup"><span data-stu-id="883e4-116">Requirements</span></span>  

 <span data-ttu-id="883e4-117">需要 alink</span><span class="sxs-lookup"><span data-stu-id="883e4-117">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="883e4-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="883e4-118">See also</span></span>

- [<span data-ttu-id="883e4-119">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="883e4-119">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="883e4-120">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="883e4-120">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="883e4-121">ALink API</span><span class="sxs-lookup"><span data-stu-id="883e4-121">ALink API</span></span>](index.md)
