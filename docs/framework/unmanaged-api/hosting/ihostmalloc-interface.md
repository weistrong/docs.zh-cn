---
description: 了解详细信息： IHostMalloc 接口
title: IHostMalloc 接口
ms.date: 03/30/2017
api_name:
- IHostMAlloc
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMAlloc
helpviewer_keywords:
- IHostMAlloc interface [.NET Framework hosting]
ms.assetid: e3c6643b-6fc7-4a99-959d-4b7b4e63fdee
topic_type:
- apiref
ms.openlocfilehash: cd04a0f71fd429ea10b9edcce02806f4afa57148
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99708172"
---
# <a name="ihostmalloc-interface"></a>IHostMalloc 接口

提供一些方法，这些方法允许公共语言运行时 (CLR) 通过宿主请求从堆进行细化分配。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[Alloc 方法](ihostmalloc-alloc-method.md)|请求宿主从堆分配请求的内存量。|  
|[DebugAlloc 方法](ihostmalloc-debugalloc-method.md)|请求宿主从堆分配请求的内存量，并另外跟踪内存的分配位置。|  
|[Free 方法](ihostmalloc-free-method.md)|释放通过使用方法分配的内存 `Alloc` 。|  
  
## <a name="remarks"></a>备注  

 CLR `IHostMalloc` 通过调用 [IHostMemoryManager：： CreateMalloc](ihostmemorymanager-createmalloc-method.md) 方法获取指向实例的接口指针。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IHostMemoryManager 接口](ihostmemorymanager-interface.md)
- [承载接口](hosting-interfaces.md)
