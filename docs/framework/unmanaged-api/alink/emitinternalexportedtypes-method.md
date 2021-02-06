---
description: 了解详细信息： EmitInternalExportedTypes 方法
title: EmitInternalExportedTypes 方法
ms.date: 03/30/2017
api_name:
- EmitInternalExportedTypes
- IALink2.EmitInternalExportedTypes
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EmitInternalExportedTypes
helpviewer_keywords:
- EmitInternalExportedTypes method
ms.assetid: 28c8b00d-2c14-40b4-aed5-a1db0e2428eb
topic_type:
- apiref
ms.openlocfilehash: 5d23c593988b31c077d3b65b11b73113e164ed74
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638296"
---
# <a name="emitinternalexportedtypes-method"></a><span data-ttu-id="39c51-103">EmitInternalExportedTypes 方法</span><span class="sxs-lookup"><span data-stu-id="39c51-103">EmitInternalExportedTypes Method</span></span>

<span data-ttu-id="39c51-104">发出添加到程序集的类型。</span><span class="sxs-lookup"><span data-stu-id="39c51-104">Emits types added to the assembly.</span></span> <span data-ttu-id="39c51-105">添加已知的内部类型后，调用此方法。</span><span class="sxs-lookup"><span data-stu-id="39c51-105">Call this method after known internal types have been added.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="39c51-106">语法</span><span class="sxs-lookup"><span data-stu-id="39c51-106">Syntax</span></span>  
  
```cpp  
HRESULT EmitInternalExportedTypes(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="39c51-107">参数</span><span class="sxs-lookup"><span data-stu-id="39c51-107">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="39c51-108">程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="39c51-108">ID of assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="39c51-109">返回值</span><span class="sxs-lookup"><span data-stu-id="39c51-109">Return Value</span></span>  

 <span data-ttu-id="39c51-110">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="39c51-110">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="39c51-111">要求</span><span class="sxs-lookup"><span data-stu-id="39c51-111">Requirements</span></span>  

 <span data-ttu-id="39c51-112">需要 alink</span><span class="sxs-lookup"><span data-stu-id="39c51-112">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="39c51-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="39c51-113">See also</span></span>

- [<span data-ttu-id="39c51-114">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="39c51-114">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="39c51-115">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="39c51-115">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="39c51-116">ALink API</span><span class="sxs-lookup"><span data-stu-id="39c51-116">ALink API</span></span>](index.md)
