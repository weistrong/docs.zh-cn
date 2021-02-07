---
description: 了解详细信息： GetScope 方法
title: GetScope 方法
ms.date: 03/30/2017
api_name:
- IALink.GetScope
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetScope
helpviewer_keywords:
- GetScope method
ms.assetid: e1555328-2c71-4ece-b357-9eb6d3a8efc4
topic_type:
- apiref
ms.openlocfilehash: cdebda457573e70755b49798ae86eae8f076216b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99718352"
---
# <a name="getscope-method"></a><span data-ttu-id="686c8-103">GetScope 方法</span><span class="sxs-lookup"><span data-stu-id="686c8-103">GetScope Method</span></span>

<span data-ttu-id="686c8-104">获取导入范围。</span><span class="sxs-lookup"><span data-stu-id="686c8-104">Gets an import scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="686c8-105">语法</span><span class="sxs-lookup"><span data-stu-id="686c8-105">Syntax</span></span>  
  
```cpp  
HRESULT GetScope(  
    mdAssembly AssemblyID,  
    mdToken FileToken,  
    DWORD dwScope,  
    IMetaDataImport** ppImportScope  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="686c8-106">参数</span><span class="sxs-lookup"><span data-stu-id="686c8-106">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="686c8-107">要导入到的程序集的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="686c8-107">Unique ID of assembly to import to.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="686c8-108">要从中导入的文件的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="686c8-108">Unique ID of the file to import from.</span></span>  
  
 `dwScope`  
 <span data-ttu-id="686c8-109">要导入的从零开始的范围。</span><span class="sxs-lookup"><span data-stu-id="686c8-109">Zero-based scope to import.</span></span>  
  
 `ppImportScope`  
 <span data-ttu-id="686c8-110">接收作用域的 [IMetaDataImport 接口](../metadata/imetadataimport-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="686c8-110">Receives [IMetaDataImport Interface](../metadata/imetadataimport-interface.md) interface for the scope.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="686c8-111">返回值</span><span class="sxs-lookup"><span data-stu-id="686c8-111">Return Value</span></span>  

 <span data-ttu-id="686c8-112">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="686c8-112">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="686c8-113">要求</span><span class="sxs-lookup"><span data-stu-id="686c8-113">Requirements</span></span>  

 <span data-ttu-id="686c8-114">需要 alink</span><span class="sxs-lookup"><span data-stu-id="686c8-114">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="686c8-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="686c8-115">See also</span></span>

- [<span data-ttu-id="686c8-116">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="686c8-116">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="686c8-117">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="686c8-117">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="686c8-118">ALink API</span><span class="sxs-lookup"><span data-stu-id="686c8-118">ALink API</span></span>](index.md)
