---
description: 了解详细信息： CreateHistoryReader 函数
title: CreateHistoryReader 函数
ms.date: 03/30/2017
api_name:
- CreateHistoryReader
api_location:
- fusion.dll
api_type:
- DLLExport
f1_keywords:
- CreateHistoryReader
helpviewer_keywords:
- CreateHistoryReader function [.NET Framework fusion]
ms.assetid: 66a89acf-8c32-44c0-8787-960c99c7b3ec
topic_type:
- apiref
ms.openlocfilehash: 0943f3d0f3322d34ed92c0a96b909e4d63ec5e7f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761117"
---
# <a name="createhistoryreader-function"></a><span data-ttu-id="1118d-103">CreateHistoryReader 函数</span><span class="sxs-lookup"><span data-stu-id="1118d-103">CreateHistoryReader Function</span></span>

<span data-ttu-id="1118d-104">为指定的文件创建历史记录读取器。</span><span class="sxs-lookup"><span data-stu-id="1118d-104">Creates a history reader for the specified file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1118d-105">语法</span><span class="sxs-lookup"><span data-stu-id="1118d-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateHistoryReader (  
    [in]  LPCWSTR        wzFilePath,  
    [out] IHistoryReader **ppHistoryReader  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="1118d-106">参数</span><span class="sxs-lookup"><span data-stu-id="1118d-106">Parameters</span></span>  

 `wzFilePath`  
 <span data-ttu-id="1118d-107">中文件路径。</span><span class="sxs-lookup"><span data-stu-id="1118d-107">[in] The file path.</span></span>  
  
 `ppHistoryReader`  
 <span data-ttu-id="1118d-108">弄成功完成后，包含指向历史记录读取器的指针。</span><span class="sxs-lookup"><span data-stu-id="1118d-108">[out] On successful completion, contains a pointer to the history reader.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1118d-109">返回值</span><span class="sxs-lookup"><span data-stu-id="1118d-109">Return Value</span></span>  

 <span data-ttu-id="1118d-110">此方法返回 Winerror.h 中定义的标准 COM 错误代码，以及下表中描述的值。</span><span class="sxs-lookup"><span data-stu-id="1118d-110">This method returns standard COM error codes as defined in WinError.h, in addition to the values described in the following table.</span></span>  
  
|<span data-ttu-id="1118d-111">返回代码</span><span class="sxs-lookup"><span data-stu-id="1118d-111">Return code</span></span>|<span data-ttu-id="1118d-112">说明</span><span class="sxs-lookup"><span data-stu-id="1118d-112">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="1118d-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="1118d-113">S_OK</span></span>|<span data-ttu-id="1118d-114">指示该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="1118d-114">Indicates that the method completed successfully.</span></span>|  
|<span data-ttu-id="1118d-115">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="1118d-115">E_INVALIDARG</span></span>|<span data-ttu-id="1118d-116">指示 `wzFilePath` 或 `ppHistoryReader` 设置为空引用。</span><span class="sxs-lookup"><span data-stu-id="1118d-116">Indicates that `wzFilePath` or `ppHistoryReader` are set to a null reference.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1118d-117">要求</span><span class="sxs-lookup"><span data-stu-id="1118d-117">Requirements</span></span>  

 <span data-ttu-id="1118d-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1118d-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1118d-119">**库：** Fusion.dll</span><span class="sxs-lookup"><span data-stu-id="1118d-119">**Library:** Fusion.dll</span></span>  
  
 <span data-ttu-id="1118d-120">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1118d-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1118d-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="1118d-121">See also</span></span>

- [<span data-ttu-id="1118d-122">合成全局静态函数</span><span class="sxs-lookup"><span data-stu-id="1118d-122">Fusion Global Static Functions</span></span>](fusion-global-static-functions.md)
