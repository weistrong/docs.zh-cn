---
description: 了解详细信息： ICorDebugILFrame：： GetLocalVariable 方法
title: ICorDebugILFrame::GetLocalVariable 方法
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame.GetLocalVariable
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugILFrame::GetLocalVariable
helpviewer_keywords:
- ICorDebugILFrame::GetLocalVariable method [.NET Framework debugging]
- GetLocalVariable method [.NET Framework debugging]
ms.assetid: c8706356-d50b-4f87-a40c-39c3b7f4fd38
topic_type:
- apiref
ms.openlocfilehash: c4bb3e5a5d970539607efbaf55f3f7f08f7e72af
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791369"
---
# <a name="icordebugilframegetlocalvariable-method"></a><span data-ttu-id="3e393-103">ICorDebugILFrame::GetLocalVariable 方法</span><span class="sxs-lookup"><span data-stu-id="3e393-103">ICorDebugILFrame::GetLocalVariable Method</span></span>

<span data-ttu-id="3e393-104">获取此 Microsoft 中间语言 (MSIL) 堆栈帧中的指定局部变量的值。</span><span class="sxs-lookup"><span data-stu-id="3e393-104">Gets the value of the specified local variable in this Microsoft intermediate language (MSIL) stack frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3e393-105">语法</span><span class="sxs-lookup"><span data-stu-id="3e393-105">Syntax</span></span>  
  
```cpp  
HRESULT GetLocalVariable (  
    [in] DWORD                  dwIndex,  
    [out] ICorDebugValue        **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3e393-106">参数</span><span class="sxs-lookup"><span data-stu-id="3e393-106">Parameters</span></span>  

 `dwIndex`  
 <span data-ttu-id="3e393-107">中此 MSIL 堆栈帧中的局部变量的索引。</span><span class="sxs-lookup"><span data-stu-id="3e393-107">[in] The index of the local variable in this MSIL stack frame.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="3e393-108">[out] 一个指向 ICorDebugValue 对象地址的指针，该对象表示检索到的值。</span><span class="sxs-lookup"><span data-stu-id="3e393-108">[out] A pointer to the address of an ICorDebugValue object that represents the retrieved value.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3e393-109">备注</span><span class="sxs-lookup"><span data-stu-id="3e393-109">Remarks</span></span>  

 <span data-ttu-id="3e393-110">`GetLocalVariable`方法既可以在 MSIL 堆栈帧中使用，也可以在实时 (JIT) 编译的框架中使用。</span><span class="sxs-lookup"><span data-stu-id="3e393-110">The `GetLocalVariable` method can be used either in an MSIL stack frame or in a just-in-time (JIT) compiled frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3e393-111">要求</span><span class="sxs-lookup"><span data-stu-id="3e393-111">Requirements</span></span>  

 <span data-ttu-id="3e393-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3e393-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3e393-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3e393-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3e393-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3e393-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3e393-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3e393-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
