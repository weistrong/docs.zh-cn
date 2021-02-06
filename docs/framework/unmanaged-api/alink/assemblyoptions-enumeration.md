---
description: 了解详细信息： AssemblyOptions 枚举
title: AssemblyOptions 枚举
ms.date: 03/30/2017
api_name:
- AssemblyOptions
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- AssemblyOptions
helpviewer_keywords:
- Alink API, AssemblyOptions enumeration
- AssemblyOptions enumeration
ms.assetid: 84f83921-64cb-49e3-ac8b-22a0b77b18a8
topic_type:
- apiref
ms.openlocfilehash: aba9ecb3176f533e2d53e2e45fef3d1dc4e55077
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638413"
---
# <a name="assemblyoptions-enumeration"></a>AssemblyOptions 枚举

枚举程序集选项。  
  
## <a name="syntax"></a>语法  
  
```cpp  
typedef enum _AssemblyOptions {  
    optAssemTitle = 0,  
    optAssemDescription,  
    optAssemConfig,  
    optAssemOS,  
    optAssemProcessor,  
    optAssemLocale,  
    optAssemVersion,  
    optAssemCompany,  
    optAssemProduct,  
    optAssemProductVersion,  
    optAssemCopyright,  
    optAssemTrademark,  
    optAssemKeyFile,  
    optAssemKeyName,  
    optAssemAlgID,  
    optAssemFlags,  
    optAssemHalfSign,  
    optAssemFileVersion,  
    optAssemSatelliteVer,  
    optLastAssemOption  
}   AssemblyOptions;  
```  
  
## <a name="fields"></a>字段  
  
|字段|说明|  
|-----------|-----------------|  
|optAssemTitle|String-表示程序集标题。|  
|optAssemDescription|String-包含程序集说明。|  
|optAssemConfig|String-包含程序集配置。|  
|optAssemOS|字符串编码为： "dwOSPlatformId. dwOSMajorVersion. dwOSMinorVersion"。|  
|optAssemProcessor|ULONG|  
|optAssemLocale|String-包含程序集的区域设置。|  
|optAssemVersion|字符串编码为： "主要版本. 次要版本. 内部版本. 修订版本"。|  
|optAssemCompany|String-包含公司。|  
|optAssemProduct|String-包含产品名称。|  
|optAssemProductVersion|String (也称为 InformationalVersion) 。|  
|optAssemCopyright|String-包含版权信息。|  
|optAssemTrademark|String-包含商标信息。|  
|optAssemKeyFile| (文件名) 字符串。|  
|optAssemKeyName| (项名称) 的字符串。|  
|optAssemAlgID|ULONG|  
|optAssemFlags|ULONG|  
|optAssemHalfSign|Bool (也称为 DelaySign) 。|  
|optAssemFileVersion|编码为 "ProductVersion" 的字符串，与 "" 相同。|  
|optAssemSatelliteVer|字符串编码为 "主要版本. 次要版本. 内部版本. 内部版本. 修订版本"。|  
|optLastAssemOption|元素数的计数器。|  
  
## <a name="requirements"></a>要求  

 **标头：** alink。h  
  
 **库**： alink.dll  
  
## <a name="see-also"></a>请参阅

- [Al.exe（程序集链接器）](../../tools/al-exe-assembly-linker.md)
