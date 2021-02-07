---
description: 了解详细信息： ValidatorFlags 枚举
title: ValidatorFlags 枚举
ms.date: 03/30/2017
api_name:
- ValidatorFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ValidatorFlags
helpviewer_keywords:
- ValidatorFlags enumeration [.NET Framework hosting]
ms.assetid: a3f5c266-3fcc-4ad1-aaf5-4cdbe26304ad
topic_type:
- apiref
ms.openlocfilehash: 473b0eef2851126256e1ea6b6d2b82be32e03e1c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99679116"
---
# <a name="validatorflags-enumeration"></a><span data-ttu-id="d9a99-103">ValidatorFlags 枚举</span><span class="sxs-lookup"><span data-stu-id="d9a99-103">ValidatorFlags Enumeration</span></span>

<span data-ttu-id="d9a99-104">包含一些值，这些值指示应在调用 [ICLRValidator：： Validate](iclrvalidator-validate-method.md) 方法时执行的验证类型。</span><span class="sxs-lookup"><span data-stu-id="d9a99-104">Contains values that indicate the type of validation that should be performed in a call to the [ICLRValidator::Validate](iclrvalidator-validate-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d9a99-105">语法</span><span class="sxs-lookup"><span data-stu-id="d9a99-105">Syntax</span></span>  
  
```cpp  
enum ValidatorFlags {  
    VALIDATOR_EXTRA_VERBOSE =       0x00000001,  
    VALIDATOR_SHOW_SOURCE_LINES =   0x00000002,  
    VALIDATOR_CHECK_ILONLY =        0x00000004,  
    VALIDATOR_CHECK_PEFORMAT_ONLY = 0x00000008,  
    VALIDATOR_NOCHECK_PEFORMAT =    0x00000010,  
};  
```  
  
## <a name="members"></a><span data-ttu-id="d9a99-106">成员</span><span class="sxs-lookup"><span data-stu-id="d9a99-106">Members</span></span>  
  
|<span data-ttu-id="d9a99-107">成员</span><span class="sxs-lookup"><span data-stu-id="d9a99-107">Member</span></span>|<span data-ttu-id="d9a99-108">说明</span><span class="sxs-lookup"><span data-stu-id="d9a99-108">Description</span></span>|  
|------------|-----------------|  
|`VALIDATOR_CHECK_ILONLY`|<span data-ttu-id="d9a99-109">指定应只验证可执行文件中的 Microsoft 中间语言 (MSIL) 。</span><span class="sxs-lookup"><span data-stu-id="d9a99-109">Specifies that only the Microsoft intermediate language (MSIL) in the executable file should be validated.</span></span>|  
|`VALIDATOR_CHECK_PEFORMAT_ONLY`|<span data-ttu-id="d9a99-110">指定只能验证可执行文件的格式。</span><span class="sxs-lookup"><span data-stu-id="d9a99-110">Specifies that only the format of the executable file should be validated.</span></span>|  
|`VALIDATOR_EXTRA_VERBOSE`|<span data-ttu-id="d9a99-111">指定应执行和报告的所有类型的验证。</span><span class="sxs-lookup"><span data-stu-id="d9a99-111">Specifies that all types of validation should be performed and reported on.</span></span>|  
|`VALIDATOR_NOCHECK_PEFORMAT`|<span data-ttu-id="d9a99-112">指定不应验证可执行文件的格式。</span><span class="sxs-lookup"><span data-stu-id="d9a99-112">Specifies that the format of the executable file should not be validated.</span></span>|  
|`VALIDATOR_SHOW_SOURCE_LINES`|<span data-ttu-id="d9a99-113">指定验证错误消息应包含引发验证错误的源代码行。</span><span class="sxs-lookup"><span data-stu-id="d9a99-113">Specifies that validation error messages should include the lines of source code that raise validation errors.</span></span> <span data-ttu-id="d9a99-114">此字段值在 .NET Framework 版本2.0 中无效。</span><span class="sxs-lookup"><span data-stu-id="d9a99-114">This field value is not valid in the .NET Framework version 2.0.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d9a99-115">要求</span><span class="sxs-lookup"><span data-stu-id="d9a99-115">Requirements</span></span>  

 <span data-ttu-id="d9a99-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d9a99-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d9a99-117">**标头：** IValidator，IValidator</span><span class="sxs-lookup"><span data-stu-id="d9a99-117">**Header:** IValidator.idl, IValidator.h</span></span>  
  
 <span data-ttu-id="d9a99-118">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d9a99-118">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d9a99-119">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d9a99-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d9a99-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="d9a99-120">See also</span></span>

- [<span data-ttu-id="d9a99-121">ICLRErrorReportingManager 接口</span><span class="sxs-lookup"><span data-stu-id="d9a99-121">ICLRErrorReportingManager Interface</span></span>](iclrerrorreportingmanager-interface.md)
- [<span data-ttu-id="d9a99-122">承载枚举</span><span class="sxs-lookup"><span data-stu-id="d9a99-122">Hosting Enumerations</span></span>](hosting-enumerations.md)
