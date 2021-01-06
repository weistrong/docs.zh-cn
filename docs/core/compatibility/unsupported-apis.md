---
title: .NET Core 和 .NET 5+ 上不支持的 API
titleSuffix: ''
description: 了解哪些 .NET API 始终在 .NET Core 和 .NET 5.0 及更高版本上引发异常。
ms.date: 10/13/2020
ms.openlocfilehash: 1bd41192d0d6752d2b659da9fb6387dac321b2c3
ms.sourcegitcommit: e301979e3049ce412d19b094c60ed95b316a8f8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/16/2020
ms.locfileid: "97593261"
---
# <a name="apis-that-always-throw-exceptions-on-net-core-and-net-5"></a><span data-ttu-id="cf1a1-103">始终在 .NET Core 和 .NET 5+ 上引发异常的 API</span><span class="sxs-lookup"><span data-stu-id="cf1a1-103">APIs that always throw exceptions on .NET Core and .NET 5+</span></span>

<span data-ttu-id="cf1a1-104">以下 API 将始终在所有或部分平台上的 .NET 5.0 及更高版本（包括所有 .NET Core 版本）中引发 <xref:System.PlatformNotSupportedException>。</span><span class="sxs-lookup"><span data-stu-id="cf1a1-104">The following APIs will always throw a <xref:System.PlatformNotSupportedException> on .NET 5.0 and later versions (including all versions of .NET Core) on all or a subset of platforms.</span></span>

<span data-ttu-id="cf1a1-105">本文按命名空间组织受影响的 API。</span><span class="sxs-lookup"><span data-stu-id="cf1a1-105">This article organizes the affected APIs by namespace.</span></span>

> [!NOTE]
>
> - <span data-ttu-id="cf1a1-106">本文是当前正在进行的工作。</span><span class="sxs-lookup"><span data-stu-id="cf1a1-106">This article is a work-in-progress.</span></span> <span data-ttu-id="cf1a1-107">它不是在 .NET 5+ 上引发异常的 API 的完整列表。</span><span class="sxs-lookup"><span data-stu-id="cf1a1-107">It is not a complete list of APIs that throw exceptions on .NET 5+.</span></span>
> - <span data-ttu-id="cf1a1-108">本文不包括在 .NET 5+ 上引发的二进制序列化的显式接口实现。</span><span class="sxs-lookup"><span data-stu-id="cf1a1-108">This article does not include the explicit interface implementations for binary serialization that throw on .NET 5+.</span></span> <span data-ttu-id="cf1a1-109">有关详细信息，请参阅 [.NET Core 中的二进制序列化](../../standard/serialization/binary-serialization.md#net-core)。</span><span class="sxs-lookup"><span data-stu-id="cf1a1-109">For more information, see [Binary serialization in .NET Core](../../standard/serialization/binary-serialization.md#net-core).</span></span>

## <a name="system"></a><span data-ttu-id="cf1a1-110">系统</span><span class="sxs-lookup"><span data-stu-id="cf1a1-110">System</span></span>

| <span data-ttu-id="cf1a1-111">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-111">Member</span></span> | <span data-ttu-id="cf1a1-112">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-112">Platforms that throw</span></span> |
| - | - |
| <xref:System.AppDomain.CreateDomain%2A?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-113">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-113">All</span></span> |
| <xref:System.AppDomain.ExecuteAssembly(System.String,System.String[],System.Byte[],System.Configuration.Assemblies.AssemblyHashAlgorithm)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-114">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-114">All</span></span> |
| <xref:System.Console.CapsLock?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-115">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-115">Linux and macOS</span></span> |
| <xref:System.Console.NumberLock?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-116">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-116">Linux and macOS</span></span> |
| <xref:System.Delegate.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-117">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-117">All</span></span> |
| <xref:System.Exception.SerializeObjectState?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-118">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-118">All</span></span> |
| <xref:System.MarshalByRefObject.GetLifetimeService?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-119">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-119">All</span></span> |
| <xref:System.MarshalByRefObject.InitializeLifetimeService?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-120">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-120">All</span></span> |
| <xref:System.OperatingSystem.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-121">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-121">All</span></span> |
| <xref:System.Type.ReflectionOnlyGetType(System.String,System.Boolean,System.Boolean)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-122">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-122">All</span></span> |

## <a name="systemcodedomcompiler"></a><span data-ttu-id="cf1a1-123">System.CodeDom.Compiler</span><span class="sxs-lookup"><span data-stu-id="cf1a1-123">System.CodeDom.Compiler</span></span>

| <span data-ttu-id="cf1a1-124">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-124">Member</span></span> | <span data-ttu-id="cf1a1-125">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-125">Platforms that throw</span></span> |
| - | - |
| <xref:System.CodeDom.Compiler.CodeDomProvider.CompileAssemblyFromDom%2A?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-126">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-126">All</span></span> |
| <xref:System.CodeDom.Compiler.CodeDomProvider.CompileAssemblyFromFile%2A?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-127">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-127">All</span></span> |
| <xref:System.CodeDom.Compiler.CodeDomProvider.CompileAssemblyFromSource%2A?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-128">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-128">All</span></span> |

## <a name="systemcollectionsspecialized"></a><span data-ttu-id="cf1a1-129">System.Collections.Specialized</span><span class="sxs-lookup"><span data-stu-id="cf1a1-129">System.Collections.Specialized</span></span>

| <span data-ttu-id="cf1a1-130">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-130">Member</span></span> | <span data-ttu-id="cf1a1-131">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-131">Platforms that throw</span></span> |
| - | - |
| <xref:System.Collections.Specialized.NameObjectCollectionBase.%23ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)> | <span data-ttu-id="cf1a1-132">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-132">All</span></span> |
| <xref:System.Collections.Specialized.NameObjectCollectionBase.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-133">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-133">All</span></span> |
| <xref:System.Collections.Specialized.NameObjectCollectionBase.OnDeserialization(System.Object)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-134">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-134">All</span></span> |

