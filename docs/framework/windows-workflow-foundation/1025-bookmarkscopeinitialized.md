---
description: 了解详细信息： 1025-BookmarkScopeInitialized
title: 1025 - BookmarkScopeInitialized
ms.date: 03/30/2017
ms.assetid: 63584434-e709-471d-9e96-97d3d99e70d6
ms.openlocfilehash: 22e686253fc5d580fba453950825072667247fad
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755494"
---
# <a name="1025---bookmarkscopeinitialized"></a>1025 - BookmarkScopeInitialized

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|1025|  
|关键字|WFRuntime|  
|级别|“详细”|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/调试|  
  
## <a name="description"></a>说明  

 指示已初始化 BookmarkScope。  
  
## <a name="message"></a>消息  

 TemporaryId 为“%1”的 BookmarkScope 已初始化，ID 为:“%2”。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|TemporaryId|xs:string|书签的临时 ID。|  
|InitializedId|xs:string|书签的初始化的 ID。|  
|应用程序域|xs:string|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
