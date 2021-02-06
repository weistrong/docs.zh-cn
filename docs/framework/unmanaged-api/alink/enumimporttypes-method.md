---
description: 了解详细信息： EnumImportTypes 方法
title: EnumImportTypes 方法
ms.date: 03/30/2017
api_name:
- EnumImportTypes
- IALink.EnumImportTypes
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EnumImportTypes
helpviewer_keywords:
- EnumImportTypes method
ms.assetid: 83a0e4e7-ec06-40cb-9b63-700b9695bb04
topic_type:
- apiref
ms.openlocfilehash: 39570740f3560f5bfef8ba80b95c0eb2aca41f59
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638114"
---
# <a name="enumimporttypes-method"></a><span data-ttu-id="85182-103">EnumImportTypes 方法</span><span class="sxs-lookup"><span data-stu-id="85182-103">EnumImportTypes Method</span></span>

<span data-ttu-id="85182-104">枚举每个范围中的每个类型。</span><span class="sxs-lookup"><span data-stu-id="85182-104">Enumerates each type in each scope.</span></span>

## <a name="syntax"></a><span data-ttu-id="85182-105">语法</span><span class="sxs-lookup"><span data-stu-id="85182-105">Syntax</span></span>

```cpp
HRESULT EnumImportTypes(
    HALINKENUM   hEnum,
    DWORD        dwMax,
    mdTypeDef    aTypeDefs[],
    DWORD*       pdwCount
) PURE;
```

## <a name="parameters"></a><span data-ttu-id="85182-106">参数</span><span class="sxs-lookup"><span data-stu-id="85182-106">Parameters</span></span>

`hEnum`\
<span data-ttu-id="85182-107">枚举器的句柄。</span><span class="sxs-lookup"><span data-stu-id="85182-107">Handle for enumerator.</span></span>

`dwMax`\
<span data-ttu-id="85182-108">要检索的类型的最大数目。</span><span class="sxs-lookup"><span data-stu-id="85182-108">Maximum number of types to retrieve.</span></span>

`aTypeDefs`\
<span data-ttu-id="85182-109">接收类型标记，而不是超出 `dwMax` 。</span><span class="sxs-lookup"><span data-stu-id="85182-109">Receives type tokens, not to exceed `dwMax`.</span></span>

`pdwCount`\
<span data-ttu-id="85182-110">接收中类型的实际数量 `aTypeDefs` 。</span><span class="sxs-lookup"><span data-stu-id="85182-110">Receives actual number of type in `aTypeDefs`.</span></span>

## <a name="return-value"></a><span data-ttu-id="85182-111">返回值</span><span class="sxs-lookup"><span data-stu-id="85182-111">Return Value</span></span>

<span data-ttu-id="85182-112">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="85182-112">Returns S_OK if the method succeeds.</span></span>

## <a name="requirements"></a><span data-ttu-id="85182-113">要求</span><span class="sxs-lookup"><span data-stu-id="85182-113">Requirements</span></span>

<span data-ttu-id="85182-114">需要 alink</span><span class="sxs-lookup"><span data-stu-id="85182-114">Requires alink.h</span></span>

## <a name="see-also"></a><span data-ttu-id="85182-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="85182-115">See also</span></span>

- [<span data-ttu-id="85182-116">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="85182-116">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="85182-117">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="85182-117">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="85182-118">ALink API</span><span class="sxs-lookup"><span data-stu-id="85182-118">ALink API</span></span>](index.md)
