---
description: 了解详细信息： ISymUnmanagedReader：： GetSymbolStoreFileName 方法
title: ISymUnmanagedReader::GetSymbolStoreFileName 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetSymbolStoreFileName
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetSymbolStoreFileName
helpviewer_keywords:
- GetSymbolStoreFileName method [.NET Framework debugging]
- ISymUnmanagedReader::GetSymbolStoreFileName method [.NET Framework debugging]
ms.assetid: c84f4846-9bc8-44a4-9a76-e39106d6d8b2
topic_type:
- apiref
ms.openlocfilehash: 5cbb33a39cf2e93eab64d5f1f1fefc5ceba1d418
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763938"
---
# <a name="isymunmanagedreadergetsymbolstorefilename-method"></a><span data-ttu-id="beaf5-103">ISymUnmanagedReader::GetSymbolStoreFileName 方法</span><span class="sxs-lookup"><span data-stu-id="beaf5-103">ISymUnmanagedReader::GetSymbolStoreFileName Method</span></span>

<span data-ttu-id="beaf5-104">提供符号存储区的磁盘上的文件名。</span><span class="sxs-lookup"><span data-stu-id="beaf5-104">Provides the on-disk file name of the symbol store.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="beaf5-105">语法</span><span class="sxs-lookup"><span data-stu-id="beaf5-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSymbolStoreFileName (  
    [in]  ULONG32 cchName,  
    [out] ULONG32 *pcchName,  
    [out, size_is (cchName),  
        length_is (*pcchName)] WCHAR szName[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="beaf5-106">参数</span><span class="sxs-lookup"><span data-stu-id="beaf5-106">Parameters</span></span>  

 `cchName`  
 <span data-ttu-id="beaf5-107">中缓冲区的大小 `szName` 。</span><span class="sxs-lookup"><span data-stu-id="beaf5-107">[in] The size of the `szName` buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="beaf5-108">弄指向一个变量的指针，该变量接收返回的名称的长度 `szName` （包括 null 终止）。</span><span class="sxs-lookup"><span data-stu-id="beaf5-108">[out] A pointer to the variable that receives the length of the name returned in `szName`, including the null termination.</span></span>  
  
 `szName`  
 <span data-ttu-id="beaf5-109">弄指向接收符号存储区文件名的变量的指针。</span><span class="sxs-lookup"><span data-stu-id="beaf5-109">[out] A pointer to the variable that receives the file name of the symbol store.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="beaf5-110">返回值</span><span class="sxs-lookup"><span data-stu-id="beaf5-110">Return Value</span></span>  

 <span data-ttu-id="beaf5-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="beaf5-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="beaf5-112">要求</span><span class="sxs-lookup"><span data-stu-id="beaf5-112">Requirements</span></span>  

 <span data-ttu-id="beaf5-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="beaf5-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="beaf5-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="beaf5-114">See also</span></span>

- [<span data-ttu-id="beaf5-115">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="beaf5-115">ISymUnmanagedReader Interface</span></span>](isymunmanagedreader-interface.md)
