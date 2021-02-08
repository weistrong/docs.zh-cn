---
description: 了解详细信息： GUID_ManagedName 属性
title: GUID_ManagedName 特性
ms.date: 03/30/2017
api_name:
- GUID_ManagedName
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GUID_ManagedName
helpviewer_keywords:
- GUID_ManagedName attribute
ms.assetid: 11e18095-e444-47bc-aff6-b887ac5dc01e
topic_type:
- apiref
ms.openlocfilehash: c139e8bdc00aa3b008a706de0c42cfbf8e3510c5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799988"
---
# <a name="guid_managedname-attribute"></a><span data-ttu-id="e2805-103">GUID_ManagedName 特性</span><span class="sxs-lookup"><span data-stu-id="e2805-103">GUID_ManagedName Attribute</span></span>

<span data-ttu-id="e2805-104">定义一个自定义接口特性，该特性指定组件对象模型 (COM) 库的托管命名空间名称。</span><span class="sxs-lookup"><span data-stu-id="e2805-104">Defines a custom interface attribute that specifies the managed namespace name for a component object model (COM) library.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e2805-105">语法</span><span class="sxs-lookup"><span data-stu-id="e2805-105">Syntax</span></span>  
  
```idl
[  
   custom(GUID_ManagedName, value)  
]  
```  
  
## <a name="parameters"></a><span data-ttu-id="e2805-106">参数</span><span class="sxs-lookup"><span data-stu-id="e2805-106">Parameters</span></span>  

 `value`  
 <span data-ttu-id="e2805-107">库的托管命名空间名称。</span><span class="sxs-lookup"><span data-stu-id="e2805-107">The managed namespace name for the library.</span></span>  
  
## <a name="definition"></a><span data-ttu-id="e2805-108">定义</span><span class="sxs-lookup"><span data-stu-id="e2805-108">Definition</span></span>  

 <span data-ttu-id="e2805-109">`GUID_ManagedName` 在 Cor 中定义，如下所示：</span><span class="sxs-lookup"><span data-stu-id="e2805-109">`GUID_ManagedName` is defined in Cor.h as follows:</span></span>  
  
```cpp
// {0F21F359-AB84-41e8-9A78-36D110E6D2F9}  
EXTERN_GUID(GUID_ManagedName, 0xf21f359, 0xab84, 0x41e8, 0x9a, 0x78, 0x36, 0xd1, 0x10, 0xe6, 0xd2, 0xf9);  
```  
  
## <a name="remarks"></a><span data-ttu-id="e2805-110">备注</span><span class="sxs-lookup"><span data-stu-id="e2805-110">Remarks</span></span>  

 <span data-ttu-id="e2805-111">自定义接口特性为类型库中的对象定义元数据。</span><span class="sxs-lookup"><span data-stu-id="e2805-111">A custom interface attribute defines metadata for an object in the type library.</span></span>  
  
 <span data-ttu-id="e2805-112">使用 <xref:System.Runtime.InteropServices.ComTypes.ITypeInfo2.GetCustData%2A?displayProperty=nameWithType> 或 <xref:System.Runtime.InteropServices.ComTypes.ITypeLib2.GetCustData%2A?displayProperty=nameWithType> 从属性中检索托管名称。</span><span class="sxs-lookup"><span data-stu-id="e2805-112">Use <xref:System.Runtime.InteropServices.ComTypes.ITypeInfo2.GetCustData%2A?displayProperty=nameWithType> or <xref:System.Runtime.InteropServices.ComTypes.ITypeLib2.GetCustData%2A?displayProperty=nameWithType> to retrieve the managed name from the attribute.</span></span>  
  
 <span data-ttu-id="e2805-113">有关详细信息，请参阅 Visual C++ 参考文档中的 [接口特性](/cpp/windows/attributes/interface-attributes) 。</span><span class="sxs-lookup"><span data-stu-id="e2805-113">For more information, see [Interface Attributes](/cpp/windows/attributes/interface-attributes) in the Visual C++ reference documentation.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e2805-114">示例</span><span class="sxs-lookup"><span data-stu-id="e2805-114">Example</span></span>  

 <span data-ttu-id="e2805-115">下面的示例演示了一个使用属性的库定义 `GUID_ManagedName` 。</span><span class="sxs-lookup"><span data-stu-id="e2805-115">The following example shows a library definition using the `GUID_ManagedName` attribute.</span></span>  
  
```idl
[  
   ...  
   custom(GUID_ManagedName, Microsoft.VisualStudio.CommandBars.dll")  
]  
library Microsoft_VisualStudio_CommandBars  
{  
   ...  
}  
```  
  
## <a name="requirements"></a><span data-ttu-id="e2805-116">要求</span><span class="sxs-lookup"><span data-stu-id="e2805-116">Requirements</span></span>  

 <span data-ttu-id="e2805-117">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="e2805-117">**Header:** Cor.h</span></span>
