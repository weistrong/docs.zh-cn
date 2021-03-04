---
description: 了解有关以下方面的详细信息：类不支持自动化或不支持所需的接口
title: 类不支持自动化或不支持所需的接口
ms.date: 07/20/2015
f1_keywords:
- vbrID430
ms.assetid: d985bb7e-e48e-443e-86f2-ddb86758757c
ms.openlocfilehash: c173eeddf3a34d6af169b91066199ce7d03cf4ba
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102106626"
---
# <a name="class-does-not-support-automation-or-does-not-support-expected-interface"></a>类不支持自动化或不支持所需的接口

在 `GetObject` 或 `CreateObject` 函数调用中所指定的类尚未公开可编程接口，或者将项目从 .dll 更改为 .exe 或相反。  
  
## <a name="to-correct-this-error"></a>更正此错误  
  
1. 检查创建对象的应用程序的相关文档，确定该对象类是否存在使用自动化的限制。  
  
2. 如果将项目从 .dll 更改为 .exe 或者相反，必须手动注销旧的 .dll 或 .exe。  
  
## <a name="see-also"></a>另请参阅

- [错误类型](../../programming-guide/language-features/error-types.md)
- [Visual Studio 反馈选项](/visualstudio/ide/feedback-options)
