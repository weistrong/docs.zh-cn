---
description: 了解详细信息： CloseCLREnumeration 函数
title: CloseCLREnumeration 函数
ms.date: 03/30/2017
api_name:
- CloseCLREnumeration
api_location:
- dbgshim.dll
api_type:
- COM
f1_keywords:
- CloseCLREnumeration
helpviewer_keywords:
- debugging API [Silverlight]
- Silverlight, debugging
- CloseCLR Enumeration function
ms.assetid: 5e3c3958-80bb-43b1-a96b-dd3e6dbd9cd7
topic_type:
- apiref
ms.openlocfilehash: 7669332cc23b78afbb3bf597e7d208a5f707aae5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772765"
---
# <a name="closeclrenumeration-function"></a>CloseCLREnumeration 函数

关闭位于 [EnumerateCLRs 函数](enumerateclrs-function.md)所返回的句柄数组中 (CLR) 继续启动事件，并释放句柄和字符串路径数组的内存。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT CloseCLREnumeration (  
    [in]  DWORD      pHandleArray,  
    [in]  LPWSTR**   pStringArray,  
    [in]  DWORD*     dwArrayLength  
);  
```  
  
## <a name="parameters"></a>参数  

 `pHandleArray`  
 中指向从 [EnumerateCLRs 函数](enumerateclrs-function.md)返回的事件句柄的数组的指针。  
  
 `pStringArray`  
 中一个指针，指向从 [EnumerateCLRs 函数](enumerateclrs-function.md)返回的 CLR 字符串路径的数组。  
  
 `dwArrayLength`  
 [in] 包含 `pHandleArray` 或 `pStringArray`大小（长度）（它们是相同）的 DWORD。  
  
## <a name="return-value"></a>返回值  

 S_OK  
 [EnumerateCLRs 函数](enumerateclrs-function.md)打开的句柄将关闭，并且将释放分配给句柄和字符串数组的内存。  
  
 E_INVALIDARG  
 `pHandleArray` 的长度与传入 `dwArrayLength` 的长度不匹配。  
  
 E_FAIL（或其他 E_ 返回代码）  
 此函数无法释放 `pHandleArray` 和 `pStringArray` 的内存。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** dbgshim.dll  
  
 **库：** dbgshim.dll  
  
 **.NET Framework 版本：** 3.5 SP1
