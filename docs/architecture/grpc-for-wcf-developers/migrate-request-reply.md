---
title: 将 WCF 请求-答复服务迁移到 WCF 开发人员的 gRPC-gRPC
description: 了解如何将简单的请求-答复服务从 WCF 迁移到 gRPC。
ms.date: 12/15/2020
ms.openlocfilehash: 38c6e33e7588dd7c1b263d813d06c088ab484948
ms.sourcegitcommit: 655f8a16c488567dfa696fc0b293b34d3c81e3df
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/06/2021
ms.locfileid: "97938567"
---
# <a name="migrate-a-wcf-request-reply-service-to-a-grpc-unary-rpc"></a><span data-ttu-id="bffee-103">将 WCF 请求-答复服务迁移到 gRPC 一元 RPC</span><span class="sxs-lookup"><span data-stu-id="bffee-103">Migrate a WCF request-reply service to a gRPC unary RPC</span></span>

<span data-ttu-id="bffee-104">本部分介绍如何将 WCF 中的基本请求-答复服务迁移到 ASP.NET Core gRPC 中的一元 RPC 服务。</span><span class="sxs-lookup"><span data-stu-id="bffee-104">This section covers how to migrate a basic request-reply service in WCF to a unary RPC service in ASP.NET Core gRPC.</span></span> <span data-ttu-id="bffee-105">这些服务是 Windows Communication Foundation (WCF) 和 gRPC 的最简单服务类型，因此，这是一个很好的起点。</span><span class="sxs-lookup"><span data-stu-id="bffee-105">These services are the simplest service types in both Windows Communication Foundation (WCF) and gRPC, so it's an excellent place to start.</span></span> <span data-ttu-id="bffee-106">迁移服务后，你将了解如何从同一文件生成客户端库， `.proto` 以便从 .net 客户端应用程序使用该服务。</span><span class="sxs-lookup"><span data-stu-id="bffee-106">After migrating the service, you'll learn how to generate a client library from the same `.proto` file to consume the service from a .NET client application.</span></span>

## <a name="the-wcf-solution"></a><span data-ttu-id="bffee-107">WCF 解决方案</span><span class="sxs-lookup"><span data-stu-id="bffee-107">The WCF solution</span></span>

