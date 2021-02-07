---
description: 了解详细信息：日志记录类
title: '记录类 (System.Net) '
ms.date: 06/12/2020
ms.technology: dotnet-networking
topic_type:
- apiref
api_name:
- System.Net.Logging
- System.Net.Logging.Associate
- System.Net.Logging.Enter
- System.Net.Logging.Exception
- System.Net.Logging.Exit
- System.Net.Logging.get_Http
- System.Net.Logging.get_On
api_location:
- System.dll
api_type:
- Assembly
ms.openlocfilehash: 1ae3079ab21502ee3f5bf71db57f0695da9a8571
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99726203"
---
# <a name="logging-class"></a><span data-ttu-id="3a41c-103">Logging 类</span><span class="sxs-lookup"><span data-stu-id="3a41c-103">Logging class</span></span>

<span data-ttu-id="3a41c-104">提供跟踪日志记录功能。</span><span class="sxs-lookup"><span data-stu-id="3a41c-104">Provides trace logging functionality.</span></span>

```csharp
internal class Logging
```

> [!WARNING]
> <span data-ttu-id="3a41c-105">此类是内部的，不应在代码中直接使用。</span><span class="sxs-lookup"><span data-stu-id="3a41c-105">This class is internal and is not meant to be used directly in your code.</span></span>
>
> <span data-ttu-id="3a41c-106">在任何情况下，Microsoft 不支持在生产应用程序中使用此类。</span><span class="sxs-lookup"><span data-stu-id="3a41c-106">Microsoft does not support the use of this class in a production application under any circumstance.</span></span>

## <a name="associate-method"></a><span data-ttu-id="3a41c-107">关联方法</span><span class="sxs-lookup"><span data-stu-id="3a41c-107">Associate method</span></span>

<span data-ttu-id="3a41c-108">记录两个对象彼此关联的信息。</span><span class="sxs-lookup"><span data-stu-id="3a41c-108">Logs information that two objects are associated with each other.</span></span>

```csharp
internal static void Associate(TraceSource traceSource, object objA, object objB)
```

### <a name="parameters"></a><span data-ttu-id="3a41c-109">参数</span><span class="sxs-lookup"><span data-stu-id="3a41c-109">Parameters</span></span>

- <span data-ttu-id="3a41c-110">`traceSource` <xref:System.Diagnostics.TraceSource></span><span class="sxs-lookup"><span data-stu-id="3a41c-110">`traceSource` <xref:System.Diagnostics.TraceSource></span></span>

  <span data-ttu-id="3a41c-111">要将事件记录到的跟踪源。</span><span class="sxs-lookup"><span data-stu-id="3a41c-111">The trace source to log the event to.</span></span>

- <span data-ttu-id="3a41c-112">`objA` <xref:System.Object></span><span class="sxs-lookup"><span data-stu-id="3a41c-112">`objA` <xref:System.Object></span></span>

  <span data-ttu-id="3a41c-113">要与关联的对象 `objB` 。</span><span class="sxs-lookup"><span data-stu-id="3a41c-113">The object to associate with `objB`.</span></span>

- <span data-ttu-id="3a41c-114">`objB` <xref:System.Object></span><span class="sxs-lookup"><span data-stu-id="3a41c-114">`objB` <xref:System.Object></span></span>

  <span data-ttu-id="3a41c-115">要与关联的对象 `objA` 。</span><span class="sxs-lookup"><span data-stu-id="3a41c-115">The object to associate with `objA`.</span></span>

## <a name="entertracesource-object-string-string-method"></a><span data-ttu-id="3a41c-116">输入 (TraceSource、object、string、string) 方法</span><span class="sxs-lookup"><span data-stu-id="3a41c-116">Enter(TraceSource, object, string, string) method</span></span>

<span data-ttu-id="3a41c-117">日志进入到方法。</span><span class="sxs-lookup"><span data-stu-id="3a41c-117">Logs entrance to a method.</span></span>

```csharp
internal static void Enter(TraceSource traceSource, object obj, string method, string param)
```

### <a name="parameters"></a><span data-ttu-id="3a41c-118">参数</span><span class="sxs-lookup"><span data-stu-id="3a41c-118">Parameters</span></span>

