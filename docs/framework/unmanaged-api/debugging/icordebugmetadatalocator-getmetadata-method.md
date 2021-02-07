---
description: 了解详细信息： ICorDebugMetaDataLocator：： GetMetaData 方法
title: ICorDebugMetaDataLocator::GetMetaData 方法
ms.date: 03/30/2017
api_name:
- ICorDebugMetaDataLocator.GetMetaData
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugMetaDataLocator::GetMetaData
helpviewer_keywords:
- ICorDebugMetaDataLocator::GetMetaData method [.NET Framework debugging]
- GetMetaData method, ICorDebugMetaDataLocator interface [.NET Framework debugging]
ms.assetid: f9b0ff22-54db-45eb-9cc3-508000a3141d
topic_type:
- apiref
ms.openlocfilehash: 419a03e42a54057ab70e31a368e918612f3a85f6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99691674"
---
# <a name="icordebugmetadatalocatorgetmetadata-method"></a><span data-ttu-id="f6d27-103">ICorDebugMetaDataLocator::GetMetaData 方法</span><span class="sxs-lookup"><span data-stu-id="f6d27-103">ICorDebugMetaDataLocator::GetMetaData Method</span></span>

<span data-ttu-id="f6d27-104">要求调试器返回模块（完成该调试器请求的操作需要其元数据）的完整路径。</span><span class="sxs-lookup"><span data-stu-id="f6d27-104">Asks the debugger to return the full path to a module whose metadata is needed to complete an operation the debugger requested.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f6d27-105">语法</span><span class="sxs-lookup"><span data-stu-id="f6d27-105">Syntax</span></span>  
  
```cpp  
HRESULT GetMetaData(  
      [in] LPCWSTR wszImagePath,  
      [in] DWORD   dwImageTimeStamp,  
      [in] DWORD   dwImageSize,  
      [in] ULONG32 cchPathBuffer,  
      [out] ULONG32 * pcchPathBuffer,  
      [out, size_is(cchPathBuffer), length_is(*pcchPathBuffer)]  
               WCHAR wszPathBuffer[]  
      );  
```  
  
## <a name="parameters"></a><span data-ttu-id="f6d27-106">参数</span><span class="sxs-lookup"><span data-stu-id="f6d27-106">Parameters</span></span>  

 `wszImagePath`  
 <span data-ttu-id="f6d27-107">[in] 以 null 结尾的字符串，表示文件的完整路径。</span><span class="sxs-lookup"><span data-stu-id="f6d27-107">[in] A null-terminated string that represents the full path to the file.</span></span> <span data-ttu-id="f6d27-108">如果未提供完整路径，则文件的名称和扩展名 (*filename*。*扩展*) 。</span><span class="sxs-lookup"><span data-stu-id="f6d27-108">If the full path is not available, the name and extension of the file (*filename*.*extension*).</span></span>  
  
 `dwImageTimeStamp`  
 <span data-ttu-id="f6d27-109">[in] 来自图像 PE 文件头的时间戳。</span><span class="sxs-lookup"><span data-stu-id="f6d27-109">[in] The time stamp from the image's PE file headers.</span></span> <span data-ttu-id="f6d27-110">此参数可能用于符号服务器 ([SymSrv](/windows/desktop/debug/using-symsrv)) lookup。</span><span class="sxs-lookup"><span data-stu-id="f6d27-110">This parameter can potentially be used for a symbol server ([SymSrv](/windows/desktop/debug/using-symsrv)) lookup.</span></span>  
  
 `dwImageSize`  
 <span data-ttu-id="f6d27-111">[in] PE 文件头中的图像大小。</span><span class="sxs-lookup"><span data-stu-id="f6d27-111">[in] The image size from PE file headers.</span></span> <span data-ttu-id="f6d27-112">此参数可能可以用于 SymSrv 查找。</span><span class="sxs-lookup"><span data-stu-id="f6d27-112">This parameter can potentially be used for a SymSrv lookup.</span></span>  
  
 `cchPathBuffer`  
 <span data-ttu-id="f6d27-113">[in] `wszPathBuffer` 中的字符计数。</span><span class="sxs-lookup"><span data-stu-id="f6d27-113">[in] The character count in `wszPathBuffer`.</span></span>  
  
 `pcchPathBuffer`  
 <span data-ttu-id="f6d27-114">[out] 写入 `wszPathBuffer` 的 `WCHAR` 的计数。</span><span class="sxs-lookup"><span data-stu-id="f6d27-114">[out] The count of `WCHAR`s written to `wszPathBuffer`.</span></span>  
  
 <span data-ttu-id="f6d27-115">如果该方法返回 E_NOT_SUFFICIENT_BUFFER，则包含存储路径所需的 `WCHAR` 计数。</span><span class="sxs-lookup"><span data-stu-id="f6d27-115">If the method returns E_NOT_SUFFICIENT_BUFFER, contains the count of `WCHAR`s needed to store the path.</span></span>  
  
 `wszPathBuffer`  
 <span data-ttu-id="f6d27-116">[out] 指向一个缓冲区的指针，调试器会将包含请求的元数据的文件的完整路径复制到该缓冲区中。</span><span class="sxs-lookup"><span data-stu-id="f6d27-116">[out] Pointer to a buffer into which the debugger will copy the full path of the file that contains the requested metadata.</span></span>  
  
 <span data-ttu-id="f6d27-117">`ofReadOnly` [CorOpenFlags](../metadata/coropenflags-enumeration.md)枚举中的标志用于请求对此文件中元数据的只读访问。</span><span class="sxs-lookup"><span data-stu-id="f6d27-117">The `ofReadOnly` flag from the [CorOpenFlags](../metadata/coropenflags-enumeration.md) enumeration is used to request read-only access to the metadata in this file.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f6d27-118">返回值</span><span class="sxs-lookup"><span data-stu-id="f6d27-118">Return Value</span></span>  

 <span data-ttu-id="f6d27-119">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="f6d27-119">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span> <span data-ttu-id="f6d27-120">所有其他失败的 HRESULT 均指示文件不可检索。</span><span class="sxs-lookup"><span data-stu-id="f6d27-120">All other failure HRESULTs indicate that the file is not retrievable.</span></span>  
  
