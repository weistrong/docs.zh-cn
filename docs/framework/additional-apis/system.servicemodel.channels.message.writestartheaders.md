---
description: 了解详细信息： WriteStartHeaders 方法
title: 'WriteStartHeaders 方法 (System.servicemodel) '
ms.date: 11/01/2019
topic_type:
- apiref
api_name:
- System.ServiceModel.Channels.Message.WriteStartHeaders
api_location:
- system.servicemodel.dll
api_type:
- Assembly
ms.openlocfilehash: 20cadf5f1eecf6d8e02c5dc4597889abaef4ec36
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99699358"
---
# <a name="messagewritestartheaders-method"></a><span data-ttu-id="66bcb-103">WriteStartHeaders 方法</span><span class="sxs-lookup"><span data-stu-id="66bcb-103">Message.WriteStartHeaders Method</span></span>

<span data-ttu-id="66bcb-104">通过调用方法，将开始标头写入 XML 文件 <xref:System.ServiceModel.Channels.Message.OnWriteStartHeaders%2A?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="66bcb-104">Writes the start header into an XML file by calling the <xref:System.ServiceModel.Channels.Message.OnWriteStartHeaders%2A?displayProperty=nameWithType> method.</span></span>

```csharp
internal void WriteStartHeaders(XmlDictionaryWriter writer)
```

## <a name="parameters"></a><span data-ttu-id="66bcb-105">参数</span><span class="sxs-lookup"><span data-stu-id="66bcb-105">Parameters</span></span>

- <span data-ttu-id="66bcb-106">`writer` <xref:System.Xml.XmlDictionaryWriter></span><span class="sxs-lookup"><span data-stu-id="66bcb-106">`writer` <xref:System.Xml.XmlDictionaryWriter></span></span>\
  <span data-ttu-id="66bcb-107">用于将开始标头写入 XML 文件的编写器。</span><span class="sxs-lookup"><span data-stu-id="66bcb-107">The writer that is used to write the start header into an XML file.</span></span>

## <a name="remarks"></a><span data-ttu-id="66bcb-108">备注</span><span class="sxs-lookup"><span data-stu-id="66bcb-108">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="66bcb-109">`Message.WriteStartHeaders`方法是内部的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="66bcb-109">The `Message.WriteStartHeaders` method is internal and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="66bcb-110">在任何情况下，Microsoft 不支持在生产应用程序中使用此方法。</span><span class="sxs-lookup"><span data-stu-id="66bcb-110">Microsoft does not support the use of this method in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="66bcb-111">要求</span><span class="sxs-lookup"><span data-stu-id="66bcb-111">Requirements</span></span>

<span data-ttu-id="66bcb-112">**命名空间：** <xref:System.ServiceModel.Channels></span><span class="sxs-lookup"><span data-stu-id="66bcb-112">**Namespace:** <xref:System.ServiceModel.Channels></span></span>

<span data-ttu-id="66bcb-113">**程序集：** System.ServiceModel.dll</span><span class="sxs-lookup"><span data-stu-id="66bcb-113">**Assembly:** System.ServiceModel.dll</span></span>

<span data-ttu-id="66bcb-114">**.NET Framework 版本：** 自3.0 起可用。</span><span class="sxs-lookup"><span data-stu-id="66bcb-114">**.NET Framework versions:** Available since 3.0.</span></span>
