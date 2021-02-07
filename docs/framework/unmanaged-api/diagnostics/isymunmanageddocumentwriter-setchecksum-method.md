---
description: 了解详细信息： ISymUnmanagedDocumentWriter：： SetCheckSum 方法
title: ISymUnmanagedDocumentWriter::SetCheckSum 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocumentWriter.SetCheckSum
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocumentWriter::SetCheckSum
helpviewer_keywords:
- ISymUnmanagedDocumentWriter::SetCheckSum method [.NET Framework debugging]
- SetCheckSum method [.NET Framework debugging]
ms.assetid: c7e99879-421f-43ce-b193-34733cf30085
topic_type:
- apiref
ms.openlocfilehash: ac2ba9654f3610dca333cf0e06c20696cf31bd1f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710083"
---
# <a name="isymunmanageddocumentwritersetchecksum-method"></a><span data-ttu-id="79936-103">ISymUnmanagedDocumentWriter::SetCheckSum 方法</span><span class="sxs-lookup"><span data-stu-id="79936-103">ISymUnmanagedDocumentWriter::SetCheckSum Method</span></span>

<span data-ttu-id="79936-104">设置校验和信息。</span><span class="sxs-lookup"><span data-stu-id="79936-104">Sets checksum information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79936-105">语法</span><span class="sxs-lookup"><span data-stu-id="79936-105">Syntax</span></span>  
  
```cpp  
HRESULT SetCheckSum(  
    [in]  GUID     algorithmId,  
    [in]  ULONG32  checkSumSize,  
    [in, size_is(checkSumSize)]  BYTE checkSum[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="79936-106">参数</span><span class="sxs-lookup"><span data-stu-id="79936-106">Parameters</span></span>  

 `algorithmId`  
 <span data-ttu-id="79936-107">中表示算法标识符的 GUID。</span><span class="sxs-lookup"><span data-stu-id="79936-107">[in] The GUID that represents the algorithm identifier.</span></span>  
  
 `checkSumSize`  
 <span data-ttu-id="79936-108">中一个 `ULONG32` ，该值指示缓冲区的大小（以字节为单位） `checkSum` 。</span><span class="sxs-lookup"><span data-stu-id="79936-108">[in] A `ULONG32` that indicates the size, in bytes, of the `checkSum` buffer.</span></span>  
  
 `checkSum`  
 <span data-ttu-id="79936-109">中存储校验和信息的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="79936-109">[in] The buffer that stores the checksum information.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="79936-110">返回值</span><span class="sxs-lookup"><span data-stu-id="79936-110">Return Value</span></span>  

 <span data-ttu-id="79936-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="79936-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="79936-112">要求</span><span class="sxs-lookup"><span data-stu-id="79936-112">Requirements</span></span>  

 <span data-ttu-id="79936-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="79936-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="79936-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="79936-114">See also</span></span>

- [<span data-ttu-id="79936-115">ISymUnmanagedDocumentWriter 接口</span><span class="sxs-lookup"><span data-stu-id="79936-115">ISymUnmanagedDocumentWriter Interface</span></span>](isymunmanageddocumentwriter-interface.md)
