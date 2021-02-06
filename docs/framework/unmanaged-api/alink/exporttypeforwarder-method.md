---
description: 了解详细信息： ExportTypeForwarder 方法
title: ExportTypeForwarder 方法
ms.date: 03/30/2017
api_name:
- IALink.ExportTypeForwarder
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ExportTypeForwarder
helpviewer_keywords:
- ExportTypeForwarder method
ms.assetid: 55989fa9-ab43-4f08-8eb6-2eb56fa7ca76
topic_type:
- apiref
ms.openlocfilehash: 59fb74c83f6d30dda87d908353795fb218190022
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637984"
---
# <a name="exporttypeforwarder-method"></a><span data-ttu-id="f2fc5-103">ExportTypeForwarder 方法</span><span class="sxs-lookup"><span data-stu-id="f2fc5-103">ExportTypeForwarder Method</span></span>

<span data-ttu-id="f2fc5-104">将类型转发器添加到给定程序集的类型表。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-104">Adds a type forwarder to the type table of the given assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f2fc5-105">语法</span><span class="sxs-lookup"><span data-stu-id="f2fc5-105">Syntax</span></span>  
  
```cpp  
HRESULT ExportTypeForwarder(  
    mdAssemblyRef   tkAssemblyRef,  
    LPCWSTR         pszTypename,  
    DWORD           dwFlags,  
    mdExportedType* pType  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="f2fc5-106">参数</span><span class="sxs-lookup"><span data-stu-id="f2fc5-106">Parameters</span></span>  

 `tkAssemblyRef`  
 <span data-ttu-id="f2fc5-107">对类型转发器所引用的程序集的引用。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-107">Reference to the assembly to which the type forwarder refers.</span></span>  
  
 `pszTypename`  
 <span data-ttu-id="f2fc5-108">要导出的完全限定的类型名称。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-108">Fully qualified type name to export.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="f2fc5-109">`ComType` 标志，如 `tdPublic` 或 `tdNested` 。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-109">`ComType` flags such as `tdPublic` or `tdNested`.</span></span> <span data-ttu-id="f2fc5-110">此值可传递给 [DefineExportedType 方法](../metadata/imetadataassemblyemit-defineexportedtype-method.md)。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-110">This value may be passed to [DefineExportedType Method](../metadata/imetadataassemblyemit-defineexportedtype-method.md).</span></span>  
  
 `pType`  
 <span data-ttu-id="f2fc5-111">接收导出类型的标记。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-111">Receives the token of the exported type.</span></span> <span data-ttu-id="f2fc5-112">这仅适用于发出嵌套类型。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-112">This is necessary only for emitting nested types.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f2fc5-113">返回值</span><span class="sxs-lookup"><span data-stu-id="f2fc5-113">Return Value</span></span>  

 <span data-ttu-id="f2fc5-114">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-114">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f2fc5-115">要求</span><span class="sxs-lookup"><span data-stu-id="f2fc5-115">Requirements</span></span>  

 <span data-ttu-id="f2fc5-116">需要 alink</span><span class="sxs-lookup"><span data-stu-id="f2fc5-116">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2fc5-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="f2fc5-117">See also</span></span>

- [<span data-ttu-id="f2fc5-118">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="f2fc5-118">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="f2fc5-119">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="f2fc5-119">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="f2fc5-120">ALink API</span><span class="sxs-lookup"><span data-stu-id="f2fc5-120">ALink API</span></span>](index.md)
