---
description: 了解详细信息： ICorDebugCode：： GetCode 方法
title: ICorDebugCode::GetCode 方法
ms.date: 03/30/2017
api_name:
- ICorDebugCode.GetCode
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::GetCode
helpviewer_keywords:
- ICorDebugCode::GetCode method [.NET Framework debugging]
- GetCode method, ICorDebugCode interface [.NET Framework debugging]
ms.assetid: 7137e3d1-1dad-48d8-8c37-16ac816534d3
topic_type:
- apiref
ms.openlocfilehash: 329770fac4f2b375c01dd68e4ea7114e59c609b5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711279"
---
# <a name="icordebugcodegetcode-method"></a><span data-ttu-id="2d27e-103">ICorDebugCode::GetCode 方法</span><span class="sxs-lookup"><span data-stu-id="2d27e-103">ICorDebugCode::GetCode Method</span></span>

<span data-ttu-id="2d27e-104">获取用于反汇编的指定函数的所有代码。</span><span class="sxs-lookup"><span data-stu-id="2d27e-104">Gets all the code for the specified function, formatted for disassembly.</span></span> <span data-ttu-id="2d27e-105">此方法在 .NET Framework 版本2.0 中已弃用。</span><span class="sxs-lookup"><span data-stu-id="2d27e-105">This method has been deprecated in the .NET Framework version 2.0.</span></span> <span data-ttu-id="2d27e-106">改 [为使用 ICorDebugCode2：： GetCodeChunks](icordebugcode2-getcodechunks-method.md) 。</span><span class="sxs-lookup"><span data-stu-id="2d27e-106">Use [ICorDebugCode2::GetCodeChunks](icordebugcode2-getcodechunks-method.md) instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2d27e-107">语法</span><span class="sxs-lookup"><span data-stu-id="2d27e-107">Syntax</span></span>  
  
```cpp  
HRESULT GetCode (  
    [in] ULONG32     startOffset,
    [in] ULONG32     endOffset,  
    [in] ULONG32     cBufferAlloc,  
    [out, size_is(cBufferAlloc),  
        length_is(*pcBufferSize)] BYTE buffer[],  
    [out] ULONG32    *pcBufferSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2d27e-108">参数</span><span class="sxs-lookup"><span data-stu-id="2d27e-108">Parameters</span></span>  

 `startOffset`  
 <span data-ttu-id="2d27e-109">中函数开头的偏移量。</span><span class="sxs-lookup"><span data-stu-id="2d27e-109">[in] The offset of the beginning of the function.</span></span>  
  
 `endOffset`  
 <span data-ttu-id="2d27e-110">中函数末尾的偏移量。</span><span class="sxs-lookup"><span data-stu-id="2d27e-110">[in] The offset of the end of the function.</span></span>  
  
 `cBufferAlloc`  
 <span data-ttu-id="2d27e-111">中 `buffer` 将返回代码的数组的大小。</span><span class="sxs-lookup"><span data-stu-id="2d27e-111">[in] The size of the `buffer` array into which the code will be returned.</span></span>  
  
 `buffer`  
 <span data-ttu-id="2d27e-112">弄将向其中返回代码的数组。</span><span class="sxs-lookup"><span data-stu-id="2d27e-112">[out] The array into which the code will be returned.</span></span>  
  
 `pcBufferSize`  
 <span data-ttu-id="2d27e-113">弄返回的字节数。</span><span class="sxs-lookup"><span data-stu-id="2d27e-113">[out] The number of bytes returned.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2d27e-114">备注</span><span class="sxs-lookup"><span data-stu-id="2d27e-114">Remarks</span></span>  

 <span data-ttu-id="2d27e-115">如果函数的代码已划分为多个块，则它们将按照增加的本机偏移量的顺序进行连接。</span><span class="sxs-lookup"><span data-stu-id="2d27e-115">If the function's code has been divided into multiple chunks, they are concatenated in order of increasing native offset.</span></span> <span data-ttu-id="2d27e-116">不检查指令边界。</span><span class="sxs-lookup"><span data-stu-id="2d27e-116">Instruction boundaries are not checked.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2d27e-117">要求</span><span class="sxs-lookup"><span data-stu-id="2d27e-117">Requirements</span></span>  

 <span data-ttu-id="2d27e-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2d27e-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2d27e-119">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2d27e-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2d27e-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2d27e-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2d27e-121">**.NET Framework 版本：** 1.1、1。0</span><span class="sxs-lookup"><span data-stu-id="2d27e-121">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2d27e-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="2d27e-122">See also</span></span>

- [<span data-ttu-id="2d27e-123">GetCodeChunks 方法</span><span class="sxs-lookup"><span data-stu-id="2d27e-123">GetCodeChunks Method</span></span>](icordebugcode2-getcodechunks-method.md)
