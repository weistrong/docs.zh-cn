---
description: 了解详细信息： ISymUnmanagedSymbolSearchInfo 接口
title: ISymUnmanagedSymbolSearchInfo 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedSymbolSearchInfo
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedSymbolSearchInfo
helpviewer_keywords:
- ISymUnmanagedSymbolSearchInfo interface [.NET Framework debugging]
ms.assetid: 30817373-0a21-49c1-a0c4-8e8daeecb8db
topic_type:
- apiref
ms.openlocfilehash: 2f2ab198d2c54a9fcc5fa2e24b9196a38c583f81
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762976"
---
# <a name="isymunmanagedsymbolsearchinfo-interface"></a><span data-ttu-id="07f30-103">ISymUnmanagedSymbolSearchInfo 接口</span><span class="sxs-lookup"><span data-stu-id="07f30-103">ISymUnmanagedSymbolSearchInfo Interface</span></span>

<span data-ttu-id="07f30-104">提供获取有关搜索路径的信息的方法。</span><span class="sxs-lookup"><span data-stu-id="07f30-104">Provides methods that get information about the search path.</span></span> <span data-ttu-id="07f30-105">通过 `QueryInterface` 对实现 [ISymUnmanagedReader](isymunmanagedreader-interface.md) 接口的对象调用来获取此接口。</span><span class="sxs-lookup"><span data-stu-id="07f30-105">Obtain this interface by calling `QueryInterface` on an object that implements the [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="07f30-106">方法</span><span class="sxs-lookup"><span data-stu-id="07f30-106">Methods</span></span>  
  
|<span data-ttu-id="07f30-107">方法</span><span class="sxs-lookup"><span data-stu-id="07f30-107">Method</span></span>|<span data-ttu-id="07f30-108">说明</span><span class="sxs-lookup"><span data-stu-id="07f30-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="07f30-109">GetHRESULT 方法</span><span class="sxs-lookup"><span data-stu-id="07f30-109">GetHRESULT Method</span></span>](isymunmanagedsymbolsearchinfo-gethresult-method.md)|<span data-ttu-id="07f30-110">获取 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="07f30-110">Gets the HRESULT.</span></span>|  
|[<span data-ttu-id="07f30-111">GetSearchPath 方法</span><span class="sxs-lookup"><span data-stu-id="07f30-111">GetSearchPath Method</span></span>](isymunmanagedsymbolsearchinfo-getsearchpath-method.md)|<span data-ttu-id="07f30-112">获取搜索路径。</span><span class="sxs-lookup"><span data-stu-id="07f30-112">Gets the search path.</span></span>|  
|[<span data-ttu-id="07f30-113">GetSearchPathLength 方法</span><span class="sxs-lookup"><span data-stu-id="07f30-113">GetSearchPathLength Method</span></span>](isymunmanagedsymbolsearchinfo-getsearchpathlength-method.md)|<span data-ttu-id="07f30-114">获取搜索路径长度。</span><span class="sxs-lookup"><span data-stu-id="07f30-114">Gets the search path length.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="07f30-115">要求</span><span class="sxs-lookup"><span data-stu-id="07f30-115">Requirements</span></span>  

 <span data-ttu-id="07f30-116">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="07f30-116">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="07f30-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="07f30-117">See also</span></span>

- [<span data-ttu-id="07f30-118">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="07f30-118">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
