---
description: 了解详细信息： ISymUnmanagedDispose 接口
title: ISymUnmanagedDispose 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDispose
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDispose
helpviewer_keywords:
- ISymUnmanagedDispose interface [.NET Framework debugging]
ms.assetid: b1d74e83-a200-4d00-8fbd-27918808616d
topic_type:
- apiref
ms.openlocfilehash: a94a8e8e462b5031cac3f0a8702a5685f993910d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790173"
---
# <a name="isymunmanageddispose-interface"></a><span data-ttu-id="5389e-103">ISymUnmanagedDispose 接口</span><span class="sxs-lookup"><span data-stu-id="5389e-103">ISymUnmanagedDispose Interface</span></span>

<span data-ttu-id="5389e-104">释放非托管资源。</span><span class="sxs-lookup"><span data-stu-id="5389e-104">Disposes of unmanaged resources.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="5389e-105">方法</span><span class="sxs-lookup"><span data-stu-id="5389e-105">Methods</span></span>  
  
|<span data-ttu-id="5389e-106">方法</span><span class="sxs-lookup"><span data-stu-id="5389e-106">Method</span></span>|<span data-ttu-id="5389e-107">说明</span><span class="sxs-lookup"><span data-stu-id="5389e-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="5389e-108">Destroy 方法</span><span class="sxs-lookup"><span data-stu-id="5389e-108">Destroy Method</span></span>](isymunmanageddispose-destroy-method.md)|<span data-ttu-id="5389e-109">使基础对象释放所有内部引用，并在所有后续方法调用中返回失败。</span><span class="sxs-lookup"><span data-stu-id="5389e-109">Causes the underlying object to release all internal references and return failure on any subsequent method calls.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5389e-110">要求</span><span class="sxs-lookup"><span data-stu-id="5389e-110">Requirements</span></span>  

 <span data-ttu-id="5389e-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="5389e-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5389e-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="5389e-112">See also</span></span>

- [<span data-ttu-id="5389e-113">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="5389e-113">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
