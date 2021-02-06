---
description: 了解详细信息： CloseAssembly 方法
title: CloseAssembly 方法
ms.date: 03/30/2017
api_name:
- IALink.CloseAssembly
- CloseAssembly
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- CloseAssembly
helpviewer_keywords:
- CloseAssembly method
ms.assetid: f66a43bc-a5c5-4190-acbe-63fd27640634
topic_type:
- apiref
ms.openlocfilehash: 927a66f948f691c00a695c626d9c31950a722cb5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638387"
---
# <a name="closeassembly-method"></a><span data-ttu-id="a9670-103">CloseAssembly 方法</span><span class="sxs-lookup"><span data-stu-id="a9670-103">CloseAssembly Method</span></span>

<span data-ttu-id="a9670-104">终结程序集操作。</span><span class="sxs-lookup"><span data-stu-id="a9670-104">Finalizes assembly operations.</span></span> <span data-ttu-id="a9670-105">在开始新的程序集或未绑定的模块之前，请调用此方法。</span><span class="sxs-lookup"><span data-stu-id="a9670-105">Call this method before beginning a new assembly or unbound module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a9670-106">语法</span><span class="sxs-lookup"><span data-stu-id="a9670-106">Syntax</span></span>  
  
```cpp  
HRESULT CloseAssembly(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="a9670-107">参数</span><span class="sxs-lookup"><span data-stu-id="a9670-107">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="a9670-108">程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="a9670-108">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a9670-109">返回值</span><span class="sxs-lookup"><span data-stu-id="a9670-109">Return Value</span></span>  

 <span data-ttu-id="a9670-110">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="a9670-110">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a9670-111">要求</span><span class="sxs-lookup"><span data-stu-id="a9670-111">Requirements</span></span>  

 <span data-ttu-id="a9670-112">需要 alink。</span><span class="sxs-lookup"><span data-stu-id="a9670-112">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a9670-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="a9670-113">See also</span></span>

- [<span data-ttu-id="a9670-114">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="a9670-114">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="a9670-115">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="a9670-115">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="a9670-116">ALink API</span><span class="sxs-lookup"><span data-stu-id="a9670-116">ALink API</span></span>](index.md)
