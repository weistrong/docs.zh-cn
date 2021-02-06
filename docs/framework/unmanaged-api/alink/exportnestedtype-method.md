---
description: 了解详细信息： ExportNestedType 方法
title: ExportNestedType 方法
ms.date: 03/30/2017
api_name:
- IALink.ExportNestedType
- ExportNestedType
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ExportNestedType
helpviewer_keywords:
- ExportNestedType method
ms.assetid: dec7df60-4d30-47c8-99db-72e0419e5f76
topic_type:
- apiref
ms.openlocfilehash: 66cf4c3572857a0e7e99efa966cdb0b9ae2be673
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638135"
---
# <a name="exportnestedtype-method"></a><span data-ttu-id="e73aa-103">ExportNestedType 方法</span><span class="sxs-lookup"><span data-stu-id="e73aa-103">ExportNestedType Method</span></span>

<span data-ttu-id="e73aa-104">指定嵌套类型为可导出。</span><span class="sxs-lookup"><span data-stu-id="e73aa-104">Specifies nested types as exportable.</span></span> <span data-ttu-id="e73aa-105">[ExportType 方法](exporttype-method.md)还可以导出嵌套类型，但此方法的速度更快。</span><span class="sxs-lookup"><span data-stu-id="e73aa-105">The [ExportType Method](exporttype-method.md) can also export nested types, but this method is faster.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e73aa-106">语法</span><span class="sxs-lookup"><span data-stu-id="e73aa-106">Syntax</span></span>  
  
```cpp  
HRESULT ExportNestedType(  
    mdAssembly      AssemblyID,  
    mdToken         FileToken,  
    mdTypeDef       TypeToken,  
    mdExportedType  ParentType,  
    LPCWSTR         pszTypename,  
    DWORD           dwFlags,  
    mdExportedType* pType  
) PURE;
```  
  
## <a name="parameters"></a><span data-ttu-id="e73aa-107">参数</span><span class="sxs-lookup"><span data-stu-id="e73aa-107">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="e73aa-108">要从中导出的程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="e73aa-108">ID of assembly to export from.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="e73aa-109">定义要导出的类型的文件标记或文件的程序集。</span><span class="sxs-lookup"><span data-stu-id="e73aa-109">File token or Assembly of file that defines the type to be made exportable.</span></span>  
  
 `TypeToken`  
 <span data-ttu-id="e73aa-110">要使其可导出的类型的类型标记。</span><span class="sxs-lookup"><span data-stu-id="e73aa-110">Type token of type to be made exportable.</span></span>  
  
 `ParentType`  
 <span data-ttu-id="e73aa-111">父类型的标记。</span><span class="sxs-lookup"><span data-stu-id="e73aa-111">Token of parent type.</span></span>  
  
 `pszTypename`  
 <span data-ttu-id="e73aa-112">要导出的完全限定的类型名称。</span><span class="sxs-lookup"><span data-stu-id="e73aa-112">Fully qualified type name to export.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="e73aa-113">`ComType` 标志，如 `tdPublic` 或 `tdNested` 。</span><span class="sxs-lookup"><span data-stu-id="e73aa-113">`ComType` flags such as `tdPublic` or `tdNested`.</span></span> <span data-ttu-id="e73aa-114">此值可传递给 [DefineExportedType 方法](../metadata/imetadataassemblyemit-defineexportedtype-method.md)。</span><span class="sxs-lookup"><span data-stu-id="e73aa-114">This value may be passed to [DefineExportedType Method](../metadata/imetadataassemblyemit-defineexportedtype-method.md).</span></span>  
  
 `pType`  
 <span data-ttu-id="e73aa-115">接收导出类型的令牌。</span><span class="sxs-lookup"><span data-stu-id="e73aa-115">Receives token for exported type.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e73aa-116">返回值</span><span class="sxs-lookup"><span data-stu-id="e73aa-116">Return Value</span></span>  

 <span data-ttu-id="e73aa-117">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="e73aa-117">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e73aa-118">要求</span><span class="sxs-lookup"><span data-stu-id="e73aa-118">Requirements</span></span>  

 <span data-ttu-id="e73aa-119">需要 alink</span><span class="sxs-lookup"><span data-stu-id="e73aa-119">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e73aa-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="e73aa-120">See also</span></span>

- [<span data-ttu-id="e73aa-121">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="e73aa-121">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="e73aa-122">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="e73aa-122">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="e73aa-123">ALink API</span><span class="sxs-lookup"><span data-stu-id="e73aa-123">ALink API</span></span>](index.md)
