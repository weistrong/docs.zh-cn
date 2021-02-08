---
description: 了解详细信息： ISymUnmanagedAsyncMethodPropertiesWriter：:D efineKickoffMethod 方法
title: ISymUnmanagedAsyncMethodPropertiesWriter::DefineKickoffMethod 方法
ms.date: 03/30/2017
ms.assetid: 4662f70d-817b-4374-8da8-e0545585939f
ms.openlocfilehash: 7333823bce27eace4e9cb988ac31252743cca952
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790225"
---
# <a name="isymunmanagedasyncmethodpropertieswriterdefinekickoffmethod-method"></a><span data-ttu-id="b63e3-103">ISymUnmanagedAsyncMethodPropertiesWriter::DefineKickoffMethod 方法</span><span class="sxs-lookup"><span data-stu-id="b63e3-103">ISymUnmanagedAsyncMethodPropertiesWriter::DefineKickoffMethod Method</span></span>

<span data-ttu-id="b63e3-104">设置启动异步操作的启动方法。</span><span class="sxs-lookup"><span data-stu-id="b63e3-104">Sets the starting method that initiates the async operation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b63e3-105">语法</span><span class="sxs-lookup"><span data-stu-id="b63e3-105">Syntax</span></span>  
  
```idl  
HRESULT DefineKickoffMethod(    [in] mdToken kickoffMethod);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b63e3-106">参数</span><span class="sxs-lookup"><span data-stu-id="b63e3-106">Parameters</span></span>  
  
|<span data-ttu-id="b63e3-107">参数</span><span class="sxs-lookup"><span data-stu-id="b63e3-107">Parameter</span></span>|<span data-ttu-id="b63e3-108">说明</span><span class="sxs-lookup"><span data-stu-id="b63e3-108">Description</span></span>|  
|---------------|-----------------|  
|`kickoffMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="b63e3-109">返回值</span><span class="sxs-lookup"><span data-stu-id="b63e3-109">Return Value</span></span>  

 <span data-ttu-id="b63e3-110">返回 `HRESULT`。</span><span class="sxs-lookup"><span data-stu-id="b63e3-110">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b63e3-111">要求</span><span class="sxs-lookup"><span data-stu-id="b63e3-111">Requirements</span></span>  

 <span data-ttu-id="b63e3-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="b63e3-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b63e3-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="b63e3-113">See also</span></span>

- [<span data-ttu-id="b63e3-114">ISymUnmanagedAsyncMethodPropertiesWriter 接口</span><span class="sxs-lookup"><span data-stu-id="b63e3-114">ISymUnmanagedAsyncMethodPropertiesWriter Interface</span></span>](isymunmanagedasyncmethodpropertieswriter-interface.md)
