---
description: 了解详细信息： ISymUnmanagedReader：： GetUserEntryPoint 方法
title: ISymUnmanagedReader::GetUserEntryPoint 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetUserEntryPoint
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetUserEntryPoint
helpviewer_keywords:
- GetUserEntryPoint method [.NET Framework debugging]
- ISymUnmanagedReader::GetUserEntryPoint method [.NET Framework debugging]
ms.assetid: 3fd3a34c-d176-46e9-9996-fb1646cff9b0
topic_type:
- apiref
ms.openlocfilehash: b8696a339fc8aefca2b1a1f9b960ba94ce565d8d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763912"
---
# <a name="isymunmanagedreadergetuserentrypoint-method"></a><span data-ttu-id="563c5-103">ISymUnmanagedReader::GetUserEntryPoint 方法</span><span class="sxs-lookup"><span data-stu-id="563c5-103">ISymUnmanagedReader::GetUserEntryPoint Method</span></span>

<span data-ttu-id="563c5-104">返回指定为模块的用户入口点的方法（如果有）。</span><span class="sxs-lookup"><span data-stu-id="563c5-104">Returns the method that was specified as the user entry point for the module, if any.</span></span> <span data-ttu-id="563c5-105">例如，在 main 方法之前，此方法可以是用户的 main 方法，而不是编译器生成的存根。</span><span class="sxs-lookup"><span data-stu-id="563c5-105">For example, this method could be the user's main method rather than compiler-generated stubs before the main method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="563c5-106">语法</span><span class="sxs-lookup"><span data-stu-id="563c5-106">Syntax</span></span>  
  
```cpp  
HRESULT GetUserEntryPoint (  
    [out, retval]  mdMethodDef  *pToken);  
```  
  
## <a name="parameters"></a><span data-ttu-id="563c5-107">参数</span><span class="sxs-lookup"><span data-stu-id="563c5-107">Parameters</span></span>  

 `pToken`  
 <span data-ttu-id="563c5-108">弄指向接收入口点的变量的指针。</span><span class="sxs-lookup"><span data-stu-id="563c5-108">[out] A pointer to a variable that receives the entry point.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="563c5-109">返回值</span><span class="sxs-lookup"><span data-stu-id="563c5-109">Return Value</span></span>  

 <span data-ttu-id="563c5-110">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="563c5-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="563c5-111">要求</span><span class="sxs-lookup"><span data-stu-id="563c5-111">Requirements</span></span>  

 <span data-ttu-id="563c5-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="563c5-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="563c5-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="563c5-113">See also</span></span>

- [<span data-ttu-id="563c5-114">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="563c5-114">ISymUnmanagedReader Interface</span></span>](isymunmanagedreader-interface.md)
