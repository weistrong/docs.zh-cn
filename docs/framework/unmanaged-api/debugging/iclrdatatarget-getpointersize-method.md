---
description: 了解详细信息： ICLRDataTarget：： GetPointerSize 方法
title: ICLRDataTarget::GetPointerSize 方法
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.GetPointerSize
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::GetPointerSize
helpviewer_keywords:
- GetPointerSize method [.NET Framework debugging]
- ICLRDataTarget::GetPointerSize method [.NET Framework debugging]
ms.assetid: 51d9f4a4-81a7-4527-8537-5212bdb05c70
topic_type:
- apiref
ms.openlocfilehash: 4c6e5ab9b919d1c5d2d6e2267a48d46a11cccc09
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801327"
---
# <a name="iclrdatatargetgetpointersize-method"></a><span data-ttu-id="a03f8-103">ICLRDataTarget::GetPointerSize 方法</span><span class="sxs-lookup"><span data-stu-id="a03f8-103">ICLRDataTarget::GetPointerSize Method</span></span>

<span data-ttu-id="a03f8-104">获取目标进程使用的指针类型的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="a03f8-104">Gets the size, in bytes, of the pointer type that the target process uses.</span></span> <span data-ttu-id="a03f8-105">此方法由公共语言运行时数据访问服务调用。</span><span class="sxs-lookup"><span data-stu-id="a03f8-105">This method is called by the common language runtime data access services.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a03f8-106">语法</span><span class="sxs-lookup"><span data-stu-id="a03f8-106">Syntax</span></span>  
  
```cpp  
HRESULT GetPointerSize (  
    [out] ULONG32     *pointerSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a03f8-107">参数</span><span class="sxs-lookup"><span data-stu-id="a03f8-107">Parameters</span></span>  

 `pointerSize`  
 <span data-ttu-id="a03f8-108">弄指向一个整数值的指针，该整数值指定目标进程上的指针的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="a03f8-108">[out] A pointer to an integer value that specifies the size, in bytes, of a pointer on the target process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a03f8-109">备注</span><span class="sxs-lookup"><span data-stu-id="a03f8-109">Remarks</span></span>  

 <span data-ttu-id="a03f8-110">此方法由调试应用程序的编写器实现。</span><span class="sxs-lookup"><span data-stu-id="a03f8-110">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a03f8-111">要求</span><span class="sxs-lookup"><span data-stu-id="a03f8-111">Requirements</span></span>  

 <span data-ttu-id="a03f8-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a03f8-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a03f8-113">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="a03f8-113">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="a03f8-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a03f8-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a03f8-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a03f8-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a03f8-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="a03f8-116">See also</span></span>

- [<span data-ttu-id="a03f8-117">ICLRDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="a03f8-117">ICLRDataTarget Interface</span></span>](iclrdatatarget-interface.md)
