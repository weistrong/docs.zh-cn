---
description: 了解详细信息： ISymUnmanagedWriter：： OpenNamespace 方法
title: ISymUnmanagedWriter::OpenNamespace 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.OpenNamespace
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::OpenNamespace
helpviewer_keywords:
- ISymUnmanagedWriter::OpenNamespace method [.NET Framework debugging]
- OpenNamespace method [.NET Framework debugging]
ms.assetid: 426f4e4f-e60d-4ad1-b546-a10e3c55c283
topic_type:
- apiref
ms.openlocfilehash: ab848e44dfda1f5caaa92bfd3376bdcbd67d8a9b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762118"
---
# <a name="isymunmanagedwriteropennamespace-method"></a><span data-ttu-id="24279-103">ISymUnmanagedWriter::OpenNamespace 方法</span><span class="sxs-lookup"><span data-stu-id="24279-103">ISymUnmanagedWriter::OpenNamespace Method</span></span>

<span data-ttu-id="24279-104">打开一个新的命名空间。</span><span class="sxs-lookup"><span data-stu-id="24279-104">Opens a new namespace.</span></span> <span data-ttu-id="24279-105">在定义占用命名空间的方法或变量之前调用此方法。</span><span class="sxs-lookup"><span data-stu-id="24279-105">Call this method before defining methods or variables that occupy a namespace.</span></span> <span data-ttu-id="24279-106">命名空间可以嵌套。</span><span class="sxs-lookup"><span data-stu-id="24279-106">Namespaces can be nested.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="24279-107">语法</span><span class="sxs-lookup"><span data-stu-id="24279-107">Syntax</span></span>  
  
```cpp  
HRESULT OpenNamespace(  
    [in] const WCHAR *name);  
```  
  
## <a name="parameters"></a><span data-ttu-id="24279-108">参数</span><span class="sxs-lookup"><span data-stu-id="24279-108">Parameters</span></span>  

 `name`  
 <span data-ttu-id="24279-109">中指向新命名空间的名称的指针。</span><span class="sxs-lookup"><span data-stu-id="24279-109">[in] A pointer to the name of the new namespace.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="24279-110">返回值</span><span class="sxs-lookup"><span data-stu-id="24279-110">Return Value</span></span>  

 <span data-ttu-id="24279-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="24279-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="24279-112">要求</span><span class="sxs-lookup"><span data-stu-id="24279-112">Requirements</span></span>  

 <span data-ttu-id="24279-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="24279-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="24279-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="24279-114">See also</span></span>

- [<span data-ttu-id="24279-115">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="24279-115">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
- [<span data-ttu-id="24279-116">CloseNamespace 方法</span><span class="sxs-lookup"><span data-stu-id="24279-116">CloseNamespace Method</span></span>](isymunmanagedwriter-closenamespace-method.md)
