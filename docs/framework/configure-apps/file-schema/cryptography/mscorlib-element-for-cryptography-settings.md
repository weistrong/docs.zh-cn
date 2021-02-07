---
description: 了解详细信息： <mscorlib> 密码设置的元素
title: Cryptography 设置的 <mscorlib> 元素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#mscorlib
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib
helpviewer_keywords:
- mscorlib element
- <mscorlib> element
ms.assetid: d549668f-31f1-4b92-8021-a9135c09ca3c
ms.openlocfilehash: 7606cdd1349c7594b5303832eed59ac51c1ddfe6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698890"
---
# <a name="mscorlib-element-for-cryptography-settings"></a><span data-ttu-id="bbf95-103">Cryptography 设置的 \<mscorlib> 元素</span><span class="sxs-lookup"><span data-stu-id="bbf95-103">\<mscorlib> Element for Cryptography Settings</span></span>

<span data-ttu-id="bbf95-104">包含[ \<cryptographySettings> 元素](cryptographysettings-element.md)。</span><span class="sxs-lookup"><span data-stu-id="bbf95-104">Contains the [\<cryptographySettings> element](cryptographysettings-element.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)  
&nbsp;&nbsp;**\<mscorlib>**  
  
## <a name="syntax"></a><span data-ttu-id="bbf95-105">语法</span><span class="sxs-lookup"><span data-stu-id="bbf95-105">Syntax</span></span>  
  
```xml  
      <mscorlib>
</mscorlib>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bbf95-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="bbf95-106">Attributes and Elements</span></span>  

 <span data-ttu-id="bbf95-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bbf95-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bbf95-108">特性</span><span class="sxs-lookup"><span data-stu-id="bbf95-108">Attributes</span></span>  

 <span data-ttu-id="bbf95-109">无。</span><span class="sxs-lookup"><span data-stu-id="bbf95-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="bbf95-110">子元素</span><span class="sxs-lookup"><span data-stu-id="bbf95-110">Child Elements</span></span>  
  
|<span data-ttu-id="bbf95-111">元素</span><span class="sxs-lookup"><span data-stu-id="bbf95-111">Element</span></span>|<span data-ttu-id="bbf95-112">说明</span><span class="sxs-lookup"><span data-stu-id="bbf95-112">Description</span></span>|  
|-------------|-----------------|  
|`cryptographySettings`|<span data-ttu-id="bbf95-113">包含加密设置。</span><span class="sxs-lookup"><span data-stu-id="bbf95-113">Contains cryptography settings.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="bbf95-114">父元素</span><span class="sxs-lookup"><span data-stu-id="bbf95-114">Parent Elements</span></span>  
  
|<span data-ttu-id="bbf95-115">元素</span><span class="sxs-lookup"><span data-stu-id="bbf95-115">Element</span></span>|<span data-ttu-id="bbf95-116">说明</span><span class="sxs-lookup"><span data-stu-id="bbf95-116">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="bbf95-117">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="bbf95-117">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="bbf95-118">示例</span><span class="sxs-lookup"><span data-stu-id="bbf95-118">Example</span></span>  

 <span data-ttu-id="bbf95-119">下面的示例演示如何使用 **\<mscorlib>** 元素来引用加密类并配置运行时。</span><span class="sxs-lookup"><span data-stu-id="bbf95-119">The following example shows how to use the **\<mscorlib>** element to reference a cryptography class and to configure the runtime.</span></span> <span data-ttu-id="bbf95-120">然后，你可以将字符串 "RSA" 传递给 <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A?displayProperty=nameWithType> 方法，并使用 <xref:System.Security.Cryptography.AsymmetricAlgorithm.Create%2A> 方法返回 `MyCryptoRSAClass` 对象。</span><span class="sxs-lookup"><span data-stu-id="bbf95-120">You can then pass the string "RSA" to the <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A?displayProperty=nameWithType> method and use the <xref:System.Security.Cryptography.AsymmetricAlgorithm.Create%2A> method to return a `MyCryptoRSAClass` object.</span></span>  
  
```xml  
<configuration>  
   <mscorlib>  
      <cryptographySettings>  
         <cryptoNameMapping>  
            <cryptoClasses>  
               <cryptoClass   MyCryptoRSA="MyCryptoRSAClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
            </cryptoClasses>  
            <nameEntry name="RSA" class="MyCryptoRSA"/>  
            <nameEntry name="System.Security.Cryptography.AsymmetricAlgorithm"  
                       class="MyCryptoRSA"/>  
         </cryptoNameMapping>  
      </cryptographySettings>  
   </mscorlib>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="bbf95-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="bbf95-121">See also</span></span>

- <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A>
- <xref:System.Security.Cryptography>
- [<span data-ttu-id="bbf95-122">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="bbf95-122">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="bbf95-123">加密设置架构</span><span class="sxs-lookup"><span data-stu-id="bbf95-123">Cryptography Settings Schema</span></span>](index.md)
- [<span data-ttu-id="bbf95-124">加密服务</span><span class="sxs-lookup"><span data-stu-id="bbf95-124">Cryptographic Services</span></span>](../../../../standard/security/cryptographic-services.md)
- [<span data-ttu-id="bbf95-125">配置加密类</span><span class="sxs-lookup"><span data-stu-id="bbf95-125">Configuring Cryptography Classes</span></span>](../../configure-cryptography-classes.md)
