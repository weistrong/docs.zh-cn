---
description: 了解详细信息： EnumCustomAttributes 方法
title: EnumCustomAttributes 方法
ms.date: 03/30/2017
api_name:
- EnumCustomAttributes
- IALink.EnumCustomAttributes
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EnumCustomAttributes
helpviewer_keywords:
- EnumCustomAttributes method
ms.assetid: 08dff60c-f01b-4050-8865-ea3f95361c9f
topic_type:
- apiref
ms.openlocfilehash: d5b537462745914903f0cdb1e9f4436f2c27a68d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638127"
---
# <a name="enumcustomattributes-method"></a><span data-ttu-id="d328c-103">EnumCustomAttributes 方法</span><span class="sxs-lookup"><span data-stu-id="d328c-103">EnumCustomAttributes Method</span></span>

<span data-ttu-id="d328c-104">检索程序集级别的自定义特性。</span><span class="sxs-lookup"><span data-stu-id="d328c-104">Retrieves assembly-level custom attributes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d328c-105">语法</span><span class="sxs-lookup"><span data-stu-id="d328c-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumCustomAttributes(  
    HALINKENUM hEnum,  
    mdToken tkType,  
    mdCustomAttribute rCustomValues[],  
    ULONG cMax,  
    ULONG* pcCustomValues  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="d328c-106">参数</span><span class="sxs-lookup"><span data-stu-id="d328c-106">Parameters</span></span>  

 `hEnum`  
 <span data-ttu-id="d328c-107">枚举器的句柄。</span><span class="sxs-lookup"><span data-stu-id="d328c-107">Handle of enumerator.</span></span>  
  
 `tkType`  
 <span data-ttu-id="d328c-108">要枚举的属性的类型。</span><span class="sxs-lookup"><span data-stu-id="d328c-108">Type of attributes to be enumerated.</span></span> <span data-ttu-id="d328c-109">用于 `mdTokenNill` 所有属性。</span><span class="sxs-lookup"><span data-stu-id="d328c-109">Use `mdTokenNill` for all attributes.</span></span>  
  
 `rCustomValues`  
 <span data-ttu-id="d328c-110">接收自定义特性标记。</span><span class="sxs-lookup"><span data-stu-id="d328c-110">Receives custom attributes tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="d328c-111">指定数组的大小 `rCustomValues` 。</span><span class="sxs-lookup"><span data-stu-id="d328c-111">Specifies size of `rCustomValues` array.</span></span>  
  
 `pcCustomValues`  
 <span data-ttu-id="d328c-112">可以选择接收令牌值的计数。</span><span class="sxs-lookup"><span data-stu-id="d328c-112">Optionally receives count of token values.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d328c-113">返回值</span><span class="sxs-lookup"><span data-stu-id="d328c-113">Return Value</span></span>  

 <span data-ttu-id="d328c-114">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="d328c-114">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d328c-115">要求</span><span class="sxs-lookup"><span data-stu-id="d328c-115">Requirements</span></span>  

 <span data-ttu-id="d328c-116">需要 alink</span><span class="sxs-lookup"><span data-stu-id="d328c-116">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d328c-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="d328c-117">See also</span></span>

- [<span data-ttu-id="d328c-118">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="d328c-118">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="d328c-119">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="d328c-119">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="d328c-120">ALink API</span><span class="sxs-lookup"><span data-stu-id="d328c-120">ALink API</span></span>](index.md)
