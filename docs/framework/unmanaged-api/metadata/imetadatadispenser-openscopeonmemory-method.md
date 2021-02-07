---
description: 了解详细信息： IMetaDataDispenser：： OpenScopeOnMemory 方法
title: IMetaDataDispenser::OpenScopeOnMemory 方法
ms.date: 03/30/2017
api_name:
- IMetaDataDispenser.OpenScopeOnMemory
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenser::OpenScopeOnMemory
helpviewer_keywords:
- OpenScopeOnMemory method [.NET Framework metadata]
- IMetaDataDispenser::OpenScopeOnMemory method [.NET Framework metadata]
ms.assetid: 14218249-bdec-48ae-b5fc-9f57f7ca8501
topic_type:
- apiref
ms.openlocfilehash: 589c68ab60eec55efc43d077807789e75ae1682f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753583"
---
# <a name="imetadatadispenseropenscopeonmemory-method"></a><span data-ttu-id="143f5-103">IMetaDataDispenser::OpenScopeOnMemory 方法</span><span class="sxs-lookup"><span data-stu-id="143f5-103">IMetaDataDispenser::OpenScopeOnMemory Method</span></span>

<span data-ttu-id="143f5-104">打开包含现有元数据的内存区域。</span><span class="sxs-lookup"><span data-stu-id="143f5-104">Opens an area of memory that contains existing metadata.</span></span> <span data-ttu-id="143f5-105">也就是说，此方法将打开一个指定的内存区域，其中的现有数据将被视为元数据。</span><span class="sxs-lookup"><span data-stu-id="143f5-105">That is, this method opens a specified area of memory in which the existing data is treated as metadata.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="143f5-106">语法</span><span class="sxs-lookup"><span data-stu-id="143f5-106">Syntax</span></span>  
  
```cpp  
HRESULT OpenScopeOnMemory (  
    [in]  LPCVOID     pData,
    [in]  ULONG       cbData,
    [in]  DWORD       dwOpenFlags,
    [in]  REFIID      riid,
    [out] IUnknown    **ppIUnk  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="143f5-107">参数</span><span class="sxs-lookup"><span data-stu-id="143f5-107">Parameters</span></span>  

 `pData`  
 <span data-ttu-id="143f5-108">中指定内存区域起始地址的指针。</span><span class="sxs-lookup"><span data-stu-id="143f5-108">[in] A pointer that specifies the starting address of the memory area.</span></span>  
  
 `cbData`  
 <span data-ttu-id="143f5-109">中内存区域的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="143f5-109">[in] The size of the memory area, in bytes.</span></span>  
  
 `dwOpenFlags`  
 <span data-ttu-id="143f5-110">中 [CorOpenFlags](coropenflags-enumeration.md) 枚举的一个值，用于指定要打开的模式 (读取、写入等) 。</span><span class="sxs-lookup"><span data-stu-id="143f5-110">[in] A value of the [CorOpenFlags](coropenflags-enumeration.md) enumeration to specify the mode (read, write, and so on) for opening.</span></span>  
  
 `riid`  
 <span data-ttu-id="143f5-111">中要返回的所需元数据接口的 IID;调用方将使用接口导入 (读取) 或发出 (写入) 元数据。</span><span class="sxs-lookup"><span data-stu-id="143f5-111">[in] The IID of the desired metadata interface to be returned; the caller will use the interface to import (read) or emit (write) metadata.</span></span>  
  
 <span data-ttu-id="143f5-112">的值 `riid` 必须指定一个 "导入" 或 "发出" 接口。</span><span class="sxs-lookup"><span data-stu-id="143f5-112">The value of `riid` must specify one of the "import" or "emit" interfaces.</span></span> <span data-ttu-id="143f5-113">有效值为 IID_IMetaDataEmit、IID_IMetaDataImport、IID_IMetaDataAssemblyEmit、IID_IMetaDataAssemblyImport、IID_IMetaDataEmit2 或 IID_IMetaDataImport2。</span><span class="sxs-lookup"><span data-stu-id="143f5-113">Valid values are IID_IMetaDataEmit, IID_IMetaDataImport, IID_IMetaDataAssemblyEmit, IID_IMetaDataAssemblyImport, IID_IMetaDataEmit2, or IID_IMetaDataImport2.</span></span>  
  
 `ppIUnk`  
 <span data-ttu-id="143f5-114">弄指向返回的接口的指针。</span><span class="sxs-lookup"><span data-stu-id="143f5-114">[out] The pointer to the returned interface.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="143f5-115">备注</span><span class="sxs-lookup"><span data-stu-id="143f5-115">Remarks</span></span>  

 <span data-ttu-id="143f5-116">可以使用 "导入" 接口中的方法查询元数据的内存中副本，或使用 "发出" 接口之一中的方法将其添加到中。</span><span class="sxs-lookup"><span data-stu-id="143f5-116">The in-memory copy of the metadata can be queried using methods from one of the "import" interfaces, or added to using methods from the one of the "emit" interfaces.</span></span>  
  
 <span data-ttu-id="143f5-117">`OpenScopeOnMemory`方法类似于[IMetaDataDispenser：： OpenScope](imetadatadispenser-openscope-method.md)方法，不同之处在于相关元数据已存在于内存中，而不是位于磁盘上的文件中。</span><span class="sxs-lookup"><span data-stu-id="143f5-117">The `OpenScopeOnMemory` method is similar to the [IMetaDataDispenser::OpenScope](imetadatadispenser-openscope-method.md) method, except that the metadata of interest already exists in memory, rather than in a file on disk.</span></span>  
  
 <span data-ttu-id="143f5-118">如果内存的目标区域不包含公共语言运行时 (CLR) 元数据，则该 `OpenScopeOnMemory` 方法将失败。</span><span class="sxs-lookup"><span data-stu-id="143f5-118">If the target area of memory does not contain common language runtime (CLR) metadata, the `OpenScopeOnMemory` method will fail.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="143f5-119">要求</span><span class="sxs-lookup"><span data-stu-id="143f5-119">Requirements</span></span>  

 <span data-ttu-id="143f5-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="143f5-120">**Platform:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="143f5-121">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="143f5-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="143f5-122">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="143f5-122">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="143f5-123">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="143f5-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="143f5-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="143f5-124">See also</span></span>

- [<span data-ttu-id="143f5-125">IMetaDataDispenser 接口</span><span class="sxs-lookup"><span data-stu-id="143f5-125">IMetaDataDispenser Interface</span></span>](imetadatadispenser-interface.md)
- [<span data-ttu-id="143f5-126">IMetaDataDispenserEx 接口</span><span class="sxs-lookup"><span data-stu-id="143f5-126">IMetaDataDispenserEx Interface</span></span>](imetadatadispenserex-interface.md)
- [<span data-ttu-id="143f5-127">IMetaDataAssemblyEmit 接口</span><span class="sxs-lookup"><span data-stu-id="143f5-127">IMetaDataAssemblyEmit Interface</span></span>](imetadataassemblyemit-interface.md)
- [<span data-ttu-id="143f5-128">IMetaDataAssemblyImport 接口</span><span class="sxs-lookup"><span data-stu-id="143f5-128">IMetaDataAssemblyImport Interface</span></span>](imetadataassemblyimport-interface.md)
- [<span data-ttu-id="143f5-129">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="143f5-129">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="143f5-130">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="143f5-130">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
- [<span data-ttu-id="143f5-131">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="143f5-131">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="143f5-132">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="143f5-132">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
