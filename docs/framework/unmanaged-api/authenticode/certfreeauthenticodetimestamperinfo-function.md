---
description: 了解详细信息： CertFreeAuthenticodeTimestamperInfo 函数
title: CertFreeAuthenticodeTimestamperInfo 函数
ms.date: 03/30/2017
api_name:
- CertFreeAuthenticodeTimestamperInfo
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: 3eb14c49-68c2-4516-ac89-e5bd7473831c
topic_type:
- apiref
ms.openlocfilehash: 5234a90ea1d0272a7409b1b0b4def2160b77a513
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772934"
---
# <a name="certfreeauthenticodetimestamperinfo-function"></a><span data-ttu-id="8c1d7-103">CertFreeAuthenticodeTimestamperInfo 函数</span><span class="sxs-lookup"><span data-stu-id="8c1d7-103">CertFreeAuthenticodeTimestamperInfo Function</span></span>

<span data-ttu-id="8c1d7-104">释放为 [AXL_AUTHENTICODE_TIMESTAMPER_INFO](axl-authenticode-timestamper-info-structure.md) 结构分配的资源。</span><span class="sxs-lookup"><span data-stu-id="8c1d7-104">Frees resources allocated for the [AXL_AUTHENTICODE_TIMESTAMPER_INFO](axl-authenticode-timestamper-info-structure.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c1d7-105">语法</span><span class="sxs-lookup"><span data-stu-id="8c1d7-105">Syntax</span></span>

```cpp
HRESULT CertFreeAuthenticodeTimestamperInfo (
    [in, out]  PAXL_AUTHENTICODE_TIMESTAMPER_INFO   pTimestamperInfo
);
```

## <a name="parameters"></a><span data-ttu-id="8c1d7-106">参数</span><span class="sxs-lookup"><span data-stu-id="8c1d7-106">Parameters</span></span>

 `pTimestamperInfo`\
 <span data-ttu-id="8c1d7-107">[in, out] 要释放的时间戳签署人的信息。</span><span class="sxs-lookup"><span data-stu-id="8c1d7-107">[in, out] The time stamper information to be released.</span></span> <span data-ttu-id="8c1d7-108">请参阅 [AXL_AUTHENTICODE_TIMESTAMPER_INFO](axl-authenticode-timestamper-info-structure.md) 结构。</span><span class="sxs-lookup"><span data-stu-id="8c1d7-108">See the [AXL_AUTHENTICODE_TIMESTAMPER_INFO](axl-authenticode-timestamper-info-structure.md) structure.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c1d7-109">返回值</span><span class="sxs-lookup"><span data-stu-id="8c1d7-109">Return Value</span></span>

 <span data-ttu-id="8c1d7-110">如果此函数成功，则返回 `S_OK`。</span><span class="sxs-lookup"><span data-stu-id="8c1d7-110">`S_OK` if the function succeeds.</span></span> <span data-ttu-id="8c1d7-111">否则，返回错误代码。</span><span class="sxs-lookup"><span data-stu-id="8c1d7-111">Otherwise, returns an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c1d7-112">要求</span><span class="sxs-lookup"><span data-stu-id="8c1d7-112">Requirements</span></span>

<span data-ttu-id="8c1d7-113">**程序集**： clr.dll</span><span class="sxs-lookup"><span data-stu-id="8c1d7-113">**Assembly**: clr.dll</span></span>

## <a name="see-also"></a><span data-ttu-id="8c1d7-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="8c1d7-114">See also</span></span>

- [<span data-ttu-id="8c1d7-115">验证码</span><span class="sxs-lookup"><span data-stu-id="8c1d7-115">Authenticode</span></span>](index.md)
