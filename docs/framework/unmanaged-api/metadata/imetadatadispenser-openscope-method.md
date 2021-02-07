---
description: 了解详细信息： IMetaDataDispenser：： OpenScope 方法
title: IMetaDataDispenser::OpenScope 方法
ms.date: 03/30/2017
api_name:
- IMetaDataDispenser.OpenScope
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenser::OpenScope
helpviewer_keywords:
- IMetaDataDispenser::OpenScope method [.NET Framework metadata]
- OpenScope method, IMetaDataDispenser interface [.NET Framework metadata]
ms.assetid: 65063ad5-e0d9-4c01-8f8b-9a5950109fa6
topic_type:
- apiref
ms.openlocfilehash: a1fa9a955bfc38ee4b2f23efbe8e492877a3d0c6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753609"
---
# <a name="imetadatadispenseropenscope-method"></a><span data-ttu-id="d726a-103">IMetaDataDispenser::OpenScope 方法</span><span class="sxs-lookup"><span data-stu-id="d726a-103">IMetaDataDispenser::OpenScope Method</span></span>

<span data-ttu-id="d726a-104">打开现有的磁盘上的文件，并将其元数据映射到内存。</span><span class="sxs-lookup"><span data-stu-id="d726a-104">Opens an existing, on-disk file and maps its metadata into memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d726a-105">语法</span><span class="sxs-lookup"><span data-stu-id="d726a-105">Syntax</span></span>  
  
