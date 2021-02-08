---
description: 了解详细信息： ISymUnmanagedReader：： GetMethodByVersion 方法
title: ISymUnmanagedReader::GetMethodByVersion 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetMethodByVersion
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetMethodByVersion
helpviewer_keywords:
- ISymUnmanagedReader::GetMethodByVersion method [.NET Framework debugging]
- GetMethodByVersion method [.NET Framework debugging]
ms.assetid: 6ddb0631-4569-41b3-93e4-50fdfaa486dc
topic_type:
- apiref
ms.openlocfilehash: 6b2fa3ff3af91d59bb79029d039e5656610bebff
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772063"
---
# <a name="isymunmanagedreadergetmethodbyversion-method"></a><span data-ttu-id="3a945-103">ISymUnmanagedReader::GetMethodByVersion 方法</span><span class="sxs-lookup"><span data-stu-id="3a945-103">ISymUnmanagedReader::GetMethodByVersion Method</span></span>

<span data-ttu-id="3a945-104">在给定方法标记和编辑和复制版本号的情况下，获取符号读取器方法。</span><span class="sxs-lookup"><span data-stu-id="3a945-104">Gets a symbol reader method, given a method token and an edit-and-copy version number.</span></span> <span data-ttu-id="3a945-105">版本号从1开始，并在每次通过编辑和复制操作更改方法时递增。</span><span class="sxs-lookup"><span data-stu-id="3a945-105">Version numbers start at 1 and are incremented each time the method is changed as a result of an edit-and-copy operation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3a945-106">语法</span><span class="sxs-lookup"><span data-stu-id="3a945-106">Syntax</span></span>  
  
```cpp  
HRESULT GetMethodByVersion (  
    [in]  mdMethodDef  token,  
    [in]  int  version,  
    [out, retval] ISymUnmanagedMethod** pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3a945-107">参数</span><span class="sxs-lookup"><span data-stu-id="3a945-107">Parameters</span></span>  

 `token`  
 <span data-ttu-id="3a945-108">中方法标记。</span><span class="sxs-lookup"><span data-stu-id="3a945-108">[in] The method token.</span></span>  
  
 `version`  
 <span data-ttu-id="3a945-109">中方法版本。</span><span class="sxs-lookup"><span data-stu-id="3a945-109">[in] The method version.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="3a945-110">弄指向返回的接口的指针。</span><span class="sxs-lookup"><span data-stu-id="3a945-110">[out] A pointer to the returned interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3a945-111">返回值</span><span class="sxs-lookup"><span data-stu-id="3a945-111">Return Value</span></span>  

 <span data-ttu-id="3a945-112">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="3a945-112">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3a945-113">要求</span><span class="sxs-lookup"><span data-stu-id="3a945-113">Requirements</span></span>  

 <span data-ttu-id="3a945-114">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="3a945-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3a945-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="3a945-115">See also</span></span>

- [<span data-ttu-id="3a945-116">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="3a945-116">ISymUnmanagedReader Interface</span></span>](isymunmanagedreader-interface.md)
