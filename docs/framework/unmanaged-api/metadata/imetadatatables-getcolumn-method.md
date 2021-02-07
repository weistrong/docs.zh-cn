---
description: 了解详细信息： IMetaDataTables：： GetColumn 方法
title: IMetaDataTables::GetColumn 方法
ms.date: 02/25/2019
api_name:
- IMetaDataTables.GetColumn
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetColumn
helpviewer_keywords:
- IMetaDataTables::GetColumn method [.NET Framework metadata]
- GetColumn method [.NET Framework metadata]
ms.assetid: 1032055b-cabb-45c5-a50e-7e853201b175
topic_type:
- apiref
ms.openlocfilehash: 4c4cec7216f93783b34b594330358d1e6036ed40
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99688255"
---
# <a name="imetadatatablesgetcolumn-method"></a><span data-ttu-id="c79c4-103">IMetaDataTables::GetColumn 方法</span><span class="sxs-lookup"><span data-stu-id="c79c4-103">IMetaDataTables::GetColumn Method</span></span>

<span data-ttu-id="c79c4-104">获取一个指针，该指针指向给定表中指定列和行的单元中包含的值。</span><span class="sxs-lookup"><span data-stu-id="c79c4-104">Gets a pointer to the value contained in the cell of the specified column and row in the given table.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c79c4-105">语法</span><span class="sxs-lookup"><span data-stu-id="c79c4-105">Syntax</span></span>  
  
