---
description: 了解详细信息： ISymUnmanagedDocumentWriter：： SetSource 方法
title: ISymUnmanagedDocumentWriter::SetSource 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocumentWriter.SetSource
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocumentWriter::SetSource
helpviewer_keywords:
- ISymUnmanagedDocumentWriter::SetSource method [.NET Framework debugging]
- SetSource method [.NET Framework debugging]
ms.assetid: ea5b9d9f-ff06-4bd3-8de5-6435343aba59
topic_type:
- apiref
ms.openlocfilehash: e24e34a297a9931babf3df4f2bae1b5e8f60db1b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721471"
---
# <a name="isymunmanageddocumentwritersetsource-method"></a><span data-ttu-id="f0138-103">ISymUnmanagedDocumentWriter::SetSource 方法</span><span class="sxs-lookup"><span data-stu-id="f0138-103">ISymUnmanagedDocumentWriter::SetSource Method</span></span>

<span data-ttu-id="f0138-104">为正在编写的文档设置嵌入源。</span><span class="sxs-lookup"><span data-stu-id="f0138-104">Sets embedded source for a document that is being written.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f0138-105">语法</span><span class="sxs-lookup"><span data-stu-id="f0138-105">Syntax</span></span>  
  
```cpp  
HRESULT SetSource(  
    [in]  ULONG32  sourceSize,  
    [in, size_is(sourceSize)] BYTE  source[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f0138-106">参数</span><span class="sxs-lookup"><span data-stu-id="f0138-106">Parameters</span></span>  

 `sourceSize`  
 <span data-ttu-id="f0138-107">中一个 `ULONG32` 包含缓冲区大小的 `source` 。</span><span class="sxs-lookup"><span data-stu-id="f0138-107">[in] A `ULONG32` that contains the size of the `source` buffer.</span></span>  
  
 `source`  
 <span data-ttu-id="f0138-108">中存储嵌入源的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="f0138-108">[in] The buffer that stores the embedded source.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f0138-109">返回值</span><span class="sxs-lookup"><span data-stu-id="f0138-109">Return Value</span></span>  

 <span data-ttu-id="f0138-110">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="f0138-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f0138-111">要求</span><span class="sxs-lookup"><span data-stu-id="f0138-111">Requirements</span></span>  

 <span data-ttu-id="f0138-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="f0138-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f0138-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="f0138-113">See also</span></span>

- [<span data-ttu-id="f0138-114">ISymUnmanagedDocumentWriter 接口</span><span class="sxs-lookup"><span data-stu-id="f0138-114">ISymUnmanagedDocumentWriter Interface</span></span>](isymunmanageddocumentwriter-interface.md)