## <a name="systemconfiguration"></a><span data-ttu-id="cf1a1-135">System.Configuration</span><span class="sxs-lookup"><span data-stu-id="cf1a1-135">System.Configuration</span></span>

| <span data-ttu-id="cf1a1-136">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-136">Member</span></span> | <span data-ttu-id="cf1a1-137">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-137">Platforms that throw</span></span> |
| - | - |
| <span data-ttu-id="cf1a1-138"><xref:System.Configuration.RsaProtectedConfigurationProvider?displayProperty=nameWithType>（所有成员）</span><span class="sxs-lookup"><span data-stu-id="cf1a1-138"><xref:System.Configuration.RsaProtectedConfigurationProvider?displayProperty=nameWithType> (all members)</span></span> | <span data-ttu-id="cf1a1-139">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-139">All</span></span> |

## <a name="systemconsole"></a><span data-ttu-id="cf1a1-140">System.Console</span><span class="sxs-lookup"><span data-stu-id="cf1a1-140">System.Console</span></span>

| <span data-ttu-id="cf1a1-141">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-141">Member</span></span> | <span data-ttu-id="cf1a1-142">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-142">Platforms that throw</span></span> |
| - | - |
| <xref:System.Console.Beep?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-143">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-143">Linux and macOS</span></span> |
| <span data-ttu-id="cf1a1-144"><xref:System.Console.BufferHeight?displayProperty=nameWithType>（仅设置）</span><span class="sxs-lookup"><span data-stu-id="cf1a1-144"><xref:System.Console.BufferHeight?displayProperty=nameWithType> (set only)</span></span> | <span data-ttu-id="cf1a1-145">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-145">Linux and macOS</span></span> |
| <span data-ttu-id="cf1a1-146"><xref:System.Console.BufferWidth?displayProperty=nameWithType>（仅设置）</span><span class="sxs-lookup"><span data-stu-id="cf1a1-146"><xref:System.Console.BufferWidth?displayProperty=nameWithType> (set only)</span></span> | <span data-ttu-id="cf1a1-147">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-147">Linux and macOS</span></span> |
| <span data-ttu-id="cf1a1-148"><xref:System.Console.CursorSize?displayProperty=nameWithType>（仅设置）</span><span class="sxs-lookup"><span data-stu-id="cf1a1-148"><xref:System.Console.CursorSize?displayProperty=nameWithType> (set only)</span></span> | <span data-ttu-id="cf1a1-149">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-149">Linux and macOS</span></span> |
| <span data-ttu-id="cf1a1-150"><xref:System.Console.CursorVisible?displayProperty=nameWithType>（仅获取）</span><span class="sxs-lookup"><span data-stu-id="cf1a1-150"><xref:System.Console.CursorVisible?displayProperty=nameWithType> (get only)</span></span> | <span data-ttu-id="cf1a1-151">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-151">Linux and macOS</span></span> |
| <xref:System.Console.MoveBufferArea%2A?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-152">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-152">Linux and macOS</span></span> |
| <xref:System.Console.SetWindowPosition%2A?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-153">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-153">Linux and macOS</span></span> |
| <xref:System.Console.SetWindowSize%2A?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-154">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-154">Linux and macOS</span></span> |
| <span data-ttu-id="cf1a1-155"><xref:System.Console.Title?displayProperty=nameWithType>（仅获取）</span><span class="sxs-lookup"><span data-stu-id="cf1a1-155"><xref:System.Console.Title?displayProperty=nameWithType> (get only)</span></span> | <span data-ttu-id="cf1a1-156">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-156">Linux and macOS</span></span> |
| <span data-ttu-id="cf1a1-157"><xref:System.Console.WindowHeight?displayProperty=nameWithType>（仅设置）</span><span class="sxs-lookup"><span data-stu-id="cf1a1-157"><xref:System.Console.WindowHeight?displayProperty=nameWithType> (set only)</span></span> | <span data-ttu-id="cf1a1-158">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-158">Linux and macOS</span></span> |
| <span data-ttu-id="cf1a1-159"><xref:System.Console.WindowLeft?displayProperty=nameWithType>（仅设置）</span><span class="sxs-lookup"><span data-stu-id="cf1a1-159"><xref:System.Console.WindowLeft?displayProperty=nameWithType> (set only)</span></span> | <span data-ttu-id="cf1a1-160">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-160">Linux and macOS</span></span> |
| <span data-ttu-id="cf1a1-161"><xref:System.Console.WindowTop?displayProperty=nameWithType>（仅设置）</span><span class="sxs-lookup"><span data-stu-id="cf1a1-161"><xref:System.Console.WindowTop?displayProperty=nameWithType> (set only)</span></span> | <span data-ttu-id="cf1a1-162">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-162">Linux and macOS</span></span> |
| <span data-ttu-id="cf1a1-163"><xref:System.Console.WindowWidth?displayProperty=nameWithType>（仅设置）</span><span class="sxs-lookup"><span data-stu-id="cf1a1-163"><xref:System.Console.WindowWidth?displayProperty=nameWithType> (set only)</span></span> | <span data-ttu-id="cf1a1-164">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-164">Linux and macOS</span></span> |

