---
description: 了解详细信息： MustUnderstandBehavior
title: MustUnderstandBehavior
ms.date: 03/30/2017
ms.assetid: 911ed04a-c4b8-4c72-a5c3-fc7b4e3b4348
ms.openlocfilehash: 173548f2f3346a79bf7f53c90384db94a638a366
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803121"
---
# <a name="mustunderstandbehavior"></a><span data-ttu-id="a90d9-103">MustUnderstandBehavior</span><span class="sxs-lookup"><span data-stu-id="a90d9-103">MustUnderstandBehavior</span></span>

<span data-ttu-id="a90d9-104">MustUnderstandBehavior</span><span class="sxs-lookup"><span data-stu-id="a90d9-104">MustUnderstandBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a90d9-105">语法</span><span class="sxs-lookup"><span data-stu-id="a90d9-105">Syntax</span></span>  
  
```csharp
class MustUnderstandBehavior : Behavior  
{  
  boolean ValidateMustUnderstand;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="a90d9-106">方法</span><span class="sxs-lookup"><span data-stu-id="a90d9-106">Methods</span></span>  

 <span data-ttu-id="a90d9-107">MustUnderstandBehavior 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="a90d9-107">The MustUnderstandBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="a90d9-108">属性</span><span class="sxs-lookup"><span data-stu-id="a90d9-108">Properties</span></span>  

 <span data-ttu-id="a90d9-109">MustUnderstandBehavior 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="a90d9-109">The MustUnderstandBehavior class has the following property:</span></span>  
  
### <a name="validatemustunderstand"></a><span data-ttu-id="a90d9-110">ValidateMustUnderstand</span><span class="sxs-lookup"><span data-stu-id="a90d9-110">ValidateMustUnderstand</span></span>  

 <span data-ttu-id="a90d9-111">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="a90d9-111">Data type: boolean</span></span>  
  
 <span data-ttu-id="a90d9-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="a90d9-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="a90d9-113">如果为 `true`，则所有具有 `MustUnderstand` 属性的未处理 SOAP 标头将导致引发异常的行为。</span><span class="sxs-lookup"><span data-stu-id="a90d9-113">When `true`, all SOAP headers with the `MustUnderstand` attribute that are not handled cause the behavior to throw an exception.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a90d9-114">要求</span><span class="sxs-lookup"><span data-stu-id="a90d9-114">Requirements</span></span>  
  
|<span data-ttu-id="a90d9-115">MOF</span><span class="sxs-lookup"><span data-stu-id="a90d9-115">MOF</span></span>|<span data-ttu-id="a90d9-116">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="a90d9-116">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="a90d9-117">命名空间</span><span class="sxs-lookup"><span data-stu-id="a90d9-117">Namespace</span></span>|<span data-ttu-id="a90d9-118">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="a90d9-118">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a90d9-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="a90d9-119">See also</span></span>

- <xref:System.ServiceModel.Description.MustUnderstandBehavior>
