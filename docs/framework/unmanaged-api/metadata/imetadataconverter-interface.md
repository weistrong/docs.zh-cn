---
description: 了解详细信息： IMetaDataConverter 接口
title: IMetaDataConverter 接口
ms.date: 03/30/2017
api_name:
- IMetaDataConverter
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataConverter
helpviewer_keywords:
- IMetaDataConverter interface [.NET Framework metadata]
ms.assetid: 9caea662-0167-4267-b14a-2fa42c3be4ea
topic_type:
- apiref
ms.openlocfilehash: 6ed84083bad924e760c576afe485bd7ccad012cf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789250"
---
# <a name="imetadataconverter-interface"></a><span data-ttu-id="886fc-103">IMetaDataConverter 接口</span><span class="sxs-lookup"><span data-stu-id="886fc-103">IMetaDataConverter Interface</span></span>

<span data-ttu-id="886fc-104">提供将类型库映射到其元数据签名并进行相互转换的方法。</span><span class="sxs-lookup"><span data-stu-id="886fc-104">Provides methods to map type libraries to their metadata signatures, and to convert from one to the other.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="886fc-105">方法</span><span class="sxs-lookup"><span data-stu-id="886fc-105">Methods</span></span>  
  
|<span data-ttu-id="886fc-106">方法</span><span class="sxs-lookup"><span data-stu-id="886fc-106">Method</span></span>|<span data-ttu-id="886fc-107">说明</span><span class="sxs-lookup"><span data-stu-id="886fc-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="886fc-108">GetMetaDataFromTypeInfo 方法</span><span class="sxs-lookup"><span data-stu-id="886fc-108">GetMetaDataFromTypeInfo Method</span></span>](imetadataconverter-getmetadatafromtypeinfo-method.md)|<span data-ttu-id="886fc-109">获取一个指针，该指针指向表示指定实例引用的类型库的元数据签名的 [IMetaDataImport](imetadataimport-interface.md) 实例 `ITypeInfo` 。</span><span class="sxs-lookup"><span data-stu-id="886fc-109">Gets a pointer to an [IMetaDataImport](imetadataimport-interface.md) instance that represents the metadata signature for the type library referenced by the specified `ITypeInfo` instance.</span></span>|  
|[<span data-ttu-id="886fc-110">GetMetaDataFromTypeLib 方法</span><span class="sxs-lookup"><span data-stu-id="886fc-110">GetMetaDataFromTypeLib Method</span></span>](imetadataconverter-getmetadatafromtypelib-method.md)|<span data-ttu-id="886fc-111">获取一个指针，该指针指向 `IMetaDataImport` 表示指定实例所表示的类型库的元数据签名的实例 `ITypeLib` 。</span><span class="sxs-lookup"><span data-stu-id="886fc-111">Gets a pointer to an `IMetaDataImport` instance that represents the metadata signature for the type library represented by the specified `ITypeLib` instance.</span></span>|  
|[<span data-ttu-id="886fc-112">GetTypeLibFromMetaData 方法</span><span class="sxs-lookup"><span data-stu-id="886fc-112">GetTypeLibFromMetaData Method</span></span>](imetadataconverter-gettypelibfrommetadata-method.md)|<span data-ttu-id="886fc-113">获取一个指向实例的指针，该 `ITypeLib` 对象表示具有指定模块和库名称的类型库。</span><span class="sxs-lookup"><span data-stu-id="886fc-113">Gets a pointer to an `ITypeLib` instance that represents the type library that has the specified module and library names.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="886fc-114">要求</span><span class="sxs-lookup"><span data-stu-id="886fc-114">Requirements</span></span>  

 <span data-ttu-id="886fc-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="886fc-115">**Platform:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="886fc-116">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="886fc-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="886fc-117">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="886fc-117">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="886fc-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="886fc-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="886fc-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="886fc-119">See also</span></span>

- [<span data-ttu-id="886fc-120">元数据接口</span><span class="sxs-lookup"><span data-stu-id="886fc-120">Metadata Interfaces</span></span>](metadata-interfaces.md)
- [<span data-ttu-id="886fc-121">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="886fc-121">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
