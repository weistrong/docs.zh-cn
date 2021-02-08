---
description: 了解详细信息： <etwTracking>
title: <etwTracking>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: cb45c82e-6ea1-4c4d-924c-118a25ae1f35
ms.openlocfilehash: b89d832e73440d5b60a05477ccf85178c2f43a2d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795074"
---
# \<etwTracking>

<span data-ttu-id="c8c59-102">一种服务行为，允许服务使用 <xref:System.Activities.Tracking.EtwTrackingParticipant> 来利用 ETW 跟踪。</span><span class="sxs-lookup"><span data-stu-id="c8c59-102">A service behavior that allows a service to utilize ETW tracking using an <xref:System.Activities.Tracking.EtwTrackingParticipant>.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.ServiceModel>**](system-servicemodel-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<behaviors>**](behaviors-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceBehaviors>**](servicebehaviors-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<behavior>**](behavior-of-servicebehaviors-of-workflow.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<etwTracking>**  
  
## <a name="syntax"></a><span data-ttu-id="c8c59-103">语法</span><span class="sxs-lookup"><span data-stu-id="c8c59-103">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <etwTracking profileName="String" />
    </behavior>
  </serviceBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c8c59-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="c8c59-104">Attributes and Elements</span></span>  

 <span data-ttu-id="c8c59-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c8c59-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c8c59-106">特性</span><span class="sxs-lookup"><span data-stu-id="c8c59-106">Attributes</span></span>  
  
|<span data-ttu-id="c8c59-107">属性</span><span class="sxs-lookup"><span data-stu-id="c8c59-107">Attribute</span></span>|<span data-ttu-id="c8c59-108">说明</span><span class="sxs-lookup"><span data-stu-id="c8c59-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c8c59-109">profileName</span><span class="sxs-lookup"><span data-stu-id="c8c59-109">profileName</span></span>|<span data-ttu-id="c8c59-110">一个字符串，指定与此行为关联的跟踪配置文件的名称。</span><span class="sxs-lookup"><span data-stu-id="c8c59-110">A string that specifies the name of the tracking profile associated with this behavior.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c8c59-111">子元素</span><span class="sxs-lookup"><span data-stu-id="c8c59-111">Child Elements</span></span>  

 <span data-ttu-id="c8c59-112">无。</span><span class="sxs-lookup"><span data-stu-id="c8c59-112">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="c8c59-113">父元素</span><span class="sxs-lookup"><span data-stu-id="c8c59-113">Parent Elements</span></span>  
  
|<span data-ttu-id="c8c59-114">元素</span><span class="sxs-lookup"><span data-stu-id="c8c59-114">Element</span></span>|<span data-ttu-id="c8c59-115">说明</span><span class="sxs-lookup"><span data-stu-id="c8c59-115">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c8c59-116">\<serviceBehaviors> 的 \<behavior></span><span class="sxs-lookup"><span data-stu-id="c8c59-116">\<behavior> of \<serviceBehaviors></span></span>](behavior-of-servicebehaviors-of-workflow.md)|<span data-ttu-id="c8c59-117">指定行为元素。</span><span class="sxs-lookup"><span data-stu-id="c8c59-117">Specifies a behavior element.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c8c59-118">备注</span><span class="sxs-lookup"><span data-stu-id="c8c59-118">Remarks</span></span>  

 <span data-ttu-id="c8c59-119">在添加到服务的行为配置后，此配置元素对工作流服务配置跟踪参与者。</span><span class="sxs-lookup"><span data-stu-id="c8c59-119">When added to the service’s behavior configuration, this configuration element configures a tracking participant on a workflow service.</span></span>  
  
 <span data-ttu-id="c8c59-120">跟踪参与者用于获取从工作流发出的跟踪数据并将其存储在不同的媒体中。</span><span class="sxs-lookup"><span data-stu-id="c8c59-120">Tracking participants are used to get the tracking data emitted from the workflow and store it into different mediums.</span></span> <span data-ttu-id="c8c59-121">同样，也可以在跟踪参与者中执行对跟踪记录的任何后续处理。</span><span class="sxs-lookup"><span data-stu-id="c8c59-121">Likewise, any post processing on the tracking Records can also be done within the tracking participant.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c8c59-122">示例</span><span class="sxs-lookup"><span data-stu-id="c8c59-122">Example</span></span>  

 <span data-ttu-id="c8c59-123">下面的配置示例演示在 Web.config 文件中配置的标准 ETW 跟踪参与者。</span><span class="sxs-lookup"><span data-stu-id="c8c59-123">The following configuration example shows the standard ETW tracking participant being configured in the Web.config file.</span></span>  
  
 <span data-ttu-id="c8c59-124">ETW 跟踪参与者用于将跟踪记录写入 ETW 的提供程序 Id 在部分中定义 **\<diagnostics>** 。</span><span class="sxs-lookup"><span data-stu-id="c8c59-124">The Provider Id that the ETW Tracking Participant uses for writing the Tracking Records to ETW is defined in the **\<diagnostics>** section.</span></span> <span data-ttu-id="c8c59-125">跟踪参与者具有一个与其关联的配置文件，用来指定跟踪参与者已订阅的跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="c8c59-125">The tracking participant has a profile associated with it to specify the tracking records it has subscribed to.</span></span> <span data-ttu-id="c8c59-126">这由元素的 **profileName** 属性定义 **\<add>** 。</span><span class="sxs-lookup"><span data-stu-id="c8c59-126">This is defined by the **profileName** attribute of the **\<add>** element.</span></span> <span data-ttu-id="c8c59-127">一旦定义了这些操作，就会将跟踪参与者添加到 **\<etwTracking>** 服务行为中。</span><span class="sxs-lookup"><span data-stu-id="c8c59-127">Once these are defined, the Tracking Participant is added to the **\<etwTracking>** service behavior.</span></span> <span data-ttu-id="c8c59-128">这会将所选跟踪参与者添加到工作流实例的扩展中，以便它们开始接收跟踪记录。</span><span class="sxs-lookup"><span data-stu-id="c8c59-128">This will add the selected Tracking Participants to the Workflow instance’s extensions, so that they begin to receive the Tracking Records.</span></span>  
  
```xml  
<configuration>
  <system.web>
    <compilation targetFrameworkMoniker=".NETFramework,Version=v4.0"/>
  </system.web>
  <system.serviceModel>
    <diagnostics etwProviderId="52A3165D-4AD9-405C-B1E8-7D9A257EAC9F" />
    <tracking>
      <participants>
        <add name="EtwTrackingParticipant"
             type="System.Activities.Tracking.EtwTrackingParticipant, System.Activities, Version=4.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"
             profileName="HealthMonitoring_Tracking_Profile"/>
      </participants>
    </tracking>
    <behaviors>
      <serviceBehaviors>
        <behavior>
          <etwTracking profileName="Sample Tracking Profile"/>  
        </behavior>
      </serviceBehaviors>
    </behaviors>
  </system.serviceModel>
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="c8c59-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="c8c59-129">See also</span></span>

- <xref:System.ServiceModel.Activities.Description.EtwTrackingBehavior>
- <xref:System.ServiceModel.Activities.Configuration.EtwTrackingBehaviorElement>
- [<span data-ttu-id="c8c59-130">工作流跟踪</span><span class="sxs-lookup"><span data-stu-id="c8c59-130">Workflow Tracking and Tracing</span></span>](../../../windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="c8c59-131">跟踪参与者</span><span class="sxs-lookup"><span data-stu-id="c8c59-131">Tracking Participants</span></span>](../../../windows-workflow-foundation/tracking-participants.md)
