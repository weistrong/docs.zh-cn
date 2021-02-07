---
description: 了解详细信息： IValidator：： Validate 方法
title: IValidator::Validate 方法
ms.date: 03/30/2017
api_name:
- IValidator.Validate
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- Validate
helpviewer_keywords:
- IValidator::Validate method [.NET Framework hosting]
- Validate method, IValidator interface [.NET Framework hosting]
ms.assetid: 7d68666a-fb73-4455-bebd-908d49a16abc
topic_type:
- apiref
ms.openlocfilehash: 6df70274a788b949686fe2509b525c5a8b04089c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99680013"
---
# <a name="ivalidatorvalidate-method"></a><span data-ttu-id="6405a-103">IValidator::Validate 方法</span><span class="sxs-lookup"><span data-stu-id="6405a-103">IValidator::Validate Method</span></span>

<span data-ttu-id="6405a-104"> (PE) 或 Microsoft 中间语言 (MSIL) 文件来验证指定的可移植可执行文件。</span><span class="sxs-lookup"><span data-stu-id="6405a-104">Validates the specified portable executable (PE) or Microsoft intermediate language (MSIL) file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6405a-105">语法</span><span class="sxs-lookup"><span data-stu-id="6405a-105">Syntax</span></span>  
  
```cpp  
HRESULT Validate (  
    [in] IVEHandler            *veh,  
    [in] IUnknown              *pAppDomain,  
    [in] unsigned long          ulFlags,  
    [in] unsigned long          ulMaxError,  
    [in] unsigned long          token,  
    [in] LPWSTR                 fileName,  
    [in, size_is(ulSize)] BYTE *pe,  
    [in] unsigned long          ulSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6405a-106">参数</span><span class="sxs-lookup"><span data-stu-id="6405a-106">Parameters</span></span>  

 `veh`  
 <span data-ttu-id="6405a-107">中指向 `IVEHandler` 处理验证错误的实例的指针。</span><span class="sxs-lookup"><span data-stu-id="6405a-107">[in] A pointer to an `IVEHandler` instance that handles validation errors.</span></span>  
  
 `pAppDomain`  
 <span data-ttu-id="6405a-108">中一个指针，指向要在其中加载文件的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="6405a-108">[in] A pointer to the application domain in which the file is loaded.</span></span>  
  
 `ulFlags`  
 <span data-ttu-id="6405a-109">中 [ValidatorFlags](validatorflags-enumeration.md) 值的按位组合，指示应执行的验证。</span><span class="sxs-lookup"><span data-stu-id="6405a-109">[in] A bitwise combination of [ValidatorFlags](validatorflags-enumeration.md) values, indicating the validations that should be performed.</span></span>  
  
 `ulMaxError`  
 <span data-ttu-id="6405a-110">中在退出验证之前允许的最大错误数。</span><span class="sxs-lookup"><span data-stu-id="6405a-110">[in] The maximum number of errors to allow before exiting the validation.</span></span>  
  
 `token`  
 <span data-ttu-id="6405a-111">中不使用。</span><span class="sxs-lookup"><span data-stu-id="6405a-111">[in] Not used.</span></span>  
  
 `fileName`  
 <span data-ttu-id="6405a-112">中一个字符串，指定要验证的文件的名称。</span><span class="sxs-lookup"><span data-stu-id="6405a-112">[in] A string that specifies the name of the file to be validated.</span></span>  
  
 `pe`  
 <span data-ttu-id="6405a-113">中指向存储文件的内存缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="6405a-113">[in] A pointer to the memory buffer in which the file is stored.</span></span>  
  
 `ulSize`  
 <span data-ttu-id="6405a-114">中要验证的文件的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="6405a-114">[in] The size, in bytes, of the file to be validated.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6405a-115">要求</span><span class="sxs-lookup"><span data-stu-id="6405a-115">Requirements</span></span>  

 <span data-ttu-id="6405a-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6405a-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6405a-117">**标头：** IValidator，IValidator</span><span class="sxs-lookup"><span data-stu-id="6405a-117">**Header:** IValidator.idl, IValidator.h</span></span>  
  
 <span data-ttu-id="6405a-118">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6405a-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6405a-119">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6405a-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
