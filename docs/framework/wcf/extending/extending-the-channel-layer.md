---
description: 了解详细信息：扩展通道层
title: 扩展通道层
ms.date: 03/30/2017
helpviewer_keywords:
- extending channels [WCF]
ms.assetid: 4238db74-2fb6-4dc8-a326-f58527230810
ms.openlocfilehash: 4588a2749127e454801615cc8916d83fc15592bc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99685577"
---
# <a name="extending-the-channel-layer"></a><span data-ttu-id="e0675-103">扩展通道层</span><span class="sxs-lookup"><span data-stu-id="e0675-103">Extending the Channel Layer</span></span>

<span data-ttu-id="e0675-104">通道层负责在客户端和服务之间交换消息。</span><span class="sxs-lookup"><span data-stu-id="e0675-104">The channel layer is responsible for the exchange of messages between clients and services.</span></span> <span data-ttu-id="e0675-105">通道扩展可以实现新的协议功能（例如安全性）或传输功能（例如实现新的网络传输来传送 SOAP 消息）。</span><span class="sxs-lookup"><span data-stu-id="e0675-105">Channel extensions can implement new protocol functionality, such as security, or transport functionality, such as implementing a new network transport to carry SOAP messages.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="e0675-106">本节内容</span><span class="sxs-lookup"><span data-stu-id="e0675-106">In This Section</span></span>  

 [<span data-ttu-id="e0675-107">通道模型概述</span><span class="sxs-lookup"><span data-stu-id="e0675-107">Channel Model Overview</span></span>](channel-model-overview.md)  
 <span data-ttu-id="e0675-108">在较高层面概述了什么是通道、通道提供的功能以及通道在服务和客户端应用程序中的工作方式。</span><span class="sxs-lookup"><span data-stu-id="e0675-108">Provides a high-level overview of what channels are, the features that they provide and how they work both in a service and a client application.</span></span>  
  
 [<span data-ttu-id="e0675-109">开发通道</span><span class="sxs-lookup"><span data-stu-id="e0675-109">Developing Channels</span></span>](developing-channels.md)  
 <span data-ttu-id="e0675-110">深入描述各种通道基础结构类型所起的作用、状态引擎和状态生命周期的工作方式、如何处理异常和错误、如何实现元数据支持以及通道如何使用消息编码器。</span><span class="sxs-lookup"><span data-stu-id="e0675-110">Describes in depth the roles that the various channel infrastructure types play, how the state engine and state lifecycle works, how to handle exceptions and faults, how to implement metadata support, and how channels work with message encoders.</span></span>  
  
 [<span data-ttu-id="e0675-111">自定义编码器</span><span class="sxs-lookup"><span data-stu-id="e0675-111">Custom Encoders</span></span>](custom-encoders.md)  
 <span data-ttu-id="e0675-112">描述消息编码器在通道中所起的作用以及如何生成消息编码器。</span><span class="sxs-lookup"><span data-stu-id="e0675-112">Describes the role that message encoders play in channels and how to build one.</span></span>  
  
 [<span data-ttu-id="e0675-113">自定义流升级</span><span class="sxs-lookup"><span data-stu-id="e0675-113">Custom Stream Upgrades</span></span>](custom-stream-upgrades.md)  
 <span data-ttu-id="e0675-114">描述由面向流的传输所提供的流的升级过程。</span><span class="sxs-lookup"><span data-stu-id="e0675-114">Describes the process of upgrading the streams provided by stream-oriented transports.</span></span>
