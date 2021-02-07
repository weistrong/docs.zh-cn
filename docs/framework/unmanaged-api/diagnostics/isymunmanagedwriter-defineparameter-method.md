---
description: 了解详细信息： ISymUnmanagedWriter：:D efineParameter 方法
title: ISymUnmanagedWriter::DefineParameter 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.DefineParameter
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::DefineParameter
helpviewer_keywords:
- DefineParameter method [.NET Framework debugging]
- ISymUnmanagedWriter::DefineParameter method [.NET Framework debugging]
ms.assetid: a8e3dd32-6a44-4371-9a74-f417b11998c8
topic_type:
- apiref
ms.openlocfilehash: 1e42140e33a99b224ccf3eff7ea29b7aa3ff1b15
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762352"
---
# <a name="isymunmanagedwriterdefineparameter-method"></a><span data-ttu-id="eb0f9-103">ISymUnmanagedWriter::DefineParameter 方法</span><span class="sxs-lookup"><span data-stu-id="eb0f9-103">ISymUnmanagedWriter::DefineParameter Method</span></span>

<span data-ttu-id="eb0f9-104">在当前方法中定义单个参数。</span><span class="sxs-lookup"><span data-stu-id="eb0f9-104">Defines a single parameter in the current method.</span></span> <span data-ttu-id="eb0f9-105">参数类型从参数的位置获取， (序列) 在方法的签名中。</span><span class="sxs-lookup"><span data-stu-id="eb0f9-105">The parameter type is taken from the parameter's position (sequence) within the method's signature.</span></span>  
  
 <span data-ttu-id="eb0f9-106">如果在给定方法的元数据中定义了参数，则无需使用此方法再次定义这些参数。</span><span class="sxs-lookup"><span data-stu-id="eb0f9-106">If parameters are defined in the metadata for a given method, you do not have to define them again by using this method.</span></span> <span data-ttu-id="eb0f9-107">符号读取器必须在检查符号存储区之前检查参数的正常元数据。</span><span class="sxs-lookup"><span data-stu-id="eb0f9-107">The symbol readers must check the normal metadata for the parameters before checking the symbol store.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eb0f9-108">语法</span><span class="sxs-lookup"><span data-stu-id="eb0f9-108">Syntax</span></span>  
  
```cpp  
HRESULT DefineParameter(  
    [in] const WCHAR  *name,  
    [in] ULONG32      attributes,  
    [in] ULONG32      sequence,  
    [in] ULONG32      addrKind,  
    [in] ULONG32      addr1,  
    [in] ULONG32      addr2,  
    [in] ULONG32      addr3);  
```  
  
## <a name="parameters"></a><span data-ttu-id="eb0f9-109">参数</span><span class="sxs-lookup"><span data-stu-id="eb0f9-109">Parameters</span></span>  

 `name`  
 <span data-ttu-id="eb0f9-110">中参数名称。</span><span class="sxs-lookup"><span data-stu-id="eb0f9-110">[in] The parameter name.</span></span>  
  
 `attributes`  
 <span data-ttu-id="eb0f9-111">中参数特性。</span><span class="sxs-lookup"><span data-stu-id="eb0f9-111">[in] The parameter attributes.</span></span>  
  
 `sequence`  
 <span data-ttu-id="eb0f9-112">中参数签名。</span><span class="sxs-lookup"><span data-stu-id="eb0f9-112">[in] The parameter signature.</span></span>  
  
 `addrKind`  
 <span data-ttu-id="eb0f9-113">中地址类型。</span><span class="sxs-lookup"><span data-stu-id="eb0f9-113">[in] The address type.</span></span>  
  
 `addr1`  
 <span data-ttu-id="eb0f9-114">中参数规范的第一个地址。</span><span class="sxs-lookup"><span data-stu-id="eb0f9-114">[in] The first address for the parameter specification.</span></span>  
  
 `addr2`  
 <span data-ttu-id="eb0f9-115">中参数规范的第二个地址。</span><span class="sxs-lookup"><span data-stu-id="eb0f9-115">[in] The second address for the parameter specification.</span></span>  
  
 `addr3`  
 <span data-ttu-id="eb0f9-116">中参数规范的第三个地址。</span><span class="sxs-lookup"><span data-stu-id="eb0f9-116">[in] The third address for the parameter specification.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="eb0f9-117">返回值</span><span class="sxs-lookup"><span data-stu-id="eb0f9-117">Return Value</span></span>  

 <span data-ttu-id="eb0f9-118">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="eb0f9-118">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eb0f9-119">要求</span><span class="sxs-lookup"><span data-stu-id="eb0f9-119">Requirements</span></span>  

 <span data-ttu-id="eb0f9-120">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="eb0f9-120">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb0f9-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="eb0f9-121">See also</span></span>

- [<span data-ttu-id="eb0f9-122">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="eb0f9-122">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
