---
description: 了解详细信息： <cryptographySettings> 元素
title: <cryptographySettings> 元素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib/cryptographySettings
- http://schemas.microsoft.com/.NetConfiguration/v2.0#cryptographySettings
helpviewer_keywords:
- cryptographySettings element
- <cryptographySettings> element
ms.assetid: 6201b7da-bcb7-49f7-b9f5-ba1fe05573b9
ms.openlocfilehash: afd4fdbc24dfaac60ce24b7a439a8d4d8a9427ea
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99730091"
---
# <a name="cryptographysettings-element"></a><span data-ttu-id="b46bb-103">\<cryptographySettings> 元素</span><span class="sxs-lookup"><span data-stu-id="b46bb-103">\<cryptographySettings> Element</span></span>

<span data-ttu-id="b46bb-104">包含加密设置。</span><span class="sxs-lookup"><span data-stu-id="b46bb-104">Contains cryptography settings.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<mscorlib>**](mscorlib-element-for-cryptography-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<cryptographySettings>**

## <a name="syntax"></a><span data-ttu-id="b46bb-105">语法</span><span class="sxs-lookup"><span data-stu-id="b46bb-105">Syntax</span></span>  
  
```xml  
      <cryptographySettings>
</cryptographySettings>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b46bb-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="b46bb-106">Attributes and Elements</span></span>  

 <span data-ttu-id="b46bb-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b46bb-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b46bb-108">特性</span><span class="sxs-lookup"><span data-stu-id="b46bb-108">Attributes</span></span>  

 <span data-ttu-id="b46bb-109">无。</span><span class="sxs-lookup"><span data-stu-id="b46bb-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="b46bb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b46bb-110">Child Elements</span></span>  
  
|<span data-ttu-id="b46bb-111">元素</span><span class="sxs-lookup"><span data-stu-id="b46bb-111">Element</span></span>|<span data-ttu-id="b46bb-112">说明</span><span class="sxs-lookup"><span data-stu-id="b46bb-112">Description</span></span>|  
|-------------|-----------------|  
|[\<cryptoNameMapping>](cryptonamemapping-element.md)|<span data-ttu-id="b46bb-113">包含类到友好名称的映射。</span><span class="sxs-lookup"><span data-stu-id="b46bb-113">Contains mappings of classes to friendly names.</span></span>|  
|[\<oidMap>](oidmap-element.md)|<span data-ttu-id="b46bb-114">包含) 映射到类 (OID 对象标识符。</span><span class="sxs-lookup"><span data-stu-id="b46bb-114">Contains ASN.1 object identifier (OID) mappings to classes.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="b46bb-115">父元素</span><span class="sxs-lookup"><span data-stu-id="b46bb-115">Parent Elements</span></span>  
  
|<span data-ttu-id="b46bb-116">元素</span><span class="sxs-lookup"><span data-stu-id="b46bb-116">Element</span></span>|<span data-ttu-id="b46bb-117">说明</span><span class="sxs-lookup"><span data-stu-id="b46bb-117">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="b46bb-118">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="b46bb-118">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`mscorlib`|<span data-ttu-id="b46bb-119">包含 `cryptographySettings` 元素。</span><span class="sxs-lookup"><span data-stu-id="b46bb-119">Contains the `cryptographySettings` element.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="b46bb-120">示例</span><span class="sxs-lookup"><span data-stu-id="b46bb-120">Example</span></span>  

 <span data-ttu-id="b46bb-121">下面的示例演示如何使用 **\<cryptographySettings>** 元素包含加密名称映射和 OID 映射。</span><span class="sxs-lookup"><span data-stu-id="b46bb-121">The following example shows how use the **\<cryptographySettings>** element to contain cryptography name mappings and OID mappings.</span></span> <span data-ttu-id="b46bb-122">此示例将配置运行时，以便 <xref:System.Security.Cryptography.HashAlgorithm.Create%2A?displayProperty=nameWithType> 返回 `MyHashClass` 对象， `MyCryptoClass` 类映射到对象标识符1.3.36.2.1。</span><span class="sxs-lookup"><span data-stu-id="b46bb-122">This example configures the runtime so that <xref:System.Security.Cryptography.HashAlgorithm.Create%2A?displayProperty=nameWithType> returns a `MyHashClass` object and the `MyCryptoClass` class maps to the object identifier 1.3.36.2.1.</span></span>  
  
```xml  
<configuration>  
   <mscorlib>  
      <cryptographySettings>  
         <cryptoNameMapping>  
            <cryptoClasses>  
               <cryptoClass   MyHash="MyHashClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
               <cryptoClass   MyCrypto="MyCryptoClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
            </cryptoClasses>  
            <nameEntry name="System.Security.Cryptography.HashAlgorithm"  
                       class="MyHash"/>  
         </cryptoNameMapping>  
         <oidMap>  
            <oidEntry OID="1.3.36.3.2.1"   name="MyCryptoClass"/>  
         </oidMap>  
      </cryptographySettings>  
   </mscorlib>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="b46bb-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="b46bb-123">See also</span></span>

- [<span data-ttu-id="b46bb-124">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="b46bb-124">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="b46bb-125">加密设置架构</span><span class="sxs-lookup"><span data-stu-id="b46bb-125">Cryptography Settings Schema</span></span>](index.md)
- [<span data-ttu-id="b46bb-126">加密服务</span><span class="sxs-lookup"><span data-stu-id="b46bb-126">Cryptographic Services</span></span>](../../../../standard/security/cryptographic-services.md)