## <a name="systemdatacommon"></a><span data-ttu-id="cf1a1-165">System.Data.Common</span><span class="sxs-lookup"><span data-stu-id="cf1a1-165">System.Data.Common</span></span>

| <span data-ttu-id="cf1a1-166">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-166">Member</span></span> | <span data-ttu-id="cf1a1-167">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-167">Platforms that throw</span></span> |
| - | - |
| <span data-ttu-id="cf1a1-168"><xref:System.Data.Common.DbDataReader.GetSchemaTable%2A?displayProperty=nameWithType>（引发 <xref:System.NotSupportedException>）</span><span class="sxs-lookup"><span data-stu-id="cf1a1-168"><xref:System.Data.Common.DbDataReader.GetSchemaTable%2A?displayProperty=nameWithType> (throws <xref:System.NotSupportedException>)</span></span> | <span data-ttu-id="cf1a1-169">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-169">All</span></span> |

## <a name="systemdiagnosticsprocess"></a><span data-ttu-id="cf1a1-170">System.Diagnostics.Process</span><span class="sxs-lookup"><span data-stu-id="cf1a1-170">System.Diagnostics.Process</span></span>

| <span data-ttu-id="cf1a1-171">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-171">Member</span></span> | <span data-ttu-id="cf1a1-172">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-172">Platforms that throw</span></span> |
| - | - |
| <span data-ttu-id="cf1a1-173"><xref:System.Diagnostics.Process.MaxWorkingSet?displayProperty=nameWithType>（仅设置）</span><span class="sxs-lookup"><span data-stu-id="cf1a1-173"><xref:System.Diagnostics.Process.MaxWorkingSet?displayProperty=nameWithType> (set only)</span></span> | <span data-ttu-id="cf1a1-174">Linux</span><span class="sxs-lookup"><span data-stu-id="cf1a1-174">Linux</span></span> |
| <span data-ttu-id="cf1a1-175"><xref:System.Diagnostics.Process.MinWorkingSet?displayProperty=nameWithType>（仅设置）</span><span class="sxs-lookup"><span data-stu-id="cf1a1-175"><xref:System.Diagnostics.Process.MinWorkingSet?displayProperty=nameWithType> (set only)</span></span> | <span data-ttu-id="cf1a1-176">Linux</span><span class="sxs-lookup"><span data-stu-id="cf1a1-176">Linux</span></span> |
| <xref:System.Diagnostics.Process.ProcessorAffinity?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-177">macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-177">macOS</span></span> |
| <xref:System.Diagnostics.Process.MainWindowHandle?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-178">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-178">Linux and macOS</span></span> |
| <xref:System.Diagnostics.Process.Start(System.String,System.String,System.String,System.Security.SecureString,System.String)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-179">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-179">Linux and macOS</span></span> |
| <xref:System.Diagnostics.Process.Start(System.String,System.String,System.Security.SecureString,System.String)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-180">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-180">Linux and macOS</span></span> |
| <xref:System.Diagnostics.ProcessStartInfo.UserName?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-181">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-181">Linux and macOS</span></span> |
| <xref:System.Diagnostics.ProcessStartInfo.PasswordInClearText?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-182">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-182">Linux and macOS</span></span> |
| <xref:System.Diagnostics.ProcessStartInfo.Domain?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-183">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-183">Linux and macOS</span></span> |
| <xref:System.Diagnostics.ProcessStartInfo.LoadUserProfile?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-184">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-184">Linux and macOS</span></span> |
| <span data-ttu-id="cf1a1-185"><xref:System.Diagnostics.ProcessThread.BasePriority?displayProperty=nameWithType>（仅设置）</span><span class="sxs-lookup"><span data-stu-id="cf1a1-185"><xref:System.Diagnostics.ProcessThread.BasePriority?displayProperty=nameWithType> (set only)</span></span> | <span data-ttu-id="cf1a1-186">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-186">Linux and macOS</span></span> |
| <span data-ttu-id="cf1a1-187"><xref:System.Diagnostics.ProcessThread.BasePriority?displayProperty=nameWithType>（仅获取）</span><span class="sxs-lookup"><span data-stu-id="cf1a1-187"><xref:System.Diagnostics.ProcessThread.BasePriority?displayProperty=nameWithType> (get only)</span></span> | <span data-ttu-id="cf1a1-188">macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-188">macOS</span></span> |
| <span data-ttu-id="cf1a1-189"><xref:System.Diagnostics.ProcessThread.ProcessorAffinity?displayProperty=nameWithType>（仅设置）</span><span class="sxs-lookup"><span data-stu-id="cf1a1-189"><xref:System.Diagnostics.ProcessThread.ProcessorAffinity?displayProperty=nameWithType> (set only)</span></span> | <span data-ttu-id="cf1a1-190">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-190">Linux and macOS</span></span> |

