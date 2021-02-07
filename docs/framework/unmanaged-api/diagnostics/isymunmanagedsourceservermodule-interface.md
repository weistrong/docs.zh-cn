---
description: 了解详细信息： ISymUnmanagedSourceServerModule 接口
title: ISymUnmanagedSourceServerModule 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedSourceServerModule
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedSourceServerModule
helpviewer_keywords:
- ISymUnmanagedSourceServerModule interface [.NET Framework debugging]
ms.assetid: a19b23bd-2061-476e-b67d-252f57404f8b
topic_type:
- apiref
ms.openlocfilehash: c837af4cda443ec93bfbaa2d73feeb2b8f8a2803
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763119"
---
# <a name="isymunmanagedsourceservermodule-interface"></a><span data-ttu-id="d5733-103">ISymUnmanagedSourceServerModule 接口</span><span class="sxs-lookup"><span data-stu-id="d5733-103">ISymUnmanagedSourceServerModule Interface</span></span>

<span data-ttu-id="d5733-104">提供模块的源服务器数据。</span><span class="sxs-lookup"><span data-stu-id="d5733-104">Provides source server data for a module.</span></span> <span data-ttu-id="d5733-105">通过 `QueryInterface` 对实现 [ISymUnmanagedReader](isymunmanagedreader-interface.md) 接口的对象调用来获取此接口。</span><span class="sxs-lookup"><span data-stu-id="d5733-105">Obtain this interface by calling `QueryInterface` on an object that implements the [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d5733-106">方法</span><span class="sxs-lookup"><span data-stu-id="d5733-106">Methods</span></span>  
  
|<span data-ttu-id="d5733-107">方法</span><span class="sxs-lookup"><span data-stu-id="d5733-107">Method</span></span>|<span data-ttu-id="d5733-108">说明</span><span class="sxs-lookup"><span data-stu-id="d5733-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d5733-109">GetSourceServerData 方法</span><span class="sxs-lookup"><span data-stu-id="d5733-109">GetSourceServerData Method</span></span>](isymunmanagedsourceservermodule-getsourceserverdata-method.md)|<span data-ttu-id="d5733-110">返回模块的源服务器数据。</span><span class="sxs-lookup"><span data-stu-id="d5733-110">Returns the source server data for the module.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d5733-111">要求</span><span class="sxs-lookup"><span data-stu-id="d5733-111">Requirements</span></span>  

 <span data-ttu-id="d5733-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="d5733-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d5733-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="d5733-113">See also</span></span>

- [<span data-ttu-id="d5733-114">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="d5733-114">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
