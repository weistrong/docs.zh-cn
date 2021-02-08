---
description: 了解详细信息：属性或方法调用不能包括对私有对象的引用，不管是作为参数还是作为返回值
title: 无论是作为参数还是作为返回值，属性或方法调用都不能包括对私有对象的引用
ms.date: 07/20/2015
f1_keywords:
- vbrID98
ms.assetid: 059b43e1-202d-4fa2-806b-7bad63c1e7ca
ms.openlocfilehash: 8fe570c9ed789a5bac36aafa9b1ec2f507a55d51
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797193"
---
# <a name="a-property-or-method-call-cannot-include-a-reference-to-a-private-object-either-as-an-argument-or-as-a-return-value"></a><span data-ttu-id="88285-103">无论是作为参数还是作为返回值，属性或方法调用都不能包括对私有对象的引用</span><span class="sxs-lookup"><span data-stu-id="88285-103">A property or method call cannot include a reference to a private object, either as an argument or as a return value</span></span>

<span data-ttu-id="88285-104">此错误的可能原因包括：</span><span class="sxs-lookup"><span data-stu-id="88285-104">Among the possible causes of this error are:</span></span>

- <span data-ttu-id="88285-105">客户端调用了进程外组件的属性或方法，并且试图将对私有对象的引用作为参数之一进行传递。</span><span class="sxs-lookup"><span data-stu-id="88285-105">A client invoked a property or method of an out-of-process component and attempted to pass a reference to a private object as one of the arguments.</span></span>

- <span data-ttu-id="88285-106">进程外组件调用了其客户端上的回调方法，并试图传递对私有对象的引用。</span><span class="sxs-lookup"><span data-stu-id="88285-106">An out-of-process component invoked a call-back method on its client and attempted to pass a reference to a private object.</span></span>

- <span data-ttu-id="88285-107">进程外组件试图将对私有对象的引用作为它所引发的事件的参数进行传递。</span><span class="sxs-lookup"><span data-stu-id="88285-107">An out-of-process component attempted to pass a reference to a private object as an argument of an event it was raising.</span></span>

- <span data-ttu-id="88285-108">客户端试图将私有对象引用赋给它正在处理的事件的 `ByRef` 参数。</span><span class="sxs-lookup"><span data-stu-id="88285-108">A client attempted to assign a private object reference to a `ByRef` argument of an event it was handling.</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="88285-109">更正此错误</span><span class="sxs-lookup"><span data-stu-id="88285-109">To correct this error</span></span>

- <span data-ttu-id="88285-110">删除引用。</span><span class="sxs-lookup"><span data-stu-id="88285-110">Remove the reference.</span></span>

## <a name="see-also"></a><span data-ttu-id="88285-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="88285-111">See also</span></span>

- [<span data-ttu-id="88285-112">专用</span><span class="sxs-lookup"><span data-stu-id="88285-112">Private</span></span>](../modifiers/private.md)
