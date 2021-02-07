---
description: 了解详细信息： GetFileDef 方法
title: GetFileDef 方法
ms.date: 03/30/2017
api_name:
- IALink2.GetFileDef
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetFileDef
helpviewer_keywords:
- GetFileDef method
ms.assetid: 4e3fbe6c-b82a-4181-ab17-7faa1263f5b3
topic_type:
- apiref
ms.openlocfilehash: 5d44336e686ca565f468fb95ce5290ee41d5e16e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99718442"
---
# <a name="getfiledef-method"></a><span data-ttu-id="8b2a8-103">GetFileDef 方法</span><span class="sxs-lookup"><span data-stu-id="8b2a8-103">GetFileDef Method</span></span>

<span data-ttu-id="8b2a8-104">检索元数据 (中使用的实际 FileDef 标记，而不是由 ALink) 分配的令牌。</span><span class="sxs-lookup"><span data-stu-id="8b2a8-104">Retrieves the actual FileDef token used in metadata (as opposed to the token assigned by ALink).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8b2a8-105">语法</span><span class="sxs-lookup"><span data-stu-id="8b2a8-105">Syntax</span></span>  
  
```cpp  
HRESULT GetFileDef(  
    mdAssembly AssemblyID,  
    mdFile TargetFile,  
    mdFile* pScope  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="8b2a8-106">参数</span><span class="sxs-lookup"><span data-stu-id="8b2a8-106">Parameters</span></span>  

 `AssemblyID`  
 <span data-ttu-id="8b2a8-107">程序集的 ID。</span><span class="sxs-lookup"><span data-stu-id="8b2a8-107">ID of the assembly.</span></span>  
  
 `TargetFile`  
 <span data-ttu-id="8b2a8-108">从 AddFile 方法或 AddImport 方法检索到的已添加文件的标记。</span><span class="sxs-lookup"><span data-stu-id="8b2a8-108">Token of the added file as retrieved from AddFile Method or AddImport Method.</span></span>  
  
 `pScope`  
 <span data-ttu-id="8b2a8-109">接收 FileDef 标记。</span><span class="sxs-lookup"><span data-stu-id="8b2a8-109">Receives the FileDef token.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8b2a8-110">返回值</span><span class="sxs-lookup"><span data-stu-id="8b2a8-110">Return Value</span></span>  

 <span data-ttu-id="8b2a8-111">如果方法成功，则返回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="8b2a8-111">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8b2a8-112">要求</span><span class="sxs-lookup"><span data-stu-id="8b2a8-112">Requirements</span></span>  

 <span data-ttu-id="8b2a8-113">需要 alink</span><span class="sxs-lookup"><span data-stu-id="8b2a8-113">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8b2a8-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="8b2a8-114">See also</span></span>

- [<span data-ttu-id="8b2a8-115">IALink2 接口</span><span class="sxs-lookup"><span data-stu-id="8b2a8-115">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="8b2a8-116">IALink 接口</span><span class="sxs-lookup"><span data-stu-id="8b2a8-116">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="8b2a8-117">ALink API</span><span class="sxs-lookup"><span data-stu-id="8b2a8-117">ALink API</span></span>](index.md)
