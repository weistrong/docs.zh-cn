---
description: 了解详细信息：变量使用 Visual Basic 中不支持的自动化类型
title: 变量使用了不支持的自动化类型
ms.date: 07/20/2015
f1_keywords:
- vbrID458
ms.assetid: bde4f4da-493b-452c-b6e4-1d370edba4cd
ms.openlocfilehash: 9aa8f8a2a49e54c547dc47d38305d40f855b1815
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99666142"
---
# <a name="variable-uses-an-automation-type-not-supported-in-visual-basic"></a><span data-ttu-id="4a692-103">变量使用了 Visual Basic 不支持的自动化类型</span><span class="sxs-lookup"><span data-stu-id="4a692-103">Variable uses an Automation type not supported in Visual Basic</span></span>

<span data-ttu-id="4a692-104">尝试使用类型库或对象库中定义的变量，该变量的数据类型不受 Visual Basic 支持。</span><span class="sxs-lookup"><span data-stu-id="4a692-104">You tried to use a variable defined in a type library or object library that has a data type not supported by Visual Basic.</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="4a692-105">更正此错误</span><span class="sxs-lookup"><span data-stu-id="4a692-105">To correct this error</span></span>

- <span data-ttu-id="4a692-106">使用 Visual Basic 可识别的类型的变量。</span><span class="sxs-lookup"><span data-stu-id="4a692-106">Use a variable of a type recognized by Visual Basic.</span></span>

     <span data-ttu-id="4a692-107">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="4a692-107">-or-</span></span>

- <span data-ttu-id="4a692-108">如果你在使用或时遇到此错误 `FileGet` `FileGetObject` ，请确保你尝试使用的文件已使用 `FilePut` 或写入 `FilePutObject` 。</span><span class="sxs-lookup"><span data-stu-id="4a692-108">If you encounter this error while using `FileGet` or `FileGetObject`, make sure the file you are trying to use was written to with `FilePut` or `FilePutObject`.</span></span>

## <a name="see-also"></a><span data-ttu-id="4a692-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="4a692-109">See also</span></span>

- [<span data-ttu-id="4a692-110">数据类型</span><span class="sxs-lookup"><span data-stu-id="4a692-110">Data Types</span></span>](../data-types/index.md)
