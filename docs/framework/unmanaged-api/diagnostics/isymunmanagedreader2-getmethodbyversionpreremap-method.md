---
description: 了解详细信息： ISymUnmanagedReader2：： GetMethodByVersionPreRemap 方法
title: ISymUnmanagedReader2::GetMethodByVersionPreRemap 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader2.GetMethodByVersionPreRemap
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader2::GetMethodByVersionPreRemap
helpviewer_keywords:
- GetMethodByVersionPreRemap method [.NET Framework debugging]
- ISymUnmanagedReader2::GetMethodByVersionPreRemap method [.NET Framework debugging]
ms.assetid: 0d144ed4-bdb0-4cac-960c-cb90f4dca173
topic_type:
- apiref
ms.openlocfilehash: b827821f529b9917c6bbb3452f0c3fe3283f1ee9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763717"
---
# <a name="isymunmanagedreader2getmethodbyversionpreremap-method"></a><span data-ttu-id="75688-103">ISymUnmanagedReader2::GetMethodByVersionPreRemap 方法</span><span class="sxs-lookup"><span data-stu-id="75688-103">ISymUnmanagedReader2::GetMethodByVersionPreRemap Method</span></span>

<span data-ttu-id="75688-104">在给定方法标记和编辑并继续版本号的情况下，获取符号读取器方法。</span><span class="sxs-lookup"><span data-stu-id="75688-104">Gets a symbol reader method, given a method token and an edit-and-continue version number.</span></span> <span data-ttu-id="75688-105">版本号从1开始，并在每次通过 "编辑并继续" 操作的结果更改方法时递增。</span><span class="sxs-lookup"><span data-stu-id="75688-105">Version numbers start at 1 and are incremented each time the method is changed as a result of an edit-and-continue operation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="75688-106">语法</span><span class="sxs-lookup"><span data-stu-id="75688-106">Syntax</span></span>  
  
```cpp  
HRESULT GetMethodByVersionPreRemap(  
    [in]  mdMethodDef token,  
    [in]  int version,  
    [out, retval] ISymUnmanagedMethod** pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="75688-107">参数</span><span class="sxs-lookup"><span data-stu-id="75688-107">Parameters</span></span>  

 `token`  
 <span data-ttu-id="75688-108">中方法元数据标记。</span><span class="sxs-lookup"><span data-stu-id="75688-108">[in] The method metadata token.</span></span>  
  
 `version`  
 <span data-ttu-id="75688-109">中方法版本。</span><span class="sxs-lookup"><span data-stu-id="75688-109">[in] The method version.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="75688-110">弄指向返回的 [ISymUnmanagedMethod](isymunmanagedmethod-interface.md) 接口的指针。</span><span class="sxs-lookup"><span data-stu-id="75688-110">[out] A pointer to the returned [ISymUnmanagedMethod](isymunmanagedmethod-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="75688-111">返回值</span><span class="sxs-lookup"><span data-stu-id="75688-111">Return Value</span></span>  

 <span data-ttu-id="75688-112">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="75688-112">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="75688-113">要求</span><span class="sxs-lookup"><span data-stu-id="75688-113">Requirements</span></span>  

 <span data-ttu-id="75688-114">**标头：** CorSym。</span><span class="sxs-lookup"><span data-stu-id="75688-114">**Header:** CorSym.idl.</span></span> <span data-ttu-id="75688-115">CorSym</span><span class="sxs-lookup"><span data-stu-id="75688-115">CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="75688-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="75688-116">See also</span></span>

- [<span data-ttu-id="75688-117">ISymUnmanagedReader2 接口</span><span class="sxs-lookup"><span data-stu-id="75688-117">ISymUnmanagedReader2 Interface</span></span>](isymunmanagedreader2-interface.md)
