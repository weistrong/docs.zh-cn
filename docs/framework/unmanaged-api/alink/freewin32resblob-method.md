---
description: 了解详细信息： FreeWin32ResBlob 方法
title: FreeWin32ResBlob 方法
ms.date: 03/30/2017
api_name:
- IALink.FreeWin32ResBlob
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- FreeWin32ResBlob
helpviewer_keywords:
- FreeWin32ResBlob method
ms.assetid: d941102b-2679-4c49-b15e-c0fc9c53e11f
topic_type:
- apiref
ms.openlocfilehash: 56c83632b623eec76e8e2d24030c79a8262f506f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637935"
---
# <a name="freewin32resblob-method"></a><span data-ttu-id="5bb7e-103">FreeWin32ResBlob 方法</span><span class="sxs-lookup"><span data-stu-id="5bb7e-103">FreeWin32ResBlob Method</span></span>

<span data-ttu-id="5bb7e-104">释放 Win32 资源 blob 和关联的资源。</span><span class="sxs-lookup"><span data-stu-id="5bb7e-104">Releases the Win32 resource blob and associated resources.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5bb7e-105">语法</span><span class="sxs-lookup"><span data-stu-id="5bb7e-105">Syntax</span></span>  
  
```cpp  
HRESULT FreeWin32ResBlob(  
    const void** ppResBlob  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="5bb7e-106">参数</span><span class="sxs-lookup"><span data-stu-id="5bb7e-106">Parameters</span></span>  

 `ppResBlob`  
 <span data-ttu-id="5bb7e-107">要释放的资源 blob。</span><span class="sxs-lookup"><span data-stu-id="5bb7e-107">The resource blob to be released.</span></span> <span data-ttu-id="5bb7e-108">此方法将 blob 指针赋给 NULL。</span><span class="sxs-lookup"><span data-stu-id="5bb7e-108">This method assigns the blob pointer to NULL.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5bb7e-109">返回值</span><span class="sxs-lookup"><span data-stu-id="5bb7e-109">Return Value</span></span>  

 <span data-ttu-id="5bb7e-110">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="5bb7e-110">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5bb7e-111">要求</span><span class="sxs-lookup"><span data-stu-id="5bb7e-111">Requirements</span></span>  

 <span data-ttu-id="5bb7e-112">需要 alink</span><span class="sxs-lookup"><span data-stu-id="5bb7e-112">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5bb7e-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="5bb7e-113">See also</span></span>

- [<span data-ttu-id="5bb7e-114">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="5bb7e-114">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="5bb7e-115">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="5bb7e-115">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="5bb7e-116">ALink API</span><span class="sxs-lookup"><span data-stu-id="5bb7e-116">ALink API</span></span>](index.md)