## <a name="systemio"></a><span data-ttu-id="cf1a1-191">System.IO</span><span class="sxs-lookup"><span data-stu-id="cf1a1-191">System.IO</span></span>

| <span data-ttu-id="cf1a1-192">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-192">Member</span></span> | <span data-ttu-id="cf1a1-193">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-193">Platforms that throw</span></span> |
| - | - |
| <xref:System.IO.FileSystemInfo.%23ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)> | <span data-ttu-id="cf1a1-194">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-194">All</span></span> |
| <xref:System.IO.FileSystemInfo.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-195">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-195">All</span></span> |

## <a name="systemiopipes"></a><span data-ttu-id="cf1a1-196">System.IO.Pipes</span><span class="sxs-lookup"><span data-stu-id="cf1a1-196">System.IO.Pipes</span></span>

| <span data-ttu-id="cf1a1-197">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-197">Member</span></span> | <span data-ttu-id="cf1a1-198">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-198">Platforms that throw</span></span> |
| - | - |
| <xref:System.IO.Pipes.NamedPipeClientStream.NumberOfServerInstances?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-199">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-199">Linux and macOS</span></span> |
| <xref:System.IO.Pipes.NamedPipeServerStream.GetImpersonationUserName?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-200">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-200">Linux and macOS</span></span> |
| <xref:System.IO.Pipes.PipeStream.InBufferSize?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-201">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-201">Linux and macOS</span></span> |
| <xref:System.IO.Pipes.PipeStream.OutBufferSize?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-202">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-202">Linux and macOS</span></span> |
| <span data-ttu-id="cf1a1-203"><xref:System.IO.Pipes.PipeStream.ReadMode?displayProperty=nameWithType>（仅设置）</span><span class="sxs-lookup"><span data-stu-id="cf1a1-203"><xref:System.IO.Pipes.PipeStream.ReadMode?displayProperty=nameWithType> (set only)</span></span> | <span data-ttu-id="cf1a1-204">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-204">Linux and macOS</span></span> |
| <xref:System.IO.Pipes.PipeStream.WaitForPipeDrain?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-205">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-205">Linux and macOS</span></span> |

## <a name="systemmedia"></a><span data-ttu-id="cf1a1-206">System.Media</span><span class="sxs-lookup"><span data-stu-id="cf1a1-206">System.Media</span></span>

| <span data-ttu-id="cf1a1-207">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-207">Member</span></span> | <span data-ttu-id="cf1a1-208">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-208">Platforms that throw</span></span> |
| - | - |
| <xref:System.Media.SoundPlayer.%23ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)> | <span data-ttu-id="cf1a1-209">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-209">All</span></span> |

## <a name="systemnet"></a><span data-ttu-id="cf1a1-210">System.Net</span><span class="sxs-lookup"><span data-stu-id="cf1a1-210">System.Net</span></span>

| <span data-ttu-id="cf1a1-211">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-211">Member</span></span> | <span data-ttu-id="cf1a1-212">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-212">Platforms that throw</span></span> |
| - | - |
| <xref:System.Net.AuthenticationManager.Authenticate(System.String,System.Net.WebRequest,System.Net.ICredentials)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-213">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-213">All</span></span> |
| <xref:System.Net.AuthenticationManager.PreAuthenticate(System.Net.WebRequest,System.Net.ICredentials)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-214">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-214">All</span></span> |
| <xref:System.Net.FileWebRequest.%23ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)> | <span data-ttu-id="cf1a1-215">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-215">All</span></span> |
| <xref:System.Net.FileWebRequest.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-216">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-216">All</span></span> |
| <xref:System.Net.FileWebResponse.%23ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)> | <span data-ttu-id="cf1a1-217">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-217">All</span></span> |
| <xref:System.Net.FileWebResponse.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-218">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-218">All</span></span> |
| <xref:System.Net.HttpWebRequest.%23ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)> | <span data-ttu-id="cf1a1-219">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-219">All</span></span> |
| <xref:System.Net.HttpWebRequest.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-220">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-220">All</span></span> |
| <xref:System.Net.HttpWebResponse.%23ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)> | <span data-ttu-id="cf1a1-221">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-221">All</span></span> |
| <xref:System.Net.HttpWebResponse.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-222">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-222">All</span></span> |
| <xref:System.Net.WebProxy.%23ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)> | <span data-ttu-id="cf1a1-223">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-223">All</span></span> |
| <xref:System.Net.WebProxy.GetDefaultProxy?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-224">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-224">All</span></span> |
| <xref:System.Net.WebProxy.GetObjectData%2A?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-225">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-225">All</span></span> |
| <xref:System.Net.WebRequest.%23ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)> | <span data-ttu-id="cf1a1-226">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-226">All</span></span> |
| <xref:System.Net.WebRequest.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-227">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-227">All</span></span> |
| <xref:System.Net.WebResponse.%23ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)> | <span data-ttu-id="cf1a1-228">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-228">All</span></span> |
| <xref:System.Net.WebResponse.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-229">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-229">All</span></span> |

