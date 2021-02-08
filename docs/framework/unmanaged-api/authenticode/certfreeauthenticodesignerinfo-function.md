---
description: 了解详细信息： CertFreeAuthenticodeSignerInfo 函数
title: CertFreeAuthenticodeSignerInfo 函数
ms.date: 03/30/2017
api_name:
- CertFreeAuthenticodeSignerInfo
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: 8029633c-b6e4-4665-a7c2-89607c3247ef
topic_type:
- apiref
ms.openlocfilehash: 6e8a97e8fee37d885c7d32102ed8cc7654992223
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772973"
---
# <a name="certfreeauthenticodesignerinfo-function"></a><span data-ttu-id="2b3b9-103">CertFreeAuthenticodeSignerInfo 函数</span><span class="sxs-lookup"><span data-stu-id="2b3b9-103">CertFreeAuthenticodeSignerInfo Function</span></span>

<span data-ttu-id="2b3b9-104">释放为 [AXL_AUTHENTICODE_SIGNER_INFO](axl-authenticode-signer-info-structure.md) 结构分配的资源。</span><span class="sxs-lookup"><span data-stu-id="2b3b9-104">Frees resources allocated for the [AXL_AUTHENTICODE_SIGNER_INFO](axl-authenticode-signer-info-structure.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b3b9-105">语法</span><span class="sxs-lookup"><span data-stu-id="2b3b9-105">Syntax</span></span>

```cpp
HRESULT CertFreeAuthenticodeSignerInfo (
    [in, out]  PAXL_AUTHENTICODE_SIGNER_INFO   pSignerInfo);
```

## <a name="parameters"></a><span data-ttu-id="2b3b9-106">参数</span><span class="sxs-lookup"><span data-stu-id="2b3b9-106">Parameters</span></span>

 `pSignerInfo`\
 <span data-ttu-id="2b3b9-107">[in, out] 要释放的签署人信息。</span><span class="sxs-lookup"><span data-stu-id="2b3b9-107">[in, out] Signer information to be released.</span></span> <span data-ttu-id="2b3b9-108">请参阅 [AXL_AUTHENTICODE_SIGNER_INFO](axl-authenticode-signer-info-structure.md) 结构。</span><span class="sxs-lookup"><span data-stu-id="2b3b9-108">See the [AXL_AUTHENTICODE_SIGNER_INFO](axl-authenticode-signer-info-structure.md) structure.</span></span>

## <a name="return-value"></a><span data-ttu-id="2b3b9-109">返回值</span><span class="sxs-lookup"><span data-stu-id="2b3b9-109">Return Value</span></span>

 <span data-ttu-id="2b3b9-110">如果此函数成功，则返回 `S_OK`。</span><span class="sxs-lookup"><span data-stu-id="2b3b9-110">`S_OK` if the function succeeds.</span></span> <span data-ttu-id="2b3b9-111">否则，返回错误代码。</span><span class="sxs-lookup"><span data-stu-id="2b3b9-111">Otherwise, returns an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b3b9-112">要求</span><span class="sxs-lookup"><span data-stu-id="2b3b9-112">Requirements</span></span>

<span data-ttu-id="2b3b9-113">**程序集**： clr.dll</span><span class="sxs-lookup"><span data-stu-id="2b3b9-113">**Assembly**: clr.dll</span></span>

## <a name="see-also"></a><span data-ttu-id="2b3b9-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="2b3b9-114">See also</span></span>

- [<span data-ttu-id="2b3b9-115">验证码</span><span class="sxs-lookup"><span data-stu-id="2b3b9-115">Authenticode</span></span>](index.md)