- <span data-ttu-id="3a41c-119">`traceSource` <xref:System.Diagnostics.TraceSource></span><span class="sxs-lookup"><span data-stu-id="3a41c-119">`traceSource` <xref:System.Diagnostics.TraceSource></span></span>

  <span data-ttu-id="3a41c-120">要将事件记录到的跟踪源。</span><span class="sxs-lookup"><span data-stu-id="3a41c-120">The trace source to log the event to.</span></span>

- <span data-ttu-id="3a41c-121">`obj` <xref:System.Object></span><span class="sxs-lookup"><span data-stu-id="3a41c-121">`obj` <xref:System.Object></span></span>

  <span data-ttu-id="3a41c-122">在其上调用方法的对象。</span><span class="sxs-lookup"><span data-stu-id="3a41c-122">The object that the method was called on.</span></span>

- <span data-ttu-id="3a41c-123">`method` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-123">`method` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-124">正在输入的方法。</span><span class="sxs-lookup"><span data-stu-id="3a41c-124">The method that is being entered.</span></span>

- <span data-ttu-id="3a41c-125">`param` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-125">`param` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-126">传递给方法的参数。</span><span class="sxs-lookup"><span data-stu-id="3a41c-126">The parameters that were passed to the method.</span></span>

## <a name="entertracesource-object-string-object-method"></a><span data-ttu-id="3a41c-127">输入 (TraceSource、object、string、object) 方法</span><span class="sxs-lookup"><span data-stu-id="3a41c-127">Enter(TraceSource, object, string, object) method</span></span>

<span data-ttu-id="3a41c-128">日志进入到方法。</span><span class="sxs-lookup"><span data-stu-id="3a41c-128">Logs entrance to a method.</span></span>

```csharp
internal static void Enter(TraceSource traceSource, object obj, string method, object paramObject)
```

### <a name="parameters"></a><span data-ttu-id="3a41c-129">参数</span><span class="sxs-lookup"><span data-stu-id="3a41c-129">Parameters</span></span>

- <span data-ttu-id="3a41c-130">`traceSource` <xref:System.Diagnostics.TraceSource></span><span class="sxs-lookup"><span data-stu-id="3a41c-130">`traceSource` <xref:System.Diagnostics.TraceSource></span></span>

  <span data-ttu-id="3a41c-131">要将事件记录到的跟踪源。</span><span class="sxs-lookup"><span data-stu-id="3a41c-131">The trace source to log the event to.</span></span>

- <span data-ttu-id="3a41c-132">`obj` <xref:System.Object></span><span class="sxs-lookup"><span data-stu-id="3a41c-132">`obj` <xref:System.Object></span></span>

  <span data-ttu-id="3a41c-133">在其上调用方法的对象。</span><span class="sxs-lookup"><span data-stu-id="3a41c-133">The object that the method was called on.</span></span>

- <span data-ttu-id="3a41c-134">`method` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-134">`method` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-135">正在输入的方法。</span><span class="sxs-lookup"><span data-stu-id="3a41c-135">The method that is being entered.</span></span>

- <span data-ttu-id="3a41c-136">`paramObject` <xref:System.Object></span><span class="sxs-lookup"><span data-stu-id="3a41c-136">`paramObject` <xref:System.Object></span></span>

  <span data-ttu-id="3a41c-137">传递给方法的参数。</span><span class="sxs-lookup"><span data-stu-id="3a41c-137">The parameters that were passed to the method.</span></span>

## <a name="entertracesource-string-string-string-method"></a><span data-ttu-id="3a41c-138">输入 (TraceSource、string、string、string) 方法</span><span class="sxs-lookup"><span data-stu-id="3a41c-138">Enter(TraceSource, string, string, string) method</span></span>

<span data-ttu-id="3a41c-139">日志进入到方法。</span><span class="sxs-lookup"><span data-stu-id="3a41c-139">Logs entrance to a method.</span></span>

```csharp
internal static void Enter(TraceSource traceSource, string obj, string method, string param)
```

### <a name="parameters"></a><span data-ttu-id="3a41c-140">参数</span><span class="sxs-lookup"><span data-stu-id="3a41c-140">Parameters</span></span>

- <span data-ttu-id="3a41c-141">`traceSource` <xref:System.Diagnostics.TraceSource></span><span class="sxs-lookup"><span data-stu-id="3a41c-141">`traceSource` <xref:System.Diagnostics.TraceSource></span></span>

  <span data-ttu-id="3a41c-142">要将事件记录到的跟踪源。</span><span class="sxs-lookup"><span data-stu-id="3a41c-142">The trace source to log the event to.</span></span>