## <a name="systemnetnetworkinformation"></a><span data-ttu-id="cf1a1-230">System.Net.NetworkInformation</span><span class="sxs-lookup"><span data-stu-id="cf1a1-230">System.Net.NetworkInformation</span></span>

| <span data-ttu-id="cf1a1-231">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-231">Member</span></span> | <span data-ttu-id="cf1a1-232">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-232">Platforms that throw</span></span> |
| - | - |
| <xref:System.Net.NetworkInformation.Ping.Send%2A?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-233">Windows (UWP)</span><span class="sxs-lookup"><span data-stu-id="cf1a1-233">Windows (UWP)</span></span> |

## <a name="systemnetsockets"></a><span data-ttu-id="cf1a1-234">System.Net.Sockets</span><span class="sxs-lookup"><span data-stu-id="cf1a1-234">System.Net.Sockets</span></span>

| <span data-ttu-id="cf1a1-235">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-235">Member</span></span> | <span data-ttu-id="cf1a1-236">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-236">Platforms that throw</span></span> |
| - | - |
| <xref:System.Net.Sockets.Socket.%23ctor(System.Net.Sockets.SocketInformation)> | <span data-ttu-id="cf1a1-237">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-237">All</span></span> |
| <xref:System.Net.Sockets.Socket.DuplicateAndClose(System.Int32)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-238">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-238">All</span></span> |

## <a name="systemnetwebsockets"></a><span data-ttu-id="cf1a1-239">System.Net.WebSockets</span><span class="sxs-lookup"><span data-stu-id="cf1a1-239">System.Net.WebSockets</span></span>

| <span data-ttu-id="cf1a1-240">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-240">Member</span></span> | <span data-ttu-id="cf1a1-241">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-241">Platforms that throw</span></span> |
| - | - |
| <xref:System.Net.WebSockets.WebSocket.RegisterPrefixes?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-242">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-242">All</span></span> |

## <a name="systemreflection"></a><span data-ttu-id="cf1a1-243">System.Reflection</span><span class="sxs-lookup"><span data-stu-id="cf1a1-243">System.Reflection</span></span>

| <span data-ttu-id="cf1a1-244">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-244">Member</span></span> | <span data-ttu-id="cf1a1-245">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-245">Platforms that throw</span></span> |
| - | - |
| <xref:System.Reflection.Assembly.ReflectionOnlyLoad%2A?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-246">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-246">All</span></span> |
| <xref:System.Reflection.Assembly.ReflectionOnlyLoadFrom(System.String)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-247">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-247">All</span></span> |
| <xref:System.Reflection.AssemblyName.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-248">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-248">All</span></span> |
| <xref:System.Reflection.AssemblyName.OnDeserialization(System.Object)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-249">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-249">All</span></span> |
| <xref:System.Reflection.StrongNameKeyPair.%23ctor(System.String)> | <span data-ttu-id="cf1a1-250">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-250">All</span></span> |
| <xref:System.Reflection.StrongNameKeyPair.%23ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)> | <span data-ttu-id="cf1a1-251">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-251">All</span></span> |
| <xref:System.Reflection.StrongNameKeyPair.PublicKey?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-252">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-252">All</span></span> |

## <a name="systemruntimecompilerservices"></a><span data-ttu-id="cf1a1-253">System.Runtime.CompilerServices</span><span class="sxs-lookup"><span data-stu-id="cf1a1-253">System.Runtime.CompilerServices</span></span>

| <span data-ttu-id="cf1a1-254">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-254">Member</span></span> | <span data-ttu-id="cf1a1-255">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-255">Platforms that throw</span></span> |
| - | - |
| <xref:System.Runtime.CompilerServices.DebugInfoGenerator.CreatePdbGenerator?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-256">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-256">All</span></span> |

## <a name="systemruntimeinteropservices"></a><span data-ttu-id="cf1a1-257">System.Runtime.InteropServices</span><span class="sxs-lookup"><span data-stu-id="cf1a1-257">System.Runtime.InteropServices</span></span>

| <span data-ttu-id="cf1a1-258">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-258">Member</span></span> | <span data-ttu-id="cf1a1-259">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-259">Platforms that throw</span></span> |
| - | - |
| <xref:System.Runtime.InteropServices.Marshal.GetIDispatchForObject(System.Object)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-260">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-260">All</span></span> |
| <xref:System.Runtime.InteropServices.RuntimeEnvironment.SystemConfigurationFile?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-261">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-261">All</span></span> |
| <xref:System.Runtime.InteropServices.RuntimeEnvironment.GetRuntimeInterfaceAsIntPtr(System.Guid,System.Guid)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-262">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-262">All</span></span> |
| <xref:System.Runtime.InteropServices.RuntimeEnvironment.GetRuntimeInterfaceAsObject(System.Guid,System.Guid)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-263">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-263">All</span></span> |
| <xref:System.Runtime.InteropServices.WindowsRuntime.WindowsRuntimeMarshal.StringToHString(System.String)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-264">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-264">Linux and macOS</span></span> |
| <xref:System.Runtime.InteropServices.WindowsRuntime.WindowsRuntimeMarshal.PtrToStringHString(System.IntPtr)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-265">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-265">Linux and macOS</span></span> |
| <xref:System.Runtime.InteropServices.WindowsRuntime.WindowsRuntimeMarshal.FreeHString(System.IntPtr)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-266">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-266">Linux and macOS</span></span> |

