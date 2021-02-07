---
description: 了解详细信息： ISymUnmanagedDocument：： GetCheckSum 方法
title: ISymUnmanagedDocument::GetCheckSum 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetCheckSum
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetCheckSum
helpviewer_keywords:
- ISymUnmanagedDocument::GetCheckSum method [.NET Framework debugging]
- GetCheckSum method [.NET Framework debugging]
ms.assetid: 9bc881b3-e2ce-48a7-ad69-17eaaa304120
topic_type:
- apiref
ms.openlocfilehash: 9f9a42e58b22661a2233fcb457b9b42b0d6a3d1a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99737683"
---
# <a name="isymunmanageddocumentgetchecksum-method"></a><span data-ttu-id="9a471-103">ISymUnmanagedDocument::GetCheckSum 方法</span><span class="sxs-lookup"><span data-stu-id="9a471-103">ISymUnmanagedDocument::GetCheckSum Method</span></span>

<span data-ttu-id="9a471-104">获取校验和。</span><span class="sxs-lookup"><span data-stu-id="9a471-104">Gets the checksum.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9a471-105">语法</span><span class="sxs-lookup"><span data-stu-id="9a471-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCheckSum(  
    [in]  ULONG32  cData,  
    [out] ULONG32  *pcData,  
    [out, size_is(cData), length_is(*pcData)] BYTE data[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9a471-106">参数</span><span class="sxs-lookup"><span data-stu-id="9a471-106">Parameters</span></span>  

 `cData`  
 <span data-ttu-id="9a471-107">中参数所提供的缓冲区的长度 `data`</span><span class="sxs-lookup"><span data-stu-id="9a471-107">[in] The length of the buffer provided by the `data` parameter</span></span>  
  
 `pcData`  
 <span data-ttu-id="9a471-108">弄校验和的大小和长度（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="9a471-108">[out] The size and length of the checksum, in bytes.</span></span>  
  
 `data`  
 <span data-ttu-id="9a471-109">弄接收校验和的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="9a471-109">[out] The buffer that receives the checksum.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9a471-110">返回值</span><span class="sxs-lookup"><span data-stu-id="9a471-110">Return Value</span></span>  

 <span data-ttu-id="9a471-111">如果该方法成功，则 S_OK;否则为错误代码。</span><span class="sxs-lookup"><span data-stu-id="9a471-111">S_OK if the method succeeds; otherwise, an error code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9a471-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="9a471-112">See also</span></span>

- [<span data-ttu-id="9a471-113">ISymUnmanagedDocument 接口</span><span class="sxs-lookup"><span data-stu-id="9a471-113">ISymUnmanagedDocument Interface</span></span>](isymunmanageddocument-interface.md)