- <span data-ttu-id="3a41c-143">`obj` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-143">`obj` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-144">在其上调用方法的对象。</span><span class="sxs-lookup"><span data-stu-id="3a41c-144">The object that the method was called on.</span></span>

- <span data-ttu-id="3a41c-145">`method` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-145">`method` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-146">正在输入的方法。</span><span class="sxs-lookup"><span data-stu-id="3a41c-146">The method that is being entered.</span></span>

- <span data-ttu-id="3a41c-147">`param` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-147">`param` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-148">传递给方法的参数。</span><span class="sxs-lookup"><span data-stu-id="3a41c-148">The parameters that were passed to the method.</span></span>

## <a name="entertracesource-string-string-object-method"></a><span data-ttu-id="3a41c-149">输入 (TraceSource、string、string、object) 方法</span><span class="sxs-lookup"><span data-stu-id="3a41c-149">Enter(TraceSource, string, string, object) method</span></span>

<span data-ttu-id="3a41c-150">日志进入到方法。</span><span class="sxs-lookup"><span data-stu-id="3a41c-150">Logs entrance to a method.</span></span>

```csharp
internal static void Enter(TraceSource traceSource, string obj, string method, object paramObject)
```

### <a name="parameters"></a><span data-ttu-id="3a41c-151">参数</span><span class="sxs-lookup"><span data-stu-id="3a41c-151">Parameters</span></span>

- <span data-ttu-id="3a41c-152">`traceSource` <xref:System.Diagnostics.TraceSource></span><span class="sxs-lookup"><span data-stu-id="3a41c-152">`traceSource` <xref:System.Diagnostics.TraceSource></span></span>

  <span data-ttu-id="3a41c-153">要将事件记录到的跟踪源。</span><span class="sxs-lookup"><span data-stu-id="3a41c-153">The trace source to log the event to.</span></span>

- <span data-ttu-id="3a41c-154">`obj` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-154">`obj` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-155">在其上调用方法的对象。</span><span class="sxs-lookup"><span data-stu-id="3a41c-155">The object that the method was called on.</span></span>

- <span data-ttu-id="3a41c-156">`method` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-156">`method` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-157">正在输入的方法。</span><span class="sxs-lookup"><span data-stu-id="3a41c-157">The method that is being entered.</span></span>

- <span data-ttu-id="3a41c-158">`paramObject` <xref:System.Object></span><span class="sxs-lookup"><span data-stu-id="3a41c-158">`paramObject` <xref:System.Object></span></span>

  <span data-ttu-id="3a41c-159">传递给方法的参数。</span><span class="sxs-lookup"><span data-stu-id="3a41c-159">The parameters that were passed to the method.</span></span>

## <a name="entertracesource-string-string-method"></a><span data-ttu-id="3a41c-160">输入 (TraceSource、string、string) 方法</span><span class="sxs-lookup"><span data-stu-id="3a41c-160">Enter(TraceSource, string, string) method</span></span>

<span data-ttu-id="3a41c-161">日志进入到方法。</span><span class="sxs-lookup"><span data-stu-id="3a41c-161">Logs entrance to a method.</span></span>

```csharp
internal static void Enter(TraceSource traceSource, string method, string parameters)
```

### <a name="parameters"></a><span data-ttu-id="3a41c-162">参数</span><span class="sxs-lookup"><span data-stu-id="3a41c-162">Parameters</span></span>

- <span data-ttu-id="3a41c-163">`traceSource` <xref:System.Diagnostics.TraceSource></span><span class="sxs-lookup"><span data-stu-id="3a41c-163">`traceSource` <xref:System.Diagnostics.TraceSource></span></span>

  <span data-ttu-id="3a41c-164">要将事件记录到的跟踪源。</span><span class="sxs-lookup"><span data-stu-id="3a41c-164">The trace source to log the event to.</span></span>

- <span data-ttu-id="3a41c-165">`method` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-165">`method` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-166">正在输入的方法。</span><span class="sxs-lookup"><span data-stu-id="3a41c-166">The method that is being entered.</span></span>

