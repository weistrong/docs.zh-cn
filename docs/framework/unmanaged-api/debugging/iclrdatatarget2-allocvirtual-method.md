---
description: 了解详细信息： ICLRDataTarget2：： AllocVirtual 方法
title: ICLRDataTarget2::AllocVirtual 方法
ms.date: 03/30/2017
api_name:
- ICLRDataTarget2.AllocVirtual
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget2::AllocVirtual
helpviewer_keywords:
- ICLRDataTarget2::AllocVirtual method [.NET Framework debugging]
- AllocVirtual method [.NET Framework debugging]
ms.assetid: e3226230-964b-47fb-9f53-d6fdbeda1e9e
topic_type:
- apiref
ms.openlocfilehash: d81474e4067599178285b6fa876919298617919d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99729323"
---
# <a name="iclrdatatarget2allocvirtual-method"></a>ICLRDataTarget2::AllocVirtual 方法

由公共语言运行时 (CLR) 数据访问服务调用以在此目标进程的地址空间中分配内存。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT AllocVirtual(  
    [in] CLRDATA_ADDRESS addr,  
    [in] ULONG32 size,  
    [in] ULONG32 typeFlags,  
    [in] ULONG32 protectFlags,  
    [out] CLRDATA_ADDRESS* virt  
);  
```  
  
## <a name="parameters"></a>参数  

 `addr`  
 中一个 `CLRDATA_ADDRESS` 值，该值指定要分配的内存的起始地址。  
  
 `size`  
 中要分配的内存的大小（以字节为单位）。  
  
 `typeFlags`  
 中控制内存分配的标志。 请参阅 Win32 `VirtualAlloc` 函数。  
  
 `protectFlags`  
 中已分配内存的保护特性。 请参阅 Win32 `VirtualAlloc` 函数。  
  
 `virt`  
 弄一个指向值的指针，该 `CLRDATA_ADDRESS` 值指定分配的内存的实际起始地址。  
  
## <a name="remarks"></a>备注  

 `AllocVirtual`方法用作 Win32 函数的逻辑包装 `VirtualAlloc` 。  
  
 此方法由调试应用程序的编写器实现。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** ClrData，ClrData  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICLRDataTarget2 接口](iclrdatatarget2-interface.md)
- [FreeVirtual 方法](iclrdatatarget2-freevirtual-method.md)
