---
description: 了解详细信息： IInstallReferenceEnum：： GetNextInstallReferenceItem 方法
title: IInstallReferenceEnum::GetNextInstallReferenceItem 方法
ms.date: 03/30/2017
api_name:
- IInstallReferenceEnum.GetNextInstallReferenceItem
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IInstallReferenceEnum::GetNextInstallReferenceItem
helpviewer_keywords:
- IInstallReferenceEnum::GetNextInstallReferenceItem method [.NET Framework fusion]
- GetNextInstallReferenceItem method [.NET Framework fusion]
ms.assetid: ce969c9d-6538-4c34-8784-148ffd99fe7a
topic_type:
- apiref
ms.openlocfilehash: d410407fe16a46b45786ff74f694aaa8931be542
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800106"
---
# <a name="iinstallreferenceenumgetnextinstallreferenceitem-method"></a>IInstallReferenceEnum::GetNextInstallReferenceItem 方法

获取一个指针，该指针指向此[IInstallReferenceEnum](iinstallreferenceenum-interface.md)对象中包含的下一个[IInstallReferenceItem](iinstallreferenceitem-interface.md)对象。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetNextInstallReferenceItem (  
    [out] IInstallReferenceItem **ppRefItem,  
    [in]  DWORD dwFlags,  
    [in]  LPVOID pvReserved  
);  
```  
  
## <a name="parameters"></a>参数  

 `ppRefItem`  
 弄返回的 `IInstallReferenceItem` 指针。  
  
 `dwFlags`  
 中保留以供将来进行扩展。 `dwFlags` 必须为 0 (零) 。  
  
 `pvReserved`  
 中保留以供将来进行扩展。 `pvReserved` 必须为空引用。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** 合成。h  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IInstallReferenceItem 接口](iinstallreferenceitem-interface.md)
- [IInstallReferenceEnum 接口](iinstallreferenceenum-interface.md)
