---
description: 了解详细信息： <cryptoClass> 元素
title: <cryptoClass> 元素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib/cryptographySettings/cryptoNameMapping/cryptoClasses/cryptoClass
- http://schemas.microsoft.com/.NetConfiguration/v2.0#cryptoClass
helpviewer_keywords:
- cryptoClass element
- <cryptoClass> element
ms.assetid: 03db52ef-010e-44ea-b6fd-b9c900ecad50
ms.openlocfilehash: 503a079ea78a71a11e4c750a629cf67c9244a25d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99698930"
---
# <a name="cryptoclass-element"></a><span data-ttu-id="70a62-103">\<cryptoClass> 元素</span><span class="sxs-lookup"><span data-stu-id="70a62-103">\<cryptoClass> Element</span></span>

<span data-ttu-id="70a62-104">包含一个加密类，该类具有到元素中的友好名称的映射 [\<nameEntry>](nameentry-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="70a62-104">Contains a cryptography class that has a mapping to a friendly name in the [\<nameEntry>](nameentry-element.md) element.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<mscorlib>**](mscorlib-element-for-cryptography-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<cryptographySettings>**](cryptographysettings-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<cryptoNameMapping>**](cryptonamemapping-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<cryptoClasses>**](cryptoclasses-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<cryptoClass>**

## <a name="syntax"></a><span data-ttu-id="70a62-105">语法</span><span class="sxs-lookup"><span data-stu-id="70a62-105">Syntax</span></span>  
  
```xml  
<cryptoClass customClassName="fully qualified type name" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="70a62-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="70a62-106">Attributes and Elements</span></span>  

 <span data-ttu-id="70a62-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="70a62-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="70a62-108">特性</span><span class="sxs-lookup"><span data-stu-id="70a62-108">Attributes</span></span>  
  
|<span data-ttu-id="70a62-109">属性</span><span class="sxs-lookup"><span data-stu-id="70a62-109">Attribute</span></span>|<span data-ttu-id="70a62-110">描述</span><span class="sxs-lookup"><span data-stu-id="70a62-110">Description</span></span>|  
|---------------|-----------------|  
|`customClassName`|<span data-ttu-id="70a62-111">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="70a62-111">Required attribute.</span></span><br /><br /> <span data-ttu-id="70a62-112">包含加密类的信息。</span><span class="sxs-lookup"><span data-stu-id="70a62-112">Contains the information for the cryptography class.</span></span> <span data-ttu-id="70a62-113">使用此特性可为你的类提供一个短名称。</span><span class="sxs-lookup"><span data-stu-id="70a62-113">Use this attribute to provide a short name for your class.</span></span> <span data-ttu-id="70a62-114">您必须指定满足指定 [完全限定的类型名称](../../../reflection-and-codedom/specifying-fully-qualified-type-names.md)中指定的要求的字符串。</span><span class="sxs-lookup"><span data-stu-id="70a62-114">You must specify a string that meets the requirements specified in [Specifying Fully Qualified Type Names](../../../reflection-and-codedom/specifying-fully-qualified-type-names.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="70a62-115">子元素</span><span class="sxs-lookup"><span data-stu-id="70a62-115">Child Elements</span></span>  

 <span data-ttu-id="70a62-116">无。</span><span class="sxs-lookup"><span data-stu-id="70a62-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="70a62-117">父元素</span><span class="sxs-lookup"><span data-stu-id="70a62-117">Parent Elements</span></span>  
  
|<span data-ttu-id="70a62-118">元素</span><span class="sxs-lookup"><span data-stu-id="70a62-118">Element</span></span>|<span data-ttu-id="70a62-119">说明</span><span class="sxs-lookup"><span data-stu-id="70a62-119">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="70a62-120">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="70a62-120">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`cryptoClasses`|<span data-ttu-id="70a62-121">包含加密类的列表，这些类具有到元素中的友好名称的映射 [\<nameEntry>](nameentry-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="70a62-121">Contains a list of cryptography classes that have a mapping to a friendly name in the [\<nameEntry>](nameentry-element.md) element.</span></span>|  
|`cryptographySettings`|<span data-ttu-id="70a62-122">包含加密设置。</span><span class="sxs-lookup"><span data-stu-id="70a62-122">Contains cryptography settings.</span></span>|  
|`cryptoNameMapping`|<span data-ttu-id="70a62-123">包含类到友好名称的映射。</span><span class="sxs-lookup"><span data-stu-id="70a62-123">Contains mappings of classes to friendly names.</span></span>|  
|`mscorlib`|<span data-ttu-id="70a62-124">包含 [\<cryptographySettings>](cryptographysettings-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="70a62-124">Contains the [\<cryptographySettings>](cryptographysettings-element.md) element.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="70a62-125">示例</span><span class="sxs-lookup"><span data-stu-id="70a62-125">Example</span></span>  

 <span data-ttu-id="70a62-126">下面的示例演示如何使用 **\<cryptoClass>** 元素来引用加密类并配置运行时。</span><span class="sxs-lookup"><span data-stu-id="70a62-126">The following example shows how use the **\<cryptoClass>** element to reference a cryptography class and to configure the runtime.</span></span> <span data-ttu-id="70a62-127">然后，你可以将字符串 "RSA" 传递给 <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A?displayProperty=nameWithType> 方法，并使用 <xref:System.Security.Cryptography.AsymmetricAlgorithm.Create%2A> 方法返回 `MyCryptoRSAClass` 对象。</span><span class="sxs-lookup"><span data-stu-id="70a62-127">You can then pass the string "RSA" to the <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A?displayProperty=nameWithType> method and use the <xref:System.Security.Cryptography.AsymmetricAlgorithm.Create%2A> method to return a `MyCryptoRSAClass` object.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="70a62-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="70a62-128">See also</span></span>

- [<span data-ttu-id="70a62-129">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="70a62-129">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="70a62-130">加密设置架构</span><span class="sxs-lookup"><span data-stu-id="70a62-130">Cryptography Settings Schema</span></span>](index.md)
- [<span data-ttu-id="70a62-131">加密服务</span><span class="sxs-lookup"><span data-stu-id="70a62-131">Cryptographic Services</span></span>](../../../../standard/security/cryptographic-services.md)
- [<span data-ttu-id="70a62-132">配置加密类</span><span class="sxs-lookup"><span data-stu-id="70a62-132">Configuring Cryptography Classes</span></span>](../../configure-cryptography-classes.md)
