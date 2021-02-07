---
description: 了解详细信息： CreateInstallReferenceEnum 函数
title: CreateInstallReferenceEnum 函数
ms.date: 03/30/2017
api_name:
- CreateInstallReferenceEnum
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- CreateInstallReference
helpviewer_keywords:
- CreateInstallReference function [.NET Framework fusion]
ms.assetid: 80dbbbf8-54fc-4894-b74a-0179d3201083
topic_type:
- apiref
ms.openlocfilehash: cc7551707cb46bcf0c475a0095684dbc790836e3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761130"
---
# <a name="createinstallreferenceenum-function"></a>CreateInstallReferenceEnum 函数

获取一个指针，该指针指向表示应用程序对指定程序集的引用列表的 [IInstallReferenceEnum](iinstallreferenceenum-interface.md) 实例。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT CreateInstallReferenceEnum (  
    [out] IInstallReferenceEnum **ppRefEnum,  
    [in]  IAssemblyName         *pName,  
    [in]  DWORD                 dwFlags,  
    [in]  LPVOID                pvReserved  
 );  
```  
  
## <a name="parameters"></a>参数  

 `ppRefEnum`  
 弄返回的 `IInstallReferenceEnum` 指针。  
  
 `pName`  
 中标识要枚举其引用的程序集的 [IAssemblyName](iassemblyname-interface.md) 。  
  
 `dwFlags`  
 中影响枚举器行为的标志。  
  
 `pvReserved`  
 中保留以供将来进行扩展。 `pvReserved` 必须为空引用。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** 合成。h  
  
 **库：** Fusion.dll 和 Mscorwks.dll。 使用 Fusion.dll 而不是 Mscorwks.dll 确保以正确的 .NET Framework 版本为目标。  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IInstallReferenceEnum 接口](iinstallreferenceenum-interface.md)
- [IAssemblyName 接口](iassemblyname-interface.md)
- [合成全局静态函数](fusion-global-static-functions.md)
