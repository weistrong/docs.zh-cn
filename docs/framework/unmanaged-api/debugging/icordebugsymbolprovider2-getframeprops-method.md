---
description: 了解详细信息： ICorDebugSymbolProvider2：： GetFrameProps 方法
title: ICorDebugSymbolProvider2::GetFrameProps 方法
ms.date: 03/30/2017
ms.assetid: f07b73f3-188d-43a9-8f7d-44dce2f1ddb7
ms.openlocfilehash: c0286e423f8f395568ad4df94fac38a7ef91c6bd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99659551"
---
# <a name="icordebugsymbolprovider2getframeprops-method"></a><span data-ttu-id="0f9d1-103">ICorDebugSymbolProvider2::GetFrameProps 方法</span><span class="sxs-lookup"><span data-stu-id="0f9d1-103">ICorDebugSymbolProvider2::GetFrameProps Method</span></span>

<span data-ttu-id="0f9d1-104">返回启动方法相对虚拟地址的方法和具有代码相对虚拟地址的父框架。</span><span class="sxs-lookup"><span data-stu-id="0f9d1-104">Returns the method starting relative virtual address of a method and the parent frame given a code relative virtual address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0f9d1-105">语法</span><span class="sxs-lookup"><span data-stu-id="0f9d1-105">Syntax</span></span>  
  
```cpp  
HRESULT GetFrameProps(  
   [in] ULONG32 codeRva,  
   [out] ULONG32 *pCodeStartRva,  
   [out] ULONG32 *pParentFrameStartRva  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0f9d1-106">参数</span><span class="sxs-lookup"><span data-stu-id="0f9d1-106">Parameters</span></span>  

 `codeRva`  
 <span data-ttu-id="0f9d1-107">[in] 代码相对虚拟地址。</span><span class="sxs-lookup"><span data-stu-id="0f9d1-107">[in] A code relative virtual address.</span></span>  
  
 `pCodeStartRva`  
 <span data-ttu-id="0f9d1-108">[out] 指向方法的启动相对虚拟地址的指针。</span><span class="sxs-lookup"><span data-stu-id="0f9d1-108">[out] A pointer to the method's starting relative virtual address.</span></span>  
  
 `pParentFrameStartRva`  
 <span data-ttu-id="0f9d1-109">[out] 指向框架的启动相对虚拟地址的指针。</span><span class="sxs-lookup"><span data-stu-id="0f9d1-109">[out] A pointer to the frame's starting relative virtual address.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0f9d1-110">备注</span><span class="sxs-lookup"><span data-stu-id="0f9d1-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="0f9d1-111">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="0f9d1-111">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0f9d1-112">要求</span><span class="sxs-lookup"><span data-stu-id="0f9d1-112">Requirements</span></span>  

 <span data-ttu-id="0f9d1-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0f9d1-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0f9d1-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0f9d1-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0f9d1-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0f9d1-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0f9d1-116">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0f9d1-116">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0f9d1-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="0f9d1-117">See also</span></span>

- [<span data-ttu-id="0f9d1-118">ICorDebugSymbolProvider2 接口</span><span class="sxs-lookup"><span data-stu-id="0f9d1-118">ICorDebugSymbolProvider2 Interface</span></span>](icordebugsymbolprovider2-interface.md)
- [<span data-ttu-id="0f9d1-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="0f9d1-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
