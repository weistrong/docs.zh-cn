---
ms.openlocfilehash: bf7ea8a36b9c36d82b4c00ada890829bf4c2c024
ms.sourcegitcommit: a4cecb7389f02c27e412b743f9189bd2a6dea4d6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/14/2021
ms.locfileid: "97700850"
---
### <a name="include-specific-api-surfaces"></a><span data-ttu-id="99673-101">包含特定的 API 图面</span><span class="sxs-lookup"><span data-stu-id="99673-101">Include specific API surfaces</span></span>

<span data-ttu-id="99673-102">你可以根据其可访问性，将基本代码的哪些部分配置为在上运行此规则。</span><span class="sxs-lookup"><span data-stu-id="99673-102">You can configure which parts of your codebase to run this rule on, based on their accessibility.</span></span> <span data-ttu-id="99673-103">例如，若要指定规则只应针对非公共 API 图面运行，请在项目中的 *editorconfig* 文件中添加以下键/值对：</span><span class="sxs-lookup"><span data-stu-id="99673-103">For example, to specify that the rule should run only against the non-public API surface, add the following key-value pair to an *.editorconfig* file in your project:</span></span>

```ini
dotnet_code_quality.CAXXXX.api_surface = private, internal
```
