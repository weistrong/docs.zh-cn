---
description: 了解详细信息： <certificateValidator>
title: <certificateValidator>
ms.date: 03/30/2017
ms.assetid: 86161897-c20f-4ad8-9d7f-050c247251bf
author: BrucePerlerMS
ms.openlocfilehash: 0b92eada916b239ca56342021bb958da6d02c2e7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802159"
---
# \<certificateValidator>

<span data-ttu-id="f18f5-102">指定证书验证的自定义类型。</span><span class="sxs-lookup"><span data-stu-id="f18f5-102">Specifies a custom type for certificate validation.</span></span> <span data-ttu-id="f18f5-103">仅当 `certificateValidationMode` 元素的属性 [\<certificateValidation>](certificatevalidation.md) 设置为 "Custom" 时才使用此类型。</span><span class="sxs-lookup"><span data-stu-id="f18f5-103">This type is used only if the `certificateValidationMode` attribute of the [\<certificateValidation>](certificatevalidation.md) element is set to "Custom".</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.identityModel>**](system-identitymodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<identityConfiguration>**](identityconfiguration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<certificateValidation>**](certificatevalidation.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<certificateValidator>**  
  
## <a name="syntax"></a><span data-ttu-id="f18f5-104">语法</span><span class="sxs-lookup"><span data-stu-id="f18f5-104">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <certificateValidation>  
      <certificateValidator type=xs:string>  
      </certificateValidator>  
    </certificateValidation>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f18f5-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="f18f5-105">Attributes and Elements</span></span>  

 <span data-ttu-id="f18f5-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f18f5-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f18f5-107">特性</span><span class="sxs-lookup"><span data-stu-id="f18f5-107">Attributes</span></span>  
  
|<span data-ttu-id="f18f5-108">属性</span><span class="sxs-lookup"><span data-stu-id="f18f5-108">Attribute</span></span>|<span data-ttu-id="f18f5-109">说明</span><span class="sxs-lookup"><span data-stu-id="f18f5-109">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f18f5-110">type</span><span class="sxs-lookup"><span data-stu-id="f18f5-110">type</span></span>|<span data-ttu-id="f18f5-111">指定从类派生的自定义类型 <xref:System.IdentityModel.Selectors.X509CertificateValidator> 。</span><span class="sxs-lookup"><span data-stu-id="f18f5-111">Specifies a custom type that derives from the <xref:System.IdentityModel.Selectors.X509CertificateValidator> class.</span></span> <span data-ttu-id="f18f5-112">将 `certificateValidationMode` 元素的属性设置 [\<certificateValidation>](certificatevalidation.md) 为 "自定义" 可使用此类型。</span><span class="sxs-lookup"><span data-stu-id="f18f5-112">Set the `certificateValidationMode` attribute of the [\<certificateValidation>](certificatevalidation.md) element to "Custom" to use this type.</span></span> <span data-ttu-id="f18f5-113">有关如何指定属性的详细信息 `type` ，请参阅 [自定义类型引用](../windows-workflow-foundation/index.md)。</span><span class="sxs-lookup"><span data-stu-id="f18f5-113">For more information about how to specify the `type` attribute, see [Custom Type References](../windows-workflow-foundation/index.md).</span></span> <span data-ttu-id="f18f5-114">可选。</span><span class="sxs-lookup"><span data-stu-id="f18f5-114">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f18f5-115">子元素</span><span class="sxs-lookup"><span data-stu-id="f18f5-115">Child Elements</span></span>  

 <span data-ttu-id="f18f5-116">无</span><span class="sxs-lookup"><span data-stu-id="f18f5-116">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f18f5-117">父元素</span><span class="sxs-lookup"><span data-stu-id="f18f5-117">Parent Elements</span></span>  
  
|<span data-ttu-id="f18f5-118">元素</span><span class="sxs-lookup"><span data-stu-id="f18f5-118">Element</span></span>|<span data-ttu-id="f18f5-119">说明</span><span class="sxs-lookup"><span data-stu-id="f18f5-119">Description</span></span>|  
|-------------|-----------------|  
|[\<certificateValidation>](certificatevalidation.md)|<span data-ttu-id="f18f5-120">控制标记处理程序用于验证证书的设置。</span><span class="sxs-lookup"><span data-stu-id="f18f5-120">Controls the settings that token handlers use to validate certificates.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="f18f5-121">示例</span><span class="sxs-lookup"><span data-stu-id="f18f5-121">Example</span></span>  
  
```xml  
<certificateValidation certificateValidationMode="Custom"  
                       revocationMode="Online"  
                       trustedStoreLocation="LocalMachine">  
    <certificateValidator type="MyNamespace.CustomValidator, MyAssembly" />
</certificateValidation>
```
