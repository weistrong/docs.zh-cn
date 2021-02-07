---
description: 了解详细信息： ICorDebugProcess6：： GetExportStepInfo 方法
title: ICorDebugProcess6::GetExportStepInfo 方法
ms.date: 03/30/2017
ms.assetid: a927e0ac-f110-426d-bbec-9377a29c8f17
ms.openlocfilehash: e14b5e66d90fb2ece91991b3634fc2ad86fac895
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722004"
---
# <a name="icordebugprocess6getexportstepinfo-method"></a><span data-ttu-id="7f1fd-103">ICorDebugProcess6::GetExportStepInfo 方法</span><span class="sxs-lookup"><span data-stu-id="7f1fd-103">ICorDebugProcess6::GetExportStepInfo Method</span></span>

<span data-ttu-id="7f1fd-104">提供运行时导出功能信息以帮助单步调试托管代码。</span><span class="sxs-lookup"><span data-stu-id="7f1fd-104">Provides information on runtime exported functions to help step through managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7f1fd-105">语法</span><span class="sxs-lookup"><span data-stu-id="7f1fd-105">Syntax</span></span>  
  
```cpp  
HRESULT GetExportStepInfo(  
    [in] LPCWSTR pszExportName,
    [out] CorDebugCodeInvokeKind* pInvokeKind,
    [out] CorDebugCodeInvokePurpose* pInvokePurpose);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7f1fd-106">参数</span><span class="sxs-lookup"><span data-stu-id="7f1fd-106">Parameters</span></span>  

 <span data-ttu-id="7f1fd-107">psz导出名</span><span class="sxs-lookup"><span data-stu-id="7f1fd-107">pszExportName</span></span>  
 <span data-ttu-id="7f1fd-108">[输入] 如 PE 导出表中所写的运行时间导出函数名。</span><span class="sxs-lookup"><span data-stu-id="7f1fd-108">[in] The name of a runtime export function as written in the PE export table.</span></span>  
  
 <span data-ttu-id="7f1fd-109">调用类型</span><span class="sxs-lookup"><span data-stu-id="7f1fd-109">invokeKind</span></span>  
 <span data-ttu-id="7f1fd-110">弄一个指针，指向 [CorDebugCodeInvokeKind](cordebugcodeinvokekind-enumeration.md) 枚举的成员，该枚举描述导出函数将如何调用托管代码。</span><span class="sxs-lookup"><span data-stu-id="7f1fd-110">[out] A pointer to a member of the [CorDebugCodeInvokeKind](cordebugcodeinvokekind-enumeration.md) enumeration that describes how the exported function will invoke managed code.</span></span>  
  
 <span data-ttu-id="7f1fd-111">调用目的</span><span class="sxs-lookup"><span data-stu-id="7f1fd-111">invokePurpose</span></span>  
 <span data-ttu-id="7f1fd-112">弄指向 [CorDebugCodeInvokePurpose](cordebugcodeinvokepurpose-enumeration.md) 枚举的成员的指针，该成员描述导出函数将调用托管代码的原因。</span><span class="sxs-lookup"><span data-stu-id="7f1fd-112">[out] A pointer to a member of the [CorDebugCodeInvokePurpose](cordebugcodeinvokepurpose-enumeration.md) enumeration that describes why the exported function will call managed code.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7f1fd-113">返回值</span><span class="sxs-lookup"><span data-stu-id="7f1fd-113">Return Value</span></span>  

 <span data-ttu-id="7f1fd-114">该方法可以返回下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="7f1fd-114">The method can return the values listed in the following table.</span></span>  
  
|<span data-ttu-id="7f1fd-115">返回值</span><span class="sxs-lookup"><span data-stu-id="7f1fd-115">Return value</span></span>|<span data-ttu-id="7f1fd-116">说明</span><span class="sxs-lookup"><span data-stu-id="7f1fd-116">Description</span></span>|  
|------------------|-----------------|  
|`S_OK`|<span data-ttu-id="7f1fd-117">方法调用成功。</span><span class="sxs-lookup"><span data-stu-id="7f1fd-117">The method call was successful.</span></span>|  
|`E_POINTER`|<span data-ttu-id="7f1fd-118">`pInvokeKind` 或 `pInvokePurpose` 为 **null**。</span><span class="sxs-lookup"><span data-stu-id="7f1fd-118">`pInvokeKind` or `pInvokePurpose` is **null**.</span></span>|  
|<span data-ttu-id="7f1fd-119">其他失败 `HRESULT` 值。</span><span class="sxs-lookup"><span data-stu-id="7f1fd-119">Other failing `HRESULT` values.</span></span>|<span data-ttu-id="7f1fd-120">根据需要。</span><span class="sxs-lookup"><span data-stu-id="7f1fd-120">As appropriate.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7f1fd-121">备注</span><span class="sxs-lookup"><span data-stu-id="7f1fd-121">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="7f1fd-122">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="7f1fd-122">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7f1fd-123">要求</span><span class="sxs-lookup"><span data-stu-id="7f1fd-123">Requirements</span></span>  

 <span data-ttu-id="7f1fd-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7f1fd-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7f1fd-125">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7f1fd-125">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7f1fd-126">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7f1fd-126">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7f1fd-127">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7f1fd-127">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7f1fd-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="7f1fd-128">See also</span></span>

- [<span data-ttu-id="7f1fd-129">“ICor调试进程6”接口</span><span class="sxs-lookup"><span data-stu-id="7f1fd-129">ICorDebugProcess6 Interface</span></span>](icordebugprocess6-interface.md)
- [<span data-ttu-id="7f1fd-130">调试接口</span><span class="sxs-lookup"><span data-stu-id="7f1fd-130">Debugging Interfaces</span></span>](debugging-interfaces.md)
