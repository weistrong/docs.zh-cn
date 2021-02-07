---
description: '了解详细信息： (实体 SQL 输入字符集) '
title: 输入字符集 (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 13d291d3-e6bc-4719-b953-758b61a590b6
ms.openlocfilehash: b17b9b2022a49717aace3c9f642ac62a2f30b2b5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99748500"
---
# <a name="input-character-set-entity-sql"></a><span data-ttu-id="7bee8-103">输入字符集 (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="7bee8-103">Input Character Set (Entity SQL)</span></span>

[!INCLUDE[esql](../../../../../../includes/esql-md.md)] <span data-ttu-id="7bee8-104">接受使用 UTF-16 进行编码的 UNICODE 字符。</span><span class="sxs-lookup"><span data-stu-id="7bee8-104">accepts UNICODE characters encoded in UTF-16.</span></span>  
  
 <span data-ttu-id="7bee8-105">字符串文字可以包含用单引号括起来的任何 UTF-16 字符。</span><span class="sxs-lookup"><span data-stu-id="7bee8-105">String literals can contain any UTF-16 character enclosed in single quotes.</span></span> <span data-ttu-id="7bee8-106">例如，N'文字列リテラル'。</span><span class="sxs-lookup"><span data-stu-id="7bee8-106">For example, N'文字列リテラル'.</span></span> <span data-ttu-id="7bee8-107">比较字符串文字时，将使用原始的 UTF-16 值。</span><span class="sxs-lookup"><span data-stu-id="7bee8-107">When string literals are compared, the original UTF-16 values are used.</span></span> <span data-ttu-id="7bee8-108">例如，N'ABC' 在日语代码页和拉丁语代码页中是不同的。</span><span class="sxs-lookup"><span data-stu-id="7bee8-108">For example, N'ABC' is different in Japanese and Latin codepages.</span></span>  
  
 <span data-ttu-id="7bee8-109">注释可包含任何 UTF-16 字符。</span><span class="sxs-lookup"><span data-stu-id="7bee8-109">Comments can contain any UTF-16 character.</span></span>  
  
 <span data-ttu-id="7bee8-110">转义标识符可以包含用方括号括起来的任何 UTF-16 字符。</span><span class="sxs-lookup"><span data-stu-id="7bee8-110">Escaped identifiers can contain any UTF-16 character enclosed in square brackets.</span></span> <span data-ttu-id="7bee8-111">例如，[エスケープされた識別子]。</span><span class="sxs-lookup"><span data-stu-id="7bee8-111">For example, [エスケープされた識別子].</span></span> <span data-ttu-id="7bee8-112">UTF-16 转义标识符的比较不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="7bee8-112">The comparison of UTF-16 escaped identifiers is case insensitive.</span></span> [!INCLUDE[esql](../../../../../../includes/esql-md.md)] <span data-ttu-id="7bee8-113">将看上去相同但来自不同代码页的字母视为不同的字符。</span><span class="sxs-lookup"><span data-stu-id="7bee8-113">treats versions of letters that appear the same but are from different code pages as different characters.</span></span> <span data-ttu-id="7bee8-114">例如，如果 [ABC] 和 [abc] 的字符来自同一代码页，则 [ABC] 等效于 [abc]。</span><span class="sxs-lookup"><span data-stu-id="7bee8-114">For example, [ABC] is equivalent to [abc] if the corresponding characters are from the same code page.</span></span> <span data-ttu-id="7bee8-115">但如果这两个标识符来自不同的代码页，它们就不等效。</span><span class="sxs-lookup"><span data-stu-id="7bee8-115">However, if the same two identifiers are from different code pages, they are not equivalent.</span></span>  
  
 <span data-ttu-id="7bee8-116">空白是任何 UTF-16 空白字符。</span><span class="sxs-lookup"><span data-stu-id="7bee8-116">White space is any UTF-16 white space character.</span></span>  
  
 <span data-ttu-id="7bee8-117">换行符是任何标准化的 UTF-16 换行符。</span><span class="sxs-lookup"><span data-stu-id="7bee8-117">A newline is any normalized UTF-16 newline character.</span></span> <span data-ttu-id="7bee8-118">例如，'\n' 和 '\r\n' 被视为换行符，但 '\r' 不是换行符。</span><span class="sxs-lookup"><span data-stu-id="7bee8-118">For example, '\n' and '\r\n' are considered newline characters, but '\r' is not a newline character.</span></span>  
  
 <span data-ttu-id="7bee8-119">关键字、表达式和标点可以是任何标准化为拉丁语的 UTF-16 字符。</span><span class="sxs-lookup"><span data-stu-id="7bee8-119">Keywords, expressions, and punctuation can be any UTF-16 character that normalizes to Latin.</span></span> <span data-ttu-id="7bee8-120">例如，SELECT 在日语代码页中是有效的关键字。</span><span class="sxs-lookup"><span data-stu-id="7bee8-120">For example, SELECT in a Japanese codepage is a valid keyword.</span></span>  
  
 <span data-ttu-id="7bee8-121">关键字、表达式和标点只能是拉丁语字符。</span><span class="sxs-lookup"><span data-stu-id="7bee8-121">Keywords, expressions, and punctuation can only be Latin characters.</span></span> <span data-ttu-id="7bee8-122">`SELECT` 在日语代码页中不是关键字。</span><span class="sxs-lookup"><span data-stu-id="7bee8-122">`SELECT` in a Japanese codepage is not a keyword.</span></span> <span data-ttu-id="7bee8-123">+、-、 \* 、/、=、 (、) 、'、[，] 以及此处不带引号的任何其他语言构造只能是拉丁字符。</span><span class="sxs-lookup"><span data-stu-id="7bee8-123">+, -, \*, /, =, (, ), ‘, [, ] and any other language construct not quoted here can only be Latin characters.</span></span>  
  
 <span data-ttu-id="7bee8-124">简单标识符只能为拉丁字符。</span><span class="sxs-lookup"><span data-stu-id="7bee8-124">Simple identifiers can only be Latin characters.</span></span> <span data-ttu-id="7bee8-125">这可以避免比较时的不确定性，因为比较时使用的是原始值。</span><span class="sxs-lookup"><span data-stu-id="7bee8-125">This avoids ambiguity during comparison, because original values are compared.</span></span> <span data-ttu-id="7bee8-126">例如，在日语和拉丁语代码页中，ABC 将有所不同。</span><span class="sxs-lookup"><span data-stu-id="7bee8-126">For example, ABC would be different in Japanese and Latin codepages.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7bee8-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="7bee8-127">See also</span></span>

- [<span data-ttu-id="7bee8-128">Entity SQL 概述</span><span class="sxs-lookup"><span data-stu-id="7bee8-128">Entity SQL Overview</span></span>](entity-sql-overview.md)