- <span data-ttu-id="3a41c-167">`parameters` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-167">`parameters` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-168">传递给方法的参数。</span><span class="sxs-lookup"><span data-stu-id="3a41c-168">The parameters that were passed to the method.</span></span>

## <a name="entertracesource-string-method"></a><span data-ttu-id="3a41c-169">输入 (TraceSource，string) 方法</span><span class="sxs-lookup"><span data-stu-id="3a41c-169">Enter(TraceSource, string) method</span></span>

<span data-ttu-id="3a41c-170">日志进入到方法。</span><span class="sxs-lookup"><span data-stu-id="3a41c-170">Logs entrance to a method.</span></span>

```csharp
internal static void Enter(TraceSource traceSource, string msg)
```

### <a name="parameters"></a><span data-ttu-id="3a41c-171">参数</span><span class="sxs-lookup"><span data-stu-id="3a41c-171">Parameters</span></span>

- <span data-ttu-id="3a41c-172">`traceSource` <xref:System.Diagnostics.TraceSource></span><span class="sxs-lookup"><span data-stu-id="3a41c-172">`traceSource` <xref:System.Diagnostics.TraceSource></span></span>

  <span data-ttu-id="3a41c-173">要将事件记录到的跟踪源。</span><span class="sxs-lookup"><span data-stu-id="3a41c-173">The trace source to log the event to.</span></span>

- <span data-ttu-id="3a41c-174">`msg` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-174">`msg` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-175">要记录到跟踪源的入口消息。</span><span class="sxs-lookup"><span data-stu-id="3a41c-175">The entrance message to log to the trace source.</span></span>

## <a name="exception-method"></a><span data-ttu-id="3a41c-176">Exception 方法</span><span class="sxs-lookup"><span data-stu-id="3a41c-176">Exception method</span></span>

<span data-ttu-id="3a41c-177">记录异常并还原缩进。</span><span class="sxs-lookup"><span data-stu-id="3a41c-177">Logs an exception and restores indentation.</span></span>

```csharp
internal static void Exception(TraceSource traceSource, object obj, string method, Exception e)
```

### <a name="parameters"></a><span data-ttu-id="3a41c-178">参数</span><span class="sxs-lookup"><span data-stu-id="3a41c-178">Parameters</span></span>

- <span data-ttu-id="3a41c-179">`traceSource` <xref:System.Diagnostics.TraceSource></span><span class="sxs-lookup"><span data-stu-id="3a41c-179">`traceSource` <xref:System.Diagnostics.TraceSource></span></span>

  <span data-ttu-id="3a41c-180">要将事件记录到的跟踪源。</span><span class="sxs-lookup"><span data-stu-id="3a41c-180">The trace source to log the event to.</span></span>

- <span data-ttu-id="3a41c-181">`obj` <xref:System.Object></span><span class="sxs-lookup"><span data-stu-id="3a41c-181">`obj` <xref:System.Object></span></span>

  <span data-ttu-id="3a41c-182">调用了引发异常的方法的对象。</span><span class="sxs-lookup"><span data-stu-id="3a41c-182">The object that the method that threw an exception was called on.</span></span>

- <span data-ttu-id="3a41c-183">`method` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-183">`method` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-184">引发异常的方法。</span><span class="sxs-lookup"><span data-stu-id="3a41c-184">The method that threw the exception.</span></span>

- <span data-ttu-id="3a41c-185">`e` <xref:System.Exception></span><span class="sxs-lookup"><span data-stu-id="3a41c-185">`e` <xref:System.Exception></span></span>

  <span data-ttu-id="3a41c-186">抛出的异常。</span><span class="sxs-lookup"><span data-stu-id="3a41c-186">The exception that was thrown.</span></span>

## <a name="exittracesource-object-string-object-method"></a><span data-ttu-id="3a41c-187">Exit (TraceSource、object、string、object) 方法</span><span class="sxs-lookup"><span data-stu-id="3a41c-187">Exit(TraceSource, object, string, object) method</span></span>

<span data-ttu-id="3a41c-188">日志从函数退出。</span><span class="sxs-lookup"><span data-stu-id="3a41c-188">Logs exit from a function.</span></span>

```csharp
internal static void Exit(TraceSource traceSource, object obj, string method, object retObject)
```

### <a name="parameters"></a><span data-ttu-id="3a41c-189">参数</span><span class="sxs-lookup"><span data-stu-id="3a41c-189">Parameters</span></span>