## <a name="systemruntimeserialization"></a><span data-ttu-id="cf1a1-267">System.Runtime.Serialization</span><span class="sxs-lookup"><span data-stu-id="cf1a1-267">System.Runtime.Serialization</span></span>

| <span data-ttu-id="cf1a1-268">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-268">Member</span></span> | <span data-ttu-id="cf1a1-269">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-269">Platforms that throw</span></span> |
| - | - |
| <xref:System.Runtime.Serialization.XsdDataContractExporter.Schemas?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-270">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-270">All</span></span> |

## <a name="systemsecurity"></a><span data-ttu-id="cf1a1-271">System.Security</span><span class="sxs-lookup"><span data-stu-id="cf1a1-271">System.Security</span></span>

| <span data-ttu-id="cf1a1-272">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-272">Member</span></span> | <span data-ttu-id="cf1a1-273">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-273">Platforms that throw</span></span> |
| - | - |
| <xref:System.Security.CodeAccessPermission.Deny?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-274">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-274">All</span></span> |
| <xref:System.Security.CodeAccessPermission.PermitOnly?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-275">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-275">All</span></span> |
| <xref:System.Security.PermissionSet.ConvertPermissionSet(System.String,System.Byte[],System.String)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-276">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-276">All</span></span> |
| <xref:System.Security.PermissionSet.Deny?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-277">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-277">All</span></span> |
| <xref:System.Security.PermissionSet.PermitOnly?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-278">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-278">All</span></span> |
| <xref:System.Security.SecurityContext.Capture?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-279">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-279">All</span></span> |
| <xref:System.Security.SecurityContext.CreateCopy?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-280">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-280">All</span></span> |
| <xref:System.Security.SecurityContext.Dispose?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-281">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-281">All</span></span> |
| <xref:System.Security.SecurityContext.IsFlowSuppressed?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-282">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-282">All</span></span> |
| <xref:System.Security.SecurityContext.IsWindowsIdentityFlowSuppressed?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-283">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-283">All</span></span> |
| <xref:System.Security.SecurityContext.RestoreFlow?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-284">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-284">All</span></span> |
| <xref:System.Security.SecurityContext.Run(System.Security.SecurityContext,System.Threading.ContextCallback,System.Object)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-285">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-285">All</span></span> |
| <xref:System.Security.SecurityContext.SuppressFlow?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-286">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-286">All</span></span> |
| <xref:System.Security.SecurityContext.SuppressFlowWindowsIdentity?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-287">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-287">All</span></span> |

## <a name="systemsecurityclaims"></a><span data-ttu-id="cf1a1-288">System.Security.Claims</span><span class="sxs-lookup"><span data-stu-id="cf1a1-288">System.Security.Claims</span></span>

| <span data-ttu-id="cf1a1-289">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-289">Member</span></span> | <span data-ttu-id="cf1a1-290">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-290">Platforms that throw</span></span> |
| - | - |
| <xref:System.Security.Claims.ClaimsPrincipal.%23ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)> | <span data-ttu-id="cf1a1-291">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-291">All</span></span> |
| <xref:System.Security.Claims.ClaimsPrincipal.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-292">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-292">All</span></span> |
| <xref:System.Security.Claims.ClaimsIdentity.%23ctor(System.Runtime.Serialization.SerializationInfo)> | <span data-ttu-id="cf1a1-293">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-293">All</span></span> |
| <xref:System.Security.Claims.ClaimsIdentity.%23ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)> | <span data-ttu-id="cf1a1-294">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-294">All</span></span> |
| <xref:System.Security.Claims.ClaimsIdentity.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-295">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-295">All</span></span> |

## <a name="systemsecuritycryptography"></a><span data-ttu-id="cf1a1-296">System.Security.Cryptography</span><span class="sxs-lookup"><span data-stu-id="cf1a1-296">System.Security.Cryptography</span></span>

