---
description: 了解详细信息： CoUninitializeEE 函数
title: CoUninitializeEE 函数
ms.date: 03/30/2017
api_name:
- CoUninitializeEE
api_location:
- mscoree.dll
- mscorsvr.dll
api_type:
- DLLExport
f1_keywords:
- CoUninitializeEE
helpviewer_keywords:
- CoUninitializeEE function [.NET Framework hosting]
ms.assetid: 5f5a311a-839a-465f-89d9-ff1c74da9736
topic_type:
- apiref
ms.openlocfilehash: e356135ea027bd52520eff9084ad2f7f09e1fe0b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99746160"
---
# <a name="couninitializeee-function"></a>CoUninitializeEE 函数

`CoUninitializeEE` 已过时，不提供任何功能。  
  
## <a name="syntax"></a>语法  
  
```cpp  
void CoUninitializeEE (  
    BOOL fFlags  
);  
```  
  
## <a name="remarks"></a>备注  

 不能从进程中卸载公共语言运行时的执行引擎。 若要关闭执行引擎，请调用 [CorExitProcess](corexitprocess-function.md)。  
  
## <a name="see-also"></a>请参阅

- [CoInitializeEE 函数](coinitializeee-function.md)
- [元数据全局静态函数](../metadata/metadata-global-static-functions.md)