- <span data-ttu-id="3a41c-190">`traceSource` <xref:System.Diagnostics.TraceSource></span><span class="sxs-lookup"><span data-stu-id="3a41c-190">`traceSource` <xref:System.Diagnostics.TraceSource></span></span>

  <span data-ttu-id="3a41c-191">要将事件记录到的跟踪源。</span><span class="sxs-lookup"><span data-stu-id="3a41c-191">The trace source to log the event to.</span></span>

- <span data-ttu-id="3a41c-192">`obj` <xref:System.Object></span><span class="sxs-lookup"><span data-stu-id="3a41c-192">`obj` <xref:System.Object></span></span>

  <span data-ttu-id="3a41c-193">在其上调用方法的对象。</span><span class="sxs-lookup"><span data-stu-id="3a41c-193">The object that the method was called on.</span></span>

- <span data-ttu-id="3a41c-194">`method` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-194">`method` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-195">正在退出的方法。</span><span class="sxs-lookup"><span data-stu-id="3a41c-195">The method that is being exited.</span></span>

- <span data-ttu-id="3a41c-196">`retObject` <xref:System.Object></span><span class="sxs-lookup"><span data-stu-id="3a41c-196">`retObject` <xref:System.Object></span></span>

  <span data-ttu-id="3a41c-197">由方法返回的值。</span><span class="sxs-lookup"><span data-stu-id="3a41c-197">The value that's being returned by the method.</span></span>

## <a name="exittracesource-string-string-object-method"></a><span data-ttu-id="3a41c-198">Exit (TraceSource、string、string、object) 方法</span><span class="sxs-lookup"><span data-stu-id="3a41c-198">Exit(TraceSource, string, string, object) method</span></span>

<span data-ttu-id="3a41c-199">日志从函数退出。</span><span class="sxs-lookup"><span data-stu-id="3a41c-199">Logs exit from a function.</span></span>

```csharp
internal static void Exit(TraceSource traceSource, string obj, string method, object retObject)
```

### <a name="parameters"></a><span data-ttu-id="3a41c-200">参数</span><span class="sxs-lookup"><span data-stu-id="3a41c-200">Parameters</span></span>

- <span data-ttu-id="3a41c-201">`traceSource` <xref:System.Diagnostics.TraceSource></span><span class="sxs-lookup"><span data-stu-id="3a41c-201">`traceSource` <xref:System.Diagnostics.TraceSource></span></span>

  <span data-ttu-id="3a41c-202">要将事件记录到的跟踪源。</span><span class="sxs-lookup"><span data-stu-id="3a41c-202">The trace source to log the event to.</span></span>

- <span data-ttu-id="3a41c-203">`obj` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-203">`obj` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-204">在其上调用方法的对象。</span><span class="sxs-lookup"><span data-stu-id="3a41c-204">The object that the method was called on.</span></span>

- <span data-ttu-id="3a41c-205">`method` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-205">`method` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-206">正在退出的方法。</span><span class="sxs-lookup"><span data-stu-id="3a41c-206">The method that is being exited.</span></span>

- <span data-ttu-id="3a41c-207">`retObject` <xref:System.Object></span><span class="sxs-lookup"><span data-stu-id="3a41c-207">`retObject` <xref:System.Object></span></span>

  <span data-ttu-id="3a41c-208">由方法返回的值。</span><span class="sxs-lookup"><span data-stu-id="3a41c-208">The value that's being returned by the method.</span></span>

## <a name="exittracesource-object-string-string-method"></a><span data-ttu-id="3a41c-209">Exit (TraceSource、object、string、string) 方法</span><span class="sxs-lookup"><span data-stu-id="3a41c-209">Exit(TraceSource, object, string, string) method</span></span>

<span data-ttu-id="3a41c-210">日志从函数退出。</span><span class="sxs-lookup"><span data-stu-id="3a41c-210">Logs exit from a function.</span></span>

```csharp
internal static void Exit(TraceSource traceSource, object obj, string method, string retValue)
```

### <a name="parameters"></a><span data-ttu-id="3a41c-211">参数</span><span class="sxs-lookup"><span data-stu-id="3a41c-211">Parameters</span></span>

