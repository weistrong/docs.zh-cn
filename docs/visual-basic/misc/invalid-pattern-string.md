---
description: 了解详细信息：无效的模式字符串
title: 无效模式字符串
ms.date: 07/20/2015
ms.assetid: ec1aecdb-5339-4a93-be71-eec56b1d7438
ms.openlocfilehash: 4fbf16dd43ac4ae44e1a99d85caae4a7baf99109
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100462056"
---
# <a name="invalid-pattern-string"></a><span data-ttu-id="41db8-103">无效模式字符串</span><span class="sxs-lookup"><span data-stu-id="41db8-103">Invalid pattern string</span></span>

<span data-ttu-id="41db8-104">在搜索的 `Like` 操作中指定的模式字符串无效。</span><span class="sxs-lookup"><span data-stu-id="41db8-104">The pattern string specified in the `Like` operation of a search is invalid.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="41db8-105">更正此错误</span><span class="sxs-lookup"><span data-stu-id="41db8-105">To correct this error</span></span>  
  
1. <span data-ttu-id="41db8-106">查看列表中表达式的有效字符。</span><span class="sxs-lookup"><span data-stu-id="41db8-106">Review the valid characters for list expressions.</span></span>  
  
2. <span data-ttu-id="41db8-107">在模式范围内，请确保起始范围字符小于结束范围字符，如 `[a-z]`中所示。</span><span class="sxs-lookup"><span data-stu-id="41db8-107">In the pattern range, ensure that the start range character is less than the end range character, as in `[a-z]`.</span></span>  
  
3. <span data-ttu-id="41db8-108">在模式范围内，请确保不存在彼此相邻的多个连字符，如 `[a--z]`中所示。</span><span class="sxs-lookup"><span data-stu-id="41db8-108">In the pattern range, ensure that there are not multiple hyphens next to each other, as in `[a--z]`.</span></span>  
  
4. <span data-ttu-id="41db8-109">以右括号结束模式范围。</span><span class="sxs-lookup"><span data-stu-id="41db8-109">End pattern ranges with a closing bracket.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="41db8-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="41db8-110">See also</span></span>

- [<span data-ttu-id="41db8-111">Like 运算符</span><span class="sxs-lookup"><span data-stu-id="41db8-111">Like Operator</span></span>](../language-reference/operators/like-operator.md)
