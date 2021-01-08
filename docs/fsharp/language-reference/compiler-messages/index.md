---
title: 编译器错误和警告
description: F# 编译器将发出的错误和警告的说明和解决方案
ms.date: 12/21/2019
ms.openlocfilehash: 58430297abe807027afdc52841d67d1233401ff1
ms.sourcegitcommit: e395fabeeea5c705d243d246fa64446839ac85b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/03/2021
ms.locfileid: "97856115"
---
# <a name="f-compiler-messages"></a><span data-ttu-id="ac268-103">F# 编译器消息</span><span class="sxs-lookup"><span data-stu-id="ac268-103">F# compiler messages</span></span>

<span data-ttu-id="ac268-104">此部分详细介绍 F# 编译器将针对某些构造发出的编译器错误和警告。</span><span class="sxs-lookup"><span data-stu-id="ac268-104">This section details compiler errors and warnings that the F# compiler will emit for certain constructs.</span></span> <span data-ttu-id="ac268-105">可以通过以下方式更改默认错误集：</span><span class="sxs-lookup"><span data-stu-id="ac268-105">The default sets of errors can be changed by:</span></span>

- <span data-ttu-id="ac268-106">使用 `-warnaserror+` 编译器选项，将特定警告视为错误，</span><span class="sxs-lookup"><span data-stu-id="ac268-106">Treating specific warnings as if they were errors by using the `-warnaserror+` compiler option,</span></span>

- <span data-ttu-id="ac268-107">使用 `-nowarn` 编译器选项，忽略特定警告</span><span class="sxs-lookup"><span data-stu-id="ac268-107">Ignoring specific warnings by using the `-nowarn` compiler option</span></span>

<span data-ttu-id="ac268-108">如果此部分中尚未记录特定警告或错误：</span><span class="sxs-lookup"><span data-stu-id="ac268-108">If a particular warning or error is not yet recorded in this section:</span></span>

- <span data-ttu-id="ac268-109">请转到此页末尾，然后发送包含错误号或文本的反馈，或者</span><span class="sxs-lookup"><span data-stu-id="ac268-109">Go to the end of this page and send feedback that includes the number or text of the error, or</span></span>
- <span data-ttu-id="ac268-110">按照 [create-new-fsharp-compiler-message.fsx](https://github.com/dotnet/docs/blob/master/docs/fsharp/language-reference/compiler-messages/util/create-new-fsharp-compiler-message.fsx) 中的说明进行操作，并打开此存储库的拉取请求，自行添加。</span><span class="sxs-lookup"><span data-stu-id="ac268-110">Add it yourself by following the instructions in [create-new-fsharp-compiler-message.fsx](https://github.com/dotnet/docs/blob/master/docs/fsharp/language-reference/compiler-messages/util/create-new-fsharp-compiler-message.fsx) and opening a pull request for this repository.</span></span>

## <a name="see-also"></a><span data-ttu-id="ac268-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ac268-111">See also</span></span>

- [<span data-ttu-id="ac268-112">F# 编译器选项</span><span class="sxs-lookup"><span data-stu-id="ac268-112">F# Compiler Options</span></span>](../compiler-options.md)
