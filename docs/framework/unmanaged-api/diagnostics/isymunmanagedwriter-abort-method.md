---
description: 了解详细信息： ISymUnmanagedWriter：： Abort 方法
title: ISymUnmanagedWriter::Abort 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.Abort
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::Abort
helpviewer_keywords:
- ISymUnmanagedWriter::Abort method [.NET Framework debugging]
- Abort method, ISymUnmanagedWriter interface [.NET Framework debugging]
ms.assetid: 416b220f-38d4-48e0-bb49-d2faa7366702
topic_type:
- apiref
ms.openlocfilehash: 312694bf2b667ea78bf5ddc993d0e2b71c85a8ad
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762677"
---
# <a name="isymunmanagedwriterabort-method"></a><span data-ttu-id="3b7e6-103">ISymUnmanagedWriter::Abort 方法</span><span class="sxs-lookup"><span data-stu-id="3b7e6-103">ISymUnmanagedWriter::Abort Method</span></span>

<span data-ttu-id="3b7e6-104">关闭符号编写器，而不将符号提交到符号存储区。</span><span class="sxs-lookup"><span data-stu-id="3b7e6-104">Closes the symbol writer without committing the symbols to the symbol store.</span></span> <span data-ttu-id="3b7e6-105">在此调用之后，符号编写器将变为无效以便进一步更新。</span><span class="sxs-lookup"><span data-stu-id="3b7e6-105">After this call, the symbol writer becomes invalid for further updates.</span></span> <span data-ttu-id="3b7e6-106">若要提交符号并关闭符号编写器，请改为使用 [ISymUnmanagedWriter：： close](isymunmanagedwriter-close-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3b7e6-106">To commit the symbols and close the symbol writer, use the [ISymUnmanagedWriter::Close](isymunmanagedwriter-close-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3b7e6-107">语法</span><span class="sxs-lookup"><span data-stu-id="3b7e6-107">Syntax</span></span>  
  
```cpp  
HRESULT Abort();  
```  
  
## <a name="return-value"></a><span data-ttu-id="3b7e6-108">返回值</span><span class="sxs-lookup"><span data-stu-id="3b7e6-108">Return Value</span></span>  

 <span data-ttu-id="3b7e6-109">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="3b7e6-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3b7e6-110">要求</span><span class="sxs-lookup"><span data-stu-id="3b7e6-110">Requirements</span></span>  

 <span data-ttu-id="3b7e6-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="3b7e6-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3b7e6-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="3b7e6-112">See also</span></span>

- [<span data-ttu-id="3b7e6-113">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="3b7e6-113">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
