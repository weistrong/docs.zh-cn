---
description: 了解详细信息：此单实例应用程序未能连接到原始实例
title: 此单实例应用程序未能连接到原始实例
ms.date: 07/20/2015
f1_keywords:
- vbrAppModel_SingleInstanceCantConnect
ms.assetid: 7c2c0cee-02a1-4157-be03-39d18e18408f
ms.openlocfilehash: 123cf2cded43c10d0f538fc12f31f4065caeb6dd
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100427916"
---
# <a name="this-single-instance-application-could-not-connect-to-the-original-instance"></a><span data-ttu-id="6a619-103">此单实例应用程序未能连接到原始实例</span><span class="sxs-lookup"><span data-stu-id="6a619-103">This single-instance application could not connect to the original instance</span></span>

<span data-ttu-id="6a619-104">此单实例应用程序未能连接到原始实例。</span><span class="sxs-lookup"><span data-stu-id="6a619-104">This single-instance application could not connect to the original instance.</span></span> <span data-ttu-id="6a619-105">一些可能导致此问题的原因包括：</span><span class="sxs-lookup"><span data-stu-id="6a619-105">Some of the possible causes for this problem are as follows:</span></span>  
  
- <span data-ttu-id="6a619-106">原始实例停止了响应。</span><span class="sxs-lookup"><span data-stu-id="6a619-106">The original instance stopped responding.</span></span>  
  
- <span data-ttu-id="6a619-107">应用程序没有创建内核对象的权限。</span><span class="sxs-lookup"><span data-stu-id="6a619-107">The application does not have permissions to create kernel objects.</span></span> <span data-ttu-id="6a619-108">有关内核对象的详细信息，请参阅 [mutex](../../standard/threading/mutexes.md)。</span><span class="sxs-lookup"><span data-stu-id="6a619-108">For more information about kernel objects, see [Mutexes](../../standard/threading/mutexes.md).</span></span>  
  
     <span data-ttu-id="6a619-109">内核对象的基名称是通过串联程序集的 GUID、主版本号和次版本号得到的。</span><span class="sxs-lookup"><span data-stu-id="6a619-109">The base name for the kernel objects comes from concatenating the assembly's GUID, major version number, and minor version number.</span></span> <span data-ttu-id="6a619-110">例如，基名称可能是 `3639f15d-9547-43da-8145-60da347829915.1`。</span><span class="sxs-lookup"><span data-stu-id="6a619-110">For example, the base name could be `3639f15d-9547-43da-8145-60da347829915.1`.</span></span>  
  
## <a name="to-correct-this-error-when-developing-the-application"></a><span data-ttu-id="6a619-111">在开发应用程序时更正此错误</span><span class="sxs-lookup"><span data-stu-id="6a619-111">To correct this error when developing the application</span></span>  
  
1. <span data-ttu-id="6a619-112">检查应用程序未进入未响应状态。</span><span class="sxs-lookup"><span data-stu-id="6a619-112">Check that the application does not go into an unresponsive state.</span></span>  
  
2. <span data-ttu-id="6a619-113">检查应用程序是否具有创建内核对象的足够权限。</span><span class="sxs-lookup"><span data-stu-id="6a619-113">Check that the application has sufficient permissions to create kernel objects.</span></span>  
  
3. <span data-ttu-id="6a619-114">重启应用程序的原始实例。</span><span class="sxs-lookup"><span data-stu-id="6a619-114">Restart the original instance of the application.</span></span>  
  
4. <span data-ttu-id="6a619-115">重启计算机，以清除可能正在使用连接到原始实例应用程序所需资源的任何进程。</span><span class="sxs-lookup"><span data-stu-id="6a619-115">Restart the computer to clear any process that may be using the resource that is required to connect to the original instance application.</span></span>  
  
5. <span data-ttu-id="6a619-116">记录发生错误的环境，并与 Microsoft 产品支持服务联系。</span><span class="sxs-lookup"><span data-stu-id="6a619-116">Note the circumstances under which the error occurred, and telephone Microsoft Product Support Services.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6a619-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="6a619-117">See also</span></span>

- [<span data-ttu-id="6a619-118">调试器基础知识</span><span class="sxs-lookup"><span data-stu-id="6a619-118">Debugger Basics</span></span>](/visualstudio/debugger/debugger-feature-tour)
