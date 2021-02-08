---
description: 了解详细信息： MemoryStream. InternalGetOriginAndLength 方法
title: 'MemoryStream. InternalGetOriginAndLength 方法 (System.IO) '
ms.date: 11/19/2019
topic_type:
- apiref
api_name:
- System.IO.MemoryStream.InternalGetOriginAndLength
api_location:
- mscorlib.dll
api_type:
- Assembly
ms.openlocfilehash: 4232852c0835a43454f36271a43062e1240297a5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802536"
---
# <a name="memorystreaminternalgetoriginandlength-method"></a><span data-ttu-id="e8986-103">MemoryStream.InternalGetOriginAndLength 方法</span><span class="sxs-lookup"><span data-stu-id="e8986-103">MemoryStream.InternalGetOriginAndLength method</span></span>

<span data-ttu-id="e8986-104">获取内存流的源的内部值和长度。</span><span class="sxs-lookup"><span data-stu-id="e8986-104">Gets the internal values of origin and length of the memory stream.</span></span>

```csharp
internal void InternalGetOriginAndLength(out int origin, out int length)
```

## <a name="parameters"></a><span data-ttu-id="e8986-105">参数</span><span class="sxs-lookup"><span data-stu-id="e8986-105">Parameters</span></span>

- <span data-ttu-id="e8986-106">`origin` <xref:System.Int32></span><span class="sxs-lookup"><span data-stu-id="e8986-106">`origin` <xref:System.Int32></span></span>\
  <span data-ttu-id="e8986-107">此方法返回时，创建新对象时指定的字节数组的偏移量 <xref:System.IO.MemoryStream> 。</span><span class="sxs-lookup"><span data-stu-id="e8986-107">When this method returns, the offset of the byte array specified when creating a new <xref:System.IO.MemoryStream> object.</span></span> <span data-ttu-id="e8986-108">如果创建字节数组，则包含 0 <xref:System.IO.MemoryStream> 。</span><span class="sxs-lookup"><span data-stu-id="e8986-108">Contains 0 if the byte array was created by <xref:System.IO.MemoryStream>.</span></span>

- <span data-ttu-id="e8986-109">`length` <xref:System.Int32></span><span class="sxs-lookup"><span data-stu-id="e8986-109">`length` <xref:System.Int32></span></span>\
  <span data-ttu-id="e8986-110">此方法返回时，为内存流中的字节数。</span><span class="sxs-lookup"><span data-stu-id="e8986-110">When this method returns, the number of bytes within the memory stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8986-111">备注</span><span class="sxs-lookup"><span data-stu-id="e8986-111">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="e8986-112">`MemoryStream.InternalGetOriginAndLength`方法是内部的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="e8986-112">The `MemoryStream.InternalGetOriginAndLength` method is internal and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="e8986-113">在任何情况下，Microsoft 不支持在生产应用程序中使用此方法。</span><span class="sxs-lookup"><span data-stu-id="e8986-113">Microsoft does not support the use of this method in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8986-114">要求</span><span class="sxs-lookup"><span data-stu-id="e8986-114">Requirements</span></span>

<span data-ttu-id="e8986-115">**命名空间：** <xref:System.IO></span><span class="sxs-lookup"><span data-stu-id="e8986-115">**Namespace:** <xref:System.IO></span></span>

<span data-ttu-id="e8986-116">**程序集：** mscorlib.dll (mscorlib.dll 中) </span><span class="sxs-lookup"><span data-stu-id="e8986-116">**Assembly:** mscorlib.dll (in mscorlib.dll)</span></span>

<span data-ttu-id="e8986-117">**.NET Framework 版本：** 自2.0 起可用。</span><span class="sxs-lookup"><span data-stu-id="e8986-117">**.NET Framework versions:** Available since 2.0.</span></span>
