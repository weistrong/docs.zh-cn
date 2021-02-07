---
description: 了解详细信息： ISymUnmanagedReader：： GetMethodVersion 方法
title: ISymUnmanagedReader::GetMethodVersion 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetMethodVersion
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetMethodVersion
helpviewer_keywords:
- GetMethodVersion method [.NET Framework debugging]
- ISymUnmanagedReader::GetMethodVersion method [.NET Framework debugging]
ms.assetid: d6f9ac84-302a-4f5e-b990-e76f4269fceb
topic_type:
- apiref
ms.openlocfilehash: 027f65f858aab3e4ad0bc0bfbffd91f6118b80b2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99764016"
---
# <a name="isymunmanagedreadergetmethodversion-method"></a><span data-ttu-id="a867d-103">ISymUnmanagedReader::GetMethodVersion 方法</span><span class="sxs-lookup"><span data-stu-id="a867d-103">ISymUnmanagedReader::GetMethodVersion Method</span></span>

<span data-ttu-id="a867d-104">获取方法版本。</span><span class="sxs-lookup"><span data-stu-id="a867d-104">Gets the method version.</span></span> <span data-ttu-id="a867d-105">方法版本从1开始，并在每次重新编译方法时递增。</span><span class="sxs-lookup"><span data-stu-id="a867d-105">The method version starts at 1 and is incremented each time the method is recompiled.</span></span> <span data-ttu-id="a867d-106">重新编译可能会发生，而不会对方法进行更改。</span><span class="sxs-lookup"><span data-stu-id="a867d-106">Recompilation can happen without changes to the method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a867d-107">语法</span><span class="sxs-lookup"><span data-stu-id="a867d-107">Syntax</span></span>  
  
```cpp  
HRESULT GetMethodVersion (  
    [in]  ISymUnmanagedMethod* pMethod,  
    [out] int* version);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a867d-108">参数</span><span class="sxs-lookup"><span data-stu-id="a867d-108">Parameters</span></span>  

 `pMethod`  
 <span data-ttu-id="a867d-109">中要获取其版本的方法。</span><span class="sxs-lookup"><span data-stu-id="a867d-109">[in] The method for which to get the version.</span></span>  
  
 `version`  
 <span data-ttu-id="a867d-110">弄指向接收方法版本的变量的指针。</span><span class="sxs-lookup"><span data-stu-id="a867d-110">[out] A pointer to a variable that receives the method version.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a867d-111">返回值</span><span class="sxs-lookup"><span data-stu-id="a867d-111">Return Value</span></span>  

 <span data-ttu-id="a867d-112">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="a867d-112">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a867d-113">要求</span><span class="sxs-lookup"><span data-stu-id="a867d-113">Requirements</span></span>  

 <span data-ttu-id="a867d-114">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="a867d-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a867d-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="a867d-115">See also</span></span>

- [<span data-ttu-id="a867d-116">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="a867d-116">ISymUnmanagedReader Interface</span></span>](isymunmanagedreader-interface.md)
