---
description: 了解详细信息：调试全局静态函数
title: 调试全局静态函数
ms.date: 03/30/2017
helpviewer_keywords:
- global static functions [.NET Framework debugging]
- debugging global static functions [.NET Framework]
- unmanaged global static functions [.NET Framework], debugging
ms.assetid: efc64414-77c3-48d0-881a-8594ed416aad
ms.openlocfilehash: efee1bfb6eb61ae2311320a4c12bf08ec0f9534b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99661449"
---
# <a name="debugging-global-static-functions"></a><span data-ttu-id="1eb09-103">调试全局静态函数</span><span class="sxs-lookup"><span data-stu-id="1eb09-103">Debugging Global Static Functions</span></span>

<span data-ttu-id="1eb09-104">本节介绍了调试 API 使用的非托管全局静态函数。</span><span class="sxs-lookup"><span data-stu-id="1eb09-104">This section describes the unmanaged global static functions that the debugging API uses.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="1eb09-105">本节内容</span><span class="sxs-lookup"><span data-stu-id="1eb09-105">In This Section</span></span>  

 [<span data-ttu-id="1eb09-106">_EFN_GetManagedExcepStack 函数</span><span class="sxs-lookup"><span data-stu-id="1eb09-106">_EFN_GetManagedExcepStack Function</span></span>](efn-getmanagedexcepstack-function.md)  
 <span data-ttu-id="1eb09-107">给定托管的异常对象地址后，将返回其中包含的堆栈跟踪的字符串版本。</span><span class="sxs-lookup"><span data-stu-id="1eb09-107">Given a managed exception object address, returns a string version of the stack trace contained inside.</span></span>  
  
 [<span data-ttu-id="1eb09-108">_EFN_GetManagedObjectFieldInfo 函数</span><span class="sxs-lookup"><span data-stu-id="1eb09-108">_EFN_GetManagedObjectFieldInfo Function</span></span>](efn-getmanagedobjectfieldinfo-function.md)  
 <span data-ttu-id="1eb09-109">使用提供的对象指针和字段名，获取从对象的开头到字段和字段值的偏移量。</span><span class="sxs-lookup"><span data-stu-id="1eb09-109">Gets the offset from the start of an object to a field and the field's value, using the provided object pointer and field name.</span></span>  
  
 [<span data-ttu-id="1eb09-110">_EFN_GetManagedObjectName 函数</span><span class="sxs-lookup"><span data-stu-id="1eb09-110">_EFN_GetManagedObjectName Function</span></span>](efn-getmanagedobjectname-function.md)  
 <span data-ttu-id="1eb09-111">通过使用提供的托管对象指针获取类型名称。</span><span class="sxs-lookup"><span data-stu-id="1eb09-111">Gets the name of a type by using the provided managed object pointer.</span></span>  
  
 [<span data-ttu-id="1eb09-112">_EFN_StackTrace 函数</span><span class="sxs-lookup"><span data-stu-id="1eb09-112">_EFN_StackTrace Function</span></span>](efn-stacktrace-function.md)  
 <span data-ttu-id="1eb09-113">提供托管堆栈跟踪的文本表示形式以及 `CONTEXT` 记录的数组，其中每项对应非托管代码和托管代码之间的每个转换。</span><span class="sxs-lookup"><span data-stu-id="1eb09-113">Provides a text representation of a managed stack trace and an array of `CONTEXT` records, one for each transition between unmanaged and managed code.</span></span>  
  
 [<span data-ttu-id="1eb09-114">CLRDataCreateInstance 函数</span><span class="sxs-lookup"><span data-stu-id="1eb09-114">CLRDataCreateInstance Function</span></span>](clrdatacreateinstance-function.md)  
 <span data-ttu-id="1eb09-115">由公共语言运行时 (CLR) 数据访问服务调用，用于创建指定目标进程的指定接口对象。</span><span class="sxs-lookup"><span data-stu-id="1eb09-115">Called by the common language runtime (CLR) data access services to create the specified interface object for the specified target process.</span></span>  
  
 [<span data-ttu-id="1eb09-116">PFN_CLRDataCreateInstance 函数指针</span><span class="sxs-lookup"><span data-stu-id="1eb09-116">PFN_CLRDataCreateInstance Function Pointer</span></span>](pfn-clrdatacreateinstance-function-pointer.md)  
 <span data-ttu-id="1eb09-117">指向 CLR 数据访问服务调用来创建指定目标进程的指定接口对象的函数。</span><span class="sxs-lookup"><span data-stu-id="1eb09-117">Points to a function that is called by the CLR data access services to create the specified interface object for the specified target process.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="1eb09-118">相关章节</span><span class="sxs-lookup"><span data-stu-id="1eb09-118">Related Sections</span></span>  

 [<span data-ttu-id="1eb09-119">调试 Coclass</span><span class="sxs-lookup"><span data-stu-id="1eb09-119">Debugging Coclasses</span></span>](debugging-coclasses.md)  
  
 [<span data-ttu-id="1eb09-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="1eb09-120">Debugging Interfaces</span></span>](debugging-interfaces.md)  
  
 [<span data-ttu-id="1eb09-121">调试枚举</span><span class="sxs-lookup"><span data-stu-id="1eb09-121">Debugging Enumerations</span></span>](debugging-enumerations.md)  
  
 [<span data-ttu-id="1eb09-122">调试结构</span><span class="sxs-lookup"><span data-stu-id="1eb09-122">Debugging Structures</span></span>](debugging-structures.md)
