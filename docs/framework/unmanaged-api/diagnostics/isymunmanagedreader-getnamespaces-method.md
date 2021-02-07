---
description: 了解详细信息： ISymUnmanagedReader：： GetNamespaces 方法
title: ISymUnmanagedReader::GetNamespaces 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetNamespaces
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetNamespaces
helpviewer_keywords:
- ISymUnmanagedReader::GetNamespaces method [.NET Framework debugging]
- GetNamespaces method, ISymUnmanagedReader interface [.NET Framework debugging]
ms.assetid: 3feb4796-2fab-45ce-beca-6f5bc530b971
topic_type:
- apiref
ms.openlocfilehash: 47f7bff829ca2a52eb95d7d7693a7486301de092
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99764003"
---
# <a name="isymunmanagedreadergetnamespaces-method"></a><span data-ttu-id="e4a9a-103">ISymUnmanagedReader::GetNamespaces 方法</span><span class="sxs-lookup"><span data-stu-id="e4a9a-103">ISymUnmanagedReader::GetNamespaces Method</span></span>

<span data-ttu-id="e4a9a-104">获取在此符号存储区的全局范围内定义的命名空间。</span><span class="sxs-lookup"><span data-stu-id="e4a9a-104">Gets the namespaces defined at global scope within this symbol store.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e4a9a-105">语法</span><span class="sxs-lookup"><span data-stu-id="e4a9a-105">Syntax</span></span>  
  
```cpp  
HRESULT GetNamespaces (  
    [in]  ULONG32  cNameSpaces,  
    [out] ULONG32  *pcNameSpaces,  
    [out, size_is (cNameSpaces),  
        length_is (*pcNameSpaces)]  
        ISymUnmanagedNamespace*  namespaces[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e4a9a-106">参数</span><span class="sxs-lookup"><span data-stu-id="e4a9a-106">Parameters</span></span>  

 `cNameSpaces`  
 <span data-ttu-id="e4a9a-107">中命名空间数组的大小。</span><span class="sxs-lookup"><span data-stu-id="e4a9a-107">[in] The size of the namespaces array.</span></span>  
  
 `pcNameSpaces`  
 <span data-ttu-id="e4a9a-108">弄指向一个变量的指针，该变量接收命名空间列表的长度。</span><span class="sxs-lookup"><span data-stu-id="e4a9a-108">[out] A pointer to a variable that receives the length of the namespace list.</span></span>  
  
 `namespaces`  
 <span data-ttu-id="e4a9a-109">弄指向接收命名空间列表的变量的指针。</span><span class="sxs-lookup"><span data-stu-id="e4a9a-109">[out] A pointer to a variable that receives the namespace list.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e4a9a-110">返回值</span><span class="sxs-lookup"><span data-stu-id="e4a9a-110">Return Value</span></span>  

 <span data-ttu-id="e4a9a-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="e4a9a-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e4a9a-112">要求</span><span class="sxs-lookup"><span data-stu-id="e4a9a-112">Requirements</span></span>  

 <span data-ttu-id="e4a9a-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="e4a9a-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e4a9a-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="e4a9a-114">See also</span></span>

- [<span data-ttu-id="e4a9a-115">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="e4a9a-115">ISymUnmanagedReader Interface</span></span>](isymunmanagedreader-interface.md)
