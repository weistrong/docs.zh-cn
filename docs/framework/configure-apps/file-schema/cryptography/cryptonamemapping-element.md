---
description: 了解详细信息： <cryptoNameMapping> 元素
title: <cryptoNameMapping> 元素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#cryptoNameMapping
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib/cryptographySettings/cryptoNameMapping
helpviewer_keywords:
- <cryptoNameMapping> element
- cryptoNameMapping element
ms.assetid: c59c9494-149b-4ce6-b38d-371f896ae85c
ms.openlocfilehash: b7dac458fdda0aabf36df96b43dca1529ffe4743
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698903"
---
# <a name="cryptonamemapping-element"></a><span data-ttu-id="421f6-103">\<cryptoNameMapping> 元素</span><span class="sxs-lookup"><span data-stu-id="421f6-103">\<cryptoNameMapping> Element</span></span>

<span data-ttu-id="421f6-104">包含类到友好名称的映射。</span><span class="sxs-lookup"><span data-stu-id="421f6-104">Contains mappings of classes to friendly names.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<mscorlib>**](mscorlib-element-for-cryptography-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<cryptographySettings>**](cryptographysettings-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<cryptoNameMapping>**

## <a name="syntax"></a><span data-ttu-id="421f6-105">语法</span><span class="sxs-lookup"><span data-stu-id="421f6-105">Syntax</span></span>  
  
```xml  
      <cryptoNameMapping>
</cryptoNameMapping>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="421f6-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="421f6-106">Attributes and Elements</span></span>  

 <span data-ttu-id="421f6-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="421f6-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="421f6-108">特性</span><span class="sxs-lookup"><span data-stu-id="421f6-108">Attributes</span></span>  

 <span data-ttu-id="421f6-109">无。</span><span class="sxs-lookup"><span data-stu-id="421f6-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="421f6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="421f6-110">Child Elements</span></span>  
  
|<span data-ttu-id="421f6-111">元素</span><span class="sxs-lookup"><span data-stu-id="421f6-111">Element</span></span>|<span data-ttu-id="421f6-112">说明</span><span class="sxs-lookup"><span data-stu-id="421f6-112">Description</span></span>|  
|-------------|-----------------|  
|`cryptoClasses`|<span data-ttu-id="421f6-113">包含加密类的列表，这些类具有到元素中的友好名称的映射 **\<nameEntry>** 。</span><span class="sxs-lookup"><span data-stu-id="421f6-113">Contains a list of cryptography classes that have a mapping to a friendly name in the **\<nameEntry>** element.</span></span>|  
|`nameEntry`|<span data-ttu-id="421f6-114">将类名称映射到友好算法名称，允许一个类具有多个友好名称。</span><span class="sxs-lookup"><span data-stu-id="421f6-114">Maps a class name to a friendly algorithm name, which allows one class to have many friendly names.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="421f6-115">父元素</span><span class="sxs-lookup"><span data-stu-id="421f6-115">Parent Elements</span></span>  
  
|<span data-ttu-id="421f6-116">元素</span><span class="sxs-lookup"><span data-stu-id="421f6-116">Element</span></span>|<span data-ttu-id="421f6-117">说明</span><span class="sxs-lookup"><span data-stu-id="421f6-117">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="421f6-118">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="421f6-118">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`cryptographySettings`|<span data-ttu-id="421f6-119">包含加密设置。</span><span class="sxs-lookup"><span data-stu-id="421f6-119">Contains cryptography settings.</span></span>|  
|`cryptoNameMapping`|<span data-ttu-id="421f6-120">包含类到友好名称的映射。</span><span class="sxs-lookup"><span data-stu-id="421f6-120">Contains mappings of classes to friendly names.</span></span>|  
|`mscorlib`|<span data-ttu-id="421f6-121">包含 \<cryptographySettings> 元素。</span><span class="sxs-lookup"><span data-stu-id="421f6-121">Contains the \<cryptographySettings> element.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="421f6-122">示例</span><span class="sxs-lookup"><span data-stu-id="421f6-122">Example</span></span>  

 <span data-ttu-id="421f6-123">下面的示例演示如何使用 **\<cryptoNameMapping>** 元素来引用加密类并配置运行时。</span><span class="sxs-lookup"><span data-stu-id="421f6-123">The following example shows how to use the **\<cryptoNameMapping>** element to reference a cryptography class and to configure the runtime.</span></span> <span data-ttu-id="421f6-124">然后，你可以将字符串 "RSA" 传递给 <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A?displayProperty=nameWithType> 方法，并使用 <xref:System.Security.Cryptography.AsymmetricAlgorithm.Create%2A> 方法返回 `MyCryptoRSAClass` 对象。</span><span class="sxs-lookup"><span data-stu-id="421f6-124">You can then pass the string "RSA" to the <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A?displayProperty=nameWithType> method and use the <xref:System.Security.Cryptography.AsymmetricAlgorithm.Create%2A> method to return a `MyCryptoRSAClass` object.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="421f6-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="421f6-125">See also</span></span>

- [<span data-ttu-id="421f6-126">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="421f6-126">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="421f6-127">加密设置架构</span><span class="sxs-lookup"><span data-stu-id="421f6-127">Cryptography Settings Schema</span></span>](index.md)
- [<span data-ttu-id="421f6-128">加密服务</span><span class="sxs-lookup"><span data-stu-id="421f6-128">Cryptographic Services</span></span>](../../../../standard/security/cryptographic-services.md)
- [<span data-ttu-id="421f6-129">配置加密类</span><span class="sxs-lookup"><span data-stu-id="421f6-129">Configuring Cryptography Classes</span></span>](../../configure-cryptography-classes.md)
