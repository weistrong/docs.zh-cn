---
description: 了解详细信息： ISymUnmanagedDocument：： GetSourceLength 方法
title: ISymUnmanagedDocument::GetSourceLength 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetSourceLength
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetSourceLength
helpviewer_keywords:
- GetSourceLength method [.NET Framework debugging]
- ISymUnmanagedDocument::GetSourceLength method [.NET Framework debugging]
ms.assetid: e087dbbb-f4fb-4fbe-8292-e4f1a14d0df2
topic_type:
- apiref
ms.openlocfilehash: 91ac1327afc84458c87122dddc31d0f5b2186f10
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721510"
---
# <a name="isymunmanageddocumentgetsourcelength-method"></a><span data-ttu-id="bbab1-103">ISymUnmanagedDocument::GetSourceLength 方法</span><span class="sxs-lookup"><span data-stu-id="bbab1-103">ISymUnmanagedDocument::GetSourceLength Method</span></span>

<span data-ttu-id="bbab1-104">获取嵌入源的长度（以字节表示）。</span><span class="sxs-lookup"><span data-stu-id="bbab1-104">Gets the length, in bytes, of the embedded source.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bbab1-105">语法</span><span class="sxs-lookup"><span data-stu-id="bbab1-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSourceLength(  
    [out, retval]  ULONG32*  pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bbab1-106">参数</span><span class="sxs-lookup"><span data-stu-id="bbab1-106">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="bbab1-107">弄指向变量的指针，该变量指示嵌入源的长度（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="bbab1-107">[out] A pointer to a variable that indicates the length, in bytes, of the embedded source.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="bbab1-108">返回值</span><span class="sxs-lookup"><span data-stu-id="bbab1-108">Return Value</span></span>  

 <span data-ttu-id="bbab1-109">如果方法成功，则 S_OK。</span><span class="sxs-lookup"><span data-stu-id="bbab1-109">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bbab1-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="bbab1-110">See also</span></span>

- [<span data-ttu-id="bbab1-111">ISymUnmanagedDocument 接口</span><span class="sxs-lookup"><span data-stu-id="bbab1-111">ISymUnmanagedDocument Interface</span></span>](isymunmanageddocument-interface.md)
