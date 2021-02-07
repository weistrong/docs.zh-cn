---
description: 了解详细信息： ISymUnmanagedReader：： ReplaceSymbolStore 方法
title: ISymUnmanagedReader::ReplaceSymbolStore 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.ReplaceSymbolStore
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::ReplaceSymbolStore
helpviewer_keywords:
- ReplaceSymbolStore method [.NET Framework debugging]
- ISymUnmanagedReader::ReplaceSymbolStore method [.NET Framework debugging]
ms.assetid: 43257761-8cb1-4eaf-8fb5-1f3980cb66cd
topic_type:
- apiref
ms.openlocfilehash: e05344ee0b14d40d735ca3e557c319998daf7849
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763757"
---
# <a name="isymunmanagedreaderreplacesymbolstore-method"></a><span data-ttu-id="72328-103">ISymUnmanagedReader::ReplaceSymbolStore 方法</span><span class="sxs-lookup"><span data-stu-id="72328-103">ISymUnmanagedReader::ReplaceSymbolStore Method</span></span>

<span data-ttu-id="72328-104">用增量符号存储区替换现有的符号存储区。</span><span class="sxs-lookup"><span data-stu-id="72328-104">Replaces the existing symbol store with a delta symbol store.</span></span> <span data-ttu-id="72328-105">此方法类似于 [UpdateSymbolStore](isymunmanagedreader-updatesymbolstore-method.md) 方法，不同之处在于给定增量充当完全替换而不是更新。</span><span class="sxs-lookup"><span data-stu-id="72328-105">This method is similar to the [UpdateSymbolStore](isymunmanagedreader-updatesymbolstore-method.md) method, except that the given delta acts as a complete replacement rather than an update.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="72328-106">只需指定 `filename` 或 `pIStream` 参数之一，而不能同时指定两者。</span><span class="sxs-lookup"><span data-stu-id="72328-106">You need specify only one of the `filename` or `pIStream` parameters, not both.</span></span> <span data-ttu-id="72328-107">如果 `filename` 指定了，则将用该文件中的符号更新符号存储区。</span><span class="sxs-lookup"><span data-stu-id="72328-107">If `filename` is specified, the symbol store will be updated with the symbols in that file.</span></span> <span data-ttu-id="72328-108">如果 `pIStream` 指定了，则将用中的数据更新存储区 <xref:System.Runtime.InteropServices.ComTypes.IStream> 。</span><span class="sxs-lookup"><span data-stu-id="72328-108">If `pIStream` is specified, the store will be updated with the data from the <xref:System.Runtime.InteropServices.ComTypes.IStream>.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="72328-109">语法</span><span class="sxs-lookup"><span data-stu-id="72328-109">Syntax</span></span>  
  
```cpp  
HRESULT ReplaceSymbolStore (  
    [in] const WCHAR *filename,  
    [in] IStream *pIStream);  
```  
  
## <a name="parameters"></a><span data-ttu-id="72328-110">参数</span><span class="sxs-lookup"><span data-stu-id="72328-110">Parameters</span></span>  

 `filename`  
 <span data-ttu-id="72328-111">中包含符号存储区的文件的名称。</span><span class="sxs-lookup"><span data-stu-id="72328-111">[in] The name of the file containing the symbol store.</span></span>  
  
 `pIStream`  
 <span data-ttu-id="72328-112">中文件流，用作参数的替代项 `filename` 。</span><span class="sxs-lookup"><span data-stu-id="72328-112">[in] The file stream, used as an alternative to the `filename` parameter.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="72328-113">返回值</span><span class="sxs-lookup"><span data-stu-id="72328-113">Return Value</span></span>  

 <span data-ttu-id="72328-114">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="72328-114">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="72328-115">要求</span><span class="sxs-lookup"><span data-stu-id="72328-115">Requirements</span></span>  

 <span data-ttu-id="72328-116">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="72328-116">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="72328-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="72328-117">See also</span></span>

- [<span data-ttu-id="72328-118">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="72328-118">ISymUnmanagedReader Interface</span></span>](isymunmanagedreader-interface.md)
