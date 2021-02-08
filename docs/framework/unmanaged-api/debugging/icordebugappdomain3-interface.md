---
description: 了解详细信息： ICorDebugAppDomain3 接口
title: ICorDebugAppDomain3 接口
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain3
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain3
helpviewer_keywords:
- ICorDebugAppDomain3 interface [.NET Framework debugging]
ms.assetid: 875ef5be-c1e7-4d95-97e9-d3a667aeaba0
topic_type:
- apiref
ms.openlocfilehash: 6575aa685759102443babeaf82774e6221b80693
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772206"
---
# <a name="icordebugappdomain3-interface"></a>ICorDebugAppDomain3 接口

提供方法以检索有关应用程序域中当前加载的 Windows 运行时类型的托管表示形式的信息。 此接口是 ICorDebugAppDomain 和 ICorDebugAppDomain2 接口的扩展。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[ICorDebugAppDomain3：： GetCachedWinRTTypes](icordebugappdomain3-getcachedwinrttypes-method.md)|获取所有缓存 Windows 运行时类型的枚举器。|  
|[ICorDebugAppDomain3：： GetCachedWinRTTypesForIIDs](icordebugappdomain3-getcachedwinrttypesforiids-method.md)|基于其接口标识符获取应用程序域中缓存的 Windows 运行时类型的枚举器。|  
  
## <a name="remarks"></a>备注  

 此接口旨在由调试器结合使用，并与函数计算调用一起使用 `M:System.Runtime.InteropServices.Marshal.GetInspectableIIDs(System.Object)` 。 当方法检索 Windows 运行时 server 对象支持的接口标识符时，调试器可以使用在此接口中定义的方法，将它们映射到与这些接口相对应的托管类型。  
  
 若要检索此接口的实例，请 `QueryInterface` 在 ICorDebugAppDomain 或 ICorDebugAppDomain2 接口的实例上运行。  
  
> [!NOTE]
> 此接口不支持跨计算机或跨进程远程调用。  
  
## <a name="requirements"></a>要求  

 **平台：** Windows 运行时  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [调试接口](debugging-interfaces.md)
