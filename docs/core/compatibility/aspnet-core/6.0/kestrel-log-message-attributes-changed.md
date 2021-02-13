---
title: 中断性变更：Kestrel：日志消息属性已更改
description: 了解 ASP.NET Core 6.0 中的以下中断性变更：Kestrel：日志消息属性已更改
author: scottaddie
ms.author: scaddie
ms.date: 02/01/2021
ms.openlocfilehash: 30b03c22a6c85623fec7db14b58b169f887395a0
ms.sourcegitcommit: 4df8e005c074ceb1f978f007b222fe253be2baf3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2021
ms.locfileid: "99551528"
---
# <a name="kestrel-log-message-attributes-changed"></a><span data-ttu-id="d2187-103">Kestrel：日志消息属性已更改</span><span class="sxs-lookup"><span data-stu-id="d2187-103">Kestrel: Log message attributes changed</span></span>

<span data-ttu-id="d2187-104">Kestrel 日志消息具有关联的 ID 和名称。</span><span class="sxs-lookup"><span data-stu-id="d2187-104">Kestrel log messages have associated IDs and names.</span></span> <span data-ttu-id="d2187-105">这些属性唯一地标识了不同类型的日志消息。</span><span class="sxs-lookup"><span data-stu-id="d2187-105">These attributes uniquely identify different kinds of log messages.</span></span> <span data-ttu-id="d2187-106">其中一些 ID 和名称是错误重复的。</span><span class="sxs-lookup"><span data-stu-id="d2187-106">Some of those IDs and names were incorrectly duplicated.</span></span> <span data-ttu-id="d2187-107">这个重复问题在 ASP.NET Core 6.0 中得到了修复。</span><span class="sxs-lookup"><span data-stu-id="d2187-107">This duplication problem is fixed in ASP.NET Core 6.0.</span></span>

## <a name="version-introduced"></a><span data-ttu-id="d2187-108">引入的版本</span><span class="sxs-lookup"><span data-stu-id="d2187-108">Version introduced</span></span>

<span data-ttu-id="d2187-109">6.0</span><span class="sxs-lookup"><span data-stu-id="d2187-109">6.0</span></span>

## <a name="old-behavior"></a><span data-ttu-id="d2187-110">旧行为</span><span class="sxs-lookup"><span data-stu-id="d2187-110">Old behavior</span></span>

<span data-ttu-id="d2187-111">下表显示 ASP.NET Core 6.0 之前受影响的日志消息的状态。</span><span class="sxs-lookup"><span data-stu-id="d2187-111">The following table shows the state of the affected log messages before ASP.NET Core 6.0.</span></span>

| <span data-ttu-id="d2187-112">消息描述</span><span class="sxs-lookup"><span data-stu-id="d2187-112">Message description</span></span>                   | <span data-ttu-id="d2187-113">名称</span><span class="sxs-lookup"><span data-stu-id="d2187-113">Name</span></span>                    | <span data-ttu-id="d2187-114">ID</span><span class="sxs-lookup"><span data-stu-id="d2187-114">ID</span></span> |
|---------------------------------------|-------------------------|----|
| <span data-ttu-id="d2187-115">HTTP/2 连接关闭日志消息</span><span class="sxs-lookup"><span data-stu-id="d2187-115">HTTP/2 connection closed log messages</span></span> | `Http2ConnectionClosed` | <span data-ttu-id="d2187-116">36</span><span class="sxs-lookup"><span data-stu-id="d2187-116">36</span></span> |
| <span data-ttu-id="d2187-117">HTTP/2 帧发送日志消息</span><span class="sxs-lookup"><span data-stu-id="d2187-117">HTTP/2 frame sending log messages</span></span>     | `Http2FrameReceived`    | <span data-ttu-id="d2187-118">37</span><span class="sxs-lookup"><span data-stu-id="d2187-118">37</span></span> |

## <a name="new-behavior"></a><span data-ttu-id="d2187-119">新行为</span><span class="sxs-lookup"><span data-stu-id="d2187-119">New behavior</span></span>

<span data-ttu-id="d2187-120">下表显示 ASP.NET Core 6.0 中受影响的日志消息的状态。</span><span class="sxs-lookup"><span data-stu-id="d2187-120">The following table shows the state of the affected log messages in ASP.NET Core 6.0.</span></span>

| <span data-ttu-id="d2187-121">消息描述</span><span class="sxs-lookup"><span data-stu-id="d2187-121">Message description</span></span>                   | <span data-ttu-id="d2187-122">名称</span><span class="sxs-lookup"><span data-stu-id="d2187-122">Name</span></span>                    | <span data-ttu-id="d2187-123">ID</span><span class="sxs-lookup"><span data-stu-id="d2187-123">ID</span></span> |
|---------------------------------------|-------------------------|----|
| <span data-ttu-id="d2187-124">HTTP/2 连接关闭日志消息</span><span class="sxs-lookup"><span data-stu-id="d2187-124">HTTP/2 connection closed log messages</span></span> | `Http2ConnectionClosed` | <span data-ttu-id="d2187-125">48</span><span class="sxs-lookup"><span data-stu-id="d2187-125">48</span></span> |
| <span data-ttu-id="d2187-126">HTTP/2 帧发送日志消息</span><span class="sxs-lookup"><span data-stu-id="d2187-126">HTTP/2 frame sending log messages</span></span>     | `Http2FrameSending`     | <span data-ttu-id="d2187-127">49</span><span class="sxs-lookup"><span data-stu-id="d2187-127">49</span></span> |

## <a name="reason-for-change"></a><span data-ttu-id="d2187-128">更改原因</span><span class="sxs-lookup"><span data-stu-id="d2187-128">Reason for change</span></span>

<span data-ttu-id="d2187-129">日志 ID 和名称应是唯一的，这样才能识别不同的消息类型。</span><span class="sxs-lookup"><span data-stu-id="d2187-129">Log IDs and names should be unique so different message types can be identified.</span></span>

## <a name="recommended-action"></a><span data-ttu-id="d2187-130">建议的操作</span><span class="sxs-lookup"><span data-stu-id="d2187-130">Recommended action</span></span>

<span data-ttu-id="d2187-131">如果你的代码或配置引用了旧的 ID 和名称，请更新这些引用以使用新的 ID 和名称。</span><span class="sxs-lookup"><span data-stu-id="d2187-131">If you have code or configuration that references the old IDs and names, update those references to use the new IDs and names.</span></span>

<!--

## Category

ASP.NET Core

## Affected APIs

Not detectable via API analysis

-->
