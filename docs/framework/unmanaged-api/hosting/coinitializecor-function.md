---
description: 了解详细信息： CoInitializeCor 函数
title: CoInitializeCor 函数
ms.date: 03/30/2017
api_name:
- CoInitializeCor
api_location:
- mscoree.dll
- mscorsvr.dll
api_type:
- DLLExport
f1_keywords:
- CoInitializeCor
helpviewer_keywords:
- CoInitializeCor function [.NET Framework hosting]
ms.assetid: 9b9079fb-579e-4141-b3f0-791072dd40dc
topic_type:
- apiref
ms.openlocfilehash: e1db9914cce8a92cecf78123a2e247d75ec74acf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799845"
---
# <a name="coinitializecor-function"></a>CoInitializeCor 函数

`CoInitializeCor` 已过时。  
  
## <a name="syntax"></a>语法  
  
```cpp  
STDAPI CoInitializeCor (  
    DWORD fFlags  
);  
```  
  
## <a name="remarks"></a>备注  

 若要初始化公共语言运行时，请使用 [CorBindToRuntimeEx](corbindtoruntimeex-function.md) 或 [CorBindToCurrentRuntime](corbindtocurrentruntime-function.md)。  
  
## <a name="requirements"></a>要求  

 **标头：** Cor  
  
## <a name="see-also"></a>请参阅

- [元数据全局静态函数](../metadata/metadata-global-static-functions.md)