```cpp  
HRESULT OpenScope (  
    [in]  LPCWSTR     szScope,
    [in]  DWORD       dwOpenFlags,
    [in]  REFIID      riid,
    [out] IUnknown    **ppIUnk  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d726a-106">参数</span><span class="sxs-lookup"><span data-stu-id="d726a-106">Parameters</span></span>  

 `szScope`  
 <span data-ttu-id="d726a-107">中要打开的文件的名称。</span><span class="sxs-lookup"><span data-stu-id="d726a-107">[in] The name of the file to be opened.</span></span> <span data-ttu-id="d726a-108">文件必须包含公共语言运行时 (CLR) 元数据。</span><span class="sxs-lookup"><span data-stu-id="d726a-108">The file must contain common language runtime (CLR) metadata.</span></span>  
  
 `dwOpenFlags`  
 <span data-ttu-id="d726a-109">中 [CorOpenFlags](coropenflags-enumeration.md) 枚举的一个值，用于指定要打开的模式 (读取、写入等) 。</span><span class="sxs-lookup"><span data-stu-id="d726a-109">[in] A value of the [CorOpenFlags](coropenflags-enumeration.md) enumeration to specify the mode (read, write, and so on) for opening.</span></span>  
  
 `riid`  
 <span data-ttu-id="d726a-110">中要返回的所需元数据接口的 IID;调用方将使用接口导入 (读取) 或发出 (写入) 元数据。</span><span class="sxs-lookup"><span data-stu-id="d726a-110">[in] The IID of the desired metadata interface to be returned; the caller will use the interface to import (read) or emit (write) metadata.</span></span>  
  
 <span data-ttu-id="d726a-111">的值 `riid` 必须指定一个 "导入" 或 "发出" 接口。</span><span class="sxs-lookup"><span data-stu-id="d726a-111">The value of `riid` must specify one of the "import" or "emit" interfaces.</span></span> <span data-ttu-id="d726a-112">有效值为 IID_IMetaDataEmit、IID_IMetaDataImport、IID_IMetaDataAssemblyEmit、IID_IMetaDataAssemblyImport、IID_IMetaDataEmit2 或 IID_IMetaDataImport2。</span><span class="sxs-lookup"><span data-stu-id="d726a-112">Valid values are IID_IMetaDataEmit, IID_IMetaDataImport, IID_IMetaDataAssemblyEmit, IID_IMetaDataAssemblyImport, IID_IMetaDataEmit2, or IID_IMetaDataImport2.</span></span>  
  
 `ppIUnk`  
 <span data-ttu-id="d726a-113">弄指向返回的接口的指针。</span><span class="sxs-lookup"><span data-stu-id="d726a-113">[out] The pointer to the returned interface.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d726a-114">备注</span><span class="sxs-lookup"><span data-stu-id="d726a-114">Remarks</span></span>  

 <span data-ttu-id="d726a-115">可以使用 "导入" 接口中的方法查询元数据的内存中副本，或使用 "发出" 接口之一中的方法将其添加到中。</span><span class="sxs-lookup"><span data-stu-id="d726a-115">The in-memory copy of the metadata can be queried using methods from one of the "import" interfaces, or added to using methods from the one of the "emit" interfaces.</span></span>  
  
 <span data-ttu-id="d726a-116">如果目标文件不包含 CLR 元数据，则该 `OpenScope` 方法将失败。</span><span class="sxs-lookup"><span data-stu-id="d726a-116">If the target file does not contain CLR metadata, the `OpenScope` method will fail.</span></span>  
  
 <span data-ttu-id="d726a-117">在 .NET Framework 版本1.0 和1.1 版中，如果在 `dwOpenFlags` 设置为 ofRead 的情况下打开范围，则它有资格进行共享。</span><span class="sxs-lookup"><span data-stu-id="d726a-117">In the .NET Framework version 1.0 and version 1.1, if a scope is opened with `dwOpenFlags` set to ofRead, it is eligible for sharing.</span></span> <span data-ttu-id="d726a-118">也就是说，如果后续调用 `OpenScope` 传入以前打开的文件的名称，则将重用现有范围并不创建新的数据结构集。</span><span class="sxs-lookup"><span data-stu-id="d726a-118">That is, if subsequent calls to `OpenScope` pass in the name of a file that was previously opened, the existing scope is reused and a new set of data structures is not created.</span></span> <span data-ttu-id="d726a-119">但是，这种共享可能导致问题。</span><span class="sxs-lookup"><span data-stu-id="d726a-119">However, problems can arise due to this sharing.</span></span>  
  
 <span data-ttu-id="d726a-120">在 .NET Framework 版本2.0 中， `dwOpenFlags` 将不再共享用设置为 ofRead 打开的作用域。</span><span class="sxs-lookup"><span data-stu-id="d726a-120">In the .NET Framework version 2.0, scopes opened with `dwOpenFlags` set to ofRead are no longer shared.</span></span> <span data-ttu-id="d726a-121">使用 ofReadOnly 值允许共享作用域。</span><span class="sxs-lookup"><span data-stu-id="d726a-121">Use the ofReadOnly value to allow the scope to be shared.</span></span> <span data-ttu-id="d726a-122">共享作用域时，使用 "读/写" 元数据接口的查询会失败。</span><span class="sxs-lookup"><span data-stu-id="d726a-122">When a scope is shared, queries that use "read/write" metadata interfaces will fail.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d726a-123">要求</span><span class="sxs-lookup"><span data-stu-id="d726a-123">Requirements</span></span>  

 <span data-ttu-id="d726a-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d726a-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d726a-125">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="d726a-125">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="d726a-126">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="d726a-126">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d726a-127">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d726a-127">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d726a-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="d726a-128">See also</span></span>

- [<span data-ttu-id="d726a-129">IMetaDataDispenser 接口</span><span class="sxs-lookup"><span data-stu-id="d726a-129">IMetaDataDispenser Interface</span></span>](imetadatadispenser-interface.md)
- [<span data-ttu-id="d726a-130">IMetaDataDispenserEx 接口</span><span class="sxs-lookup"><span data-stu-id="d726a-130">IMetaDataDispenserEx Interface</span></span>](imetadatadispenserex-interface.md)
- [<span data-ttu-id="d726a-131">IMetaDataAssemblyEmit 接口</span><span class="sxs-lookup"><span data-stu-id="d726a-131">IMetaDataAssemblyEmit Interface</span></span>](imetadataassemblyemit-interface.md)
- [<span data-ttu-id="d726a-132">IMetaDataAssemblyImport 接口</span><span class="sxs-lookup"><span data-stu-id="d726a-132">IMetaDataAssemblyImport Interface</span></span>](imetadataassemblyimport-interface.md)
- [<span data-ttu-id="d726a-133">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="d726a-133">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="d726a-134">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="d726a-134">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
- [<span data-ttu-id="d726a-135">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="d726a-135">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="d726a-136">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="d726a-136">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