```cpp  
HRESULT GetColumn (
    [in]  ULONG   ixTbl,  
    [in]  ULONG   ixCol,  
    [in]  ULONG   rid,  
    [out] ULONG   *pVal  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c79c4-106">参数</span><span class="sxs-lookup"><span data-stu-id="c79c4-106">Parameters</span></span>

 `ixTbl`  
 <span data-ttu-id="c79c4-107">中表的索引。</span><span class="sxs-lookup"><span data-stu-id="c79c4-107">[in] The index of the table.</span></span>  
  
 `ixCol`  
 <span data-ttu-id="c79c4-108">中表中的列的索引。</span><span class="sxs-lookup"><span data-stu-id="c79c4-108">[in] The index of the column in the table.</span></span>  
  
 `rid`  
 <span data-ttu-id="c79c4-109">中表中的行的索引。</span><span class="sxs-lookup"><span data-stu-id="c79c4-109">[in] The index of the row in the table.</span></span>  
  
 `pVal`  
 <span data-ttu-id="c79c4-110">弄指向单元格中的值的指针。</span><span class="sxs-lookup"><span data-stu-id="c79c4-110">[out] A pointer to the value in the cell.</span></span>  

## <a name="remarks"></a><span data-ttu-id="c79c4-111">备注</span><span class="sxs-lookup"><span data-stu-id="c79c4-111">Remarks</span></span>

<span data-ttu-id="c79c4-112">返回的值的 interpretion `pVal` 取决于列的类型。</span><span class="sxs-lookup"><span data-stu-id="c79c4-112">The interpretion of the value returned through `pVal` depends on the column's type.</span></span> <span data-ttu-id="c79c4-113">列类型可通过调用 [IMetaDataTables](imetadatatables-getcolumninfo-method.md)来确定。</span><span class="sxs-lookup"><span data-stu-id="c79c4-113">The column type can be determined by calling [IMetaDataTables.GetColumnInfo](imetadatatables-getcolumninfo-method.md).</span></span>

- <span data-ttu-id="c79c4-114">**GetColumn** 方法自动将 **Rid** 或 **CodedToken** 类型的列转换为完整的32位 `mdToken` 值。</span><span class="sxs-lookup"><span data-stu-id="c79c4-114">The **GetColumn** method automatically converts columns of type **Rid** or **CodedToken** to full 32-bit `mdToken` values.</span></span>
- <span data-ttu-id="c79c4-115">它还会自动将8位或16位值转换为完整的32位值。</span><span class="sxs-lookup"><span data-stu-id="c79c4-115">It also automatically converts 8-bit or 16-bit values to full 32-bit values.</span></span>
- <span data-ttu-id="c79c4-116">对于 *堆* 类型列，返回的 *pVal* 将是对应堆中的索引。</span><span class="sxs-lookup"><span data-stu-id="c79c4-116">For *heap* type columns, the returned *pVal* will be an index into the corresponding heap.</span></span>

| <span data-ttu-id="c79c4-117">列类型</span><span class="sxs-lookup"><span data-stu-id="c79c4-117">Column type</span></span>              | <span data-ttu-id="c79c4-118">pVal 包含</span><span class="sxs-lookup"><span data-stu-id="c79c4-118">pVal contains</span></span> | <span data-ttu-id="c79c4-119">评论</span><span class="sxs-lookup"><span data-stu-id="c79c4-119">Comment</span></span>                          |
|--------------------------|---------------|-----------------------------------|
| <span data-ttu-id="c79c4-120">`0`..`iRidMax`</span><span class="sxs-lookup"><span data-stu-id="c79c4-120">`0`..`iRidMax`</span></span><br><span data-ttu-id="c79c4-121"> (0. 63) </span><span class="sxs-lookup"><span data-stu-id="c79c4-121">(0..63)</span></span>  | <span data-ttu-id="c79c4-122">mdToken</span><span class="sxs-lookup"><span data-stu-id="c79c4-122">mdToken</span></span>     | <span data-ttu-id="c79c4-123">*pVal* 将包含一个完整的令牌。</span><span class="sxs-lookup"><span data-stu-id="c79c4-123">*pVal* will contain a full Token.</span></span> <span data-ttu-id="c79c4-124">函数自动将 Rid 转换为完整的标记。</span><span class="sxs-lookup"><span data-stu-id="c79c4-124">The function automatically converts the Rid into a full token.</span></span> |
| <span data-ttu-id="c79c4-125">`iCodedToken`..`iCodedTokenMax`</span><span class="sxs-lookup"><span data-stu-id="c79c4-125">`iCodedToken`..`iCodedTokenMax`</span></span><br><span data-ttu-id="c79c4-126"> (64.. 95) </span><span class="sxs-lookup"><span data-stu-id="c79c4-126">(64..95)</span></span> | <span data-ttu-id="c79c4-127">mdToken</span><span class="sxs-lookup"><span data-stu-id="c79c4-127">mdToken</span></span> | <span data-ttu-id="c79c4-128">返回后， *pVal* 将包含一个完整的令牌。</span><span class="sxs-lookup"><span data-stu-id="c79c4-128">Upon return, *pVal* will contain a full Token.</span></span> <span data-ttu-id="c79c4-129">函数自动将 CodedToken 解压缩到完整的令牌中。</span><span class="sxs-lookup"><span data-stu-id="c79c4-129">The function automatically decompresses the CodedToken into a full token.</span></span> |
| <span data-ttu-id="c79c4-130">`iSHORT` (96) </span><span class="sxs-lookup"><span data-stu-id="c79c4-130">`iSHORT` (96)</span></span>            | <span data-ttu-id="c79c4-131">Int16</span><span class="sxs-lookup"><span data-stu-id="c79c4-131">Int16</span></span>         | <span data-ttu-id="c79c4-132">自动将符号扩展为32位。</span><span class="sxs-lookup"><span data-stu-id="c79c4-132">Automatically sign-extended to 32-bit.</span></span>  |
| <span data-ttu-id="c79c4-133">`iUSHORT` (97) </span><span class="sxs-lookup"><span data-stu-id="c79c4-133">`iUSHORT` (97)</span></span>           | <span data-ttu-id="c79c4-134">UInt16</span><span class="sxs-lookup"><span data-stu-id="c79c4-134">UInt16</span></span>        | <span data-ttu-id="c79c4-135">自动将符号扩展为32位。</span><span class="sxs-lookup"><span data-stu-id="c79c4-135">Automatically sign-extended to 32-bit.</span></span>  |
| <span data-ttu-id="c79c4-136">`iLONG` (98) </span><span class="sxs-lookup"><span data-stu-id="c79c4-136">`iLONG` (98)</span></span>             | <span data-ttu-id="c79c4-137">Int32</span><span class="sxs-lookup"><span data-stu-id="c79c4-137">Int32</span></span>         |                                        |
| <span data-ttu-id="c79c4-138">`iULONG` (99) </span><span class="sxs-lookup"><span data-stu-id="c79c4-138">`iULONG` (99)</span></span>            | <span data-ttu-id="c79c4-139">UInt32</span><span class="sxs-lookup"><span data-stu-id="c79c4-139">UInt32</span></span>        |                                        |
| <span data-ttu-id="c79c4-140">`iBYTE` (100) </span><span class="sxs-lookup"><span data-stu-id="c79c4-140">`iBYTE` (100)</span></span>            | <span data-ttu-id="c79c4-141">Byte</span><span class="sxs-lookup"><span data-stu-id="c79c4-141">Byte</span></span>          | <span data-ttu-id="c79c4-142">自动将符号扩展为32位。</span><span class="sxs-lookup"><span data-stu-id="c79c4-142">Automatically sign-extended to 32-bit.</span></span>  |
| <span data-ttu-id="c79c4-143">`iSTRING` (101) </span><span class="sxs-lookup"><span data-stu-id="c79c4-143">`iSTRING` (101)</span></span>          | <span data-ttu-id="c79c4-144">字符串堆索引</span><span class="sxs-lookup"><span data-stu-id="c79c4-144">String heap index</span></span> | <span data-ttu-id="c79c4-145">*pVal* 是字符串堆中的索引。</span><span class="sxs-lookup"><span data-stu-id="c79c4-145">*pVal* is an index into the String heap.</span></span> <span data-ttu-id="c79c4-146">使用 [IMetadataTables：： GetString](imetadatatables-getstring-method.md) 获取实际的列字符串值。</span><span class="sxs-lookup"><span data-stu-id="c79c4-146">Use [IMetadataTables::GetString](imetadatatables-getstring-method.md) to get the actual column String value.</span></span> |
| <span data-ttu-id="c79c4-147">`iGUID` (102) </span><span class="sxs-lookup"><span data-stu-id="c79c4-147">`iGUID` (102)</span></span>            | <span data-ttu-id="c79c4-148">Guid 堆索引</span><span class="sxs-lookup"><span data-stu-id="c79c4-148">Guid heap index</span></span> | <span data-ttu-id="c79c4-149">*pVal* 是 Guid 堆中的索引。</span><span class="sxs-lookup"><span data-stu-id="c79c4-149">*pVal* is an index into the Guid heap.</span></span> <span data-ttu-id="c79c4-150">使用 [IMetadataTables：： GetGuid](imetadatatables-getguid-method.md) 获取实际的列 Guid 值。</span><span class="sxs-lookup"><span data-stu-id="c79c4-150">Use [IMetadataTables::GetGuid](imetadatatables-getguid-method.md) to get the actual column Guid value.</span></span> |
| <span data-ttu-id="c79c4-151">`iBLOB` (103) </span><span class="sxs-lookup"><span data-stu-id="c79c4-151">`iBLOB` (103)</span></span>            | <span data-ttu-id="c79c4-152">Blob 堆索引</span><span class="sxs-lookup"><span data-stu-id="c79c4-152">Blob heap index</span></span> | <span data-ttu-id="c79c4-153">*pVal* 是 Blob 堆中的索引。</span><span class="sxs-lookup"><span data-stu-id="c79c4-153">*pVal* is an index into the Blob heap.</span></span> <span data-ttu-id="c79c4-154">使用 [IMetadataTables：： GetBlob](imetadatatables-getblob-method.md) 获取实际的列 Blob 值。</span><span class="sxs-lookup"><span data-stu-id="c79c4-154">Use [IMetadataTables::GetBlob](imetadatatables-getblob-method.md) to get the actual column Blob value.</span></span> |
  
## <a name="requirements"></a><span data-ttu-id="c79c4-155">要求</span><span class="sxs-lookup"><span data-stu-id="c79c4-155">Requirements</span></span>  

 <span data-ttu-id="c79c4-156">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c79c4-156">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c79c4-157">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="c79c4-157">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c79c4-158">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="c79c4-158">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="c79c4-159">**.NET Framework 版本**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c79c4-159">**.NET Framework Versions** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c79c4-160">请参阅</span><span class="sxs-lookup"><span data-stu-id="c79c4-160">See also</span></span>

- [<span data-ttu-id="c79c4-161">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="c79c4-161">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)
- [<span data-ttu-id="c79c4-162">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="c79c4-162">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)
