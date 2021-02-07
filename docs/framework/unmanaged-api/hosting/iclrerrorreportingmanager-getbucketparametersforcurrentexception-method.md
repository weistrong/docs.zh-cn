---
description: 了解详细信息： ICLRErrorReportingManager：： GetBucketParametersForCurrentException 方法
title: ICLRErrorReportingManager::GetBucketParametersForCurrentException 方法
ms.date: 03/30/2017
api_name:
- ICLRErrorReportingManager.GetBucketParametersForCurrentException
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRErrorReportingManager::GetBucketParametersForCurrentException
helpviewer_keywords:
- ICLRErrorReportingManager::GetBucketParametersForCurrentException method [.NET Framework hosting]
- GetBucketParametersForCurrentException method [.NET Framework hosting]
ms.assetid: a13ec8a6-8e18-4acb-8054-77f5b1a0e0b9
topic_type:
- apiref
ms.openlocfilehash: ba2b6cf1215e5d57f608a76a870b0a9c846ee8ac
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689399"
---
# <a name="iclrerrorreportingmanagergetbucketparametersforcurrentexception-method"></a><span data-ttu-id="8fca2-103">ICLRErrorReportingManager::GetBucketParametersForCurrentException 方法</span><span class="sxs-lookup"><span data-stu-id="8fca2-103">ICLRErrorReportingManager::GetBucketParametersForCurrentException Method</span></span>

<span data-ttu-id="8fca2-104">获取调用线程上的当前异常的 Watson 存储桶。</span><span class="sxs-lookup"><span data-stu-id="8fca2-104">Gets the Watson bucket for the current exception on the calling thread.</span></span>  
  
 <span data-ttu-id="8fca2-105">*存储桶* 是与相同代码缺陷相关的错误数据的集合。</span><span class="sxs-lookup"><span data-stu-id="8fca2-105">A *bucket* is a collection of error data that is related to the same code defect.</span></span> <span data-ttu-id="8fca2-106">*Watson* 指的是一组用于收集和分析与异常相关联的数据的技术。</span><span class="sxs-lookup"><span data-stu-id="8fca2-106">*Watson* refers to a set of technologies for collecting and analyzing data that is associated with an exception.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8fca2-107">语法</span><span class="sxs-lookup"><span data-stu-id="8fca2-107">Syntax</span></span>  
  
```cpp  
HRESULT GetBucketParametersForCurrentException(  
    [out] BucketParameters *pParams  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8fca2-108">参数</span><span class="sxs-lookup"><span data-stu-id="8fca2-108">Parameters</span></span>  

 `pParams`  
 <span data-ttu-id="8fca2-109">弄指向 [BucketParameters](bucketparameters-structure.md) 结构的指针，该结构包含异常的错误数据。</span><span class="sxs-lookup"><span data-stu-id="8fca2-109">[out] A pointer to a [BucketParameters](bucketparameters-structure.md) structure that contains error data for the exception.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8fca2-110">要求</span><span class="sxs-lookup"><span data-stu-id="8fca2-110">Requirements</span></span>  

 <span data-ttu-id="8fca2-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8fca2-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8fca2-112">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="8fca2-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8fca2-113">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8fca2-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8fca2-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8fca2-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8fca2-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="8fca2-115">See also</span></span>

- [<span data-ttu-id="8fca2-116">ICLRErrorReportingManager 接口</span><span class="sxs-lookup"><span data-stu-id="8fca2-116">ICLRErrorReportingManager Interface</span></span>](iclrerrorreportingmanager-interface.md)