- <span data-ttu-id="3a41c-212">`traceSource` <xref:System.Diagnostics.TraceSource></span><span class="sxs-lookup"><span data-stu-id="3a41c-212">`traceSource` <xref:System.Diagnostics.TraceSource></span></span>

  <span data-ttu-id="3a41c-213">要将事件记录到的跟踪源。</span><span class="sxs-lookup"><span data-stu-id="3a41c-213">The trace source to log the event to.</span></span>

- <span data-ttu-id="3a41c-214">`obj` <xref:System.Object></span><span class="sxs-lookup"><span data-stu-id="3a41c-214">`obj` <xref:System.Object></span></span>

  <span data-ttu-id="3a41c-215">在其上调用方法的对象。</span><span class="sxs-lookup"><span data-stu-id="3a41c-215">The object that the method was called on.</span></span>

- <span data-ttu-id="3a41c-216">`method` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-216">`method` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-217">正在退出的方法。</span><span class="sxs-lookup"><span data-stu-id="3a41c-217">The method that is being exited.</span></span>

- <span data-ttu-id="3a41c-218">`retValue` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-218">`retValue` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-219">由方法返回的值。</span><span class="sxs-lookup"><span data-stu-id="3a41c-219">The value that's being returned by the method.</span></span>

## <a name="exittracesource-string-string-string-method"></a><span data-ttu-id="3a41c-220">Exit (TraceSource、string、string、string) 方法</span><span class="sxs-lookup"><span data-stu-id="3a41c-220">Exit(TraceSource, string, string, string) method</span></span>

<span data-ttu-id="3a41c-221">日志从函数退出。</span><span class="sxs-lookup"><span data-stu-id="3a41c-221">Logs exit from a function.</span></span>

```csharp
internal static void Exit(TraceSource traceSource, string obj, string method, string retValue)
```

### <a name="parameters"></a><span data-ttu-id="3a41c-222">参数</span><span class="sxs-lookup"><span data-stu-id="3a41c-222">Parameters</span></span>

- <span data-ttu-id="3a41c-223">`traceSource` <xref:System.Diagnostics.TraceSource></span><span class="sxs-lookup"><span data-stu-id="3a41c-223">`traceSource` <xref:System.Diagnostics.TraceSource></span></span>

  <span data-ttu-id="3a41c-224">要将事件记录到的跟踪源。</span><span class="sxs-lookup"><span data-stu-id="3a41c-224">The trace source to log the event to.</span></span>

- <span data-ttu-id="3a41c-225">`obj` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-225">`obj` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-226">在其上调用方法的对象。</span><span class="sxs-lookup"><span data-stu-id="3a41c-226">The object that the method was called on.</span></span>

- <span data-ttu-id="3a41c-227">`method` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-227">`method` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-228">正在退出的方法。</span><span class="sxs-lookup"><span data-stu-id="3a41c-228">The method that is being exited.</span></span>

- <span data-ttu-id="3a41c-229">`retValue` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-229">`retValue` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-230">由方法返回的值。</span><span class="sxs-lookup"><span data-stu-id="3a41c-230">The value that's being returned by the method.</span></span>

## <a name="exittracesource-string-string-method"></a><span data-ttu-id="3a41c-231">Exit (TraceSource、string、string) 方法</span><span class="sxs-lookup"><span data-stu-id="3a41c-231">Exit(TraceSource, string, string) method</span></span>

<span data-ttu-id="3a41c-232">日志从函数退出。</span><span class="sxs-lookup"><span data-stu-id="3a41c-232">Logs exit from a function.</span></span>

```csharp
internal static void Exit(TraceSource traceSource, string method, string parameters)
```

### <a name="parameters"></a><span data-ttu-id="3a41c-233">参数</span><span class="sxs-lookup"><span data-stu-id="3a41c-233">Parameters</span></span>

- <span data-ttu-id="3a41c-234">`traceSource` <xref:System.Diagnostics.TraceSource></span><span class="sxs-lookup"><span data-stu-id="3a41c-234">`traceSource` <xref:System.Diagnostics.TraceSource></span></span>

  <span data-ttu-id="3a41c-235">要将事件记录到的跟踪源。</span><span class="sxs-lookup"><span data-stu-id="3a41c-235">The trace source to log the event to.</span></span>

