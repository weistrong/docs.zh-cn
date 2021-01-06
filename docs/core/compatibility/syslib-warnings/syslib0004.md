---
title: SYSLIB0004 警告
description: 了解有关生成编译时警告 SYSLIB0004 的过时信息。
ms.topic: reference
ms.date: 10/20/2020
ms.openlocfilehash: 03be8bb54f71f74ed94ee2c3f8489397ae1e99b5
ms.sourcegitcommit: e301979e3049ce412d19b094c60ed95b316a8f8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/16/2020
ms.locfileid: "97596274"
---
# <a name="syslib0004-the-constrained-execution-region-cer-feature-is-not-supported"></a><span data-ttu-id="43c01-103">SYSLIB0004：不支持受约束的执行区域 (CER) 功能</span><span class="sxs-lookup"><span data-stu-id="43c01-103">SYSLIB0004: The constrained execution region (CER) feature is not supported</span></span>

<span data-ttu-id="43c01-104">[受约束的执行区域 (CER)](../../../framework/performance/constrained-execution-regions.md) 功能仅在 .NET Framework 中受支持。</span><span class="sxs-lookup"><span data-stu-id="43c01-104">The [Constrained execution regions (CER)](../../../framework/performance/constrained-execution-regions.md) feature is supported only in .NET Framework.</span></span> <span data-ttu-id="43c01-105">因此从 .NET 5.0 开始，与 CER 相关的各种 API 标记为已过时。</span><span class="sxs-lookup"><span data-stu-id="43c01-105">As such, various CER-related APIs are marked obsolete, starting in .NET 5.0.</span></span> <span data-ttu-id="43c01-106">使用这些 API 会在编译时生成警告 `SYSLIB0004`。</span><span class="sxs-lookup"><span data-stu-id="43c01-106">Using these APIs generates warning `SYSLIB0004` at compile time.</span></span>

<span data-ttu-id="43c01-107">以下与 CER 相关的 API 已过时：</span><span class="sxs-lookup"><span data-stu-id="43c01-107">The following CER-related APIs are obsolete:</span></span>

- <xref:System.Runtime.CompilerServices.RuntimeHelpers.ExecuteCodeWithGuaranteedCleanup(System.Runtime.CompilerServices.RuntimeHelpers.TryCode,System.Runtime.CompilerServices.RuntimeHelpers.CleanupCode,System.Object)?displayProperty=nameWithType>
- <xref:System.Runtime.CompilerServices.RuntimeHelpers.PrepareConstrainedRegions?displayProperty=nameWithType>
- <xref:System.Runtime.CompilerServices.RuntimeHelpers.PrepareConstrainedRegionsNoOP?displayProperty=nameWithType>
- <xref:System.Runtime.CompilerServices.RuntimeHelpers.PrepareContractedDelegate(System.Delegate)?displayProperty=nameWithType>
- <xref:System.Runtime.CompilerServices.RuntimeHelpers.ProbeForSufficientStack?displayProperty=nameWithType>
- <xref:System.Runtime.ConstrainedExecution.Cer?displayProperty=nameWithType>
- <xref:System.Runtime.ConstrainedExecution.Consistency?displayProperty=nameWithType>
- <xref:System.Runtime.ConstrainedExecution.PrePrepareMethodAttribute?displayProperty=nameWithType>
- <xref:System.Runtime.ConstrainedExecution.ReliabilityContractAttribute?displayProperty=nameWithType>

## <a name="workarounds"></a><span data-ttu-id="43c01-108">工作区</span><span class="sxs-lookup"><span data-stu-id="43c01-108">Workarounds</span></span>

