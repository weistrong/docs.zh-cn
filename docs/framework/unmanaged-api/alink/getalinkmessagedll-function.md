---
description: 了解详细信息： GetALinkMessageDll 函数
title: GetALinkMessageDll 函数
ms.date: 03/30/2017
api_name:
- GetALinkMessageDll
api_location:
- alink.dll
api_type:
- DLLExport
f1_keywords:
- GetALinkMessageDll
helpviewer_keywords:
- Alink API, GetALinkMessageDll function
- GetALinkMessageDll function
ms.assetid: 67985a22-88a2-4c54-8d99-4bcde9d6213e
topic_type:
- apiref
ms.openlocfilehash: 67a294d1f21f50cee938ddeb14d1f30b4ccf911b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637867"
---
# <a name="getalinkmessagedll-function"></a><span data-ttu-id="c3fd2-103">GetALinkMessageDll 函数</span><span class="sxs-lookup"><span data-stu-id="c3fd2-103">GetALinkMessageDll Function</span></span>

<span data-ttu-id="c3fd2-104">查找并加载消息 DLL。</span><span class="sxs-lookup"><span data-stu-id="c3fd2-104">Finds and loads the message DLL.</span></span> <span data-ttu-id="c3fd2-105">如果找不到或无法加载消息 DLL，则返回0。</span><span class="sxs-lookup"><span data-stu-id="c3fd2-105">Returns 0 if the message DLL could not be located or loaded.</span></span> <span data-ttu-id="c3fd2-106">消息 DLL 应位于其名称为语言 ID 的子目录中，或位于当前目录中。</span><span class="sxs-lookup"><span data-stu-id="c3fd2-106">The message DLL should be either in a subdirectory whose name is a language ID, or in the current directory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c3fd2-107">语法</span><span class="sxs-lookup"><span data-stu-id="c3fd2-107">Syntax</span></span>  
  
```cpp  
HINSTANCE WINAPI GetALinkMessageDll();  
```  
  
## <a name="requirements"></a><span data-ttu-id="c3fd2-108">要求</span><span class="sxs-lookup"><span data-stu-id="c3fd2-108">Requirements</span></span>  

 <span data-ttu-id="c3fd2-109">**标头：** alink。h</span><span class="sxs-lookup"><span data-stu-id="c3fd2-109">**Header:** alink.h</span></span>  
  
 <span data-ttu-id="c3fd2-110">**库**： alink.dll</span><span class="sxs-lookup"><span data-stu-id="c3fd2-110">**Library**: alink.dll</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c3fd2-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="c3fd2-111">See also</span></span>

- [<span data-ttu-id="c3fd2-112">Al.exe（程序集链接器）</span><span class="sxs-lookup"><span data-stu-id="c3fd2-112">Al.exe (Assembly Linker)</span></span>](../../tools/al-exe-assembly-linker.md)
