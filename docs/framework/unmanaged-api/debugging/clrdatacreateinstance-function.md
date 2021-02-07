---
description: 了解详细信息： CLRDataCreateInstance 函数
title: CLRDataCreateInstance 函数
ms.date: 03/30/2017
api_name:
- CLRDataCreateInstance
api_location:
- mscordbi.dll
- mscordacwks.dll
api_type:
- DLLExport
f1_keywords:
- CLRDataCreateInstance
helpviewer_keywords:
- CLRDataCreateInstance function [.NET Framework debugging]
ms.assetid: 440bad90-5a88-45e7-9157-4596801d8d19
topic_type:
- apiref
ms.openlocfilehash: 923b0c687d2b337eacb475973927452e3b47ad0d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99747252"
---
# <a name="clrdatacreateinstance-function"></a><span data-ttu-id="c36ac-103">CLRDataCreateInstance 函数</span><span class="sxs-lookup"><span data-stu-id="c36ac-103">CLRDataCreateInstance Function</span></span>

<span data-ttu-id="c36ac-104">为指定的目标项创建接口对象。</span><span class="sxs-lookup"><span data-stu-id="c36ac-104">Creates an interface object for the specified target item.</span></span>

## <a name="syntax"></a><span data-ttu-id="c36ac-105">语法</span><span class="sxs-lookup"><span data-stu-id="c36ac-105">Syntax</span></span>

```cpp
HRESULT CLRDataCreateInstance (
    [in]  REFIID           iid,
    [in]  ICLRDataTarget  *target,
    [out] void           **iface  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c36ac-106">参数</span><span class="sxs-lookup"><span data-stu-id="c36ac-106">Parameters</span></span>  

 `iid`  
 <span data-ttu-id="c36ac-107">中要实例化的接口的标识符。</span><span class="sxs-lookup"><span data-stu-id="c36ac-107">[in] The identifier of the interface to be instantiated.</span></span>  
  
 `target`  
 <span data-ttu-id="c36ac-108">中一个指向用户实现的 [ICLRDataTarget](iclrdatatarget-interface.md) 对象的指针，该对象表示要为其创建 interface 对象的目标项。</span><span class="sxs-lookup"><span data-stu-id="c36ac-108">[in] A pointer to a user-implemented [ICLRDataTarget](iclrdatatarget-interface.md) object that represents the target item for which to create the interface object.</span></span>  
  
 `iface`  
 <span data-ttu-id="c36ac-109">弄指向返回的接口对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="c36ac-109">[out] A pointer to the address of the returned interface object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c36ac-110">备注</span><span class="sxs-lookup"><span data-stu-id="c36ac-110">Remarks</span></span>  

 <span data-ttu-id="c36ac-111">`ICLRDataTarget`对象由调试应用程序的编写器实现。</span><span class="sxs-lookup"><span data-stu-id="c36ac-111">The `ICLRDataTarget` object is implemented by the writer of the debugging application.</span></span> <span data-ttu-id="c36ac-112">实现取决于所表示的目标项的类型。</span><span class="sxs-lookup"><span data-stu-id="c36ac-112">The implementation depends on the type of target item being represented.</span></span> <span data-ttu-id="c36ac-113">目标项可以是进程、内存转储、远程计算机，等等。</span><span class="sxs-lookup"><span data-stu-id="c36ac-113">The target item may be a process, memory dump, remote machine, and so on.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c36ac-114">要求</span><span class="sxs-lookup"><span data-stu-id="c36ac-114">Requirements</span></span>  

 <span data-ttu-id="c36ac-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c36ac-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c36ac-116">**标头：** ClrData .idl</span><span class="sxs-lookup"><span data-stu-id="c36ac-116">**Header:** ClrData.idl</span></span>  
  
 <span data-ttu-id="c36ac-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c36ac-117">**Library:** CorGuids.lib</span></span>  

 <span data-ttu-id="c36ac-118">**程序集**： mscordacwks.dll、mscordbi.dll</span><span class="sxs-lookup"><span data-stu-id="c36ac-118">**Assembly**: mscordacwks.dll, mscordbi.dll</span></span>
  
 <span data-ttu-id="c36ac-119">**.NET Framework 版本：** 自 .NET Framework 2.0 起可用</span><span class="sxs-lookup"><span data-stu-id="c36ac-119">**.NET Framework Versions:** Available since .NET Framework 2.0</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c36ac-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="c36ac-120">See also</span></span>

- [<span data-ttu-id="c36ac-121">调试全局静态函数</span><span class="sxs-lookup"><span data-stu-id="c36ac-121">Debugging Global Static Functions</span></span>](debugging-global-static-functions.md)
