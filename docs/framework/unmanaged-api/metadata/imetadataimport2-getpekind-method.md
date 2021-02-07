---
description: 了解详细信息： IMetaDataImport2：： GetPEKind 方法
title: IMetaDataImport2::GetPEKind 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.GetPEKind
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::GetPEKind
helpviewer_keywords:
- GetPEKind method [.NET Framework metadata]
- IMetaDataImport2::GetPEKind method [.NET Framework metadata]
ms.assetid: d91c3d89-8022-4a4c-a2a2-a8af2c387507
topic_type:
- apiref
ms.openlocfilehash: 3cd003f4b1a56f59b9e8c89bf1c4f8f2f8c7fea1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99688567"
---
# <a name="imetadataimport2getpekind-method"></a><span data-ttu-id="00642-103">IMetaDataImport2::GetPEKind 方法</span><span class="sxs-lookup"><span data-stu-id="00642-103">IMetaDataImport2::GetPEKind Method</span></span>

<span data-ttu-id="00642-104">获取一个值，该值标识可移植可执行文件中代码的性质 (PE) 文件（通常为 DLL 或 EXE 文件），该文件在当前的元数据范围内定义。</span><span class="sxs-lookup"><span data-stu-id="00642-104">Gets a value identifying the nature of the code in the portable executable (PE) file, typically a DLL or EXE file, that is defined in the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="00642-105">语法</span><span class="sxs-lookup"><span data-stu-id="00642-105">Syntax</span></span>  
  
```cpp  
HRESULT GetPEKind (  
   [out] DWORD *pdwPEKind,  
   [out] DWORD *pdwMachine  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="00642-106">参数</span><span class="sxs-lookup"><span data-stu-id="00642-106">Parameters</span></span>  

 `pdwPEKind`  
 <span data-ttu-id="00642-107">弄一个指针，指向描述 PE 文件的 [CorPEKind](corpekind-enumeration.md) 枚举的值。</span><span class="sxs-lookup"><span data-stu-id="00642-107">[out] A pointer to a value of the [CorPEKind](corpekind-enumeration.md) enumeration that describes the PE file.</span></span>  
  
 `pdwMachine`  
 <span data-ttu-id="00642-108">弄一个指针，指向用于标识计算机体系结构的值。</span><span class="sxs-lookup"><span data-stu-id="00642-108">[out] A pointer to a value that identifies the architecture of the machine.</span></span> <span data-ttu-id="00642-109">有关可能的值，请参阅下一节。</span><span class="sxs-lookup"><span data-stu-id="00642-109">See the next section for possible values.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="00642-110">备注</span><span class="sxs-lookup"><span data-stu-id="00642-110">Remarks</span></span>  

 <span data-ttu-id="00642-111">参数引用的值 `pdwMachine` 可以是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="00642-111">The value referenced by the `pdwMachine` parameter can be one of the following.</span></span>  
  
|<span data-ttu-id="00642-112">值</span><span class="sxs-lookup"><span data-stu-id="00642-112">Value</span></span>|<span data-ttu-id="00642-113">计算机体系结构</span><span class="sxs-lookup"><span data-stu-id="00642-113">Machine architecture</span></span>|  
|-----------|--------------------------|  
|<span data-ttu-id="00642-114">IMAGE_FILE_MACHINE_I386</span><span class="sxs-lookup"><span data-stu-id="00642-114">IMAGE_FILE_MACHINE_I386</span></span><br /><br /> <span data-ttu-id="00642-115">0x014C</span><span class="sxs-lookup"><span data-stu-id="00642-115">0x014C</span></span>|<span data-ttu-id="00642-116">x86</span><span class="sxs-lookup"><span data-stu-id="00642-116">x86</span></span>|  
|<span data-ttu-id="00642-117">IMAGE_FILE_MACHINE_IA64</span><span class="sxs-lookup"><span data-stu-id="00642-117">IMAGE_FILE_MACHINE_IA64</span></span><br /><br /> <span data-ttu-id="00642-118">0x0200</span><span class="sxs-lookup"><span data-stu-id="00642-118">0x0200</span></span>|<span data-ttu-id="00642-119">Intel IPF</span><span class="sxs-lookup"><span data-stu-id="00642-119">Intel IPF</span></span>|  
|<span data-ttu-id="00642-120">IMAGE_FILE_MACHINE_AMD64</span><span class="sxs-lookup"><span data-stu-id="00642-120">IMAGE_FILE_MACHINE_AMD64</span></span><br /><br /> <span data-ttu-id="00642-121">0x8664</span><span class="sxs-lookup"><span data-stu-id="00642-121">0x8664</span></span>|<span data-ttu-id="00642-122">X64</span><span class="sxs-lookup"><span data-stu-id="00642-122">x64</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="00642-123">要求</span><span class="sxs-lookup"><span data-stu-id="00642-123">Requirements</span></span>  

 <span data-ttu-id="00642-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="00642-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="00642-125">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="00642-125">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="00642-126">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="00642-126">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="00642-127">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="00642-127">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="00642-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="00642-128">See also</span></span>

- [<span data-ttu-id="00642-129">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="00642-129">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
- [<span data-ttu-id="00642-130">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="00642-130">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="00642-131">CorPEKind 枚举</span><span class="sxs-lookup"><span data-stu-id="00642-131">CorPEKind Enumeration</span></span>](corpekind-enumeration.md)