- <span data-ttu-id="43c01-109">如果已将 CER 属性应用于方法，请删除该属性。</span><span class="sxs-lookup"><span data-stu-id="43c01-109">If you have applied a CER attribute to a method, remove the attribute.</span></span> <span data-ttu-id="43c01-110">这些属性在 .NET 5.0 和更高版本中无效。</span><span class="sxs-lookup"><span data-stu-id="43c01-110">These attributes have no effect in .NET 5.0 and later versions.</span></span>

  ```csharp
  // REMOVE the attribute below.
  [ReliabilityContract(Consistency.WillNotCorruptState, Cer.Success)]
  public void DoSomething()
  {
  }

  // REMOVE the attribute below.
  [PrePrepareMethod]
  public void DoSomething()
  {
  }
  ```

- <span data-ttu-id="43c01-111">如果调用 `RuntimeHelpers.ProbeForSufficientStack` 或 `RuntimeHelpers.PrepareContractedDelegate`，请删除该调用。</span><span class="sxs-lookup"><span data-stu-id="43c01-111">If you are calling `RuntimeHelpers.ProbeForSufficientStack` or `RuntimeHelpers.PrepareContractedDelegate`, remove the call.</span></span> <span data-ttu-id="43c01-112">这些调用在 .NET 5.0 和更高版本中无效。</span><span class="sxs-lookup"><span data-stu-id="43c01-112">These calls have no effect in .NET 5.0 and later versions.</span></span>

  ```csharp
  public void DoSomething()
  {
      // REMOVE the call below.
      RuntimeHelpers.ProbeForSufficientStack();

      // (Remainder of your method logic here.)
  }
  ```

- <span data-ttu-id="43c01-113">如果要调用 `RuntimeHelpers.PrepareConstrainedRegions`，请删除该调用。</span><span class="sxs-lookup"><span data-stu-id="43c01-113">If you are calling `RuntimeHelpers.PrepareConstrainedRegions`, remove the call.</span></span> <span data-ttu-id="43c01-114">该调用在 .NET 5.0 和更高版本中无效。</span><span class="sxs-lookup"><span data-stu-id="43c01-114">This call has no effect in .NET 5.0 and later versions.</span></span>

  ```csharp
  public void DoSomething_Old()
  {
      // REMOVE the call below.
      RuntimeHelpers.PrepareConstrainedRegions();
      try
      {
          // try code
      }
      finally
      {
          // cleanup code
      }
  }

  public void DoSomething_Corrected()
  {
      // There is no call to PrepareConstrainedRegions. It's a normal try / finally block.

      try
      {
          // try code
      }
      finally
      {
          // cleanup code
      }
  }
  ```

- <span data-ttu-id="43c01-115">如果调用 `RuntimeHelpers.ExecuteCodeWithGuaranteedCleanup`，请将调用替换为标准 try / catch / finall 块。</span><span class="sxs-lookup"><span data-stu-id="43c01-115">If you are calling `RuntimeHelpers.ExecuteCodeWithGuaranteedCleanup`, replace the call with a standard _try / catch / finally_ block.</span></span>

  ```csharp
  // The sample below produces warning SYSLIB0004.
  public void DoSomething_Old()
  {
      RuntimeHelpers.ExecuteCodeWithGuaranteedCleanup(MyTryCode, MyCleanupCode, null);
  }
  public void MyTryCode(object state) { /* try code */ }
  public void MyCleanupCode(object state, bool exceptionThrown) { /* cleanup code */ }

  // The corrected sample below does not produce warning SYSLIB0004.
  public void DoSomething_Corrected()
  {
      try
      {
          // try code
      }
      catch (Exception ex)
      {
          // exception handling code
      }
      finally
      {
          // cleanup code
      }
  }
  ```

[!INCLUDE [suppress-syslib-warning](../../../../includes/suppress-syslib-warning.md)]

## <a name="see-also"></a><span data-ttu-id="43c01-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="43c01-116">See also</span></span>

- [<span data-ttu-id="43c01-117">受约束的执行区域</span><span class="sxs-lookup"><span data-stu-id="43c01-117">Constrained execution regions</span></span>](../../../framework/performance/constrained-execution-regions.md)
