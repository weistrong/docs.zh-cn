---
description: 了解详细信息： WAITORTIMERCALLBACK 函数指针
title: WAITORTIMERCALLBACK 函数指针
ms.date: 03/30/2017
api_name:
- WAITORTIMERCALLBACK
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- WAITORTIMERCALLBACK
helpviewer_keywords:
- WAITORTIMERCALLBACK function pointer [.NET Framework hosting]
ms.assetid: 1fec4aef-0a06-4df0-bae7-d31a9ef9603d
topic_type:
- apiref
ms.openlocfilehash: 6fd9e7eab56e48086eefcb26fc48cbf5f45d4a0e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99679051"
---
# <a name="waitortimercallback-function-pointer"></a>WAITORTIMERCALLBACK 函数指针

指向一个函数，该函数向宿主通知等待句柄 (<xref:System.Threading.WaitHandle>) 已发出信号或超时。  
  
 此函数指针在 .NET Framework 4 中已弃用。  
  
## <a name="syntax"></a>语法  
  
```cpp  
typedef VOID (__stdcall *WAITORTIMERCALLBACK) (  
    [in] PVOID lpParameter,  
    [in] BOOL  TimerOrWaitFired  
);  
```  
  
## <a name="parameters"></a>参数  

 `lpParameter`  
 中指向对象的指针，该对象包含由宿主定义的信息。  
  
 `TimerOrWaitFired`  
 [in] `true` 如果等待句柄超时，则为; 如果等待句柄已终止，则为 `false` 。  
  
## <a name="remarks"></a>备注  

 指向该函数的 `WAITORTIMERCALLBACK` 点是回调函数，并且必须由宿主应用程序的编写器实现。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** MSCorWks.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [弃用的 CLR 承载函数](deprecated-clr-hosting-functions.md)