<span data-ttu-id="bffee-108">[PortfoliosSample 解决方案](https://github.com/dotnet-architecture/grpc-for-wcf-developers/tree/master/PortfoliosSample/wcf/TraderSys)包括一个简单的请求-答复项目组合服务，可下载给定交易的单个项目组合或所有包。</span><span class="sxs-lookup"><span data-stu-id="bffee-108">The [PortfoliosSample solution](https://github.com/dotnet-architecture/grpc-for-wcf-developers/tree/master/PortfoliosSample/wcf/TraderSys) includes a simple request-reply Portfolio service to download either a single portfolio or all portfolios for a given trader.</span></span> <span data-ttu-id="bffee-109">服务在具有属性的接口中定义 `IPortfolioService` `ServiceContract` ：</span><span class="sxs-lookup"><span data-stu-id="bffee-109">The service is defined in the interface `IPortfolioService` with a `ServiceContract` attribute:</span></span>

```csharp
[ServiceContract]
public interface IPortfolioService
{
    [OperationContract]
    Task<Portfolio> Get(Guid traderId, int portfolioId);

    [OperationContract]
    Task<List<Portfolio>> GetAll(Guid traderId);
}
```

<span data-ttu-id="bffee-110">该 `Portfolio` 模型是一个用 [DataContract](xref:System.Runtime.Serialization.DataContractAttribute) 标记的简单 c # 类，其中包含 `PortfolioItem` 对象的列表。</span><span class="sxs-lookup"><span data-stu-id="bffee-110">The `Portfolio` model is a simple C# class marked with [DataContract](xref:System.Runtime.Serialization.DataContractAttribute) and including a list of `PortfolioItem` objects.</span></span> <span data-ttu-id="bffee-111">这些模型是在项目中定义的， `TraderSys.PortfolioData` 以及一个表示数据访问抽象的存储库类。</span><span class="sxs-lookup"><span data-stu-id="bffee-111">These models are defined in the `TraderSys.PortfolioData` project along with a repository class that represents a data access abstraction.</span></span>

```csharp
[DataContract]
public class Portfolio
{
    [DataMember]
    public int Id { get; set; }

    [DataMember]
    public Guid TraderId { get; set; }

    [DataMember]
    public List<PortfolioItem> Items { get; set; }
}

[DataContract]
public class PortfolioItem
{
    [DataMember]
    public int Id { get; set; }

    [DataMember]
    public int ShareId { get; set; }

    [DataMember]
    public int Holding { get; set; }

    [DataMember]
    public decimal Cost { get; set; }
}
```

<span data-ttu-id="bffee-112">`ServiceContract`实现使用由返回类型实例的依赖项注入提供的存储库类 `DataContract` ：</span><span class="sxs-lookup"><span data-stu-id="bffee-112">The `ServiceContract` implementation uses a repository class provided via dependency injection that returns instances of the `DataContract` types:</span></span>

```csharp
public class PortfolioService : IPortfolioService
{
    private readonly IPortfolioRepository _repository;

    public PortfolioService(IPortfolioRepository repository)
    {
        _repository = repository;
    }

    public async Task<Portfolio> Get(Guid traderId, int portfolioId)
    {
        return await _repository.GetAsync(traderId, portfolioId);
    }

    public async Task<List<Portfolio>> GetAll(Guid traderId)
    {
        return await _repository.GetAllAsync(traderId);
    }
}
```

## <a name="the-portfoliosproto-file"></a><span data-ttu-id="bffee-113">包 proto 文件</span><span class="sxs-lookup"><span data-stu-id="bffee-113">The portfolios.proto file</span></span>

<span data-ttu-id="bffee-114">如果按照上一部分中的说明进行操作，则应具有一个 gRPC 项目，其中包含如下所示的 `portfolios.proto` 文件：</span><span class="sxs-lookup"><span data-stu-id="bffee-114">If you followed the instructions in the previous section, you should have a gRPC project with a `portfolios.proto` file that looks like this:</span></span>

```protobuf
syntax = "proto3";

option csharp_namespace = "TraderSys.Portfolios.Protos";

package PortfolioServer;

service Portfolios {
  // RPCs will go here
}
```

<span data-ttu-id="bffee-115">第一步是将类迁移 `DataContract` 到它们的 Protobuf 等效项。</span><span class="sxs-lookup"><span data-stu-id="bffee-115">The first step is to migrate the `DataContract` classes to their Protobuf equivalents.</span></span>

## <a name="convert-the-datacontract-classes-to-grpc-messages"></a><span data-ttu-id="bffee-116">将 DataContract 类转换为 gRPC 消息</span><span class="sxs-lookup"><span data-stu-id="bffee-116">Convert the DataContract classes to gRPC messages</span></span>

<span data-ttu-id="bffee-117">`PortfolioItem`类将首先转换为 Protobuf 消息，因为 `Portfolio` 类依赖于它。</span><span class="sxs-lookup"><span data-stu-id="bffee-117">The `PortfolioItem` class will be converted to a Protobuf message first, because the `Portfolio` class depends on it.</span></span> <span data-ttu-id="bffee-118">类很简单，而三个属性直接映射到 gRPC 数据类型。</span><span class="sxs-lookup"><span data-stu-id="bffee-118">The class is simple, and three of the properties map directly to gRPC data types.</span></span> <span data-ttu-id="bffee-119">此 `Cost` 属性表示为购买的股票支付的价格，是一个 `decimal` 字段。</span><span class="sxs-lookup"><span data-stu-id="bffee-119">The `Cost` property, which represents the price paid for the shares at purchase, is a `decimal` field.</span></span> <span data-ttu-id="bffee-120">gRPC 仅支持 `float` 或 `double` 对于不适用于货币的实数。</span><span class="sxs-lookup"><span data-stu-id="bffee-120">gRPC supports only `float` or `double` for real numbers, which aren't suitable for currency.</span></span> <span data-ttu-id="bffee-121">由于共享价格的最小值仅有1美分，因此成本可表示为 1 `int32` 美分。</span><span class="sxs-lookup"><span data-stu-id="bffee-121">Because share prices vary by a minimum of one cent, the cost can be expressed as an `int32` of cents.</span></span>

> [!NOTE]
> <span data-ttu-id="bffee-122">请记住 `snake_case` 在文件中使用作为字段名称 `.proto` 。</span><span class="sxs-lookup"><span data-stu-id="bffee-122">Remember to use `snake_case` for field names in your `.proto` file.</span></span> <span data-ttu-id="bffee-123">C # 代码生成器会将它们转换为 `PascalCase` ，而其他语言的用户则感谢您遵从它们的不同编码标准。</span><span class="sxs-lookup"><span data-stu-id="bffee-123">The C# code generator will convert them to `PascalCase` for you, and users of other languages will thank you for respecting their different coding standards.</span></span>

```protobuf
message PortfolioItem {
    int32 id = 1;
    int32 share_id = 2;
    int32 holding = 3;
    int32 cost_cents = 4;
}
```

<span data-ttu-id="bffee-124">`Portfolio`类稍微复杂一些。</span><span class="sxs-lookup"><span data-stu-id="bffee-124">The `Portfolio` class is a little more complicated.</span></span> <span data-ttu-id="bffee-125">在 WCF 代码中，开发人员使用的是 `Guid` `TraderId` 属性的，并且包含 `List<PortfolioItem>` 。</span><span class="sxs-lookup"><span data-stu-id="bffee-125">In the WCF code, the developer used a `Guid` for the `TraderId` property, and contains a `List<PortfolioItem>`.</span></span> <span data-ttu-id="bffee-126">在不具有第一类类型的 Protobuf 中 `UUID` ，你应将用作 `string` 字段的， `traderId` 并在自己的代码中对其进行分析。</span><span class="sxs-lookup"><span data-stu-id="bffee-126">In Protobuf, which doesn't have a first-class `UUID` type, you should use a `string` for the `traderId` field and parse it in your own code.</span></span> <span data-ttu-id="bffee-127">对于项列表，请 `repeated` 在字段上使用关键字。</span><span class="sxs-lookup"><span data-stu-id="bffee-127">For the list of items, use the `repeated` keyword on the field.</span></span>

```protobuf
message Portfolio {
    int32 id = 1;
    string trader_id = 2;
    repeated PortfolioItem items = 3;
}
```

<span data-ttu-id="bffee-128">现在，你已有了数据消息，可以声明服务 RPC 终结点了。</span><span class="sxs-lookup"><span data-stu-id="bffee-128">Now that you have the data messages, you can declare the service RPC endpoints.</span></span>

## <a name="convert-servicecontract-to-a-grpc-service"></a><span data-ttu-id="bffee-129">将 ServiceContract 转换为 gRPC 服务</span><span class="sxs-lookup"><span data-stu-id="bffee-129">Convert ServiceContract to a gRPC service</span></span>

<span data-ttu-id="bffee-130">WCF `Get` 方法使用两个参数： `Guid traderId` 和 `int portfolioId` 。</span><span class="sxs-lookup"><span data-stu-id="bffee-130">The WCF `Get` method takes two parameters: `Guid traderId` and `int portfolioId`.</span></span> <span data-ttu-id="bffee-131">gRPC 服务方法只需要一个参数，因此需要创建一条消息来保存这两个值。</span><span class="sxs-lookup"><span data-stu-id="bffee-131">gRPC service methods can take only a single parameter, so you need to create a message to hold the two values.</span></span> <span data-ttu-id="bffee-132">常见的做法是将这些请求对象命名为与方法后跟后缀的名称相同 `Request` 。</span><span class="sxs-lookup"><span data-stu-id="bffee-132">It's common practice to name these request objects with the same name as the method followed by the suffix `Request`.</span></span> <span data-ttu-id="bffee-133">同样， `string` 将用于 `traderId` 字段而不是 `Guid` 。</span><span class="sxs-lookup"><span data-stu-id="bffee-133">Again, `string` is being used for the `traderId` field instead of `Guid`.</span></span>

<span data-ttu-id="bffee-134">该服务只是直接返回 `Portfolio` 消息，但这可能会影响将来的向后兼容性。</span><span class="sxs-lookup"><span data-stu-id="bffee-134">The service could just return a `Portfolio` message directly, but again, this could affect backward compatibility in the future.</span></span> <span data-ttu-id="bffee-135">最好为 `Request` `Response` 服务中的每个方法定义单独的和消息，即使其中许多方法现在都是相同的。</span><span class="sxs-lookup"><span data-stu-id="bffee-135">It's a good practice to define separate `Request` and `Response` messages for every method in a service, even if many of them are the same right now.</span></span> <span data-ttu-id="bffee-136">因此，请 `GetResponse` 使用单个字段声明一条消息 `Portfolio` 。</span><span class="sxs-lookup"><span data-stu-id="bffee-136">So declare a `GetResponse` message with a single `Portfolio` field.</span></span>

<span data-ttu-id="bffee-137">此示例显示了 gRPC 服务方法的声明以及 `GetRequest` 以下消息：</span><span class="sxs-lookup"><span data-stu-id="bffee-137">This example shows the declaration of the gRPC service method with the `GetRequest` message:</span></span>

```protobuf
message GetRequest {
    string trader_id = 1;
    int32 portfolio_id = 2;
}

message GetResponse {
    Portfolio portfolio = 1;
}

service Portfolios {
    rpc Get(GetRequest) returns (GetResponse);
}
```

<span data-ttu-id="bffee-138">WCF `GetAll` 方法仅采用单个参数， `traderId` 因此，可能看起来可以指定 `string` 作为参数类型。</span><span class="sxs-lookup"><span data-stu-id="bffee-138">The WCF `GetAll` method takes only a single parameter, `traderId`, so it might seem that you could specify `string` as the parameter type.</span></span> <span data-ttu-id="bffee-139">但 gRPC 要求使用定义的消息类型。</span><span class="sxs-lookup"><span data-stu-id="bffee-139">But gRPC requires a defined message type.</span></span> <span data-ttu-id="bffee-140">此要求可帮助强制执行将自定义消息用于所有输入和输出的操作，以便将来能够向后兼容。</span><span class="sxs-lookup"><span data-stu-id="bffee-140">This requirement helps to enforce the practice of using custom messages for all inputs and outputs, for future backward compatibility.</span></span>

<span data-ttu-id="bffee-141">WCF 方法还返回 `List<Portfolio>` ，但出于相同原因，它不允许简单参数类型，gRPC 不允许 `repeated Portfolio` 作为返回类型。</span><span class="sxs-lookup"><span data-stu-id="bffee-141">The WCF method also returns a `List<Portfolio>`, but for the same reason it doesn't allow simple parameter types, gRPC won't allow `repeated Portfolio` as a return type.</span></span> <span data-ttu-id="bffee-142">而是创建一个 `GetAllResponse` 类型来包装列表。</span><span class="sxs-lookup"><span data-stu-id="bffee-142">Instead, create a `GetAllResponse` type to wrap the list.</span></span>

> [!WARNING]
> <span data-ttu-id="bffee-143">您可能想要创建一个 `PortfolioList` 或多个类似的消息，并在多个服务方法中使用它，但您应该不能做到这一点。</span><span class="sxs-lookup"><span data-stu-id="bffee-143">You might be tempted to create a `PortfolioList` message or something similar and use it across multiple service methods, but you should resist this temptation.</span></span> <span data-ttu-id="bffee-144">不可能知道如何改进服务的各种方法，使其消息保持特定和明确的隔离。</span><span class="sxs-lookup"><span data-stu-id="bffee-144">It's impossible to know how the various methods on a service will evolve, so keep their messages specific and cleanly separated.</span></span>

```protobuf
message GetAllRequest {
    string trader_id = 1;
}

message PortfolioList {
    repeated Portfolio portfolios = 1;
}

service Portfolios {
    rpc Get(GetRequest) returns (Portfolio);
    rpc GetAll(GetAllRequest) returns (GetAllResponse);
}
```

<span data-ttu-id="bffee-145">如果你使用这些更改保存你的项目，则 gRPC 生成目标将在后台运行并生成所有 Protobuf 消息类型以及可继承以实现该服务的基类。</span><span class="sxs-lookup"><span data-stu-id="bffee-145">If you save your project with these changes, the gRPC build target will run in the background and generate all the Protobuf message types and a base class that you can inherit to implement the service.</span></span>

<span data-ttu-id="bffee-146">打开 `Services/GreeterService.cs` 类并删除示例代码。</span><span class="sxs-lookup"><span data-stu-id="bffee-146">Open the `Services/GreeterService.cs` class and delete the example code.</span></span> <span data-ttu-id="bffee-147">现在，你可以添加项目组合服务实现。</span><span class="sxs-lookup"><span data-stu-id="bffee-147">Now you can add the Portfolio service implementation.</span></span> <span data-ttu-id="bffee-148">生成的基类将位于 `Protos` 命名空间中，并以嵌套类的形式生成。</span><span class="sxs-lookup"><span data-stu-id="bffee-148">The generated base class will be in the `Protos` namespace and is generated as a nested class.</span></span> <span data-ttu-id="bffee-149">gRPC 创建一个静态类，该静态类的名称与该文件中的服务的名称相同， `.proto` 并在该静态类内创建一个具有后缀的基类 `Base` ，因此，基类型的完整标识符为 `TraderSys.Portfolios.Protos.Portfolios.PortfoliosBase` 。</span><span class="sxs-lookup"><span data-stu-id="bffee-149">gRPC creates a static class with the same name as the service in the `.proto` file and a base class with the suffix `Base` inside that static class, so the full identifier for the base type is `TraderSys.Portfolios.Protos.Portfolios.PortfoliosBase`.</span></span>

```csharp
namespace TraderSys.Portfolios.Services
{
    public class PortfolioService : Protos.Portfolios.PortfoliosBase
    {
    }
}
```

<span data-ttu-id="bffee-150">基类声明 `virtual` 和的方法， `Get` `GetAll` 这些方法可重写以实现服务。</span><span class="sxs-lookup"><span data-stu-id="bffee-150">The base class declares `virtual` methods for `Get` and `GetAll` that can be overridden to implement the service.</span></span> <span data-ttu-id="bffee-151">这些方法不是 `virtual` `abstract` 这样，因此，如果未实现这些方法，服务可以返回显式 gRPC `Unimplemented` 状态代码，就像您可以 `NotImplementedException` 在常规 c # 代码中引发。</span><span class="sxs-lookup"><span data-stu-id="bffee-151">The methods are `virtual` rather than `abstract` so that if you don't implement them, the service can return an explicit gRPC `Unimplemented` status code, much like you might throw a `NotImplementedException` in regular C# code.</span></span>

<span data-ttu-id="bffee-152">ASP.NET Core 中所有 gRPC 一元服务方法的签名都是一致的。</span><span class="sxs-lookup"><span data-stu-id="bffee-152">The signature for all gRPC unary service methods in ASP.NET Core is consistent.</span></span> <span data-ttu-id="bffee-153">有两个参数：第一个参数是在文件中声明的消息类型 `.proto` ，第二个参数的 `ServerCallContext` 工作方式类似于 `HttpContext` from ASP.NET Core。</span><span class="sxs-lookup"><span data-stu-id="bffee-153">There are two parameters: the first is the message type declared in the `.proto` file, and the second is a `ServerCallContext` that works similarly to the `HttpContext` from ASP.NET Core.</span></span> <span data-ttu-id="bffee-154">事实上，在类上有一个名为的扩展方法， `GetHttpContext` `ServerCallContext` 您可以使用它来获取基础 `HttpContext` ，不过您不需要经常使用它。</span><span class="sxs-lookup"><span data-stu-id="bffee-154">In fact, there's an extension method called `GetHttpContext` on the `ServerCallContext` class that you can use to get the underlying `HttpContext`, although you shouldn't need to use it often.</span></span> <span data-ttu-id="bffee-155">本章稍后将对此进行 `ServerCallContext` 介绍，并在讨论身份验证一章中介绍。</span><span class="sxs-lookup"><span data-stu-id="bffee-155">We'll take a look at `ServerCallContext` later in this chapter, and also in the chapter that discusses authentication.</span></span>

<span data-ttu-id="bffee-156">此方法的返回类型为 `Task<T>` ，其中 `T` 是响应消息类型。</span><span class="sxs-lookup"><span data-stu-id="bffee-156">The method's return type is a `Task<T>`, where `T` is the response message type.</span></span> <span data-ttu-id="bffee-157">所有 gRPC 服务方法都是异步的。</span><span class="sxs-lookup"><span data-stu-id="bffee-157">All gRPC service methods are asynchronous.</span></span>

## <a name="migrate-the-portfoliodata-library-to-net"></a><span data-ttu-id="bffee-158">将 PortfolioData 库迁移到 .NET</span><span class="sxs-lookup"><span data-stu-id="bffee-158">Migrate the PortfolioData library to .NET</span></span>

<span data-ttu-id="bffee-159">此时，项目需要 WCF 解决方案的类库中包含的项目组合存储库和模型 `TraderSys.PortfolioData` 。</span><span class="sxs-lookup"><span data-stu-id="bffee-159">At this point, the project needs the Portfolio repository and models contained in the `TraderSys.PortfolioData` class library in the WCF solution.</span></span> <span data-ttu-id="bffee-160">最简单的方法是通过使用 Visual Studio " **新建项目** " 对话框和 "类库" ( .NET Standard) "模板，或从命令行使用 .NET Core CLI 来创建新的类库，从包含该文件的目录运行以下命令 `TraderSys.sln` ：</span><span class="sxs-lookup"><span data-stu-id="bffee-160">The easiest way to bring them across is to create a new class library by using either the Visual Studio **New project** dialog box with the Class Library (.NET Standard) template, or from the command line by using the .NET Core CLI, running these commands from the directory that contains the `TraderSys.sln` file:</span></span>

```dotnetcli
dotnet new classlib -o src/TraderSys.PortfolioData
dotnet sln add src/TraderSys.PortfolioData
```

<span data-ttu-id="bffee-161">创建库并将其添加到解决方案后，请删除生成的文件， `Class1.cs` 并将文件从 WCF 解决方案的库复制到新的类库文件夹，同时保留文件夹结构：</span><span class="sxs-lookup"><span data-stu-id="bffee-161">After you've created the library and added it to the solution, delete the generated `Class1.cs` file and copy the files from the WCF solution's library into the new class library's folder, keeping the folder structure:</span></span>

```
Models
  Portfolio.cs
  PortfolioItem.cs
IPortfolioRepository.cs
PortfolioRepository.cs
```

<span data-ttu-id="bffee-162">SDK 样式的 .NET 项目会自动 `.cs` 将所有文件包含在其自己的目录中，因此无需将其显式添加到项目。</span><span class="sxs-lookup"><span data-stu-id="bffee-162">SDK-style .NET projects automatically include any `.cs` files in or under their own directory, so you don't need to explicitly add them to the project.</span></span> <span data-ttu-id="bffee-163">剩下的唯一步骤是 `DataContract` `DataMember` 从和类中删除和属性 `Portfolio` ， `PortfolioItem` 使其成为普通的旧 c # 类：</span><span class="sxs-lookup"><span data-stu-id="bffee-163">The only step remaining is to remove the `DataContract` and `DataMember` attributes from the `Portfolio` and `PortfolioItem` classes so they're plain old C# classes:</span></span>

```csharp
public class Portfolio
{
    public int Id { get; set; }
    public Guid TraderId { get; set; }
    public List<PortfolioItem> Items { get; set; }
}

public class PortfolioItem
{
    public int Id { get; set; }
    public int ShareId { get; set; }
    public int Holding { get; set; }
    public decimal Cost { get; set; }
}
```

## <a name="use-aspnet-core-dependency-injection"></a><span data-ttu-id="bffee-164">使用 ASP.NET Core 依赖关系注入</span><span class="sxs-lookup"><span data-stu-id="bffee-164">Use ASP.NET Core dependency injection</span></span>

<span data-ttu-id="bffee-165">现在，可以将对此库的引用添加到 gRPC 应用程序项目，并 `PortfolioRepository` 在 gRPC 服务实现中使用依赖关系注入来使用该类。</span><span class="sxs-lookup"><span data-stu-id="bffee-165">Now you can add a reference to this library to the gRPC application project and consume the `PortfolioRepository` class by using dependency injection in the gRPC service implementation.</span></span> <span data-ttu-id="bffee-166">在 WCF 应用程序中，依赖关系注入由 Autofac IoC 容器提供。</span><span class="sxs-lookup"><span data-stu-id="bffee-166">In the WCF application, dependency injection was provided by the Autofac IoC container.</span></span> <span data-ttu-id="bffee-167">ASP.NET Core 在中具有依赖关系注入融入。</span><span class="sxs-lookup"><span data-stu-id="bffee-167">ASP.NET Core has dependency injection baked in.</span></span> <span data-ttu-id="bffee-168">可以在类的方法中注册存储库 `ConfigureServices` `Startup` ：</span><span class="sxs-lookup"><span data-stu-id="bffee-168">You can register the repository in the `ConfigureServices` method in the `Startup` class:</span></span>

```csharp
public class Startup
{
    public void ConfigureServices(IServiceCollection services)
    {
        // Register the repository class as a scoped service (instance per request)
        services.AddScoped<IPortfolioRepository, PortfolioRepository>();

        services.AddGrpc();
    }

    // ...
}
```

<span data-ttu-id="bffee-169">`IPortfolioRepository`现在可以将实现指定为类中的构造函数参数 `PortfolioService` ，如下所示：</span><span class="sxs-lookup"><span data-stu-id="bffee-169">The `IPortfolioRepository` implementation can now be specified as a constructor parameter in the `PortfolioService` class, as follows:</span></span>

```csharp
public class PortfolioService : Protos.Portfolios.PortfoliosBase
{
    private readonly IPortfolioRepository _repository;

    public PortfolioService(IPortfolioRepository repository)
    {
        _repository = repository;
    }
}
```

## <a name="implement-the-grpc-service"></a><span data-ttu-id="bffee-170">实现 gRPC 服务</span><span class="sxs-lookup"><span data-stu-id="bffee-170">Implement the gRPC service</span></span>

<span data-ttu-id="bffee-171">现在您已在文件中声明了您的消息和服务 `portfolios.proto` ，您必须在类中实现 `PortfolioService` 从 gRPC 生成的类继承的服务方法 `Portfolios.PortfoliosBase` 。</span><span class="sxs-lookup"><span data-stu-id="bffee-171">Now that you've declared your messages and your service in the `portfolios.proto` file, you have to implement the service methods in the `PortfolioService` class that inherits from the gRPC-generated `Portfolios.PortfoliosBase` class.</span></span> <span data-ttu-id="bffee-172">方法 `virtual` 在基类中声明为。</span><span class="sxs-lookup"><span data-stu-id="bffee-172">The methods are declared as `virtual` in the base class.</span></span> <span data-ttu-id="bffee-173">如果不重写这些值，则默认情况下，它们将返回 "未实现" 状态代码 gRPC。</span><span class="sxs-lookup"><span data-stu-id="bffee-173">If you don't override them, they'll return a gRPC "Not Implemented" status code by default.</span></span>

<span data-ttu-id="bffee-174">首先实现 `Get` 方法。</span><span class="sxs-lookup"><span data-stu-id="bffee-174">Start by implementing the `Get` method.</span></span> <span data-ttu-id="bffee-175">默认替代如下例所示：</span><span class="sxs-lookup"><span data-stu-id="bffee-175">The default override looks like this example:</span></span>

```csharp
public override Task<GetResponse> Get(GetRequest request, ServerCallContext context)
{
    return base.Get(request, context);
}
```

<span data-ttu-id="bffee-176">第一个问题是 `request.TraderId` 字符串，而服务需要 `Guid` 。</span><span class="sxs-lookup"><span data-stu-id="bffee-176">The first problem is that `request.TraderId` is a string, and the service requires a `Guid`.</span></span> <span data-ttu-id="bffee-177">即使字符串的预期格式为 `UUID` ，代码也必须处理调用方发送了无效值并做出相应响应的可能性。</span><span class="sxs-lookup"><span data-stu-id="bffee-177">Even though the expected format for the string is `UUID`, the code has to deal with the possibility that a caller has sent an invalid value and respond appropriately.</span></span> <span data-ttu-id="bffee-178">服务可以通过引发来响应错误 `RpcException` ，并使用标准 `InvalidArgument` 状态代码来表示问题：</span><span class="sxs-lookup"><span data-stu-id="bffee-178">The service can respond with errors by throwing an `RpcException` and use the standard `InvalidArgument` status code to express the problem:</span></span>

```csharp
public override Task<GetResponse> Get(GetRequest request, ServerCallContext context)
{
    if (!Guid.TryParse(request.TraderId, out var traderId))
    {
        throw new RpcException(new Status(StatusCode.InvalidArgument, "traderId must be a UUID"));
    }

    return base.Get(request, context);
}
```

<span data-ttu-id="bffee-179">`Guid`为提供合适的值后 `traderId` ，你可以使用存储库来检索组合并将其返回到客户端：</span><span class="sxs-lookup"><span data-stu-id="bffee-179">After there's a proper `Guid` value for `traderId`, you can use the repository to retrieve the Portfolio and return it to the client:</span></span>

```csharp
    var response = new GetResponse
    {
        Portfolio = await _repository.GetAsync(request.TraderId, request.PortfolioId)
    };
```

### <a name="map-internal-models-to-grpc-messages"></a><span data-ttu-id="bffee-180">将内部模型映射到 gRPC 消息</span><span class="sxs-lookup"><span data-stu-id="bffee-180">Map internal models to gRPC messages</span></span>

<span data-ttu-id="bffee-181">前面的代码实际上不起作用，因为存储库返回自己的 POCO 模型 `Portfolio` ，但 gRPC 需要其自己的 Protobuf 消息 `Portfolio` 。</span><span class="sxs-lookup"><span data-stu-id="bffee-181">The previous code doesn't actually work because the repository is returning its own POCO model `Portfolio`, but gRPC needs its own Protobuf message `Portfolio`.</span></span> <span data-ttu-id="bffee-182">与将实体框架类型映射到数据传输类型一样，最佳解决方案是在两者之间提供转换。</span><span class="sxs-lookup"><span data-stu-id="bffee-182">As when you map Entity Framework types to data transfer types, the best solution is to provide a conversion between the two.</span></span> <span data-ttu-id="bffee-183">放置此转换的代码的好地方是在 Protobuf 生成的类中，该类被声明为类， `partial` 以便能够进行扩展：</span><span class="sxs-lookup"><span data-stu-id="bffee-183">A good place to put the code for this conversion is in the Protobuf-generated class, which is declared as a `partial` class so it can be extended:</span></span>

```csharp
namespace TraderSys.Portfolios.Protos
{
    public partial class PortfolioItem
    {
        public static PortfolioItem FromRepositoryModel(PortfolioData.Models.PortfolioItem source)
        {
            if (source is null) return null;

            return new PortfolioItem
            {
                Id = source.Id,
                ShareId = source.ShareId,
                Holding = source.Holding,
                CostCents = (int)(source.Cost * 100)
            };
        }
    }

    public partial class Portfolio
    {
        public static Portfolio FromRepositoryModel(PortfolioData.Models.Portfolio source)
        {
            if (source is null) return null;

            var target = new Portfolio
            {
                Id = source.Id,
                TraderId = source.TraderId.ToString(),
            };

            target.Items.AddRange(source.Items.Select(PortfolioItem.FromRepositoryModel));

            return target;
        }
    }
}
```

> [!NOTE]
> <span data-ttu-id="bffee-184">您可以使用类似[AutoMapper](https://automapper.org/)的库来处理从内部模型类到 Protobuf 类型的这种转换，前提是您配置了类似于或的更低级别类型转换 `string` / `Guid` `decimal` / `double` 和列表映射。</span><span class="sxs-lookup"><span data-stu-id="bffee-184">You could use a library like [AutoMapper](https://automapper.org/) to handle this conversion from internal model classes to Protobuf types, as long as you configure the lower-level type conversions like `string`/`Guid` or `decimal`/`double` and the list mapping.</span></span>

<span data-ttu-id="bffee-185">现在，你已准备好转换代码，接下来可以完成 `Get` 方法实现：</span><span class="sxs-lookup"><span data-stu-id="bffee-185">Now that you have the conversion code in place, you can complete the `Get` method implementation:</span></span>

```csharp
public override async Task<GetResponse> Get(GetRequest request, ServerCallContext context)
{
    if (!Guid.TryParse(request.TraderId, out var traderId))
    {
        throw new RpcException(new Status(StatusCode.InvalidArgument, "traderId must be a UUID"));
    }

    var portfolio = await _repository.GetAsync(traderId, request.PortfolioId);

    return new GetResponse
    {
        Portfolio = Portfolio.FromRepositoryModel(portfolio)
    };
}

```

<span data-ttu-id="bffee-186">方法的实现 `GetAll` 类似。</span><span class="sxs-lookup"><span data-stu-id="bffee-186">The implementation of the `GetAll` method is similar.</span></span> <span data-ttu-id="bffee-187">请注意， `repeated` Protobuf 消息上的字段生成为 `readonly` 类型的属性 `RepeatedField<T>` ，因此您必须通过使用方法向其中添加项 `AddRange` ，如本示例所示：</span><span class="sxs-lookup"><span data-stu-id="bffee-187">Note that the `repeated` fields on Protobuf messages are generated as `readonly` properties of type `RepeatedField<T>`, so you have to add items to them by using the `AddRange` method, like in this example:</span></span>

```csharp
public override async Task<GetAllResponse> GetAll(GetAllRequest request, ServerCallContext context)
{
    if (!Guid.TryParse(request.TraderId, out var traderId))
    {
        throw new RpcException(new Status(StatusCode.InvalidArgument, "traderId must be a UUID"));
    }

    var portfolios = await _repository.GetAllAsync(traderId);

    var response = new GetAllResponse();
    response.Portfolios.AddRange(portfolios.Select(Portfolio.FromRepositoryModel));

    return response;
}
```

<span data-ttu-id="bffee-188">已成功将 WCF 请求-答复服务迁移到 gRPC，我们来看看如何从该文件创建客户端 `.proto` 。</span><span class="sxs-lookup"><span data-stu-id="bffee-188">Having successfully migrated the WCF request-reply service to gRPC, let's look at creating a client for it from the `.proto` file.</span></span>

## <a name="generate-client-code"></a><span data-ttu-id="bffee-189">生成客户端代码</span><span class="sxs-lookup"><span data-stu-id="bffee-189">Generate client code</span></span>

<span data-ttu-id="bffee-190">在同一解决方案中创建 .NET Standard 类库，以包含客户端。</span><span class="sxs-lookup"><span data-stu-id="bffee-190">Create a .NET Standard class library in the same solution to contain the client.</span></span> <span data-ttu-id="bffee-191">这主要是创建客户端代码的示例，但你可以使用 NuGet 打包此类库，并将其分发到供其他 .NET 团队使用的内部存储库中。</span><span class="sxs-lookup"><span data-stu-id="bffee-191">This is primarily an example of creating client code, but you could package such a library by using NuGet and distribute it on an internal repository for other .NET teams to consume.</span></span> <span data-ttu-id="bffee-192">继续并向解决方案中添加一个名为的新 .NET Standard 类库 `TraderSys.Portfolios.Client` ，然后删除该 `Class1.cs` 文件。</span><span class="sxs-lookup"><span data-stu-id="bffee-192">Go ahead and add a new .NET Standard class library called `TraderSys.Portfolios.Client` to the solution and delete the `Class1.cs` file.</span></span>

> [!CAUTION]
> <span data-ttu-id="bffee-193">[Grpc](https://www.nuget.org/packages/Grpc.Net.Client) NuGet 包需要 .net Core 3.0 或更高版本 (或其他 .NET Standard 2.1 兼容的运行时) 。</span><span class="sxs-lookup"><span data-stu-id="bffee-193">The [Grpc.Net.Client](https://www.nuget.org/packages/Grpc.Net.Client) NuGet package requires .NET Core 3.0 or later (or another .NET Standard 2.1-compliant runtime).</span></span> <span data-ttu-id="bffee-194">[Grpc](https://www.nuget.org/packages/Grpc.Core) NuGet 包支持早期版本的 .NET FRAMEWORK 和 .net Core。</span><span class="sxs-lookup"><span data-stu-id="bffee-194">Earlier versions of .NET Framework and .NET Core are supported by the [Grpc.Core](https://www.nuget.org/packages/Grpc.Core) NuGet package.</span></span>

<span data-ttu-id="bffee-195">在 Visual Studio 2019 中，可以通过类似于在 Visual Studio 早期版本中添加对 WCF 项目的服务引用的方式来添加对 gRPC 服务的引用。</span><span class="sxs-lookup"><span data-stu-id="bffee-195">In Visual Studio 2019, you can add references to gRPC services in a way that's similar to how you'd add service references to WCF projects in earlier versions of Visual Studio.</span></span> <span data-ttu-id="bffee-196">现在，服务引用和连接服务都是在同一个 UI 下进行管理。</span><span class="sxs-lookup"><span data-stu-id="bffee-196">Service references and connected services are all managed under the same UI now.</span></span> <span data-ttu-id="bffee-197">可以通过在解决方案资源管理器中右键单击项目中的 " **依赖项** " 节点 `TraderSys.Portfolios.Client` ，然后选择 " **添加连接的服务**" 来访问该 UI。</span><span class="sxs-lookup"><span data-stu-id="bffee-197">You can access the UI by right-clicking the **Dependencies** node in the `TraderSys.Portfolios.Client` project in Solution Explorer and selecting **Add Connected Service**.</span></span> <span data-ttu-id="bffee-198">在出现的工具窗口中，选择 " **服务引用** " 部分，然后选择 " **添加新的 gRPC 服务引用**"：</span><span class="sxs-lookup"><span data-stu-id="bffee-198">In the tool window that appears, select the **Service References** section and then select **Add new gRPC service reference**:</span></span>

![Visual Studio 2019 中的连接的服务 UI](media/migrate-request-reply/add-connected-service.png)

<span data-ttu-id="bffee-200">浏览到 `portfolios.proto` 项目中的文件 `TraderSys.Portfolios` ，将 " **客户端** " 下的 " **选择要生成的类的类型**" 下，然后选择 **"确定"**：</span><span class="sxs-lookup"><span data-stu-id="bffee-200">Browse to the `portfolios.proto` file in the `TraderSys.Portfolios` project, leave **Client** under **Select the type of class to be generated**, and then select **OK**:</span></span>

![Visual Studio 2019 中的 "添加新的 gRPC 服务引用" 对话框](media/migrate-request-reply/add-new-grpc-service-reference.png)

> [!TIP]
> <span data-ttu-id="bffee-202">请注意，此对话框还提供了 "URL" 字段。</span><span class="sxs-lookup"><span data-stu-id="bffee-202">Notice that this dialog box also provides a URL field.</span></span> <span data-ttu-id="bffee-203">如果你的组织维护可通过 web 访问的 `.proto` 文件目录，你只需通过设置此 URL 地址来创建客户端。</span><span class="sxs-lookup"><span data-stu-id="bffee-203">If your organization maintains a web-accessible directory of `.proto` files, you can create clients just by setting this URL address.</span></span>

<span data-ttu-id="bffee-204">当你使用 Visual Studio " **添加连接服务** " 功能时，该 `portfolios.proto` 文件将作为 *链接文件* 添加到类库项目，而不是复制到一起，因此对服务项目中的文件所做的更改将自动应用到客户端项目中。</span><span class="sxs-lookup"><span data-stu-id="bffee-204">When you use the Visual Studio **Add Connected Service** feature, the `portfolios.proto` file is added to the class library project as a *linked file* rather than copied, so changes to the file in the service project will automatically be applied in the client project.</span></span> <span data-ttu-id="bffee-205">`<Protobuf>`文件中的元素如下所 `csproj` 示：</span><span class="sxs-lookup"><span data-stu-id="bffee-205">The `<Protobuf>` element in the `csproj` file looks like this:</span></span>

```xml
<Protobuf Include="..\TraderSys.Portfolios\Protos\portfolios.proto" GrpcServices="Client">
  <Link>Protos\portfolios.proto</Link>
</Protobuf>
```

> [!TIP]
> <span data-ttu-id="bffee-206">如果未使用 Visual Studio 或想要从命令行运行，则可以使用 `dotnet-grpc` 全局工具来管理 .Net gRPC 项目中的 Protobuf 引用。</span><span class="sxs-lookup"><span data-stu-id="bffee-206">If you're not using Visual Studio or prefer to work from the command line, you can use the `dotnet-grpc` global tool to manage Protobuf references in a .NET gRPC project.</span></span> <span data-ttu-id="bffee-207">有关详细信息，请参阅[ `dotnet-grpc` 文档](/aspnet/core/grpc/dotnet-grpc)。</span><span class="sxs-lookup"><span data-stu-id="bffee-207">For more information, see the [`dotnet-grpc` documentation](/aspnet/core/grpc/dotnet-grpc).</span></span>

### <a name="use-the-portfolios-service-from-a-client-application"></a><span data-ttu-id="bffee-208">使用客户端应用程序中的 "包" 服务</span><span class="sxs-lookup"><span data-stu-id="bffee-208">Use the Portfolios service from a client application</span></span>

<span data-ttu-id="bffee-209">以下代码是如何在控制台应用程序中使用生成的客户端的简单示例。</span><span class="sxs-lookup"><span data-stu-id="bffee-209">The following code is a brief example of how to use the generated client in a console application.</span></span> <span data-ttu-id="bffee-210">本章末尾详细探讨了 gRPC 客户端代码。</span><span class="sxs-lookup"><span data-stu-id="bffee-210">A more detailed exploration of the gRPC client code is at the end of this chapter.</span></span>

```csharp
public class Program
{
    public async Task Main(string[] args)
    {
        GetResponse response;

        using (var channel = GrpcChannel.ForAddress("https://localhost:5001"))
        {
            var client = new Protos.Portfolios.PortfoliosClient(channel);

            response = await client.GetAsync(new GetRequest
            {
                TraderId = args[0],
                PortfolioId = int.Parse(args[1])
            });
        }

        foreach (var item in response.Portfolio.Items)
        {
            Console.WriteLine($"Holding {item.Holding} of Share ID {item.ShareId}.");
        }
    }
}
```

<span data-ttu-id="bffee-211">现在，已将基本 WCF 应用程序迁移到 ASP.NET Core gRPC 服务，并创建了客户端，以便从 .NET 应用程序使用该服务。</span><span class="sxs-lookup"><span data-stu-id="bffee-211">You've now migrated a basic WCF application to an ASP.NET Core gRPC service and created a client to consume the service from a .NET application.</span></span> <span data-ttu-id="bffee-212">下一节将介绍更多的双工服务。</span><span class="sxs-lookup"><span data-stu-id="bffee-212">The next section will cover the more involved duplex services.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="bffee-213">[上一页](create-project.md)
>[下一页](migrate-duplex-services.md)</span><span class="sxs-lookup"><span data-stu-id="bffee-213">[Previous](create-project.md)
[Next](migrate-duplex-services.md)</span></span>
