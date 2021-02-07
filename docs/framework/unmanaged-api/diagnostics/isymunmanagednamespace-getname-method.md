---
description: 了解详细信息： ISymUnmanagedNamespace：： GetName 方法
title: ISymUnmanagedNamespace::GetName 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedNamespace.GetName
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedNamespace::GetName
helpviewer_keywords:
- ISymUnmanagedNamespace::GetName method [.NET Framework debugging]
- GetName method, ISymUnmanagedNamespace interface [.NET Framework debugging]
ms.assetid: 657bf91d-005a-4ea4-9298-04d1291c0bc3
topic_type:
- apiref
ms.openlocfilehash: f4d366363cd089995f98039389f59077e949fb79
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721211"
---
# <a name="isymunmanagednamespacegetname-method"></a><span data-ttu-id="4b46b-103">ISymUnmanagedNamespace::GetName 方法</span><span class="sxs-lookup"><span data-stu-id="4b46b-103">ISymUnmanagedNamespace::GetName Method</span></span>

<span data-ttu-id="4b46b-104">获取此命名空间的名称。</span><span class="sxs-lookup"><span data-stu-id="4b46b-104">Gets the name of this namespace.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4b46b-105">语法</span><span class="sxs-lookup"><span data-stu-id="4b46b-105">Syntax</span></span>  
  
```cpp  
HRESULT GetName(  
    [in]  ULONG32  cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName),  
        length_is(*pcchName)] WCHAR szName[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4b46b-106">参数</span><span class="sxs-lookup"><span data-stu-id="4b46b-106">Parameters</span></span>  

 `cchName`  
 <span data-ttu-id="4b46b-107">中 `ULONG32` 指示缓冲区大小的 `szName` 。</span><span class="sxs-lookup"><span data-stu-id="4b46b-107">[in] A `ULONG32` that indicates the size of the `szName` buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="4b46b-108">弄指向的指针， `ULONG32` 该指针接收包含命名空间名称（包括 null 终止）所需的缓冲区大小（以字符数表示）。</span><span class="sxs-lookup"><span data-stu-id="4b46b-108">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the namespace name, including the null termination.</span></span>  
  
 `szName`  
 <span data-ttu-id="4b46b-109">弄指向包含命名空间名称的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="4b46b-109">[out] A pointer to a buffer that contains the namespace name.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4b46b-110">返回值</span><span class="sxs-lookup"><span data-stu-id="4b46b-110">Return Value</span></span>  

 <span data-ttu-id="4b46b-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="4b46b-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4b46b-112">要求</span><span class="sxs-lookup"><span data-stu-id="4b46b-112">Requirements</span></span>  

 <span data-ttu-id="4b46b-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="4b46b-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4b46b-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="4b46b-114">See also</span></span>

- [<span data-ttu-id="4b46b-115">ISymUnmanagedNamespace 接口</span><span class="sxs-lookup"><span data-stu-id="4b46b-115">ISymUnmanagedNamespace Interface</span></span>](isymunmanagednamespace-interface.md)
