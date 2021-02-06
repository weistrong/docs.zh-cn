---
description: 了解详细信息： SetNonAssemblyFlags 方法
title: SetNonAssemblyFlags 方法
ms.date: 03/30/2017
api_name:
- IALink.SetNonAssemblyFlags
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- SetNonAssemblyFlags
helpviewer_keywords:
- SetNonAssemblyFlags method
ms.assetid: f8ba6fc8-f5aa-4066-ac96-56332758f5ec
topic_type:
- apiref
ms.openlocfilehash: 9cf311ec8f04f97da03be626e20c1c07065eac38
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662307"
---
# <a name="setnonassemblyflags-method"></a><span data-ttu-id="9a198-103">SetNonAssemblyFlags 方法</span><span class="sxs-lookup"><span data-stu-id="9a198-103">SetNonAssemblyFlags Method</span></span>

<span data-ttu-id="9a198-104">设置不是程序集特定的标志。</span><span class="sxs-lookup"><span data-stu-id="9a198-104">Sets flags that are not assembly-specific.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9a198-105">语法</span><span class="sxs-lookup"><span data-stu-id="9a198-105">Syntax</span></span>  
  
```cpp  
HRESULT SetNonAssemblyFlags(  
    AssemblyFlags afFlags  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="9a198-106">参数</span><span class="sxs-lookup"><span data-stu-id="9a198-106">Parameters</span></span>  

 `afFlags`  
 <span data-ttu-id="9a198-107">ALink 标志。</span><span class="sxs-lookup"><span data-stu-id="9a198-107">ALink flags.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9a198-108">返回值</span><span class="sxs-lookup"><span data-stu-id="9a198-108">Return Value</span></span>  

 <span data-ttu-id="9a198-109">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="9a198-109">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9a198-110">要求</span><span class="sxs-lookup"><span data-stu-id="9a198-110">Requirements</span></span>  

 <span data-ttu-id="9a198-111">需要 alink</span><span class="sxs-lookup"><span data-stu-id="9a198-111">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9a198-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="9a198-112">See also</span></span>

- [<span data-ttu-id="9a198-113">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="9a198-113">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="9a198-114">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="9a198-114">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="9a198-115">ALink API</span><span class="sxs-lookup"><span data-stu-id="9a198-115">ALink API</span></span>](index.md)
