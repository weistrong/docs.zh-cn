---
description: 了解详细信息： ICLRDataTarget：： GetMachineType 方法
title: ICLRDataTarget::GetMachineType 方法
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.GetMachineType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::GetMachineType
helpviewer_keywords:
- ICLRDataTarget::GetMachineType method [.NET Framework debugging]
- GetMachineType method [.NET Framework debugging]
ms.assetid: 5f1f9c61-3e3b-48b2-b111-a4395f7623a7
topic_type:
- apiref
ms.openlocfilehash: 5624f734a77f51b4ea6cd9dd0c9df393c72e7d26
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801340"
---
# <a name="iclrdatatargetgetmachinetype-method"></a><span data-ttu-id="d2b08-103">ICLRDataTarget::GetMachineType 方法</span><span class="sxs-lookup"><span data-stu-id="d2b08-103">ICLRDataTarget::GetMachineType Method</span></span>

<span data-ttu-id="d2b08-104">获取目标进程正在使用的指令集类型的标识符。</span><span class="sxs-lookup"><span data-stu-id="d2b08-104">Gets the identifier for the kind of instruction set that the target process is using.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d2b08-105">语法</span><span class="sxs-lookup"><span data-stu-id="d2b08-105">Syntax</span></span>  
  
```cpp  
HRESULT GetMachineType (  
    [out] ULONG32     *machineType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d2b08-106">参数</span><span class="sxs-lookup"><span data-stu-id="d2b08-106">Parameters</span></span>  

 `machineType`  
 <span data-ttu-id="d2b08-107">弄一个指向值的指针，该指针指示目标进程使用的指令集。</span><span class="sxs-lookup"><span data-stu-id="d2b08-107">[out] A pointer to a value that indicates the instruction set that the target process is using.</span></span> <span data-ttu-id="d2b08-108">返回的 `machineType` 是在 WinNT 头文件中定义的 IMAGE_FILE_MACHINE 常数之一。</span><span class="sxs-lookup"><span data-stu-id="d2b08-108">The returned `machineType` is one of the IMAGE_FILE_MACHINE constants, which are defined in the WinNT.h header file.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d2b08-109">要求</span><span class="sxs-lookup"><span data-stu-id="d2b08-109">Requirements</span></span>  

 <span data-ttu-id="d2b08-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d2b08-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d2b08-111">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="d2b08-111">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="d2b08-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d2b08-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d2b08-113">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d2b08-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d2b08-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="d2b08-114">See also</span></span>

- [<span data-ttu-id="d2b08-115">ICLRDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="d2b08-115">ICLRDataTarget Interface</span></span>](iclrdatatarget-interface.md)
