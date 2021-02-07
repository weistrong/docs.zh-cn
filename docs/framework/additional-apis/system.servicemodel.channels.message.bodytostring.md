---
description: 了解详细信息： BodyToString 方法
title: 'BodyToString 方法 (System.servicemodel) '
ms.date: 11/01/2019
topic_type:
- apiref
api_name:
- System.ServiceModel.Channels.Message.BodyToString
api_location:
- system.servicemodel.dll
api_type:
- Assembly
ms.openlocfilehash: babcd881d191ff46b98e9999c4ff04166479a68d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99699371"
---
# <a name="messagebodytostring-method"></a><span data-ttu-id="385af-103">BodyToString 方法</span><span class="sxs-lookup"><span data-stu-id="385af-103">Message.BodyToString Method</span></span>

<span data-ttu-id="385af-104">通过调用方法将消息正文转换为字符串 <xref:System.ServiceModel.Channels.Message.OnBodyToString%2A?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="385af-104">Converts the message body into a string by calling the <xref:System.ServiceModel.Channels.Message.OnBodyToString%2A?displayProperty=nameWithType> method.</span></span>

```csharp
internal void BodyToString(XmlDictionaryWriter writer);
```

## <a name="parameters"></a><span data-ttu-id="385af-105">参数</span><span class="sxs-lookup"><span data-stu-id="385af-105">Parameters</span></span>

- <span data-ttu-id="385af-106">`writer` <xref:System.Xml.XmlDictionaryWriter></span><span class="sxs-lookup"><span data-stu-id="385af-106">`writer` <xref:System.Xml.XmlDictionaryWriter></span></span>\
  <span data-ttu-id="385af-107">用于将消息正文转换为字符串的编写器。</span><span class="sxs-lookup"><span data-stu-id="385af-107">The writer that is used to convert the message body to a string.</span></span>

## <a name="remarks"></a><span data-ttu-id="385af-108">备注</span><span class="sxs-lookup"><span data-stu-id="385af-108">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="385af-109">`Message.BodyToString`方法是内部的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="385af-109">The `Message.BodyToString` method is internal and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="385af-110">在任何情况下，Microsoft 不支持在生产应用程序中使用此方法。</span><span class="sxs-lookup"><span data-stu-id="385af-110">Microsoft does not support the use of this method in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="385af-111">要求</span><span class="sxs-lookup"><span data-stu-id="385af-111">Requirements</span></span>

<span data-ttu-id="385af-112">**命名空间：** <xref:System.ServiceModel.Channels></span><span class="sxs-lookup"><span data-stu-id="385af-112">**Namespace:** <xref:System.ServiceModel.Channels></span></span>

<span data-ttu-id="385af-113">**程序集：** System.ServiceModel.dll</span><span class="sxs-lookup"><span data-stu-id="385af-113">**Assembly:** System.ServiceModel.dll</span></span>

<span data-ttu-id="385af-114">**.NET Framework 版本：** 自3.0 起可用。</span><span class="sxs-lookup"><span data-stu-id="385af-114">**.NET Framework versions:** Available since 3.0.</span></span>