| <span data-ttu-id="cf1a1-297">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-297">Member</span></span> | <span data-ttu-id="cf1a1-298">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-298">Platforms that throw</span></span> |
| - | - |
| <xref:System.Security.Cryptography.AsymmetricAlgorithm.Create(System.String)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-299">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-299">All</span></span> |
| <xref:System.Security.Cryptography.CspKeyContainerInfo.%23ctor%2A> | <span data-ttu-id="cf1a1-300">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-300">Linux and macOS</span></span> |
| <xref:System.Security.Cryptography.CspKeyContainerInfo.Accessible?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-301">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-301">Linux and macOS</span></span> |
| <xref:System.Security.Cryptography.CspKeyContainerInfo.Exportable?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-302">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-302">Linux and macOS</span></span> |
| <xref:System.Security.Cryptography.CspKeyContainerInfo.HardwareDevice?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-303">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-303">Linux and macOS</span></span> |
| <xref:System.Security.Cryptography.CspKeyContainerInfo.KeyContainerName?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-304">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-304">Linux and macOS</span></span> |
| <xref:System.Security.Cryptography.CspKeyContainerInfo.KeyNumber?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-305">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-305">Linux and macOS</span></span> |
| <xref:System.Security.Cryptography.CspKeyContainerInfo.MachineKeyStore?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-306">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-306">Linux and macOS</span></span> |
| <xref:System.Security.Cryptography.CspKeyContainerInfo.Protected?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-307">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-307">Linux and macOS</span></span> |
| <xref:System.Security.Cryptography.CspKeyContainerInfo.ProviderName?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-308">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-308">Linux and macOS</span></span> |
| <xref:System.Security.Cryptography.CspKeyContainerInfo.ProviderType?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-309">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-309">Linux and macOS</span></span> |
| <xref:System.Security.Cryptography.CspKeyContainerInfo.RandomlyGenerated?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-310">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-310">Linux and macOS</span></span> |
| <xref:System.Security.Cryptography.CspKeyContainerInfo.Removable?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-311">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-311">Linux and macOS</span></span> |
| <xref:System.Security.Cryptography.CspKeyContainerInfo.UniqueKeyContainerName?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-312">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-312">Linux and macOS</span></span> |
| <xref:System.Security.Cryptography.HashAlgorithm.Create?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-313">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-313">All</span></span> |
| <xref:System.Security.Cryptography.HMAC.Create?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-314">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-314">All</span></span> |
| <xref:System.Security.Cryptography.HMAC.Create(System.String)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-315">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-315">All</span></span> |
| <xref:System.Security.Cryptography.HMAC.HashCore%2A?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-316">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-316">All</span></span> |
| <xref:System.Security.Cryptography.HMAC.HashFinal%2A?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-317">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-317">All</span></span> |
| <xref:System.Security.Cryptography.HMAC.Initialize%2A?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-318">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-318">All</span></span> |
| <xref:System.Security.Cryptography.KeyedHashAlgorithm.Create?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-319">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-319">All</span></span> |
| <xref:System.Security.Cryptography.KeyedHashAlgorithm.Create(System.String)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-320">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-320">All</span></span> |
| <xref:System.Security.Cryptography.ProtectedData.Protect%2A?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-321">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-321">Linux and macOS</span></span> |
| <xref:System.Security.Cryptography.ProtectedData.Unprotect%2A?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-322">Linux 和 macOS</span><span class="sxs-lookup"><span data-stu-id="cf1a1-322">Linux and macOS</span></span> |
| <xref:System.Security.Cryptography.RSA.FromXmlString%2A?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-323">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-323">All</span></span> |
| <xref:System.Security.Cryptography.RSA.ToXmlString%2A?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-324">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-324">All</span></span> |
| <xref:System.Security.Cryptography.SymmetricAlgorithm.Create?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-325">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-325">All</span></span> |
| <xref:System.Security.Cryptography.SymmetricAlgorithm.Create(System.String)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-326">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-326">All</span></span> |

## <a name="systemsecuritycryptographypkcs"></a><span data-ttu-id="cf1a1-327">System.Security.Cryptography.Pkcs</span><span class="sxs-lookup"><span data-stu-id="cf1a1-327">System.Security.Cryptography.Pkcs</span></span>

| <span data-ttu-id="cf1a1-328">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-328">Member</span></span> | <span data-ttu-id="cf1a1-329">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-329">Platforms that throw</span></span> |
| - | - |
| <xref:System.Security.Cryptography.Pkcs.CmsSigner.%23ctor(System.Security.Cryptography.CspParameters)> | <span data-ttu-id="cf1a1-330">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-330">All</span></span> |
| <xref:System.Security.Cryptography.Pkcs.SignerInfo.ComputeCounterSignature?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-331">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-331">All</span></span> |

## <a name="systemsecuritycryptographyx509certificates"></a><span data-ttu-id="cf1a1-332">System.Security.Cryptography.X509Certificates</span><span class="sxs-lookup"><span data-stu-id="cf1a1-332">System.Security.Cryptography.X509Certificates</span></span>

| <span data-ttu-id="cf1a1-333">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-333">Member</span></span> | <span data-ttu-id="cf1a1-334">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-334">Platforms that throw</span></span> |
| - | - |
| <xref:System.Security.Cryptography.X509Certificates.X509Certificate.%23ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)> | <span data-ttu-id="cf1a1-335">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-335">All</span></span> |
| <xref:System.Security.Cryptography.X509Certificates.X509Certificate.Import%2A?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-336">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-336">All</span></span> |
| <xref:System.Security.Cryptography.X509Certificates.X509Certificate2.%23ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)> | <span data-ttu-id="cf1a1-337">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-337">All</span></span> |
| <span data-ttu-id="cf1a1-338"><xref:System.Security.Cryptography.X509Certificates.X509Certificate2.PrivateKey?displayProperty=nameWithType>（仅设置）</span><span class="sxs-lookup"><span data-stu-id="cf1a1-338"><xref:System.Security.Cryptography.X509Certificates.X509Certificate2.PrivateKey?displayProperty=nameWithType> (set only)</span></span> | <span data-ttu-id="cf1a1-339">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-339">All</span></span> |

## <a name="systemsecurityauthenticationextendedprotection"></a><span data-ttu-id="cf1a1-340">System.Security.Authentication.ExtendedProtection</span><span class="sxs-lookup"><span data-stu-id="cf1a1-340">System.Security.Authentication.ExtendedProtection</span></span>

