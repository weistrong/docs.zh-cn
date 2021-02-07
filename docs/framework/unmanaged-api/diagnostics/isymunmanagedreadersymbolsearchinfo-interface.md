---
description: 了解详细信息： ISymUnmanagedReaderSymbolSearchInfo 接口
title: ISymUnmanagedReaderSymbolSearchInfo 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReaderSymbolSearchInfo
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReaderSymbolSearchInfo
helpviewer_keywords:
- ISymUnmanagedReaderSymbolSearchInfo interface [.NET Framework debugging]
ms.assetid: fde7e21d-1169-4bed-a34d-792e69652bf9
topic_type:
- apiref
ms.openlocfilehash: f5d13027709698df735af5fceac31f7b73741440
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763561"
---
# <a name="isymunmanagedreadersymbolsearchinfo-interface"></a><span data-ttu-id="0ae23-103">ISymUnmanagedReaderSymbolSearchInfo 接口</span><span class="sxs-lookup"><span data-stu-id="0ae23-103">ISymUnmanagedReaderSymbolSearchInfo Interface</span></span>

<span data-ttu-id="0ae23-104">提供用于获取符号搜索信息的方法。</span><span class="sxs-lookup"><span data-stu-id="0ae23-104">Provides methods that get symbol search information.</span></span> <span data-ttu-id="0ae23-105">通过 `QueryInterface` 对实现 [ISymUnmanagedReader](isymunmanagedreader-interface.md) 接口的对象调用来获取此接口。</span><span class="sxs-lookup"><span data-stu-id="0ae23-105">Obtain this interface by calling `QueryInterface` on an object that implements the [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="0ae23-106">方法</span><span class="sxs-lookup"><span data-stu-id="0ae23-106">Methods</span></span>  
  
|<span data-ttu-id="0ae23-107">方法</span><span class="sxs-lookup"><span data-stu-id="0ae23-107">Method</span></span>|<span data-ttu-id="0ae23-108">说明</span><span class="sxs-lookup"><span data-stu-id="0ae23-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="0ae23-109">GetSymbolSearchInfo 方法</span><span class="sxs-lookup"><span data-stu-id="0ae23-109">GetSymbolSearchInfo Method</span></span>](isymunmanagedreadersymbolsearchinfo-getsymbolsearchinfo-method.md)|<span data-ttu-id="0ae23-110">获取符号搜索信息。</span><span class="sxs-lookup"><span data-stu-id="0ae23-110">Gets symbol search information.</span></span>|  
|[<span data-ttu-id="0ae23-111">GetSymbolSearchInfoCount 方法</span><span class="sxs-lookup"><span data-stu-id="0ae23-111">GetSymbolSearchInfoCount Method</span></span>](isymunmanagedreadersymbolsearchinfo-getsymbolsearchinfocount-method.md)|<span data-ttu-id="0ae23-112">获取符号搜索信息的计数。</span><span class="sxs-lookup"><span data-stu-id="0ae23-112">Gets a count of symbol search information.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="0ae23-113">要求</span><span class="sxs-lookup"><span data-stu-id="0ae23-113">Requirements</span></span>  

 <span data-ttu-id="0ae23-114">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="0ae23-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0ae23-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="0ae23-115">See also</span></span>

- [<span data-ttu-id="0ae23-116">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="0ae23-116">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
