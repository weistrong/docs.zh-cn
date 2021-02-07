---
description: 了解详细信息： IAssemblyName：： Finalize 方法
title: IAssemblyName::Finalize 方法
ms.date: 03/30/2017
api_name:
- IAssemblyName.Finalize
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::Finalize
helpviewer_keywords:
- Finalize method [.NET Framework fusion]
- IAssemblyName::Finalize method [.NET Framework fusion]
ms.assetid: 610e792d-98ef-411f-90b0-5b9a3813f547
topic_type:
- apiref
ms.openlocfilehash: d6277fdbc15f6f907d5e758dac4a3670570d585d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760766"
---
# <a name="iassemblynamefinalize-method"></a><span data-ttu-id="5f228-103">IAssemblyName::Finalize 方法</span><span class="sxs-lookup"><span data-stu-id="5f228-103">IAssemblyName::Finalize Method</span></span>

<span data-ttu-id="5f228-104">允许此 [IAssemblyName](iassemblyname-interface.md) 对象在调用其析构函数之前释放资源并执行其他清理操作。</span><span class="sxs-lookup"><span data-stu-id="5f228-104">Allows this [IAssemblyName](iassemblyname-interface.md) object to release resources and perform other cleanup operations before its destructor is called.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5f228-105">语法</span><span class="sxs-lookup"><span data-stu-id="5f228-105">Syntax</span></span>  
  
```cpp  
HRESULT Finalize ();  
```  
  
## <a name="requirements"></a><span data-ttu-id="5f228-106">要求</span><span class="sxs-lookup"><span data-stu-id="5f228-106">Requirements</span></span>  

 <span data-ttu-id="5f228-107">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5f228-107">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5f228-108">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="5f228-108">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="5f228-109">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5f228-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5f228-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="5f228-110">See also</span></span>

- [<span data-ttu-id="5f228-111">IAssemblyName 接口</span><span class="sxs-lookup"><span data-stu-id="5f228-111">IAssemblyName Interface</span></span>](iassemblyname-interface.md)
