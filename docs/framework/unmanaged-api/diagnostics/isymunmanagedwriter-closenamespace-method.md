---
description: 了解详细信息： ISymUnmanagedWriter：： CloseNamespace 方法
title: ISymUnmanagedWriter::CloseNamespace 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.CloseNamespace
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::CloseNamespace
helpviewer_keywords:
- ISymUnmanagedWriter::CloseNamespace method [.NET Framework debugging]
- CloseNamespace method [.NET Framework debugging]
ms.assetid: 7f74d9c5-1377-4958-b842-6306d611cbd5
topic_type:
- apiref
ms.openlocfilehash: c552d8bc86ab2bbd93918fdd6be3f880b3d83178
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762560"
---
# <a name="isymunmanagedwriterclosenamespace-method"></a><span data-ttu-id="abef6-103">ISymUnmanagedWriter::CloseNamespace 方法</span><span class="sxs-lookup"><span data-stu-id="abef6-103">ISymUnmanagedWriter::CloseNamespace Method</span></span>

<span data-ttu-id="abef6-104">关闭最近打开的命名空间。</span><span class="sxs-lookup"><span data-stu-id="abef6-104">Closes the most recently opened namespace.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="abef6-105">语法</span><span class="sxs-lookup"><span data-stu-id="abef6-105">Syntax</span></span>  
  
```cpp  
HRESULT CloseNamespace();  
```  
  
## <a name="return-value"></a><span data-ttu-id="abef6-106">返回值</span><span class="sxs-lookup"><span data-stu-id="abef6-106">Return Value</span></span>  

 <span data-ttu-id="abef6-107">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="abef6-107">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="abef6-108">要求</span><span class="sxs-lookup"><span data-stu-id="abef6-108">Requirements</span></span>  

 <span data-ttu-id="abef6-109">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="abef6-109">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="abef6-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="abef6-110">See also</span></span>

- [<span data-ttu-id="abef6-111">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="abef6-111">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
- [<span data-ttu-id="abef6-112">OpenNamespace 方法</span><span class="sxs-lookup"><span data-stu-id="abef6-112">OpenNamespace Method</span></span>](isymunmanagedwriter-opennamespace-method.md)
