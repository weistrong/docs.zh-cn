---
description: 了解详细信息： ISymUnmanagedENCUpdate：： InitializeForEnc 方法
title: ISymUnmanagedENCUpdate::InitializeForEnc 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedENCUpdate.InitializeForEnc
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedENCUpdate::InitializeForEnc
helpviewer_keywords:
- ISymUnmanagedENCUpdate::InitializeForEnc method [.NET Framework debugging]
- InitializeForEnc method [.NET Framework debugging]
ms.assetid: 796b2154-b53c-4d07-9e67-80fd6064725a
topic_type:
- apiref
ms.openlocfilehash: 2b70554cc565f025dcf35e2a84523a5f9a6130f4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710096"
---
# <a name="isymunmanagedencupdateinitializeforenc-method"></a><span data-ttu-id="c465a-103">ISymUnmanagedENCUpdate::InitializeForEnc 方法</span><span class="sxs-lookup"><span data-stu-id="c465a-103">ISymUnmanagedENCUpdate::InitializeForEnc Method</span></span>

<span data-ttu-id="c465a-104">允许在首次调用 [ISymUnmanagedENCUpdate：： UpdateSymbolStore2](isymunmanagedencupdate-updatesymbolstore2-method.md) 方法之前计算方法边界。</span><span class="sxs-lookup"><span data-stu-id="c465a-104">Allows method boundaries to be computed before the first call to the [ISymUnmanagedENCUpdate::UpdateSymbolStore2](isymunmanagedencupdate-updatesymbolstore2-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c465a-105">语法</span><span class="sxs-lookup"><span data-stu-id="c465a-105">Syntax</span></span>  
  
```cpp  
HRESULT InitializeForEnc();  
```  
  
## <a name="return-value"></a><span data-ttu-id="c465a-106">返回值</span><span class="sxs-lookup"><span data-stu-id="c465a-106">Return Value</span></span>  

 <span data-ttu-id="c465a-107">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="c465a-107">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c465a-108">要求</span><span class="sxs-lookup"><span data-stu-id="c465a-108">Requirements</span></span>  

 <span data-ttu-id="c465a-109">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="c465a-109">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c465a-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="c465a-110">See also</span></span>

- [<span data-ttu-id="c465a-111">ISymUnmanagedENCUpdate 接口</span><span class="sxs-lookup"><span data-stu-id="c465a-111">ISymUnmanagedENCUpdate Interface</span></span>](isymunmanagedencupdate-interface.md)
