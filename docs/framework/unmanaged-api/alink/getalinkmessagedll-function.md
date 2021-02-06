---
description: 了解详细信息： GetALinkMessageDll 函数
title: GetALinkMessageDll 函数
ms.date: 03/30/2017
api_name:
- GetALinkMessageDll
api_location:
- alink.dll
api_type:
- DLLExport
f1_keywords:
- GetALinkMessageDll
helpviewer_keywords:
- Alink API, GetALinkMessageDll function
- GetALinkMessageDll function
ms.assetid: 67985a22-88a2-4c54-8d99-4bcde9d6213e
topic_type:
- apiref
ms.openlocfilehash: 67a294d1f21f50cee938ddeb14d1f30b4ccf911b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637867"
---
# <a name="getalinkmessagedll-function"></a>GetALinkMessageDll 函数

查找并加载消息 DLL。 如果找不到或无法加载消息 DLL，则返回0。 消息 DLL 应位于其名称为语言 ID 的子目录中，或位于当前目录中。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HINSTANCE WINAPI GetALinkMessageDll();  
```  
  
## <a name="requirements"></a>要求  

 **标头：** alink。h  
  
 **库**： alink.dll  
  
## <a name="see-also"></a>请参阅

- [Al.exe（程序集链接器）](../../tools/al-exe-assembly-linker.md)
