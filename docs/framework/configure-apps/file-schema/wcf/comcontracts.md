---
description: 了解详细信息： <comContracts>
title: <comContracts>
ms.date: 03/30/2017
ms.assetid: 42e74148-223d-4888-a8ed-1d928527eb09
ms.openlocfilehash: 263210b4499274fe009a6b1b1e46c1f09dd007ab
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638647"
---
# \<comContracts>

<span data-ttu-id="7aed7-102">`comContracts` 配置节所包含的元素允许指定 COM+ 集成服务协定的各个属性。</span><span class="sxs-lookup"><span data-stu-id="7aed7-102">The `comContracts` configuration section contains elements that allow you to specify various properties of a COM+ integration service contract.</span></span>  
  
## <a name="specifying-namespace-and-contract"></a><span data-ttu-id="7aed7-103">指定命名空间和协定</span><span class="sxs-lookup"><span data-stu-id="7aed7-103">Specifying Namespace and Contract</span></span>  

 <span data-ttu-id="7aed7-104">COM + 集成服务协定当前仅限于 `http://tempuri.org` 命名空间，协定名称派生自支持的 COM 接口。</span><span class="sxs-lookup"><span data-stu-id="7aed7-104">COM+ integration service contracts are currently restricted to the `http://tempuri.org` namespace, and contract name is derived from the supporting COM interface.</span></span> <span data-ttu-id="7aed7-105">但是，可以使用配置文件中的 `comContracts` 节来指定替代服务协定。</span><span class="sxs-lookup"><span data-stu-id="7aed7-105">You can, however, specify alternatives by using the `comContracts` section in the configuration file.</span></span>  
  
 <span data-ttu-id="7aed7-106">例如，可以使用以下配置来指定服务协定的命名空间和协定名称，也可以指定某个选项以在会话绑定上强制使用。</span><span class="sxs-lookup"><span data-stu-id="7aed7-106">For example, you can use the following configuration to specify the namespace and contract name of the service contract, as well as an option to enforce usage on sessionful bindings.</span></span>  
  
```xml  
<comContracts>
  <comContract contract="{5163B1E7-F0CF-4B6A-9A02-4AB654F34284}"
               namespace="http://tempuri.org/5163B1E7-F0CF-4B6A-9A02-4AB654F34284"
               name="_Broker"
               requireSession="true">
  </comContract>
</comContracts>
```  
  
 <span data-ttu-id="7aed7-107">在初始化服务时，指定的命名空间和协定名称将应用到生成的服务说明。</span><span class="sxs-lookup"><span data-stu-id="7aed7-107">When the service is initialized, the specified namespaces and contract names are applied to the generated service descriptions.</span></span>  
  
 <span data-ttu-id="7aed7-108">当此节为空时，服务初始化将应用取自提供支持的 COM 接口 ID 的默认命名空间和协定名称。</span><span class="sxs-lookup"><span data-stu-id="7aed7-108">When this section is empty, the service initialization applies a default namespace and contract name taken from the supporting COM interface ID.</span></span>  
  
 <span data-ttu-id="7aed7-109">此外，还可以使用 [\<exposedMethod>](exposedmethod.md) 元素指定在 COM + 组件上的接口作为 Web 服务公开时公开的 COM + 方法。</span><span class="sxs-lookup"><span data-stu-id="7aed7-109">In addition, you can use the [\<exposedMethod>](exposedmethod.md) element to specify COM+ methods that are exposed when the interface on a COM+ component is exposed as a Web service.</span></span> <span data-ttu-id="7aed7-110">你还可以使用 [\<persistableTypes>](persistabletypes.md) 来指定集成中使用的持久类型。</span><span class="sxs-lookup"><span data-stu-id="7aed7-110">You can also use the [\<persistableTypes>](persistabletypes.md) to specify persistable types used in integration.</span></span> <span data-ttu-id="7aed7-111">最后，你可以使用 [\<userDefinedType>](userdefinedtype.md) 元素来包含要包含在服务协定中 (UDT) 的用户定义类型。</span><span class="sxs-lookup"><span data-stu-id="7aed7-111">Finally, you can use the [\<userDefinedType>](userdefinedtype.md) element to include User Defined Types (UDT) that are to be included in the service contract.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7aed7-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="7aed7-112">See also</span></span>

- <xref:System.ServiceModel.Configuration.ComContractElementCollection>
- <xref:System.ServiceModel.Configuration.ComContractElement>
- [\<exposedMethod>](exposedmethod.md)
- [\<persistableTypes>](persistabletypes.md)
- [\<userDefinedType>](userdefinedtype.md)
- [\<comContract>](comcontract.md)
- [<span data-ttu-id="7aed7-113">与 COM + 应用程序集成</span><span class="sxs-lookup"><span data-stu-id="7aed7-113">Integrating with COM+ Applications</span></span>](../../../wcf/feature-details/integrating-with-com-plus-applications.md)
- [<span data-ttu-id="7aed7-114">如何：配置 COM+ 服务设置</span><span class="sxs-lookup"><span data-stu-id="7aed7-114">How to: Configure COM+ Service Settings</span></span>](../../../wcf/feature-details/how-to-configure-com-service-settings.md)
