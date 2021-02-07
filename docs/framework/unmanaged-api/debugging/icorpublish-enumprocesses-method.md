---
description: 了解详细信息： ICorPublish：： EnumProcesses 方法
title: ICorPublish::EnumProcesses 方法
ms.date: 03/30/2017
api_name:
- ICorPublish.EnumProcesses
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublish::EnumProcesses
helpviewer_keywords:
- ICorPublish::EnumProcesses method [.NET Framework debugging]
- EnumProcesses method [.NET Framework debugging]
ms.assetid: 4ae765f0-93b2-4b6f-aea1-7b0cf44e04a7
topic_type:
- apiref
ms.openlocfilehash: 2451f179301eff4caca966568f966d145e269f51
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721991"
---
# <a name="icorpublishenumprocesses-method"></a><span data-ttu-id="4abe6-103">ICorPublish::EnumProcesses 方法</span><span class="sxs-lookup"><span data-stu-id="4abe6-103">ICorPublish::EnumProcesses Method</span></span>

<span data-ttu-id="4abe6-104">获取在此计算机上运行的托管进程的枚举器。</span><span class="sxs-lookup"><span data-stu-id="4abe6-104">Gets an enumerator for the managed processes running on this computer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4abe6-105">语法</span><span class="sxs-lookup"><span data-stu-id="4abe6-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumProcesses (  
    [in] COR_PUB_ENUMPROCESS       Type,  
    [out] ICorPublishProcessEnum   **ppIEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4abe6-106">参数</span><span class="sxs-lookup"><span data-stu-id="4abe6-106">Parameters</span></span>  

 `Type`  
 <span data-ttu-id="4abe6-107">一个 [COR_PUB_ENUMPROCESS](cor-pub-enumprocess-enumeration.md) 枚举的值，该值指定要检索的进程的类型。</span><span class="sxs-lookup"><span data-stu-id="4abe6-107">A value of the [COR_PUB_ENUMPROCESS](cor-pub-enumprocess-enumeration.md) enumeration that specifies the type of process to be retrieved.</span></span> <span data-ttu-id="4abe6-108">在当前版本中，只有 COR_PUB_MANAGEDONLY 是有效的。</span><span class="sxs-lookup"><span data-stu-id="4abe6-108">In the current version, only COR_PUB_MANAGEDONLY is valid.</span></span>  
  
 `ppIEnum`  
 <span data-ttu-id="4abe6-109">一个指针，指向作为进程枚举器的 [ICorPublishProcessEnum](icorpublishprocessenum-interface.md) 实例的地址。</span><span class="sxs-lookup"><span data-stu-id="4abe6-109">A pointer to the address of an [ICorPublishProcessEnum](icorpublishprocessenum-interface.md) instance that is the enumerator of the processes.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4abe6-110">备注</span><span class="sxs-lookup"><span data-stu-id="4abe6-110">Remarks</span></span>  

 <span data-ttu-id="4abe6-111">枚举器的进程集合基于调用方法时正在运行的进程的快照 `EnumProcesses` 。</span><span class="sxs-lookup"><span data-stu-id="4abe6-111">The enumerator's collection of processes is based on a snapshot of the processes that are running when the `EnumProcesses` method is called.</span></span> <span data-ttu-id="4abe6-112">枚举器将不包含在调用之后终止或开始后终止的任何进程 `EnumProcesses` 。</span><span class="sxs-lookup"><span data-stu-id="4abe6-112">The enumerator will not include any processes that terminate before or start after `EnumProcesses` is called.</span></span>  
  
 <span data-ttu-id="4abe6-113">`EnumProcesses`此方法可能会在此[ICorPublish](icorpublish-interface.md)实例上调用多次，以创建新的最新进程集合。</span><span class="sxs-lookup"><span data-stu-id="4abe6-113">The `EnumProcesses` method may be called more than once on this [ICorPublish](icorpublish-interface.md) instance to create a new up-to-date collection of processes.</span></span> <span data-ttu-id="4abe6-114">对方法的后续调用将不会影响现有集合 `EnumProcesses` 。</span><span class="sxs-lookup"><span data-stu-id="4abe6-114">Existing collections will not be affected by subsequent calls of the `EnumProcesses` method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4abe6-115">要求</span><span class="sxs-lookup"><span data-stu-id="4abe6-115">Requirements</span></span>  

 <span data-ttu-id="4abe6-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4abe6-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4abe6-117">**标头：** CorPub，CorPub</span><span class="sxs-lookup"><span data-stu-id="4abe6-117">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="4abe6-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4abe6-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4abe6-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4abe6-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4abe6-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="4abe6-120">See also</span></span>

- [<span data-ttu-id="4abe6-121">ICorPublish 接口</span><span class="sxs-lookup"><span data-stu-id="4abe6-121">ICorPublish Interface</span></span>](icorpublish-interface.md)
