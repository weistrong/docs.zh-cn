---
description: 了解详细信息： GCLOHThreshold 元素
title: GCLOHThreshold 元素
ms.date: 11/20/2019
helpviewer_keywords:
- GCLOHThreshold element
- <GCLOHThreshold> element
ms.openlocfilehash: 5d4ef4e6aaf44642c2307dc27ac2e99e966d3ad0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99652804"
---
# <a name="gclohthreshold-element"></a>GCLOHThreshold 元素

指定阈值大小（以字节为单位），垃圾回收器将对象放置在大型对象堆上 (LOH) 。

[\<configuration>](../configuration-element.md)\
&nbsp;&nbsp;[\<runtime>](runtime-element.md)\
&nbsp;&nbsp;&nbsp;&nbsp;\<GCLOHThreshold>

## <a name="syntax"></a>语法

```xml
<GCLOHThreshold
   enabled="nnnn"/>
```

## <a name="attributes"></a>特性

|属性|描述|
|---------------|-----------------|
|`enabled`|必需的特性。<br /><br />指定导致对象在大型对象堆上的阈值大小。|

### <a name="enabled-attribute"></a>enabled 属性

|值|说明|
|-----------|-----------------|
|`nnnn`|导致对象在大型对象堆上的阈值大小（以字节为单位）。|

## <a name="child-elements"></a>子元素

无。

## <a name="parent-elements"></a>父元素

|元素|说明|
|-------------|-----------------|
|`configuration`|公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。|
|`runtime`|包含有关程序集绑定和垃圾回收的信息。|

## <a name="remarks"></a>备注

.NET Framework 4.8 中引入了此设置。

## <a name="see-also"></a>请参阅

- [运行时设置架构](index.md)
- [配置文件架构](../index.md)
- [垃圾回收的基本知识](../../../../standard/garbage-collection/fundamentals.md)
- [用于 GC 的 NET Core 运行时配置选项](../../../../core/run-time-config/garbage-collector.md)
