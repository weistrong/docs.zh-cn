---
description: 了解详细信息： ISymUnmanagedDocument：： GetCheckSumAlgorithmId 方法
title: ISymUnmanagedDocument::GetCheckSumAlgorithmId 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetCheckSumAlgorithmId
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetCheckSumAlgorithmId
helpviewer_keywords:
- ISymUnmanagedDocument::GetCheckSumAlgorithmId method [.NET Framework debugging]
- GetCheckSumAlgorithmId method [.NET Framework debugging]
ms.assetid: c7f941cd-e25b-4b85-b1ce-5f77c9208fa9
topic_type:
- apiref
ms.openlocfilehash: 835f56875a1adc3a3b6617a5a0b280f60f918236
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772115"
---
# <a name="isymunmanageddocumentgetchecksumalgorithmid-method"></a><span data-ttu-id="374f5-103">ISymUnmanagedDocument::GetCheckSumAlgorithmId 方法</span><span class="sxs-lookup"><span data-stu-id="374f5-103">ISymUnmanagedDocument::GetCheckSumAlgorithmId Method</span></span>

<span data-ttu-id="374f5-104">如果没有校验和，则获取校验和算法标识符，或返回所有零的 GUID。</span><span class="sxs-lookup"><span data-stu-id="374f5-104">Gets the checksum algorithm identifier, or returns a GUID of all zeros if there is no checksum.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="374f5-105">语法</span><span class="sxs-lookup"><span data-stu-id="374f5-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCheckSumAlgorithmId(  
    [out, retval] GUID*  pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="374f5-106">参数</span><span class="sxs-lookup"><span data-stu-id="374f5-106">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="374f5-107">弄指向接收校验和算法标识符的变量的指针。</span><span class="sxs-lookup"><span data-stu-id="374f5-107">[out] A pointer to a variable that receives the checksum algorithm identifier.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="374f5-108">返回值</span><span class="sxs-lookup"><span data-stu-id="374f5-108">Return Value</span></span>  

 <span data-ttu-id="374f5-109">如果方法成功，则 S_OK。</span><span class="sxs-lookup"><span data-stu-id="374f5-109">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="374f5-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="374f5-110">See also</span></span>

- [<span data-ttu-id="374f5-111">ISymUnmanagedDocument 接口</span><span class="sxs-lookup"><span data-stu-id="374f5-111">ISymUnmanagedDocument Interface</span></span>](isymunmanageddocument-interface.md)
