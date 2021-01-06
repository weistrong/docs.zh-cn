---
title: SYSLIB0001 警告
description: 了解有关生成编译时警告 SYSLIB0001 的过时信息。
ms.topic: reference
ms.date: 10/20/2020
ms.openlocfilehash: 6c4b6a2f41e9dc044ef76bb5a53a4a54a44bca5a
ms.sourcegitcommit: e301979e3049ce412d19b094c60ed95b316a8f8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/16/2020
ms.locfileid: "97596293"
---
# <a name="syslib0001-the-utf-7-encoding-is-insecure"></a><span data-ttu-id="f060b-103">SYSLIB0001：UTF-7 编码不安全</span><span class="sxs-lookup"><span data-stu-id="f060b-103">SYSLIB0001: The UTF-7 encoding is insecure</span></span>

<span data-ttu-id="f060b-104">UTF-7 编码在应用程序中不再广泛使用，并且许多规范现在在交换中[禁止其使用](https://security.stackexchange.com/a/68609/3573)。</span><span class="sxs-lookup"><span data-stu-id="f060b-104">The UTF-7 encoding is no longer in wide use among applications, and many specs now [forbid its use](https://security.stackexchange.com/a/68609/3573) in interchange.</span></span> <span data-ttu-id="f060b-105">它偶尔还会在不期望遇到 UTF-7 编码数据的应用程序中[用作攻击途径](https://cve.mitre.org/cgi-bin/cvekey.cgi?keyword=utf-7)。</span><span class="sxs-lookup"><span data-stu-id="f060b-105">It's also occasionally [used as an attack vector](https://cve.mitre.org/cgi-bin/cvekey.cgi?keyword=utf-7) in applications that don't anticipate encountering UTF-7-encoded data.</span></span> <span data-ttu-id="f060b-106">Microsoft 警告不要使用 <xref:System.Text.UTF7Encoding?displayProperty=nameWithType>，因为它不提供错误检测。</span><span class="sxs-lookup"><span data-stu-id="f060b-106">Microsoft warns against use of <xref:System.Text.UTF7Encoding?displayProperty=nameWithType> because it doesn't provide error detection.</span></span>

<span data-ttu-id="f060b-107">因此从 .NET 5.0 开始，以下 API 标记为已过时。</span><span class="sxs-lookup"><span data-stu-id="f060b-107">Consequently, the following APIs are marked obsolete, starting in .NET 5.0.</span></span> <span data-ttu-id="f060b-108">使用这些 API 会在编译时生成警告 `SYSLIB0001`。</span><span class="sxs-lookup"><span data-stu-id="f060b-108">Use of these APIs generates warning `SYSLIB0001` at compile time.</span></span>

- <span data-ttu-id="f060b-109"><xref:System.Text.Encoding.UTF7?displayProperty=nameWithType> 属性</span><span class="sxs-lookup"><span data-stu-id="f060b-109"><xref:System.Text.Encoding.UTF7?displayProperty=nameWithType> property</span></span>
- <span data-ttu-id="f060b-110"><xref:System.Text.UTF7Encoding.%23ctor%2A> 构造函数</span><span class="sxs-lookup"><span data-stu-id="f060b-110"><xref:System.Text.UTF7Encoding.%23ctor%2A> constructors</span></span>

## <a name="workarounds"></a><span data-ttu-id="f060b-111">工作区</span><span class="sxs-lookup"><span data-stu-id="f060b-111">Workarounds</span></span>

- <span data-ttu-id="f060b-112">如果在你自己的协议或文件格式中使用的是 <xref:System.Text.Encoding.UTF7?displayProperty=nameWithType> 或 <xref:System.Text.UTF7Encoding>：</span><span class="sxs-lookup"><span data-stu-id="f060b-112">If you're using <xref:System.Text.Encoding.UTF7?displayProperty=nameWithType> or <xref:System.Text.UTF7Encoding> within your own protocol or file format:</span></span>

  <span data-ttu-id="f060b-113">切换到使用 <xref:System.Text.Encoding.UTF8?displayProperty=nameWithType> 或 <xref:System.Text.UTF8Encoding>。</span><span class="sxs-lookup"><span data-stu-id="f060b-113">Switch to using <xref:System.Text.Encoding.UTF8?displayProperty=nameWithType> or <xref:System.Text.UTF8Encoding>.</span></span> <span data-ttu-id="f060b-114">UTF-8 是一种行业标准，并且受到语言、操作系统和运行时的广泛支持。</span><span class="sxs-lookup"><span data-stu-id="f060b-114">UTF-8 is an industry standard and is widely supported across languages, operating systems, and runtimes.</span></span> <span data-ttu-id="f060b-115">使用 UTF-8 简化了代码的将来维护，并使其与生态系统的其余部分更具互操作性。</span><span class="sxs-lookup"><span data-stu-id="f060b-115">Using UTF-8 eases future maintenance of your code and makes it more interoperable with the rest of the ecosystem.</span></span>

- <span data-ttu-id="f060b-116">如果要将 <xref:System.Text.Encoding> 实例与 <xref:System.Text.Encoding.UTF7?displayProperty=nameWithType> 进行比较：</span><span class="sxs-lookup"><span data-stu-id="f060b-116">If you're comparing an <xref:System.Text.Encoding> instance against <xref:System.Text.Encoding.UTF7?displayProperty=nameWithType>:</span></span>

  <span data-ttu-id="f060b-117">可转为考虑针对众所周知的 UTF-7 代码页（即 `65000`）执行检查。</span><span class="sxs-lookup"><span data-stu-id="f060b-117">Instead, consider performing a check against the well-known UTF-7 code page, which is `65000`.</span></span> <span data-ttu-id="f060b-118">通过与代码页进行比较，可以避免出现警告，还可以处理一些边缘情况，例如，如果有人调用 `new UTF7Encoding()` 或子类化类型。</span><span class="sxs-lookup"><span data-stu-id="f060b-118">By comparing against the code page, you avoid the warning and also handle some edge cases, such as if somebody called `new UTF7Encoding()` or subclassed the type.</span></span>

  ```csharp
  void DoSomething(Encoding enc)
  {
      // Don't perform the check this way.
      // It produces a warning and misses some edge cases.
      if (enc == Encoding.UTF7)
      {
          // Encoding is UTF-7.
      }

      // Instead, perform the check this way.
      if (enc != null && enc.CodePage == 65000)
      {
          // Encoding is UTF-7.
      }
  }
  ```

[!INCLUDE [suppress-syslib-warning](../../../../includes/suppress-syslib-warning.md)]

## <a name="see-also"></a><span data-ttu-id="f060b-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f060b-119">See also</span></span>

- [<span data-ttu-id="f060b-120">UTF-7 代码路径已过时</span><span class="sxs-lookup"><span data-stu-id="f060b-120">UTF-7 code paths are obsolete</span></span>](../core-libraries/5.0/utf-7-code-paths-obsolete.md)
