---
description: 了解详细信息： ExportType 方法
title: ExportType 方法
ms.date: 03/30/2017
api_name:
- IALink.ExportType
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ExportType
helpviewer_keywords:
- ExportType method
ms.assetid: 91a7ce63-f5b8-4f16-b2c4-e1d0baa88944
topic_type:
- apiref
ms.openlocfilehash: 6dc047cac3b80e6fe7a6f2cd980061b34bb7f286
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638062"
---
# <a name="exporttype-method"></a><span data-ttu-id="c5f74-103">ExportType 方法</span><span class="sxs-lookup"><span data-stu-id="c5f74-103">ExportType Method</span></span>

<span data-ttu-id="c5f74-104">指定类型可导出。</span><span class="sxs-lookup"><span data-stu-id="c5f74-104">Specifies that a type is exportable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c5f74-105">语法</span><span class="sxs-lookup"><span data-stu-id="c5f74-105">Syntax</span></span>  
  
```cpp  
HRESULT ExportType(  
    mdAssembly      AssemblyID,  
    mdToken         FileToken,  
    mdTypeDef       TypeToken,  
    LPCWSTR         pszTypename,  
    DWORD           dwFlags,  
    mdExportedType* pType  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="c5f74-106">参数</span><span class="sxs-lookup"><span data-stu-id="c5f74-106">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="c5f74-107">要从中导出的程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="c5f74-107">ID of the assembly to export from.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="c5f74-108">定义可导出类型的文件的文件标记或程序集 ID。</span><span class="sxs-lookup"><span data-stu-id="c5f74-108">File token or assembly ID of file that defines the exportable type.</span></span>  
  
 `TypeToken`  
 <span data-ttu-id="c5f74-109">要使其可导出的类型的标记。</span><span class="sxs-lookup"><span data-stu-id="c5f74-109">Token of type to be made exportable.</span></span>  
  
 `pszTypename`  
 <span data-ttu-id="c5f74-110">要使其可导出的完全限定的类型名称。</span><span class="sxs-lookup"><span data-stu-id="c5f74-110">Fully qualified type name to be made exportable.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="c5f74-111">`ComType` 标志，如 `tdPublic` 或 `tdNested` 。</span><span class="sxs-lookup"><span data-stu-id="c5f74-111">`ComType` flags such as `tdPublic` or `tdNested`.</span></span> <span data-ttu-id="c5f74-112">此参数可传递给 [DefineExportedType 方法](../metadata/imetadataassemblyemit-defineexportedtype-method.md)。</span><span class="sxs-lookup"><span data-stu-id="c5f74-112">This parameter may be passed to [DefineExportedType Method](../metadata/imetadataassemblyemit-defineexportedtype-method.md).</span></span>  
  
 `pType`  
 <span data-ttu-id="c5f74-113">接收导出类型的令牌。</span><span class="sxs-lookup"><span data-stu-id="c5f74-113">Receives token for exported type.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c5f74-114">返回值</span><span class="sxs-lookup"><span data-stu-id="c5f74-114">Return Value</span></span>  

 <span data-ttu-id="c5f74-115">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="c5f74-115">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c5f74-116">要求</span><span class="sxs-lookup"><span data-stu-id="c5f74-116">Requirements</span></span>  

 <span data-ttu-id="c5f74-117">需要 alink</span><span class="sxs-lookup"><span data-stu-id="c5f74-117">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c5f74-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="c5f74-118">See also</span></span>

- [<span data-ttu-id="c5f74-119">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="c5f74-119">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="c5f74-120">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="c5f74-120">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="c5f74-121">ALink API</span><span class="sxs-lookup"><span data-stu-id="c5f74-121">ALink API</span></span>](index.md)
