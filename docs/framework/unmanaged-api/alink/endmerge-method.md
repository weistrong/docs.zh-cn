---
description: 了解详细信息： EndMerge 方法
title: EndMerge 方法
ms.date: 03/30/2017
api_name:
- IALink.EndMerge
- EndMerge
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EndMerge
helpviewer_keywords:
- EndMerge method
ms.assetid: 1d03bb15-a2c8-4a04-8fc6-b126c89c3778
topic_type:
- apiref
ms.openlocfilehash: aac23d6d87f3fe74c1094bdd4a7f9c9f7f3fa7cc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638153"
---
# <a name="endmerge-method"></a><span data-ttu-id="5c4f4-103">EndMerge 方法</span><span class="sxs-lookup"><span data-stu-id="5c4f4-103">EndMerge Method</span></span>

<span data-ttu-id="5c4f4-104">指示所有自定义特性都已合并到发出范围中。</span><span class="sxs-lookup"><span data-stu-id="5c4f4-104">Indicates that all custom attributes have been merged into the emit scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5c4f4-105">语法</span><span class="sxs-lookup"><span data-stu-id="5c4f4-105">Syntax</span></span>  
  
```cpp  
HRESULT EndMerge(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="5c4f4-106">参数</span><span class="sxs-lookup"><span data-stu-id="5c4f4-106">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="5c4f4-107">程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="5c4f4-107">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5c4f4-108">返回值</span><span class="sxs-lookup"><span data-stu-id="5c4f4-108">Return Value</span></span>  

 <span data-ttu-id="5c4f4-109">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="5c4f4-109">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5c4f4-110">要求</span><span class="sxs-lookup"><span data-stu-id="5c4f4-110">Requirements</span></span>  

 <span data-ttu-id="5c4f4-111">需要 alink</span><span class="sxs-lookup"><span data-stu-id="5c4f4-111">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5c4f4-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="5c4f4-112">See also</span></span>

- [<span data-ttu-id="5c4f4-113">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="5c4f4-113">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="5c4f4-114">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="5c4f4-114">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="5c4f4-115">ALink API</span><span class="sxs-lookup"><span data-stu-id="5c4f4-115">ALink API</span></span>](index.md)
