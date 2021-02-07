---
description: 了解详细信息： ISymUnmanagedWriter：： SetSymAttribute 方法
title: ISymUnmanagedWriter::SetSymAttribute 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.SetSymAttribute
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::SetSymAttribute
helpviewer_keywords:
- SetSymAttribute method [.NET Framework debugging]
- ISymUnmanagedWriter::SetSymAttribute method [.NET Framework debugging]
ms.assetid: 64d9b80e-b883-4539-89c7-03573185a1eb
topic_type:
- apiref
ms.openlocfilehash: 0509e6430646fa67112b29d30d5053eb4a541415
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761988"
---
# <a name="isymunmanagedwritersetsymattribute-method"></a><span data-ttu-id="ff6d5-103">ISymUnmanagedWriter::SetSymAttribute 方法</span><span class="sxs-lookup"><span data-stu-id="ff6d5-103">ISymUnmanagedWriter::SetSymAttribute Method</span></span>

<span data-ttu-id="ff6d5-104">基于名称定义自定义属性。</span><span class="sxs-lookup"><span data-stu-id="ff6d5-104">Defines a custom attribute based upon its name.</span></span> <span data-ttu-id="ff6d5-105">这些特性保存在符号存储区中，与元数据自定义特性不同。</span><span class="sxs-lookup"><span data-stu-id="ff6d5-105">These attributes are held in the symbol store, unlike metadata custom attributes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ff6d5-106">语法</span><span class="sxs-lookup"><span data-stu-id="ff6d5-106">Syntax</span></span>  
  
```cpp  
HRESULT SetSymAttribute(  
    [in] mdToken parent,  
    [in] const WCHAR *name,  
    [in] ULONG32 cData,  
    [in, size_is(cData)] unsigned char data[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ff6d5-107">参数</span><span class="sxs-lookup"><span data-stu-id="ff6d5-107">Parameters</span></span>  

 `parent`  
 <span data-ttu-id="ff6d5-108">中正在为其定义特性的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="ff6d5-108">[in] The metadata token for which the attribute is being defined.</span></span>  
  
 `name`  
 <span data-ttu-id="ff6d5-109">中指向 `WCHAR` 包含特性名称的的指针。</span><span class="sxs-lookup"><span data-stu-id="ff6d5-109">[in] A pointer to a `WCHAR` that contains the attribute name.</span></span>  
  
 `cData`  
 <span data-ttu-id="ff6d5-110">中 `ULONG32` 指示数组大小的 `data` 。</span><span class="sxs-lookup"><span data-stu-id="ff6d5-110">[in] A `ULONG32` that indicates the size of the `data` array.</span></span>  
  
 `data`  
 <span data-ttu-id="ff6d5-111">中特性值。</span><span class="sxs-lookup"><span data-stu-id="ff6d5-111">[in] The attribute value.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ff6d5-112">返回值</span><span class="sxs-lookup"><span data-stu-id="ff6d5-112">Return Value</span></span>  

 <span data-ttu-id="ff6d5-113">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="ff6d5-113">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ff6d5-114">要求</span><span class="sxs-lookup"><span data-stu-id="ff6d5-114">Requirements</span></span>  

 <span data-ttu-id="ff6d5-115">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="ff6d5-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ff6d5-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="ff6d5-116">See also</span></span>

- [<span data-ttu-id="ff6d5-117">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="ff6d5-117">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