| <span data-ttu-id="cf1a1-341">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-341">Member</span></span> | <span data-ttu-id="cf1a1-342">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-342">Platforms that throw</span></span> |
| - | - |
| <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy.%23ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)> | <span data-ttu-id="cf1a1-343">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-343">All</span></span> |

## <a name="systemsecuritypolicy"></a><span data-ttu-id="cf1a1-344">System.Security.Policy</span><span class="sxs-lookup"><span data-stu-id="cf1a1-344">System.Security.Policy</span></span>

| <span data-ttu-id="cf1a1-345">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-345">Member</span></span> | <span data-ttu-id="cf1a1-346">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-346">Platforms that throw</span></span> |
| - | - |
| <xref:System.Security.Policy.Hash.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-347">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-347">All</span></span> |

## <a name="systemserviceprocessservicecontroller"></a><span data-ttu-id="cf1a1-348">System.ServiceProcess.ServiceController</span><span class="sxs-lookup"><span data-stu-id="cf1a1-348">System.ServiceProcess.ServiceController</span></span>

| <span data-ttu-id="cf1a1-349">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-349">Member</span></span> | <span data-ttu-id="cf1a1-350">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-350">Platforms that throw</span></span> |
| - | - |
| <xref:System.ServiceProcess.TimeoutException.%23ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)> | <span data-ttu-id="cf1a1-351">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-351">All</span></span> |

## <a name="systemtextregularexpressions"></a><span data-ttu-id="cf1a1-352">System.Text.RegularExpressions</span><span class="sxs-lookup"><span data-stu-id="cf1a1-352">System.Text.RegularExpressions</span></span>

| <span data-ttu-id="cf1a1-353">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-353">Member</span></span> | <span data-ttu-id="cf1a1-354">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-354">Platforms that throw</span></span> |
| - | - |
| <xref:System.Text.RegularExpressions.Regex.CompileToAssembly%2A?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-355">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-355">All</span></span> |

## <a name="systemthreading"></a><span data-ttu-id="cf1a1-356">System.Threading</span><span class="sxs-lookup"><span data-stu-id="cf1a1-356">System.Threading</span></span>

| <span data-ttu-id="cf1a1-357">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-357">Member</span></span> | <span data-ttu-id="cf1a1-358">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-358">Platforms that throw</span></span> |
| - | - |
| <xref:System.Threading.CompressedStack.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-359">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-359">All</span></span> |
| <xref:System.Threading.ExecutionContext.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-360">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-360">All</span></span> |
| <xref:System.Threading.Thread.Abort%2A?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-361">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-361">All</span></span> |
| <xref:System.Threading.Thread.ResetAbort?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-362">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-362">All</span></span> |
| <xref:System.Threading.Thread.Resume?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-363">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-363">All</span></span> |
| <xref:System.Threading.Thread.Suspend?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-364">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-364">All</span></span> |

## <a name="systemxml"></a><span data-ttu-id="cf1a1-365">System.Xml</span><span class="sxs-lookup"><span data-stu-id="cf1a1-365">System.Xml</span></span>

| <span data-ttu-id="cf1a1-366">成员</span><span class="sxs-lookup"><span data-stu-id="cf1a1-366">Member</span></span> | <span data-ttu-id="cf1a1-367">引发异常的平台</span><span class="sxs-lookup"><span data-stu-id="cf1a1-367">Platforms that throw</span></span> |
| - | - |
| <xref:System.Xml.XmlDictionaryReader.CreateMtomReader(System.Byte[],System.Int32,System.Int32,System.Text.Encoding[],System.String,System.Xml.XmlDictionaryReaderQuotas,System.Int32,System.Xml.OnXmlDictionaryReaderClose)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-368">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-368">All</span></span> |
| <xref:System.Xml.XmlDictionaryReader.CreateMtomReader(System.IO.Stream,System.Text.Encoding[],System.String,System.Xml.XmlDictionaryReaderQuotas,System.Int32,System.Xml.OnXmlDictionaryReaderClose)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-369">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-369">All</span></span> |
| <xref:System.Xml.XmlDictionaryWriter.CreateMtomWriter(System.IO.Stream,System.Text.Encoding,System.Int32,System.String,System.String,System.String,System.Boolean,System.Boolean)?displayProperty=nameWithType> | <span data-ttu-id="cf1a1-370">All</span><span class="sxs-lookup"><span data-stu-id="cf1a1-370">All</span></span> |

## <a name="see-also"></a><span data-ttu-id="cf1a1-371">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cf1a1-371">See also</span></span>

- [<span data-ttu-id="cf1a1-372">从 .NET Framework 迁移到 .NET Core 的中断性变更</span><span class="sxs-lookup"><span data-stu-id="cf1a1-372">Breaking changes for migration from .NET Framework to .NET Core</span></span>](fx-core.md)
- [<span data-ttu-id="cf1a1-373">.NET Core 中的二进制序列化</span><span class="sxs-lookup"><span data-stu-id="cf1a1-373">Binary serialization in .NET Core</span></span>](../../standard/serialization/binary-serialization.md#net-core)
- [<span data-ttu-id="cf1a1-374">.NET 可移植性分析器</span><span class="sxs-lookup"><span data-stu-id="cf1a1-374">.NET portability analyzer</span></span>](../../standard/analyzers/portability-analyzer.md)
