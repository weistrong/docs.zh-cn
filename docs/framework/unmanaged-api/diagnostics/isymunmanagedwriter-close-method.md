---
description: 了解详细信息： ISymUnmanagedWriter：： Close 方法
title: ISymUnmanagedWriter::Close 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.Close
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::Close
helpviewer_keywords:
- Close method, ISymUnmanagedWriter interface [.NET Framework debugging]
- ISymUnmanagedWriter::Close method [.NET Framework debugging]
ms.assetid: 4cce59e1-80b9-4fc4-b3aa-126f1c5876bc
topic_type:
- apiref
ms.openlocfilehash: 02f4d8d4a232240160ad5065947282f40af42f4e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762625"
---
# <a name="isymunmanagedwriterclose-method"></a><span data-ttu-id="618af-103">ISymUnmanagedWriter::Close 方法</span><span class="sxs-lookup"><span data-stu-id="618af-103">ISymUnmanagedWriter::Close Method</span></span>

<span data-ttu-id="618af-104">将符号提交到符号存储区后关闭符号编写器。</span><span class="sxs-lookup"><span data-stu-id="618af-104">Closes the symbol writer after committing the symbols to the symbol store.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="618af-105">语法</span><span class="sxs-lookup"><span data-stu-id="618af-105">Syntax</span></span>  
  
```cpp  
HRESULT Close();  
```  
  
## <a name="return-value"></a><span data-ttu-id="618af-106">返回值</span><span class="sxs-lookup"><span data-stu-id="618af-106">Return Value</span></span>  

 <span data-ttu-id="618af-107">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="618af-107">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="618af-108">备注</span><span class="sxs-lookup"><span data-stu-id="618af-108">Remarks</span></span>  

 <span data-ttu-id="618af-109">在此调用之后，符号编写器将变为无效以便进一步更新。</span><span class="sxs-lookup"><span data-stu-id="618af-109">After this call, the symbol writer becomes invalid for further updates.</span></span> <span data-ttu-id="618af-110">若要在不提交符号的情况下关闭符号编写器，请改用 [ISymUnmanagedWriter：： Abort](isymunmanagedwriter-abort-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="618af-110">To close the symbol writer without committing the symbols, use the [ISymUnmanagedWriter::Abort](isymunmanagedwriter-abort-method.md) method instead.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="618af-111">要求</span><span class="sxs-lookup"><span data-stu-id="618af-111">Requirements</span></span>  

 <span data-ttu-id="618af-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="618af-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="618af-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="618af-113">See also</span></span>

- [<span data-ttu-id="618af-114">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="618af-114">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
