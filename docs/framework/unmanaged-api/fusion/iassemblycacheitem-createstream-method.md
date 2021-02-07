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
# <a name="iassemblycacheitemcreatestream-method"></a><span data-ttu-id="13f62-103">IAssemblyCacheItem::CreateStream 方法</span><span class="sxs-lookup"><span data-stu-id="13f62-103">IAssemblyCacheItem::CreateStream Method</span></span>

<span data-ttu-id="13f62-104">创建具有指定名称和格式的流。</span><span class="sxs-lookup"><span data-stu-id="13f62-104">Creates a stream with the specified name and format.</span></span>

## <a name="syntax"></a><span data-ttu-id="13f62-105">语法</span><span class="sxs-lookup"><span data-stu-id="13f62-105">Syntax</span></span>

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

## <a name="parameters"></a><span data-ttu-id="13f62-106">参数</span><span class="sxs-lookup"><span data-stu-id="13f62-106">Parameters</span></span>

`dwFlags`\
<span data-ttu-id="13f62-107">中在合成 .idl 中定义的标志。</span><span class="sxs-lookup"><span data-stu-id="13f62-107">[in] Flags defined in Fusion.idl.</span></span>

`pszStreamName`\
<span data-ttu-id="13f62-108">中要创建的流的名称。</span><span class="sxs-lookup"><span data-stu-id="13f62-108">[in] The name of the stream to be created.</span></span>

`dwFormat`\
<span data-ttu-id="13f62-109">中要进行流处理的文件的格式。</span><span class="sxs-lookup"><span data-stu-id="13f62-109">[in] The format of the file to be streamed.</span></span>

`dwFormatFlags`\
<span data-ttu-id="13f62-110">中在合成 .idl 中定义的特定于格式的标志。</span><span class="sxs-lookup"><span data-stu-id="13f62-110">[in] Format-specific flags defined in Fusion.idl.</span></span>

`ppIStream`\
<span data-ttu-id="13f62-111">弄指向返回的 [IStream](/windows/desktop/api/objidl/nn-objidl-istream) 实例的地址的指针。</span><span class="sxs-lookup"><span data-stu-id="13f62-111">[out] A pointer to the address of the returned [IStream](/windows/desktop/api/objidl/nn-objidl-istream) instance.</span></span>

`puliMaxSize`\
<span data-ttu-id="13f62-112">[in，可选]引用的流的最大大小 `ppIStream` 。</span><span class="sxs-lookup"><span data-stu-id="13f62-112">[in, optional] The maximum size of the stream referenced by `ppIStream`.</span></span>

## <a name="requirements"></a><span data-ttu-id="13f62-113">要求</span><span class="sxs-lookup"><span data-stu-id="13f62-113">Requirements</span></span>

<span data-ttu-id="13f62-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="13f62-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="13f62-115">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="13f62-115">**Header:** Fusion.h</span></span>

<span data-ttu-id="13f62-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="13f62-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="13f62-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="13f62-117">See also</span></span>

- [<span data-ttu-id="13f62-118">IAssemblyCacheItem 接口</span><span class="sxs-lookup"><span data-stu-id="13f62-118">IAssemblyCacheItem Interface</span></span>](iassemblycacheitem-interface.md)
