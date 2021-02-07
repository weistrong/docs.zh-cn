---
description: 了解详细信息： <oidMap> 元素
title: <oidMap> 元素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#oidMap
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib/cryptographySettings/oidMap
helpviewer_keywords:
- <oidMap> element
- oidMap element
ms.assetid: 7f0c2246-c070-4748-b96a-2f66a296c539
ms.openlocfilehash: 9a71cc54546f49fcada90a0f9915d44d1fc65e89
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99729987"
---
# <a name="oidmap-element"></a><span data-ttu-id="d6191-103">\<oidMap> 元素</span><span class="sxs-lookup"><span data-stu-id="d6191-103">\<oidMap> Element</span></span>

<span data-ttu-id="d6191-104">包含) 映射到类 (OID 对象标识符。</span><span class="sxs-lookup"><span data-stu-id="d6191-104">Contains ASN.1 object identifier (OID) mappings to classes.</span></span>  

[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<mscorlib>**](mscorlib-element-for-cryptography-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<cryptographySettings>**](cryptographysettings-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<oidMap>**

## <a name="syntax"></a><span data-ttu-id="d6191-105">语法</span><span class="sxs-lookup"><span data-stu-id="d6191-105">Syntax</span></span>  
  
```xml  
<oidMap>
</oidMap>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d6191-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="d6191-106">Attributes and Elements</span></span>  

 <span data-ttu-id="d6191-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d6191-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d6191-108">特性</span><span class="sxs-lookup"><span data-stu-id="d6191-108">Attributes</span></span>  

 <span data-ttu-id="d6191-109">无。</span><span class="sxs-lookup"><span data-stu-id="d6191-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="d6191-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d6191-110">Child Elements</span></span>  
  
|<span data-ttu-id="d6191-111">元素</span><span class="sxs-lookup"><span data-stu-id="d6191-111">Element</span></span>|<span data-ttu-id="d6191-112">说明</span><span class="sxs-lookup"><span data-stu-id="d6191-112">Description</span></span>|  
|-------------|-----------------|  
|[\<oidEntry>](oidentry-element.md)|<span data-ttu-id="d6191-113">将一个 asn.1 OID 映射到友好名称。</span><span class="sxs-lookup"><span data-stu-id="d6191-113">Maps an ASN.1 OID to a friendly name.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d6191-114">父元素</span><span class="sxs-lookup"><span data-stu-id="d6191-114">Parent Elements</span></span>  
  
|<span data-ttu-id="d6191-115">元素</span><span class="sxs-lookup"><span data-stu-id="d6191-115">Element</span></span>|<span data-ttu-id="d6191-116">说明</span><span class="sxs-lookup"><span data-stu-id="d6191-116">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="d6191-117">公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="d6191-117">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`cryptographySettings`|<span data-ttu-id="d6191-118">包含加密设置。</span><span class="sxs-lookup"><span data-stu-id="d6191-118">Contains cryptography settings.</span></span>|  
|`mscorlib`|<span data-ttu-id="d6191-119">包含 `cryptographySettings` 元素。</span><span class="sxs-lookup"><span data-stu-id="d6191-119">Contains the `cryptographySettings` element.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="d6191-120">示例</span><span class="sxs-lookup"><span data-stu-id="d6191-120">Example</span></span>  

 <span data-ttu-id="d6191-121">下面的示例演示如何使用元素来 **\<oidMap>** 包含 RIPEMD-160 哈希算法的 OID 到哈希算法的实现的映射。</span><span class="sxs-lookup"><span data-stu-id="d6191-121">The following example shows how to use the **\<oidMap>** element to contain a mapping of an OID for the RIPEMD-160 hash algorithm to an implementation of that hash algorithm.</span></span>  
  
```xml  
<configuration>  
   <mscorlib>  
      <cryptographySettings>  
         <cryptoNameMapping>  
            <cryptoClasses>  
               <cryptoClass   MyCrypto="MyCryptoClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
            </cryptoClasses>  
            <nameEntry name="RIPEMD-160" class="MyCrypto"/>  
         </cryptoNameMapping>  
         <oidMap>  
            <oidEntry OID="1.3.36.3.2.1"  name="MyCryptoClass"/>  
         </oidMap>  
      </cryptographySettings>  
   </mscorlib>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="d6191-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="d6191-122">See also</span></span>

- [<span data-ttu-id="d6191-123">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="d6191-123">Configuration File Schema</span></span>](../index.md)
- [<span data-ttu-id="d6191-124">加密设置架构</span><span class="sxs-lookup"><span data-stu-id="d6191-124">Cryptography Settings Schema</span></span>](index.md)
- [<span data-ttu-id="d6191-125">加密服务</span><span class="sxs-lookup"><span data-stu-id="d6191-125">Cryptographic Services</span></span>](../../../../standard/security/cryptographic-services.md)
- [<span data-ttu-id="d6191-126">配置加密类</span><span class="sxs-lookup"><span data-stu-id="d6191-126">Configuring Cryptography Classes</span></span>](../../configure-cryptography-classes.md)
- [<span data-ttu-id="d6191-127">将对象标识符映射到加密算法</span><span class="sxs-lookup"><span data-stu-id="d6191-127">Mapping Object Identifiers to Cryptography Algorithms</span></span>](../../map-object-identifiers-to-cryptography-algorithms.md)
