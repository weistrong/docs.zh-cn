---
description: 了解详细信息： GetAssemblyRefHash 方法
title: GetAssemblyRefHash 方法
ms.date: 03/30/2017
api_name:
- IALink.GetAssemblyRefHash
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetAssemblyRefHash
helpviewer_keywords:
- GetAssemblyRefHash method
ms.assetid: 091a18bd-e901-46f6-b999-74d71c8a7c41
topic_type:
- apiref
ms.openlocfilehash: d8222d2fdd2c05ca1a23f881989dc344ba294bc1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99718468"
---
# <a name="getassemblyrefhash-method"></a><span data-ttu-id="66f51-103">GetAssemblyRefHash 方法</span><span class="sxs-lookup"><span data-stu-id="66f51-103">GetAssemblyRefHash Method</span></span>

<span data-ttu-id="66f51-104">检索给定程序集的哈希 blob。</span><span class="sxs-lookup"><span data-stu-id="66f51-104">Retrieves a hash blob for a given assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="66f51-105">语法</span><span class="sxs-lookup"><span data-stu-id="66f51-105">Syntax</span></span>  
  
```cpp  
HRESULT GetAssemblyRefHash(  
    mdToken FileToken,  
    const void** ppvHash,  
    DWORD* pcbHash  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="66f51-106">参数</span><span class="sxs-lookup"><span data-stu-id="66f51-106">Parameters</span></span>  

 `FileToken`  
 <span data-ttu-id="66f51-107">哈希将引用的程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="66f51-107">ID of assembly to which the hash will refer.</span></span>  
  
 `ppvHash`  
 <span data-ttu-id="66f51-108">接收生成的哈希 blob。</span><span class="sxs-lookup"><span data-stu-id="66f51-108">Receives the resulting hash blob.</span></span>  
  
 `pcbHash`  
 <span data-ttu-id="66f51-109">接收哈希 blob 的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="66f51-109">Receives size, in bytes, of hash blob.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="66f51-110">返回值</span><span class="sxs-lookup"><span data-stu-id="66f51-110">Return Value</span></span>  

 <span data-ttu-id="66f51-111">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="66f51-111">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="66f51-112">要求</span><span class="sxs-lookup"><span data-stu-id="66f51-112">Requirements</span></span>  

 <span data-ttu-id="66f51-113">需要 alink</span><span class="sxs-lookup"><span data-stu-id="66f51-113">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="66f51-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="66f51-114">See also</span></span>

- [<span data-ttu-id="66f51-115">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="66f51-115">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="66f51-116">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="66f51-116">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="66f51-117">ALink API</span><span class="sxs-lookup"><span data-stu-id="66f51-117">ALink API</span></span>](index.md)
