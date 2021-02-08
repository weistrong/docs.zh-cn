---
description: 了解详细信息： IMetaDataTables 接口
title: IMetaDataTables 接口
ms.date: 03/30/2017
api_name:
- IMetaDataTables
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables
helpviewer_keywords:
- IMetaDataTables interface [.NET Framework metadata]
ms.assetid: 31272cce-506a-4f18-bcbf-01ee45e36356
topic_type:
- apiref
ms.openlocfilehash: c3edf504586bad1252c36d6e8254193eaf9cc26d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799260"
---
# <a name="imetadatatables-interface"></a><span data-ttu-id="486c4-103">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="486c4-103">IMetaDataTables Interface</span></span>

<span data-ttu-id="486c4-104">提供存储和检索表中元数据信息的方法。</span><span class="sxs-lookup"><span data-stu-id="486c4-104">Provides methods for the storage and retrieval of metadata information in tables.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="486c4-105">方法</span><span class="sxs-lookup"><span data-stu-id="486c4-105">Methods</span></span>  
  
|<span data-ttu-id="486c4-106">方法</span><span class="sxs-lookup"><span data-stu-id="486c4-106">Method</span></span>|<span data-ttu-id="486c4-107">说明</span><span class="sxs-lookup"><span data-stu-id="486c4-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="486c4-108">GetBlob 方法</span><span class="sxs-lookup"><span data-stu-id="486c4-108">GetBlob Method</span></span>](imetadatatables-getblob-method.md)|<span data-ttu-id="486c4-109">获取一个指针，该指针指向指定列索引 (BLOB) 的二进制大型对象。</span><span class="sxs-lookup"><span data-stu-id="486c4-109">Gets a pointer to the binary large object (BLOB) at the specified column index.</span></span>|  
|[<span data-ttu-id="486c4-110">GetBlobHeapSize 方法</span><span class="sxs-lookup"><span data-stu-id="486c4-110">GetBlobHeapSize Method</span></span>](imetadatatables-getblobheapsize-method.md)|<span data-ttu-id="486c4-111">获取 BLOB 堆的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="486c4-111">Gets the size, in bytes, of the BLOB heap.</span></span>|  
|[<span data-ttu-id="486c4-112">GetCodedTokenInfo 方法</span><span class="sxs-lookup"><span data-stu-id="486c4-112">GetCodedTokenInfo Method</span></span>](imetadatatables-getcodedtokeninfo-method.md)|<span data-ttu-id="486c4-113">获取一个指针，该指针指向与指定的行索引相关联的标记的数组。</span><span class="sxs-lookup"><span data-stu-id="486c4-113">Gets a pointer to an array of tokens associated with the specified row index.</span></span>|  
|[<span data-ttu-id="486c4-114">GetColumn 方法</span><span class="sxs-lookup"><span data-stu-id="486c4-114">GetColumn Method</span></span>](imetadatatables-getcolumn-method.md)|<span data-ttu-id="486c4-115">获取一个指针，该指针指向指定表索引处的表中指定列索引处的列中包含的值。</span><span class="sxs-lookup"><span data-stu-id="486c4-115">Gets a pointer to the values contained in the column at the specified column index, in the table at the specified table index.</span></span>|  
|[<span data-ttu-id="486c4-116">GetColumnInfo 方法</span><span class="sxs-lookup"><span data-stu-id="486c4-116">GetColumnInfo Method</span></span>](imetadatatables-getcolumninfo-method.md)|<span data-ttu-id="486c4-117">获取有关指定表中指定列的数据。</span><span class="sxs-lookup"><span data-stu-id="486c4-117">Gets data about the specified column in the specified table.</span></span>|  
|[<span data-ttu-id="486c4-118">GetGuid 方法</span><span class="sxs-lookup"><span data-stu-id="486c4-118">GetGuid Method</span></span>](imetadatatables-getguid-method.md)|<span data-ttu-id="486c4-119">获取指定索引处的行的 GUID。</span><span class="sxs-lookup"><span data-stu-id="486c4-119">Gets a GUID from the row at the specified index.</span></span>|  
|[<span data-ttu-id="486c4-120">GetGuidHeapSize 方法</span><span class="sxs-lookup"><span data-stu-id="486c4-120">GetGuidHeapSize Method</span></span>](imetadatatables-getguidheapsize-method.md)|<span data-ttu-id="486c4-121">获取 GUID 堆的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="486c4-121">Gets the size, in bytes, of the GUID heap.</span></span>|  
|[<span data-ttu-id="486c4-122">GetNextBlob 方法</span><span class="sxs-lookup"><span data-stu-id="486c4-122">GetNextBlob Method</span></span>](imetadatatables-getnextblob-method.md)|<span data-ttu-id="486c4-123">获取表中下一个 BLOB 的索引。</span><span class="sxs-lookup"><span data-stu-id="486c4-123">Gets the index of the next BLOB in the table.</span></span>|  
|[<span data-ttu-id="486c4-124">GetNextGuid 方法</span><span class="sxs-lookup"><span data-stu-id="486c4-124">GetNextGuid Method</span></span>](imetadatatables-getnextguid-method.md)|<span data-ttu-id="486c4-125">获取当前表列中的下一个 GUID 值的索引。</span><span class="sxs-lookup"><span data-stu-id="486c4-125">Gets the index of the next GUID value in the current table column.</span></span>|  
|[<span data-ttu-id="486c4-126">GetNextString 方法</span><span class="sxs-lookup"><span data-stu-id="486c4-126">GetNextString Method</span></span>](imetadatatables-getnextstring-method.md)|<span data-ttu-id="486c4-127">获取当前表列中的下一个字符串的索引。</span><span class="sxs-lookup"><span data-stu-id="486c4-127">Gets the index of the next string in the current table column.</span></span>|  
|[<span data-ttu-id="486c4-128">GetNextUserString 方法</span><span class="sxs-lookup"><span data-stu-id="486c4-128">GetNextUserString Method</span></span>](imetadatatables-getnextuserstring-method.md)|<span data-ttu-id="486c4-129">获取包含当前表列中的下一个硬编码字符串的行的索引。</span><span class="sxs-lookup"><span data-stu-id="486c4-129">Gets the index of the row that contains the next hard-coded string in the current table column.</span></span>|  
|[<span data-ttu-id="486c4-130">GetNumTables 方法</span><span class="sxs-lookup"><span data-stu-id="486c4-130">GetNumTables Method</span></span>](imetadatatables-getnumtables-method.md)|<span data-ttu-id="486c4-131">获取当前实例的范围中的表数 `IMetaDataTables` 。</span><span class="sxs-lookup"><span data-stu-id="486c4-131">Gets the number of tables in the scope of the current `IMetaDataTables` instance.</span></span>|  
|[<span data-ttu-id="486c4-132">GetRow 方法</span><span class="sxs-lookup"><span data-stu-id="486c4-132">GetRow Method</span></span>](imetadatatables-getrow-method.md)|<span data-ttu-id="486c4-133">获取位于指定表索引处的表中指定行索引处的行。</span><span class="sxs-lookup"><span data-stu-id="486c4-133">Gets the row at the specified row index, in the table at the specified table index.</span></span>|  
|[<span data-ttu-id="486c4-134">GetString 方法</span><span class="sxs-lookup"><span data-stu-id="486c4-134">GetString Method</span></span>](imetadatatables-getstring-method.md)|<span data-ttu-id="486c4-135">从当前引用范围内的表列中获取指定索引处的字符串。</span><span class="sxs-lookup"><span data-stu-id="486c4-135">Gets the string at the specified index from the table column in the current reference scope.</span></span>|  
|[<span data-ttu-id="486c4-136">GetStringHeapSize 方法</span><span class="sxs-lookup"><span data-stu-id="486c4-136">GetStringHeapSize Method</span></span>](imetadatatables-getstringheapsize-method.md)|<span data-ttu-id="486c4-137">获取字符串堆的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="486c4-137">Gets the size, in bytes, of the string heap.</span></span>|  
|[<span data-ttu-id="486c4-138">GetTableIndex 方法</span><span class="sxs-lookup"><span data-stu-id="486c4-138">GetTableIndex Method</span></span>](imetadatatables-gettableindex-method.md)|<span data-ttu-id="486c4-139">获取指定的标记所引用的表的索引。</span><span class="sxs-lookup"><span data-stu-id="486c4-139">Gets the index for the table referenced by the specified token.</span></span>|  
|[<span data-ttu-id="486c4-140">GetTableInfo 方法</span><span class="sxs-lookup"><span data-stu-id="486c4-140">GetTableInfo Method</span></span>](imetadatatables-gettableinfo-method.md)|<span data-ttu-id="486c4-141">获取指定表索引处的表的名称、行大小、行数、列数和键列索引。</span><span class="sxs-lookup"><span data-stu-id="486c4-141">Gets the name, row size, number of rows, number of columns, and key column index of the table at the specified table index.</span></span>|  
|[<span data-ttu-id="486c4-142">GetUserString 方法</span><span class="sxs-lookup"><span data-stu-id="486c4-142">GetUserString Method</span></span>](imetadatatables-getuserstring-method.md)|<span data-ttu-id="486c4-143">获取当前范围内字符串列中指定索引处的硬编码字符串。</span><span class="sxs-lookup"><span data-stu-id="486c4-143">Gets the hard-coded string at the specified index in the string column in the current scope.</span></span>|  
|[<span data-ttu-id="486c4-144">GetUserStringHeapSize 方法</span><span class="sxs-lookup"><span data-stu-id="486c4-144">GetUserStringHeapSize Method</span></span>](imetadatatables-getuserstringheapsize-method.md)|<span data-ttu-id="486c4-145">获取用户字符串堆的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="486c4-145">Gets the size, in bytes, of the user string heap.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="486c4-146">要求</span><span class="sxs-lookup"><span data-stu-id="486c4-146">Requirements</span></span>  

 <span data-ttu-id="486c4-147">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="486c4-147">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="486c4-148">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="486c4-148">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="486c4-149">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="486c4-149">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="486c4-150">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="486c4-150">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="486c4-151">请参阅</span><span class="sxs-lookup"><span data-stu-id="486c4-151">See also</span></span>

- [<span data-ttu-id="486c4-152">元数据接口</span><span class="sxs-lookup"><span data-stu-id="486c4-152">Metadata Interfaces</span></span>](metadata-interfaces.md)
- [<span data-ttu-id="486c4-153">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="486c4-153">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)
