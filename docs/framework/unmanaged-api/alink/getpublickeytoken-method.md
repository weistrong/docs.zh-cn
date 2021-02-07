---
description: 了解详细信息： GetPublicKeyToken 方法
title: GetPublicKeyToken 方法
ms.date: 03/30/2017
api_name:
- IALink2.GetPublicKeyToken
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetPublicKeyToken
helpviewer_keywords:
- GetPublicKeyToken method
ms.assetid: 4a16374c-94b0-47b0-9fed-88c2b0cdccd4
topic_type:
- apiref
ms.openlocfilehash: b864c1dc61c7498ccca6aa04ef29b57a30e1a9ea
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99718416"
---
# <a name="getpublickeytoken-method"></a><span data-ttu-id="d43cf-103">GetPublicKeyToken 方法</span><span class="sxs-lookup"><span data-stu-id="d43cf-103">GetPublicKeyToken Method</span></span>

<span data-ttu-id="d43cf-104">检索给定 keyfile 或 key 容器的公钥标记。</span><span class="sxs-lookup"><span data-stu-id="d43cf-104">Retrieves the public key token for a given keyfile or key container.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d43cf-105">语法</span><span class="sxs-lookup"><span data-stu-id="d43cf-105">Syntax</span></span>  
  
```cpp  
HRESULT GetPublicKeyToken(  
    LPCWSTR pszKeyFile,  
    LPCWSTR pszKeyContainer,  
    void* pvPublicKeyToken,  
    DWORD* pcbPublicKeyToken  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="d43cf-106">参数</span><span class="sxs-lookup"><span data-stu-id="d43cf-106">Parameters</span></span>  

 `pszKeyFile`  
 <span data-ttu-id="d43cf-107">密钥的文件名。</span><span class="sxs-lookup"><span data-stu-id="d43cf-107">Filename of the key.</span></span>  
  
 `pszKeyContainer`  
 <span data-ttu-id="d43cf-108">密钥容器的名称。</span><span class="sxs-lookup"><span data-stu-id="d43cf-108">Name of the key container.</span></span>  
  
 `pvPublicKeyToken`  
 <span data-ttu-id="d43cf-109">要存储密钥标记的地址。</span><span class="sxs-lookup"><span data-stu-id="d43cf-109">Address where key token is to be stored.</span></span>  
  
 `pcbPublicKeyToken`  
 <span data-ttu-id="d43cf-110">指定指定的缓冲区的大小（以字节为单位） `pvPublicKeyToken` 。</span><span class="sxs-lookup"><span data-stu-id="d43cf-110">Specifies the size, in bytes, of the buffer indicated by `pvPublicKeyToken`.</span></span> <span data-ttu-id="d43cf-111">返回时，包含所使用的实际字节数。</span><span class="sxs-lookup"><span data-stu-id="d43cf-111">Upon return, contains actual number of bytes used.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d43cf-112">返回值</span><span class="sxs-lookup"><span data-stu-id="d43cf-112">Return Value</span></span>  

 <span data-ttu-id="d43cf-113">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="d43cf-113">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d43cf-114">要求</span><span class="sxs-lookup"><span data-stu-id="d43cf-114">Requirements</span></span>  

 <span data-ttu-id="d43cf-115">需要 alink。</span><span class="sxs-lookup"><span data-stu-id="d43cf-115">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d43cf-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="d43cf-116">See also</span></span>

- [<span data-ttu-id="d43cf-117">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="d43cf-117">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="d43cf-118">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="d43cf-118">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="d43cf-119">ALink API</span><span class="sxs-lookup"><span data-stu-id="d43cf-119">ALink API</span></span>](index.md)
