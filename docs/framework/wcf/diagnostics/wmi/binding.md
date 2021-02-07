---
description: 了解详细信息：绑定
title: Binding2
ms.date: 03/30/2017
ms.assetid: 09511c6c-5749-4bb0-874e-0f0be36bfe04
ms.openlocfilehash: 36887a9296bfafd0790105e7f4d513efc3009bf8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99757782"
---
# <a name="binding"></a><span data-ttu-id="bba9e-103">绑定</span><span class="sxs-lookup"><span data-stu-id="bba9e-103">Binding</span></span>

<span data-ttu-id="bba9e-104">wmi Binding</span><span class="sxs-lookup"><span data-stu-id="bba9e-104">wmi Binding</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bba9e-105">语法</span><span class="sxs-lookup"><span data-stu-id="bba9e-105">Syntax</span></span>  
  
```csharp
class Binding  
{  
  BindingElement BindingElements[];  
  datetime CloseTimeout;  
  string Name;  
  string Namespace;  
  datetime OpenTimeout;  
  datetime ReceiveTimeout;  
  string Scheme;  
  datetime SendTimeout;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="bba9e-106">方法</span><span class="sxs-lookup"><span data-stu-id="bba9e-106">Methods</span></span>  

 <span data-ttu-id="bba9e-107">Binding 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="bba9e-107">The Binding class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="bba9e-108">属性</span><span class="sxs-lookup"><span data-stu-id="bba9e-108">Properties</span></span>  

 <span data-ttu-id="bba9e-109">Binding 类具有以下属性。</span><span class="sxs-lookup"><span data-stu-id="bba9e-109">The Binding class has the following properties.</span></span>  
  
### <a name="bindingelements"></a><span data-ttu-id="bba9e-110">BindingElements</span><span class="sxs-lookup"><span data-stu-id="bba9e-110">BindingElements</span></span>  

 <span data-ttu-id="bba9e-111">数据类型：BindingElement 数组</span><span class="sxs-lookup"><span data-stu-id="bba9e-111">Data type: BindingElement array</span></span>  
  
 <span data-ttu-id="bba9e-112">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="bba9e-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="bba9e-113">由绑定实现的绑定元素的集合。</span><span class="sxs-lookup"><span data-stu-id="bba9e-113">The collection of binding elements implemented by the binding.</span></span>  
  
### <a name="closetimeout"></a><span data-ttu-id="bba9e-114">CloseTimeout</span><span class="sxs-lookup"><span data-stu-id="bba9e-114">CloseTimeout</span></span>  

 <span data-ttu-id="bba9e-115">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="bba9e-115">Data type: datetime</span></span>  
  
 <span data-ttu-id="bba9e-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="bba9e-116">Access type: Read-only</span></span>  
  
 <span data-ttu-id="bba9e-117">为完成关闭操作提供的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="bba9e-117">The interval of time provided for a close operation to complete.</span></span>  
  
### <a name="name"></a><span data-ttu-id="bba9e-118">名称</span><span class="sxs-lookup"><span data-stu-id="bba9e-118">Name</span></span>  

 <span data-ttu-id="bba9e-119">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="bba9e-119">Data type: string</span></span>  
  
 <span data-ttu-id="bba9e-120">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="bba9e-120">Access type: Read-only</span></span>  
  
 <span data-ttu-id="bba9e-121">绑定的名称。</span><span class="sxs-lookup"><span data-stu-id="bba9e-121">The name of the binding.</span></span>  
  
### <a name="namespace"></a><span data-ttu-id="bba9e-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="bba9e-122">Namespace</span></span>  

 <span data-ttu-id="bba9e-123">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="bba9e-123">Data type: string</span></span>  
  
 <span data-ttu-id="bba9e-124">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="bba9e-124">Access type: Read-only</span></span>  
  
 <span data-ttu-id="bba9e-125">绑定的 XML 命名空间。</span><span class="sxs-lookup"><span data-stu-id="bba9e-125">The XML namespace of the binding.</span></span>  
  
### <a name="opentimeout"></a><span data-ttu-id="bba9e-126">OpenTimeout</span><span class="sxs-lookup"><span data-stu-id="bba9e-126">OpenTimeout</span></span>  

 <span data-ttu-id="bba9e-127">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="bba9e-127">Data type: datetime</span></span>  
  
 <span data-ttu-id="bba9e-128">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="bba9e-128">Access type: Read-only</span></span>  
  
 <span data-ttu-id="bba9e-129">为完成打开操作提供的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="bba9e-129">The interval of time provided for an open operation to complete.</span></span>  
  
### <a name="receivetimeout"></a><span data-ttu-id="bba9e-130">ReceiveTimeout</span><span class="sxs-lookup"><span data-stu-id="bba9e-130">ReceiveTimeout</span></span>  

 <span data-ttu-id="bba9e-131">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="bba9e-131">Data type: datetime</span></span>  
  
 <span data-ttu-id="bba9e-132">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="bba9e-132">Access type: Read-only</span></span>  
  
 <span data-ttu-id="bba9e-133">为完成接收操作提供的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="bba9e-133">The interval of time provided for a receive operation to complete.</span></span>  
  
### <a name="scheme"></a><span data-ttu-id="bba9e-134">Scheme</span><span class="sxs-lookup"><span data-stu-id="bba9e-134">Scheme</span></span>  

 <span data-ttu-id="bba9e-135">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="bba9e-135">Data type: string</span></span>  
  
 <span data-ttu-id="bba9e-136">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="bba9e-136">Access type: Read-only</span></span>  
  
 <span data-ttu-id="bba9e-137">绑定建立的通道和侦听器工厂所使用的 URI 传输方案。</span><span class="sxs-lookup"><span data-stu-id="bba9e-137">The URI transport scheme that is used by the channel and listener factories that are built by the binding.</span></span>  
  
### <a name="sendtimeout"></a><span data-ttu-id="bba9e-138">SendTimeout</span><span class="sxs-lookup"><span data-stu-id="bba9e-138">SendTimeout</span></span>  

 <span data-ttu-id="bba9e-139">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="bba9e-139">Data type: datetime</span></span>  
  
 <span data-ttu-id="bba9e-140">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="bba9e-140">Access type: Read-only</span></span>  
  
 <span data-ttu-id="bba9e-141">为完成发送操作提供的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="bba9e-141">The interval of time provided for a send operation to complete.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bba9e-142">要求</span><span class="sxs-lookup"><span data-stu-id="bba9e-142">Requirements</span></span>  
  
|<span data-ttu-id="bba9e-143">MOF</span><span class="sxs-lookup"><span data-stu-id="bba9e-143">MOF</span></span>|<span data-ttu-id="bba9e-144">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="bba9e-144">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="bba9e-145">命名空间</span><span class="sxs-lookup"><span data-stu-id="bba9e-145">Namespace</span></span>|<span data-ttu-id="bba9e-146">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="bba9e-146">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="bba9e-147">请参阅</span><span class="sxs-lookup"><span data-stu-id="bba9e-147">See also</span></span>

- <xref:System.ServiceModel.Channels.Binding>
