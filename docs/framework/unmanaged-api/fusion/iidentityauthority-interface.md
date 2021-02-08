---
description: 了解详细信息： IIdentityAuthority 接口
title: IIdentityAuthority 接口
ms.date: 03/30/2017
api_name:
- IIdentityAuthority
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IIdentityAuthority
helpviewer_keywords:
- IIdentityAuthority interface [.NET Framework fusion]
ms.assetid: 6277f914-51a8-49be-bec6-52d6d648527d
topic_type:
- apiref
ms.openlocfilehash: 3064a3d95ebe9a098a7cac0766f18654c6fab8b9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800131"
---
# <a name="iidentityauthority-interface"></a>IIdentityAuthority 接口

管理代码对象的标识键。

## <a name="methods"></a>方法

|方法|说明|
|------------|-----------------|
|`IIdentityAuthority::AreDefinitionsEqual`|获取一个值，该值指示两个指定的 [IDefinitionIdentity](idefinitionidentity-interface.md) 实例是否相等。|
|`IIdentityAuthority::AreReferencesEqual`|获取一个值，该值指示两个指定的 [IReferenceIdentity](ireferenceidentity-interface.md) 实例是否相等。|
|`IIdentityAuthority::AreTextualDefinitionsEqual`|获取一个值，该值指示两个指定的字符串定义标识表示形式是否相等。|
|`IIdentityAuthority::AreTextualReferencesEqual`|获取一个值，该值指示两个指定的字符串引用标识表示形式是否相等。|
|`IIdentityAuthority::CreateDefinition`|获取一个指针，该指针指向 `IDefinitionIdentity` 表示当前范围内的代码对象的新实例。|
|`IIdentityAuthority::CreateReference`|获取一个指针，该指针指向 `IReferenceIdentity` 表示当前范围内的代码对象的新实例。|
|`IIdentityAuthority::DefinitionToText`|获取指定的格式化字符串版本 `IDefinitionIdentity` 。|
|`IIdentityAuthority::DefinitionToTextBuffer`|使用指定的字符串版本填充指定的宽字符缓冲区 `IDefinitionIdentity` 。|
|`IIdentityAuthority::DoesDefinitionMatchReference`|获取一个值，该值指示指定的 `IDefinitionIdentity` 和 `IReferenceIdentity` 实例是否引用同一代码对象。|
|`IIdentityAuthority::DoesTextualDefinitionMatchTextualReference`|获取一个值，该值指示指定的字符串是否引用同一代码对象。|
|`IIdentityAuthority::GenerateDefinitionKey`|获取一个指针，该指针指向指定的新创建的字符串键 `IDefinitionIdentity` 。|
|`IIdentityAuthority::GenerateReferenceKey`|获取一个指针，该指针指向指定的新创建的字符串键 `IReferenceIdentity` 。|
|`IIdentityAuthority::HashDefinition`|获取指定的的哈希值 `IDefinitionIdentity` 。|
|`IIdentityAuthority::HashReference`|获取指定的的哈希值 `IReferenceIdentity` 。|
|`IIdentityAuthority::ReferenceToText`|获取指定的格式化字符串版本 `IReferenceIdentity` 。|
|`IIdentityAuthority::ReferenceToTextBuffer`|使用指定的字符串版本填充指定的宽字符缓冲区 `IReferenceIdentity` 。|
|`IIdentityAuthority::TextToDefinition`|获取一个接口指针，该指针指向 `IDefinitionIdentity` 从指定的格式化字符串生成的实例。|
|`IIdentityAuthority::TextToReference`|获取一个接口指针，该指针指向 `IReferenceIdentity` 从指定的格式化字符串生成的实例。|

## <a name="requirements"></a>要求

**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。

**标头：** 隔离。h

**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]

## <a name="see-also"></a>请参阅

- [合成接口](fusion-interfaces.md)
