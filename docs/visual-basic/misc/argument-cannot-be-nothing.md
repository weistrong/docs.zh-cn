---
description: 了解详细信息：参数不能为 Nothing
title: 参数不能为 Nothing
ms.date: 07/20/2015
f1_keywords:
- vbrGeneral_ArgumentNullException
ms.assetid: 2abd995b-36a5-45f0-b3c1-6e0c3b31a875
ms.openlocfilehash: 7a35d464b9e8cdbcfd0ee98a538eff653dca346c
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100472327"
---
# <a name="argument-cannot-be-nothing"></a><span data-ttu-id="71ec4-103">参数不能为 Nothing</span><span class="sxs-lookup"><span data-stu-id="71ec4-103">Argument cannot be Nothing</span></span>

<span data-ttu-id="71ec4-104">向必须具有值的参数提供了 null 值。</span><span class="sxs-lookup"><span data-stu-id="71ec4-104">A null value has been supplied for an argument that must have a value.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="71ec4-105">更正此错误</span><span class="sxs-lookup"><span data-stu-id="71ec4-105">To correct this error</span></span>  
  
- <span data-ttu-id="71ec4-106">你可能试图在未先提供对象的实例的情况下使用对象。</span><span class="sxs-lookup"><span data-stu-id="71ec4-106">You might have tried to use an object without providing an instance of the object.</span></span> <span data-ttu-id="71ec4-107">在这种情况下，请使用 `New` 关键字创建实例。</span><span class="sxs-lookup"><span data-stu-id="71ec4-107">In such a case, use the `New` keyword to create the instance.</span></span>  
  
- <span data-ttu-id="71ec4-108">检查值是否计算正确。</span><span class="sxs-lookup"><span data-stu-id="71ec4-108">Check that the value is calculated correctly.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="71ec4-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="71ec4-109">See also</span></span>

- <xref:System.NullReferenceException>
