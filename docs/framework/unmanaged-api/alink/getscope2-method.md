---
description: 了解详细信息： GetScope2 方法
title: GetScope2 方法
ms.date: 03/30/2017
api_name:
- IALink2.GetScope2
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetScope2
helpviewer_keywords:
- GetScope2 method
ms.assetid: 49435665-6f5a-4acd-9034-8c9244a04a63
topic_type:
- apiref
ms.openlocfilehash: 9a68f02a638b58e7a70207d8610607bf24b2b96b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99718338"
---
# <a name="getscope2-method"></a><span data-ttu-id="f6699-103">GetScope2 方法</span><span class="sxs-lookup"><span data-stu-id="f6699-103">GetScope2 Method</span></span>

<span data-ttu-id="f6699-104">获取导入范围。</span><span class="sxs-lookup"><span data-stu-id="f6699-104">Gets an import scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f6699-105">语法</span><span class="sxs-lookup"><span data-stu-id="f6699-105">Syntax</span></span>  
  
```cpp  
HRESULT GetScope2(  
    mdAssembly AssemblyID,  
    mdToken FileToken,  
    DWORD dwScope,  
    IMetaDataImport2** ppImportScope  
) PURE;
```  
  
## <a name="parameters"></a><span data-ttu-id="f6699-106">参数</span><span class="sxs-lookup"><span data-stu-id="f6699-106">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="f6699-107">目标程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="f6699-107">ID of target assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="f6699-108">要从中导入的文件的 ID。</span><span class="sxs-lookup"><span data-stu-id="f6699-108">ID of file from which to import.</span></span>  
  
 `dwScope`  
 <span data-ttu-id="f6699-109">要导入的从零开始的范围。</span><span class="sxs-lookup"><span data-stu-id="f6699-109">Zero-based scope to import.</span></span>  
  
 `ppImportScope`  
 <span data-ttu-id="f6699-110">接收指向指定范围的 [IMetaDataImport2 接口](../metadata/imetadataimport2-interface.md) 接口的指针。</span><span class="sxs-lookup"><span data-stu-id="f6699-110">Receives pointer to [IMetaDataImport2 Interface](../metadata/imetadataimport2-interface.md) interface for indicated scope.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f6699-111">返回值</span><span class="sxs-lookup"><span data-stu-id="f6699-111">Return Value</span></span>  

 <span data-ttu-id="f6699-112">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="f6699-112">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f6699-113">要求</span><span class="sxs-lookup"><span data-stu-id="f6699-113">Requirements</span></span>  

 <span data-ttu-id="f6699-114">需要 alink。</span><span class="sxs-lookup"><span data-stu-id="f6699-114">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f6699-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="f6699-115">See also</span></span>

- [<span data-ttu-id="f6699-116">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="f6699-116">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="f6699-117">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="f6699-117">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="f6699-118">ALink API</span><span class="sxs-lookup"><span data-stu-id="f6699-118">ALink API</span></span>](index.md)
