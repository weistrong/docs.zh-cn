---
description: 详细了解： <remove> 的元素 <namedCaches>
title: <namedCaches> 的 <remove> 元素
ms.date: 03/30/2017
helpviewer_keywords:
- remove element for namedCaches
- <remove> element for namedCaches
ms.assetid: 24211ea5-163e-4fe5-aed8-004d8499760c
ms.openlocfilehash: 5b39fc596735d746c52cdb5623962f5b9952fa3e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802455"
---
# <a name="remove-element-for-namedcaches"></a>\<namedCaches> 的 \<remove> 元素

从内存缓存的 `namedCaches` 集合中删除一个命名的缓存条目。  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.runtime.caching>**](system-runtime-caching-element-cache-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<memoryCache>**](memorycache-element-cache-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<namedCaches>**](namedcaches-element-cache-settings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<remove>**  
  
## <a name="syntax"></a>语法  
  
```xml  
<namedCaches>  
    <remove name="default" />  
    <!-- child elements -->  
 </namedCaches>  
```  
  
## <a name="type"></a>类型  

 `None`  
  
## <a name="attributes-and-elements"></a>特性和元素  

 下列各节描述了特性、子元素和父元素。  
  
### <a name="attributes"></a>特性  

 `None`  
  
### <a name="child-elements"></a>子元素  

 `None`  
  
### <a name="parent-elements"></a>父元素  
  
|元素|说明|  
|-------------|-----------------|  
|[\<namedCaches>](namedcaches-element-cache-settings.md)|包含命名实例的配置设置的集合 <xref:System.Runtime.Caching.MemoryCache> 。|  
  
## <a name="remarks"></a>备注  

 `remove`元素 `namedCache` 从内存缓存的命名缓存集合中删除一个条目。  
  
## <a name="see-also"></a>请参阅

- [\<namedCaches> 元素 (缓存设置) ](namedcaches-element-cache-settings.md)
