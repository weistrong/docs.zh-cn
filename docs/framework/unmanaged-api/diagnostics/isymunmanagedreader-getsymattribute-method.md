---
description: 了解详细信息： ISymUnmanagedReader：： GetSymAttribute 方法
title: ISymUnmanagedReader::GetSymAttribute 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetSymAttribute
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetSymAttribute
helpviewer_keywords:
- GetSymAttribute method [.NET Framework debugging]
- ISymUnmanagedReader::GetSymAttribute method [.NET Framework debugging]
ms.assetid: c675ce7e-76e7-45ff-8273-3b6489a2767c
topic_type:
- apiref
ms.openlocfilehash: cd1c453e9f2ef68799fc5eccf1288a7665c5cfdf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763964"
---
# <a name="isymunmanagedreadergetsymattribute-method"></a><span data-ttu-id="83ec8-103">ISymUnmanagedReader::GetSymAttribute 方法</span><span class="sxs-lookup"><span data-stu-id="83ec8-103">ISymUnmanagedReader::GetSymAttribute Method</span></span>

<span data-ttu-id="83ec8-104">根据名称获取自定义属性。</span><span class="sxs-lookup"><span data-stu-id="83ec8-104">Gets a custom attribute based upon its name.</span></span> <span data-ttu-id="83ec8-105">与元数据自定义属性不同，这些自定义属性保存在符号存储区中。</span><span class="sxs-lookup"><span data-stu-id="83ec8-105">Unlike metadata custom attributes, these custom attributes are held in the symbol store.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="83ec8-106">语法</span><span class="sxs-lookup"><span data-stu-id="83ec8-106">Syntax</span></span>  
  
```cpp  
HRESULT GetSymAttribute (  
    [in]  mdToken  parent,  
    [in]  WCHAR    *name,  
    [in]  ULONG32  cBuffer,  
    [out] ULONG32  *pcBuffer,  
    [out, size_is (cBuffer),  
        length_is (*pcBuffer)] BYTE buffer[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="83ec8-107">参数</span><span class="sxs-lookup"><span data-stu-id="83ec8-107">Parameters</span></span>  

 `parent`  
 <span data-ttu-id="83ec8-108">中请求其属性的对象的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="83ec8-108">[in] The metadata token for the object for which the attribute is requested.</span></span>  
  
 `name`  
 <span data-ttu-id="83ec8-109">中指向变量的指针，该变量指示要检索的属性。</span><span class="sxs-lookup"><span data-stu-id="83ec8-109">[in] A pointer to the variable that indicates the attribute to retrieve.</span></span>  
  
 `cBuffer`  
 <span data-ttu-id="83ec8-110">[in] `buffer` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="83ec8-110">[in] The size of the `buffer` array.</span></span>  
  
 `pcBuffer`  
 <span data-ttu-id="83ec8-111">弄指向接收属性数据长度的变量的指针。</span><span class="sxs-lookup"><span data-stu-id="83ec8-111">[out] A pointer to the variable that receives the length of the attribute data.</span></span>  
  
 `buffer`  
 <span data-ttu-id="83ec8-112">弄指向接收特性数据的变量的指针。</span><span class="sxs-lookup"><span data-stu-id="83ec8-112">[out] A pointer to the variable that receives the attribute data.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="83ec8-113">返回值</span><span class="sxs-lookup"><span data-stu-id="83ec8-113">Return Value</span></span>  

 <span data-ttu-id="83ec8-114">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="83ec8-114">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="83ec8-115">要求</span><span class="sxs-lookup"><span data-stu-id="83ec8-115">Requirements</span></span>  

 <span data-ttu-id="83ec8-116">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="83ec8-116">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="83ec8-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="83ec8-117">See also</span></span>

- [<span data-ttu-id="83ec8-118">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="83ec8-118">ISymUnmanagedReader Interface</span></span>](isymunmanagedreader-interface.md)
