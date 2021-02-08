---
description: 了解详细信息： ISymUnmanagedDispose：:D estroy 方法
title: ISymUnmanagedDispose::Destroy 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDispose.Destroy
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDispose::Destroy
helpviewer_keywords:
- ISymUnmanagedDispose::Destroy method [.NET Framework debugging]
- Destroy method [.NET Framework debugging]
ms.assetid: a854ab9f-d2ba-470e-867f-808c1e7bd07a
topic_type:
- apiref
ms.openlocfilehash: 3c13f90e08f2ba0dd7c70acc3321913b14195f1c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790199"
---
# <a name="isymunmanageddisposedestroy-method"></a><span data-ttu-id="b5041-103">ISymUnmanagedDispose::Destroy 方法</span><span class="sxs-lookup"><span data-stu-id="b5041-103">ISymUnmanagedDispose::Destroy Method</span></span>

<span data-ttu-id="b5041-104">使基础对象释放所有内部引用，并在所有后续方法调用中返回失败。</span><span class="sxs-lookup"><span data-stu-id="b5041-104">Causes the underlying object to release all internal references and return failure on any subsequent method calls.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b5041-105">语法</span><span class="sxs-lookup"><span data-stu-id="b5041-105">Syntax</span></span>  
  
```cpp  
HRESULT Destroy();  
```  
  
## <a name="return-value"></a><span data-ttu-id="b5041-106">返回值</span><span class="sxs-lookup"><span data-stu-id="b5041-106">Return Value</span></span>  

 <span data-ttu-id="b5041-107">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="b5041-107">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b5041-108">要求</span><span class="sxs-lookup"><span data-stu-id="b5041-108">Requirements</span></span>  

 <span data-ttu-id="b5041-109">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="b5041-109">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b5041-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="b5041-110">See also</span></span>

- [<span data-ttu-id="b5041-111">ISymUnmanagedDispose 接口</span><span class="sxs-lookup"><span data-stu-id="b5041-111">ISymUnmanagedDispose Interface</span></span>](isymunmanageddispose-interface.md)
