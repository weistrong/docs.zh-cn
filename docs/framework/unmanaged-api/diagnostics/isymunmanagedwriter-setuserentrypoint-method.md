---
description: 了解详细信息： ISymUnmanagedWriter：： SetUserEntryPoint 方法
title: ISymUnmanagedWriter::SetUserEntryPoint 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.SetUserEntryPoint
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::SetUserEntryPoint
helpviewer_keywords:
- ISymUnmanagedWriter::SetUserEntryPoint method [.NET Framework debugging]
- SetUserEntryPoint method [.NET Framework debugging]
ms.assetid: d4dcc575-3ac8-4453-9be1-2b24f47363d7
topic_type:
- apiref
ms.openlocfilehash: a01d23a0462fabd7a2fc259722dcdf2a1c8e0a4c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761975"
---
# <a name="isymunmanagedwritersetuserentrypoint-method"></a><span data-ttu-id="ce4fc-103">ISymUnmanagedWriter::SetUserEntryPoint 方法</span><span class="sxs-lookup"><span data-stu-id="ce4fc-103">ISymUnmanagedWriter::SetUserEntryPoint Method</span></span>

<span data-ttu-id="ce4fc-104">指定用户定义的方法，该方法是此模块的入口点。</span><span class="sxs-lookup"><span data-stu-id="ce4fc-104">Specifies the user-defined method that is the entry point for this module.</span></span> <span data-ttu-id="ce4fc-105">例如，在 main 之前，此入口点可能是用户的 main 方法，而不是编译器生成的存根。</span><span class="sxs-lookup"><span data-stu-id="ce4fc-105">For example, this entry point could be the user's main method instead of compiler-generated stubs before main.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ce4fc-106">语法</span><span class="sxs-lookup"><span data-stu-id="ce4fc-106">Syntax</span></span>  
  
```cpp  
HRESULT SetUserEntryPoint(  
    [in] mdMethodDef entryMethod);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ce4fc-107">参数</span><span class="sxs-lookup"><span data-stu-id="ce4fc-107">Parameters</span></span>  

 `entryMethod`  
 <span data-ttu-id="ce4fc-108">中方法的元数据标记，它是用户入口点。</span><span class="sxs-lookup"><span data-stu-id="ce4fc-108">[in] The metadata token for the method that is the user entry point.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ce4fc-109">返回值</span><span class="sxs-lookup"><span data-stu-id="ce4fc-109">Return Value</span></span>  

 <span data-ttu-id="ce4fc-110">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="ce4fc-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ce4fc-111">要求</span><span class="sxs-lookup"><span data-stu-id="ce4fc-111">Requirements</span></span>  

 <span data-ttu-id="ce4fc-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="ce4fc-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ce4fc-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="ce4fc-113">See also</span></span>

- [<span data-ttu-id="ce4fc-114">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="ce4fc-114">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
