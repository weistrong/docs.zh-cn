---
description: 了解详细信息： ESymbolReadingPolicy 枚举
title: ESymbolReadingPolicy 枚举
ms.date: 03/30/2017
api_name:
- ESymbolReadingPolicy
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ESymbolReadingPolicy
helpviewer_keywords:
- ESymbolReadingPolicy enumeration [.NET Framework hosting]
ms.assetid: 4dc6c80d-b694-480b-a378-d5b18420ce17
topic_type:
- apiref
ms.openlocfilehash: e84c31343b589cb6019d88fafc9b94207c5f5892
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785414"
---
# <a name="esymbolreadingpolicy-enumeration"></a><span data-ttu-id="62d3b-103">ESymbolReadingPolicy 枚举</span><span class="sxs-lookup"><span data-stu-id="62d3b-103">ESymbolReadingPolicy Enumeration</span></span>

<span data-ttu-id="62d3b-104">包含一些值，这些值设置用于读取程序数据库 (PDB) 文件的策略。</span><span class="sxs-lookup"><span data-stu-id="62d3b-104">Contains values that set the policy for reading program database (PDB) files.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="62d3b-105">语法</span><span class="sxs-lookup"><span data-stu-id="62d3b-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    eSymbolReadingNever,  
    eSymbolReadingAlways,  
    eSymbolReadingFullTrustOnly  
} ESymbolReadingPolicy;  
```  
  
## <a name="members"></a><span data-ttu-id="62d3b-106">成员</span><span class="sxs-lookup"><span data-stu-id="62d3b-106">Members</span></span>  
  
|<span data-ttu-id="62d3b-107">成员</span><span class="sxs-lookup"><span data-stu-id="62d3b-107">Member</span></span>|<span data-ttu-id="62d3b-108">说明</span><span class="sxs-lookup"><span data-stu-id="62d3b-108">Description</span></span>|  
|------------|-----------------|  
|`eSymbolReadingAlways`|<span data-ttu-id="62d3b-109">指定调试器应始终读取 PDB 文件。</span><span class="sxs-lookup"><span data-stu-id="62d3b-109">Specifies that the debugger should always read PDB files.</span></span>|  
|`eSymbolReadingFullTrustOnly`|<span data-ttu-id="62d3b-110">指定调试器只应读取与完全信任程序集关联的 PDB 文件。</span><span class="sxs-lookup"><span data-stu-id="62d3b-110">Specifies that the debugger should read only PDB files that are associated with full-trust assemblies.</span></span>|  
|`eSymbolReadingNever`|<span data-ttu-id="62d3b-111">指定调试器不应读取 PDB 文件。</span><span class="sxs-lookup"><span data-stu-id="62d3b-111">Specifies that the debugger should never read PDB files.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="62d3b-112">备注</span><span class="sxs-lookup"><span data-stu-id="62d3b-112">Remarks</span></span>  

 <span data-ttu-id="62d3b-113">`ESymbolReadingPolicy`枚举与[ICLRDebugManager：： SetSymbolReadingPolicy](iclrdebugmanager-setsymbolreadingpolicy-method.md)方法一起使用。</span><span class="sxs-lookup"><span data-stu-id="62d3b-113">The `ESymbolReadingPolicy` enumeration is used with the [ICLRDebugManager::SetSymbolReadingPolicy](iclrdebugmanager-setsymbolreadingpolicy-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="62d3b-114">要求</span><span class="sxs-lookup"><span data-stu-id="62d3b-114">Requirements</span></span>  

 <span data-ttu-id="62d3b-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="62d3b-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="62d3b-116">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="62d3b-116">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="62d3b-117">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="62d3b-117">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="62d3b-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="62d3b-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="62d3b-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="62d3b-119">See also</span></span>

- [<span data-ttu-id="62d3b-120">承载枚举</span><span class="sxs-lookup"><span data-stu-id="62d3b-120">Hosting Enumerations</span></span>](hosting-enumerations.md)
