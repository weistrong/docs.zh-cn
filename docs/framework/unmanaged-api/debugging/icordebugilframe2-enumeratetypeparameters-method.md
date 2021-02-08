---
description: 了解详细信息： ICorDebugILFrame2：： EnumerateTypeParameters 方法
title: ICorDebugILFrame2::EnumerateTypeParameters 方法
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame2.EnumerateTypeParameters
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugILFrame2::EnumerateTypeParameters
helpviewer_keywords:
- EnumerateTypeParameters method, ICorDebugILFrame2 interface [.NET Framework debugging]
- ICorDebugILFrame2::EnumerateTypeParameters method [.NET Framework debugging]
ms.assetid: 722d0d74-e0df-491f-98c4-62d501dfaf6f
topic_type:
- apiref
ms.openlocfilehash: 34f305b7793e4909318ae2301d72e2af7c12f2c1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791281"
---
# <a name="icordebugilframe2enumeratetypeparameters-method"></a><span data-ttu-id="76208-103">ICorDebugILFrame2::EnumerateTypeParameters 方法</span><span class="sxs-lookup"><span data-stu-id="76208-103">ICorDebugILFrame2::EnumerateTypeParameters Method</span></span>

<span data-ttu-id="76208-104">获取一个 ICorDebugTypeEnum 对象，该对象包含 <xref:System.Type> 此帧中的参数。</span><span class="sxs-lookup"><span data-stu-id="76208-104">Gets an ICorDebugTypeEnum object that contains the <xref:System.Type> parameters in this frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="76208-105">语法</span><span class="sxs-lookup"><span data-stu-id="76208-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumerateTypeParameters (  
    [out] ICorDebugTypeEnum    **ppTyParEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="76208-106">参数</span><span class="sxs-lookup"><span data-stu-id="76208-106">Parameters</span></span>  

 `ppTyParEnum`  
 <span data-ttu-id="76208-107">指向允许枚举类型参数的 ICorDebugTypeEnum 接口对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="76208-107">A pointer to the address of a ICorDebugTypeEnum interface object that allows enumeration of type parameters.</span></span>  
  
 <span data-ttu-id="76208-108">类型参数的列表包括类类型参数， (如果任何) 后跟方法类型参数， (if 任何) 。</span><span class="sxs-lookup"><span data-stu-id="76208-108">The list of type parameters include the class type parameters (if any) followed by the method type parameters (if any).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="76208-109">备注</span><span class="sxs-lookup"><span data-stu-id="76208-109">Remarks</span></span>  

 <span data-ttu-id="76208-110">使用 [IMetaDataImport2：： EnumGenericParams](../metadata/imetadataimport2-enumgenericparams-method.md) 方法确定此列表包含多少类类型参数和方法类型参数。</span><span class="sxs-lookup"><span data-stu-id="76208-110">Use the [IMetaDataImport2::EnumGenericParams](../metadata/imetadataimport2-enumgenericparams-method.md) method to determine how many class type parameters and method type parameters this list contains.</span></span>  
  
 <span data-ttu-id="76208-111">类型参数并非始终可用。</span><span class="sxs-lookup"><span data-stu-id="76208-111">The type parameters are not always available.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="76208-112">要求</span><span class="sxs-lookup"><span data-stu-id="76208-112">Requirements</span></span>  

 <span data-ttu-id="76208-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="76208-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="76208-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="76208-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="76208-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="76208-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="76208-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="76208-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
