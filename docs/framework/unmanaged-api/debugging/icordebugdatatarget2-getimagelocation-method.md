---
description: 了解详细信息： ICorDebugDataTarget2：： GetImageLocation 方法
title: ICorDebugDataTarget2::GetImageLocation 方法
ms.date: 03/30/2017
ms.assetid: 696afe71-5852-478d-a33f-b2d2dbc4b91f
ms.openlocfilehash: f79ba89d3ba467c2e81224d64147c2b5dd5db079
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710486"
---
# <a name="icordebugdatatarget2getimagelocation-method"></a><span data-ttu-id="b17b1-103">ICorDebugDataTarget2::GetImageLocation 方法</span><span class="sxs-lookup"><span data-stu-id="b17b1-103">ICorDebugDataTarget2::GetImageLocation Method</span></span>

<span data-ttu-id="b17b1-104">返回模块基址中的模块路径。</span><span class="sxs-lookup"><span data-stu-id="b17b1-104">Returns the path of a module from the module's base address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b17b1-105">语法</span><span class="sxs-lookup"><span data-stu-id="b17b1-105">Syntax</span></span>  
  
```cpp  
HRESULT GetImageLocation(    [in] CORDB_ADDRESS baseAddress,  
    [in] ULONG32 cchName,  
    [out] ULONG32 *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b17b1-106">参数</span><span class="sxs-lookup"><span data-stu-id="b17b1-106">Parameters</span></span>  

 `baseAddress`  
 <span data-ttu-id="b17b1-107">中一个 [CORDB_ADDRESS](../common-data-types-unmanaged-api-reference.md) 值，该值表示模块的基址。</span><span class="sxs-lookup"><span data-stu-id="b17b1-107">[in] A [CORDB_ADDRESS](../common-data-types-unmanaged-api-reference.md) value that represents the module's base address.</span></span>  
  
 `cchName`  
 <span data-ttu-id="b17b1-108">[输入] 缓冲器中将接收模块路径的字符数。</span><span class="sxs-lookup"><span data-stu-id="b17b1-108">[in] The number of characters in the buffer that is to receive the module path.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="b17b1-109">[输出] 指针指向写入 `szName` 缓冲器的字符数。</span><span class="sxs-lookup"><span data-stu-id="b17b1-109">[out] A pointer to the number of characters written to the `szName` buffer.</span></span>  
  
 `szName`  
 <span data-ttu-id="b17b1-110">[输出] 模块路径。</span><span class="sxs-lookup"><span data-stu-id="b17b1-110">[out] The path of the module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b17b1-111">备注</span><span class="sxs-lookup"><span data-stu-id="b17b1-111">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="b17b1-112">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="b17b1-112">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b17b1-113">要求</span><span class="sxs-lookup"><span data-stu-id="b17b1-113">Requirements</span></span>  

 <span data-ttu-id="b17b1-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b17b1-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b17b1-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b17b1-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b17b1-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b17b1-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b17b1-117">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b17b1-117">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b17b1-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="b17b1-118">See also</span></span>

- [<span data-ttu-id="b17b1-119">“ICor调试数据目标2”接口</span><span class="sxs-lookup"><span data-stu-id="b17b1-119">ICorDebugDataTarget2 Interface</span></span>](icordebugdatatarget2-interface.md)
- [<span data-ttu-id="b17b1-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="b17b1-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
