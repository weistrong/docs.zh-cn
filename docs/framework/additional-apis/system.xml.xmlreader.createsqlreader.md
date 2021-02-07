---
description: 了解详细信息： CreateSqlReader 方法
title: 'CreateSqlReader 方法 ( # A0) '
ms.date: 10/17/2019
topic_type:
- apiref
api_name:
- System.Xml.XmlReader.CreateSqlReader
api_location:
- system.xml.dll
api_type:
- Assembly
ms.openlocfilehash: 61d594c0438c86863ce4052387439f5483d8a34c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99740428"
---
# <a name="xmlreadercreatesqlreader-method"></a><span data-ttu-id="59d9d-103">XmlReader.CreateSqlReader 方法</span><span class="sxs-lookup"><span data-stu-id="59d9d-103">XmlReader.CreateSqlReader Method</span></span>

<span data-ttu-id="59d9d-104">使用指定的流、设置和用于分析的上下文信息创建一个新的 <xref:System.Xml.XmlReader> 实例。</span><span class="sxs-lookup"><span data-stu-id="59d9d-104">Creates a new <xref:System.Xml.XmlReader> instance using the specified stream, settings, and context information for parsing.</span></span>

```csharp
internal static XmlReader CreateSqlReader(Stream input,
  XmlReaderSettings settings, XmlParserContext inputContext)
```

## <a name="parameters"></a><span data-ttu-id="59d9d-105">参数</span><span class="sxs-lookup"><span data-stu-id="59d9d-105">Parameters</span></span>

- <span data-ttu-id="59d9d-106">`input` <xref:System.IO.Stream></span><span class="sxs-lookup"><span data-stu-id="59d9d-106">`input` <xref:System.IO.Stream></span></span>  
  <span data-ttu-id="59d9d-107">包含 XML 数据的流。</span><span class="sxs-lookup"><span data-stu-id="59d9d-107">The stream that contains the XML data.</span></span>

- <span data-ttu-id="59d9d-108">`settings` <xref:System.Xml.XmlReaderSettings></span><span class="sxs-lookup"><span data-stu-id="59d9d-108">`settings` <xref:System.Xml.XmlReaderSettings></span></span>  
  <span data-ttu-id="59d9d-109">新 <xref:System.Xml.XmlReader> 实例的设置。</span><span class="sxs-lookup"><span data-stu-id="59d9d-109">The settings for the new <xref:System.Xml.XmlReader> instance.</span></span> <span data-ttu-id="59d9d-110">此值可为 `null`。</span><span class="sxs-lookup"><span data-stu-id="59d9d-110">This value can be `null`.</span></span>

- <span data-ttu-id="59d9d-111">`inputContext` <xref:System.Xml.XmlParserContext></span><span class="sxs-lookup"><span data-stu-id="59d9d-111">`inputContext` <xref:System.Xml.XmlParserContext></span></span>  
  <span data-ttu-id="59d9d-112">分析 XML 片段所需的上下文信息.</span><span class="sxs-lookup"><span data-stu-id="59d9d-112">The context information required to parse the XML fragment.</span></span> <span data-ttu-id="59d9d-113">此值可为 `null`。</span><span class="sxs-lookup"><span data-stu-id="59d9d-113">This value can be `null`.</span></span>

## <a name="returns"></a><span data-ttu-id="59d9d-114">返回</span><span class="sxs-lookup"><span data-stu-id="59d9d-114">Returns</span></span>

<xref:System.Xml.XmlReader>  
<span data-ttu-id="59d9d-115">一个用于读取数据流中所含数据的对象。</span><span class="sxs-lookup"><span data-stu-id="59d9d-115">An object that is used to read the XML data in the stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="59d9d-116">备注</span><span class="sxs-lookup"><span data-stu-id="59d9d-116">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="59d9d-117">`XmlReader.CreateSqlReader`方法是内部的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="59d9d-117">The `XmlReader.CreateSqlReader` method is internal and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="59d9d-118">在任何情况下，Microsoft 不支持在生产应用程序中使用此方法。</span><span class="sxs-lookup"><span data-stu-id="59d9d-118">Microsoft does not support the use of this method in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="59d9d-119">要求</span><span class="sxs-lookup"><span data-stu-id="59d9d-119">Requirements</span></span>

<span data-ttu-id="59d9d-120">**命名空间：** <xref:System.Xml></span><span class="sxs-lookup"><span data-stu-id="59d9d-120">**Namespace:** <xref:System.Xml></span></span>

<span data-ttu-id="59d9d-121">**程序集：** System.Xml.dll</span><span class="sxs-lookup"><span data-stu-id="59d9d-121">**Assembly:** System.Xml.dll</span></span>

<span data-ttu-id="59d9d-122">**.NET Framework 版本：** 自2.0 起可用。</span><span class="sxs-lookup"><span data-stu-id="59d9d-122">**.NET Framework versions:** Available since 2.0.</span></span>