- <span data-ttu-id="3a41c-236">`method` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-236">`method` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-237">正在退出的方法。</span><span class="sxs-lookup"><span data-stu-id="3a41c-237">The method that is being exited.</span></span>

- <span data-ttu-id="3a41c-238">`parameters` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-238">`parameters` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-239">传递给正在退出的方法的参数。</span><span class="sxs-lookup"><span data-stu-id="3a41c-239">The parameters that were passed to the method that's being exited.</span></span>

## <a name="exittracesource-string-method"></a><span data-ttu-id="3a41c-240">Exit (TraceSource，string) 方法</span><span class="sxs-lookup"><span data-stu-id="3a41c-240">Exit(TraceSource, string) method</span></span>

<span data-ttu-id="3a41c-241">日志从函数退出。</span><span class="sxs-lookup"><span data-stu-id="3a41c-241">Logs exit from a function.</span></span>

```csharp
internal static void Exit(TraceSource traceSource, string msg)
```

### <a name="parameters"></a><span data-ttu-id="3a41c-242">参数</span><span class="sxs-lookup"><span data-stu-id="3a41c-242">Parameters</span></span>

- <span data-ttu-id="3a41c-243">`traceSource` <xref:System.Diagnostics.TraceSource></span><span class="sxs-lookup"><span data-stu-id="3a41c-243">`traceSource` <xref:System.Diagnostics.TraceSource></span></span>

  <span data-ttu-id="3a41c-244">要将事件记录到的跟踪源。</span><span class="sxs-lookup"><span data-stu-id="3a41c-244">The trace source to log the event to.</span></span>

- <span data-ttu-id="3a41c-245">`msg` <xref:System.String></span><span class="sxs-lookup"><span data-stu-id="3a41c-245">`msg` <xref:System.String></span></span>

  <span data-ttu-id="3a41c-246">要记录到跟踪源的退出消息。</span><span class="sxs-lookup"><span data-stu-id="3a41c-246">The exit message to log to the trace source.</span></span>

## <a name="http-property"></a><span data-ttu-id="3a41c-247">Http 属性</span><span class="sxs-lookup"><span data-stu-id="3a41c-247">Http property</span></span>

<span data-ttu-id="3a41c-248">获取 "系统 .Net" 的跟踪源。</span><span class="sxs-lookup"><span data-stu-id="3a41c-248">Gets the trace source for "System.Net.Http".</span></span>

```csharp
internal static TraceSource Http { get; }
```

### <a name="property-value"></a><span data-ttu-id="3a41c-249">属性值</span><span class="sxs-lookup"><span data-stu-id="3a41c-249">Property value</span></span>

<xref:System.Diagnostics.TraceSource>\
<span data-ttu-id="3a41c-250">"系统 .Net" 的跟踪源， `null` 如果未启用日志记录，则为。</span><span class="sxs-lookup"><span data-stu-id="3a41c-250">The trace source for "System.Net.Http", or `null` if logging is not enabled.</span></span>

## <a name="on-property"></a><span data-ttu-id="3a41c-251">On 属性</span><span class="sxs-lookup"><span data-stu-id="3a41c-251">On property</span></span>

<span data-ttu-id="3a41c-252">获取一个值，该值指示是否启用日志记录。</span><span class="sxs-lookup"><span data-stu-id="3a41c-252">Gets a value that indicates whether logging is enabled.</span></span>

```csharp
internal static bool On { get; }
```

### <a name="property-value"></a><span data-ttu-id="3a41c-253">属性值</span><span class="sxs-lookup"><span data-stu-id="3a41c-253">Property value</span></span>

<xref:System.Boolean>\
<span data-ttu-id="3a41c-254">如果启用日志记录，则为 `true`；否则为 `false`。</span><span class="sxs-lookup"><span data-stu-id="3a41c-254">`true` if logging is enabled; otherwise, `false`.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a41c-255">要求</span><span class="sxs-lookup"><span data-stu-id="3a41c-255">Requirements</span></span>

<span data-ttu-id="3a41c-256">**命名空间：** <xref:System.Net></span><span class="sxs-lookup"><span data-stu-id="3a41c-256">**Namespace:** <xref:System.Net></span></span>

<span data-ttu-id="3a41c-257">**程序集：** System.dll 中的系统 () </span><span class="sxs-lookup"><span data-stu-id="3a41c-257">**Assembly:** System (in System.dll)</span></span>
