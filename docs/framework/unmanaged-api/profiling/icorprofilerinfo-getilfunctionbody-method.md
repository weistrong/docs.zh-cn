---
description: 了解详细信息： ICorProfilerInfo：： GetILFunctionBody 方法
title: ICorProfilerInfo::GetILFunctionBody 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetILFunctionBody
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetILFunctionBody
helpviewer_keywords:
- GetILFunctionBody method [.NET Framework profiling]
- ICorProfilerInfo::GetILFunctionBody method [.NET Framework profiling]
ms.assetid: e29b46bc-5fdc-4894-b0c2-619df4b65ded
topic_type:
- apiref
ms.openlocfilehash: 7294592d1a2747dc10f44d1206561a9a1662ce7b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99647474"
---
# <a name="icorprofilerinfogetilfunctionbody-method"></a><span data-ttu-id="e57db-103">ICorProfilerInfo::GetILFunctionBody 方法</span><span class="sxs-lookup"><span data-stu-id="e57db-103">ICorProfilerInfo::GetILFunctionBody Method</span></span>

<span data-ttu-id="e57db-104">获取一个指针，该指针指向 Microsoft 中间语言 (MSIL) 代码的方法体，从其标头开始。</span><span class="sxs-lookup"><span data-stu-id="e57db-104">Gets a pointer to the body of a method in Microsoft intermediate language (MSIL) code, starting at its header.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e57db-105">语法</span><span class="sxs-lookup"><span data-stu-id="e57db-105">Syntax</span></span>  
  
```cpp  
HRESULT GetILFunctionBody(  
    [in]  ModuleID    moduleId,  
    [in]  mdMethodDef methodId,  
    [out] LPCBYTE     *ppMethodHeader,  
    [out] ULONG       *pcbMethodSize);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e57db-106">参数</span><span class="sxs-lookup"><span data-stu-id="e57db-106">Parameters</span></span>  

 `moduleId`  
 <span data-ttu-id="e57db-107">中函数所在模块的 ID。</span><span class="sxs-lookup"><span data-stu-id="e57db-107">[in] The ID of the module in which the function resides.</span></span>  
  
 `methodId`  
 <span data-ttu-id="e57db-108">中方法的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="e57db-108">[in] The metadata token for the method.</span></span>  
  
 `ppMethodHeader`  
 <span data-ttu-id="e57db-109">弄指向方法的标头的指针。</span><span class="sxs-lookup"><span data-stu-id="e57db-109">[out] A pointer to the method's header.</span></span>  
  
 `pcbMethodSize`  
 <span data-ttu-id="e57db-110">弄一个整数，指定方法的大小。</span><span class="sxs-lookup"><span data-stu-id="e57db-110">[out] An integer that specifies the size of the method.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e57db-111">备注</span><span class="sxs-lookup"><span data-stu-id="e57db-111">Remarks</span></span>  

 <span data-ttu-id="e57db-112">方法的作用域由其所在的模块确定。</span><span class="sxs-lookup"><span data-stu-id="e57db-112">A method is scoped by the module in which it lives.</span></span> <span data-ttu-id="e57db-113">由于 `GetILFunctionBody` 方法旨在在公共语言运行时 (CLR) 加载 MSIL 代码之前提供对这些代码的访问权限，因此它使用方法的元数据标记来查找所需的实例。</span><span class="sxs-lookup"><span data-stu-id="e57db-113">Because the `GetILFunctionBody` method is designed to give a tool access to the MSIL code before it has been loaded by the common language runtime (CLR), it uses the metadata token of the method to find the desired instance.</span></span>  
  
 <span data-ttu-id="e57db-114">`GetILFunctionBody` 如果 `methodId` 指向不包含任何 MSIL 代码的方法 (（如抽象方法）或平台调用 (PInvoke) 方法) ，则可以返回 CORPROF_E_FUNCTION_NOT_IL HRESULT。</span><span class="sxs-lookup"><span data-stu-id="e57db-114">`GetILFunctionBody` can return a CORPROF_E_FUNCTION_NOT_IL HRESULT if the `methodId` points to a method without any MSIL code (such as an abstract method, or a platform invoke (PInvoke) method).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e57db-115">要求</span><span class="sxs-lookup"><span data-stu-id="e57db-115">Requirements</span></span>  

 <span data-ttu-id="e57db-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e57db-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e57db-117">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e57db-117">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e57db-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e57db-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e57db-119">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e57db-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e57db-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="e57db-120">See also</span></span>

- [<span data-ttu-id="e57db-121">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="e57db-121">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
