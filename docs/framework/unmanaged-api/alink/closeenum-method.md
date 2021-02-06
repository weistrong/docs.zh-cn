---
description: 了解详细信息： CloseEnum 方法
title: CloseEnum 方法
ms.date: 03/30/2017
api_name:
- CloseEnum
- IALink.CloseEnum
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- CloseEnum
helpviewer_keywords:
- CloseEnum method
ms.assetid: aa4a091e-13fe-4264-91de-e12f1c767c87
topic_type:
- apiref
ms.openlocfilehash: 700c54de5af2e5c0be6940d4045019092655d46f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638374"
---
# <a name="closeenum-method"></a><span data-ttu-id="a6748-103">CloseEnum 方法</span><span class="sxs-lookup"><span data-stu-id="a6748-103">CloseEnum Method</span></span>

<span data-ttu-id="a6748-104">关闭所指示的枚举并释放关联的资源。</span><span class="sxs-lookup"><span data-stu-id="a6748-104">Closes the indicated enumeration and frees associated resources.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a6748-105">语法</span><span class="sxs-lookup"><span data-stu-id="a6748-105">Syntax</span></span>  
  
```cpp  
HRESULT CloseEnum(  
    HALINKENUM hEnum  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="a6748-106">参数</span><span class="sxs-lookup"><span data-stu-id="a6748-106">Parameters</span></span>  

 `hEnum`  
 <span data-ttu-id="a6748-107">要关闭的枚举的句柄。</span><span class="sxs-lookup"><span data-stu-id="a6748-107">Handle of enumeration to be closed.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a6748-108">返回值</span><span class="sxs-lookup"><span data-stu-id="a6748-108">Return Value</span></span>  

 <span data-ttu-id="a6748-109">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="a6748-109">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a6748-110">要求</span><span class="sxs-lookup"><span data-stu-id="a6748-110">Requirements</span></span>  

 <span data-ttu-id="a6748-111">需要 alink</span><span class="sxs-lookup"><span data-stu-id="a6748-111">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a6748-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="a6748-112">See also</span></span>

- [<span data-ttu-id="a6748-113">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="a6748-113">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="a6748-114">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="a6748-114">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="a6748-115">ALink API</span><span class="sxs-lookup"><span data-stu-id="a6748-115">ALink API</span></span>](index.md)
