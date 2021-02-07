---
description: 了解详细信息： ISymUnmanagedWriter3：： Commit 方法
title: ISymUnmanagedWriter3::Commit 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter3.Commit
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter3::Commit
helpviewer_keywords:
- Commit method, ISymUnmanagedWriter3 interface [.NET Framework debugging]
- ISymUnmanagedWriter3::Commit method [.NET Framework debugging]
ms.assetid: f6961922-46ec-4d2c-8369-85f880731f37
topic_type:
- apiref
ms.openlocfilehash: 308f5d3a16cf60a0e77a581a318d6fd6c398b3f3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761754"
---
# <a name="isymunmanagedwriter3commit-method"></a><span data-ttu-id="1d90f-103">ISymUnmanagedWriter3::Commit 方法</span><span class="sxs-lookup"><span data-stu-id="1d90f-103">ISymUnmanagedWriter3::Commit Method</span></span>

<span data-ttu-id="1d90f-104">将迄今为止写入的更改提交到流。</span><span class="sxs-lookup"><span data-stu-id="1d90f-104">Commits the changes written so far to the stream.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1d90f-105">语法</span><span class="sxs-lookup"><span data-stu-id="1d90f-105">Syntax</span></span>  
  
```cpp  
HRESULT Commit();  
```  
  
## <a name="return-value"></a><span data-ttu-id="1d90f-106">返回值</span><span class="sxs-lookup"><span data-stu-id="1d90f-106">Return Value</span></span>  

 <span data-ttu-id="1d90f-107">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="1d90f-107">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1d90f-108">要求</span><span class="sxs-lookup"><span data-stu-id="1d90f-108">Requirements</span></span>  

 <span data-ttu-id="1d90f-109">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="1d90f-109">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1d90f-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="1d90f-110">See also</span></span>

- [<span data-ttu-id="1d90f-111">ISymUnmanagedWriter3 接口</span><span class="sxs-lookup"><span data-stu-id="1d90f-111">ISymUnmanagedWriter3 Interface</span></span>](isymunmanagedwriter3-interface.md)
