---
description: 了解详细信息： ISymUnmanagedVariable：： GetName 方法
title: ISymUnmanagedVariable::GetName 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetName
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetName
helpviewer_keywords:
- GetName method, ISymUnmanagedVariable interface [.NET Framework debugging]
- ISymUnmanagedVariable::GetName method [.NET Framework debugging]
ms.assetid: eedf1ef0-9d4a-4847-a201-4e99572dfe5e
topic_type:
- apiref
ms.openlocfilehash: 88d8cf4c81200a30e2a102b63af2817fef2b50c9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762781"
---
# <a name="isymunmanagedvariablegetname-method"></a><span data-ttu-id="b8138-103">ISymUnmanagedVariable::GetName 方法</span><span class="sxs-lookup"><span data-stu-id="b8138-103">ISymUnmanagedVariable::GetName Method</span></span>

<span data-ttu-id="b8138-104">获取此变量的名称。</span><span class="sxs-lookup"><span data-stu-id="b8138-104">Gets the name of this variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b8138-105">语法</span><span class="sxs-lookup"><span data-stu-id="b8138-105">Syntax</span></span>  
  
```cpp  
HRESULT GetName(  
    [in]  ULONG32  cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName),  
        length_is(*pcchName)] WCHAR szName[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b8138-106">参数</span><span class="sxs-lookup"><span data-stu-id="b8138-106">Parameters</span></span>  

 `cchName`  
 <span data-ttu-id="b8138-107">中参数指向的缓冲区的长度 `pcchName` 。</span><span class="sxs-lookup"><span data-stu-id="b8138-107">[in] The length of the buffer that the `pcchName` parameter points to.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="b8138-108">弄指向的指针， `ULONG32` 该指针接收包含名称（包括 null 终止）所需的缓冲区的大小（以字符数表示）。</span><span class="sxs-lookup"><span data-stu-id="b8138-108">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the name, including the null termination.</span></span>  
  
 `szName`  
 <span data-ttu-id="b8138-109">弄存储名称的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="b8138-109">[out] The buffer that stores the name.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b8138-110">返回值</span><span class="sxs-lookup"><span data-stu-id="b8138-110">Return Value</span></span>  

 <span data-ttu-id="b8138-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="b8138-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b8138-112">要求</span><span class="sxs-lookup"><span data-stu-id="b8138-112">Requirements</span></span>  

 <span data-ttu-id="b8138-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="b8138-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b8138-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="b8138-114">See also</span></span>

- [<span data-ttu-id="b8138-115">ISymUnmanagedVariable 接口</span><span class="sxs-lookup"><span data-stu-id="b8138-115">ISymUnmanagedVariable Interface</span></span>](isymunmanagedvariable-interface.md)
