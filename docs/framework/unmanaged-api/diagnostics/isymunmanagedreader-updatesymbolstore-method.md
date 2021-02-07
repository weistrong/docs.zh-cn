---
description: 了解详细信息： ISymUnmanagedReader：： UpdateSymbolStore 方法
title: ISymUnmanagedReader::UpdateSymbolStore 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.UpdateSymbolStore
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::UpdateSymbolStore
helpviewer_keywords:
- UpdateSymbolStore method [.NET Framework debugging]
- ISymUnmanagedReader::UpdateSymbolStore method [.NET Framework debugging]
ms.assetid: 4a17d723-86b9-4f27-bd0d-b70c3259011c
topic_type:
- apiref
ms.openlocfilehash: eb6ca01b7978b66d0a8674e5b83ce26ee341e890
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763743"
---
# <a name="isymunmanagedreaderupdatesymbolstore-method"></a><span data-ttu-id="0aa4e-103">ISymUnmanagedReader::UpdateSymbolStore 方法</span><span class="sxs-lookup"><span data-stu-id="0aa4e-103">ISymUnmanagedReader::UpdateSymbolStore Method</span></span>

<span data-ttu-id="0aa4e-104">使用增量符号存储区更新现有的符号存储区。</span><span class="sxs-lookup"><span data-stu-id="0aa4e-104">Updates the existing symbol store with a delta symbol store.</span></span> <span data-ttu-id="0aa4e-105">此方法在 "编辑并继续" 方案中用于更新符号存储区，以便将增量与原始可移植可执行文件 (PE) 文件相匹配。</span><span class="sxs-lookup"><span data-stu-id="0aa4e-105">This method is used in edit-and-continue scenarios to update the symbol store to match deltas to the original portable executable (PE) file.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="0aa4e-106">只需指定 `filename` 或 `pIStream` 参数之一，而不能同时指定两者。</span><span class="sxs-lookup"><span data-stu-id="0aa4e-106">You need specify only one of the `filename` or `pIStream` parameters, not both.</span></span> <span data-ttu-id="0aa4e-107">如果 `filename` 指定了，则将用该文件中的符号更新符号存储区。</span><span class="sxs-lookup"><span data-stu-id="0aa4e-107">If `filename` is specified, the symbol store will be updated with the symbols in that file.</span></span> <span data-ttu-id="0aa4e-108">如果 `pIStream` 指定了，则将用中的数据更新存储区 <xref:System.Runtime.InteropServices.ComTypes.IStream> 。</span><span class="sxs-lookup"><span data-stu-id="0aa4e-108">If `pIStream` is specified, the store will be updated with the data from the <xref:System.Runtime.InteropServices.ComTypes.IStream>.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0aa4e-109">语法</span><span class="sxs-lookup"><span data-stu-id="0aa4e-109">Syntax</span></span>  
  
```cpp  
HRESULT UpdateSymbolStore (  
    [in] const WCHAR *filename,  
    [in] IStream *pIStream);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0aa4e-110">参数</span><span class="sxs-lookup"><span data-stu-id="0aa4e-110">Parameters</span></span>  

 `filename`  
 <span data-ttu-id="0aa4e-111">中包含符号存储区的文件的名称。</span><span class="sxs-lookup"><span data-stu-id="0aa4e-111">[in] The name of the file that contains the symbol store.</span></span>  
  
 `pIStream`  
 <span data-ttu-id="0aa4e-112">中文件流，用作参数的替代项 `filename` 。</span><span class="sxs-lookup"><span data-stu-id="0aa4e-112">[in] The file stream, used as an alternative to the `filename` parameter.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0aa4e-113">返回值</span><span class="sxs-lookup"><span data-stu-id="0aa4e-113">Return Value</span></span>  

 <span data-ttu-id="0aa4e-114">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="0aa4e-114">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0aa4e-115">要求</span><span class="sxs-lookup"><span data-stu-id="0aa4e-115">Requirements</span></span>  

 <span data-ttu-id="0aa4e-116">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="0aa4e-116">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0aa4e-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="0aa4e-117">See also</span></span>

- [<span data-ttu-id="0aa4e-118">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="0aa4e-118">ISymUnmanagedReader Interface</span></span>](isymunmanagedreader-interface.md)
