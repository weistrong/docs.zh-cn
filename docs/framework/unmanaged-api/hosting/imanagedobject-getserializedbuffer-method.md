---
description: 了解详细信息： IManagedObject：： GetSerializedBuffer 方法
title: IManagedObject::GetSerializedBuffer 方法
ms.date: 03/30/2017
api_name:
- IManagedObject.GetSerializedBuffer
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- GetSerializedBuffer
helpviewer_keywords:
- IManagedObject::GetSerializedBuffer method [.NET Framework hosting]
- GetSerializedBuffer method [.NET Framework hosting]
ms.assetid: c17105bb-b49f-434e-8f9b-77f8c85b9220
topic_type:
- apiref
ms.openlocfilehash: f324b6ed1e9cea21fec9027a954fbad54174dd0c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753765"
---
# <a name="imanagedobjectgetserializedbuffer-method"></a><span data-ttu-id="a3f79-103">IManagedObject::GetSerializedBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="a3f79-103">IManagedObject::GetSerializedBuffer Method</span></span>

<span data-ttu-id="a3f79-104">获取此托管对象的字符串表示形式。</span><span class="sxs-lookup"><span data-stu-id="a3f79-104">Gets the string representation of this managed object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a3f79-105">语法</span><span class="sxs-lookup"><span data-stu-id="a3f79-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSerializedBuffer (  
    [out] BSTR *pBSTR  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a3f79-106">参数</span><span class="sxs-lookup"><span data-stu-id="a3f79-106">Parameters</span></span>  

 `pBSTR`  
 <span data-ttu-id="a3f79-107">弄指向字符串的指针，该字符串是序列化的对象。</span><span class="sxs-lookup"><span data-stu-id="a3f79-107">[out] A pointer to a string that is the serialized object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a3f79-108">备注</span><span class="sxs-lookup"><span data-stu-id="a3f79-108">Remarks</span></span>  

 <span data-ttu-id="a3f79-109">`GetSerializedBuffer`方法会序列化对象，以便将其封送到客户端。</span><span class="sxs-lookup"><span data-stu-id="a3f79-109">The `GetSerializedBuffer` method serializes the object so it can be marshaled to the client.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a3f79-110">要求</span><span class="sxs-lookup"><span data-stu-id="a3f79-110">Requirements</span></span>  

 <span data-ttu-id="a3f79-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a3f79-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a3f79-112">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="a3f79-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a3f79-113">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a3f79-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a3f79-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a3f79-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a3f79-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="a3f79-115">See also</span></span>

- [<span data-ttu-id="a3f79-116">IManagedObject 接口</span><span class="sxs-lookup"><span data-stu-id="a3f79-116">IManagedObject Interface</span></span>](imanagedobject-interface.md)
