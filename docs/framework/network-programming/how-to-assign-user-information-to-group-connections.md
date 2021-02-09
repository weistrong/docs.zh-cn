---
description: 详细了解：操作说明：将用户信息分配给组连接
title: 如何：将用户信息分配给组连接
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 7ce550d6-8f7c-4ea7-add8-5bc27a7b51be
ms.openlocfilehash: 2af901b91c561f5f46c63ed627cbd0053d30e624
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99729258"
---
# <a name="how-to-assign-user-information-to-group-connections"></a><span data-ttu-id="440e8-103">如何：将用户信息分配给组连接</span><span class="sxs-lookup"><span data-stu-id="440e8-103">How to: Assign User Information to Group Connections</span></span>

 <span data-ttu-id="440e8-104">以下示例演示如何将用户信息分配给组连接，其假定应用程序在调用此部分的代码之前设置了变量“UserName”、“SecurelyStoredPassword”和“域”，且“UserName”唯一。</span><span class="sxs-lookup"><span data-stu-id="440e8-104">The following example demonstrates how to assign user information to group connections, assuming that the application sets the variables *UserName*, *SecurelyStoredPassword*, and *Domain* before this section of code is called and that *UserName* is unique.</span></span>  
  
### <a name="to-assign-user-information-to-a-group-connection"></a><span data-ttu-id="440e8-105">将用户信息分配给组连接</span><span class="sxs-lookup"><span data-stu-id="440e8-105">To assign user information to a group connection</span></span>  
  
1. <span data-ttu-id="440e8-106">创建连接组名称。</span><span class="sxs-lookup"><span data-stu-id="440e8-106">Create a connection group name.</span></span>  
  
    ```csharp  
    SHA1Managed Sha1 = new SHA1Managed();  
    Byte[] updHash = Sha1.ComputeHash(Encoding.UTF8.GetBytes(UserName + SecurelyStoredPassword + Domain));  
    String secureGroupName = Encoding.Default.GetString(updHash);  
    ```  
  
    ```vb  
    Dim Sha1 As New SHA1Managed()  
    Dim updHash As [Byte]() = Sha1.ComputeHash(Encoding.UTF8.GetBytes((UserName + SecurelyStoredPassword + Domain)))  
    Dim secureGroupName As [String] = Encoding.Default.GetString(updHash)  
    ```  
  
2. <span data-ttu-id="440e8-107">为特定的 URL 创建请求。</span><span class="sxs-lookup"><span data-stu-id="440e8-107">Create a request for a specific URL.</span></span> <span data-ttu-id="440e8-108">例如，以下代码为 URL `http://www.contoso.com.` 创建请求</span><span class="sxs-lookup"><span data-stu-id="440e8-108">For example, the following code creates a request for the URL `http://www.contoso.com.`</span></span>  
  
    ```csharp  
    WebRequest myWebRequest=WebRequest.Create("http://www.contoso.com");  
    ```  
  
    ```vb  
    Dim myWebRequest As WebRequest = WebRequest.Create("http://www.contoso.com")  
    ```  
  
3. <span data-ttu-id="440e8-109">为 Web 请求设置凭据和连接组名称，并调用 GetResponse 以检索 WebResponse 对象。</span><span class="sxs-lookup"><span data-stu-id="440e8-109">Set the credentials and Connection GroupName for the Web request, and call **GetResponse** to retrieve a **WebResponse** object.</span></span>  
  
    ```csharp  
    myWebRequest.Credentials = new NetworkCredential(UserName, SecurelyStoredPassword, Domain);
    myWebRequest.ConnectionGroupName = secureGroupName;  
  
    WebResponse myWebResponse=myWebRequest.GetResponse();  
    ```  
  
    ```vb  
    myWebRequest.Credentials = New NetworkCredential(UserName, SecurelyStoredPassword, Domain)  
    myWebRequest.ConnectionGroupName = secureGroupName  
  
    Dim myWebResponse As WebResponse = myWebRequest.GetResponse()  
    ```  
  
4. <span data-ttu-id="440e8-110">使用 WebRespose 对象后关闭响应流。</span><span class="sxs-lookup"><span data-stu-id="440e8-110">Close the response stream after using the WebRespose object.</span></span>  
  
    ```csharp  
    MyWebResponse.Close();  
    ```  
  
    ```vb  
    MyWebResponse.Close()  
    ```  
  
 <span data-ttu-id="440e8-111">示例</span><span class="sxs-lookup"><span data-stu-id="440e8-111">Example</span></span>  
  
```csharp  
// Create a connection group name.  
SHA1Managed Sha1 = new SHA1Managed();  
Byte[] updHash = Sha1.ComputeHash(Encoding.UTF8.GetBytes(UserName + SecurelyStoredPassword + Domain));  
String secureGroupName = Encoding.Default.GetString(updHash);  
  
// Create a request for a specific URL.  
WebRequest myWebRequest=WebRequest.Create("http://www.contoso.com");  
  
myWebRequest.Credentials = new NetworkCredential(UserName, SecurelyStoredPassword, Domain);
myWebRequest.ConnectionGroupName = secureGroupName;  
  
WebResponse myWebResponse=myWebRequest.GetResponse();  
  
// Insert the code that uses myWebResponse.  
  
MyWebResponse.Close();  
```  
  
```vb  
' Create a secure group name.  
Dim Sha1 As New SHA1Managed()  
Dim updHash As [Byte]() = Sha1.ComputeHash(Encoding.UTF8.GetBytes((UserName + SecurelyStoredPassword + Domain)))  
Dim secureGroupName As [String] = Encoding.Default.GetString(updHash)  
  
' Create a request for a specific URL.  
Dim myWebRequest As WebRequest = WebRequest.Create("http://www.contoso.com")  
  
myWebRequest.Credentials = New NetworkCredential(UserName, SecurelyStoredPassword, Domain)  
myWebRequest.ConnectionGroupName = secureGroupName  
  
Dim myWebResponse As WebResponse = myWebRequest.GetResponse()  
  
' Insert the code that uses myWebResponse.  
MyWebResponse.Close()  
```  
  
## <a name="see-also"></a><span data-ttu-id="440e8-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="440e8-112">See also</span></span>

- [<span data-ttu-id="440e8-113">管理连接</span><span class="sxs-lookup"><span data-stu-id="440e8-113">Managing Connections</span></span>](managing-connections.md)
- [<span data-ttu-id="440e8-114">连接分组</span><span class="sxs-lookup"><span data-stu-id="440e8-114">Connection Grouping</span></span>](connection-grouping.md)
