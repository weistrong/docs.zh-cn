---
description: 了解详细信息： ICLRMetadataLocator：： GetMetadata 方法
title: ICLRMetadataLocator::GetMetadata 方法
ms.date: 03/30/2017
api_name:
- ICLRMetadataLocator.GetMetadata
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRMetadataLocator::GetMetadata
helpviewer_keywords:
- GetMetadata method, ICLRMetadataLocator interface [.NET Framework debugging]
- ICLRMetadataLocator::GetMetadata method [.NET Framework debugging]
ms.assetid: 704a8893-ac56-43b4-90ea-715f38ccb40e
topic_type:
- apiref
ms.openlocfilehash: 4a7e8b906b66c4295dd24800d260790526114701
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772598"
---
# <a name="iclrmetadatalocatorgetmetadata-method"></a><span data-ttu-id="5e559-103">ICLRMetadataLocator::GetMetadata 方法</span><span class="sxs-lookup"><span data-stu-id="5e559-103">ICLRMetadataLocator::GetMetadata Method</span></span>

<span data-ttu-id="5e559-104">由公共语言运行时调用 (CLR) 数据访问服务检索图像的元数据。</span><span class="sxs-lookup"><span data-stu-id="5e559-104">Called by the common language runtime (CLR) data access services to retrieve the metadata of an image.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5e559-105">语法</span><span class="sxs-lookup"><span data-stu-id="5e559-105">Syntax</span></span>  
  
```cpp  
HRESULT GetMetadata(  
    [in]  LPCWSTR         imagePath,  
    [in]  ULONG32         imageTimestamp,  
    [in]  ULONG32         imageSize,  
    [in]  GUID*           mvid,  
    [in]  ULONG32         mdRva,  
    [in]  ULONG32         flags,  
    [in]  ULONG32         bufferSize,  
    [out, size_is(bufferSize), length_is(*dataSize)]  
          BYTE*           buffer,  
    [out] ULONG32*        dataSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5e559-106">参数</span><span class="sxs-lookup"><span data-stu-id="5e559-106">Parameters</span></span>  

 `imagePath`  
 <span data-ttu-id="5e559-107">中一个字符串，指定图像文件的路径。</span><span class="sxs-lookup"><span data-stu-id="5e559-107">[in] A string that specifies the path of the image file.</span></span>  
  
 `imageTimestamp`  
 <span data-ttu-id="5e559-108">中图像文件的时间戳。</span><span class="sxs-lookup"><span data-stu-id="5e559-108">[in] The time stamp of the image file.</span></span>  
  
 `imageSize`  
 <span data-ttu-id="5e559-109">中图像文件的大小。</span><span class="sxs-lookup"><span data-stu-id="5e559-109">[in] The size of the image file.</span></span>  
  
 `mvid`  
 <span data-ttu-id="5e559-110">中图像的全局唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="5e559-110">[in] The globally unique identifier of the image.</span></span>  
  
 `mdRva`  
 <span data-ttu-id="5e559-111">中元数据 (RVA) 的相对虚拟地址。</span><span class="sxs-lookup"><span data-stu-id="5e559-111">[in] The relative virtual address (RVA) of the metadata.</span></span> <span data-ttu-id="5e559-112">地址相对于映像基址。</span><span class="sxs-lookup"><span data-stu-id="5e559-112">The address is relative to the image base address.</span></span>  
  
 `flags`  
 <span data-ttu-id="5e559-113">中保留供将来使用。</span><span class="sxs-lookup"><span data-stu-id="5e559-113">[in] Reserved for future use.</span></span>  
  
 `bufferSize`  
 <span data-ttu-id="5e559-114">中要在其中放置元数据的缓冲区的大小。</span><span class="sxs-lookup"><span data-stu-id="5e559-114">[in] The size of the buffer in which to place the metadata.</span></span>  
  
 `buffer`  
 <span data-ttu-id="5e559-115">弄要在其中放置元数据的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="5e559-115">[out] The buffer in which to place the metadata.</span></span>  
  
 `dataSize`  
 <span data-ttu-id="5e559-116">弄返回的元数据的大小。</span><span class="sxs-lookup"><span data-stu-id="5e559-116">[out] The size of the metadata that is returned.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5e559-117">备注</span><span class="sxs-lookup"><span data-stu-id="5e559-117">Remarks</span></span>  

 <span data-ttu-id="5e559-118">此方法由调试应用程序的编写器实现。</span><span class="sxs-lookup"><span data-stu-id="5e559-118">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5e559-119">要求</span><span class="sxs-lookup"><span data-stu-id="5e559-119">Requirements</span></span>  

 <span data-ttu-id="5e559-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5e559-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5e559-121">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="5e559-121">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="5e559-122">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5e559-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5e559-123">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5e559-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5e559-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="5e559-124">See also</span></span>

- [<span data-ttu-id="5e559-125">ICLRMetadataLocator 接口</span><span class="sxs-lookup"><span data-stu-id="5e559-125">ICLRMetadataLocator Interface</span></span>](iclrmetadatalocator-interface.md)
