---
description: 了解详细信息： IAssemblyCacheItem：： CreateStream 方法
title: IAssemblyCacheItem::CreateStream 方法
ms.date: 03/30/2017
api_name:
- IAssemblyCacheItem.CreateStream
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCacheItem::CreateStream
helpviewer_keywords:
- CreateStream method [.NET Framework fusion]
- IAssemblyCacheItem::CreateStream method [.NET Framework fusion]
ms.assetid: 697ab0f4-470c-4baa-a415-4a975c42d0d5
topic_type:
- apiref
ms.openlocfilehash: 89592d8fe1a7f43a7da20dd10883881c3339f088
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760861"
---
# <a name="iassemblycacheitemcreatestream-method"></a>IAssemblyCacheItem::CreateStream 方法

创建具有指定名称和格式的流。

## <a name="syntax"></a>语法

```cpp
HRESULT CreateStream (
    [in]  DWORD dwFlags,
    [in]  LPCWSTR pszStreamName,
    [in]  DWORD dwFormat,
    [in]  DWORD dwFormatFlags,
    [out] IStream **ppIStream,
    [in, optional] ULARGE_INTEGER *puliMaxSize
);
```

## <a name="parameters"></a>参数

`dwFlags`\
中在合成 .idl 中定义的标志。

`pszStreamName`\
中要创建的流的名称。

`dwFormat`\
中要进行流处理的文件的格式。

`dwFormatFlags`\
中在合成 .idl 中定义的特定于格式的标志。

`ppIStream`\
弄指向返回的 [IStream](/windows/desktop/api/objidl/nn-objidl-istream) 实例的地址的指针。

`puliMaxSize`\
[in，可选]引用的流的最大大小 `ppIStream` 。

## <a name="requirements"></a>要求

**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。

**标头：** 合成。h

**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]

## <a name="see-also"></a>请参阅

- [IAssemblyCacheItem 接口](iassemblycacheitem-interface.md)