|<span data-ttu-id="f6d27-121">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f6d27-121">HRESULT</span></span>|<span data-ttu-id="f6d27-122">说明</span><span class="sxs-lookup"><span data-stu-id="f6d27-122">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f6d27-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="f6d27-123">S_OK</span></span>|<span data-ttu-id="f6d27-124">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="f6d27-124">The method completed successfully.</span></span> <span data-ttu-id="f6d27-125">`wszPathBuffer` 包含文件的完整路径，以 null 结尾。</span><span class="sxs-lookup"><span data-stu-id="f6d27-125">`wszPathBuffer` contains the full path to the file and is null-terminated.</span></span>|  
|<span data-ttu-id="f6d27-126">E_NOT_SUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="f6d27-126">E_NOT_SUFFICIENT_BUFFER</span></span>|<span data-ttu-id="f6d27-127">`wszPathBuffer` 的当前大小不足以容纳完整路径。</span><span class="sxs-lookup"><span data-stu-id="f6d27-127">The current size of `wszPathBuffer` is not sufficient to hold the full path.</span></span> <span data-ttu-id="f6d27-128">在这种情况下，`pcchPathBuffer` 包含所需的 `WCHAR` 计数（包括终止 null 字符），并且使用请求的缓冲区大小第二次调用 `GetMetaData`。</span><span class="sxs-lookup"><span data-stu-id="f6d27-128">In this case, `pcchPathBuffer` contains the needed count of `WCHAR`s, including the terminating null character, and `GetMetaData` is called a second time with the requested buffer size.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f6d27-129">备注</span><span class="sxs-lookup"><span data-stu-id="f6d27-129">Remarks</span></span>  

 <span data-ttu-id="f6d27-130">如果 `wszImagePath` 包含转储中模块的完整路径，则它从收集转储的计算机指定路径。</span><span class="sxs-lookup"><span data-stu-id="f6d27-130">If `wszImagePath` contains a full path for a module from a dump, it specifies the path from the computer where the dump was collected.</span></span> <span data-ttu-id="f6d27-131">文件可能不位于此位置，或者具有相同名称的不正确文件可能存储在该路径上。</span><span class="sxs-lookup"><span data-stu-id="f6d27-131">The file may not exist at this location, or an incorrect file with the same name may be stored on the path.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f6d27-132">要求</span><span class="sxs-lookup"><span data-stu-id="f6d27-132">Requirements</span></span>  

 <span data-ttu-id="f6d27-133">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f6d27-133">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f6d27-134">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f6d27-134">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f6d27-135">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f6d27-135">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f6d27-136">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f6d27-136">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f6d27-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="f6d27-137">See also</span></span>

- [<span data-ttu-id="f6d27-138">ICorDebugThread4 接口</span><span class="sxs-lookup"><span data-stu-id="f6d27-138">ICorDebugThread4 Interface</span></span>](icordebugthread4-interface.md)
- [<span data-ttu-id="f6d27-139">调试接口</span><span class="sxs-lookup"><span data-stu-id="f6d27-139">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="f6d27-140">调试</span><span class="sxs-lookup"><span data-stu-id="f6d27-140">Debugging</span></span>](index.md)
