---
description: 了解详细信息： IMetaDataTables：： GetColumnInfo 方法
title: IMetaDataTables::GetColumnInfo 方法
ms.date: 10/10/2019
api_name:
- IMetaDataTables.GetColumnInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetColumnInfo
helpviewer_keywords:
- IMetaDataTables::GetColumnInfo method [.NET Framework metadata]
- GetColumnInfo method [.NET Framework metadata]
ms.assetid: 68c160ea-ae7d-4750-985d-a038b2c8e7d9
topic_type:
- apiref
ms.openlocfilehash: 21980567c5f9b364362f7e3ff02ee3a5e60b01ee
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99688216"
---
# <a name="imetadatatablesgetcolumninfo-method"></a><span data-ttu-id="bb331-103">IMetaDataTables::GetColumnInfo 方法</span><span class="sxs-lookup"><span data-stu-id="bb331-103">IMetaDataTables::GetColumnInfo Method</span></span>

<span data-ttu-id="bb331-104">获取有关指定表中指定列的数据。</span><span class="sxs-lookup"><span data-stu-id="bb331-104">Gets data about the specified column in the specified table.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bb331-105">语法</span><span class="sxs-lookup"><span data-stu-id="bb331-105">Syntax</span></span>  
  
```cpp  
HRESULT GetColumnInfo (
    [in]  ULONG        ixTbl,  
    [in]  ULONG        ixCol,  
    [out] ULONG        *poCol,  
    [out] ULONG        *pcbCol,  
    [out] ULONG        *pType,  
    [out] const char   **ppName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bb331-106">参数</span><span class="sxs-lookup"><span data-stu-id="bb331-106">Parameters</span></span>

=======

 `ixTbl`  
 <span data-ttu-id="bb331-107">中所需表的索引。</span><span class="sxs-lookup"><span data-stu-id="bb331-107">[in] The index of the desired table.</span></span>  
  
 `ixCol`  
 <span data-ttu-id="bb331-108">中所需列的索引。</span><span class="sxs-lookup"><span data-stu-id="bb331-108">[in] The index of the desired column.</span></span>  
  
 `poCol`  
 <span data-ttu-id="bb331-109">弄指向行中列的偏移量的指针。</span><span class="sxs-lookup"><span data-stu-id="bb331-109">[out] A pointer to the offset of the column in the row.</span></span>  
  
 `pcbCol`  
 <span data-ttu-id="bb331-110">弄一个指针，指向列的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="bb331-110">[out] A pointer to the size, in bytes, of the column.</span></span>  
  
 `pType`  
 <span data-ttu-id="bb331-111">弄一个指针，指向列中值的类型。</span><span class="sxs-lookup"><span data-stu-id="bb331-111">[out] A pointer to the type of the values in the column.</span></span>  
  
 `ppName`  
 <span data-ttu-id="bb331-112">弄指向列名的指针的指针。</span><span class="sxs-lookup"><span data-stu-id="bb331-112">[out] A pointer to a pointer to the column name.</span></span>  

## <a name="remarks"></a><span data-ttu-id="bb331-113">备注</span><span class="sxs-lookup"><span data-stu-id="bb331-113">Remarks</span></span>

<span data-ttu-id="bb331-114">返回的列类型位于值的范围内：</span><span class="sxs-lookup"><span data-stu-id="bb331-114">The returned column type falls within a range of values:</span></span>

| <span data-ttu-id="bb331-115">pType</span><span class="sxs-lookup"><span data-stu-id="bb331-115">pType</span></span>                    | <span data-ttu-id="bb331-116">说明</span><span class="sxs-lookup"><span data-stu-id="bb331-116">Description</span></span>   | <span data-ttu-id="bb331-117">Helper 函数</span><span class="sxs-lookup"><span data-stu-id="bb331-117">Helper function</span></span>                   |
|--------------------------|---------------|-----------------------------------|
| <span data-ttu-id="bb331-118">`0`..`iRidMax`</span><span class="sxs-lookup"><span data-stu-id="bb331-118">`0`..`iRidMax`</span></span><br><span data-ttu-id="bb331-119"> (0. 63) </span><span class="sxs-lookup"><span data-stu-id="bb331-119">(0..63)</span></span>   | <span data-ttu-id="bb331-120">去掉</span><span class="sxs-lookup"><span data-stu-id="bb331-120">Rid</span></span>           | <span data-ttu-id="bb331-121">**IsRidType**</span><span class="sxs-lookup"><span data-stu-id="bb331-121">**IsRidType**</span></span><br><span data-ttu-id="bb331-122">**IsRidOrToken**</span><span class="sxs-lookup"><span data-stu-id="bb331-122">**IsRidOrToken**</span></span> |
| <span data-ttu-id="bb331-123">`iCodedToken`..`iCodedTokenMax`</span><span class="sxs-lookup"><span data-stu-id="bb331-123">`iCodedToken`..`iCodedTokenMax`</span></span><br><span data-ttu-id="bb331-124"> (64.. 95) </span><span class="sxs-lookup"><span data-stu-id="bb331-124">(64..95)</span></span> | <span data-ttu-id="bb331-125">编码标记</span><span class="sxs-lookup"><span data-stu-id="bb331-125">Coded token</span></span> | <span data-ttu-id="bb331-126">**IsCodedTokenType**</span><span class="sxs-lookup"><span data-stu-id="bb331-126">**IsCodedTokenType**</span></span> <br><span data-ttu-id="bb331-127">**IsRidOrToken**</span><span class="sxs-lookup"><span data-stu-id="bb331-127">**IsRidOrToken**</span></span> |
| <span data-ttu-id="bb331-128">`iSHORT` (96) </span><span class="sxs-lookup"><span data-stu-id="bb331-128">`iSHORT` (96)</span></span>            | <span data-ttu-id="bb331-129">Int16</span><span class="sxs-lookup"><span data-stu-id="bb331-129">Int16</span></span>         | <span data-ttu-id="bb331-130">**IsFixedType**</span><span class="sxs-lookup"><span data-stu-id="bb331-130">**IsFixedType**</span></span>                   |
| <span data-ttu-id="bb331-131">`iUSHORT` (97) </span><span class="sxs-lookup"><span data-stu-id="bb331-131">`iUSHORT` (97)</span></span>           | <span data-ttu-id="bb331-132">UInt16</span><span class="sxs-lookup"><span data-stu-id="bb331-132">UInt16</span></span>        | <span data-ttu-id="bb331-133">**IsFixedType**</span><span class="sxs-lookup"><span data-stu-id="bb331-133">**IsFixedType**</span></span>                   |
| <span data-ttu-id="bb331-134">`iLONG` (98) </span><span class="sxs-lookup"><span data-stu-id="bb331-134">`iLONG` (98)</span></span>             | <span data-ttu-id="bb331-135">Int32</span><span class="sxs-lookup"><span data-stu-id="bb331-135">Int32</span></span>         | <span data-ttu-id="bb331-136">**IsFixedType**</span><span class="sxs-lookup"><span data-stu-id="bb331-136">**IsFixedType**</span></span>                   |
| <span data-ttu-id="bb331-137">`iULONG` (99) </span><span class="sxs-lookup"><span data-stu-id="bb331-137">`iULONG` (99)</span></span>            | <span data-ttu-id="bb331-138">UInt32</span><span class="sxs-lookup"><span data-stu-id="bb331-138">UInt32</span></span>        | <span data-ttu-id="bb331-139">**IsFixedType**</span><span class="sxs-lookup"><span data-stu-id="bb331-139">**IsFixedType**</span></span>                   |
| <span data-ttu-id="bb331-140">`iBYTE` (100) </span><span class="sxs-lookup"><span data-stu-id="bb331-140">`iBYTE` (100)</span></span>            | <span data-ttu-id="bb331-141">Byte</span><span class="sxs-lookup"><span data-stu-id="bb331-141">Byte</span></span>          | <span data-ttu-id="bb331-142">**IsFixedType**</span><span class="sxs-lookup"><span data-stu-id="bb331-142">**IsFixedType**</span></span>                   |
| <span data-ttu-id="bb331-143">`iSTRING` (101) </span><span class="sxs-lookup"><span data-stu-id="bb331-143">`iSTRING` (101)</span></span>          | <span data-ttu-id="bb331-144">字符串</span><span class="sxs-lookup"><span data-stu-id="bb331-144">String</span></span>        | <span data-ttu-id="bb331-145">**IsHeapType**</span><span class="sxs-lookup"><span data-stu-id="bb331-145">**IsHeapType**</span></span>                    |
| <span data-ttu-id="bb331-146">`iGUID` (102) </span><span class="sxs-lookup"><span data-stu-id="bb331-146">`iGUID` (102)</span></span>            | <span data-ttu-id="bb331-147">Guid</span><span class="sxs-lookup"><span data-stu-id="bb331-147">Guid</span></span>          | <span data-ttu-id="bb331-148">**IsHeapType**</span><span class="sxs-lookup"><span data-stu-id="bb331-148">**IsHeapType**</span></span>                    |
| <span data-ttu-id="bb331-149">`iBLOB` (103) </span><span class="sxs-lookup"><span data-stu-id="bb331-149">`iBLOB` (103)</span></span>            | <span data-ttu-id="bb331-150">Blob</span><span class="sxs-lookup"><span data-stu-id="bb331-150">Blob</span></span>          | <span data-ttu-id="bb331-151">**IsHeapType**</span><span class="sxs-lookup"><span data-stu-id="bb331-151">**IsHeapType**</span></span>                    |

<span data-ttu-id="bb331-152">存储在 *堆* 中的值 (即， `IsHeapType == true` 可以使用读取) ：</span><span class="sxs-lookup"><span data-stu-id="bb331-152">Values that are stored in the *heap* (that is, `IsHeapType == true`) can be read using:</span></span>

- <span data-ttu-id="bb331-153">`iSTRING`： **IMetadataTables. GetString**</span><span class="sxs-lookup"><span data-stu-id="bb331-153">`iSTRING`: **IMetadataTables.GetString**</span></span>
- <span data-ttu-id="bb331-154">`iGUID`： **IMetadataTables. GetGUID**</span><span class="sxs-lookup"><span data-stu-id="bb331-154">`iGUID`: **IMetadataTables.GetGUID**</span></span>
- <span data-ttu-id="bb331-155">`iBLOB`： **IMetadataTables. GetBlob**</span><span class="sxs-lookup"><span data-stu-id="bb331-155">`iBLOB`: **IMetadataTables.GetBlob**</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bb331-156">若要使用上表中定义的常量，请包含 `#define _DEFINE_META_DATA_META_CONSTANTS` *cor* 头文件提供的指令。</span><span class="sxs-lookup"><span data-stu-id="bb331-156">To use the constants defined in the table above, include the directive `#define _DEFINE_META_DATA_META_CONSTANTS` provided by the *cor.h* header file.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb331-157">要求</span><span class="sxs-lookup"><span data-stu-id="bb331-157">Requirements</span></span>  

 <span data-ttu-id="bb331-158">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bb331-158">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bb331-159">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="bb331-159">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="bb331-160">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="bb331-160">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="bb331-161">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bb331-161">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bb331-162">请参阅</span><span class="sxs-lookup"><span data-stu-id="bb331-162">See also</span></span>

- [<span data-ttu-id="bb331-163">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="bb331-163">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)
- [<span data-ttu-id="bb331-164">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="bb331-164">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)
